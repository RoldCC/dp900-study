# Page Context & Design Spec

## Purpose
An interactive single-page study app for the DP-900 Azure Data Fundamentals certification.
The page must feel like a proper study tool — not a document dump.
Every section should encourage active learning, not passive reading.

---

## Visual Design

### Theme
- Dark mode only — no light mode toggle
- Background: #0f1117 (near black)
- Surface: #1a1d27 (cards, panels)
- Border: #2a2d3e (subtle separators)
- Primary accent: #6c63ff (purple — Azure-inspired)
- Success: #22c55e (correct answers, completed states)
- Danger: #ef4444 (wrong answers)
- Warning: #f59e0b (weak topics, watch out tips)
- Text primary: #e2e8f0
- Text secondary: #94a3b8
- Text muted: #475569

### Typography
- Font: Inter (Google Fonts CDN)
- Headings: 600 weight
- Body: 400 weight, 1.6 line-height
- Code/terms: monospace, accent color background

### Layout
- Max content width: 900px, centered
- Mobile-first: 375px base, scales up gracefully
- Consistent 16px/24px spacing grid
- No horizontal scroll at any viewport width

---

## Navigation
- Sticky top nav bar with 4 domain tabs
- Active tab: accent color underline + bold label
- Tab labels: short (Core / Relational / Non-Relational / Analytics)
- Smooth scroll to section on tab click
- On mobile: tabs scroll horizontally if needed (no wrapping)

---

## Sections per domain tab

### 1. Summary (accordion)
- Each accordion item: topic title + chevron icon
- Closed by default, one open at a time
- Inside each item:
  - Concept explanation (2-4 sentences, plain English)
  - "When to use" bullet list
  - Exam tip box (⚠️ yellow border, slightly different background)
- Smooth expand/collapse animation

### 2. Flashcards
- Card with CSS 3D flip on click (front → back)
- Front: question or concept name, centered, large text
- Back: answer + 1-line explanation, smaller text
- Progress indicator: "Card 3 of 12"
- Previous / Next buttons, keyboard arrow support
- Shuffle button
- Card counter resets on domain switch

### 3. Mind Map (D3.js)
- Dark background, colored nodes
- Central node: domain name (accent color, larger)
- First-level nodes: main services/concepts (white)
- Second-level nodes: details/sub-concepts (muted)
- Click a node: shows a tooltip with a 2-line description
- Drag nodes to reposition
- Scroll to zoom in/out
- Fit-to-screen button

### 4. Quiz
- One question at a time (not all at once)
- Question number + progress bar at top
- 4 answer options as clickable cards
- On selection:
  - Correct: card turns green, checkmark icon
  - Wrong: selected card turns red, correct card turns green
  - Explanation text appears below immediately
- Next button appears after answering
- Final screen: score (X/5), summary of wrong answers, Retry button
- No score persistence — each quiz is fresh

---

## Interactions & Polish
- Tab switching: fade transition between domains
- All hover states: subtle background lift (no harsh outlines)
- Buttons: rounded corners, accent color, darken on hover
- Focus states visible for keyboard navigation
- Smooth scrolling enabled globally
- No page reloads — everything is client-side state

---

## What to avoid
- No light backgrounds or white cards
- No Comic Sans or system fonts
- No full-page spinners
- No alerts or confirm dialogs
- No external dependencies beyond D3.js and Inter font
- No features not listed in this file
