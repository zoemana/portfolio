# portfolio

The portfolio site of ZM Nishimura-Russ ([zoemana.com](https://zoemana.com)), rebuilt from the original Framer site as plain HTML and CSS. It has no build step and no framework, so it's easy to edit by hand or with Claude.

## What's where

| Path | What it is |
| --- | --- |
| `index.html` | Home page: the project grid |
| `page_about.html` | About page and resume |
| `page_<project>.html` | One file per project (same URLs as the Framer site) |
| `page_rpi-sub-1.html` | RPI before/after full-page screenshots |
| `assets/css/site.css` | All styles. Colors, fonts and spacing are variables at the top |
| `assets/img/<page>/NN.webp` | Images, one folder per page, numbered top to bottom |
| `assets/favicon.svg` | Browser tab icon (the ZMNR logo) |

## Common edits

- **Add a project:** copy an existing `page_*.html`, swap the title, text and images, then add a card to the grid in `index.html`. Update the "Next project" link on the page before it.
- **Change text:** edit the HTML file directly. The header and footer appear on every page, so change them in each file.
- **Change colors or fonts:** edit the variables under `:root` in `assets/css/site.css`.

## Preview locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000. Links without `.html` (like `/page_about`) work on GitHub Pages but not with this simple local server. Add `.html` to the URL when previewing.

## Fonts

The site uses SF Pro on Apple devices (built in, as on the Framer site) and falls back to Inter from Google Fonts everywhere else.
