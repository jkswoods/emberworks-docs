# Configuration

The server creates its Emberworks properties in the plugin data directory. The shipped development source also defines the defaults below. Restart before relying on a configuration change.

| Setting | Default | Meaning |
|---|---:|---|
| `generator.fluxPerStep` | 100 | Flux generated per 0.1-second loaded work step |
| `generator.fluxPerCharcoal` | 20,000 | Flux supplied by one charcoal |
| `machine.fluxCapacity` | 20,000 | Base machine storage, scaled by worker lanes |
| `cell.fluxCapacity` | 200,000 | Base Reservoir storage, scaled by tier |
| `network.fluxPerStep` | 1,000 | Base source transfer budget per work step |
| `scheduler.jobsPerStep` | 256 | Bounded production scheduler work |
| `network.visitLimit` | 4,096 | Bounded route visits |
| `world.maxNodes` | 20,000 | Saved factory node limit |

Recipe work and Flux settings use `recipe.<recipe-id>.work` and `recipe.<recipe-id>.fluxPerWork`. The [catalog data](assets/data/catalog.json) lists the authored IDs and default quantities/times.

Existing saves retain their saved balance and recipe contracts. Editing the server properties does **not** silently rewrite a paid batch. Catalog adoption/migration is a separate deliberate operation; back up the paired save/JAR before a maintainer applies it. Reduced limits that cannot retain contents must refuse rather than truncate them.

Treat high limits as configuration bounds, not a production performance guarantee. The development target is a steady 33.3ms world tick; production and multiplayer performance acceptance remain open.
