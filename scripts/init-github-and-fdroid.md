# Innings Max GitHub + F-Droid Setup

## Repository secrets
Add these same signing secrets used by StreamVault/Fantag:

- `FANTAG_KEYSTORE_BASE64`
- `FANTAG_KEYSTORE_PASSWORD`
- `FANTAG_KEY_ALIAS`
- `FANTAG_KEY_PASSWORD`

The Gradle file also supports `INNINGS_KEYSTORE_*` names, but the GitHub workflows are wired to the existing `FANTAG_*` names so you can reuse the same keystore method.

## First push

```bash
git init
git branch -M main
git add .
git commit -m "Initial Innings Max Android app v1.6.7 b32"
git remote add origin https://github.com/northstar-works/InningsCapMaximizer.git
git push -u origin main
```

## First release / F-Droid publish

```bash
git tag v1.6.7-b32
git push origin v1.6.7-b32
```

That tag triggers:

- `.github/workflows/android-release.yml` — signed release APK and GitHub Release.
- `.github/workflows/fdroid-repo.yml` — signed APK copied into an F-Droid repository and published to `gh-pages`.

## F-Droid repo URL after GitHub Pages is enabled

```text
https://northstar-works.github.io/InningsCapMaximizer/repo
```

Enable GitHub Pages in the repository settings with branch `gh-pages` and root `/`.
