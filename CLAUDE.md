# DP-900 Study Page

## What this is
A single static HTML page for studying the Azure Data Fundamentals (DP-900) certification.
One `index.html` — no framework, no build step, no npm, no API keys.
Deployed to GitHub Pages via GitHub Actions.

## Behavioral rules
Read `CLAUDE_LAW.md` before doing anything. No exceptions.

---

## Stack
- `index.html` — all HTML, CSS, and JS inline in one file
- D3.js for mind maps (CDN: cdnjs.cloudflare.com only)
- No npm, no package.json, no node_modules, no build step

---

## Content source
Read `sources.md` first. Fetch each URL. Extract content. Hardcode into `index.html`.
Never invent content from memory — only use what the sources say.
If a URL is unreachable, stop and report it.

---

## DP-900 domains (25% each)
- Core data concepts
- Relational data in Azure
- Non-relational data in Azure
- Analytics in Azure

---

## Page structure
Four domain tabs. Each tab has:

1. **Summary** — accordion sections per topic (concept → explanation → exam tip)
2. **Flashcards** — flip animation, front: question, back: answer, 10+ cards per domain
3. **Mind map** — D3.js interactive graph, central node = domain, child nodes = services/concepts
4. **Quiz** — 5 static questions, 4 options, immediate feedback, explanation after answer

---

## Rules
1. Read `sources.md` before writing any content
2. Never hardcode content from memory
3. No features beyond what is listed above
4. `index.html` must work by double-clicking locally (no server required)
5. Mobile-first: design for 375px, scale up
6. Before marking done: open in browser and verify every section works
