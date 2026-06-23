<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Contractor Safety Statistics Analyzer</title>
    <style>
        :root {
            --bg-dark-blue: #0f172a;
            --bg-sidebar: #1e293b;
            --bg-main: #f1f5f9;
            --bg-panel: #ffffff;
            --primary: #3b82f6;
            --primary-hover: #2563eb;
            --text-main: #334155;
            --text-light: #94a3b8;
            --text-white: #f8fafc;
            --border-color: #e2e8f0;
            --success: #10b981;
            --error: #ef4444;
            --chat-user: #e0f2fe;
            --chat-ai: #f1f5f9;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            height: 100vh;
            display: flex;
            flex-direction: column;
            overflow: hidden;
            background-color: var(--bg-main);
            color: var(--text-main);
        }

        /* Header Styles */
        header {
            height: 60px;
            background-color: var(--bg-panel);
            border-bottom: 1px solid var(--border-color);
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
            z-index: 10;
        }

        .logo-area {
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 600;
            font-size: 1.2rem;
            color: var(--bg-dark-blue);
        }

        .logo-icon {
            background-color: var(--primary);
            color: white;
            width: 32px;
            height: 32px;
            border-radius: 6px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
        }

        .header-controls {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .api-input-group {
            display: flex;
            align-items: center;
            background: var(--bg-main);
            border: 1px solid var(--border-color);
            border-radius: 6px;
            padding: 4px 10px;
        }

        .api-input-group input {
            border: none;
            background: transparent;
            outline: none;
            padding: 4px;
            width: 250px;
            font-size: 0.9rem;
        }

        .status-indicator {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background-color: var(--error);
            transition: background-color 0.3s;
            margin-left: 8px;
        }

        .status-indicator.connected {
            background-color: var(--success);
            box-shadow: 0 0 8px var(--success);
        }

        .btn {
            padding: 8px 16px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.2s;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .btn-primary { background-color: var(--primary); color: white; }
        .btn-primary:hover { background-color: var(--primary-hover); }
        .btn-outline { background-color: transparent; border: 1px solid var(--primary); color: var(--primary); }
        .btn-outline:hover { background-color: var(--chat-user); }

        /* Main Application Layout */
        .app-container {
            display: flex;
            flex: 1;
            overflow: hidden;
        }

        /* 1. Left Sidebar: Document Management */
        .sidebar-left {
            width: 250px;
            min-width: 250px;
            background-color: var(--bg-dark-blue);
            color: var(--text-white);
            display: flex;
            flex-direction: column;
            border-right: 1px solid var(--border-color);
        }

        .upload-area {
            padding: 20px;
            border-bottom: 1px solid var(--bg-sidebar);
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .upload-label {
            background-color: rgba(255, 255, 255, 0.1);
            border: 2px dashed rgba(255, 255, 255, 0.3);
            border-radius: 8px;
            padding: 20px 10px;
            text-align: center;
            cursor: pointer;
            transition: all 0.2s;
            font-size: 0.9rem;
        }

        .upload-label:hover {
            background-color: rgba(255, 255, 255, 0.2);
            border-color: white;
        }

        .file-list-header {
            padding: 15px 20px 5px;
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--text-light);
        }

        .file-list {
            flex: 1;
            overflow-y: auto;
            list-style: none;
            padding: 0 10px;
        }

        .file-item {
            padding: 10px 15px;
            margin: 5px 0;
            border-radius: 6px;
            cursor: pointer;
            transition: background 0.2s;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 10px;
            overflow: hidden;
            text-overflow: ellipsis;
            white-space: nowrap;
        }

        .file-item:hover {
            background-color: var(--bg-sidebar);
        }

        .file-item.active {
            background-color: var(--primary);
            color: white;
        }

        /* 2. Center Panel: PDF Viewer */
        .center-panel {
            flex: 1;
            display: flex;
            flex-direction: column;
            background-color: var(--bg-main);
            position: relative;
        }

        .viewer-header {
            height: 50px;
            background-color: var(--bg-panel);
            border-bottom: 1px solid var(--border-color);
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 20px;
        }

        .viewer-title {
            font-weight: 600;
            color: var(--text-main);
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .viewer-actions {
            display: flex;
            gap: 10px;
        }

        .pdf-container {
            flex: 1;
            width: 100%;
            height: 100%;
        }

        .pdf-container iframe {
            width: 100%;
            height: 100%;
            border: none;
        }

        .empty-state {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100%;
            color: var(--text-light);
            text-align: center;
            padding: 20px;
        }

        /* 3. Right Sidebar: AI Chatbot */
        .sidebar-right {
            width: 350px;
            min-width: 300px;
            background-color: var(--bg-panel);
            border-left: 1px solid var(--border-color);
            display: flex;
            flex-direction: column;
        }

        .chat-header {
            padding: 15px 20px;
            border-bottom: 1px solid var(--border-color);
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .chat-history {
            flex: 1;
            overflow-y: auto;
            padding: 20px;
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .chat-bubble {
            max-width: 85%;
            padding: 12px 16px;
            border-radius: 8px;
            font-size: 0.95rem;
            line-height: 1.5;
        }

        .chat-user {
            background-color: var(--chat-user);
            color: var(--bg-dark-blue);
            align-self: flex-end;
            border-bottom-right-radius: 0;
        }

        .chat-ai {
            background-color: var(--chat-ai);
            color: var(--text-main);
            align-self: flex-start;
            border-bottom-left-radius: 0;
        }

        .chat-input-area {
            padding: 15px;
            border-top: 1px solid var(--border-color);
            display: flex;
            flex-direction: column;
            gap: 10px;
            background-color: #fafafa;
        }

        .chat-input-wrapper {
            display: flex;
            gap: 10px;
        }

        .chat-input-area textarea {
            flex: 1;
            padding: 10px;
            border: 1px solid var(--border-color);
            border-radius: 6px;
            resize: none;
            height: 45px;
            outline: none;
            font-family: inherit;
        }

        .chat-input-area textarea:focus {
            border-color: var(--primary);
        }

        .btn-send {
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: 6px;
            width: 45px;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: background 0.2s;
        }

        .btn-send:hover { background-color: var(--primary-hover); }

        .chat-hint {
            font-size: 0.75rem;
            color: var(--text-light);
            text-align: center;
        }

        /* Modals (Mindmap & Presentation) */
        .modal-overlay {
            position: fixed;
            top: 0; left: 0; width: 100vw; height: 100vh;
            background: rgba(0,0,0,0.8);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 100;
            opacity: 0;
            transition: opacity 0.3s;
        }

        .modal-overlay.active {
            display: flex;
            opacity: 1;
        }

        .modal-content {
            background: var(--bg-panel);
            width: 90vw;
            height: 90vh;
            border-radius: 12px;
            display: flex;
            flex-direction: column;
            overflow: hidden;
            position: relative;
        }

        .modal-header {
            padding: 15px 25px;
            border-bottom: 1px solid var(--border-color);
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: #f8fafc;
        }

        .modal-close {
            background: transparent;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--text-light);
        }
        .modal-close:hover { color: var(--error); }

        .modal-body {
            flex: 1;
            position: relative;
            overflow: hidden;
            background: #ffffff;
        }

        /* Mindmap Specific Styles (Vanilla CSS Tree) */
        .mindmap-viewport {
            width: 100%;
            height: 100%;
            overflow: hidden;
            cursor: grab;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            background: #f4f7f6;
        }
        
        .mindmap-viewport:active { cursor: grabbing; }

        .mindmap-canvas {
            transform-origin: center center;
            transition: transform 0.1s ease-out;
            padding: 50px;
        }

        /* CSS Tree Layout */
        .tree ul {
            padding-top: 20px; position: relative;
            transition: all 0.5s;
            display: flex; justify-content: center;
        }
        .tree li {
            float: left; text-align: center;
            list-style-type: none;
            position: relative;
            padding: 20px 5px 0 5px;
            transition: all 0.5s;
        }
        .tree li::before, .tree li::after {
            content: ''; position: absolute; top: 0; right: 50%;
            border-top: 2px solid #94a3b8;
            width: 50%; height: 20px;
        }
        .tree li::after { right: auto; left: 50%; border-left: 2px solid #94a3b8; }
        .tree li:only-child::after, .tree li:only-child::before { display: none; }
        .tree li:only-child { padding-top: 0; }
        .tree li:first-child::before, .tree li:last-child::after { border: 0 none; }
        .tree li:last-child::before { border-right: 2px solid #94a3b8; border-radius: 0 5px 0 0; }
        .tree li:first-child::after { border-radius: 5px 0 0 0; }
        .tree ul ul::before {
            content: ''; position: absolute; top: 0; left: 50%;
            border-left: 2px solid #94a3b8; width: 0; height: 20px;
        }
        .tree li .node-box {
            border: 2px solid #3b82f6;
            padding: 10px 15px;
            text-decoration: none;
            color: #334155;
            font-family: arial, verdana, tahoma;
            font-size: 12px;
            display: inline-block;
            border-radius: 8px;
            transition: all 0.5s;
            background: white;
            box-shadow: 0 4px 6px -1px rgba(0,0,0,0.1);
            max-width: 200px;
            text-align: left;
        }
        .tree li .node-box .title { font-weight: bold; margin-bottom: 5px; display: block; color: #1e293b; font-size: 14px;}
        .tree li .node-box .desc { font-size: 11px; color: #64748b; line-height: 1.3;}

        /* Presentation Specific Styles */
        .slide-container {
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 50px;
            background: radial-gradient(circle, #ffffff 0%, #f1f5f9 100%);
        }
        .slide-card {
            width: 80%;
            max-width: 900px;
            height: 70%;
            background: white;
            border-radius: 12px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            padding: 50px;
            display: flex;
            flex-direction: column;
        }
        .slide-title {
            font-size: 2.5rem;
            color: var(--bg-dark-blue);
            margin-bottom: 30px;
            border-bottom: 3px solid var(--primary);
            padding-bottom: 10px;
        }
        .slide-content {
            flex: 1;
            font-size: 1.5rem;
            line-height: 1.8;
            color: var(--text-main);
        }
        .slide-content ul { padding-left: 30px; }
        .slide-content li { margin-bottom: 15px; }
        
        .pres-controls {
            position: absolute;
            bottom: 30px;
            left: 0; right: 0;
            display: flex;
            justify-content: center;
            gap: 20px;
            align-items: center;
        }
        .slide-counter { font-weight: bold; color: var(--text-light); }

        /* Loader */
        .loader {
            border: 3px solid #f3f3f3;
            border-top: 3px solid var(--primary);
            border-radius: 50%;
            width: 20px;
            height: 20px;
            animation: spin 1s linear infinite;
            display: inline-block;
        }
        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
        
        .loading-overlay {
            position: absolute; top: 0; left: 0; right: 0; bottom: 0;
            background: rgba(255,255,255,0.8);
            display: none; justify-content: center; align-items: center; flex-direction: column; z-index: 10;
        }
        .loading-overlay.active { display: flex; }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="logo-area">
            <div class="logo-icon">S</div>
            Contractor Safety Statistics Analyzer
        </div>
        <div class="header-controls">
            <div class="api-input-group">
                <input type="password" id="api-key" placeholder="Enter Gemini API Key (gemini-2.5-flash)">
                <div class="status-indicator" id="api-status" title="API Status"></div>
            </div>
            <button class="btn btn-outline" onclick="testConnection()">Connect API</button>
        </div>
    </header>

    <!-- Main Container -->
    <div class="app-container">
        
        <!-- 1. Left Sidebar -->
        <aside class="sidebar-left">
            <div class="upload-area">
                <input type="file" id="file-upload" multiple accept="application/pdf" style="display:none;">
                <label for="file-upload" class="upload-label">
                    <svg viewBox="0 0 24 24" width="24" height="24" stroke="currentColor" stroke-width="2" fill="none" style="margin-bottom: 8px;">
                        <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"></path>
                        <polyline points="17 8 12 3 7 8"></polyline>
                        <line x1="12" y1="3" x2="12" y2="15"></line>
                    </svg><br>
                    Upload Safety Reports (PDF)
                </label>
            </div>
            <div class="file-list-header">Uploaded Documents</div>
            <ul class="file-list" id="file-list">
                <!-- File items will be injected here -->
            </ul>
        </aside>

        <!-- 2. Center Panel -->
        <main class="center-panel">
            <div class="viewer-header">
                <div class="viewer-title" id="viewer-title">No document selected</div>
                <div class="viewer-actions">
                    <button class="btn btn-outline" id="btn-mindmap" onclick="generateMindmap()" disabled>
                        <svg viewBox="0 0 24 24" width="16" height="16" stroke="currentColor" stroke-width="2" fill="none"><circle cx="12" cy="12" r="3"></circle><path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1 0 2.83 2 2 0 0 1-2.83 0l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-2 2 2 2 0 0 1-2-2v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83 0 2 2 0 0 1 0-2.83l.06-.06a1.65 1.65 0 0 0 .33-1.82 1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1-2-2 2 2 0 0 1 2-2h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 0-2.83 2 2 0 0 1 2.83 0l.06.06a1.65 1.65 0 0 0 1.82.33H9a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 2-2 2 2 0 0 1 2 2v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 0 2 2 0 0 1 0 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 2 2 2 2 0 0 1-2 2h-.09a1.65 1.65 0 0 0-1.51 1z"></path></svg>
                        Mindmap
                    </button>
                    <button class="btn btn-outline" id="btn-presentation" onclick="generatePresentation()" disabled>
                        <svg viewBox="0 0 24 24" width="16" height="16" stroke="currentColor" stroke-width="2" fill="none"><rect x="2" y="3" width="20" height="14" rx="2" ry="2"></rect><line x1="8" y1="21" x2="16" y2="21"></line><line x1="12" y1="17" x2="12" y2="21"></line></svg>
                        Presentation
                    </button>
                </div>
            </div>
            
            <div class="pdf-container" id="pdf-container">
                <div class="empty-state">
                    <svg viewBox="0 0 24 24" width="48" height="48" stroke="#cbd5e1" stroke-width="1" fill="none"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path><polyline points="14 2 14 8 20 8"></polyline><line x1="16" y1="13" x2="8" y2="13"></line><line x1="16" y1="17" x2="8" y2="17"></line><polyline points="10 9 9 9 8 9"></polyline></svg>
                    <h3 style="margin-top: 15px; color: #64748b;">No PDF Loaded</h3>
                    <p style="margin-top: 5px; font-size: 0.9rem;">Upload from the sidebar to view</p>
                </div>
            </div>
        </main>

        <!-- 3. Right Sidebar -->
        <aside class="sidebar-right">
            <div class="chat-header">
                <svg viewBox="0 0 24 24" width="18" height="18" stroke="currentColor" stroke-width="2" fill="none"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"></path></svg>
                AI Assistant
            </div>
            
            <div class="chat-history" id="chat-history">
                <div class="chat-bubble chat-ai">
                    Hello! Please connect your Gemini API key, upload your Contractor Safety Statistics Reports, and ask me to analyze or compare them.
                </div>
            </div>

            <div class="chat-input-area">
                <div class="chat-hint">Use "compare all" to analyze across multiple uploads.</div>
                <div class="chat-input-wrapper">
                    <textarea id="chat-input" placeholder="Ask about safety metrics..."></textarea>
                    <button class="btn-send" onclick="sendMessage()">
                        <svg viewBox="0 0 24 24" width="18" height="18" stroke="currentColor" stroke-width="2" fill="none"><line x1="22" y1="2" x2="11" y2="13"></line><polygon points="22 2 15 22 11 13 2 9 22 2"></polygon></svg>
                    </button>
                </div>
            </div>
        </aside>

    </div>

    <!-- Modals -->
    <!-- Mindmap Modal -->
    <div class="modal-overlay" id="modal-mindmap">
        <div class="modal-content">
            <div class="modal-header">
                <h3>Document Mindmap (Interactive)</h3>
                <div style="font-size: 0.8rem; color: #64748b;">Scroll to zoom, drag to pan</div>
                <button class="modal-close" onclick="closeModal('modal-mindmap')">&times;</button>
            </div>
            <div class="modal-body">
                <div class="loading-overlay" id="mindmap-loader">
                    <div class="loader" style="width: 40px; height: 40px; border-width: 4px;"></div>
                    <p style="margin-top: 15px; font-weight: bold; color: var(--primary);">Analyzing Document & Building Mindmap...</p>
                </div>
                <div class="mindmap-viewport" id="mindmap-viewport">
                    <div class="mindmap-canvas tree" id="mindmap-canvas">
                        <!-- Custom CSS Tree rendered here -->
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Presentation Modal -->
    <div class="modal-overlay" id="modal-presentation">
        <div class="modal-content">
            <div class="modal-header">
                <h3>Executive Summary Presentation</h3>
                <button class="modal-close" onclick="closeModal('modal-presentation')">&times;</button>
            </div>
            <div class="modal-body">
                <div class="loading-overlay" id="pres-loader">
                    <div class="loader" style="width: 40px; height: 40px; border-width: 4px;"></div>
                    <p style="margin-top: 15px; font-weight: bold; color: var(--primary);">Generating Slides...</p>
                </div>
                <div class="slide-container">
                    <div class="slide-card" id="slide-card">
                        <div class="slide-title" id="slide-title">Title</div>
                        <div class="slide-content" id="slide-content">Content</div>
                    </div>
                    <div class="pres-controls">
                        <button class="btn btn-primary" onclick="prevSlide()">&#8592; Prev</button>
                        <span class="slide-counter"><span id="slide-current">1</span> / <span id="slide-total">1</span></span>
                        <button class="btn btn-primary" onclick="nextSlide()">Next &#8594;</button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Application Logic -->
    <script>
        // --- State Management ---
        let files = []; // [{id, name, base64, mimeType}]
        let currentFileId = null;
        let isApiConnected = false;
        
        // Presentation State
        let currentSlides = [];
        let currentSlideIndex = 0;

        // --- DOM Elements ---
        const fileUpload = document.getElementById('file-upload');
        const fileList = document.getElementById('file-list');
        const pdfContainer = document.getElementById('pdf-container');
        const viewerTitle = document.getElementById('viewer-title');
        const chatHistory = document.getElementById('chat-history');
        const chatInput = document.getElementById('chat-input');
        const btnMindmap = document.getElementById('btn-mindmap');
        const btnPresentation = document.getElementById('btn-presentation');

        // --- File Handling ---
        fileUpload.addEventListener('change', (e) => {
            const selectedFiles = Array.from(e.target.files);
            selectedFiles.forEach(file => {
                if(file.type !== 'application/pdf') {
                    alert('Only PDF files are supported.');
                    return;
                }

                const reader = new FileReader();
                reader.onload = (event) => {
                    const dataUrl = event.target.result;
                    const base64 = dataUrl.split(',')[1];
                    
                    const newFile = {
                        id: 'file_' + Date.now() + Math.random().toString(36).substr(2, 9),
                        name: file.name,
                        base64: base64,
                        mimeType: 'application/pdf',
                        dataUrl: dataUrl
                    };

                    files.push(newFile);
                    renderFileList();
                    
                    // Auto-select if it's the first file
                    if(files.length === 1) {
                        selectFile(newFile.id);
                    }
                };
                reader.readAsDataURL(file);
            });
        });

        function renderFileList() {
            fileList.innerHTML = '';
            files.forEach(file => {
                const li = document.createElement('li');
                li.className = `file-item ${file.id === currentFileId ? 'active' : ''}`;
                li.innerHTML = `
                    <svg viewBox="0 0 24 24" width="16" height="16" stroke="currentColor" stroke-width="2" fill="none"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path><polyline points="14 2 14 8 20 8"></polyline><line x1="16" y1="13" x2="8" y2="13"></line><line x1="16" y1="17" x2="8" y2="17"></line><polyline points="10 9 9 9 8 9"></polyline></svg>
                    ${file.name}
                `;
                li.onclick = () => selectFile(file.id);
                fileList.appendChild(li);
            });
            
            const hasFiles = files.length > 0;
            btnMindmap.disabled = !hasFiles;
            btnPresentation.disabled = !hasFiles;
        }

        function selectFile(id) {
            currentFileId = id;
            renderFileList();
            const file = files.find(f => f.id === id);
            if(file) {
                viewerTitle.textContent = file.name;
                // Using embedded object for native PDF rendering
                pdfContainer.innerHTML = `<object data="${file.dataUrl}#view=FitH" type="application/pdf" width="100%" height="100%">
                    <p>Your browser does not support PDFs. Please download the PDF to view it.</p>
                </object>`;
            }
        }

        // --- Gemini API Integration ---
        function getApiKey() {
            return document.getElementById('api-key').value.trim();
        }

        async function testConnection() {
            const apiKey = getApiKey();
            const statusIndicator = document.getElementById('api-status');
            
            if(!apiKey) {
                alert("Please enter an API Key first.");
                return;
            }

            statusIndicator.className = 'status-indicator loader';
            statusIndicator.style.background = 'transparent';

            try {
                // Test call using gemini-2.5-flash
                const url = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash:generateContent?key=${apiKey}`;
                const response = await fetch(url, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({
                        contents: [{ parts: [{ text: "Respond with exactly one word: OK" }] }]
                    })
                });

                if(response.ok) {
                    isApiConnected = true;
                    statusIndicator.className = 'status-indicator connected';
                    statusIndicator.style.background = '';
                    addChatMessage("AI", "Successfully connected to Gemini API! I'm ready to analyze your safety reports.");
                } else {
                    throw new Error("API call failed");
                }
            } catch (error) {
                isApiConnected = false;
                statusIndicator.className = 'status-indicator';
                statusIndicator.style.background = '';
                alert("Connection failed. Please check your API key.");
            }
        }

        async function callGemini(promptText, useAllFiles = false) {
            const apiKey = getApiKey();
            if(!apiKey) throw new Error("API Key missing");

            const url = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash:generateContent?key=${apiKey}`;
            
            let parts = [{ text: promptText }];

            // Attach PDFs as inline data
            if (useAllFiles && files.length > 0) {
                files.forEach((f, idx) => {
                    parts.push({ text: `\n--- Document ${idx + 1}: ${f.name} ---\n` });
                    parts.push({
                        inlineData: {
                            mimeType: f.mimeType,
                            data: f.base64
                        }
                    });
                });
            } else if (currentFileId) {
                const activeFile = files.find(f => f.id === currentFileId);
                parts.push({ text: `\n--- Currently Viewed Document: ${activeFile.name} ---\n` });
                parts.push({
                    inlineData: {
                        mimeType: activeFile.mimeType,
                        data: activeFile.base64
                    }
                });
            }

            const payload = {
                contents: [{ parts: parts }],
                generationConfig: {
                    temperature: 0.2 // Low temp for factual analysis
                }
            };

            const response = await fetch(url, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify(payload)
            });

            if (!response.ok) {
                const err = await response.json();
                throw new Error(err.error?.message || "API Error");
            }

            const data = await response.json();
            return data.candidates[0].content.parts[0].text;
        }

        // --- Chat Functionality ---
        function addChatMessage(sender, text) {
            const bubble = document.createElement('div');
            bubble.className = `chat-bubble ${sender === 'User' ? 'chat-user' : 'chat-ai'}`;
            // Simple markdown bold parsing for better readability
            const formattedText = text.replace(/\*\*(.*?)\*\*/g, '<strong>$1</strong>').replace(/\n/g, '<br>');
            bubble.innerHTML = formattedText;
            chatHistory.appendChild(bubble);
            chatHistory.scrollTop = chatHistory.scrollHeight;
        }

        async function sendMessage() {
            const text = chatInput.value.trim();
            if(!text) return;
            
            if(!isApiConnected) {
                alert("Please connect the API first.");
                return;
            }

            if(files.length === 0) {
                alert("Please upload a PDF document first.");
                return;
            }

            addChatMessage('User', text);
            chatInput.value = '';

            const bubbleId = 'loading-' + Date.now();
            const loadingBubble = document.createElement('div');
            loadingBubble.id = bubbleId;
            loadingBubble.className = 'chat-bubble chat-ai';
            loadingBubble.innerHTML = '<div class="loader"></div> Analyzing document(s)...';
            chatHistory.appendChild(loadingBubble);
            chatHistory.scrollTop = chatHistory.scrollHeight;

            const isCompare = text.toLowerCase().includes('compare') || text.toLowerCase().includes('all documents');

            try {
                const systemPrompt = "You are an expert AI Assistant specialized in analyzing Contractor Safety Statistics Reports. Answer the user's question accurately based strictly on the provided PDF document(s). If comparing, highlight differences in incidents, leading/lagging indicators, and hours worked. \n\nUser Question: " + text;
                const reply = await callGemini(systemPrompt, isCompare);
                document.getElementById(bubbleId).remove();
                addChatMessage('AI', reply);
            } catch (error) {
                document.getElementById(bubbleId).remove();
                addChatMessage('AI', 'Error: ' + error.message);
            }
        }

        chatInput.addEventListener('keypress', function (e) {
            if (e.key === 'Enter' && !e.shiftKey) {
                e.preventDefault();
                sendMessage();
            }
        });

        // --- Modal & Features ---
        function openModal(id) { document.getElementById(id).classList.add('active'); }
        function closeModal(id) { document.getElementById(id).classList.remove('active'); }

        // Mindmap Feature
        async function generateMindmap() {
            if(!isApiConnected || files.length === 0) { alert("API connection and a document are required."); return; }
            openModal('modal-mindmap');
            document.getElementById('mindmap-loader').classList.add('active');
            document.getElementById('mindmap-canvas').innerHTML = '';

            const prompt = `Analyze the provided Contractor Safety Statistics Report. Extract the core structure to build a tree/mindmap.
            You must return strictly valid JSON representing a hierarchical tree structure. Do not return markdown, just raw JSON.
            Structure MUST be:
            {
                "name": "Main Subject",
                "desc": "Minimalistic description",
                "children": [
                    { "name": "Subtopic", "desc": "Description", "children": [] }
                ]
            }
            Extract categories like 'Incident Rates', 'Leading Indicators', 'Audits', etc. Keep 'desc' very brief, summarizing the data inside (e.g., '5 Minor, 0 Major'). Limit depth to 3 levels.`;

            try {
                const response = await callGemini(prompt, false);
                // Extract JSON from response in case model adds markdown
                let jsonStr = response;
                const match = response.match(/\{[\s\S]*\}/);
                if (match) jsonStr = match[0];
                
                const treeData = JSON.parse(jsonStr);
                renderTree(treeData, document.getElementById('mindmap-canvas'));
                document.getElementById('mindmap-loader').classList.remove('active');
                
                // Reset Pan/Zoom
                scale = 1; pointX = 0; pointY = 0;
                applyTransform();
            } catch (e) {
                document.getElementById('mindmap-loader').classList.remove('active');
                document.getElementById('mindmap-canvas').innerHTML = `<div style="color:red; padding:20px;">Failed to generate mindmap: ${e.message}</div>`;
            }
        }

        // Recursive function to build the CSS Tree DOM
        function renderTree(nodeData, parentElement) {
            const ul = document.createElement('ul');
            const li = document.createElement('li');
            
            const nodeBox = document.createElement('div');
            nodeBox.className = 'node-box';
            nodeBox.innerHTML = `<span class="title">${nodeData.name || 'Node'}</span><span class="desc">${nodeData.desc || ''}</span>`;
            
            li.appendChild(nodeBox);

            if (nodeData.children && nodeData.children.length > 0) {
                nodeData.children.forEach(child => {
                    renderTree(child, li);
                });
            }

            ul.appendChild(li);
            parentElement.appendChild(ul);
        }

        // Pan and Zoom logic for Mindmap
        let scale = 1, panning = false, pointX = 0, pointY = 0, start = { x: 0, y: 0 };
        const viewport = document.getElementById('mindmap-viewport');
        const canvas = document.getElementById('mindmap-canvas');

        function applyTransform() {
            canvas.style.transform = `translate(${pointX}px, ${pointY}px) scale(${scale})`;
        }

        viewport.onmousedown = (e) => {
            e.preventDefault();
            panning = true;
            start = { x: e.clientX - pointX, y: e.clientY - pointY };
        };
        viewport.onmouseup = () => { panning = false; };
        viewport.onmouseleave = () => { panning = false; };
        viewport.onmousemove = (e) => {
            if (!panning) return;
            pointX = e.clientX - start.x;
            pointY = e.clientY - start.y;
            applyTransform();
        };
        viewport.onwheel = (e) => {
            e.preventDefault();
            const xs = (e.clientX - pointX) / scale;
            const ys = (e.clientY - pointY) / scale;
            const delta = (e.wheelDelta ? e.wheelDelta : -e.deltaY);
            (delta > 0) ? (scale *= 1.2) : (scale /= 1.2);
            
            // Limit scale
            scale = Math.min(Math.max(0.3, scale), 3);

            pointX = e.clientX - xs * scale;
            pointY = e.clientY - ys * scale;
            applyTransform();
        };


        // Presentation Feature
        async function generatePresentation() {
            if(!isApiConnected || files.length === 0) { alert("API connection and a document are required."); return; }
            openModal('modal-presentation');
            document.getElementById('pres-loader').classList.add('active');
            document.getElementById('slide-card').style.display = 'none';

            const prompt = `Act as an executive summarizer. Create a presentation summarizing the attached Contractor Safety Statistics Report.
            Return STRICTLY a JSON array of slide objects. No markdown blocks.
            Format:
            [
              { "title": "Slide 1 Title", "bullets": ["Point 1 with specific metric", "Point 2 with specific metric"] }
            ]
            Create exactly 5 slides: 1. Executive Summary, 2. Incident Overview, 3. Leading Indicators, 4. Areas of Concern, 5. Recommendations.`;

            try {
                const response = await callGemini(prompt, false);
                let jsonStr = response;
                const match = response.match(/\[[\s\S]*\]/);
                if (match) jsonStr = match[0];
                
                currentSlides = JSON.parse(jsonStr);
                currentSlideIndex = 0;
                
                document.getElementById('pres-loader').classList.remove('active');
                document.getElementById('slide-card').style.display = 'flex';
                updateSlideView();
            } catch (e) {
                document.getElementById('pres-loader').classList.remove('active');
                document.getElementById('slide-card').style.display = 'flex';
                document.getElementById('slide-card').innerHTML = `<div style="color:red;">Error generating presentation: ${e.message}</div>`;
            }
        }

        function updateSlideView() {
            if(currentSlides.length === 0) return;
            const slide = currentSlides[currentSlideIndex];
            
            document.getElementById('slide-title').textContent = slide.title || 'Slide';
            
            const contentDiv = document.getElementById('slide-content');
            contentDiv.innerHTML = '';
            const ul = document.createElement('ul');
            if(slide.bullets && Array.isArray(slide.bullets)) {
                slide.bullets.forEach(b => {
                    const li = document.createElement('li');
                    li.textContent = b;
                    ul.appendChild(li);
                });
            }
            contentDiv.appendChild(ul);

            document.getElementById('slide-current').textContent = currentSlideIndex + 1;
            document.getElementById('slide-total').textContent = currentSlides.length;
        }

        function prevSlide() {
            if (currentSlideIndex > 0) {
                currentSlideIndex--;
                updateSlideView();
            }
        }

        function nextSlide() {
            if (currentSlideIndex < currentSlides.length - 1) {
                currentSlideIndex++;
                updateSlideView();
            }
        }

        // Keyboard navigation for presentation
        document.addEventListener('keydown', (e) => {
            const presModal = document.getElementById('modal-presentation');
            if (presModal.classList.contains('active')) {
                if (e.key === 'ArrowRight') nextSlide();
                if (e.key === 'ArrowLeft') prevSlide();
            }
        });

    </script>
</body>
</html>
