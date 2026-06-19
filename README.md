# FixedIT Tech — Mock Marketing Site

A 4-page static mock site for FixedIT Tech, a service that sets up Microsoft Teams
calling, presence-based routing, and managed permissions for multi-location medical offices.

## Structure

```
index.html          Home
services.html        Services
how-it-works.html    How It Works
contact.html         Contact (mock form — no backend wired up)
css/styles.css       Shared stylesheet
js/script.js         Mobile nav, scroll reveal, mock form handler
```

No build step — plain HTML/CSS/JS. Open `index.html` directly in a browser to preview locally.

## Deploying from this repo + pointing your GoDaddy domain

**1. Push these files to your GitHub repo**, at the root (or to a `docs/` folder if you
prefer — just adjust the GitHub Pages setting accordingly).

**2. Turn on GitHub Pages**
Repo → Settings → Pages → set "Source" to your main branch (and `/root` or `/docs`,
matching where the files live). GitHub will give you a URL like
`https://yourusername.github.io/your-repo`.

**3. Add a custom domain in GitHub Pages**
Still in Settings → Pages, enter your domain (e.g. `fixedittech.com`) in the "Custom
domain" field. This creates a `CNAME` file in your repo automatically.

**4. Point GoDaddy's DNS at GitHub Pages**
In GoDaddy → My Products → DNS for your domain, add:
- Four `A` records for the apex domain (`@`) pointing to GitHub Pages' IPs:
  `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- A `CNAME` record for `www` pointing to `yourusername.github.io`

DNS changes can take a few hours to propagate. You do **not** need to transfer the
domain away from GoDaddy — it stays registered there; you're just changing where it points.

**Alternative:** if you'd rather not use GitHub Pages, the same repo deploys cleanly to
Netlify or Vercel (connect the repo, no build command needed), and both give you their
own DNS records to point GoDaddy at instead.

## Notes

- Contact form is non-functional by design (mock site). To make it live, wire it to a
  form service (e.g. Formspree, Netlify Forms) or a backend endpoint.
- Email/phone on the Contact page are placeholders — replace with real details before launch.
