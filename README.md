# FindIt @ Campus 📌

A shared corkboard for a campus community — pin a note when you lose
something, pin a note when you find something, and connect with whoever's on
the other end.

Built as a single-page web app with **zero setup**: no server, no build step,
no database. Open `index.html` and it just works.

**Live demo:** _[add your GitHub Pages URL here once deployed]_

---

## Why

Physical lost-and-found desks are scattered around campus, keep limited
hours, and have no searchable record. FindIt @ Campus gives students, staff,
and campus security one place to report and search for lost or found items.

## Features

- 📌 **Pin a note** for something lost or found — item title, category,
  description, location, date, and contact info.
- 🔍 **Live search** across title, description, location, and category.
- 🗂️ **Filter tabs** — All / Lost / Found / Resolved, each with a live count.
- ✅ **Mark resolved** (or reopen) once an item is returned, and remove notes
  entirely.
- 💾 **Persists in the browser** via `localStorage` — no login, no backend,
  works fully offline after the first load.
- 📱 Responsive, accessible corkboard-styled UI (keyboard focus states,
  reduced-motion support, semantic markup).

## Essential user journey

1. A student who **lost** an item clicks **"+ Pin a note"**, selects *I lost
   something*, and fills in the details.
2. A student who **found** a matching item searches or browses the board and
   finds the note.
3. They connect using the listed contact info, and either student marks the
   note **resolved** once the item is back with its owner.

## Getting started

No dependencies, no installation.

```bash
git clone https://github.com/YOUR-USERNAME/findit-campus.git
cd findit-campus
```

Then either:

- **Open directly:** double-click `index.html`, or drag it into a browser
  window.
- **Serve locally** (optional, avoids some browsers' file:// restrictions):
  ```bash
  python3 -m http.server 8000
  # then visit http://localhost:8000
  ```

## Deploying

This repo is ready for **GitHub Pages** as-is, since `index.html` sits at the
project root:

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source: Deploy from a branch**,
   **Branch: main**, folder **/ (root)**, then **Save**.
4. Your live URL will appear at the top of that page after ~30–60 seconds,
   typically `https://your-username.github.io/findit-campus/`.

## Project structure

```
findit-campus/
├── index.html   # entire app: markup, styles, and logic in one file
└── README.md    # this file
```

## Tech stack

- HTML5, CSS3, vanilla JavaScript — no framework, no build tools.
- Browser `localStorage` API for persistence.
- Google Fonts (Zilla Slab, Work Sans, Caveat) via CDN.

## Data & privacy note

All notes are stored only in the visitor's own browser. There's no account
system and no server-side database, so notes won't sync across devices or
visitors — this keeps the app genuinely working with no setup, at the cost of
shared state. A natural next step would be swapping `localStorage` for a
small backend (e.g. Firebase or a lightweight REST API) so notes are visible
to everyone who visits.

## Course context

Built for **IIC 2223 – Web Application Development**, Lab 1 Part 1: build the
best working web app possible in one hour using AI tools.

## License

For coursework use. No license specified beyond that.
