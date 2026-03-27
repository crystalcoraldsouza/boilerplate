# Setting up React Vite boilerplate

## Create your project directory

> mkdir react-vite-from-scratch

> cd react-vite-from-scratch

## Create your README.md and .gitignore files

## Create your package.json

> npm init -y

## Install core React dependencies

> npm install react react-dom

## Install Vite as a devDependency

> npm install -D vite

## Install React Plugin for Vite as a devDependency

> npm install -D @vitejs/plugin-react

## Create Folder Structure

react-from-scratch/
│
├── index.html
├── vite.config.js
├── src/
│ ─ main.jsx
│└─ App.jsx

## Setup index.html

```js
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>React From Scratch</title>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.jsx"></script>
  </body>
</html>
```

## Create React Entry (main.jsx)

```js
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
);
```

## Create App Component

```js
export default function App() {
  return <h1>Hello, React from Scratch</h1>;
}
```

## Configure Vite (vite.config.js)

```js
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";

export default defineConfig({
  plugins: [react()],
});
```

## Add Scripts to package.json

```js
"scripts": {
  "dev": "vite",
  "build": "vite build",
  "preview": "vite preview"
}
```

## Run the App

> npm run dev
