# Platform migration knowledge

Platform contributions describe an exact Minecraft and loader version pair. In both the source and target objects, include exactly these string fields:

- minecraft
- loader
- loader_version

Use the literal loader name and version for the corresponding side of the migration. Do not treat a Minecraft version alone as a complete platform identity.

The root [index](../index.json) points to each contribution JSON file. A contribution under contributions/platform/ contains one or more generic entries with applicability, migration, compatibility, verification, and public evidence references. Follow the root [contribution guide](../CONTRIBUTING.md) when adding or using a finding.

There are no reviewed platform findings in the initial index. This page documents the data organization; it does not assert that any platform migration has been researched, compiled, or run.
