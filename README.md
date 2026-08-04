 # JSON Wallet

  A fast, free, privacy-first **JSON editor and formatter** for developers — live at
  **[jsonwallet.com](https://jsonwallet.com)**.

  JSON Wallet lets you format, validate, compare, repair and transform JSON entirely in your
  browser. Nothing you paste is ever uploaded to a server. The name comes from the multi-tab
  design: like a wallet holds several cards, JSON Wallet holds several JSON documents side by
  side.

  > **Note:** JSON Wallet is a developer tool for editing JSON data. It is **not** a
  > cryptocurrency wallet, blockchain product, or any kind of financial application.

  ## Features

  - **Format & beautify** — turn minified JSON into clean, indented output
  - **Minify** — compress formatted JSON back to a single compact line
  - **Validate** — live valid/invalid feedback with the exact error location
  - **Tree & table views** — explore nested structures interactively
  - **Compare (diff)** — see exactly what changed between two JSON documents
  - **Repair** — auto-fix trailing commas, missing quotes, unescaped characters and more
  - **Escape / unescape / stringify / unstringify** — transform JSON for embedding
  - **URL encode / decode** — `encodeURIComponent` / `decodeURIComponent` helpers
  - **Multi-tab editing** — keep several documents open at once
  - **Dark mode** and a built-in product tour

  ## Privacy

  Everything runs locally in your browser using JavaScript. Your JSON is **never uploaded,
  logged, or stored on a server** — it only lives in your browser's local storage so your tabs
  survive a reload. The only exception is the optional "Share" feature, which you explicitly
  trigger; shared documents are stored for up to 24 hours. See the
  [Privacy Policy](https://jsonwallet.com/privacy-policy).

  ## Guides
  
  Alongside the tool we publish in-depth, hand-written JSON guides at
  [jsonwallet.com/guides](https://jsonwallet.com/guides), covering everything from "What is
  JSON?" to JSON Schema, JSONPath, and working with very large files. Every code sample and
  error message is tested in the editor before publishing.

  ## Tech stack

  - **React 19** + **TypeScript**
  - **Vite** (client build + SSR)
  - **React Router**
  - Static prerendering — each route is rendered to real HTML for SEO and crawlability

  ## Getting started

  ```bash
  # install dependencies
  npm install

  # start the dev server
  npm run dev

  # type-check, build the client + SSR bundles, and prerender all routes
  npm run build

  # preview the production build locally
  npm run preview

  # lint
  npm run lint

  The build script runs tsc, builds the client and SSR bundles, then runs
  scripts/prerender.mjs to generate static HTML for every route into dist/.

  Project structure

  src/
    components/     UI components (editor panel, modals, layout, tree view…)
    pages/          Route pages (Home, Guides, About, Contact, Privacy, Terms…)
    pages/guides/   Guide articles registry (content + metadata)
    utils/          SEO hook, JSON repair, share API helpers
    entry-server.tsx  SSR entry + per-route SEO metadata
  scripts/
    prerender.mjs   Renders each route to static HTML
  public/           robots.txt, sitemap.xml, manifest.json, ads.txt, favicon

  Contributing & contact

  JSON Wallet is independently built and maintained. Found a bug or have a feature idea?
  Email help@jsonwallet.com or open an issue.

  A few things to check before you commit:
  - **License** — I left it out since I don't know your intent. Add a `## License` section (e.g. MIT) and a `LICENSE` file if you want it open source, or state "All rights reserved."
  - **Author/contact** — swap `help@jsonwallet.com` if you use a different address.
