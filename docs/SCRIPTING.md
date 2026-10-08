# Java scripting concepts

The implementation uses a neutral Java API and a looping bot base class. Scripts need no RuneLite imports or plugin implementation classes.

Each outer loop reads current state, chooses one useful action and returns a delay. Bounded, cancellation-aware condition waits allow an interaction to be followed by observable progress such as animation, movement, dialogue, inventory changes or fresh guidance. A dispatched click alone is not treated as completed work.

Typed queries support entity identity, names, actions, distance and reachability, with nearest-by-path selection. The same API covers items, inventory, equipment, banking, widgets, dialogue, skills, varbits, traversal and world switching. Missing/unavailable query data is distinct from a valid empty result.

Configuration metadata supplies settings and enum dropdowns in the Bot Hub. Discovery does not automatically start a script; users explicitly start and stop it.

Read-only typed plugin capabilities provide explicitly supported semantic state. Before acting on a plugin-derived decision, scripts check that the exported snapshot is still current. RuneLite/plugin-specific implementation remains in host adapters.

The original showcase's executable Java example is deliberately absent here: this is a documentation-only repository. [Architecture](ARCHITECTURE.md) · [Feature overview](../FEATURES.md)
