# P Vault Website

The official website for **P Vault** — a private, local-first Android vault.
Live at: https://muhammadshanp.github.io/p-vault-website/

## Files

| File | Purpose |
|------|---------|
| `index.html` | Landing page |
| `update.html` | App updates page |
| `icon.svg` | App icon / favicon |
| `.nojekyll` | Tells GitHub Pages to serve files as-is (no Jekyll build) |

## How this website was created — step by step

1. **Design the pages as plain HTML** — write `index.html` (landing page) and
   `update.html` (updates page) with inline CSS/JS. No framework or build step
   is needed for a static site.
2. **Add the app icon** — create an SVG (`icon.svg`) and reference it in the
   `<head>` of both pages so it shows as the favicon.
3. **Create the GitHub repo** — on GitHub, create a public repository named
   `p-vault-website` under your account.
4. **Push the site to the repo root** — plain HTML can be served straight from
   the `main` branch's root:
   ```powershell
   cd pvault-website
   git init
   git add .
   git commit -m "Publish P Vault website"
   git remote add origin https://github.com/muhammadshanp/p-vault-website.git
   git push -u origin main
   ```
   Add an empty `.nojekyll` file so GitHub Pages serves everything without a
   Jekyll build.
5. **Enable GitHub Pages** — on GitHub, go to
   **Settings → Pages → Build and deployment**, set **Source = Deploy from a
   branch**, **Branch = main / (root)**, and save.
6. **Wait for the first deploy** — after a minute or two the site is live at
   `https://<username>.github.io/<repo>/`.
7. **Update the site** — edit the HTML files locally, then:
   ```powershell
   git add .
   git commit -m "Describe what changed"
   git push
   ```
   GitHub Pages redeploys automatically on every push to `main`.

## P Vault

- App repo: https://github.com/muhammadshanp/p-vault
- Releases: https://github.com/muhammadshanp/p-vault/releases
