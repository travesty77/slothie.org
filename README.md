# slothie.org

A fictional smoothie brand landing page for slothie.org.

## Structure

```
slothie/
├── index.html       # Full site — single file, no dependencies
└── images/          # Drop real smoothie photos here (optional)
    ├── mango-hang.jpg
    ├── jungle-green.jpg
    └── lazy-berry.jpg
```

## Swapping in real photos

The blend cards are ready for real photos. In `index.html`, find the three
`<!-- <img src="images/..." -->` comments in the blend cards and uncomment them.
Delete the `<div class="blend-img-placeholder">` block above each one.

Good free sources:
- https://unsplash.com/s/photos/mango-smoothie
- https://unsplash.com/s/photos/green-smoothie
- https://unsplash.com/s/photos/berry-smoothie

## Deploy to Cloudflare Pages

1. Push this folder to a GitHub repo (e.g. `github.com/yourname/slothie`)
2. Go to https://dash.cloudflare.com → Pages → Create a project
3. Connect your GitHub repo
4. Build settings:
   - Framework preset: None
   - Build command: (leave blank)
   - Build output directory: `/` (or leave blank)
5. Click Deploy
6. Go to Custom Domains → add `slothie.org`
7. Done — live in ~60 seconds

## Local preview

Just open index.html in a browser. No build step needed.

