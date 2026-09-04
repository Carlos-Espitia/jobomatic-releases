# Jobomatic — Releases

Release binaries and the auto-update feed for **Jobomatic**, a desktop job-application
assistant. This repository holds no source code; it exists so the app's updater has a
public place to fetch from while development stays private.

## Downloads

Grab the latest installer from the [Releases page](https://github.com/Carlos-Espitia/jobomatic-releases/releases/latest).

Windows will show a SmartScreen warning on first run — the installer is not yet
code-signed. Choose **More info → Run anyway** if you trust the source.

## What is published here

Each release carries the files `electron-updater` needs to detect and verify an update:

| File | Purpose |
|---|---|
| `Jobomatic-Setup-<version>.exe` | The NSIS installer |
| `latest.yml` | Version manifest and SHA-512, read by the updater |
| `*.blockmap` | Enables differential downloads, so an update transfers only what changed |

Installed copies check this repository for updates automatically. Downloads are never
automatic — the app asks first, because an update landing mid-run would interrupt an
application in progress.

## Disclaimer

Automating job platforms may violate their terms of service and can result in account
suspension. Use at your own risk.
