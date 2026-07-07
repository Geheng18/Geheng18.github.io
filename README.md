# My Personal Website

A simple static personal website (plain HTML + CSS). Free to host on GitHub Pages.

## Structure
This is a multi-page site — one page per section. All pages share `style.css` and `site.js`.

| File | Page |
|------|------|
| `index.html` | Home / About + research interests + current research + education + section links |
| `research.html` | Research interests, publications, presentations, service, memberships |
| `experience.html` | Consulting/research & industry experience + skills |
| `teaching.html` | Teaching — links to the course page |
| `programming-basics.html` | PHC 6099 course schedule (links to slides & code) |
| `awards.html` | Honors & awards |
| `mountaineering.html` | Bio, cycling, photos, certifications, climbing/ski route tables |
| `contact.html` | Contact info |

Supporting files:
- `style.css` — shared styling. Change the two colors at the top of the file to re-theme the whole site.
- `site.js` — shared behavior (mobile menu, footer year, active-nav highlight).
- `photo.jpg` — your profile photo (add this yourself; a square image looks best). The site works fine without it.
- `cv.pdf` — your CV (already included; the "CV (PDF)" links point to it).
- `pb-lectures/` — all PHC 6099 slide decks (self-contained HTML) and R/Python code, mirrored from the source course. ~71 MB.

### Adding mountain photos
On `mountaineering.html`, each grey dashed box is a placeholder. To use a real photo, create a `photos/` folder, drop your image in, and replace a placeholder line like:
`<div class="photo-ph">Add climbing photo</div>`
with:
`<img class="photo" src="photos/climbing.jpg" alt="Climbing" />`

## How to edit
1. Open the relevant `.html` file in any text editor and edit the text directly.
2. To add a nav link, add an `<li>` to the `.nav-links` list — it must be added to **every** page's `<nav>` (the nav is copied into each file).
3. Save and open the file in a browser to preview.

## How to publish for free (GitHub Pages)

### Option A — the easy, no-command-line way
1. Create a free account at https://github.com
2. Create a new repository named **`yourusername.github.io`** (use your actual GitHub username).
3. On the repo page, click **Add file → Upload files**, and drag in `index.html`, `style.css`, and your `photo.jpg` / `cv.pdf`.
4. Click **Commit changes**.
5. Wait ~1 minute, then visit **https://yourusername.github.io** — your site is live.

### Option B — with git (command line)
```bash
# inside this folder
git init
git add .
git commit -m "Initial website"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```
Then go to the repo's **Settings → Pages** and confirm it's building from the `main` branch. Your site will be at `https://yourusername.github.io`.

## Cost
- Building + hosting: **free**.
- Optional custom domain (e.g. `yourname.com`): ~$10–15/year from a registrar. GitHub Pages will still host it for free; add a `CNAME` file with your domain and point the domain's DNS at GitHub.
