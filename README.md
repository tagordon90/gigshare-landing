# gigshare.live static site

Minimal static pages for the apex domain (legitimacy, contact, Stripe Connect handoff).

## Stripe Connect (backend env)

Set these on the **API** (not in this folder) to match the deployed URLs exactly:

- `STRIPE_CONNECT_ONBOARDING_RETURN_URL` → `https://gigshare.live/stripe-connect/return/`
- `STRIPE_CONNECT_ONBOARDING_REFRESH_URL` → `https://gigshare.live/stripe-connect/refresh/`

Trailing slashes match Cloudflare Pages directory indexes by default. If your host serves without a trailing slash, use the same form in `.env` as in the browser address bar.

## Cloudflare Pages

1. Connect the Git repo (or upload this directory).
2. **Build command:** leave empty (static HTML, no build).
3. **Build output directory:** `/` (repository root for this project — the folder that contains `index.html`).
4. Attach custom domain **gigshare.live** in Pages → Custom domains.
5. After deploy, verify:
   - `https://gigshare.live/`
   - `https://gigshare.live/stripe-connect/return/`
   - `https://gigshare.live/stripe-connect/refresh/`

Deep links use the Expo app scheme **`gigsharemobile://`** (see `GigShareMobile/app.json`). Optional later: Universal Links on `gigshare.live` so HTTPS opens the app without a custom scheme.
