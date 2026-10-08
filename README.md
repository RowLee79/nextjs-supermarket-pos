# Grocerly Supermarket POS

A Next.js 16 / React 19 supermarket POS demo with checkout, barcode lookup, quantity and percentage discount controls, cash/card/e-wallet recording, inventory, dashboard, and transaction history.

Portfolio demonstration by RowLee Tanawan. The implementation uses Next.js-compatible App Router APIs with the Vinext runtime; deployment targets Cloudflare Workers. It is not a conventional standalone `next dev` deployment.

## Features

- Select a product to add it to the cart. Use + and - to change quantities.
- Search by product name, brand, or barcode. Press Enter after typing a full barcode to add the matching item. A USB scanner configured as a keyboard with an Enter suffix can use the same field.
- Enter a percentage discount, select Proceed to payment, choose a method, and complete the sale. Cash requires an amount received; card and e-wallet payments must be confirmed externally first.
- Use Inventory to view stock or add a product. Use Dashboard and Transactions to inspect activity. Print receipt uses your browser print dialog.

## Technology

React, TypeScript, Next.js-compatible App Router, Vinext, Vite and responsive CSS. This POS demonstration stores activity in React memory; it resets on reload.

## Run locally

Node.js 22.13+ is required. Follow [installation, database initialization and walkthrough instructions](docs/SETUP.md), including the project-specific migration command. Dependencies and local database files are excluded from source control.

## Screenshots

Actual application screenshots are pending capture. No mockup is presented as a running application screenshot.

## Project layout

- `app/page.tsx`: application interface
- `app/globals.css`: responsive styling
- `app/api/`: server workflows, where applicable
- `db/` and `drizzle/`: schema and migrations, where applicable
- `docs/SETUP.md`: full setup, workflow rules and limitations

## Demo scope

Use fictional data for portfolio demonstrations. See [documented limitations](docs/SETUP.md) before deployment; authentication, payment integrations and operational safeguards vary by project and are not implied by the portfolio presentation.
