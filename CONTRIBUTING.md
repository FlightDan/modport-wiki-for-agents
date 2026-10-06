# Contributing

Contribute small, evidence-based migration findings that apply to an explicit source and target version pair. The public Wiki is for portable knowledge. It is not a place to publish a project's private migration record or claim that a ModPort Run passed acceptance.

## Prepare the version pair

Each contribution file is JSON at contributions/{kind}/{uuid}.json. Its id is a canonical UUID and must match both the filename and the corresponding index row.

Use one of these exact identity shapes for both source and target:

- For kind platform: minecraft, loader, and loader_version.
- For kind java: java.

Use the exact versions and loader involved in the finding. Do not combine observations from different pairs into one contribution.

## Write portable entries

The contribution has schema_version 1, id, kind, source, target, and a non-empty entries array. Each entry must have exactly these fields:

- id: a stable lowercase identifier unique within the contribution.
- category: the general topic.
- summary: the finding in a concise statement.
- applicability: the versions, APIs, or conditions where it applies.
- migration: the change or decision supported by the finding.
- compat: relevant compatibility behavior or constraints.
- verification: what was checked, how, and what remains unknown.
- evidence: one or more source references.

Each evidence reference has exactly source, locator, and supports. Use a public HTTP(S) URL, identify the relevant section or symbol in locator, and state which part of the entry that source supports. Prefer official version-specific documentation, source, specifications, or release notes. Do not cite a home page when a precise source location is available.

Use the entry text to distinguish source reading, compilation, and runtime evidence. Source reading does not prove compiled or runtime behavior. Compilation does not prove runtime behavior. Runtime evidence must name the behavior and scope actually exercised. State uncertainty directly, including where evidence is incomplete or sources disagree.

The portable schema has no fields for project identity, Run identity, artifact paths, execution results, or acceptance status. Do not add custom fields. Do not include private logs, local paths, credentials, private source material, target artifacts, or claims that a specific project or Run passed migration acceptance. Keep sensitive or project-specific evidence in the private ModPort Run record.

## Review and promotion

Submit the contribution JSON for maintainer review. Contributors should not edit index.json; maintainers add reviewed material to the versioned index and research package when they promote it. Merging a file alone does not mean it has been promoted into a package.

The current local ModPort integration produces editable drafts, supports GitHub CLI browser login, and can submit a Draft Pull Request using the displayed account's fork and branch (an upstream owner uses an owned branch). Submission is an explicit user action. Local host/browser tests passed; live authentication, Draft PR creation and native Windows behavior remain unverified, and this integration is not yet released. A normal pull request using this format remains available.

Maintainers can use `modport wiki build-pack --library /path/to/checkout --revision research-v0.1.0 --output /path/to/research-v0.1.0.zip --index-output /path/to/checkout/index.json` to build a catalogue and portable ZIP. This indexes every research JSON file under `contributions/`, `platform/` and `java/`; use a checkout containing only reviewed material selected for promotion, and inspect the generated index before committing/tagging it. Attach the ZIP to the matching release. Building does not publish. New online Runs resolve the release tag and indexed files; offline users run `modport wiki import-pack --file /path/to/research-v0.1.0.zip`. Import selects the local cache; online Runs still attempt remote retrieval first and use that cache when retrieval is unavailable or host network tools are disabled.

## Licensing

This contribution guide does not establish license terms. Follow the repository's published license and contribution policy when available. If none is published, ask the maintainers about reuse terms before contributing material that requires a licensing grant.
