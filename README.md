# Brady Quinn site

Static site for the 1994 Brady oral-history interview summary.

## Contents

- `index.html` — landing page
- `ramona-and-jim-brady-interview-summary.html` — narrative summary with video player and timestamp links
- `1994-03-05_brady-interview.webm` — master recording (local / deploy artifact; not in git)

## Deploy

The video is in R2, not in this repo. HTML points at:

`https://pub-d31d2e719ae043199649a742548c9902.r2.dev/1994-03-05_brady-interview.webm`

### GitHub (already connected)

```bash
git add -A
git commit -m "Point video at R2"
git push
```

### Wrangler (HTML only)

```bash
cd ~/dev/brady-quinn-site
npx wrangler login   # first time
npx wrangler deploy
```

`wrangler.toml` publishes `public/` only. Do not deploy the `.webm` from this folder.

## Local preview

```bash
cd ~/dev/brady-quinn-site
python3 -m http.server 8080
```

Open http://localhost:8080/
