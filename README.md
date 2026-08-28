# PROVISION — Live Network build

This package is wired to the Provision Network Supabase project.

## Deploy
1. Upload every file in this folder to the GitHub Pages repository root.
2. Commit to `main`.
3. Keep Pages set to `main` / root and HTTPS enabled.
4. Reload the installed PWA after Pages redeploys.

## What is live
- Reads `public.current_offers` with the public publishable key.
- Adds live Provision Network offers alongside the existing Leeds pilot/context records.
- Subscribes to Realtime changes on `public.current_offer` and refreshes automatically.
- The public key in this build is expected to be browser-visible; RLS is the security boundary.

No service-role or secret key is included.
