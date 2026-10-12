# Math Revision Hub — `mathrevision.co.uk`

A tiny static landing site that acts as a **4-door hub** to the Math Revision family of curriculum-specific maths revision sites:

| Door | Domain | Status |
| --- | --- | --- |
| **IB Math Revision** | [ibmathrevision.com](https://ibmathrevision.com) | Live — links out |
| **A Level Math Revision** | [alevelmathrevision.com](https://alevelmathrevision.com) | Live — links out |
| **IGCSE Math Revision** | [igcsemathrevision.com](https://igcsemathrevision.com) | Live — links out |
| **CBSE Math Revision** | [cbsemathrevision.com](https://cbsemathrevision.com) | Live — links out |
| **GCSE Maths** | gcsemathrevision.com → 301 to `https://mathrevision.co.uk/gcse` | Coming soon — holding page `gcse.html` (noindex, not in sitemap) |

Below the doors, **Revision by qualification** links straight into each site's
course hubs and topic pages (the hub's job for search: one crawlable page that
points at every site's key pages). SEO files: `robots.txt` (explicit Allow for AI crawlers), `llms.txt` (summary
of the family for AI assistants), `sitemap.xml`, `404.html`, `img/og-image.jpg`
(1200×630), and an Organization + Person + WebSite JSON-LD `@graph` in
`index.html` using the same `@id`s as the four sites
(`https://mathrevision.co.uk/#org`, `#pete-bromfield`; source of truth:
`scripts/seo/identity.js` in the main repo).

**GCSE launch checklist:** remove `noindex` from `gcse.html` (or replace it with
the real site), add `/gcse` to `sitemap.xml`, turn the home-page "Coming soon"
card into a fifth door, and repoint gcsemathrevision.com.

Underneath the doors is a founder block for **Pete Bromfield** (former Head of Maths with IB examining experience; independent, not affiliated with any exam board) with a callout describing CBSE experience gained on a CIS accreditation evaluation team at a CBSE school.

---

## Stack

- Pure static HTML / CSS / vanilla JS. No build step.
- Pages: [`index.html`](./index.html), [`gcse.html`](./gcse.html) (served at `/gcse`), [`404.html`](./404.html).
- Assets in [`img/`](./img/), [`logo.png`](./logo.png), [`favicon.png`](./favicon.png).
- `CNAME` → `mathrevision.co.uk` (for GitHub Pages custom domain).

## Local preview

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy — GitHub Pages

1. Push this repo to a new GitHub repository (public or private with Pages enabled).
2. In **Settings → Pages**:
   - Source: `Deploy from a branch`
   - Branch: `main` / root `/`
3. Set **Custom domain** to `mathrevision.co.uk` (already in `CNAME`).
4. In your DNS (GoDaddy / registrar), set:
   - `A` records to GitHub Pages IPs (`185.199.108.153`, `.109.153`, `.110.153`, `.111.153`) **or**
   - `CNAME` record `www` → `<your-github-username>.github.io`
5. Enable **Enforce HTTPS** once the cert has provisioned.

## Roadmap

- [x] IB door live
- [x] A Level, IGCSE and CBSE doors live
- [ ] GCSE site (gcsemathrevision.com) — in private build; launch when excellent

---

© 2026 Pete Bromfield · [pbromfield@ibmathrevision.com](mailto:pbromfield@ibmathrevision.com)
