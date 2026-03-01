# atieve.com

> A tiny static site built with **Vite** and deployable to **Cloudflare Workers**.

This project is for one page: `index.html` - the public landing page when someone outside my VPN tries to access [atieve.com](https://atieve.com)

The assets (favicons, shared CSS, etc.) live in the `public/` folder and are served at the root of the site.

---

## 📦 Project structure

```
/.
├─ public/
│  ├─ assets/
│  │  ├─ favicon_io/      # favicons & site.webmanifest
│  │  └─ css/
│  │     └─ shared.css    # shared styling
├─ index.html
├─ vite.config.ts
├─ package.json
└─ README.md
```

---

## 🚀 Quick start

```bash
# Install dependencies
npm install

# Development server (live reload)
npm run dev

# Build the production bundle
npm run build

# Preview the production build locally
npm run preview

# Deploy to Cloudflare Workers (requires Cloudflare login)
npm run deploy
```

---

## ⚙️ Configuration

### `vite.config.ts`

* `publicDir` – static assets are served from `public/`.

### Cloudflare Wrangler

The `deploy` script runs `wrangler deploy` after building.  
simply run:

```bash
npm run deploy
```

---

## 📜 Scripts

| Script | Purpose |
|--------|---------|
| `dev` | Starts Vite dev server with hot‑reload. |
| `build` | Builds the static assets into `dist/`. |
| `preview` | Serves the built `dist/` locally to test the production output. |
| `deploy` | Builds the project and pushes it to Cloudflare Workers. |

---