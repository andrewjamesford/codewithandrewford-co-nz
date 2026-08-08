# Code with Andrew Ford landing page

- [x] Inspect the project and reference website
- [x] Scaffold a minimal Astro site
- [x] Build the responsive landing page
- [x] Verify the production build
- [x] Check the page in a real browser at desktop and mobile sizes

## Review

Built a one-page static Astro site with responsive layouts, accessible page landmarks, reduced-motion support, dark-mode styling, SEO metadata, and direct links to the channel and three current videos.

Verification completed on 8 August 2026:

- `npm run build`: passed with zero errors, warnings, or hints
- `npm audit --omit=dev`: found zero vulnerabilities
- Desktop browser check at 1440 by 1000: passed
- Mobile browser check at 390 by 844: passed
- Browser console: zero errors and zero warnings
- All three YouTube thumbnail requests returned HTTP 200

## GitHub publishing

- [x] Confirm the source files included in the repository
- [x] Initialise the repository on the `main` branch
- [x] Commit the verified site
- [x] Create and push the public GitHub repository
- [x] Confirm public visibility and the remote commit

Published to `https://github.com/andrewjamesford/codewithandrewford-co-nz` with `main` as the default branch. GitHub reports the repository visibility as public, and the local branch matches `origin/main`.

## Coolify deployment

- [x] Record the current DNS state for `codewithandrewford.com`
- [x] Inventory existing Coolify projects, resources, and domains without changing them
- [x] Create a separate Coolify application for this repository
- [x] Configure and verify the static Astro build before domain cutover
- [x] Attach `codewithandrewford.com` and `www.codewithandrewford.com`
- [x] Verify DNS, TLS, redirects, page content, and linked assets in production
- [x] Confirm existing Coolify applications still report their original status

Deployment verification completed on 8 August 2026:

- Coolify application `n102hz43n2a11fnqjmqtdp3f` runs in its own project and environment
- Nixpacks uses Node 24 through `NIXPACKS_NODE_VERSION=24`
- Deployment `n11ew87l279zqee2ly9f0o7o` built commit `e094084718cd3647efada4aa75efa39f129c6ec4` successfully
- `https://codewithandrewford.com/` returns HTTP 200 with the expected title and page content
- `https://www.codewithandrewford.com/` redirects to the canonical non-www domain
- HTTP requests redirect to HTTPS, and `/favicon.svg` returns HTTP 200
- The existing andrewford.co.nz, FastTempo, Health Scan Express API, Health Scan Express Web, Selfhost, and SlideVids resources all still report as running
