# Grocerly Supermarket POS — Source Code

A Next.js 16 / React 19 supermarket POS demo with checkout, barcode lookup, quantity and percentage discount controls, cash/card/e-wallet recording, inventory, dashboard, and transaction history.

## Requirements

- Node.js 22.13 or newer
- pnpm (recommended: run `corepack enable` to make it available)

## Run locally

1. Extract this ZIP file.
2. Open a terminal in the extracted `supermarket-pos` folder.
3. Run `pnpm install`.
4. Run `pnpm dev`.
5. Open the local address printed in your terminal (normally http://localhost:5173).

On Windows, run these commands in PowerShell or the VS Code terminal. If `corepack` is unavailable, install pnpm with `npm install -g pnpm`.

## Try it

- Select a product to add it to the cart. Use + and - to change quantities.
- Search by product name, brand, or barcode. Press Enter after typing a full barcode to add the matching item. A USB scanner configured as a keyboard with an Enter suffix can use the same field.
- Enter a percentage discount, select Proceed to payment, choose a method, and complete the sale. Cash requires an amount received; card and e-wallet payments must be confirmed externally first.
- Use Inventory to view stock or add a product. Use Dashboard and Transactions to inspect activity. Print receipt uses your browser print dialog.

## Project structure

- `app/page.tsx`: product data and interactive POS screens
- `app/globals.css`: responsive styling
- `app/layout.tsx`: page metadata
- `public/favicon.svg`: app icon
- `package.json` / `pnpm-lock.yaml`: dependencies

## Important limitation

This is a functional front-end demo. The initial transactions are sample records. Cart, added products, stock adjustments, and new transactions live only in React memory and reset when the page reloads. There is no login, shared database, tax engine, payment gateway, refund workflow, or multi-register synchronization. Do not use it for real financial records without implementing and testing those server-side features.

## Build

Run `pnpm build` to check the production bundle. This project was originally hosted with a compatible Cloudflare/Vinext build. For another hosting provider, adapt deployment configuration and verify the framework build there.
