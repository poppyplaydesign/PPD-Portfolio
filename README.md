# Poppy Play Design — Portfolio Site

Prapti Verma's portfolio: plain HTML/CSS/JS, no build step, ready for GitHub Pages.

## Structure

```
index.html        Home — project grid
about.html        Bio, toolkit, journey timeline, résumé download
connect.html      Contact links
project-1.html    Wandering Woodlings (project detail template)
project-2.html    Paperbloom Set
project-3.html    Knockabout Critters
css/style.css      All styles (brand colors, type, animations)
js/main.js         Nav scroll state, scroll reveals, parallax
images/            Placeholder photos (see below)
resume.pdf         Placeholder résumé
CNAME              Custom domain config for GitHub Pages
```

## Replacing placeholder content

Everything currently uses generated placeholder imagery and sample project
copy so the layout can be reviewed end to end. To make it real:

1. **Photos** — replace files in `images/` with real photography, keeping
   the same filenames (or update the `src` in the HTML if names change).
   Recommended sizes: covers ~1600×1200px, process shots ~1600×1100px,
   about portrait ~1200×1500px.
2. **Project copy** — edit the text directly in `project-1.html`,
   `project-2.html`, `project-3.html`, and the cards in `index.html`.
3. **Bio / timeline** — edit `about.html`.
4. **Résumé** — replace `resume.pdf` with your real résumé, same filename.
5. **Social links** — `connect.html` has placeholder Instagram/LinkedIn
   URLs; swap in your real profile links.

## Deploying to GitHub Pages

Repo: `github.com/poppyplaydesign/portfolio`

1. Push this folder's contents to the `main` branch of that repo.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a
   branch**, branch `main`, folder `/ (root)`. Save.
4. Under **Custom domain**, enter `poppyplaydesign.com` and save (this
   matches the `CNAME` file already in the repo). Wait for the DNS check
   to pass, then enable **Enforce HTTPS**.

## Pointing your domain at GitHub Pages

At your domain registrar/DNS provider, add:

**Apex domain (`poppyplaydesign.com`)** — four `A` records pointing to:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**`www` subdomain** — one `CNAME` record:
```
www → poppyplaydesign.github.io
```

DNS changes can take anywhere from a few minutes to ~24 hours to
propagate. GitHub Pages will show a green checkmark on the Pages settings
screen once it verifies the domain.

## Local preview

No build tools needed — just open `index.html` in a browser, or serve the
folder locally:

```
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.
