# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Static one-page website for **Soma Salón**, a hair salon in Llucmajor, Mallorca. Hosted on GitHub Pages at `somasalon.es`. No build system, no framework, no dependencies beyond CDN links.

## Files

| File | Purpose |
|------|---------|
| `index.html` | Single page — all HTML, SEO meta, Schema.org JSON-LD |
| `styles.css` | All styles — variables, reset, hero, about, map, footer, responsive |
| `favicon.svg` | SVG favicon (dark background + cream "S") |
| `LogoWEB.png` | White circle logo on transparent background |
| `FondoWEB.png` | Landscape background photo (Serra de Tramuntana) |
| `interior.png` | Salon interior photo — used as OG image |
| `CollectionFree.otf` | Brand display font, loaded via `@font-face` as `'Collection'` |

## Typography

Two fonts in use — do not mix their roles:

- **CollectionFree** (`--font-display`) — brand only: `.slogan` ("Less ego, more soul") and `#about h1` ("Soma Salón")
- **Special Elite** (`--font-typewriter`, Google Fonts CDN) — all other titles and buttons: `#map h2`, `.btn-primary`, `.btn-secondary`

## CSS architecture

All styles are in `styles.css`, structured in order: font → variables → reset → hero → about → map → footer → responsive. CSS custom properties are defined in `:root` — always use them, never hardcode colors or fonts.

Key variables: `--color-bg-dark`, `--color-bg-darker`, `--color-bg-section`, `--color-bg-light`, `--color-cream`, `--color-accent` (`#b89a6a`).

## External links

| Service | URL |
|---------|-----|
| Reservas Timma | `https://reserva.timma.es/somasalon` |
| Instagram | `https://www.instagram.com/somahairsalon` |
| Facebook | `https://www.facebook.com/somahairsalon` |
| WhatsApp | `https://wa.me/34611486327` |

## Deployment

Push to `main` → GitHub Pages auto-deploys. No build step needed.

After editing, commit and push:
```bash
git add index.html styles.css  # (or specific files)
git commit -m "description"
git push
```
