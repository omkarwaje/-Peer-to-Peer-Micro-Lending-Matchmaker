# KarzMitra

A standalone React recreation of the public KarzMitra micro-lending demo. Includes a responsive dark/light interface, home page, searchable loan marketplace, simulated split funding, EMI and affordability calculator, learning and legal pages, demo account screens, local dashboard, and a built-in help assistant.

## Run locally

Requires Node.js 20.19+ or 22.12+ (Node 24 recommended).

```sh
npm install
npm run dev
```

Open the localhost URL printed by Vite (usually http://127.0.0.1:5173).

## Production build

```sh
npm run build
npm run preview
```

## Deploy on Vercel

1. Push the contents of this folder to your GitHub repository.
2. Import the repository into Vercel.
3. Select the **Vite** framework preset. Build command: `npm run build`. Output: `dist`.
4. Deploy. `vercel.json` includes SPA rewrites for direct page links.

No environment variables or Base44 subscription are needed for this standalone demo. Google Fonts is optional; the interface falls back to Arial if unavailable.

## Project structure

- `src/main.jsx`: routes, pages, calculator, marketplace, demo dashboard, assistant.
- `src/styles.css`: responsive styles and dark/light themes.
- `public/favicon.svg`: local brand icon.
- `vercel.json`: deployment and client-side route configuration.

## Scope and data

This is an independently implemented recreation of the publicly visible reference, not an export of its private source or database. Public layout and flows are recreated; inaccessible authenticated pages are represented by an original demo dashboard. Sample borrower names are anonymized.

**This is not a real lending platform.** No money is transferred. Funding, requests, and sessions are simulated in browser localStorage. Login accepts sample credentials solely to enter the demo; passwords and email addresses are not stored or sent. Google OAuth, verified KYC, real AI, payments, notifications, and server-side account security are not connected. The assistant uses built-in responses, not an AI API. Clear browser site data to reset the demo.

Before any production use, implement and independently review a secure backend, real authentication, authorization, validated financial workflows, privacy controls, and applicable regulatory requirements. The included legal pages describe the demo, not production policies.

## Manual verification

- Home links, FAQ expand/collapse, dark/light mode, and responsive navigation.
- Marketplace category/search filters and contribution limits; local persistence after reload.
- Calculator: ₹10,000 at 12% over 12 months returns about ₹888/month; 0% interest returns principal / months.
- Demo registration password matching, dashboard request creation, and sign-out.
- Direct route loading under the Vercel SPA rewrite.

Reference: https://optimistic-karz-mitra-flow.base44.app/
