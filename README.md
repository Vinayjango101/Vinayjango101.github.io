<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>My Home Page</title>

  <!-- Font from Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">

  <!-- Basic styling -->
  <style>
    body {
      font-family: 'Open Sans', sans-serif;
      background-color: #f5f7fa;
      color: #333;
      margin: 0;
      padding: 0;
      line-height: 1.6;
    }

    header {
      background-color: #2c3e50;
      color: white;
      padding: 20px;
      text-align: center;
    }

    main {
      max-width: 800px;
      margin: 40px auto;
      padding: 0 20px;
      background: white;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
      border-radius: 6px;
    }

    h1, h2, h3 {
      color: #2c3e50;
    }

    code {
      background: #eee;
      padding: 2px 4px;
      border-radius: 4px;
    }

    a {
      color: #3498db;
    }

    footer {
      text-align: center;
      color: #777;
      font-size: 14px;
      padding: 20px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Welcome to My Home Page</h1>
    <p>Rendered from a Markdown file using GitHub Pages</p>
  </header>

  <main>
    <div id="content">Loading content...</div>
  </main>

  <footer>
    <p>&copy; 2025 Your Name. Powered by GitHub Pages.</p>
  </footer>

  <!-- Markdown renderer -->
  <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
  <script>
    fetch('README.md')
      .then(response => response.text())
      .then(markdown => {
        document.getElementById('content').innerHTML = marked.parse(markdown);
      })
      .catch(error => {
        document.getElementById('content').innerHTML = "<p>Failed to load content.</p>";
        console.error("Error loading README.md:", error);
      });
  </script>
</body>
</html>
