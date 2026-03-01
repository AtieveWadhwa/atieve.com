# atieve.com

> A tiny static site built with **Vite** and deployable to **Cloudflare Workers**.

The project consists of two pages:

- `index.html` – public landing page
- `private.html` – a hidden page that can only be accessed by a specific sub‑domain

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
├─ src/
│  └─ main.js             # empty Vite entry (required by Vite)
├─ index.html
├─ private.html
├─ vite.config.ts
├─ package.json
└─ README.md
```

---

## 🚀 Quick start

```bash
# Install dependencies
npm ci

# Development server (live reload)
npm run dev

# Build the production bundle
npm run build

# Preview the production build locally
npm run preview

# Deploy to Cloudflare Workers (requires a Cloudflare account + wrangler config)
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

## 🛠️ Development Notes

* **Favicons** – All favicon files are in `public/assets/favicon_io`.  
  They are referenced in the HTML with relative paths (`/assets/favicon_io/...`).
* **Shared CSS** – Put all common styling into `public/assets/css/shared.css` and link it in both pages:
  ```html
  <link rel="stylesheet" href="/assets/css/shared.css">
  ```

---