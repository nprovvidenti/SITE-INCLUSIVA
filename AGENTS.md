# AGENTS.md

## Cursor Cloud specific instructions

This repository is a **static website** (a single-page portfolio for "Inclusiva - Processos e Treinamentos / Noemi Provvidenti"). It has no build step, no package manager, no dependencies, and no automated tests.

Files:
- `index.html` — page markup (Portuguese, `pt-BR`).
- `style.css` — styles.
- `script.js` — vanilla JS (nav toggle, scroll effects, reveal-on-scroll, contact form that builds a `mailto:` link).
- `foto-perfil.jpg` — profile image.

### Running locally (development)
Serve the folder over HTTP from the repo root (do not open via `file://`, so relative asset paths resolve correctly):

```
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

### Lint / test / build
- There is no lint, test, or build tooling configured.
- Quick JS syntax sanity check: `node --check script.js`.
- The contact form does not POST anywhere; on submit it opens the user's mail client via a `mailto:` link.
