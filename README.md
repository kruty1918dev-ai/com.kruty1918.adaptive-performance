# com.kruty1918.adaptive-performance

Reusable adaptive-performance primitives: frame-time budget monitoring with
percentile snapshots and startup resource prewarm.

## Install (Unity Package Manager)

Package Manager → **+** → **Add package from git URL**:

```
https://github.com/kruty1918dev-ai/com.kruty1918.adaptive-performance.git
```

or in `Packages/manifest.json`:

```json
"com.kruty1918.adaptive-performance": "https://github.com/kruty1918dev-ai/com.kruty1918.adaptive-performance.git#v0.1.0"
```

The repository is private — Git credentials (PAT / Git Credential Manager)
are required on every machine that resolves the package.

## API surface

| Type | Purpose |
|---|---|
| `IFrameBudgetMonitorService` | Frame-time budget monitoring with percentile snapshots (p50/p95/p99) |
| `IStartupPrewarmService` | Startup resource prewarm (shaders, meshes) before first interactable frame |
| `IScenePreActivationInitializer` | Work that must finish before a scene activates |
| `FrameBudgetSettings` / `FrameTimeSnapshot` | Config and snapshot value types |
| `PrewarmSettings` | Prewarm configuration |

## Model

Reusable UPM package extracted from Moyva. No game-specific dependencies;
compose via your own installer/DI.
