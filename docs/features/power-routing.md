# Power, storage and sorting

## Flux

The Cinder Dynamo burns charcoal. Flux Rails carry power across configured face connections to machines and Reservoirs. At shipped defaults a Standard Dynamo produces 100 Flux per 0.1-second step, a Standard machine stores 20,000 Flux and a Standard Reservoir stores 200,000.

Reservoirs store and redistribute existing energy. Pausing stops their active transfers. A machine waiting for power keeps its paid work. World-axis port settings remain meaningful when the model is rotated; inspect the visible sockets and configured faces if a connection is missing.

## Plain-material storage

Supply Crates hold supported plain production materials, including catalog ingredients/results. They refuse customized or worn stacks that cannot be represented without losing their state. Charged Flux Packs are refused; plain empty packs can be stored.

The Storage page shows existing materials. Use **Deposit** for a new material kind and **Refresh** to repack the display. This changes the presentation rather than creating items. Clear contents, modules and energy through their appropriate controls before attempting machine removal.

## Filters and dispatch

Configure the source's faces and Auto output. Higher-priority eligible destinations are considered before lower-priority ones. The current filter slice supports up to **eight exact-ID or item-prefix rules**, in Allow or Deny mode. Choose the new-rule mode, hold the relevant item, then add it. A prefix such as `Ore_*` groups matching ore IDs. This is an ID-prefix rule, not a promise of every stock tag or external provider.

[![Native Supply Crate configuration with Ore prefix allow rule, priority, Auto output and dispatch controls](../assets/screenshots/sorting-controls.png)](../assets/screenshots/sorting-controls.png)

*The paused source allows the `Ore_*` prefix, sends one item per transfer and uses coordinate order for equal-priority destinations.*

Equal-priority dispatch can use saved round robin or coordinate order. **Send: 1** limits each successful transfer to one item. A Crate can be locked to a held material; incompatible contents and invalid lock changes refuse. Filters, priorities and locks do not bypass ownership, loaded-area or complete-output constraints.

Vanilla chests, third-party inventories and full bin/filter parity are not established provider support. Real second-client contention and production multiplayer performance remain open.
