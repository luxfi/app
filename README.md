# @luxfi/app — Lux cross-platform app

Lux's desktop **and** mobile app, built on **[@hanzo/gui](https://github.com/hanzoai/gui)**
(React 19 + bun). One codebase ships:

- **iOS / Android / web** via **Expo** (`expo run:ios`, `expo run:android`, `expo start --web`)
- **desktop** (macOS / Windows / Linux) via **Tauri**

It is the lux sibling of `hanzoai/desktop` and `zooai/app` — thin, reusing `@hanzogui/*`
packages rather than re-implementing UI. Branding (name/slug/scheme) is lux.

## Backends it drives

| Concern | Repo | Lang |
|---|---|---|
| Node (consensus/chains embedded) | `luxfi/node` | Go |
| AI VM + mining + rewards | `luxfi/ai` (`pkg/aivm`, `pkg/miner`, `pkg/rewards`) | Go |
| Reward/receipt conformance | `luxfi/ai/conformance` (golden vectors vs the Rust `hanzod` port) | — |

## Develop

```bash
bun install
bun start              # expo (mobile/web)
# desktop (Tauri) wiring: mirror @hanzogui/studio dev:tauri
```

## Status

Phase 1 scaffold (from `@hanzogui/expo-router-starter`, rebranded lux). Next: port the
onboarding/agent UX from `zooai/app`'s `zoo-desktop`, add the Tauri desktop target, and wire
the node-manager client to `luxfi/node` + `luxfi/ai`.
