# Sivanvika Technologies

Static company website, published via GitHub Pages.

## Structure

- `index.html` - Home
- `services.html` - Services
- `about.html` - About
- `contact.html` - Contact
- `styles.css` - All styling
- `CNAME` - Custom domain (sivanvika.com)

## Local preview

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000

## Deploy

Push to `main`. GitHub Pages publishes automatically.

## Before going live

- [ ] Replace `YOUR_FORM_ID` in `contact.html` with a real Formspree ID
- [ ] Replace placeholder email, phone and company number
- [ ] Update the team section in `about.html`

## Custom domain (pending)

`sivanvika.com` is not yet registered, so the `CNAME` file is intentionally
absent. Without DNS configured, a `CNAME` makes GitHub Pages serve the site
ONLY at the custom domain, which would make the `github.io` URL unreachable.

To enable it once the domain is registered and DNS points at GitHub:

```bash
printf 'sivanvika.com\n' > CNAME
git add CNAME && git commit -m "Enable sivanvika.com custom domain" && git push
```

Required DNS records for an apex domain:

```
@     A     185.199.108.153
@     A     185.199.109.153
@     A     185.199.110.153
@     A     185.199.111.153
www   CNAME <user-or-org>.github.io
```
