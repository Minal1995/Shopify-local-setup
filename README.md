<h1>Shopify Theme Development - Local Setup Guide</h1>

<p>This repository provides instructions to set up and run a Shopify theme locally using the Shopify CLI.</p>

  <div class="section">
    <h2>✅ Requirements</h2>
    <p>Ensure the following dependencies are installed on your machine:</p>
    <ul>
      <li><strong>Node.js:</strong> v18.20+ or v20.10+</li>
      <li><strong>Package Manager:</strong> npm, Yarn (1.x), or pnpm</li>
      <li><strong>Git:</strong> v2.28.0 or higher</li>
      <li><strong>Ruby:</strong> (for some CLI features)</li>
    </ul>
    <p>Install Ruby (Ubuntu/Debian):</p>
    <pre><code>sudo apt-get install ruby-full</code></pre>
  </div>

  <div class="section">
    <h2>🚀 Installation Steps</h2>

    <h3>1. Install Shopify CLI globally</h3>
    <pre><code>npm install -g @shopify/cli@latest</code></pre>

    <p>Alternatively, using Yarn or pnpm:</p>
    <pre><code>yarn global add @shopify/cli

  <code>pnpm add -g @shopify/cli</code>

    <h3>2. Connect to your Shopify store</h3>
    <p>Use the following command to start developing your theme locally. Replace <code>your-store-url</code> with your store’s domain (e.g., <code>my-store.myshopify.com</code>):</p>
    <pre><code>shopify theme dev --store=your-store-url</code></pre>

    <p>This will:</p>
    <ul>
      <li>Authenticate with your Shopify admin</li>
      <li>Pull your theme files (if needed)</li>
      <li>Start a local development server with hot reloading</li>
      <li>Open your theme preview in the browser</li>
    </ul>
  </div>

  <div class="section">
    <h2>📂 Recommended Project Structure</h2>
    <pre><code>shopify-theme/
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
└── theme.liquid</code></pre>

    <p>If you're starting from scratch, you can initialize a new theme using:</p>
    <pre><code>shopify theme init</code></pre>
  </div>

  <div class="section">
    <h2>🛠 Useful CLI Commands</h2>
    <ul>
      <li><code>shopify theme init</code>: Create a new theme based on Dawn (or other templates)</li>
      <li><code>shopify theme dev</code>: Run a local dev server with live reload</li>
      <li><code>shopify theme push</code>: Upload your local theme to Shopify</li>
      <li><code>shopify theme pull</code>: Download theme code from a connected Shopify store</li>
      <li><code>shopify theme serve</code>: (Alias for theme dev)</li>
    </ul>
  </div>

  <div class="section">
    <h2>💡 Tips</h2>
    <ul>
      <li>For better dev experience, use Shopify Dawn as a base theme.</li>
      <li>You can set the store permanently using:</li>
    </ul>
    <pre><code>shopify config set --store your-store-url</code></pre>
    <ul>
      <li>Add a <code>.env</code> file to store credentials securely (if needed for CI/CD).</li>
    </ul>
  </div>

  <div class="section">
    <h2>📘 Resources</h2>
    <ul>
      <li><a href="https://shopify.dev/docs/themes" target="_blank">Shopify Theme Dev Docs</a></li>
      <li><a href="https://github.com/Shopify/shopify-cli" target="_blank">Shopify CLI GitHub</a></li>
    </ul>
  </div>

  <div class="section">
    <h2>🔐 License</h2>
    <p>This project is for private or internal development. Refer to <a href="https://www.shopify.com/legal/terms" target="_blank">Shopify’s terms of service</a> for usage policies.</p>
  </div>

</body>
</html>
