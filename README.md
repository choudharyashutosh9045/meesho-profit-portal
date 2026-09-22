# Meesho Profit Portal

A single-file, fully client-side dashboard for Meesho sellers. Upload your
Meesho exports and see Sale, Cost, GST, RTO, Customer Returns, and Net
Profit in one place — nothing is ever sent to a server, everything runs
and is stored (via `localStorage`) in your own browser.

**Live demo (once deployed):** `https://<your-username>.github.io/<repo-name>/`

## Features

- Upload 4 Meesho exports: Orders, Completed/Delivered (returns), Intransit
  (RTO), and the Payment file (.xlsx)
- Total Sale counted only from **delivered, non-returned** orders — RTO,
  customer returns and cancelled orders are excluded automatically
- Editable product cost price + other cost per SKU
- Editable customer-return loss, per individual order
- RTO configured as zero loss (edit the code if you want otherwise)
- GST % and Ads Cost, both editable
- Two-owner item-wise split, with a full owner performance table
- Received vs Pending payment tabs, cross-checked against the payment file
- Sales & orders trend chart, order-outcome donut, performance rate bars
- Date-range filter
- Safe against duplicate uploads — re-uploading an overlapping export only
  adds genuinely new rows (deduped by Sub Order No / Suborder Number)
- Multiple "businesses" (owners) supported from the top bar, each with its
  own separate saved data

## Run it locally

Just open `index.html` in a browser — no build step, no server, no
dependencies to install. It pulls PapaParse, SheetJS and Chart.js from a
CDN at load time, so you do need an internet connection when you open it.

## Deploy to GitHub Pages

1. Create a new repository on GitHub (public, so Pages is free) and add
   this `index.html` (and `.nojekyll`) to it.
2. In the repo, go to **Settings → Pages**.
3. Under "Build and deployment", set **Source** to "Deploy from a branch",
   pick the `main` branch and `/ (root)` folder, then **Save**.
4. Wait a minute, then your dashboard is live at
   `https://<your-username>.github.io/<repo-name>/`.

## Data & privacy

All uploaded data and settings are stored only in your browser's
`localStorage`, scoped to whatever domain you host this on. Nothing is
uploaded anywhere. Clearing your browser data (or using a different
browser/device) starts you with a blank slate for that domain.
