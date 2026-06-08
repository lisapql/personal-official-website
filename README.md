# Qilu (Lisa) Pan — personal website

Plain HTML/CSS personal site for Lisa, mirroring the structure of Hao's site.

Lisa is on the 2025–2026 economics job market — the site is designed to make her **job market paper prominent on the home page** and to surface all 5 working papers + 2 work-in-progress on the Research page with full abstracts.

## Files

```
lisa-site/
├── index.html          ← Home: photo, bio, JMP, selected papers
├── research.html       ← All 5 working papers (with abstracts) + WIP + conferences
├── teaching.html       ← Instructor record, awards, service
├── contact.html        ← Email, office, committee references
├── styles.css          ← Shared styles
├── sitemap.xml         ← For Google indexing
├── robots.txt          ← For crawlers
└── assets/
    └── portrait.jpg    ← (Lisa needs to upload her photo here)
```

## Step 1 — Add the portrait photo

Put Lisa's headshot at `assets/portrait.jpg`. Recommended:
- 3:4 aspect ratio (taller than wide)
- ~540×720 px or larger
- Under 500 KB file size — if too large, open in Preview → Tools → Adjust Size to shrink

## Step 2 — Add her compiled CV

Compile her LaTeX CV (or use the existing `LisaCV_updated.pdf`) and copy it to the root folder as `Qilu_Pan_CV.pdf`. The CV link in the header already points there.

## Step 3 — Update social links

Search-and-replace these placeholders across all `.html` files with Lisa's real profile URLs:
- `https://www.linkedin.com/` → her LinkedIn URL
- `https://scholar.google.com/` → her Google Scholar URL
- `your-handle` (in `contact.html`) → her LinkedIn handle

## Step 4 — Preview locally

Double-click `index.html` to open in a browser. Check all 4 pages look right.

## Step 5 — Put on GitHub

1. Lisa creates a GitHub account if she doesn't have one.
2. New repo called `lisapan.org` (or `personal-website`, doesn't matter).
3. **Add file → Upload files** → drag everything in this folder → **Commit changes**.

## Step 6 — Deploy with GitHub Pages

1. Repo → **Settings** → **Pages**
2. Source: **Deploy from a branch**, Branch: **main**, Folder: **/ (root)** → **Save**
3. Wait ~1 minute, refresh — get a URL like `https://lisa-username.github.io/lisapan.org/`

## Step 7 — Connect custom domain `lisapan.org`

Since Lisa's CV already lists `https://lisapan.org/`, she's probably bought the domain (or plans to).

At her domain registrar's DNS panel, add:

| Type | Name | Value |
|---|---|---|
| A | @ | `185.199.108.153` |
| A | @ | `185.199.109.153` |
| A | @ | `185.199.110.153` |
| A | @ | `185.199.111.153` |
| CNAME | www | `lisa-username.github.io` |

Then in GitHub Pages settings, type `lisapan.org` in the Custom domain box → Save. Wait for DNS to propagate. Tick "Enforce HTTPS" once available.

## Step 8 — Submit to Google Search Console

So Lisa shows up when colleagues / hiring committees search her name:

1. Go to https://search.google.com/search-console
2. Add property: `https://lisapan.org`
3. Verify ownership (HTML tag method — paste the meta tag into `index.html` `<head>`)
4. Submit sitemap: `https://lisapan.org/sitemap.xml`

## SEO note

The site already includes:
- Strong meta tags for keywords like "Lisa Pan economics", "Qilu Pan Purdue", "EITC job market"
- Open Graph tags so LinkedIn/Twitter previews look nice
- JSON-LD structured data telling Google she's a researcher at Purdue
- Sitemap for crawlers

For backlinks (what actually makes Google rank well), add `lisapan.org` to:
- Her Purdue student profile
- Google Scholar profile
- LinkedIn profile
- Email signature
- ORCID profile if she has one
- Job market materials (CV cover sheet)

For a job market candidate, the highest-impact thing is putting `lisapan.org` on every conference slide and at the top of her CV.
