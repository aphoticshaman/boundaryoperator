# Boundary Operator - Artist Website

Official website for Boundary Operator, electronic music producer.

## Quick Start

```bash
# Install Vercel CLI (if not installed)
npm i -g vercel

# Deploy
vercel
```

## Structure

```
/
├── index.html      # Main page
├── styles.css      # Styles
├── vercel.json     # Vercel configuration
└── README.md       # This file
```

## Connecting Custom Domain

1. Go to [Vercel Dashboard](https://vercel.com/dashboard)
2. Select this project
3. Go to **Settings** → **Domains**
4. Add `boundaryoperator.com`
5. Update DNS records at your registrar:
   - **Option A (Recommended):** Add an `A` record pointing to `76.76.21.21`
   - **Option B:** Add a `CNAME` record pointing to `cname.vercel-dns.com`

For `www` subdomain:
- Add a `CNAME` record for `www` pointing to `cname.vercel-dns.com`

## Local Development

Simply open `index.html` in a browser, or use a local server:

```bash
# Python
python -m http.server 8000

# Node.js (npx)
npx serve

# Then visit http://localhost:8000
```

## Updating Content

### Change Spotify Embed
Edit the `<iframe>` src in `index.html`:
```html
src="https://open.spotify.com/embed/artist/YOUR_ARTIST_ID?utm_source=generator&theme=0"
```

### Add New Social Links
Add to the `.social-links` div in `index.html`:
```html
<a href="YOUR_URL" class="social-link" target="_blank" rel="noopener noreferrer">
    <svg><!-- icon --></svg>
    <span>Platform Name</span>
</a>
```

### Change Accent Color
Edit `--color-accent` in `styles.css`:
```css
:root {
    --color-accent: #6366f1; /* Change this hex value */
}
```

## SEO Checklist

- [x] Schema.org MusicGroup markup
- [x] Open Graph tags
- [x] Twitter Card tags
- [x] Canonical URL
- [x] Meta description
- [x] Semantic HTML
- [x] Mobile responsive

## Performance

Target: 90+ Lighthouse score across all categories.

Optimizations included:
- Minimal CSS (no frameworks)
- No JavaScript frameworks
- Lazy-loaded iframe
- Preconnect to Spotify
- Efficient CSS with variables

## License

All rights reserved. Content is property of Boundary Operator.
