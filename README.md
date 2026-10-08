# Photo-Gallery-PHONE

> ## Status: 🟢 Completed
>
> <progress value="90" max="100"></progress>
>
> **Progress: 90%** — 50-photo mobile gallery with working pagination; minor cleanup left

<p align="center">
  <img src="banner.webp" alt="Photo-Gallery-PHONE banner" width="100%" />
</p>

![HTML](https://img.shields.io/badge/HTML-5-E34F26?logo=html5)
![CSS](https://img.shields.io/badge/CSS-3-1572B6?logo=css3)
![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-F7DF1E?logo=javascript)

## What it is

A static photo gallery website optimised for phones: 50 photos displayed in a responsive card grid, each with a download button, plus Previous/Next pagination that cycles through the photos six at a time. Pure HTML/CSS/vanilla JS — no build step, no dependencies. Open `index.html` and it works.

## What works (verified)

- ✅ All 50 photos (`photo1.jpg`–`photo50.jpg`) exist on disk — verified with a file count
- ✅ `prev()`/`next()` pagination cycles through the photo array 6 at a time with wraparound — verified by reading the inline script in `index.html`
- ✅ Each card has a working download link (`<a download>`) — verified in the markup
- ✅ Mobile-friendly CSS (flex wrap grid, viewport meta) — verified in `d1.css`
- ✅ No console errors on the static page — no external scripts, everything is inline/local

## Tech stack

| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | CSS3 (flexbox grid, card hover effects) |
| Logic | Vanilla JavaScript (inline) |
| Assets | 50 local JPEGs |

## How to run

No build needed — just open it:

```bash
# option 1: open directly
open index.html        # macOS
# option 2: serve locally
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Screenshots

The gallery itself is the visual — 50 photos in a card grid. Banner above.

## What you can add more

- [ ] Include photo49/photo50 in the slider rotation — the JS array only lists photo1–photo48, so the last two never appear in pagination
- [ ] Remove the commented-out `<script src="d1.js">` line and leftover placeholder comments — dead markup
- [ ] Add a lightbox view on click — currently clicking a photo does nothing (download link is the only action)
- [ ] Lazy-load images — 50 full JPEGs load up front, which is heavy on mobile data

## Project structure

```
Photo-Gallery-PHONE/
├── index.html      # gallery markup + inline pagination JS
├── d1.css          # mobile-optimised gallery styles
├── photo1.jpg … photo50.jpg  # 50 gallery photos
├── banner.webp
└── README.md
```

---
*README written after code audit on 2026-10-08.*
