# Package provenance

This is the companion repository for *Auditing Tail-Risk Warning and Bayesian Portfolio Allocation with Financial-Semantic Controls* (unpublished). It is a new repository for a revised article from the same DeepFirm-Quant research project, not a claim of a separate independent study.

## Imported baseline

- Source repository: https://github.com/Elvin-Chow/deepfirm-quant-reproducibility
- Evaluation baseline: `v1.0.0`, commit `bbfc627671c5b52663947847dcdf35029bc14d2c`.
- Imported tracked snapshot: commit `694cb1bc1db5811079b5790824268d0475d4aada`, which adds the isolated audit harness to that baseline.
- The 151-file source snapshot was exported without its Git history, untracked files, caches, local environments, or research-working-directory contents.
- The MIT license and attribution are retained. Scientific code, fixed inputs, model bundles, protocols, and frozen evaluation result bytes are unchanged. Only repository identity, citation, runbook context, and the audit README hash were adjusted; this provenance document was added.

## Two code contexts

Root-level `models/` and `data_pipeline/` reproduce the released evaluation package. The audit imports its exact tested implementation from `audits/mathematics_2026_09_23/snapshot/`. Some module versions differ; merging those directories would change the evidence identity. The audit manifest records its 26 Python dependencies and four fixed inputs.

The original audit record reports 5/5 designed faults detected and 5/5 matched normal controls passed in 5.827 ms. The separately archived migrated replay reports the same outcomes in 8.133 ms. Both are author-executed case-function timings, excluding interpreter startup/imports. The full original and replay evidence accompanies the manuscript in `Audit_Validation_Artifacts.zip`. Creating this repository did not rerun these cases or the market evaluation.

## Version identity

The old repository retains its own history and `v1.0.0` tag. Software version 1.0.0 here identifies this separate package; no shared commit/tag identity, new publication, archival DOI, or independent reproduction is implied.
