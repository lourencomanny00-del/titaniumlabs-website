# Titaniumlabs Website

Three pages + assets, ready to deploy to GitHub Pages, Cloudflare Pages, Netlify, or any static host.

## Files

- `index.html` — homepage (landing page)
- `apply.html` — application form (submits to hello@titaniumlabs.tech via Formsubmit.co)
- `thank-you.html` — confirmation page (fires Google Ads conversion via GTM)
- `assets/` — all images, video, and logos

## Deploy to GitHub Pages

1. Create a new repo on GitHub.
2. Upload **the contents** of this folder (not the folder itself) to the root of the repo.
3. Settings → Pages → Build from `main` branch → `/ (root)`.
4. Your site will live at `https://<username>.github.io/<repo>/`.

## First-time form activation

The very first time someone submits the apply form, Formsubmit.co sends a one-time activation email to `hello@titaniumlabs.tech`. **Click the link in that email** — after that, all submissions deliver normally.

## Google Ads conversion tracking

GTM container `GTM-WK5T3BGG` is installed on all three pages. In GTM:

1. Create a **Custom Event** trigger named `apply_conversion`.
2. Create a **Google Ads Conversion Tracking** tag with your conversion ID + label.
3. Attach the trigger to the tag and publish.

Every visit to `thank-you.html` fires the conversion automatically.
