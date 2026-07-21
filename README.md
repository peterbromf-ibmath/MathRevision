# Math Revision Hub — `mathrevision.co.uk`

A tiny, single-page landing site that acts as a **3-door hub** to three curriculum-specific math revision brands:

| Door | Domain | Status |
| --- | --- | --- |
| **IB Math Revision** | [ibmathrevision.com](https://ibmathrevision.com) | Live — links out |
| **A Level Math Revision** | `alevelmathrevision.com` | Coming soon (popup) |
| **CBSE Math Revision** | *domain TBC* | Coming soon (popup) |

Underneath the doors is a founder block for **Pete Bromfield** (Director of Studies & Enrichment, IB examiner) with a callout describing CBSE experience gained on a CIS inspection team at a CBSE / A Level school.

---

## Stack

- Pure static HTML / CSS / vanilla JS. No build step.
- One file: [`index.html`](./index.html).
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
- [ ] Build `alevelmathrevision.com`
- [ ] Purchase CBSE domain + build site
- [ ] Wire "Notify me" forms to Resend / Firestore instead of `mailto:`

---

© 2026 Pete Bromfield · [pbromfield@ibmathrevision.com](mailto:pbromfield@ibmathrevision.com)
