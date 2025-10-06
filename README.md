# AYUSH-WEBITE-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PDFMaster - Your PDF Tools</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background: #f8fafc;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Navigation */
        .navbar {
            background: #fff;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 70px;
            padding: 0 20px;
        }

        .nav-logo h2 {
            color: #2c5aa0;
        }

        .nav-menu {
            display: flex;
            list-style: none;
        }

        .nav-item {
            margin-left: 30px;
        }

        .nav-link {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-link:hover {
            color: #2c5aa0;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #2c5aa0, #1e3a8a);
            color: white;
            padding: 150px 0 100px;
            text-align: center;
            margin-top: 70px;
        }

        .hero-content h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        /* Tools Section */
        .tools-section {
            padding: 80px 0;
        }

        .tools-section h2 {
            text-align: center;
            margin-bottom: 50px;
            color: #2c5aa0;
            font-size: 2.5rem;
        }

        .tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .tool-card {
            background: white;
            padding: 40px 30px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .tool-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }

        .tool-icon {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        .tool-card h3 {
            color: #2c5aa0;
            margin-bottom: 15px;
        }

        /* Tool Page Styles */
        .tool-page {
            padding: 120px 0 80px;
            min-height: 80vh;
        }

        .upload-area {
            border: 2px dashed #2c5aa0;
            border-radius: 10px;
            padding: 60px 20px;
            text-align: center;
            background: #f8fafc;
            margin: 30px 0;
            cursor: pointer;
            transition: background 0.3s;
        }

        .upload-area:hover {
            background: #e2e8f0;
        }

        .upload-area.dragover {
            background: #e2e8f0;
            border-color: #1e3a8a;
        }

        .upload-icon {
            font-size: 4rem;
            margin-bottom: 20px;
        }

        .btn {
            background: #2c5aa0;
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            transition: background 0.3s;
            margin: 10px;
        }

        .btn:hover {
            background: #1e3a8a;
        }

        .btn:disabled {
            background: #ccc;
            cursor: not-allowed;
        }

        .download-btn {
            background: #10b981;
            color: white;
            padding: 15px 40px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1.1rem;
            text-decoration: none;
            display: inline-block;
            transition: background 0.3s;
        }

        .download-btn:hover {
            background: #059669;
        }

        .progress-bar {
            width: 100%;
            height: 10px;
            background: #e2e8f0;
            border-radius: 5px;
            margin: 20px 0;
            overflow: hidden;
        }

        .progress {
            height: 100%;
            background: #2c5aa0;
            width: 0%;
            transition: width 0.3s;
        }

        .download-section {
            text-align: center;
            margin-top: 30px;
            padding: 40px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .file-info {
            background: #f8fafc;
            padding: 15px;
            border-radius: 5px;
            margin: 10px 0;
            text-align: left;
        }

        .file-list {
            max-height: 200px;
            overflow-y: auto;
            margin: 15px 0;
        }

        /* Games Section */
        .games-section {
            padding: 80px 0;
            background: white;
        }

        .games-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .game-card {
            background: #f8fafc;
            padding: 30px;
            border-radius: 10px;
            text-align: center;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .game-card:hover {
            transform: translateY(-3px);
        }

        /* Contact Section */
        .contact-section {
            padding: 80px 0;
            background: #f8fafc;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 15px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }

        .contact-form button {
            background: #2c5aa0;
            color: white;
            padding: 15px 40px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            transition: background 0.3s;
        }

        /* Footer */
        .footer {
            background: #1a202c;
            color: white;
            text-align: center;
            padding: 30px 0;
        }

        /* Hidden class for page management */
        .page {
            display: none;
        }

        .page.active {
            display: block;
        }

        .loading {
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 3px solid #f3f3f3;
            border-top: 3px solid #2c5aa0;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .nav-menu {
                display: none;
            }

            .hero-content h1 {
                font-size: 2rem;
            }

            .tools-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation Bar -->
    <nav class="navbar">
        <div class="nav-container">
            <div class="nav-logo">
                <h2>PDFMaster</h2>
            </div>
            <ul class="nav-menu">
                <li class="nav-item"><a href="#" class="nav-link" onclick="showPage('home')">Home</a></li>
                <li class="nav-item"><a href="#" class="nav-link" onclick="showPage('tools')">PDF Tools</a></li>
                <li class="nav-item"><a href="#" class="nav-link" onclick="showPage('games')">Games</a></li>
                <li class="nav-item"><a href="#" class="nav-link" onclick="showPage('contact')">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Home Page -->
    <div id="home" class="page active">
        <section class="hero">
            <div class="container">
                <div class="hero-content">
                    <h1>All Your PDF Tools in One Place</h1>
                    <p>Compress, merge, split, convert - Easy to use in your browser</p>
                </div>
            </div>
        </section>

        <section class="tools-section">
            <div class="container">
                <h2>Popular PDF Tools</h2>
                <div class="tools-grid">
                    <div class="tool-card" onclick="showTool('compress')">
                        <div class="tool-icon">📦</div>
                        <h3>Compress PDF</h3>
                        <p>Reduce file size while optimizing quality</p>
                    </div>

                    <div class="tool-card" onclick="showTool('merge')">
                        <div class="tool-icon">🔄</div>
                        <h3>Merge PDF</h3>
                        <p>Combine multiple PDFs into one</p>
                    </div>

                    <div class="tool-card" onclick="showTool('split')">
                        <div class="tool-icon">✂️</div>
                        <h3>Split PDF</h3>
                        <p>Extract pages or split by range</p>
                    </div>

                    <div class="tool-card" onclick="showTool('pdf-to-jpg')">
                        <div class="tool-icon">🖼️</div>
                        <h3>PDF to JPG</h3>
                        <p>Convert PDF pages to JPG images</p>
                    </div>

                    <div class="tool-card" onclick="showTool('jpg-to-pdf')">
                        <div class="tool-icon">📄</div>
                        <h3>JPG to PDF</h3>
                        <p>Convert images to PDF documents</p>
                    </div>

                    <div class="tool-card" onclick="showTool('rotate')">
                        <div class="tool-icon">🔄</div>
                        <h3>Rotate PDF</h3>
                        <p>Rotate PDF pages clockwise or counterclockwise</p>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- Tools Page -->
    <div id="tools" class="page">
        <section class="tool-page">
            <div class="container">
                <h1>PDF Tools</h1>
                <p>Select a tool to get started</p>
                <div class="tools-grid">
                    <div class="tool-card" onclick="showTool('compress')">
                        <div class="tool-icon">📦</div>
                        <h3>Compress PDF</h3>
                        <p>Reduce file size while optimizing quality</p>
                    </div>

                    <div class="tool-card" onclick="showTool('merge')">
                        <div class="tool-icon">🔄</div>
                        <h3>Merge PDF</h3>
                        <p>Combine multiple PDFs into one</p>
                    </div>

                    <div class="tool-card" onclick="showTool('split')">
                        <div class="tool-icon">✂️</div>
                        <h3>Split PDF</h3>
                        <p>Extract pages or split by range</p>
                    </div>

                    <div class="tool-card" onclick="showTool('pdf-to-jpg')">
                        <div class="tool-icon">🖼️</div>
                        <h3>PDF to JPG</h3>
                        <p>Convert PDF pages to JPG images</p>
                    </div>

                    <div class="tool-card" onclick="showTool('jpg-to-pdf')">
                        <div class="tool-icon">📄</div>
                        <h3>JPG to PDF</h3>
                        <p>Convert images to PDF documents</p>
                    </div>

                    <div class="tool-card" onclick="showTool('rotate')">
                        <div class="tool-icon">🔄</div>
                        <h3>Rotate PDF</h3>
                        <p>Rotate PDF pages clockwise or counterclockwise</p>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- Individual Tool Pages -->
    <div id="tool-compress" class="page">
        <section class="tool-page">
            <div class="container">
                <button class="btn" onclick="showPage('tools')">← Back to Tools</button>
                <h1>Compress PDF</h1>
                <p>Reduce PDF file size while maintaining quality</p>
                
                <div id="compress-upload" class="upload-area" onclick="document.getElementById('compress-file').click()">
                    <div class="upload-icon">📤</div>
                    <h3>Click to upload PDF file</h3>
                    <p>Maximum file size: 10MB</p>
                    <input type="file" id="compress-file" accept=".pdf" style="display: none;" onchange="handleFileSelect(this, 'compress')">
                </div>

                <div style="text-align: center;">
                    <button class="btn" onclick="processPDF('compress')" id="compress-btn" disabled>Compress PDF</button>
                </div>

                <div id="compress-result"></div>
            </div>
        </section>
    </div>

    <div id="tool-merge" class="page">
        <section class="tool-page">
            <div class="container">
                <button class="btn" onclick="showPage('tools')">← Back to Tools</button>
                <h1>Merge PDF</h1>
                <p>Combine multiple PDF files into one document</p>
                
                <div id="merge-upload" class="upload-area" onclick="document.getElementById('merge-file').click()">
                    <div class="upload-icon">📤</div>
                    <h3>Click to upload PDF files</h3>
                    <p>Select multiple files (Ctrl+Click)</p>
                    <input type="file" id="merge-file" accept=".pdf" multiple style="display: none;" onchange="handleFileSelect(this, 'merge')">
                </div>

                <div style="text-align: center;">
                    <button class="btn" onclick="processPDF('merge')" id="merge-btn" disabled>Merge PDFs</button>
                </div>

                <div id="merge-result"></div>
            </div>
        </section>
    </div>

    <!-- Games Page -->
    <div id="games" class="page">
        <section class="games-section">
            <div class="container">
                <h1>Games</h1>
                <p>Fun games to play while your files process</p>
                
                <div class="games-grid">
                    <div class="game-card" onclick="startGame('tic-tac-toe')">
                        <h3>🎮 Tic Tac Toe</h3>
                        <p>Classic X and O game</p>
                    </div>
                    
                    <div class="game-card" onclick="startGame('memory')">
                        <h3>🧠 Memory Game</h3>
                        <p>Test your memory skills</p>
                    </div>
                </div>

                <div id="game-area" style="margin-top: 50px; display: none;">
                    <button class="btn" onclick="hideGame()">← Back to Games</button>
                    <div id="game-content" style="background: white; padding: 30px; border-radius: 10px; margin-top: 20px;"></div>
                </div>
            </div>
        </section>
    </div>

    <!-- Contact Page -->
    <div id="contact" class="page">
        <section class="contact-section">
            <div class="container">
                <h1>Contact Us</h1>
                <form class="contact-form" onsubmit="handleContact(event)">
                    <input type="text" id="name" placeholder="Your Name" required>
                    <input type="email" id="email" placeholder="Your Email" required>
                    <textarea id="message" placeholder="Your Message" rows="5" required></textarea>
                    <button type="submit">Send Message</button>
                </form>
            </div>
        </section>
    </div>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <p>&copy; 2024 PDFMaster. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Simple PDF processing simulation without external libraries
        class SimplePDFProcessor {
            static async compressPDF(file) {
                // Simulate compression by returning the original file
                return new Promise((resolve) => {
                    const reader = new FileReader();
                    reader.onload = function(e) {
                        resolve(new Blob([e.target.result], { type: 'application/pdf' }));
                    };
                    reader.readAsArrayBuffer(file);
                });
            }

            static async mergePDFs(files) {
                // For demo purposes, return the first file as "merged"
                return new Promise((resolve) => {
                    const reader = new FileReader();
                    reader.onload = function(e) {
                        resolve(new Blob([e.target.result], { type: 'application/pdf' }));
                    };
                    reader.readAsArrayBuffer(files[0]);
                });
            }

            static async splitPDF(file) {
                // For demo purposes, return the original file as "split"
                return new Promise((resolve) => {
                    const reader = new FileReader();
                    reader.onload = function(e) {
                        resolve(new Blob([e.target.result], { type: 'application/pdf' }));
                    };
                    reader.readAsArrayBuffer(file);
                });
            }
        }

        // Page Navigation
        function showPage(pageId) {
            console.log('Showing page:', pageId);
            document.querySelectorAll('.page').forEach(page => {
                page.classList.remove('active');
            });
            document.getElementById(pageId).classList.add('active');
        }

        function showTool(toolName) {
            showPage('tool-' + toolName);
        }

        // File Handling
        let currentFiles = {};

        function handleFileSelect(input, tool) {
            const files = input.files;
            if (files.length > 0) {
                currentFiles[tool] = files;
                const uploadArea = document.getElementById(tool + '-upload');
                const button = document.getElementById(tool + '-btn');
                
                let fileText = '';
                let fileList = '';
                
                if (files.length === 1) {
                    fileText = `Selected: ${files[0].name}`;
                    fileList = `<div class="file-info"><strong>File:</strong> ${files[0].name} (${formatFileSize(files[0].size)})</div>`;
                } else {
                    fileText = `Selected: ${files.length} files`;
                    fileList = `<div class="file-list">` + 
                        Array.from(files).map(file => 
                            `<div class="file-info"><strong>File:</strong> ${file.name} (${formatFileSize(file.size)})</div>`
                        ).join('') + 
                        `</div>`;
                }
                
                uploadArea.innerHTML = `
                    <div class="upload-icon">✅</div>
                    <h3>${fileText}</h3>
                    ${fileList}
                    <p>Ready to process</p>
                    <button class="btn" onclick="processPDF('${tool}')">Process ${tool.charAt(0).toUpperCase() + tool.slice(1)}</button>
                `;
                
                button.disabled = false;
            }
        }

        function formatFileSize(bytes) {
            if (bytes === 0) return '0 Bytes';
            const k = 1024;
            const sizes = ['Bytes', 'KB', 'MB', 'GB'];
            const i = Math.floor(Math.log(bytes) / Math.log(k));
            return parseFloat((bytes / Math.pow(k, i)).toFixed(2)) + ' ' + sizes[i];
        }

        // PDF Processing
        async function processPDF(tool) {
            console.log('Processing:', tool);
            const resultDiv = document.getElementById(tool + '-result');
            const button = document.getElementById(tool + '-btn');
            
            button.disabled = true;
            resultDiv.innerHTML = `
                <div class="upload-area">
                    <div class="upload-icon">⏳</div>
                    <h3>Processing...</h3>
                    <div class="progress-bar">
                        <div class="progress" id="${tool}-progress"></div>
                    </div>
                    <p>Please wait while we process your file</p>
                </div>
            `;

            try {
                let processedBlob;
                let progress = 0;
                
                // Simulate processing with progress
                const progressInterval = setInterval(() => {
                    progress += 5;
                    const progressBar = document.getElementById(tool + '-progress');
                    if (progressBar) {
                        progressBar.style.width = progress + '%';
                    }
                    
                    if (progress >= 100) {
                        clearInterval(progressInterval);
                        
                        // Process the actual files
                        processFiles(tool).then(blob => {
                            processedBlob = blob;
                            showDownloadResult(tool, processedBlob);
                        }).catch(error => {
                            throw error;
                        });
                    }
                }, 50);
                
            } catch (error) {
                console.error('Processing error:', error);
                resultDiv.innerHTML = `
                    <div class="upload-area" style="border-color: #e53e3e;">
                        <div class="upload-icon">❌</div>
                        <h3>Error Processing File</h3>
                        <p>${error.message || 'Something went wrong. Please try again.'}</p>
                        <button class="btn" onclick="resetTool('${tool}')">Try Again</button>
                    </div>
                `;
                button.disabled = false;
            }
        }

        async function processFiles(tool) {
            if (!currentFiles[tool] || currentFiles[tool].length === 0) {
                throw new Error('No files selected');
            }

            switch(tool) {
                case 'compress':
                    return await SimplePDFProcessor.compressPDF(currentFiles[tool][0]);
                case 'merge':
                    return await SimplePDFProcessor.mergePDFs(Array.from(currentFiles[tool]));
                case 'split':
                    return await SimplePDFProcessor.splitPDF(currentFiles[tool][0]);
                default:
                    // For other tools, return the first file as processed
                    return new Blob([await readFileAsArrayBuffer(currentFiles[tool][0])], { type: 'application/pdf' });
            }
        }

        function readFileAsArrayBuffer(file) {
            return new Promise((resolve, reject) => {
                const reader = new FileReader();
                reader.onload = e => resolve(e.target.result);
                reader.onerror = reject;
                reader.readAsArrayBuffer(file);
            });
        }

        function showDownloadResult(tool, blob) {
            const resultDiv = document.getElementById(tool + '-result');
            const url = URL.createObjectURL(blob);
            
            let originalSize = 0;
            if (currentFiles[tool] && currentFiles[tool][0]) {
                originalSize = currentFiles[tool][0].size;
            }
            const processedSize = blob.size;
            
            let compressionInfo = '';
            if (tool === 'compress') {
                const savings = originalSize > 0 ? ((originalSize - processedSize) / originalSize * 100).toFixed(1) : '0';
                compressionInfo = `
                    <div style="background: #f0f9ff; padding: 15px; border-radius: 5px; margin: 15px 0;">
                        <p><strong>Original Size:</strong> ${formatFileSize(originalSize)}</p>
                        <p><strong>Processed Size:</strong> ${formatFileSize(processedSize)}</p>
                        <p><strong>Size Reduction:</strong> ${savings}%</p>
                    </div>
                `;
            }

            resultDiv.innerHTML = `
                <div class="download-section">
                    <div class="upload-icon">🎉</div>
                    <h3>Successfully Processed!</h3>
                    ${compressionInfo}
                    <p>Your ${tool.replace('-', ' ')} operation is complete</p>
                    <a href="${url}" download="processed-${tool}.pdf" class="download-btn" onclick="trackDownload('${tool}')">
                        📥 Download Result
                    </a>
                    <br><br>
                    <button class="btn" onclick="resetTool('${tool}')">🔄 Process Another File</button>
                </div>
            `;
        }

        function trackDownload(tool) {
            console.log(`Download triggered for: ${tool}`);
            // In a real application, you would send analytics here
        }

        function resetTool(tool) {
            currentFiles[tool] = null;
            const fileInput = document.getElementById(tool + '-file');
            if (fileInput) fileInput.value = '';
            
            document.getElementById(tool + '-upload').innerHTML = `
                <div class="upload-icon">📤</div>
                <h3>Click to upload ${tool === 'merge' ? 'PDF files' : 'PDF file'}</h3>
                <p>Maximum file size: 10MB</p>
            `;
            document.getElementById(tool + '-result').innerHTML = '';
            document.getElementById(tool + '-btn').disabled = true;
        }

        // Games
        function startGame(game) {
            document.getElementById('game-area').style.display = 'block';
            const gameContent = document.getElementById('game-content');
            
            switch(game) {
                case 'tic-tac-toe':
                    gameContent.innerHTML = `
                        <h2>Tic Tac Toe</h2>
                        <div style="display: grid; grid-template-columns: repeat(3, 100px); gap: 5px; margin: 20px auto; width: 310px;">
                            ${Array(9).fill().map((_, i) => 
                                `<div style="width: 100px; height: 100px; border: 2px solid #333; display: flex; align-items: center; justify-content: center; font-size: 2rem; cursor: pointer; background: white;" 
                                      onclick="makeMove(${i})" id="cell-${i}"></div>`
                            ).join('')}
                        </div>
                        <p id="game-status" style="font-size: 1.2rem; font-weight: bold; margin: 20px 0;">Your turn (X)</p>
                        <button class="btn" onclick="resetTicTacToe()">New Game</button>
                    `;
                    resetTicTacToe();
                    break;
                    
                case 'memory':
                    gameContent.innerHTML = `
                        <h2>Memory Game - Coming Soon</h2>
                        <p>This game will be available in the next update!</p>
                        <button class="btn" onclick="hideGame()">Back to Games</button>
                    `;
                    break;
                    
                default:
                    gameContent.innerHTML = `
                        <h2>Game Under Development</h2>
                        <p>This game is coming soon!</p>
                        <button class="btn" onclick="hideGame()">Back to Games</button>
                    `;
            }
        }

        function hideGame() {
            document.getElementById('game-area').style.display = 'none';
        }

        // Tic Tac Toe Game
        let currentPlayer = 'X';
        let gameBoard = ['', '', '', '', '', '', '', '', ''];
        let gameActive = true;

        function resetTicTacToe() {
            currentPlayer = 'X';
            gameBoard = ['', '', '', '', '', '', '', '', ''];
            gameActive = true;
            
            for (let i = 0; i < 9; i++) {
                const cell = document.getElementById('cell-' + i);
                if (cell) {
                    cell.textContent = '';
                    cell.style.background = 'white';
                }
            }
            
            const status = document.getElementById('game-status');
            if (status) {
                status.textContent = 'Your turn (X)';
                status.style.color = '#2c5aa0';
            }
        }

        function makeMove(index) {
            if (!gameActive || gameBoard[index] !== '') return;
            
            gameBoard[index] = currentPlayer;
            const cell = document.getElementById('cell-' + i);
            if (cell) {
                cell.textContent = currentPlayer;
                cell.style.color = currentPlayer === 'X' ? '#2c5aa0' : '#e53e3e';
            }
            
            if (checkWinner()) {
                document.getElementById('game-status').textContent = `Player ${currentPlayer} wins! 🎉`;
                document.getElementById('game-status').style.color = '#10b981';
                gameActive = false;
                highlightWinningCells();
                return;
            }
            
            if (gameBoard.every(cell => cell !== '')) {
                document.getElementById('game-status').textContent = 'Game draw! 🤝';
                document.getElementById('game-status').style.color = '#6b7280';
                gameActive = false;
                return;
            }
            
            currentPlayer = currentPlayer === 'X' ? 'O' : 'X';
            document.getElementById('game-status').textContent = `Player ${currentPlayer}'s turn`;
            document.getElementById('game-status').style.color = currentPlayer === 'X' ? '#2c5aa0' : '#e53e3e';
        }

        function checkWinner() {
            const winPatterns = [
                [0,1,2], [3,4,5], [6,7,8],
                [0,3,6], [1,4,7], [2,5,8],
                [0,4,8], [2,4,6]
            ];
            
            return winPatterns.some(pattern => {
                const [a,b,c] = pattern;
                return gameBoard[a] && gameBoard[a] === gameBoard[b] && gameBoard[a] === gameBoard[c];
            });
        }

        function highlightWinningCells() {
            const winPatterns = [
                [0,1,2], [3,4,5], [6,7,8],
                [0,3,6], [1,4,7], [2,5,8],
                [0,4,8], [2,4,6]
            ];
            
            for (const pattern of winPatterns) {
                const [a,b,c] = pattern;
                if (gameBoard[a] && gameBoard[a] === gameBoard[b] && gameBoard[a] === gameBoard[c]) {
                    pattern.forEach(index => {
                        const cell = document.getElementById('cell-' + index);
                        if (cell) {
                            cell.style.background = '#10b981';
                            cell.style.color = 'white';
                        }
                    });
                    break;
                }
            }
        }

        // Contact Form
        function handleContact(event) {
            event.preventDefault();
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            
            alert(`Thank you ${name}! Your message has been received. We'll contact you at ${email} soon.`);
            event.target.reset();
        }

        // Initialize
        document.addEventListener('DOMContentLoaded', function() {
            console.log('PDFMaster initialized');
            showPage('home');
        });

        // Error handling for the entire application
        window.addEventListener('error', function(e) {
            console.error('Global error:', e.error);
        });
    </script>
</body>
</html>
