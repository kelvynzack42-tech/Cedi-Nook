# CediNook

CediNook is an offline-first personal finance and savings tracker that you can install on your phone. All amounts are entered by you — it never connects to bank accounts or wallets, reads messages, or moves money.

## What it does
- Savings goals with progress, deadlines and an Ahead / On track / Behind status.
- Daily income and expense tracking with search, filters, editing, duplicate warnings and manual recurring reminders. Budgets, bills, debts, assets and accounts (including mobile money, cash and bank accounts).
- Dashboard with monthly summaries, bill and category-budget alerts, and a backup reminder. JSON restore includes a contents preview before replacing local data.
- Reports, a savings coach, a planner and a financial health centre.
- Optional PIN lock. Your data stays on this device in the app. The included server API supports optional encrypted cloud snapshots when configured, but this app build has no in-app cloud account or sync controls. Export a backup from Settings at any time.

## Install on a phone
CediNook is a Progressive Web App. Deploy this folder to an HTTPS host, then:
- **Android (Chrome):** open the address, use **Install app** in the page or Chrome menu → **Install app**.
- **iPhone (Safari):** **Share** → **Add to Home Screen** → **Add**.

A ZIP opened directly from disk (`file://`) can be used in a browser but cannot be installed as an app.

## Run locally on Windows
1. Extract this ZIP. **Open the extracted folder that directly contains `index.html`, `package.json`, and `server.js`** — do not select the ZIP itself or its parent folder.
2. Install Node.js 20 or later.
3. Double-click `TEST_LOCAL.bat` (or open Command Prompt in this folder and run `npm install` followed by `npm start`).
4. Open `http://localhost:3000`.

The website entry file is `index.html` in this folder. The Node server serves it at `/` and serves the app assets from the same folder.

## Deploy to Render
1. Upload the **contents of this folder** to the top level of your GitHub repository. `index.html`, `package.json`, `server.js`, and `render.yaml` must all be visible at the repository root.
2. In Render, create a Blueprint from that repository and select `render.yaml`.
3. Render uses `npm install` to build and `npm start` to launch the app. The blueprint includes a PostgreSQL database and generates the encryption key.
4. After deployment, open the service URL. Check `/api/health` if you need to confirm the server is running.

If you deploy as a static site instead of using the included Node web service, the API-backed account and sync endpoints will not work. Use the included Render Blueprint for the complete app.

## Tests
`npm test`
