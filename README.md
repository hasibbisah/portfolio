# Mesbah Hasib — Portfolio

A single-page portfolio site built from your resume. Static HTML/CSS/JS, no build step, no dependencies to install.

```
site/
├── index.html        # the whole site
├── assets/
│   └── portrait.jpg
└── README.md
```

## Preview it locally

Just double-click `index.html`, or from a terminal in this folder:

```bash
python3 -m http.server 8000
```

then open http://localhost:8000

## Publish it for free with GitHub Pages

1. **Create a repository.** On github.com click **New repository**. Name it whatever you like — if you name it `<your-username>.github.io` exactly, GitHub will publish it at the root of that URL instead of a subpath. Either works; a normal name (e.g. `portfolio`) is simplest.

2. **Push this folder to it.** In a terminal, from inside this `site` folder:

   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```

   (Replace `<your-username>` and `<repo-name>`. If prompted for a password, GitHub now requires a [personal access token](https://github.com/settings/tokens) instead of your account password — or use `gh auth login` if you have the GitHub CLI installed.)

3. **Turn on Pages.** In the repo on GitHub: **Settings → Pages**. Under "Build and deployment", set **Source** to "Deploy from a branch", branch `main`, folder `/ (root)`. Save.

4. **Wait about a minute**, then refresh that Pages settings page — it'll show your live URL:
   - `https://<your-username>.github.io/<repo-name>/` (normal repo name), or
   - `https://<your-username>.github.io/` (if you named the repo `<your-username>.github.io`)

Any time you edit `index.html` and push again (`git add . && git commit -m "update" && git push`), the live site updates automatically within a minute or two.

## Using a custom domain (optional)

If you own a domain, add a `CNAME` file to this folder containing just the domain (e.g. `hasib.dev`), point your domain's DNS at GitHub Pages per [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site), and set it in Settings → Pages → Custom domain.

## Editing content

Everything — text, dates, links — lives in `index.html`. Search for the section you want (`id="profile"`, `id="experience"`, etc.) and edit the text directly; no build step needed.
