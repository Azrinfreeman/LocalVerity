# Local Verity

A Forge Minecraft modpack maintained with packwiz, centred on a Verity build distributed through this repository's releases. The repository contains pack metadata, a Verity configuration, dependency references, and two bundled library JARs; it does not contain the Verity mod's source code.

## Recorded versions

| Component | Manifest value |
| --- | --- |
| Pack | Local Verity 1.0.0 |
| Minecraft | 1.20.1 |
| Forge | 47.4.26 |
| Pack format | packwiz:1.1.0 |

See [pack.toml](pack.toml) and [index.toml](index.toml). Version declarations describe this revision; launch compatibility is untested in this review.

## Pack contents

The index lists seven files: three mod metadata files, two directly bundled JARs, the Verity configuration, and `servers.dat`. Metadata references [Carry On](mods/carry-on.pw.toml), [Geckolib](mods/geckolib.pw.toml), and [Verity JE Gemini Fix](mods/verity-je-gemini-fix.pw.toml). The bundled libraries are Cloth Config and YetAnotherConfigLib. The Verity download is pinned to the repository's `fix` release and includes a SHA-256 hash.

## Setup

1. Create a separate launcher instance for the recorded Minecraft/Forge versions, with a compatible Java runtime.
2. Follow the official [packwiz-installer guide](https://packwiz.infra.link/tutorials/installing/packwiz-installer/) using an owner-confirmed hosted `pack.toml` URL. No working hosted endpoint or launcher bundle was verified here.
3. Review [verity-common.toml](config/verity-common.toml) locally before playing. It selects Gemini for AI, Kokoro for text-to-speech, and native speech-to-text. API-key fields are empty; any required provider credentials and service setup must be supplied locally and kept out of Git.
4. Verify the configured model and provider endpoints against the mod's supported configuration. A model name in this file does not prove availability or compatibility.
5. Test in a fresh instance and back up worlds before using an existing installation. Review the bundled server list before distributing a customized pack.

For pack changes, use the official [packwiz maintenance workflow](https://packwiz.infra.link/tutorials/creating/getting-started/) and refresh the index and manifest hashes together. The current index marks `servers.dat` with `preserve = true`; check update behaviour before assuming it replaces an existing server list.

## Status and attribution

See [validation notes](docs/VALIDATION.md) for metadata checks and remaining work. Minecraft, Forge, and included mods retain their respective terms. Verify redistribution rights for the bundled libraries and release JAR; this documentation adds no licence over those components.
