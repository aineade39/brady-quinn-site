# Brady Quinn site

Static site for the 1994 Brady oral-history interview summary.

## Contents

- `index.html` — landing page
- `ramona-and-jim-brady-interview-summary.html` — narrative summary with video player and timestamp links
- `1994-03-05_brady-interview.webm` — master recording (local / deploy artifact; not in git)

## Deploy

The video file is gitignored because of size (~225 MB). For Cloudflare Pages:

1. Push this repo (HTML only).
2. Upload `1994-03-05_brady-interview.webm` with a direct deploy or place it in R2 and link from HTML.

## Local preview

```bash
cd ~/dev/brady-quinn-site
python3 -m http.server 8080
```

Open http://localhost:8080/
