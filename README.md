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
| [ai-rulez](https://github.com/Goldziher/ai-rulez) | `ai-rulez` | Manage agent configuration, skills, and governance across coding agents. |
| [gitfluff](https://github.com/Goldziher/gitfluff) | `gitfluff` | Commit message linter with presets, custom formats and cleanup automation. |
| [polylint](https://github.com/Goldziher/polylint) | `poly`, `polylint` | Universal zero-dependency linter & formatter — one binary, 30+ languages, no toolchain required. |
| [skif](https://github.com/Goldziher/skif) | `skif` | Dependency and package-manager linter for JavaScript and TypeScript monorepos. |

`poly` is the command. `polylint` is an alias for it, so the name the package
carries on PyPI and npm also works as a command.

## How manifests are updated

Manifests point to each project's prebuilt Windows archive and use the SHA-256
from its published release checksums. Project release workflows can update
manifests automatically.

The `checkver` / `autoupdate` blocks let `scoop` refresh a manifest from a new
GitHub release directly, so a missed workflow run is recoverable.
