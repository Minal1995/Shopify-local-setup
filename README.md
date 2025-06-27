# Shopify Theme Development - Local Setup Guide

This repository provides instructions to set up and run a Shopify theme locally using the Shopify CLI.

---

## 📋 Requirements

Ensure the following dependencies are installed on your machine:

- **Node.js**: v18.20+ or v20.10+
- **Package Manager**: npm, Yarn (1.x), or pnpm
- **Git**: v2.28.0 or higher
- **Ruby**: Required for some CLI features  
  Install Ruby (Ubuntu/Debian):  
  ```bash
  sudo apt-get install ruby-full
🛠 Installation Steps
1. Install Shopify CLI globally
bash
Copy
Edit
npm install -g @shopify/cli@latest
Alternatively, using Yarn or pnpm:

bash
Copy
Edit
yarn global add @shopify/cli
# or
pnpm add -g @shopify/cli
2. Connect to your Shopify store
Use the following command to start developing your theme locally. Replace your-store-url with your store’s domain (e.g., my-store.myshopify.com):

bash
Copy
Edit
shopify theme dev --store=your-store-url
This will:

Authenticate with your Shopify admin

Pull your theme files (if needed)

Start a local development server with hot reloading

Open your theme preview in the browser

📂 Recommended Project Structure
arduino
Copy
Edit
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
If you're starting from scratch, you can initialize a new theme using:

bash
Copy
Edit
shopify theme init
⚙️ Useful CLI Commands
shopify theme init – Create a new theme based on Dawn (or other templates)

shopify theme dev – Run a local development server with live reload

shopify theme push – Upload your local theme to Shopify

shopify theme pull – Download theme code from a connected Shopify store

shopify theme serve – Alias for theme dev

💡 Tips
For better dev experience, use Shopify Dawn as a base theme.

You can set the store permanently using:

bash
Copy
Edit
shopify config set --store your-store-url
Add a .env file to store credentials securely (recommended for CI/CD).

📘 Resources
Shopify Theme Development Docs

Shopify CLI GitHub Repository

🔐 License
This project is for private or internal development. Refer to Shopify’s Terms of Service for usage policies.

yaml
Copy
Edit

---

### ✅ How to Use
1. Save the above content into a file named `README.md`.
2. Commit and push to your repository.
3. GitHub will automatically render this Markdown into a clean and readable format.

Let me know if you'd like this saved as a downloadable file.
