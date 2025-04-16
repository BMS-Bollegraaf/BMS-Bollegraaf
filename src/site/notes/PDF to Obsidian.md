---
{"dg-publish":true,"permalink":"/pdf-to-obsidian/","noteIcon":"lightbulb"}
---


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PDF to Markdown Converter</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js" integrity="sha512-q+4liFwdPC/NlU5laZN9RuQeQoelL7Jjgwj7StWFmUub+NZ7rBw8t3y7QdSWLDqA9+COxFq0/q9WbceZ/Y6GKg==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js" integrity="sha512-BbrZ76UNZq5BhH7LLiksJRwfJjI+VvDVp9fwdSVrRDJ544Ld7LGGzGmkyS0ZMH1Gy57Z4tv76hFkFajqYN4VVA==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>

    <style>
        body {
            font-family: sans-serif;
            line-height: 1.6;
            padding: 20px;
            max-width: 800px;
            margin: 0 auto;
            background-color: #f4f4f4;
        }
        .container {
            background-color: #fff;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        h1 {
            text-align: center;
            color: #333;
            margin-bottom: 20px;
        }
        label, button, input[type="file"] {
            display: block;
            margin-bottom: 15px;
        }
        input[type="file"] {
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            width: calc(100% - 22px); /* Adjust for padding */
        }
        button {
            padding: 12px 20px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1em;
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: #0056b3;
        }
        button:disabled {
            background-color: #cccccc;
            cursor: not-allowed;
        }
        #status {
            margin-top: 15px;
            font-weight: bold;
            min-height: 20px; /* Prevent layout shift */
        }
        #mdOutput {
            width: 100%;
            min-height: 300px;
            margin-top: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
            padding: 10px;
            font-family: monospace; /* Good for Markdown */
            box-sizing: border-box; /* Include padding in width */
        }
        .output-area {
            margin-top: 20px;
        }
        .note {
            font-size: 0.9em;
            color: #666;
            margin-top: 20px;
            border-left: 3px solid #ccc;
            padding-left: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>PDF to Markdown Converter</h1>
        <p>Select a PDF file to extract its text content into basic Markdown format. Best for simple text documents.</p>

        <label for="pdfInput">Choose PDF File:</label>
        <input type="file" id="pdfInput" accept=".pdf">

        <button id="convertButton" disabled>Convert to Markdown</button>

        <div id="status"></div>

        <div class="output-area">
            <label for="mdOutput">Markdown Output:</label>
            <textarea id="mdOutput" readonly placeholder="Markdown content will appear here..."></textarea>
            <button id="copyButton" disabled>Copy Markdown</button>
            <button id="downloadButton" disabled>Download .md File</button>
        </div>

         <div class="note">
            <strong>Note:</strong> This tool extracts text content. Complex formatting (tables, columns, lists, styles, images) may be lost or poorly represented. It works best with simple, text-based PDFs. Processing happens entirely in your browser; your file is not uploaded.
        </div>
    </div>

    <script>
        // Set worker source for pdf.js
        pdfjsLib.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js';

        const pdfInput = document.getElementById('pdfInput');
        const convertButton = document.getElementById('convertButton');
        const copyButton = document.getElementById('copyButton');
        const downloadButton = document.getElementById('downloadButton');
        const statusDiv = document.getElementById('status');
        const mdOutput = document.getElementById('mdOutput');

        let currentFile = null;
        let originalFileName = 'converted'; // Default filename base

        pdfInput.addEventListener('change', (event) => {
            currentFile = event.target.files[0];
            if (currentFile && currentFile.type === 'application/pdf') {
                convertButton.disabled = false;
                statusDiv.textContent = 'File selected. Ready to convert.';
                mdOutput.value = ''; // Clear previous output
                copyButton.disabled = true;
                downloadButton.disabled = true;
                originalFileName = currentFile.name.replace(/\.pdf$/i, ''); // Get filename without extension
            } else {
                currentFile = null;
                convertButton.disabled = true;
                statusDiv.textContent = 'Please select a valid PDF file.';
                mdOutput.value = '';
                copyButton.disabled = true;
                downloadButton.disabled = true;
            }
        });

        convertButton.addEventListener('click', async () => {
            if (!currentFile) {
                statusDiv.textContent = 'No file selected.';
                return;
            }

            statusDiv.textContent = 'Processing PDF... (This may take a moment)';
            convertButton.disabled = true;
            pdfInput.disabled = true; // Prevent changing file during processing
            mdOutput.value = ''; // Clear output area

            const reader = new FileReader();

            reader.onload = async (event) => {
                const pdfData = new Uint8Array(event.target.result);
                let fullText = '';

                try {
                    const pdf = await pdfjsLib.getDocument({ data: pdfData }).promise;
                    statusDiv.textContent = `Processing ${pdf.numPages} pages...`;

                    for (let i = 1; i <= pdf.numPages; i++) {
                        const page = await pdf.getPage(i);
                        const textContent = await page.getTextContent();

                        // Simple text extraction: join items with spaces, add double newline between blocks.
                        // This is a basic heuristic and won't perfectly capture structure.
                        let lastY = -1;
                        let pageText = '';
                        textContent.items.sort((a, b) => { // Try basic sort by Y then X
                             if (a.transform[5] < b.transform[5]) return 1;
                             if (a.transform[5] > b.transform[5]) return -1;
                             if (a.transform[4] < b.transform[4]) return -1;
                             if (a.transform[4] > b.transform[4]) return 1;
                             return 0;
                        });

                        textContent.items.forEach(item => {
                           // Add a double newline if there's a significant vertical gap (potential paragraph break)
                            if (lastY !== -1 && Math.abs(item.transform[5] - lastY) > item.height * 1.5) {
                                pageText += '\n\n';
                            } else if (lastY !== -1) {
                                // Add a space if items are on the same line but separated horizontally
                                pageText += ' ';
                            }
                            pageText += item.str;
                            lastY = item.transform[5]; // Y position
                        });

                        fullText += pageText + '\n\n---\n\n'; // Add separator between pages
                         statusDiv.textContent = `Processed page ${i}/${pdf.numPages}...`;
                    }

                    // Basic cleanup
                    fullText = fullText.replace(/(\n\n---\n\n)$/, ''); // Remove last page separator
                    fullText = fullText.replace(/ +\n/g, '\n'); // Trim trailing spaces on lines
                    fullText = fullText.replace(/\n{3,}/g, '\n\n'); // Collapse excessive newlines

                    mdOutput.value = fullText;
                    statusDiv.textContent = 'Conversion complete!';
                    copyButton.disabled = false;
                    downloadButton.disabled = false;

                } catch (error) {
                    console.error('Error processing PDF:', error);
                    statusDiv.textContent = `Error: ${error.message}`;
                    mdOutput.value = `Failed to process PDF. Error: ${error.message}`;
                    copyButton.disabled = true;
                    downloadButton.disabled = true;
                } finally {
                    // Re-enable controls whether success or failure
                     convertButton.disabled = false;
                     pdfInput.disabled = false;
                }
            };

            reader.onerror = () => {
                statusDiv.textContent = 'Error reading file.';
                console.error('FileReader error:', reader.error);
                convertButton.disabled = false;
                pdfInput.disabled = false;
            };

            reader.readAsArrayBuffer(currentFile);
        });

        copyButton.addEventListener('click', () => {
            if (mdOutput.value) {
                navigator.clipboard.writeText(mdOutput.value)
                    .then(() => {
                        statusDiv.textContent = 'Markdown copied to clipboard!';
                    })
                    .catch(err => {
                        statusDiv.textContent = 'Failed to copy text.';
                        console.error('Clipboard error:', err);
                    });
            }
        });

         downloadButton.addEventListener('click', () => {
            if (mdOutput.value) {
                const blob = new Blob([mdOutput.value], { type: 'text/markdown;charset=utf-8' });
                const url = URL.createObjectURL(blob);
                const a = document.createElement('a');
                a.href = url;
                a.download = `${originalFileName}.md`; // Use original base name + .md
                document.body.appendChild(a); // Append anchor to body (needed for Firefox)
                a.click();
                document.body.removeChild(a); // Clean up
                URL.revokeObjectURL(url); // Free up memory
                statusDiv.textContent = 'Markdown file download initiated.';
            }
        });

    </script>
</body>
</html>
