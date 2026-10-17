# Breathly in the Lyre marketplace

This is a public source fork of [mmazzarolo/breathly-app](https://github.com/mmazzarolo/breathly-app), curated for the Lyre marketplace. Original authorship, branding and license are retained; it is not an original Lyre app or a new Lyre-published store binary.

Upstream source checkpoint: `3b86b698c59cf99e7aa834ddfde117b29c0c442d`, reviewed October 16, 2026. License: **MPL-2.0**. The historical September 10 popularity observation is not a current availability or qualification claim.

![Upstream Breathly mobile screenshot](screenshots/mobile.png)

The screenshot is copied unchanged from upstream `.github/iphone-1.png` at the earlier `4107588b8c8bca076cedf4638b5a2fe53945b80e` checkpoint. It is upstream presentation artwork, not evidence of a new Lyre device test.

## October 16 source update

The seven-commit upstream range `4107588b..3b86b698` fixes the Android two-digit exercise time limit, adds the Android themed icon and updates Expo 57 patches. The upstream Android regression and Maestro flow are retained. Lyre keeps the upstream design, names and MPL-2.0 source terms.

Local qualification found that the upstream lock needed eight additional same-SDK patch recommendations. The source-owned `expo install --fix --bun` updates only those Expo 57 dependencies and their required lock closure, including Expo 57.0.30 and React Native 0.86.3. These package/lock adaptations are separate from the recorded upstream commit. No service, store or author account is activated.

Typecheck, lint, formatting, all 83 tests, all 20 Expo health checks and local Android/iOS/web JavaScript exports pass. Windows checkout line endings and stale duplicate dependencies were corrected in the isolated build environment; earlier failed attempts remain in the Lyre release ledger. See [VALIDATION.md](VALIDATION.md) for scope and evidence identities.

The fork's `.gitattributes` keeps canonical LF checkout bytes so the same formatter command works on Windows and Unix. It changes no application source content.

This is a source update. Maestro is unavailable in the local environment, so its native flow remains pending. No APK/IPA, installed-device acceptance or store release is claimed; `nativeBuildVerifiedByLyre` remains false.

## Use the released app

[Original author's iOS release](https://apps.apple.com/us/app/breathly/id1454852966) · [Original author's Android release](https://play.google.com/store/apps/details?id=com.mmazzarolo.breathly)

These links go to the original author's listings. Store binaries may differ from this source checkpoint.

## Develop the source

This checkout targets Expo 57 and React Native 0.86. Install Bun and use the committed lockfile:

```sh
bun install --frozen-lockfile
bun run start
```

The source includes native modules and an Expo development-client configuration; a browser preview does not prove native behavior. Android development requires the Android SDK; iOS requires macOS/Xcode. Existing `bun run android` / `bun run ios` scripts create native development builds. Those commands were not run for this listing.

Upstream checks include `bun run test`, `bun run typecheck`, `bun run lint`, and Maestro native flows. Do not run EAS submission scripts against the original author's project; use your own identity and signing configuration for a separately released app.

The original MPL-2.0 license and source remain intact. README.md records third-party asset origins, including commissioned audio and screenshot presentation tools. Retain notices and review those asset terms before a separately branded binary distribution; this listing does not relicense them as MIT.

## Lyre boundary

Open the repository as source and follow its own setup. Merely listing this app does not add its native modules to the Lyre companion, install it, grant host access, configure signing or certify remote preview compatibility. No native build, device installation, credential access or store submission was performed in this marketplace task.

Use the original license and notices when adapting or redistributing the source. Upstream app terms and identities do not become Lyre's subscription, privacy or release policy.
