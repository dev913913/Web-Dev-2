# My React + Vite App

This project is a web application built with **React** and **Vite**. Below, I explain what these tools are, why we’re using them, how to set up the project, and why the setup is done this way. Check [extensions.md](./extensions.md) for recommended VS Code extensions to enhance your development experience, like snippets for JSX or linters for clean code.

## What Are React and Vite?

### React

- **What It Is**: React is a JavaScript library for building user interfaces, created by Facebook. It uses reusable components to construct your app’s UI.
- **Why We Use It**:
  - **Components**: Split your app into modular pieces, like `App.jsx`, making code reusable, as we discussed with JSX (JavaScript XML).
  - **Efficiency**: Updates only changed parts of the page, keeping apps fast.
  - **Community**: Widely used (e.g., Netflix), with many resources.
  - Here, React powers features like the counter in `App.jsx` or a potential to-do list.

### Vite

- **What It Is**: Vite is a modern build tool and development server for fast web app creation.
- **Why We Use It**:
  - **Speed**: Starts instantly and reloads changes live via Hot Module Replacement (HMR).
  - **Simplicity**: Less config than Create React App, great for Codespaces.
  - **Modern**: Uses ES Modules for quick builds.
  - Vite scaffolds our React app for a smooth cloud experience.

## Why This Setup?

React builds dynamic UIs with components, while Vite streamlines development. Together, they’re perfect for learning JSX or building apps like a to-do list. Codespaces runs it in the cloud, minimizing local setup, aligning with your GitHub workflow.

## Prerequisites

You need different tools depending on whether you’re using a **Desktop IDE (VS Code)** or **GitHub Codespaces**. Here’s what’s required, why, and how to set them up.

### Desktop IDE (VS Code)

