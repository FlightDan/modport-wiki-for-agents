# Migration research worksheet

Use this worksheet to organize one generic finding for one exact source-to-target version pair. It is a drafting aid, not the published contribution format. The contribution submitted to this repository must be JSON and must follow [CONTRIBUTING.md](../CONTRIBUTING.md).

Do not fill this worksheet with private project or Run evidence. Do not claim project migration acceptance. This repository currently has no reviewed findings; this blank worksheet makes no research claim.

## Contribution identity

- Kind: platform or java
- Contribution UUID: assign one canonical UUID when preparing the JSON file; use the same value in its filename and id.
- Source version:
  - platform: Minecraft version, loader name, loader version
  - java: Java version
- Target version:
  - platform: Minecraft version, loader name, loader version
  - java: Java version

Use the same identity shape for source and target. Do not omit fields or combine findings from different version pairs.

## Entry

Repeat this section for each independent finding. The published JSON entry must contain all eight fields below and no extra fields.

- Stable entry id:
- Category:
- Summary:
- Applicability:
- Migration guidance:
- Compatibility:
- Verification and remaining uncertainty:

## Evidence

Add one or more source references for each entry. Every reference must contain all three values:

- Public HTTP(S) source:
- Locator within the source, such as a section, symbol, or path:
- What statement the source supports:

Keep the type and scope of evidence clear:

- Source reading supports claims about cited code or documentation.
- Compilation supports only the stated compile scope.
- Runtime evidence supports only behavior actually executed.

Mark unclear behavior and applicability as uncertain. If evidence does not support a conclusion, do not present that conclusion as established.

## Publication checklist

- The source and target versions are explicit and match the finding.
- Every entry has stable ids and all required generic fields.
- Every evidence item points to a public HTTP(S) source and a useful locator.
- Source-reading, compilation, and runtime claims are kept distinct.
- Uncertainty and limitations are stated.
- No project or Run acceptance claim, private record, local path, artifact, credential, or extra schema field is included.
