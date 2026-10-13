# DevCodePlus — Programs & Releases

This repository is the **public distribution channel** for DevCodePlus.

It contains **only** the built programs. The source code lives in a separate
private repository and is built by GitHub Actions.

## What lives here

- Release assets (Windows installer, macOS DMG, Linux packages)
- `sha256sums.txt` and per-file `.sha256` checksums
- GitHub release notes

## What does not live here

- Application source code
- Build configuration

## How updates reach your machine

DevCodePlus checks the **latest** release in this repository using
`https://api.github.com/repos/SaadSoftW/DevCodePlus/releases/latest`.

This endpoint must remain **public** so the check works without
authentication. GitHub returns `404` (not `403`) for private repositories on
unauthenticated requests, which the client cannot distinguish from
"no new release".

## Verifying a download

```sh
sha256sums.txt          # master list for every asset
*.exe.sha256            # per-file checksum
```

Compare the published hash before running any installer.


