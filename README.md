# Tasty Chef App

Mobile-first food ordering app built with React + Vite.

## Run locally

```
npm install
npm run dev
```

Opens at http://localhost:5173

## Build for production

```
npm run build
```

Output goes to the `dist/` folder — this is what you deploy.

## Deploy — easiest options

### Option A: Vercel (recommended, free)
1. Push this folder to a GitHub repo
2. Go to vercel.com → New Project → import the repo
3. Vercel auto-detects Vite. Click Deploy.
4. Done — you get a live URL in ~1 minute

### Option B: Netlify (also free, drag-and-drop)
1. Run `npm run build` locally first
2. Go to netlify.com → Sites → drag the `dist` folder onto the page
3. Done — live URL instantly, no GitHub needed

### Option C: GitHub Pages
1. `npm install -D gh-pages`
2. Add to package.json scripts: `"deploy": "gh-pages -d dist"`
3. Add `base: '/your-repo-name/'` to vite.config.js
4. `npm run build && npm run deploy`

## Notes

- All food photos are embedded as base64 directly in the code — no separate
  image hosting needed, but it does make the JS bundle larger (~700KB).
  This is fine for a menu app; if you want it leaner later, move images to
  `/public` and reference them by path instead.
- WhatsApp ordering is wired to +233 20 521 8123. Update the number in
  `src/App.jsx` (search for `wa.me`) if that changes.
- To use a custom domain (e.g. tastychef.com), add it in your Vercel/Netlify
  project settings after deploying — both support this free.
