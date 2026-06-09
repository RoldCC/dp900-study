# DP-900 Study App

An interactive single-page study tool for the **Microsoft Azure Data Fundamentals (DP-900)** certification exam.

🔗 **[Live app →](https://roldcc.github.io/dp900-study)**

---

## Features

- **Accordion summaries** — topic-by-topic expandable sections with concept explanations and exam tips
- **Flashcards** — 3D flip animation, shuffle, keyboard navigation
- **Mind maps** — D3.js interactive force-directed graphs per domain
- **Quizzes** — randomised 10-question sessions drawn from a pool of 56–65 questions per domain, with immediate feedback and explanations

---

## Exam Domains

| Domain | Coverage |
|---|---|
| Core data concepts | Data formats, file types, OLTP/OLAP, ETL/ELT, batch/stream, Lambda architecture, Microsoft Fabric |
| Relational data in Azure | SQL (DDL/DML/DCL/TCL), normalisation, Azure SQL DB / MI / VMs, JOINs, constraints |
| Non-relational data in Azure | Blob Storage, Azure Files, Table Storage, Cosmos DB (APIs + consistency), storage redundancy |
| Analytics in Azure | Synapse, Databricks, ADF, ADLS Gen2, Stream Analytics, Power BI, Fabric, HDInsight, Analysis Services |

---

## Stack

- Pure HTML + CSS + JavaScript — no framework, no build step, no npm
- [D3.js v7](https://d3js.org/) via CDN for mind maps
- [Inter](https://fonts.google.com/specimen/Inter) via Google Fonts
- Deployed to **GitHub Pages** via GitHub Actions

---

## Usage

**Option 1 — local:** clone the repo and double-click `index.html`

**Option 2 — live:** visit the [GitHub Pages URL](https://roldcc.github.io/dp900-study)

```bash
git clone https://github.com/RoldCC/dp900-study.git
cd dp900-study
open index.html   # macOS
xdg-open index.html  # Linux
```

---

## Project Structure

```
dp900-study/
├── index.html          ← entire app (HTML + CSS + JS inline)
├── sources.md          ← MS Learn source URLs used for all content
├── context.md          ← visual design specification
├── CLAUDE.md           ← project rules
├── CLAUDE_LAW.md       ← development guidelines
└── .github/
    └── workflows/
        └── deploy.yml  ← GitHub Actions deployment to Pages
```

---

## Content Sources

All study content is sourced directly from [Microsoft Learn](https://learn.microsoft.com/en-us/credentials/certifications/exams/dp-900/) — no invented content. Source URLs are listed in [`sources.md`](./sources.md).

---

## Deployment

Every push to `main` triggers a GitHub Actions workflow that deploys the repo root to GitHub Pages. No build step required.
