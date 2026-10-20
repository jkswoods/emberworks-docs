# Installation and compatibility

| Item | This guide |
|---|---|
| Mod | Emberworks 0.3.0-dev |
| Game | Hytale 0.7.2, pinned by the plugin manifest |
| Artifact | `Emberworks-0.3.0-dev.jar` |
| Java for building/running the server | Java 25 |
| Extra mod dependencies | None declared |
| Distribution | Development access only; no public release/download |

Use a separate disposable or backed-up test world. The current durable native adapter has been exercised in a controlled **Emberworks Integrity Lab** copy with the supported disk player storage. Water-world actions, Fluid Tank/Separator/Rotary bucket exchange, held-pack charging and Chemical Tank carrier exchange currently require that supported Lab adapter. Naming a new world the same way is not a substitute for its setup or acceptance. General world/provider support remains incomplete.

1. Obtain the development JAR from its maintainer. Do not infer a download from an unrelated similarly named mod.
2. Close the world/server. Back up its complete world, paired player data and installed Emberworks JAR together.
3. Put the JAR in Hytale's `UserData/Mods` directory, then enable Emberworks for the test world in the game's mod selection.
4. Open the supported test copy. Confirm the game and mod versions match before moving valued materials.

Do not replace one participant of a saved world/player pair by itself. If rolling back, restore the matched world, player data and JAR. **An older Emberworks build may not read a save written after portable equipment charging.** Retain the pre-upgrade pair rather than attempting a downgrade in place.

The earlier power, processing, water and equipment screenshots use this development build:

```text
2074c1f6c0dca40c005105e7ae5b342f6c7a01566999877271a3b28af3718e37
```

Never remove the mod from a valued save without a tested restore plan: the world contains Emberworks blocks, items and saved factory data. [Troubleshooting](troubleshooting.md) covers refused recovery and compatibility symptoms.


The [fluid-network page](features/fluid-networks.md) uses the later development build `6f5a4c8d7ccf193584d0cef7893deab66720be80dc99c61160ef482c8bc9c2bb`. Its fluid-network saves require the matching new build. Preserve the complete pre-upgrade world/player/JAR pair; older builds may not read the new fluid-port and buffer state.

The [chemical-network page](features/chemical-networks.md) uses development build `192a736b509f759421dd397cb9083386b185f720e3bd38bf85e1c40be0f49159`. Its chemical ports require the newer save format. The paid-batch and stocked-component trials used the preceding `6a3a7053a8efd0ecd4801d7ccba2deaeb07629145be964ce140ed3f6a0dcf94b` build; the newer build shortens the tank hint without changing the production or transfer protocol.

The [water-separation page](features/separation.md) uses development build `92353175376c118737e748fa90b767edef1e77f24718ee75ff5de28af68426d1`, following the native functional trial on `788f14d35fbbc415c545b91c9b3e47b89fd9faabec11b040926488dc5341c58b`. The newer build corrects native labels/status text; its simulation, durability, art and audio files are unchanged. Separator saves contain a newer format with the water contract and both chemical outputs. Preserve the complete earlier world/player/JAR pair for rollback.

The [Rotary guide](features/rotary.md) uses development build `6f33a62dcf008262b6cf712dd9c0a87f6c7875ae8397e586b98a52f8e8d13feb`. Its two stores, saved mode and additional phase identities require the newer save format. Retain the complete earlier world/player/JAR pair; do not attempt an in-place downgrade of a phase-conversion save.
