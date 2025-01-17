<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Advanced Website Creator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            padding: 0;
        }
        input, textarea, button {
            width: 100%;
            margin: 10px 0;
            padding: 10px;
            font-size: 16px;
        }
        button {
            background-color: #007BFF;
            color: white;
            border: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Create Your Advanced Website</h1>

    <label for="title">Website Title</label>
    <input type="text" id="title" placeholder="Enter website title" />

    <label for="header">Header</label>
    <input type="text" id="header" placeholder="Enter header text" />

    <label for="footer">Footer</label>
    <input type="text" id="footer" placeholder="Enter footer text" />

    <label for="sections">Sections (JSON format)</label>
    <textarea id="sections" placeholder='[{"title": "Section 1", "content": "This is section 1."}, {"title": "Section 2", "content": "This is section 2."}]'></textarea>

    <button onclick="submitForm()">Create Website</button>

    <script>
        async function submitForm() {
            const title = document.getElementById('title').value;
            const header = document.getElementById('header').value;
            const footer = document.getElementById('footer').value;
            const sections = JSON.parse(document.getElementById('sections').value);

            const response = await fetch('/create-website', {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({ title, header, footer, sections })
            });

            const result = await response.json();
            if (result.success) {
                alert(`Website created! File saved at: ${result.filePath}`);
            } else {
                alert('Error creating website: ' + result.message);
            }
        }
    </script>
</body>
</html>
