# Tech Group Kenya

Official marketing site for [Tech Group Kenya](https://techgroupkenya.co.ke) — Kenya's tech community connecting developers, students, and startups through events, learning, jobs, and networking.

**Live site:** [https://techgroupkenya.co.ke](https://techgroupkenya.co.ke)

## Overview

This is a static website with no build step. The homepage (`index.html`) is a single-page layout with anchored sections for features, about, contact, donate, careers, and FAQ. Standalone pages cover legal content and errors; several legacy URLs redirect to homepage sections or external subdomains.

## Tech stack

- HTML5, CSS3, vanilla JavaScript
- Images and media served from [cdn.techgroupkenya.co.ke](https://cdn.techgroupkenya.co.ke)
- [Formspree](https://formspree.io) for the contact form
- JSON-LD structured data for SEO
- Security headers via `_headers` (Cloudflare Pages / compatible hosts)

## Project structure

```
techgroupkenya/
├── index.html              # Main landing page
├── about.html              # Redirect → /#about
├── contact.html            # Redirect → /#contact
├── services.html           # Redirect → /#features
├── donate.html             # Redirect → /#donate
├── careers.html            # Redirect → app.techgroupkenya.co.ke/jobs
├── terms-of-service.html   # Terms of service
├── 404.html                # Custom not-found page
├── assets/
│   ├── tgk.css             # Main stylesheet
│   ├── tgk-single.css      # Alternate layout styles
│   ├── tgk-loader.css      # Page loader
│   ├── tgk-legal.css       # Legal pages
│   └── tgk-404.css         # 404 page
├── scripts/
│   ├── tgk.js              # Core UI (nav, hero, scroll, Formspree init)
│   ├── tgk-loader.js       # Loader utilities
│   ├── tgk-contact-form.js # Contact form validation & submission
│   ├── tgk-email.js        # Obfuscated email reveal
│   └── tgk-legal.js        # Legal page helpers
├── sitemap.xml
├── robots.txt
├── ads.txt
├── CNAME                   # Custom domain (techgroupkenya.co.ke)
└── _headers                # HTTP security headers
```

## Local development

No install or build is required. Serve the project root with any static file server:

```bash
# Python
python -m http.server 8080

# Node (npx)
npx serve .

# PHP
php -S localhost:8080
```

Then open [http://localhost:8080](http://localhost:8080).

## Deployment

The site is deployed as static files. The `CNAME` file points the custom domain to `techgroupkenya.co.ke`. Push to the configured hosting branch (e.g. GitHub Pages or Cloudflare Pages) to publish.

After deploying, verify:

- [https://techgroupkenya.co.ke/sitemap.xml](https://techgroupkenya.co.ke/sitemap.xml)
- Contact form submission
- Redirect stubs (`/about.html`, `/contact.html`, etc.)

## Related properties

| Property | URL |
|----------|-----|
| Community | [community.techgroupkenya.co.ke](https://community.techgroupkenya.co.ke) |
| Blog | [blog.techgroupkenya.co.ke](https://blog.techgroupkenya.co.ke) |
| Skill Me (courses & jobs) | [app.techgroupkenya.co.ke](https://app.techgroupkenya.co.ke) |
| Tech Events | [events.techgroupkenya.co.ke](https://events.techgroupkenya.co.ke) |
| CDN | [cdn.techgroupkenya.co.ke](https://cdn.techgroupkenya.co.ke) |

## License

© Tech Group Kenya. All rights reserved.
