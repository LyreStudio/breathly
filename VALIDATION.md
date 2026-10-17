# October 16, 2026 source qualification

Upstream range: `4107588b8c8bca076cedf4638b5a2fe53945b80e..3b86b698c59cf99e7aa834ddfde117b29c0c442d`. Lyre's additional package/lock changes follow the source-owned Expo 57 compatibility recommendations. Bun 1.3.14 and Node 24.19.0 were used locally on Windows. No hosted build runner was used.

| Check                                                                                                         | Result                                                                                 |
| ------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `bun install --frozen-lockfile --ignore-scripts`                                                              | Pass; final clean dependency layout preserves the exact lock.                          |
| `bun run validate:static`                                                                                     | Pass: types, lint, formatting and 83 tests in 14 suites; 30.041 seconds.               |
| `bun run validate:expo`                                                                                       | Pass: dependency versions current for SDK 57 and all 20 doctor checks; 33.599 seconds. |
| `bun node_modules/expo/bin/cli export --platform all --output-dir dist/daily-export-20261016 --max-workers 1` | Pass: Android/iOS Hermes and web JavaScript exports; 79.551 seconds.                   |

The recorded input digest before documentation/provenance updates is `b9894f4b33240b7f4f5ea6adc6fc55603e1da844d661eba526702f4f160ba379`. Retained log SHA256 values are `53a22aacfda779a8e85269ab1da44e0d76167457b4885f788890b12af7e8f9bc` (static), `f39dec9f3bfe2ab6dc5d11bf1f376471f91e92f1d342145ebac78cee49184796` (Expo health) and `c9530a7a7fb3c342dbad438f66a54e8ff31a08aeffa06f3d9dbbe8b86e1a5995` (exports). Documentation/provenance added after those runs changes no runtime, dependency or export input.

Earlier format attempts encountered Windows CRLF checkout bytes; the isolated checkout's UTF-8 text was normalized to canonical LF. The initial upstream lock failed current Expo recommendations. After the bounded patch update, a stale duplicate native dependency remained in the installed tree; a clean frozen-lock install resolved it. The failed attempts are retained separately, rather than being described as passes.

Maestro is absent, so the retained native time-limit flow has not run. No native build, device installation, iOS signing, EAS deployment or store submission was performed. `nativeBuildVerifiedByLyre` remains false. These source checks do not establish installed-device or store acceptance.
