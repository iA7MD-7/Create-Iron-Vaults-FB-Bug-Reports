# Create: Iron Vaults

**Create: Iron Vaults** extends Create's Item Vault with a full set of material tiers, in the spirit of Iron Chests and Sophisticated Storage. Every tier is a real Create vault: it forms the same multiblocks, feeds the same Packagers and logistics, mounts on contraptions, and keeps its connected textures.

## Tiers

Seven tiers above Create's Basic vault: Copper, Iron, Gold, Diamond, Emerald, Obsidian and Netherite.

| Tier | Slots per block | Items per stack | Total vs. Basic |
|---|---|---|---|
| Basic (Create) | 20 | 64 | 1x |
| Copper | 24 | 64 | 1.2x |
| Iron | 28 | 72 | 1.6x |
| Gold | 32 | 80 | 2.0x |
| Diamond | 36 | 88 | 2.5x |
| Emerald | 40 | 96 | 3.0x |
| Obsidian | 44 | 99 | 3.4x |
| Netherite | 48 | 99 | 3.7x |

Capacity grows on two axes on purpose. Slot count is what every inventory scan in the game has to walk, so most of the growth is in stack depth instead, which costs nothing to iterate. Both are configurable per tier.

## Two ways to upgrade

**At a crafting table.** Put the vault in the centre, six of the tier's material down the sides, and its block form above and below. Each rung steps up one tier.

**With an upgrade item.** Sneak-right-click a vault and the entire connected structure converts at once, with its contents intact. Upgrade items are a reusable key rather than a consumable: they are checked and kept, and you need one per vault block in the structure.

There are two families of upgrade item. **Basic to Tier** upgrades take any vault below their tier straight to it. **Step** upgrades — Copper to Iron, Iron to Gold, and so on — only work on the tier directly below them, and are the cheaper route. Both are crafted progressively, so each chain has to be walked in order.

Upgrading always preserves what kind of vault it is. Type, orientation and colour all survive; only the material changes.

## Create: Vibrant Vaults support

With Vibrant Vaults installed, every one of its vault kinds gets the full tier ladder: Item Vaults, Shipping Containers and Basic Shipping Containers, in both horizontal and vertical orientations, across all 17 colours. That is 714 blocks in total.

A dyed vault keeps its paint through an upgrade and shows its tier as small corner studs instead of being repainted, so a blue container stays blue and simply gains copper corners.

Without Vibrant Vaults, only the plain Item Vault tiers are registered, and the rest are not loaded at all.

## Performance

Create refreshes a vault's comparators on every single slot change, and each refresh walks the entire multiblock. Filling a large vault therefore costs dozens of full structure walks per tick. This mod collapses that to at most one per tick, which applies to Create's own vaults and other addons' vaults as well as its own. It can be turned off in the config.

Jade's item readout is also served directly rather than through its generic collector, so vault contents appear immediately instead of being counted up over several ticks.

## In-game guides

Every upgrade item has its own Ponder scene showing that exact tier transition on a full 3x3x3 vault. Press W while hovering an item, or find them gathered under the "Vault Upgrades" entry in the Ponder index.

## Requirements

- Minecraft 1.21.1, NeoForge
- Create 6.0.10 or newer
- Create: Vibrant Vaults (optional) — adds the container, vertical and coloured tiers
- Jade (optional) — fast vault contents readout
