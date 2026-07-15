# OneNotch Releases

Public source of truth for OneNotch beta updates.

## Update feed

OneNotch reads the Sparkle appcast from:

`https://raw.githubusercontent.com/tranhuy2706/OneNotch-releases/main/appcast.xml`

The feed is intentionally empty until the first signed DMG is published.

## Publishing a beta

1. Build, sign, notarize, and sign the DMG with Sparkle from the OneNotch source repository.
2. Create a GitHub release with a tag such as `v0.1.1`.
3. Upload the DMG as a release asset.
4. Add a matching `<item>` and signed `<enclosure>` to `appcast.xml`.
5. Commit and push the appcast only after the release asset is available.

Sparkle signing uses the `onenotch_tranhuy2706` account in the maintainer's macOS Keychain. Never commit or upload the private signing key.
