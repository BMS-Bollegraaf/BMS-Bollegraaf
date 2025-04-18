---
{"dg-publish":true,"permalink":"/pdf-to-obsidian/","noteIcon":"lightbulb"}
---


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PDF to Markdown Converter for Obsidian</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f7f7f7;
        }
        h1 {
            color: #5C67DE;
            text-align: center;
            margin-bottom: 30px;
        }
        .container {
            background-color: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        #dropArea {
            border: 2px dashed #5C67DE;
            border-radius: 8px;
            padding: 40px 20px;
            text-align: center;
            margin-bottom: 20px;
            background-color: #f9f9ff;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        #dropArea:hover, #dropArea.highlight {
            background-color: #eeeeff;
        }
        #fileInput {
            display: none;
        }
        button {
            background-color: #5C67DE;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #4b55c7;
        }
        button:disabled {
            background-color: #b4b8e6;
            cursor: not-allowed;
        }
        #progressContainer {
            display: none;
            margin-top: 20px;
        }
        #progressBar {
            width: 100%;
            height: 20px;
            background-color: #e0e0e0;
            border-radius: 10px;
            overflow: hidden;
        }
        #progress {
            height: 100%;
            background-color: #5C67DE;
            width: 0%;
            transition: width 0.3s;
        }
        #options {
            margin: 20px 0;
            padding: 15px;
            background-color: #f0f0f7;
            border-radius: 8px;
        }
        .option {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
        }
        select, input[type="text"] {
            width: 100%;
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-sizing: border-box;
        }
        .checkbox-label {
            display: flex;
            align-items: center;
            font-weight: normal;
        }
        .checkbox-label input {
            margin-right: 8px;
        }
        #result {
            margin-top: 20px;
            display: none;
        }
        #mdContent {
            width: 100%;
            height: 300px;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-sizing: border-box;
            font-family: monospace;
            margin-bottom: 15px;
            white-space: pre-wrap;
        }
        .download-btn {
            background-color: #4CAF50;
        }
        .download-btn:hover {
            background-color: #45a049;
        }
        footer {
            margin-top: 30px;
            text-align: center;
            font-size: 14px;
            color: #777;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>PDF to Markdown Converter for Obsidian</h1>
        
        <div id="dropArea">
            <p>Drag & drop your PDF file here or click to select</p>
            <input type="file" id="fileInput" accept=".pdf" />
        </div>
        
        <div id="options">
            <h3>Conversion Options</h3>
            <div class="option">
                <label for="headingLevel">Top-level heading</label>
                <select id="headingLevel">
                    <option value="1"># Heading 1</option>
                    <option value="2" selected>## Heading 2</option>
                    <option value="3">### Heading 3</option>
                </select>
            </div>
            <div class="option">
                <label for="imageHandling">Image handling</label>
                <select id="imageHandling">
                    <option value="embed">Extract and embed (data URLs)</option>
                    <option value="extract">Extract to separate files</option>
                    <option value="skip" selected>Skip images</option>
                </select>
            </div>
            <div class="option">
                <label for="frontMatter">Include YAML front matter</label>
                <label class="checkbox-label">
                    <input type="checkbox" id="frontMatter" checked> Add YAML front matter to the document
                </label>
            </div>
            <div class="option">
                <label for="customTags">Custom tags (comma separated)</label>
                <input type="text" id="customTags" placeholder="pdf, imported, documentation">
            </div>
            <div class="option">
                <label class="checkbox-label">
                    <input type="checkbox" id="obsidianLinks" checked> Convert URLs to Obsidian links
                </label>
            </div>
            <div class="option">
                <label class="checkbox-label">
                    <input type="checkbox" id="formatTables" checked> Format tables nicely
                </label>
            </div>
        </div>
        
        <button id="convertBtn" disabled>Convert PDF to Markdown</button>
        
        <div id="progressContainer">
            <p>Converting PDF... please wait.</p>
            <div id="progressBar">
                <div id="progress"></div>
            </div>
        </div>
        
        <div id="result">
            <h3>Markdown Result</h3>
            <textarea id="mdContent" spellcheck="false"></textarea>
            <button id="downloadBtn" class="download-btn">Download Markdown File</button>
        </div>
    </div>
    
    <footer>
        <p>This tool converts PDF files to Markdown format optimized for Obsidian. All processing happens in your browser - no files are uploaded to any server.</p>
    </footer>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.10.111/pdf.min.js"></script>
    <script>
        // Set PDF.js worker path
        pdfjsLib.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.10.111/pdf.worker.min.js';
        
        // DOM elements
        const dropArea = document.getElementById('dropArea');
        const fileInput = document.getElementById('fileInput');
        const convertBtn = document.getElementById('convertBtn');
        const progressContainer = document.getElementById('progressContainer');
        const progressBar = document.getElementById('progress');
        const resultDiv = document.getElementById('result');
        const mdContent = document.getElementById('mdContent');
        const downloadBtn = document.getElementById('downloadBtn');
        
        // Option elements
        const headingLevel = document.getElementById('headingLevel');
        const imageHandling = document.getElementById('imageHandling');
        const frontMatter = document.getElementById('frontMatter');
        const customTags = document.getElementById('customTags');
        const obsidianLinks = document.getElementById('obsidianLinks');
        const formatTables = document.getElementById('formatTables');
        
        // Current file
        let currentFile = null;
        
        // Event Listeners
        dropArea.addEventListener('click', () => fileInput.click());
        fileInput.addEventListener('change', handleFileSelect);
        
        dropArea.addEventListener('dragover', (e) => {
            e.preventDefault();
            dropArea.classList.add('highlight');
        });
        
        dropArea.addEventListener('dragleave', () => {
            dropArea.classList.remove('highlight');
        });
        
        dropArea.addEventListener('drop', (e) => {
            e.preventDefault();
            dropArea.classList.remove('highlight');
            
            if (e.dataTransfer.files.length) {
                const file = e.dataTransfer.files[0];
                if (file.type === 'application/pdf') {
                    handleFile(file);
                } else {
                    alert('Please select a PDF file');
                }
            }
        });
        
        convertBtn.addEventListener('click', convertPdfToMarkdown);
        downloadBtn.addEventListener('click', downloadMarkdown);
        
        // Functions
        function handleFileSelect(e) {
            if (e.target.files.length) {
                const file = e.target.files[0];
                if (file.type === 'application/pdf') {
                    handleFile(file);
                } else {
                    alert('Please select a PDF file');
                }
            }
        }
        
        function handleFile(file) {
            currentFile = file;
            dropArea.textContent = `Selected: ${file.name}`;
            convertBtn.disabled = false;
            resultDiv.style.display = 'none';
        }
        
        async function convertPdfToMarkdown() {
            if (!currentFile) return;
            
            // Show progress
            progressContainer.style.display = 'block';
            progressBar.style.width = '0%';
            convertBtn.disabled = true;
            
            try {
                const fileData = await readFileAsArrayBuffer(currentFile);
                const pdf = await pdfjsLib.getDocument({ data: fileData }).promise;
                
                // Create markdown with options
                const options = {
                    headingLevel: parseInt(headingLevel.value),
                    imageHandling: imageHandling.value,
                    includeFrontMatter: frontMatter.checked,
                    tags: customTags.value,
                    convertLinks: obsidianLinks.checked,
                    formatTables: formatTables.checked
                };
                
                let markdown = '';
                
                // Add YAML front matter if selected
                if (options.includeFrontMatter) {
                    const filename = currentFile.name.replace('.pdf', '');
                    const date = new Date().toISOString().split('T')[0];
                    
                    markdown += '---\n';
                    markdown += `title: "${filename}"\n`;
                    markdown += `date: ${date}\n`;
                    
                    if (options.tags) {
                        markdown += 'tags:\n';
                        const tags = options.tags.split(',').map(tag => tag.trim());
                        tags.forEach(tag => {
                            if (tag) markdown += `  - ${tag}\n`;
                        });
                    }
                    
                    markdown += 'source: "PDF Import"\n';
                    markdown += '---\n\n';
                }
                
                // Extract text from each page
                for (let i = 1; i <= pdf.numPages; i++) {
                    const page = await pdf.getPage(i);
                    const textContent = await page.getTextContent();
                    
                    // Update progress
                    const progress = Math.floor((i / pdf.numPages) * 100);
                    progressBar.style.width = `${progress}%`;
                    
                    // Convert page content to markdown
                    let pageText = '';
                    let lastY = null;
                    let textItems = [];
                    
                    // Collect all text items
                    textContent.items.forEach(item => {
                        // Check if this is a new line based on Y position
                        if (lastY !== null && Math.abs(lastY - item.transform[5]) > 1) {
                            // Process collected text items for the line
                            if (textItems.length > 0) {
                                pageText += processTextLine(textItems, options) + '\n';
                                textItems = [];
                            }
                        }
                        
                        textItems.push(item);
                        lastY = item.transform[5];
                    });
                    
                    // Process any remaining text items
                    if (textItems.length > 0) {
                        pageText += processTextLine(textItems, options) + '\n';
                    }
                    
                    // Add page marker (optional)
                    if (i > 1) {
                        markdown += `\n\n<!-- Page ${i} -->\n\n`;
                    }
                    
                    markdown += pageText;
                }
                
                // Post-processing
                markdown = cleanupMarkdown(markdown, options);
                
                // Display result
                mdContent.value = markdown;
                resultDiv.style.display = 'block';
                
            } catch (error) {
                console.error('Error converting PDF:', error);
                alert('Error converting PDF. Please try another file.');
            } finally {
                progressContainer.style.display = 'none';
                convertBtn.disabled = false;
            }
        }
        
        function processTextLine(textItems, options) {
            // Join all items in the line
            let line = textItems.map(item => item.str).join('');
            
            // Check for headings (approximately)
            if (line.trim().length > 0) {
                const trimmedLine = line.trim();
                
                // Check if possibly a heading (simple heuristic)
                const isPossibleHeading = 
                    trimmedLine.length < 100 && // Not too long
                    !trimmedLine.endsWith('.') && // Doesn't end with a period
                    textItems.length > 0 && 
                    textItems[0].height > 11; // Font size larger than normal
                
                if (isPossibleHeading) {
                    const headingDepth = Math.min(options.headingLevel + Math.floor(12 / textItems[0].height), 6);
                    line = '\n' + '#'.repeat(headingDepth) + ' ' + trimmedLine + '\n';
                }
                
                // Convert URLs to Obsidian links if option is enabled
                if (options.convertLinks) {
                    const urlRegex = /(https?:\/\/[^\s]+)/g;
                    line = line.replace(urlRegex, (url) => {
                        // Extract last part of URL for the link text
                        const parts = url.split('/');
                        const linkText = parts[parts.length - 1] || url;
                        return `[${linkText}](${url})`;
                    });
                }
            }
            
            return line;
        }
        
        function cleanupMarkdown(markdown, options) {
            // Remove excessive newlines
            markdown = markdown.replace(/\n{3,}/g, '\n\n');
            
            // Improve table formatting if option is enabled
            if (options.formatTables) {
                // Simple table detection and formatting (basic implementation)
                const tableRowRegex = /(?:^|\n)([^\n]+\|[^\n]+)(?:\n|$)/g;
                let tableMatch;
                let tables = [];
                
                while ((tableMatch = tableRowRegex.exec(markdown)) !== null) {
                    const potentialTable = tableMatch[1];
                    if (potentialTable.split('|').length > 2) {
                        tables.push(potentialTable);
                    }
                }
                
                // Format detected tables
                tables.forEach(table => {
                    const formattedTable = formatTable(table);
                    markdown = markdown.replace(table, formattedTable);
                });
            }
            
            return markdown;
        }
        
        function formatTable(tableRow) {
            // Split the row by pipe character
            const cells = tableRow.split('|').filter(cell => cell.trim() !== '');
            
            if (cells.length < 2) return tableRow; // Not likely a table
            
            // Create formatted table
            let formattedTable = '\n|';
            cells.forEach(cell => {
                formattedTable += ` ${cell.trim()} |`;
            });
            
            // Add separator row
            formattedTable += '\n|';
            cells.forEach(() => {
                formattedTable += ' --- |';
            });
            
            return formattedTable;
        }
        
        function readFileAsArrayBuffer(file) {
            return new Promise((resolve, reject) => {
                const reader = new FileReader();
                reader.onload = e => resolve(e.target.result);
                reader.onerror = reject;
                reader.readAsArrayBuffer(file);
            });
        }
        
        function downloadMarkdown() {
            if (!mdContent.value) return;
            
            const filename = currentFile.name.replace('.pdf', '.md');
            const blob = new Blob([mdContent.value], { type: 'text/markdown' });
            const url = URL.createObjectURL(blob);
            
            const a = document.createElement('a');
            a.href = url;
            a.download = filename;
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            URL.revokeObjectURL(url);
        }
    </script>
</body>
</html>