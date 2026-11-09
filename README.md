# Aisle Zero

Personal study guide to Radian and grocery merchandising. Static site (one `index.html`) reading from Supabase project `aisle-zero` (gmdgpwylevdbfhxxbavl).

## Deploy (GitHub Pages)
1. Create an empty GitHub repo `aisle-zero`, add `index.html`, push.
2. Settings → Pages → Deploy from branch `main`, folder `/`.

## One-time Supabase settings (dashboard)
- Authentication → URL Configuration: set **Site URL** to the Pages URL (e.g. `https://<user>.github.io/aisle-zero/`) and add it to **Redirect URLs**. Magic links won't return to the site without this.
- Optional: Authentication → Providers → Email → turn off "Allow new users to sign up" after your first sign-in. (Not required: private content is gated by an email allowlist in the database either way.)

## Content rules
- Every row has `verified_at`; rows without it are never returned.
- `visibility = gated` (Constellation, lesson notes, scenarios, your progress) is readable only by allowlisted emails (`app_members`).
- No personal relationship notes anywhere.
