# PROVISION — Live Network v4

This build is wired to the Provision Network Supabase project.

## Before deploying
Run `20260828_provision_provenance_location.sql` once in the Supabase SQL Editor. It adds safe update provenance to `current_offers`, the authenticated source-profile/location RPC, source Realtime, and human-friendly food counting defaults.

## Deploy
1. Upload every file in this folder to the GitHub Pages repository root.
2. Commit to `main`.
3. Keep Pages set to `main` / root and HTTPS enabled.
4. Reload the installed PWA after Pages redeploys. The service-worker cache has been bumped.

## v4 changes
- Null source coordinates no longer become 0,0; distance shows as unknown until location exists.
- Food origin distance is no longer fabricated from consumer-to-seller distance.
- Live assertions read like `surplus · declared 16:20`, not `verified`.
- Live evidence surfaces raw strength such as `declared · 1/5`.
- Consumer provenance distinguishes SOURCE DIRECT, RETAILER FEED, PUBLIC FEED, OBSERVATION and INFERRED updates.
- Source profile changes can refresh consumer distance through Realtime.

No service-role or secret key is included.
