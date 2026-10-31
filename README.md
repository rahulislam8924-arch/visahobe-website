# VisaHoBe website

Single-page marketing site for VisaHoBe — visa consulting, business migration and
international worker recruitment.

Static HTML/CSS/JS only. No build step, no dependencies. Open `index.html` or serve
the folder with any static host.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole site: markup, styles and the small mobile-nav script inline |

## Editing content

Everything lives in `index.html`. The blocks to look for, in order:

- `<!-- HERO -->` — headline, sub-headline and the two CTA buttons
- `<!-- SERVICES -->` — the four service cards
- `<!-- PROCESS -->` — the three stages
- `<!-- ABOUT -->` — company description and the three highlight stats
- `<!-- CONTACT -->` — the email addresses used by every button and mailto link

Colours are CSS variables at the top of the `<style>` block (`--navy`, `--gold`, ...).
Change them once and the whole page follows.

## Hosting on GitHub Pages (free)

1. Push this repository to GitHub (already done for you).
2. Repository **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
   branch `main`, folder `/ (root)`. Save.
3. The site appears at `https://<username>.github.io/visahobe-website/` within a minute or two.

## Custom domain (visahobe.work.gd)

DNS for the domain is managed at DNSExit. Add these records there:

**Apex (`@`)** — four A records pointing at GitHub Pages:

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**`www`** — one CNAME:

```
www  ->  <username>.github.io
```

Then in **Settings → Pages → Custom domain** enter `visahobe.work.gd` and tick
**Enforce HTTPS** once the certificate is issued (can take up to 24 hours).

Leave MX, SPF and DKIM records untouched — email for the domain is handled by Zoho Mail.
