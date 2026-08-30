# PROVISION — Live Network v5

Consumer surface for the Provision Network.

## This release
- Reads commitment fields from `current_offers`: physical quantity, reserved quantity and available-to-claim.
- Claim / hold requests use `request_claim`; cancellation uses `cancel_claim`.
- Consumer authentication appears only when a commitment or private demand signal is created.
- `I want this` creates privacy-preserving demand through `upsert_demand_signal`.
- Reads `public_evidence` and creates short-lived signed URLs for evidence assets in the private bucket.
- Live Source records no longer invent chain steps when supply-chain evidence is absent.
- Unknown source coordinates display as `Location not yet resolved`.
- Live evidence is separated cleanly from `How Provision knows` provenance.
- Realtime offer/source/evidence updates remain active; authenticated consumers also listen for claim changes.

Database contract: `20260830_provision_network_expansion_04.sql` (already applied to Production).

Deploy all files at repo root on GitHub Pages. Add the deployed consumer URL to Supabase Authentication redirect URLs before testing magic-link claims/demand.
