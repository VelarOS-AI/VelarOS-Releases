# VelarOS Releases

Private binary artifact store for every independently packaged VelarOS product and resource plugin.

- Product source remains in its owning repository; this repository stores installers and release
  manifests only.
- Every product uses a unique tag prefix, such as `desktop-v<version>` or `host-v<version>`.
- macOS products are built, signed, notarized, and staged on the release Mac. Windows and Linux
  products are built natively in the owning source repository's GitHub Actions workflow.
- GitHub prereleases are candidates, not website releases.
- VelarOS Cloud administrators control the active website version.
- Release assets are immutable; bump the component version instead of replacing bytes.
- Never commit source code, environment files, credentials, or provider keys here.

The machine-readable product registry is [`products.json`](products.json). Every future packaged
VelarOS product must be registered there before its first candidate is uploaded.
