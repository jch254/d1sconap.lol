# d1sconap.lol

A self-contained "coming soon" landing page. Everything lives in a single
[`index.html`](index.html) (inline CSS + JS, no build step, no dependencies).

## Preview locally

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

## Deploy

Pick whichever you already use — all serve the static `index.html`:

| Host | Command |
| --- | --- |
| **Netlify** | `netlify deploy --prod` (config in `netlify.toml`) |
| **Vercel** | `vercel --prod` |
| **Cloudflare Pages** | `npx wrangler pages deploy .` |
| **GitHub Pages** | push to a repo, enable Pages on the root |
| **S3 + CloudFront** | `aws s3 sync . s3://your-bucket --exclude "*.md"` |

Then point the `d1sconap.lol` DNS (A / CNAME) at the host.
