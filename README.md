# Brady Quinn site

Static site for the 1994 Brady oral-history interview summary.

## Contents

- `index.html` — landing page
- `ramona-and-jim-brady-interview-summary.html` — narrative summary with in-page player and timestamp seeks
- `1994-03-05_brady-interview.webm` — master recording (R2 object; MP4/H.264 bytes; not in git)

## Deploy

The video is in R2, not in this repo. HTML points at:

`https://media.brady-quinn.thelittlecat.app/1994-03-05_brady-interview.webm`

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
