# captainsolo.ca — Production Static Site Build

Production static deployment artifact for **[captainsolo.ca](https://captainsolo.ca)**.

Extracted and verified from the most fresh production backup archive (`public_html-20260625-1738.zip`).

---

## 🚀 Cloudflare Pages Deployment (Recommended: $0/yr Stack)

This repository is structured for direct static deployment to **Cloudflare Pages**:

1. Log in to your [Cloudflare Dashboard](https://dash.cloudflare.com/).
2. Navigate to **Workers & Pages** → **Create application** → **Pages** → **Connect to Git**.
3. Select this repository: `solufelo/captainsolo.ca` (branch: `main`).
4. Configure Build Settings:
   - **Framework preset**: None
   - **Build command**: *(leave empty)*
   - **Build output directory**: `/` *(or leave empty)*
5. Click **Save and Deploy**.
6. Under **Custom domains**, add `captainsolo.ca` and `www.captainsolo.ca`.

### Included Platform Configurations

- `_redirects`: Handles React Router SPA client-side routing (`/* /index.html 200`) so paths like `/voice-tags` and `/blog` load without 404s.
- `_headers`: Applies immutable caching for fingerprint-hashed assets (`/assets/*`) and fast revalidation for 3D models (`/models/*`) and `index.html`.
- `.htaccess`: Original Apache / cPanel rewrite and compression rules preserved for reference.
- `sitemap.xml` & `robots.txt`: Search engine indexing and SEO configuration intact.
