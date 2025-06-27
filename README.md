<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Shopify Theme Development - Local Setup Guide</title>
  <style>
    body { font-family: Arial, sans-serif; line-height: 1.6; padding: 2rem; background: #f9f9f9; }
    h1, h2 { color: #2c3e50; }
    ul { margin-left: 1.5rem; }
    code, pre { background: #f4f4f4; padding: 0.5rem; border-radius: 4px; display: block; margin: 1rem 0; }
    .structure pre { white-space: pre-wrap; }
  </style>
</head>
<body>

  <h1>Shopify Theme Development - Local Setup Guide</h1>

  <p>This repository provides instructions to set up and run a Shopify theme locally using the Shopify CLI.</p>

  <h2>📋 Requirements</h2>
  <p>Ensure the following dependencies are installed on your machine:</p>
  <ul>
    <li><strong>Node.js:</strong> v18.20+ or v20.10+</li>
    <li><strong>Package Manager:</strong> npm, Yarn (1.x), or pnpm</li>
    <li><strong>Git:</strong> v2.28.0 or higher</li>
    <li><strong>Ruby:</strong> Required for some CLI features</li>
    <li>Install Ruby (Ubuntu/Debian): <code>sudo apt-get install ruby-full</code></li>
  </ul>

  <h2>🛠 Installation Steps</h2>
  <ol>
    <li><strong>Install Shopify CLI globally:</strong>
      <pre><code>npm install -g @shopify/cli@latest</code></pre>
      <p>Alternatively, using Yarn or pnpm:</p>
      <pre><code>yarn global add @shopify/cli
# or
pnpm add -g @shopify/cli</code></pre>
    </li>

    <li><strong>Connect to your Shopify store:</strong>
      <pre><code>shopify theme dev --store=your-store-url</code></pre>
      <p>This will:</p>
      <ul>
        <li>Authenticate with your Shopify admin</li>
        <li>Pull theme files (if needed)</li>
        <li>Start a local dev server with hot reloading</li>
        <li>Open the theme preview in your browser</li>
      </ul>
    </li>
  </ol>

  <h2>📂 Recommended Project Structure</h2>
  <div class="structure">
    <pre>
shopify-theme/
├── assets/
├── config/
├── layout/
├── locales/
├── sections/
├── snippets/
├── templates/
├── .gitignore
├── README.md
├── package.json (optional)
└── theme.liquid
    </pre>
  </div>

  <p>If you're starting from scratch, run:</p>
  <pre><code>shopify theme init</code></pre>

  <h2>⚙️ Useful CLI Commands</h2>
  <ul>
    <li><code>shopify theme init</code>: Create a new theme based on Dawn (or other templates)</li>
    <li><code>shopify theme dev</code>: Run a local dev server with live reload</li>
    <li><code>shopify theme push</code>: Upload your local theme to Shopify</li>
    <li><code>shopify theme pull</code>: Download theme code from a connected Shopify store</li>
    <li><code>shopify theme serve</code>: Alias for <code>theme dev</code></li>
  </ul>

  <h2>💡 Tips</h2>
  <ul>
    <li>Use <strong>Shopify Dawn</strong> as a base theme for the best developer experience.</li>
    <li>Set store permanently with:<br>
      <code>shopify config set --store your-store-url</code>
    </li>
    <li>Use a <code>.env</code> file to store credentials securely (especially for CI/CD pipelines).</li>
  </ul>

  <h2>📘 Resources</h2>
  <ul>
    <li><a href="https://shopify.dev/docs/themes" target="_blank">Shopify Theme Development Docs</a></li>
    <li><a href="https://github.com/Shopify/shopify-cli" target="_blank">Shopify CLI GitHub</a></li>
  </ul>

  <h2>🔐 License</h2>
  <p>This project is for private or internal development. Refer to Shopify’s <a href="https://www.shopify.com/legal/terms" target="_blank">terms of service</a> for usage policies.</p>

</body>
</html>
