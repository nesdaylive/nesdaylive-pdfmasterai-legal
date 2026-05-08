"# PDF Master AI — Legal Pages

This folder contains ready-to-host HTML versions of:

- `privacy.html` — Privacy Policy (required for Play Console because the app uses `android.permission.CAMERA`)
- `terms.html` — Terms of Service

## How to host (free, 5 minutes — GitHub Pages)

1. Create a new public repo on GitHub, e.g. `nesdaylive/pdfmasterai-legal`.
2. Upload both `privacy.html` and `terms.html` to the repo root.
3. Repo → **Settings** → **Pages** → \"Deploy from a branch\" → branch `main`, folder `/ (root)` → **Save**.
4. Wait ~1 minute. Your URLs will be:
   - `https://nesdaylive.github.io/pdfmasterai-legal/privacy.html`
   - `https://nesdaylive.github.io/pdfmasterai-legal/terms.html`

## How to host on your own domain

Upload the two files to any static host (Netlify, Vercel, Cloudflare Pages, S3, your own server) and the URLs become e.g. `https://nesdaylive.com/privacy.html` / `https://nesdaylive.com/terms.html`.

## Then in Google Play Console

1. **App content** → **Privacy policy**
2. Paste the public URL of `privacy.html`
3. **Save**
4. Re-upload your AAB — the camera-permission warning will be gone.

## Inside the app

`/app/frontend/app/(tabs)/settings.tsx` already has Privacy Policy & Terms rows that open URLs. Update those two URLs to point to your hosted pages once published.
"
