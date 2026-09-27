# Assignment #2 — Advanced CSS (Flexbox & Grid)

AITU Frontend Development course. A small multi-page site built with plain
HTML and CSS (no framework), demonstrating Flexbox and CSS Grid layout
techniques.

**Student:** Dastan Abdasim
**Group:** _fill in your group_
**Live site:** _add your GitHub Pages / Netlify link here after publishing_

## Pages

| Page | Task | Techniques |
|---|---|---|
| [`index.html`](index.html) | Task 0 — Navigation bar | Flexbox |
| [`cards.html`](cards.html) | Task 1 — Card row | Flexbox |
| [`grid-layout.html`](grid-layout.html) | Task 2 — Page layout with grid areas | CSS Grid |
| [`gallery.html`](gallery.html) | Task 3 — Image gallery | CSS Grid |
| [`portfolio.html`](portfolio.html) | Task 4 — Portfolio page | Flexbox + Grid |

The same navigation bar (`header.site-header`) appears on every page and
links across all five, satisfying the assignment's submission requirement
for a shared navbar across separate pages.

## Structure

```
.
├── index.html
├── cards.html
├── grid-layout.html
├── gallery.html
├── portfolio.html
├── css/
│   └── style.css
└── README.md
```

All pages share one stylesheet, `css/style.css`, which holds the design
tokens (colors, type, spacing) at the top, followed by the navbar/footer
styles and one section per task.

## Running locally

No build step or dependencies — just open `index.html` in a browser, or
serve the folder locally, e.g.:

```bash
npx serve .
# or
python3 -m http.server
```

## Publishing to GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Source**, choose the `main` branch and `/ (root)` folder.
4. Save, then wait a minute for the link under **Pages** to go live.
5. Paste that link into the **Live site** field above and into your Moodle
   submission.

## Notes on each task

- **Task 0 / navbar:** flex container with `justify-content: space-between`
  and `align-items: center`; link spacing comes from `gap` on the link list.
- **Task 1 / card row:** `display: flex; flex-wrap: wrap;` with
  `flex: 1 1 260px` per card, so cards stay equal height (flex's default
  `align-items: stretch`) and wrap on small screens.
- **Task 2 / grid layout:** `grid-template-areas` names four regions
  (`head`, `side`, `main`, `foot`) so the layout reads like a floor plan
  instead of row/column numbers.
- **Task 3 / gallery:** a 3×3 `grid-template-columns: repeat(3, 1fr)` grid;
  captions are absolutely positioned and fade in on `:hover`/`:focus-within`
  so the effect also works with keyboard navigation.
- **Task 4 / portfolio:** Grid splits the page into a projects column and
  an info column; Flexbox arranges the content inside the project cards
  and the info panel.

## Resources used

- MDN — [CSS Flexible Box Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout)
- MDN — [CSS Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout)
- Flexbox Froggy / Grid Garden (practice games referenced in the assignment brief)
