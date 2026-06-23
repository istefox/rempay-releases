# rempay — release feed

Update feed for **rempay** (macOS). The application source is private; this
repository hosts only the public release artifacts consumed by the in-app
auto-updater (Sparkle).

- `appcast.xml` — the Sparkle feed. The app reads it from
  `https://raw.githubusercontent.com/istefox/rempay-releases/main/appcast.xml`.
- Release binaries are attached as assets to each GitHub Release; the
  `enclosure` URLs in `appcast.xml` point to them.

Updates are signed with an EdDSA key; the matching public key is embedded in
the app. Tampered or unsigned builds are rejected by the updater.
