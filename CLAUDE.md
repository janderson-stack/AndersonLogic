# CLAUDE.md — ANDERSONLOGICai

Guidance for AI assistants (and humans) working in this repository.

## What this repo is
The official **ANDERSONLOGICai** marketing website — a single, self-contained,
responsive `index.html` (all CSS and JS inline, no build step) hosted on GitHub
Pages.

- **Brand:** ANDERSONLOGICai — *Logic. Applied.*
- **Owner:** Jeff Anderson (GitHub: `janderson-stack`) — Zionsville, Indiana
- **Contact:** jeffanderson7772@gmail.com
- **Live site:** https://janderson-stack.github.io/AndersonLogic/
- **Flagship project (separate repo):** BeHistorical — https://janderson-stack.github.io/ap-world-history/

## Workflow rules
- **Always push to `main`.** Commit and push directly to `main`; do not develop on
  a separate feature branch unless explicitly told otherwise for a specific task.
- Hosting is **GitHub Pages from `main` branch root (`/`)**. Anything merged to
  `main` goes live, so keep `main` deployable.
- The repository is **PUBLIC** brand content but **proprietary** — see
  `COPYRIGHT.md`. No open-source license; do not add one.
- Do **not** create pull requests unless explicitly asked.

## Brand system (use these exact values)
| Element | Value |
|---|---|
| Blackened Steel | `#1A1C1D` |
| Antique Gold | `#C9A46A` |
| Bright Gold | `#E2C189` |
| Clean Paper | `#FFFDF7` |
| Aged Iron | `#5A5F5C` |
| Electric Blue | `#3F6DF6` |
| Display font | Manrope |
| Body font | Inter |

## Voice rule (important)
Every section is written in a neutral, professional **third-person/brand voice** —
no "I," "we," "us," or "our" — **except the About section**, which is the only place
that uses first person ("I'm Jeff Anderson…"). Preserve this when editing copy.

## Logo & signature animation
- The hero logomark is an inline **SVG "A"** (Clean Paper lettering + gold center
  dot). It is intentionally vector so the load animation can trace the letterform
  outline and circle the gold dot.
- The signature load sequence: logo fades in → a bright gold point of light traces
  the "A" (bottom-left → apex → bottom-right) leaving a gold gradient line → the
  light circles the gold center dot along its edge → a radial glow blooms behind the
  logo only during the trace and then fades out completely (no lingering/pulsing) →
  a subtle gold particle wave drifts across the hero.
- **Honor `prefers-reduced-motion`:** the page must fall back to the static logo
  with no motion (already wired via the `anim-ready` / `play` classes and a
  reduced-motion media query). Also degrade gracefully with no JS.
- To swap in an official **base64 PNG** logo (dark-mode version: black lettering
  remapped to Clean Paper `#FFFDF7`, gold untouched), place the file in `/assets`
  and follow the commented swap-in block in `index.html`. Keep the SVG if the trace
  animation should be retained.

## File map
- `index.html` — the entire website (inline CSS/JS).
- `README.md` — public brand-umbrella front door (keep largely verbatim; the only
  intentional change from the original brief is the Live-site URL pointing at this
  repo's Pages URL).
- `COPYRIGHT.md` — proprietary notice (no OSS license).
- `assets/` — logo/image files.
- `.gitignore` — `.DS_Store`, `node_modules/`, `*.log`.

## Editing conventions
- Keep everything self-contained: no external build step; CSS/JS stay inline in
  `index.html`.
- Maintain accessibility: semantic HTML, focus-visible states, `aria` labels,
  keyboard-reachable nav, and the reduced-motion fallback.
- Mobile-first and fully responsive.
