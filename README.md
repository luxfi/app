# @luxfi/app — Lux Desktop & Mobile

**Thin brand wrapper.** The Lux app *is* [`hanzoai/desktop`](https://github.com/hanzoai/desktop)
built with `VITE_BRAND=lux`. There is no duplicated app code here.

Decomplected by design — one implementation, brand as an orthogonal axis:
- **Implementation**: the `desktop/` submodule (hanzoai/desktop). One codebase for hanzo, zoo, lux.
- **Brand**: selected at build time via `VITE_BRAND` → `libs/brand-config` resolves Lux's
  name, logo, identity (`com.lux.desktop`), cloud overlay (`edge.lux.cloud`), chain
  (`lux.network`), and inference gateway.

## Build
```bash
pnpm init        # fetch the desktop submodule + install
pnpm dev         # run Lux desktop (dev)
pnpm tauri:build # desktop release
pnpm android     # / pnpm ios — mobile release
```

Hanzo and Zoo are the same app with `VITE_BRAND=hanzo` / `VITE_BRAND=zoo`.
