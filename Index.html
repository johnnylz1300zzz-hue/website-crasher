<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website Frontend Stress Tester</title>
    <style>
        :root {
            --bg-primary: #0d1117;
            --bg-secondary: #161b22;
            --bg-tertiary: #21262d;
            --border-color: #30363d;
            --text-primary: #c9d1d9;
            --text-secondary: #8b949e;
            --accent-color: #58a6ff;
            --danger-color: #f85149;
            --success-color: #3fb950;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Noto Sans", Helvetica, Arial, sans-serif;
            background-color: var(--bg-primary);
            color: var(--text-primary);
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        .container {
            width: 100%;
            max-width: 900px;
            background-color: var(--bg-secondary);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 30px;
            box-shadow: 0 16px 32px rgba(0, 0, 0, 0.75);
        }

        h1 {
            color: var(--text-primary);
            text-align: center;
            margin-bottom: 10px;
            font-weight: 600;
        }

        .subtitle {
            color: var(--text-secondary);
            text-align: center;
            margin-bottom: 30px;
            font-size: 0.9em;
        }

        .input-group {
            margin-bottom: 25px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            color: var(--text-secondary);
            font-size: 0.9em;
            font-weight: 500;
        }

        input[type="text"] {
            width: 100%;
            padding: 12px;
            background-color: var(--bg-tertiary);
            border: 1px solid var(--border-color);
            border-radius: 6px;
            color: var(--text-primary);
            font-size: 1em;
            box-sizing: border-box;
            transition: border-color 0.2s;
        }

        input[type="text"]:focus {
            outline: none;
            border-color: var(--accent-color);
        }

        .button-group {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-bottom: 25px;
        }

        button {
            padding: 12px 20px;
            border: none;
            border-radius: 6px;
            font-size: 1em;
            font-weight: 500;
            cursor: pointer;
            transition: background-color 0.2s, transform 0.1s;
        }

        button:active {
            transform: scale(0.98);
        }

        .btn-primary {
            background-color: var(--accent-color);
            color: white;
        }

        .btn-primary:hover {
            background-color: #4a96e9;
        }

        .btn-danger {
            background-color: var(--danger-color);
            color: white;
        }

        .btn-danger:hover {
            background-color: #da3633;
        }

        .btn-warning {
            background-color: #d29922;
            color: white;
        }

        .btn-warning:hover {
            background-color: #b8851c;
        }

        .btn-success {
            background-color: var(--success-color);
            color: white;
        }

        .btn-success:hover {
            background-color: #35a045;
        }

        .btn-stop {
            background-color: var(--bg-tertiary);
            color: var(--text-primary);
            border: 1px solid var(--danger-color);
        }

        .btn-stop:hover {
            background-color: var(--danger-color);
        }

        .log-container {
            background-color: var(--bg-tertiary);
            border: 1px solid var(--border-color);
            border-radius: 6px;
            padding: 15px;
            height: 250px;
            overflow-y: auto;
            font-family: "Consolas", "Monaco", "Courier New", monospace;
            font-size: 0.9em;
        }

        .log-entry {
            margin-bottom: 5px;
            padding: 2px 0;
        }

        .log-entry.info {
            color: var(--accent-color);
        }

        .log-entry.success {
            color: var(--success-color);
        }

        .log-entry.error {
            color: var(--danger-color);
        }

        .log-entry.warning {
            color: #d29922;
        }

        .iframe-container {
            position: absolute;
            left: -9999px;
            top: -9999px;
            width: 1px;
            height: 1px;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Website Frontend Stress Tester</h1>
        <p class="subtitle">For educational and authorized testing purposes only.</p>

        <div class="input-group">
            <label for="targetUrl">Target Website URL</label>
            <input type="text" id="targetUrl" placeholder="https://example.com">
        </div>

        <div class="button-group">
            <button class="btn-primary" onclick="startResourceOverload()">Resource Overload</button>
            <button class="btn-warning" onclick="startDomBombardment()">DOM Bombardment</button>
            <button class="btn-danger" onclick="startEventLoopFlood()">Event Loop Flood</button>
            <button class="btn-success" onclick="startStyleRecalculation()">Style Recalculation</button>
        </div>
        
        <div class="button-group">
             <button class="btn-stop" onclick="stopAllTests()">⛔ Stop All Tests</button>
        </div>

        <div class="input-group">
            <label for="log">Activity Log</label>
            <div id="log" class="log-container"></div>
        </div>
    </div>

    <div id="iframeContainer" class="iframe-container"></div>

    <script>
        const logContainer = document.getElementById('log');
        const iframeContainer = document.getElementById('iframeContainer');
        let activeTests = [];

        function log(message, type = 'info') {
            const entry = document.createElement('div');
            entry.className = `log-entry ${type}`;
            entry.textContent = `[${new Date().toLocaleTimeString()}] \${message}`;
            logContainer.appendChild(entry);
            logContainer.scrollTop = logContainer.scrollHeight;
        }

        function getUrl() {
            const urlInput = document.getElementById('targetUrl').value;
            if (!urlInput || !urlInput.startsWith('http')) {
                log('Invalid URL. Please enter a full URL starting with http:// or https://', 'error');
                return null;
            }
            return urlInput;
        }

        function createIframe() {
            const iframe = document.createElement('iframe');
            iframe.style.width = '800px';
            iframe.style.height = '600px';
            iframe.style.border = 'none';
            iframeContainer.appendChild(iframe);
            return iframe;
        }

        function startResourceOverload() {
            const url = getUrl();
            if (!url) return;

            log(`Starting Resource Overload on \${url}`, 'warning');
            for (let i = 0; i < 10; i++) {
                const iframe = createIframe();
                iframe.src = url;
                activeTests.push(iframe);
            }
            log('Created 10 iframes. Monitor your browser's performance.', 'success');
        }

        function startDomBombardment() {
            const url = getUrl();
            if (!url) return;

            log(`Starting DOM Bombardment on \${url}`,
