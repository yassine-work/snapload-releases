# Snapload releases

Public download point for the [Snapload](https://github.com/yassine-work/snapload) Android
app. This repo intentionally contains **no application source code** — just:

- `index.html` — the download page, served via GitHub Pages at yt-code.me/snapload-releases/
- `snapload.apk` — the app itself, committed directly here so the download page can link to
  it as `snapload.apk` (same domain the whole way — no `github.com` address ever shown to
  whoever's downloading it)
- `update.json` — a small manifest the app polls once a day to check for a newer version
  (and to enforce a minimum supported version, if one is ever needed)

To ship a new version: build the APK, replace `snapload.apk` here with it, and update
`update.json`'s `latestVersionCode` / `latestVersionName` (and `minSupportedVersionCode`,
only if older installs must be forced to update).
