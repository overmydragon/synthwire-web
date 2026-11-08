# Synthwire web assets (GitHub Pages)

Public, permanent hosting for the Synthwire catalogue data endpoint used by the
Android app and the web client.

| File | Purpose |
|---|---|
| `synthwire.json` | Catalog data: 42 newsletters, categories, and recent issue text (main content, capped). Read by the app with cache-busting. |
| `index.html` | Landing page with the Android APK download and links to the live web app. |

Live site: <https://overmydragon.github.io/synthwire-web/>

## Related

- Android app: <https://github.com/overmydragon/synthwire-android/releases>
- Web app / platform: <https://app.opzay.com>
- Legacy reader: <https://synthwire.opzay.com>

The JSON is generated from the Synthwire site database; newsletter HTML is sanitized and
capped before publication. No account data, emails, passwords or recovery codes are ever
included.
