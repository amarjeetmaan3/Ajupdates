# Ajupdates — Common Android Downloads

This public repository is the common distribution point for APKs from private source repositories. Keep every source repository private.

## Multi-app layout

- `apps/aj-auction.json` — latest-version metadata for AJ Auction.
- Add one metadata file per app using a stable lowercase app ID, e.g. `apps/smartoverlay.json`.
- APKs should be attached to releases in **this public repository**, using unique release tags such as `aj-auction-v0.2.2`. Never upload source code, signing keys, passwords, or private configuration.

## App metadata format

Each `apps/<app-id>.json` file must contain:
```json
{
  "appId": "aj-auction",
  "appName": "AJ Auction",
  "latestVersion": "0.2.2",
  "versionCode": 4,
  "apkUrl": "https://github.com/amarjeetmaan3/Ajupdates/releases/download/aj-auction-v0.2.2/app-release.apk",
  "releaseNotes": "Bug fixes and improvements"
}
```

Only publish metadata after the matching APK asset is available. Use a unique tag per app/version so releases do not overwrite each other. Android apps can read the public metadata at:
`https://raw.githubusercontent.com/amarjeetmaan3/Ajupdates/main/apps/aj-auction.json`

## Important
This repository is public. Anything committed here is publicly readable. Private repositories need an authorized publishing workflow (for example, a narrowly scoped publishing token stored as a GitHub Actions secret) to publish APK release assets here. Do not expose tokens in files or logs.
