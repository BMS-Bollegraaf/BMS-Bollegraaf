---
{"dg-publish":true,"permalink":"/pdf-to-obsidian/","noteIcon":"lightbulb"}
---

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PDF to Obsidian Text Converter</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.11.338/pdf.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.11.338/pdf.worker.min.js"></script>

    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #2c2c2c; /* Dark background */
            color: #e0e0e0; /* Light text */
            line-height: 1.6;
            padding: 20px;
            margin: 0;
        }

        .container {
            max-width: 800px;
            margin: 20px auto;
            background-color: #3a3a3a; /* Slightly lighter container background */
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
        }

        h1 {
            color: #ffffff;
            text-align: center;
            margin-bottom: 30px;
            border-bottom: 1px solid #555;
            padding-bottom: 10px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #cccccc;
        }

        input[type="file"] {
            display: block;
            margin-bottom: 20px;
            padding: 10px;
            border: 1px solid #555;
            background-color: #444;
            color: #e0e0e0;
            border-radius: 4px;
            width: calc(100% - 22px); /* Account for padding and border */
        }

        button {
            background-color: #007bff;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.2s ease;
            margin-right: 10px;
        }

        button:hover {
            background-color: #0056b3;
        }

        button:disabled {
            background-color: #555;
            cursor: not-allowed;
        }

        #outputContainer {
            margin-top: 30px;
            border-top: 1px solid #555;
            padding-top: 20px;
        }

        h2 {
            color: #eeeeee;
            margin-bottom: 15px;
        }

        #outputText {
            width: 100%;
            height: 400px;
            background-color: #222; /* Darker background for text area */
            color: #e0e0e0;
            border: 1px solid #555;
            padding: 15px;
            box-sizing: border-box;
            white-space: pre-wrap; /* Preserve whitespace and wrap text */
            word-wrap: break-word; /* Break long words */
            font-family: Consolas, Monaco, "Andale Mono", "Ubuntu Mono", monospace; /* Monospace font for code/text */
            font-size: 14px;
            border-radius: 4px;
        }

        #downloadButton {
            margin-top: 15px;
            background-color: #28a745; /* Green for download */
        }
        #downloadButton:hover {
            background-color: #218838;
        }
        #downloadButton:disabled {
             background-color: #555;
             cursor: not-allowed;
        }

        .status {
            margin-top: 15px;
            font-style: italic;
            color: #aaa;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>PDF to Obsidian Text Converter</h1>

        <label for="pdfInput">Choose a PDF file:</label>
        <input type="file" id="pdfInput" accept=".pdf">

        <button id="convertButton">Convert PDF to Text</button>
        <span id="status" class="status"></span>

        <div id="outputContainer" style="display: none;">
            <h2>Extracted Text (Obsidian Ready)</h2>
            <p style="font-size: 0.9em; color: #aaa; margin-bottom: 15px;">
                This is the raw text extracted from the PDF. Paragraph breaks are generally preserved. You may need to refine Markdown formatting (like headings #, lists *, etc.) manually in Obsidian.
            </p>
            <textarea id="outputText" readonly></textarea>
            <button id="downloadButton" disabled>Download .txt</button>
            <span id="downloadStatus" class="status"></span>
        </div>
    </div>

    <script>
        // Set the worker source for pdf.js
        pdfjsLib.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.11.338/pdf.worker.min.js';

        const pdfInput = document.getElementById('pdfInput');
        const convertButton = document.getElementById('convertButton');
        const outputContainer = document.getElementById('outputContainer');
        const outputText = document.getElementById('outputText');
        const downloadButton = document.getElementById('downloadButton');
        const statusDiv = document.getElementById('status');
        const downloadStatusDiv = document.getElementById('downloadStatus');

        let originalFileName = 'converted_text'; // Default filename

        convertButton.addEventListener('click', handlePdfConversion);
        downloadButton.addEventListener('click', handleDownload);

        async function handlePdfConversion() {
            const file = pdfInput.files[0];
            if (!file) {
                statusDiv.textContent = 'Please select a PDF file first.';
                return;
            }
            if (file.type !== 'application/pdf') {
                statusDiv.textContent = 'Error: Selected file is not a PDF.';
                return;
            }

            originalFileName = file.name.replace(/\.pdf$/i, ''); // Store filename without extension
            statusDiv.textContent = 'Processing PDF... please wait.';
            convertButton.disabled = true;
            outputContainer.style.display = 'none';
            outputText.value = ''; // Clear previous output
            downloadButton.disabled = true;
            downloadStatusDiv.textContent = '';


            try {
                const arrayBuffer = await readFileAsArrayBuffer(file);
                const pdf = await pdfjsLib.getDocument({ data: arrayBuffer }).promise;
                let fullText = '';

                statusDiv.textContent = `Processing ${pdf.numPages} pages...`;

                for (let i = 1; i <= pdf.numPages; i++) {
                    const page = await pdf.getPage(i);
                    const textContent = await page.getTextContent();

                    // Join text items, attempting to preserve paragraph structure somewhat
                    // by adding double newlines between chunks. This is heuristic.
                    let lastY = -1;
                    let pageText = '';
                    textContent.items.sort((a, b) => { // Sort items by position (top-to-bottom, left-to-right)
                        if (a.transform[5] !== b.transform[5]) {
                            return b.transform[5] - a.transform[5]; // Y position (higher value is lower on page)
                        }
                        return a.transform[4] - b.transform[4]; // X position
                    });

                    textContent.items.forEach(item => {
                        if (lastY !== -1 && Math.abs(item.transform[5] - lastY) > (item.height * 1.5) ) { // Approximate line break detection
                           pageText += '\n\n';
                        } else if (lastY !== -1) {
                            pageText += ' '; // Add space between items on roughly the same line
                        }
                        pageText += item.str.trim();
                        lastY = item.transform[5];
                    });

                    fullText += pageText + '\n\n'; // Add double newline after each page's content
                    statusDiv.textContent = `Processed page ${i} of ${pdf.numPages}...`;
                }

                outputText.value = fullText.trim(); // Set the extracted text
                outputContainer.style.display = 'block'; // Show the output area
                downloadButton.disabled = false; // Enable download
                statusDiv.textContent = 'Conversion complete!';

            } catch (error) {
                console.error("Error processing PDF:", error);
                statusDiv.textContent = `Error: ${error.message || 'Could not process PDF.'}`;
                outputContainer.style.display = 'none';
            } finally {
                convertButton.disabled = false; // Re-enable convert button
            }
        }

        function readFileAsArrayBuffer(file) {
            return new Promise((resolve, reject) => {
                const reader = new FileReader();
                reader.onload = event => resolve(event.target.result);
                reader.onerror = error => reject(error);
                reader.readAsArrayBuffer(file);
            });
        }

        function handleDownload() {
            if (!outputText.value) {
                 downloadStatusDiv.textContent = 'No text to download.';
                return;
            }

            try {
                const blob = new Blob([outputText.value], { type: 'text/plain;charset=utf-8' });
                const url = URL.createObjectURL(blob);
                const link = document.createElement('a');
                link.href = url;
                link.download = `${originalFileName}.txt`; // Use original name + .txt
                document.body.appendChild(link); // Required for Firefox
                link.click();
                document.body.removeChild(link);
                URL.revokeObjectURL(url); // Clean up
                 downloadStatusDiv.textContent = `File "${originalFileName}.txt" download initiated.`;
            } catch (error) {
                 console.error("Error creating download link:", error);
                 downloadStatusDiv.textContent = 'Error creating download link.';
            }
        }

        // Add listener to clear status when a new file is selected
         pdfInput.addEventListener('change', () => {
            statusDiv.textContent = '';
            downloadStatusDiv.textContent = '';
            outputContainer.style.display = 'none';
            outputText.value = '';
            downloadButton.disabled = true;
             const file = pdfInput.files[0];
             if (file) {
                 statusDiv.textContent = `Selected: ${file.name}`;
             }
         });

    </script>

</body>
</html>
