# jakobmolinder-uu.github.io

Personal academic website for Jakob Molinder. Plain, static HTML + one CSS file.
**No build step, no framework, no database, no tracking.**

**Live at → https://jakobmolinder-uu.github.io** (free, hosted on GitHub Pages).

```
index.html            Home (bio, research interests, news, featured project, selected pubs, UHILL)
publications.html     Full publication list
research.html         Current projects + working papers
data.html             Public datasets (linked from Dropbox + SND)
contact.html          Contact details
404.html              Friendly not-found page
css/style.css         All styling (light + dark mode, responsive sidebar layout)
assets/img/           Photo + favicon/icons
assets/cv.pdf         CV (replace anytime, keep the filename)
.nojekyll             Tells GitHub Pages to serve files as-is (no Jekyll processing)
sitemap.xml, robots.txt
_headers, _redirects  Cloudflare-only (inert on GitHub Pages; kept for portability)
```

## How updates work (easy)

The site is served from the `main` branch of this repo. **Any push to `main` auto-rebuilds
and republishes within ~1 minute.** So to update:

```bash
cd ~/jakobmolinder-website
# ...edit files...
git add -A && git commit -m "what changed" && git push
```

To add a publication, copy an existing `<li class="pub">…</li>` block in `publications.html`.
Or just ask **Claude Code** — *"add this new paper and a news item"*, *"update my bio"*,
*"swap in my new photo"* — and it edits, commits, and pushes for you.

Maintenance notes:
- The **sidebar** (photo, title, nav, links) is duplicated at the top of every page so the site
  needs zero JavaScript. Change a link → change it on all five pages (or ask Claude Code).
- Replace **`assets/cv.pdf`** with your latest CV (same filename) and the link just works.
- Replace **`assets/img/jakob-molinder.jpg`** with a new portrait (~600–800 px, optimized).

## Preview locally

```bash
cd ~/jakobmolinder-website
python3 -m http.server 8000   # then open http://localhost:8000
```

## Background / history

- Rebuilt from a paid WordPress.com site that had been partly hijacked with spam.
- The old domain **jakobmolinder.com lapsed and was re-registered by a third party in Jan 2026**
  (WHOIS creation date 2026-01-06, privacy-protected, serving spam) — so it's no longer ours.
  This site therefore lives on the GitHub Pages URL. If you ever reclaim/register a domain you
  control, point its DNS at GitHub Pages (or Cloudflare Pages) and add a `CNAME` file here.

## To confirm / finish

- **ORCID iD** — add it to the sidebar links (all 5 pages) and the JSON-LD in `index.html`.
- **"Malmsten" vs "Malmsteen"** Fellow spelling in the News item on `index.html`.
- **Lund email** — add to `contact.html` if you want it listed.
