# AGENTS.md

## Cursor Cloud specific instructions

This repository is a static marketing website with no build step, package manager, or automated tests. It consists of plain `index.html`, `style.css`, and `script.js`, plus a profile image. Google Fonts are loaded from a CDN, so internet access is needed for the intended fonts.

### Running the site (development)

There are no dependencies to install. Serve the folder with any static HTTP server, for example:

```
python3 -m http.server 8002
```

Then open `http://localhost:8002/`. Do not open `index.html` via the `file://` protocol — serve over HTTP instead.

Notes:
- There is no hot reload; refresh the browser after editing files.
- The contact form (`#contact-form`) does not POST anywhere. On submit, `script.js` builds a `mailto:` URL (to `nprovvidenti@gmail.com`) and navigates to it, so submitting opens the OS/browser email handler rather than sending over the network.
- There is no lint or test tooling configured in this repo.
