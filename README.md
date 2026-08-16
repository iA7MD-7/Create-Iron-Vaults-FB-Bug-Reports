# Create: Iron Vaults

**Create: Iron Vaults** extends Create's Item Vault with a full set of material tiers, in the spirit of Iron Chests and Sophisticated Storage. Every tier is a real Create vault: it forms the same multiblocks, feeds the same Packagers and logistics, mounts on contraptions, and keeps its connected textures.

## Tiers

Seven tiers above Create's Basic vault: Copper, Iron, Gold, Diamond, Emerald, Obsidian and Netherite.

| Tier | Slots per block | Items per stack | Total vs. Basic |
|---|---|---|---|
| Basic (Create) | 20 | 64 | 1x |
| Copper | 30 | 72 | 1.7x |
| Iron | 45 | 80 | 2.8x |
| Gold | 60 | 88 | 4.1x |
| Diamond | 80 | 96 | 6x |
| Emerald | 100 | 99 | 7.7x |
| Obsidian | 125 | 99 | 9.7x |
| Netherite | 160 | 99 | 12.4x |

Capacity grows on two axes: more slots per block, and deeper stacks in each slot. A single Netherite vault block holds 15,840 items, and a full 3x3x9 structure holds over 1.28 million. Both axes are configurable per tier, in game, from the Mods screen — and changing them resizes vaults that already exist rather than only new ones.

## Two ways to upgrade

**At a crafting table.** Put the vault in the centre, six of the tier's material down the sides, and its block form above and below. Each rung steps up one tier.

**With an upgrade item.** Sneak-right-click a vault and the entire connected structure converts at once, with its contents intact. Upgrade items are a reusable key rather than a consumable: they are checked and kept, and you need one per vault block in the structure.

There are two families of upgrade item. **Basic to Tier** upgrades take a plain, un-tiered vault straight to their tier in one jump. **Step** upgrades — Copper to Iron, Iron to Gold, and so on — take the tier directly below them, and are the cheaper route. Each upgrade works on exactly one source tier, so there is no way to skip rungs you have already climbed. Both families are crafted progressively, so each chain has to be walked in order.

Upgrading always preserves what kind of vault it is. Type, orientation and colour all survive; only the material changes.

## Create: Vibrant Vaults support

With Vibrant Vaults installed, every one of its vault kinds gets the full tier ladder: Item Vaults, Shipping Containers and Basic Shipping Containers, in both horizontal and vertical orientations, across all 17 colours. That is 714 blocks in total.

A dyed vault always keeps its paint through an upgrade. Item Vaults show their tier in the metalwork — the material replaces Create's grey trim ramp, so a blue vault stays blue and gains copper metal. Shipping Containers are painted panels with no grey to take over, so they show their tier as small corner studs instead.

Without Vibrant Vaults, only the plain Item Vault tiers are registered, and the rest are not loaded at all.

## Create: Connected support

With Create: Connected installed, its Item Silo gets the same seven tiers. Tier silos form the same multiblocks, share one inventory, keep their connected textures, take the same sneak-right-click upgrade, and support the click-the-top-face trick that fills a whole 3x3 cross-section in one go. Capacity per block matches the equivalent vault tier.

## Performance

Create refreshes a vault's comparators on every single slot change, and each refresh walks the entire multiblock. Filling a large vault therefore costs dozens of full structure walks per tick. This mod collapses that to at most one per tick, which applies to Create's own vaults and other addons' vaults as well as its own. It can be turned off in the config.

Jade's item readout is also served directly rather than through its generic collector, so vault and silo contents appear immediately instead of being counted up over several ticks.

The mod ships no copies of vault art. Every tier texture is built by the game while the block atlas is stitched, from the un-tiered block's own sprite plus a small tier overlay, which keeps the download under 2 MB. A side effect is that resource packs retexturing Create's or Vibrant Vaults' vaults automatically retexture the tier versions to match.

## In-game guides

Every upgrade item has its own Ponder scene showing that exact tier transition on a full 3x3x3 vault. Press W while hovering an item, or find them gathered under the "Vault Upgrades" entry in the Ponder index.

## Requirements

- Minecraft 1.21.1, NeoForge
- Create 6.0.10 or newer
- Create: Vibrant Vaults (optional) — adds the container, vertical and coloured tiers
- Create: Connected (optional) — adds the Item Silo tiers
- Jade (optional) — fast vault contents readout
