# portal

Front door of the `me` system. Black-and-white, extreme-minimal, editorial
(Vogue-ish Didone type). Two doors:

- **Light** (live) — helps a visitor point their _own_ AI at the record and ask
  about Sofiene. Pick an angle → a ready-made prompt is copied straight to the
  clipboard. Paste it into any AI that browses the web; it fetches the record
  (`/ls`, `/cat?filename=`) and answers from it.
- **Cool** — Nie-chan (niechan). Shown as "still cooking" until niechan is live.

The data source is never shown in the UI — it only ever lives inside the copied
prompt. No backend. Pure static `index.html` (one Google font: Bodoni Moda).

## Develop / deploy

```sh
vercel dev     # local preview
vercel --prod  # deploy
```

Static site — Vercel serves `index.html` directly, no build step.
