# Snapload releases

Public download point for the [Snapload](https://github.com/yassine-work/snapload) Android
app. This repo intentionally contains **no application source code** — just:

- `index.html` — the download page, served via GitHub Pages
- `update.json` — a small manifest the app itself polls once a day to check for a newer
  version (and to enforce a minimum supported version, if one is ever needed)
- Release APKs, attached to this repo's [Releases](../../releases)

To ship a new version: build the APK, attach it to a new GitHub Release here named to match
the version, then update `update.json`'s `latestVersionCode` / `latestVersionName` (and
`minSupportedVersionCode`, only if older installs must be forced to update).
