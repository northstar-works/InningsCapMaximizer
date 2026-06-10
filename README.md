# Innings Cap Maximizer v1.6.7 b32

Android WebView app for fantasy baseball innings-cap planning.

This build updates the UI for the v28ah backend fields:
- `active_rp_projected_before_sunday`
- `active_rp_projected_points_before_sunday`
- `projected_rp_points_before_sunday`
- `active_rp_projected_points_rows`

Dashboard wording now shows pre-Sunday projected RP IP and projected RP points separately from Sunday SP eligibility.

## GitHub Actions

This project includes workflows for the same signed-release / F-Droid style publishing method used for StreamVault/Fantag:

- `.github/workflows/android-release.yml`
- `.github/workflows/fdroid-repo.yml`

Required repository secrets:

- `FANTAG_KEYSTORE_BASE64`
- `FANTAG_KEYSTORE_PASSWORD`
- `FANTAG_KEY_ALIAS`
- `FANTAG_KEY_PASSWORD`

See `scripts/init-github-and-fdroid.md` for exact first-push and tag commands.
