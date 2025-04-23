# Recommended VS Code Extensions

This file lists recommended VS Code extensions to enhance your React + Vite development in GitHub Codespaces (or locally). They’re grouped by purpose—React development, formatting, productivity, debugging, utilities—for coding, error-catching, and productivity. Below is a list of extensions and authors, linking to details on what each does and why it’s useful.

## Extension List

- [ES7+ React/Redux/React-Native Snippets](#es7-reactreduxreact-native-snippets) by dsznajder
- [ES7 React/Redux/GraphQL/React-Native snippets](#es7-reactreduxgraphqlreact-native-snippets) by rodrigovallades
- [Auto Import](#auto-import) by steoates
- [Auto Import - ES6, TS, JSX, TSX](#auto-import---es6-ts-jsx-tsx) by Sergey Korenuk
- [Prettier - Code formatter](#prettier---code-formatter) by Prettier
- [ESLint](#eslint) by Dirk Baeumer
- [Auto Close Tag](#auto-close-tag) by Jun Han
- [Bracket Pair Colorization Toggler](#bracket-pair-colorization-toggler) by Dzhavat Ushev
- [Bracket Pair Color DLW](#bracket-pair-color-dlw) by Bracket Pair Color DLW
- [Code Runner](#code-runner) by Jun Han
- [Live Preview](#live-preview) by Microsoft
- [Tailwind CSS IntelliSense](#tailwind-css-intellisense) by Tailwind Labs
- [Rainbow CSV](#rainbow-csv) by mechatroner

## Where to Install Extensions

In Codespaces (or VS Code):
   - Click **Extensions** icon (left sidebar, square with four squares).
   - Search by name (e.g., “Prettier”).
   - Click **Install**.

## Extensions

### React Development

These speed up React and JSX coding in `src/App.jsx`.

#### ES7+ React/Redux/React-Native Snippets

- **What It Does**: Shortcuts (`rafc`, `rafce`) for React component boilerplate.
- **Why Use It**: Type `rafc` in `App.jsx` for instant components, saving time, as we discussed with JSX.

#### ES7 React/Redux/GraphQL/React-Native snippets

- **What It Does**: Snippets for React, Redux, GraphQL (`imr`, `rcc`).
- **Why Use It**: More options for advanced setups. Use this or dsznajder’s to avoid overlap—dsznajder’s suits basic React.

#### Auto Import

- **What It Does**: Auto-adds ES6 imports (e.g., `useState` from `react`).
- **Why Use It**: Cuts manual imports in `App.jsx`, preventing errors.

#### Auto Import - ES6, TS, JSX, TSX

- **What It Does**: Auto-completes imports for JSX/TypeScript.
- **Why Use It**: Great for `App.jsx` and future TypeScript. Pick this over steoates’ if TypeScript is planned.

### Code Formatting and Linting

These keep code clean, building on our double-log debugging.

#### Prettier - Code formatter

- **What It Does**: Auto-formats JSX, JavaScript, CSS.
- **Why Use It**: Tidies `App.jsx`, `index.css` effortlessly, pairs with ESLint.

#### ESLint

- **What It Does**: Flags React/JavaScript errors (e.g., missing props).
- **Why Use It**: Catches bugs in `App.jsx`, like export issues we noted.

#### Auto Close Tag

- **What It Does**: Adds closing JSX/HTML tags (e.g., `<div></div>`).
- **Why Use It**: Speeds JSX in `App.jsx`, avoids tag errors.

### Productivity and Visualization

These aid navigation in React projects.

#### Bracket Pair Colorization Toggler

- **What It Does**: Toggles color-coding for brackets.
- **Why Use It**: Clarifies nested JSX in `App.jsx`. Toggle off if distracting.

#### Bracket Pair Color DLW

- **What It Does**: Customizes bracket colorization.
- **Why Use It**: Helps read complex JSX. Choose this or Toggler.

### Debugging and Testing

These complement Vite’s server for testing.

#### Code Runner

- **What It Does**: Runs JavaScript snippets with a click.
- **Why Use It**: Tests logic outside `App.jsx`, good for experiments.

#### Live Preview

- **What It Does**: Previews HTML/apps in VS Code.
- **Why Use It**: Debugs `index.html` or React output alongside Vite.

### Optional Utilities

These support future tasks like styling.

#### Tailwind CSS IntelliSense

- **What It Does**: Autocompletes Tailwind classes.
- **Why Use It**: Prepares for styling `App.jsx`, as we discussed. Add Tailwind first.

#### Rainbow CSV

- **What It Does**: Colors CSV files for readability.
- **Why Use It**: Useful for data tasks (e.g., to-do CSVs) later.

## Why This Order?

- **React First**: Snippets/imports for `App.jsx` coding.
- **Formatting**: Prettier/ESLint for quality, tied to log fixes.
- **Productivity**: Bracket tools for JSX navigation.
- **Debugging**: Runner/Preview for tests.
- **Utilities**: Tailwind/CSV for future needs.

## Setup Tip

Reload Codespaces after installing (click **Reload**). Try `rafc` in `App.jsx`, save for Prettier, or check ESLint. Configure Tailwind before using IntelliSense.
