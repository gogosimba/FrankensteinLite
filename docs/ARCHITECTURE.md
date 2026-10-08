# Architecture

FrankensteinLite separates the upstream runtime, compatibility layer and script contracts.

```text
Pristine RuneLite runtime + original plugins
                    ↓
Standalone host / compatibility services / semantic adapters
                    ↓
Neutral public bot API and provider contract
                    ↓
Looping scripts and Bot Hub
```

## Runtime and plugins

The host supplies its own Swing/AWT application and game canvas. Generic compatibility services support original RuneLite plugin injection, lifecycle, events, client-thread work, configuration, overlays, panels and renderer callbacks. Semantic adapters are separate from generic plugin hosting.

Supported adapters export immutable neutral guidance for Quest Helper, official Flipping Copilot and GOTR Helper. Scripts do not retain implementation objects; export currentness checks prevent an old recommendation or step from authorizing a new action.

## Public API

The public bot API and provider contracts compile without RuneLite on their classpath. RuneLite-specific entity resolution, collision, input and plugin internals remain in the runtime provider. Bot helpers and scripts depend on the neutral contracts.

Navigation combines local reachability with cross-scene routing. Coordinated banking examines reasonable banks and alternate usable approach positions, choosing by reachable route cost. Unseen global routes require matching static world data; this repository contains no such data.

## Managed updates

Pristine upstream RuneLite is an independently updateable dependency. The host is compiled against an exact selected runtime artifact, then checked for compatibility and plugin lifecycle/linkage. Candidates are verified before explicit acceptance, and a previous known-good runtime is retained for rollback.

The development launcher refreshes changed API, host, helper and script sources while removing stale script outputs. This is implemented workflow documentation; source code and build tools are not supplied here.

[Feature overview](../FEATURES.md) · [Plugin compatibility](PLUGINS.md) · [Project status](PROJECT-STATUS.md)
