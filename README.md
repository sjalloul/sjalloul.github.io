# Personal site — Jekyll + GitHub Pages

A clean, GitHub Pages–ready Jekyll site to showcase your development work, CV,
interests, and writing on software engineering, thought leadership, and building a
software organization.

The visual identity is an **editorial** system inspired by the Financial Times: a warm
kraft-oat background, **Source Serif 4** for headlines and reading (a free stand-in for
the FT's proprietary *Financier*), **Inter** for tracked-uppercase labels (in place of
the FT's *Metric*), an earthy brick + olive accent pair, and a signature **ECG pulse
trace** in the hero — a nod to the cardiac-monitoring world the work comes from.

---

## Quick start — see it live

Open **`preview.html`** in any browser to see the homepage design immediately, with no
build step. (It's a static snapshot; the real site is the Jekyll project.)

---

## Make it yours (5 minutes)

1. **`_config.yml`** — set your `title`, `description`, and the whole `author:` block
   (name, role, company, location, email, GitHub/LinkedIn handles). Set `url` /
   `baseurl` — instructions are in the comments there.
2. **`_data/work.yml`** — your projects (title, summary, tags).
3. **`_data/cv.yml`** — roles, skills, education. *(The dates/orgs are placeholders —
   replace them.)*
4. **`_data/interests.yml`** — the "off the clock" cards.
5. **`_posts/`** — drop in Markdown files named `YYYY-MM-DD-title.md`. Three sample
   essays are included; edit or delete them. Each needs front matter:
   ```yaml
   ---
   layout: post
   title: "Your title"
   category: "Software Engineering"   # shows as the coloured label
   description: "One-line summary for previews and SEO."
   date: 2026-07-01
   ---
   ```

No template editing required for any of the above.

## Adding a portrait later (optional)

There's no headshot on the site right now. If you want one, add an `<img>` inside
the hero in `index.html` (or the CV header) pointing at a file in `assets/img/`.
The repo history includes an earlier engraved "hedcut" treatment if you want it back.


## Deploy to GitHub Pages

### Option A — user site (`your-username.github.io`)
1. Create a repo named exactly **`your-username.github.io`**.
2. In `_config.yml`, set `url: "https://your-username.github.io"` and `baseurl: ""`.
3. Push these files to the `main` branch.
4. Repo **Settings → Pages → Build and deployment → Deploy from a branch →
   `main` / `(root)`**.
5. Live at `https://your-username.github.io` in a minute or two.

### Option B — project site (e.g. repo named `portfolio`)
1. Push to a repo (any name).
2. In `_config.yml` set `baseurl: "/portfolio"` (matching the repo name).
3. Same Pages setting as above.
4. Live at `https://your-username.github.io/portfolio`.

All internal links use `relative_url`, so both options work without editing templates.

---

## Run locally (optional)

Requires Ruby. Then:

```bash
bundle install
bundle exec jekyll serve --livereload
# open http://localhost:4000
```

---

## Structure

```
_config.yml          site + author settings
Gemfile              pinned to the github-pages gem
index.html           homepage (hero, work, writing, interests, CV cta)
work.html            /work/    — full project list
cv.html              /cv/      — rendered from _data/cv.yml
interests.html       /interests/
writing.html         /writing/ — post archive
404.html
_layouts/            default · page · post
_includes/           head · header · footer · pulse (the signature svg)
_data/               work.yml · cv.yml · interests.yml
_posts/              three starter essays
assets/css/main.css  the whole design system
preview.html         static preview — open directly, no build needed
```

## Accessibility & polish
Responsive to mobile, keyboard focus rings, a skip link, and `prefers-reduced-motion`
respected (the pulse animation is disabled for users who ask for less motion).
