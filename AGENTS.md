# AGENTS.md

## Cursor Cloud specific instructions

This repository is a **static website** (no build step, no package manager, no tests).
It is a single-page institutional/portfolio site in Portuguese for "Inclusiva - Processos
e Treinamentos" (Noemi Provvidenti), composed of:

- `index.html` — page markup
- `style.css` — styles
- `script.js` — vanilla JS (nav toggle, scroll effects, reveal-on-scroll, contact form → `mailto:`)
- `foto-perfil.jpg` — profile image

### Running the site (development)

Serve the folder over HTTP (opening `index.html` via `file://` mostly works, but a server
matches production behavior and avoids any cross-origin quirks):

```
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

### Lint / test / build

There are no lint, test, or build commands — this is plain HTML/CSS/JS with no tooling or
dependencies. There is nothing to install. The contact form does not POST anywhere; on
submit it opens the user's mail client via a `mailto:` link.
