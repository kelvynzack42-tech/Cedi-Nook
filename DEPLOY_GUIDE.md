# CediNook — folder and deployment fix

This package is arranged with the website files at the project root.

## Required root files
- `index.html` — website entry page
- `package.json` — Node project configuration
- `server.js` — local and production web server
- `render.yaml` — Render Blueprint configuration

## Local start (Windows)
Extract the ZIP, open this folder, and double-click `TEST_LOCAL.bat`. Then visit http://localhost:3000.

## Render
Push the contents of this folder (not an enclosing `CediNook/` directory) to the root of your GitHub repository. The four required files above should be visible immediately in the repository file list. Create a Render Blueprint using `render.yaml`.

The server serves `/` from the root `index.html`; it does not require a separate `public/` or `dist/` folder.
