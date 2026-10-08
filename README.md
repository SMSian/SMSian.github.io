# sheikmohammedsha.github.io

My portfolio, live at **https://www.sheikmohammedsha.shop** (also at https://sheikmohammedsha.github.io).

I'm Sheik Mohammed Shaw, a software engineer at Zoho (ManageEngine Log360 / EventLog Analyzer). I've spent four
years working with Elasticsearch and big-data log storage and search, and these days I build LLM agents on top of
search, with weekend projects like [nlsearch](https://github.com/sheikmohammedsha/nlsearch).

The site looks like a Fallout Pip-Boy, because I play too much. If you'd rather read it plainly, the
**Pip-Boy / Professional** switch at the top changes to a clean light layout, and the browser remembers your choice.

## What's on it

| Tab | Section |
|---|---|
| STAT | About, quick facts, and a level bar based on years of experience |
| DATA | Experience at Zoho, Elasticsearch work first |
| QUESTS | Projects |
| INV | Skills |
| RADIO | Contact |

Tabs are deep-linkable (`/#data`, `/#quests`, …) and work with the arrow keys. Printing the page gives you every
section in black on white.

## How it's built

Plain HTML, CSS and a little vanilla JS, with no build step and no dependencies apart from two Google Fonts
(VT323, Chakra Petch).

- `index.html` holds all the content, plus the script for tabs, the boot screen, the typewriter, the XP bar and the view toggle.
- `style.css` holds the theme. Colors are CSS variables, and `.plain` on `<html>` swaps them for the professional view.
- `me.webp` / `me.jpg` are the portrait, 640px, about 25–40 KB.
- `favicon.png` and `cursor.png` are the favicon and the Pip-Boy cursor.

The animations are skipped for anyone with `prefers-reduced-motion` turned on, and in the professional view. The full
text is in the HTML, so screen readers, crawlers and visitors without JavaScript still get all of it.

## Run it locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy

GitHub Pages serves `main` from the repo root, so pushing to `main` publishes the site. The same files are hosted on
Zoho Catalyst behind www.sheikmohammedsha.shop; the root domain redirects to www through a Cloudflare redirect rule.

## License

Apache 2.0 (see `LICENSE`). The portrait and the personal content are mine; please don't reuse them.
