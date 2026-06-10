# ruishenzhang.com

Personal academic website of Ruishen Zhang. Plain static HTML/CSS — no build
step, no dependencies. Edit the `.html` files directly and push to update.

## Structure

| File | Purpose |
|---|---|
| `index.html` | Landing: short research summary, photo, contact, news |
| `about.html` | Full biography, education, contact, CV link |
| `research.html` | Publications and working papers |
| `teaching.html` | Teaching by institution |
| `awards.html` | Awards and grants |
| `styles.css` | Single shared stylesheet |
| `assets/Ruishen_Zhang_CV.pdf` | CV (replace this file to update the CV link) |
| `assets/portrait.jpg` | Homepage photo (600px wide; replace to update) |
| `CNAME` | Custom domain for GitHub Pages — do not delete |

## Routine updates

- **New CV:** overwrite `assets/Ruishen_Zhang_CV.pdf`, keep the same filename.
- **Photo:** replace `assets/portrait.jpg` (a ~600px-wide JPEG keeps the page fast).
- **New paper / award:** copy an existing `.entry` or `<dt>/<dd>` block and edit.
- **Footer date:** update "Last updated" in each page footer (it appears once per page).

## Deploying on GitHub Pages

1. Create a GitHub repository (e.g. `website`), then from this folder:

   ```sh
   git init && git add -A && git commit -m "Personal website"
   git branch -M main
   git remote add origin git@github.com:RayHulala/website.git
   git push -u origin main
   ```

2. On GitHub: **Settings → Pages → Source: Deploy from a branch → main / (root)**.

3. Custom domain: in the same Pages settings, enter `ruishenzhang.com`
   (the `CNAME` file in this repo keeps the setting across deploys) and tick
   **Enforce HTTPS** once the certificate is issued.

## DNS at the domain registrar

Add these records for `ruishenzhang.com`:

| Type | Host | Value |
|---|---|---|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `RayHulala.github.io.` |

DNS can take up to a few hours to propagate; GitHub then issues the HTTPS
certificate automatically.
