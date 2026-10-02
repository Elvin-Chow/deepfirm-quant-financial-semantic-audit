# Package provenance

This is the consolidated companion repository for *Executable Financial-Semantic Audits for Tail-Risk Warning and Bayesian Portfolio Evaluation* (unpublished; prepared for submission to *Computational Economics*). It contains the archived evaluation and the additional financial-semantic audit from the same DeepFirm-Quant research project.

Earlier manuscript titles include *Auditing Tail-Risk Warning and Bayesian Portfolio Allocation with Financial-Semantic Controls* and *An Auditable Explainable AI Framework for Multi-Market Tail-Risk Warning and Leakage-Guarded Bayesian Portfolio Allocation*. These identify earlier versions of the same study.

## Imported baseline

- Source repository: https://github.com/Elvin-Chow/deepfirm-quant-reproducibility
- Evaluation baseline: [`v1.0.0`](https://github.com/Elvin-Chow/deepfirm-quant-financial-semantic-audit/tree/v1.0.0), commit `bbfc627671c5b52663947847dcdf35029bc14d2c`.
- Imported tracked snapshot: commit `694cb1bc1db5811079b5790824268d0475d4aada`, which adds the isolated audit harness to that baseline.
- The 151-file source snapshot was exported without its Git history, untracked files, caches, local environments, or research-working-directory contents.
- The MIT license and attribution are retained. Scientific code, fixed inputs, model bundles, protocols, and frozen evaluation result bytes are unchanged. Only repository identity, citation, runbook context, and the audit README hash were adjusted; this provenance document was added.

## Repository consolidation: 2026-10-02

The earlier repository's complete four-commit history through `0cf63fb74d377f784f6ada6f0cb0bb3c1b1c9218` is retained as a merge parent in this repository. The original `v1.0.0` tag retains its exact commit target. Both repositories contained byte-identical scientific code, configurations, fixed inputs, model bundles, and evaluation results; the differences were repository documentation and identity metadata. Consolidation therefore keeps the current package tree and incorporates the earlier Git history without replacing scientific files.

Current citations and manuscript links use `https://github.com/Elvin-Chow/deepfirm-quant-financial-semantic-audit`. The earlier URL is retained as a historical migration entry. Manuscript titles, repository guidance, and the audit README's manifest entry are synchronized; the archived scientific evidence remains unchanged.

## Two code contexts

Root-level `models/` and `data_pipeline/` reproduce the released evaluation package. The audit imports its exact tested implementation from `audits/mathematics_2026_09_23/snapshot/`. Some module versions differ; merging those directories would change the evidence identity. The audit manifest records its 26 Python dependencies and four fixed inputs.

The original audit record reports 5/5 designed faults detected and 5/5 matched normal controls passed in 5.827 ms. The separately archived migrated replay reports the same outcomes in 8.133 ms. Both are author-executed case-function timings, excluding interpreter startup/imports. The full original and replay evidence accompanies the manuscript in `Audit_Validation_Artifacts.zip`. Creating this repository did not rerun these cases or the market evaluation.

## Version identity

This repository retains the earlier history and original `v1.0.0` evaluation tag alongside the current combined package. The baseline tag predates the audit harness; use the current `main` branch for the combined package. The historical `audits/mathematics_2026_09_23/` directory name records the audit's origin and is retained to preserve paths and evidence identity. Repository consolidation does not imply a new publication, archival DOI, experiment, or independent reproduction.
