<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Perqless - About Me</title>
    <style>
        body {
            font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            line-height: 1.6;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            color: #333;
        }
        h1, h2, h3 {
            color: #111;
        }
        hr {
            border: none;
            border-top: 1px solid #ccc;
            margin: 20px 0;
        }
        code {
            background-color: #f4f4f4;
            padding: 2px 6px;
            border-radius: 4px;
            font-family: monospace;
        }
        a {
            color: #0066cc;
            text-decoration: none;
        }
        a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

    <h1>About Me</h1>

    <p><strong>Timezone:</strong> AEST</p>
    <p><strong>My Current Time:</strong> <span id="currentTime"></span></p>

    <script>
        function updateDateTime() {
            const now = new Date();
            const dateTimeString = now.getFullYear() + '-' + 
                String(now.getMonth() + 1).padStart(2, '0') + '-' + 
                String(now.getDate()).padStart(2, '0') + ' ' + 
                String(now.getHours()).padStart(2, '0') + ':' + 
                String(now.getMinutes()).padStart(2, '0') + ':' + 
                String(now.getSeconds()).padStart(2, '0');
            document.getElementById("currentTime").innerText = dateTimeString;
        }
        updateDateTime();
        setInterval(updateDateTime, 1000);
    </script>

    <p id="timeDiff"></p>
    <script>
        const myOffset = 10; 
        const visitorOffset = new Date().getTimezoneOffset() / -60;
        const diff = visitorOffset - myOffset;
        document.getElementById("timeDiff").innerText = 
            diff === 0 ? "We are in the same timezone!" : 
            `You are ${Math.abs(diff)} hour(s) ${diff > 0 ? "ahead" : "behind"} me.`;
    </script>

    <hr>

    <h2>Technical Skills</h2>

    <h3>Development &amp; Scripting</h3>
    <ul>
        <li><strong>Languages:</strong> Java, Kotlin, Python, Assembly</li>
        <li><strong>Minecraft:</strong> Plugin Development, Modding (Forge/Fabric), Skript</li>
        <li><strong>Web:</strong> HTML, CSS, and Markdown</li>
    </ul>

    <h3>Creative Media</h3>
    <ul>
        <li>Adobe Photoshop</li>
        <li>Adobe Premiere Pro</li>
    </ul>

    <h3>Systems &amp; OS</h3>
    <ul>
        <li><strong>Linux:</strong> Primarily Ubuntu (can use other distros)</li>
        <li><strong>Windows:</strong> 7, 10, and 11</li>
    </ul>

    <h2>Contact Me</h2>
    <p><strong>Discord Username:</strong> <code>perqless</code></p>

    <h2>Socials</h2>
    <ul>
        <li><strong>X (Twitter):</strong> <a href="https://x.com/perqIess" target="_blank" rel="noopener noreferrer">x.com</a></li>
        <li><strong>GitHub:</strong> <a href="https://github.com/Perqless" target="_blank" rel="noopener noreferrer">github.com</a></li>
    </ul>

</body>
</html>
