# Processing machines

All recipes below use finite item counts and Flux. The [full catalog](../recipes.md) gives exact defaults. Auto processes eligible recipes; selecting a recipe pins new batches while already-paid batches keep their original choice.

| Machine | Current work |
|---|---|
| Stamp Mill / Arrays | Ten supported metal ores → two grit; Void crystal → Void grit |
| Arc Hearth / Arrays | Grit → bars, direct ore smelting and audited native stone/sand conversions |
| Impact Grinder / Arrays | Gravel/sandstone conversions and Yellow crystal → Lumen grit |
| Timber Splitter / Arrays | 27 supported trunk IDs → two mapped planks plus one guaranteed tree bark |
| Aggregate Press / Arrays | Gravel plus plain/red/white sand → matching aggregate |

[![Native Mill recipe selector, native inventory grids and paused parallel lanes](../assets/screenshots/mill-controls.png)](../assets/screenshots/mill-controls.png)

*Auto is selected. Output space and Flux are still required for every lane. The pictured machine is Resonant; its nine lanes are distinct saved batches.*

Timber's current secondary bark is guaranteed. The completion transaction requires room for all outputs; it waits rather than dropping bark or rerolling a paid result on reload. The wider indexed compatibility/probabilistic catalog remains outside the implemented subset.

Direct ore smelting gives one bar. The Mill → Hearth chain gives two bars per supported ore. Native zero-time stone conversions have one bounded work step; sand/clay and ore recipes have their own saved times. Do not assume every native Furnace recipe or conditional external-mod recipe is present.
