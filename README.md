# idols Backend — releases

Public release channel for **idols Backend** Windows installers.

Repository: [github.com/hqnatx/idols-Backend-release](https://github.com/hqnatx/idols-Backend-release)

**idols Link** updates are published separately: [idols-link-release](https://github.com/hqnatx/idols-link-release).

## How auto-updates work

When **idols Link** starts (once per session, if update checks are enabled):

- If **Local** backend mode is on and idols Backend is **already installed**, Link reads the newest [GitHub Release](https://github.com/hqnatx/idols-Backend-release/releases) here.
- It compares the installed `idols Backend.exe` product version with the release tag.
- If the release is newer, Link downloads the setup, runs it, and shows install progress.

First-time install is still offered from the Backend tab when Backend is missing.

Users can disable checks in **idols Link → Settings → Appearance → Disable update checks**.

## Publishing a release

1. Build the backend installer, e.g. `idols Backend Setup-1.0.0.exe`.
2. Open [Releases](https://github.com/hqnatx/idols-Backend-release/releases) → **Draft a new release**.
3. **Tag** = version to ship, e.g. `v1.0.0` or `1.0.0` (must be **higher** than the version players already have).
4. Attach the `.exe` or `.msi` installer.
5. Optional: changelog in the release body.

### Asset naming

| Include in filename | Example |
|---------------------|---------|
| `backend` or `idols`, plus `setup` / `installer` | `idols Backend Setup-1.0.0.exe` |

Do **not** put `link` or `launcher` in the backend installer name.

## Source code

Development source lives in `idols-Backend`. **This repo is only for player-facing installers.**

## Notes

- Releases must be **published** (not draft).
- Pre-releases are used only if no stable release has a matching installer.
- The Windows executable **product version** should match the release tag (e.g. tag `v1.0.0` → product version `1.0.0.0`).