- **Visual Studio Code**:
  - A code editor for JavaScript and React.
  - **Why**: Ideal for editing `App.jsx`, running terminals, and debugging.
  - **What to Do**: Download from [code.visualstudio.com](https://code.visualstudio.com/). Install and open your project folder.
- **Node.js** (version 16 or higher):
  - Includes `npm` for managing dependencies and scripts.
  - **Why**: Node.js runs Vite’s server (`npm run dev`), installs packages (`npm install`), and processes React’s JSX. Without it, the app won’t build or run.
  - **What to Do**:
    1. Check if installed: In VS Code’s terminal (`Ctrl + ~`), run:
       ```bash
       node -v
       ```
       - If v16.x or higher (e.g., v18.16.0), you’re ready.
       - If missing or old, install.
    2. Install Node.js:
       - Download LTS (e.g., v18.x) from [nodejs.org](https://nodejs.org/).
       - Follow the installer (Windows, macOS, Linux).
       - Verify:
         ```bash
         node -v
         npm -v
         ```
       - For details (e.g., using `nvm`), see: [How to Install Node.js](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-and-npm-on-ubuntu-20-04).
    - **Why Brief**: The installer is simple; the blog covers edge cases.

### GitHub Codespaces

- **GitHub Account with Codespaces Access**:
  - A cloud-based VS Code environment.
  - **Why**: Runs your project in the browser, no local setup, great for React.
  - **What to Do**: Sign in at [github.com](https://github.com). Codespaces offers free hours (check your plan).
- **Node.js** (version 16 or higher):
  - **Status**: Pre-installed in Codespaces (typically v18.x).
  - **Why**: Node.js runs Vite and React, enabling `npm` commands for your app.
  - **What to Do**:
    1. Verify:
       - In Codespaces’ terminal (`Ctrl + ~`), run:
         ```bash
         node -v
         ```
       - Expect v16.x or higher (e.g., v18.16.0). If shown, proceed—no action needed.
    2. If Missing (Rare):
       - Install via `nvm`:
         ```bash
         curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
         source ~/.bashrc
         nvm install 18
         ```
       - Verify:
         ```bash
         node -v
         npm -v
         ```
       - See: [Node.js in Dev Containers](https://code.visualstudio.com/docs/devcontainers/create-dev-container#_add-nodejs-to-the-container).
    - **Why Pre-installed**: Codespaces’ default container includes Node.js for web projects, saving time.

## How to Install and Set Up

With Node.js ready, follow these steps to set up the project.

### Step 1: Create a GitHub Repository

1. Go to [github.com](https://github.com), sign in.
2. Click **New repository**, name it (e.g., `my-react-vite-app`), add a README, create it.
3. For Codespaces: Click **Code** > **Codespaces** > **Create codespace on main**.
   - **Why**: Codespaces provides cloud VS Code with Node.js. For desktop, clone later.

### Step 2: Scaffold the React + Vite Project

1. In Codespaces (or VS Code terminal), run:
   ```bash
   npm create vite@latest my-react-app -- --template react
   ```
   - **Explanation**:
     - `npm create vite@latest`: Launches Vite’s CLI.
     - `my-react-app`: Names the folder.
     - `-- --template react`: Picks React with JavaScript.
     - **Why**: Vite creates a fast React app for JSX/components, as we discussed.
2. Confirm `create-vite` install if prompted (type `y`).
3. Choose **React** and **JavaScript**.
   - **Why**: JavaScript suits beginners, like your `App.jsx` work.

### Step 3: Install Dependencies

1. Enter the folder:
   ```bash
   cd my-react-app
   ```
   - **Why**: Commands need the project root.
2. Install dependencies:
   ```bash
   npm install
   ```
   - **Explanation**:
     - Installs `react`, `react-dom`, `@vitejs/plugin-react`.
     - Creates `node_modules`, `package-lock.json`.
     - **Why**: Enables React JSX and Vite, requiring Node.js.

### Step 4: Configure for Codespaces

1. Edit `package.json`, update `"scripts"`:
   ```json
   "scripts": {
     "dev": "vite --host",
     "build": "vite build",
     "preview": "vite preview"
   }
   ```
   - **Explanation**:
     - Added `--host` to `"dev"`.
     - Exposes the server to Codespaces’ network.
     - **Why**: Makes the app accessible in the cloud.

### Step 5: Run the App

1. Start the server:
   ```bash
   npm run dev
   ```
   - **Explanation**:
     - Runs Vite on port 5173, showing:
       ```
       Local:   http://localhost:5173/
       Network: http://<codespace-url>:5173/
       ```
     - **Why**: Enables live coding with HMR.
2. In Codespaces, click **Open in Browser** or use **Ports** tab (port 5173). In VS Code, visit `http://localhost:5173`.
   - **Why**: Shows the app’s UI.
3. See the React + Vite app with a counter.
   - **Why**: Verifies `App.jsx` works.

### Step 6: Save Your Work

1. Go to **Source Control** (left sidebar).
2. Commit (e.g., “Initial React + Vite setup”) and push.
   - **Why**: Saves to GitHub.

## Project Structure

- `src/App.jsx`:
  - Main component with JSX, like a counter or to-do list.
  - **Why**: Core UI, tied to JSX (JavaScript XML) questions.
- `src/main.jsx`:
  - Renders `App` to HTML’s `root`.
  - **Why**: Links React to the browser.
- `src/index.css`:
  - Global styles.
  - **Why**: Styles components.
- `package.json`:
  - Dependencies and scripts.
  - **Why**: Manages tools.
- `vite.config.js`:
  - Configures Vite.
  - **Why**: Supports JSX/HMR.

## Why This Setup?

- **Codespaces**: Cloud-based, minimal setup.
- **VS Code**: Flexible locally with Node.js.
- **Vite**: Fast React development.
- **React**: Dynamic UIs, like `App.jsx` exports.
- **--host**: Cloud accessibility.

## Recommended Tools

Check [extensions.md](./extensions.md) for recommended VS Code extensions to enhance your development experience, like snippets for JSX or linters for clean code.

## Running Later

1. Codespaces: Go to **Code** > **Codespaces** > select yours.
2. VS Code: Open the project folder.
3. Run:
   ```bash
   cd my-react-app
   npm run dev
   ```
4. Use the forwarded URL or `localhost:5173`.

## Troubleshooting

- **Port Not Forwarded** (Codespaces):
  - Check **Ports** tab; make 5173 public.
  - **Why**: Needed for cloud access.
- **Double Console Logs**:
  - `console.log` in `App.jsx` (e.g., “Hello, world”) runs twice due to `<React.StrictMode>` in `main.jsx`.
  - **Why**: Strict Mode checks bugs in dev, as we debugged—normal, gone in production (`npm run build`).
- **Node.js Issues**:
  - Codespaces: Reinstall via `nvm` if `node -v` fails (see Prerequisites).
  - VS Code: Ensure Node.js in PATH; reinstall if needed.
  - **Why**: Node.js runs Vite/React.

Start editing `src/App.jsx` to build your app, like resuming the to-do list we paused!