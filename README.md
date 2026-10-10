# Tristan Meynier portfolio

Static, framework-free source for [tristanmeynier.com](https://tristanmeynier.com). The repository contains only HTML and static assets; it has no package installation, build process, server, or database.

## Local preview

From the repository root:

```sh
python3 -m http.server 8080
```

Then open `http://localhost:8080/`.

## Cloudflare Pages configuration

Connect this GitHub repository to a Cloudflare Pages project with these settings:

- Production branch: `main`
- Framework preset: `None`
- Build command: `exit 0`
- Build output directory: `.`
- Root directory: leave blank

After the first deployment, open the Pages project in Cloudflare, select **Custom domains**, and add `tristanmeynier.com`. Because this is an apex domain, the domain must be an active zone in the same Cloudflare account and use the Cloudflare-assigned nameservers. Cloudflare will provision HTTPS automatically.

Optionally add `www.tristanmeynier.com` and configure a Cloudflare redirect from `www` to the apex domain.

No `CNAME` file or repository secret is required.

## Structure

- `index.html` — portfolio homepage
- `assets/` — profile image and CV
- `hepha/` — Hepha project page and media
- `what-makes-a-generalist-robot-policy/` — technical report page and PDF
- `what-robot-data-should-we-collect-next/` — research status page
- `robots.txt` and `sitemap.xml` — production-domain discovery metadata
