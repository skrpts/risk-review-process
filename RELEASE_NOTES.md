# Release Notes

## v1.1.27
GH#863 (Wave 2) — wire the never-invoked `risk-register-entry` so the register is actually produced. The bundle shipped a `risk-register-entry` prompt ("Creates a structured risk register entry") and the docs described a register-creation stage, but the `execution:` block only ran `assess-risk → language-polish` — so the pipeline output a polished risk *assessment*, not the risk *register* that is the deliverable of a risk-review process (K-045 intent/output mismatch). Restored the intended graph: inserted a **Risk Register Entry** step (backed by the new `risk-register-builder` skill so it is `from_step`-addressable) between the assessment and the polish, ordered `assess-risk → risk-register-entry → language-polish`, and converted the register prompt's positional `{{steps.Risk Assessment.output}}` ref to an explicit `from_step` binding (`{{step.context.risk_assessment}}` ← Assess Risk). Also completed the tail: repinned `polish-language` 1.0.1→1.0.6 (the version exposing the bindable `source` slot) and bound `language-polish`'s `source` ← the Risk Register Entry, so the `output_step` polishes the register rather than its positional previous — correct end-to-end. No new required inputs.

## v1.1.26
GH#845 — republish with American English (en-US) content, completing the source-only GH#805 flip that never reached the Hub. Copy only — no functional or behaviour change.

## v1.1.25
GH#745 — declare per-step `output: {name, type}` on every execution step (risk_assessment/text, polished_review/text). Lights up the #744 rich flow-map. Content-only; no bindings or logic changes.

## v1.1.24
GH#645 Row 3b — migrate to K-037 dep-referenced schema. Strip 7 inline shared-content files and declare 7 hub-shared deps (UUID id + slug name + version + checksum from `gen-dep-checksums.mjs`). Closes pre-Step-3 inline-vendoring for this bundle.

## v1.1.23
Wave 2: re-signed with canonical engine signing pipeline.

## v1.1.22
Tags migrated inline into manifest (GH#586). tags.yaml retired.

## v1.1.21
Bundle re-signed with canonical engine signing pipeline (Wave 2 migration).

## v1.1.20
Signature fix — RELEASE_NOTES.md now included in integrity checksum.

## v1.1.19
Initial catalog release with full structural and content-quality validation. All scanner checks pass.
