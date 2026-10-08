# Feature overview

The following describes the implemented project. This repository distributes documentation and four host-interface captures, not application code or binaries.

| Feature | Verified scope / boundary |
| --- | --- |
| Standalone host | Own Swing/AWT application and canvas; consumes an independently supplied RuneLite/game runtime without opening the normal RuneLite shell |
| Windows packaging | Portable EXE, bundled Temurin Java and first-run GUI tested outside development repositories; installer not implemented |
| Rendering | Original GPU and 117 HD: real OpenGL 4.6 context on NVIDIA RTX 3060 Ti, renderer DrawCallbacks ownership and native frame capture; HD resize and return to software verified |
| Plugin lifecycle | 133/134 startup/shutdown checks at LOGIN_SCREEN; four original external plugin implementations hosted. Configuration/Plugin Hub UI unsupported |
| Preferences | Persistent enable/configuration settings; a fresh portable-client restart restored Notes and a test setting |
| Public API | Neutral API/provider contracts; entity/item/widget queries, inventory, equipment, banking, dialogue, skills, varbits/varps, traversal and world switching |
| Navigation | Local collision reachability, cross-scene traversal and reachable-bank selection by route cost with alternate approach tiles. Fresh global routes need a matching static world dataset |
| Bot Hub | 12 script/example classes discovered in the clean portable client; explicit controls and configurable settings, no automatic execution |
| Updates | Pristine upstream dependency, exact-artifact builds, compatibility checks and previous-runtime rollback |

## Script evidence

| Script | Implementation / live evidence |
| --- | --- |
| GotrBot | Multiplayer contribution and reactive recovery; full unattended games confirmed |
| EclipseWineBot | Collection/hops and full inventory → two ladders → bank → return → resumed collection verified |
| AgilityBot | Ordered object/action queries, generic reachability, mixed input and bounded progress waits; repeated Draynor laps verified. Other course settings do not imply equal certification |
| RunecraftingBot | Simple air altar/pure essence/talisman/bank loop |
| FightingBot | Combat/loot flow and generic banking integration; historical API/navigation testing |
| MiningBot / WoodcuttingBot | Configurable gathering, banking and return traversal; tool/account/route prerequisites |
| QuestHelperBot | Resolved guidance and dialogue; limited traversal and safe NPC/object execution. Unsupported or ambiguous steps stop |
| FlippingGuidanceLogger | Official Copilot recommendation changes; read-only, without GE execution |
| API/example scripts | Diagnostic and instructional scripts, not comprehensive unattended products |

GOTR's measured results and their limitations are described in [GOTR.md](docs/GOTR.md). [Project status](docs/PROJECT-STATUS.md) distinguishes implemented functionality from public availability.
