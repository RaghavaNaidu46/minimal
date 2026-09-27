# Minimal — support site

Public pages for **Minimal – Block Apps & Focus** (iPhone), served with GitHub Pages at
<https://raghavanaidu46.github.io/minimal/>.

| Page | URL | Used for |
|---|---|---|
| Home | `/minimal/` | App Store marketing URL |
| Support | `/minimal/support/` | App Store support URL |
| Privacy Policy | `/minimal/privacy/` | App Store privacy policy URL, in-app link |
| Terms of Use | `/minimal/terms/` | Subscription terms (Apple Standard EULA) |
| Update config | `/minimal/version.json` | Read by the app at launch (`UpdateChecker`) |

## `version.json`

```json
{ "minimumForcedVersion": "1.0", "appStoreURL": "https://apps.apple.com/app/id6816326753" }
```

- The app suggests an update (once per version) when the App Store has a newer version than the one running.
- **`minimumForcedVersion`** — builds below it can't be used until they update. Leave it at the oldest version that
  still works; raise it only for a critical fix, and only after that version is live on the App Store (the app forces
  only when the store already has something newer).
- **`appStoreURL`** — where "Update" goes. Empty means the link from Apple's lookup.

Plain HTML + one stylesheet; no build step (`.nojekyll`). Keep the privacy policy in step with the app: if the app
starts collecting or sending any data, this page and the App Store privacy answers must change first.
