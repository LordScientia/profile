# L.S 2.0 — personal site

Static HTML/CSS/JS. No build step, no framework. Personal profile site — not a sales page.

## Structure
```
index.html          home — who I am, quick links to the rest of the site
interests.html       interests & hobbies, one card per topic (edit freely)
gallery.html         image mood board
journal/index.html   life updates / journal, post list
journal/posts/*.html individual journal entries (copy starting-this.html as a template)
work.html            light, one-page mention of dev work (Sentinel etc.)
css/style.css         all styling — design tokens at the top under :root
assets/               images used across the site
```

## Deploy on Cloudflare Pages
1. Push this folder to a GitHub repo.
2. Cloudflare dashboard → Pages → Create a project → Connect to Git → pick the repo.
3. Framework preset: **None**. Build command: (empty). Build output directory: `/`
4. Deploy — auto-redeploys on every push to main.

## Editing content
Every placeholder is marked `<!-- EDIT ME -->` in the HTML. Look for those first —
bio text on the homepage, the interest card descriptions, and the first journal entry.

## Adding a journal entry
1. Copy `journal/posts/starting-this.html`, rename it, update title/date/body.
2. Add a row for it at the top of `journal/index.html`.

## Adding a gallery image
1. Drop the image in `assets/`.
2. Add a `<div class="gallery-item"><img src="assets/yourfile.jpg" alt="..."></div>` block in `gallery.html`.

## Colors & fonts
All design tokens are CSS variables at the top of `css/style.css` under `:root`.
