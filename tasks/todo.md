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

## Google Analytics and Search Console

- [x] Create a dedicated GA4 property and web data stream for `codewithandrewford.com`
- [x] Add the GA4 tag to the Astro page without collecting custom personal data
- [x] Correct the canonical site URL from the old `.co.nz` hostname to `.com`
- [x] Add and verify `/sitemap.xml` and `/robots.txt`
- [x] Build, commit, push, and deploy the updated site
- [x] Verify the production analytics tag, canonical metadata, sitemap, and robots rules
- [x] Add and verify the site in Google Search Console
- [x] Submit the production sitemap and confirm Google accepts it
- [x] Confirm the pre-existing Coolify applications remain running
- [ ] Confirm Google clears the historical `Deceptive pages` warning after its security review

Analytics and indexing setup completed on 8 August 2026:

- GA4 property: `Code with Andrew Ford` (`549081768`)
- Web stream: `Code with Andrew Ford Website` (`15401615421`)
- Measurement ID: `G-NWMRVPLT4E`
- Production commit: `30f1aebeaf933af6b3635d4915c23e005958da7c`
- Coolify deployment: `wp2ars036wrk7e6tshrx9v7m`, finished successfully
- Production exposes the GA4 tag, `.com` canonical and Open Graph URLs, valid `/sitemap.xml`, and `/robots.txt`
- Search Console domain property `codewithandrewford.com` reports Andrew as a verified owner
- Search Console accepted `https://codewithandrewford.com/sitemap.xml` with status `Success` and one discovered page
- The Search Console property is associated with the new GA4 property and web stream
- GA4 real-time reporting received the production verification visit and reported one active user from New Zealand
- Search Console found the homepage through the sitemap and accepted a manual indexing request into its priority crawl queue
- Search Console reported a historical `Deceptive pages` issue with no sample URLs. The current static site was reviewed and a security review request was submitted successfully.
- andrewford.co.nz, FastTempo, both Health Scan Express resources, Selfhost, and SlideVids still report as running
