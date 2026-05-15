# Varnish & Veil GitHub Pages

Publish these static files in a public GitHub repository under the `springdatauk` organisation:

- `index.html`
- `privacy.html`
- `support.html`

Expected URLs:

- `https://springdatauk.github.io/varnish-veil-pages/privacy.html`
- `https://springdatauk.github.io/varnish-veil-pages/support.html`

## Terminal Commands

```bash
cd /Users/cwilson/Projects/springData/VarnishVeil
mkdir -p /tmp/varnish-veil-pages
cp web/privacy.html /tmp/varnish-veil-pages/privacy.html
cp web/support.html /tmp/varnish-veil-pages/support.html
cp web/index.html /tmp/varnish-veil-pages/index.html
cd /tmp/varnish-veil-pages
git init
git branch -M main
git add index.html privacy.html support.html
git commit -m "Add Varnish and Veil legal pages"
gh repo create springdatauk/varnish-veil-pages --public --source=. --remote=origin --push
```

If the repository already exists, use:

```bash
cd /tmp/varnish-veil-pages
git remote add origin git@github.com:springdatauk/varnish-veil-pages.git
git push -u origin main
```

## GitHub UI Steps

1. Open the new `springdatauk/varnish-veil-pages` repository on GitHub.
2. Go to Settings.
3. Open Pages.
4. Under Build and deployment, choose Deploy from a branch.
5. Set Branch to `main` and Folder to `/root`.
6. Save.
7. Wait for GitHub Pages to publish.
8. Confirm both URLs load:
   - `https://springdatauk.github.io/varnish-veil-pages/privacy.html`
   - `https://springdatauk.github.io/varnish-veil-pages/support.html`
