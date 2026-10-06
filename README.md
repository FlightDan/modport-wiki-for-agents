# ModPort Wiki for Agents

Version-specific migration knowledge for ModPort research and coding agents.

[简体中文](README.zh-CN.md)

This repository stores portable findings for explicit source-to-target version pairs. It is designed as optional research material; an entry describes cited evidence and migration guidance, not acceptance of a particular project or Run.

## Start here

The root [index.json](index.json) lists the available contributions. Its first reviewed finding covers Java 17 → 25 and preserving empty-list exceptions when choosing between `List.get(0)` and `List.getFirst()`. It cites the version-specific Oracle API documentation; custom implementations and project runtime behavior remain unverified.

Online ModPort readers can run `modport wiki update`. For offline use, download `research-v0.1.0.zip` from the [research-v0.1.0 release](https://github.com/FlightDan/modport-wiki-for-agents/releases/tag/research-v0.1.0), then run `modport wiki import-pack --file /path/to/research-v0.1.0.zip`. These commands require the current ModPort source containing the Wiki integration; that application integration is not yet a released ModPort version.

You can read the indexed JSON directly. The command examples are for maintainers and users with access to the current ModPort source; obtain that source and its installation instructions from its maintainer. This research repository distributes knowledge packages.

Each index row identifies a contribution by ID, kind, source version, target version, and file path. Read the linked JSON file for its entries and evidence.

| Kind | Source and target version fields |
| --- | --- |
| platform | minecraft, loader, loader_version |
| java | java |

Version values describe the scope of a contribution. They do not by themselves show that every feature or environment in those versions was checked.

## How to read an entry

Each entry has an ID, category, summary, applicability, migration guidance, compatibility notes, verification guidance, and evidence references. Each evidence reference gives a public HTTP(S) source, a locator within that source, and the statement it supports.

Keep the evidence type clear. Reading source or documentation supports claims about those sources. A compile result supports only the stated compilation scope. Runtime evidence supports only behavior actually exercised. Record uncertainty directly in the entry, and do not turn a limited finding into a project migration or acceptance claim.

## Contributing

Use [CONTRIBUTING.md](CONTRIBUTING.md) and the [research worksheet](templates/research.md) to prepare a portable contribution. Contributions are JSON files under contributions/platform/ or contributions/java/; maintainers review and promote accepted material into the versioned index and research package.

The current local ModPort integration prepares editable drafts and supports GitHub CLI browser login and explicitly submitted Draft Pull Requests through the displayed account's fork and branch (the upstream owner uses an owned branch). Actual browser authorization and owner-account Draft PR creation were verified with [contribution #1](https://github.com/FlightDan/modport-wiki-for-agents/pull/1); repeating submission returned the same PR. External contributor fork routing, real model research and native Windows behavior remain unverified. This application integration is not yet released.

Maintainers promote reviewed files with the local `modport wiki build-pack` command described in [CONTRIBUTING.md](CONTRIBUTING.md). Online readers use the versioned index at the release revision; offline readers can import the release ZIP with `modport wiki import-pack --file FILE`.

## License and reuse

This documentation draft does not set license terms. Consult the repository's published licensing information and its maintainers before reusing or redistributing contributions. If the repository has no published license, reuse permission remains unresolved.

Last reviewed: 2026-10-07.
