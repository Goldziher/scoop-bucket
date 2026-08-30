# Goldziher Scoop Bucket

[Scoop](https://scoop.sh) manifests for Goldziher's tools, mirroring the
[Homebrew tap](https://github.com/Goldziher/homebrew-tap) on Windows.

## Usage

```powershell
scoop bucket add goldziher https://github.com/Goldziher/scoop-bucket
scoop install poly
```

## Available

| App | Commands | Description |
| --- | --- | --- |
| [poly](https://github.com/Goldziher/poly) | `poly`, `polylint` | Universal zero-dependency linter & formatter — one binary, 30+ languages, no toolchain required. |

`poly` is the command. `polylint` is an alias for it, so the name the package
carries on PyPI and npm also works as a command.

## How manifests are updated

Each manifest is published by its own project's release workflow, which points
it at that release's prebuilt Windows archive and reuses the `sha256sums.txt`
already attached to the release — the hash is never recomputed here, so the
bucket and the release artifacts cannot disagree.

The `checkver` / `autoupdate` blocks let `scoop` refresh a manifest from a new
GitHub release directly, so a missed workflow run is recoverable.
