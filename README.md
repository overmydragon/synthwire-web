# Synthwire web assets (GitHub Pages)

Public, permanent hosting for the Synthwire catalogue data endpoint used by the
Android app and the web client.

| File | Purpose |
|---|---|
| `synthwire.json` | Catalog data: 100 newsletters, categories, and recent issue text (main content, capped). Read by the app with cache-busting. |
| `index.html` | Liquid-glass landing page: warm brutalist typography on layered glass panels, light/dark theme toggle, Android APK download and links to the live web app. No paid tiers, no ads. |
| `fonts/` | Self-hosted OFL 1.1 latin subsets (Inter, Playfair Display, JetBrains Mono) so the typography does not depend on third-party font services. |

Live site: <https://overmydragon.github.io/synthwire-web/>

## Related

- Android app: <https://github.com/overmydragon/synthwire-android/releases>
- Web app / platform: <https://app.opzay.com>
- Legacy reader: <https://synthwire.opzay.com>

The JSON is generated from the Synthwire site database; newsletter HTML is sanitized and
capped before publication. No account data, emails, passwords or recovery codes are ever
included.


## Design notes

- Material: a glass system with an outer shell, a readable inner scrim plate,
  a specular rim, warm refracted light, and layered back plates. Typography and
  the orange accent carry over from the original Synthwire identity.
- Navigation mirrors the Android v0.6.2 floating glass tab bar: a detached glass
  capsule with text links on desktop, icon-only links on mobile, and an accent pill
  that follows the active section.
- Theme: follows the OS preference on first load; the header toggle overrides it
  and stores the choice in `localStorage`.
- Motion: one authored hero sequence (the glass stage assembles), pointer-driven
  tilt and specular glint on fine pointers, a slow specular sweep, and a limited
  scroll reveal on the feature list. Every effect is disabled or reduced under
  `prefers-reduced-motion`.
- Anti-slop: the page passes the Gesso anti-slop detector with zero gating hits.
  Deliberate glass rims, layered plates and the live-status pill are marked with
  visible `--slop-allow` / `data-slop-allow` opt-outs instead of being removed.
