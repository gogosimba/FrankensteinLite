# RuneLite plugin compatibility

The standalone host supplies lifecycle, dependency injection, EventBus/client-thread support, configuration persistence, overlays, panels, game canvas and rendering callbacks. It uses original plugins rather than reproducing their functionality.

Original Quest Helper, official Flipping Copilot, GOTR Helper and 117 HD were hosted without modifying their JARs. Generic hosting is separate from the small neutral semantic adapters that expose supported guidance to scripts.

## Rendering

Original RuneLite GPU and 117 HD have native OpenGL verification on NVIDIA RTX 3060 Ti hardware. Tests established real renderer callback ownership and frame rendering, HD operation after resize and return to software rendering when stopped. Their upstream mutual conflict is preserved; they are not run together.

![Real host configuration with original 117 HD enabled](../media/plugin-configuration.png)

This is a logged-out host-interface capture. It shows configuration state; the rendering claims come from separate native/runtime verification, not from this image alone.

## Coverage and limits

An isolated login-screen audit passed **133 of 134 original plugin startup/shutdown checks**. Configuration/Plugin Hub UI is unsupported. Lifecycle acceptance does not certify every in-game branch or third-party network service.

Enabled/disabled preferences and supported configuration persist across launches. A fresh portable-client restart restored Notes and a test setting. Optional plugins absent did not block startup.

This repository includes no plugin binaries, textures or third-party source. Names identify tested integrations and imply no endorsement.

[Architecture](ARCHITECTURE.md) · [Feature overview](../FEATURES.md)
