# portal

Front door of the `me` system. A tiny static, dark page with two doors:

- **Light** (live) — helps a visitor point their _own_ AI at the data plane
  ([shouldknowaboutme](https://shouldknowaboutme.vercel.app)) and ask about
  Sofiene. Pick an intent → copy a ready-made prompt that tells the AI to fetch
  the data (`/ls`, `/cat?filename=`) and answer from it.
- **Cool** — links to Nie-chan (niechan). Shown as "still cooking" until niechan
  is live.

No backend. Pure static `index.html`.

## Data plane

The Light prompts point at the live data URL:

```
https://shouldknowaboutme.vercel.app
```

- `GET /ls?wc=PATTERN` — list files
- `GET /cat?filename=NAME` — read one file

## Develop / deploy

```sh
vercel dev     # local preview
vercel --prod  # deploy
```

Static site — Vercel serves `index.html` directly, no build step.
