# DeepFirm-Quant Financial-Semantic Audit

Companion code and frozen evaluation artifacts for **Executable Financial-Semantic Audits for Tail-Risk Warning and Bayesian Portfolio Evaluation**.

**Author:** Hongyi Zhou. **Manuscript status:** Unpublished; prepared for submission to *Computational Economics*.

This is the single current repository for the manuscript's warning and allocation evaluation, reproducibility materials, and five-case financial-semantic audit. It includes executable code, fixed configurations and inputs, accepted/failed/legacy warning bundles, derived results, decision logs, result generators, and targeted tests. The companion supplementary archive `Audit_Validation_Artifacts.zip` preserves the original audit results, original runner, failed invocation notes, and a separate migrated replay.

The package supports offline inspection. It excludes manuscript submission files, provider price caches, local environments, and an executable path that repeats the frozen final evaluation. See [provenance](docs/provenance.md) for its relationship to the earlier DeepFirm-Quant repository.

## Repository and version history

| Version | Role |
|---|---|
| [Current package](https://github.com/Elvin-Chow/deepfirm-quant-financial-semantic-audit) | The evaluation, reproducibility materials, and audit used by the current unpublished manuscript. |
| [Original evaluation release](https://github.com/Elvin-Chow/deepfirm-quant-financial-semantic-audit/tree/v1.0.0) | The preserved `v1.0.0` baseline, before the audit harness was added. |
| [Earlier repository history](https://github.com/Elvin-Chow/deepfirm-quant-financial-semantic-audit/commit/0cf63fb74d377f784f6ada6f0cb0bb3c1b1c9218) | The original repository's complete history through its last local documentation update, retained in this repository's Git history. |

The manuscript belongs to the same DeepFirm-Quant research project as the earlier article versions. The earlier repository remains a historical source; current use and citations should point here. Consolidation preserves the scientific evidence and its limitations. See [provenance](docs/provenance.md) for the original titles, commits, and package relationship.

## Evidence boundary

The offline audit uses five designed faults and five matched normal controls. The archived original run detected all five faults and accepted all five controls (5.827 ms); a separately preserved migrated replay recorded the same outcomes (8.133 ms). These are case-function timings, excluding startup and imports. Three cases exercise existing guards; two use checks added to the audit harness. These ten inputs do not estimate field false-alarm/miss rates or demonstrate independent audit effectiveness. See the [audit README](audits/mathematics_2026_09_23/README.md) for the executable scope and archived-evidence boundary.

The primary result is a short security-disjoint and out-of-time evaluation across 10 portfolios in five markets. The accepted H1 artifact covers 522 portfolio-date rows and 50 tail events. It records average precision 0.1241, Brier score 0.0876, and recall 0.0800 at the calibration-selected threshold 0.100746. Recall is zero at the historical 0.60 reference. Gradient boosting records five-seed mean average precision 0.1291 and recall 0.1760, but no primary warning comparison survives Holm correction.

At the 12 basis point one-way cost, the guarded Smart allocation records net mean log return 0.001033 and net Information Ratio 0.8350. No parent component or Smart subcomponent comparison survives its specified correction. H5 fails its frozen validation gate and its final test remains unopened.

These files support identity, integrity, traceability, bounded executability, and inspection of the archived values. They do not establish predictive superiority, practical alarm utility, benchmark outperformance, alpha, causal component effects, deployment readiness, broad multi-market generalization, independent audit, or investment advice. The clean-environment reproduction was executed by the authoring workflow, not by an evaluator outside the author team.

## Quick start

Use Python 3.11 or later. The recorded environment used Python 3.13.9.

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements-lock.txt
```

Run the offline package check:

```bash
bash scripts/run_reproducibility_smoke.sh
```

Run all public tests:

```bash
python -m pytest -q
```

Regenerate the reader-facing tables and primary overview figure from archived result files:

```bash
python scripts/generate_tables.py
python scripts/generate_figures.py
```

These commands do not contact a market-data provider, train a model, tune a threshold, score a new snapshot, or repeat the frozen final evaluation.

## Package map

| Surface | Public path | Offline check |
|---|---|---|
| Resolved environment | `requirements-lock.txt`, `Dockerfile` | smoke inventory |
| Reproduction runbook | `docs/reproduction.md` | smoke inventory |
| Data and license boundary | `DATA.md` | policy test and trace scan |
| Warning artifacts | `artifacts/crisis_warning/` | artifact hash and schema checks |
| Fixed protocols | `configs/` | JSON/YAML schema and expected-value checks |
| Core method source | `models/`, `data_pipeline/` | unit tests |
| Frozen results | `results/frozen/` | `results/manifest.sha256` and value checks |
| Generated tables and figures | `results/generated/`, `results/figures/` | generator regression tests |
| Offline entry point | `scripts/run_reproducibility_smoke.sh` | direct execution |
| Public tests | `tests/` | `python -m pytest -q` |
| Five-case financial-semantic audit | [audits/mathematics_2026_09_23/](audits/mathematics_2026_09_23/README.md) | `python audits/mathematics_2026_09_23/run_injections.py` |

## Artifact status

- `artifacts/crisis_warning/accepted/global_h1/`: role-separated H1 bundle that passed the fixed validation gates.
- `artifacts/crisis_warning/failed/global_h5/`: role-separated H5 bundle that failed the ROC-AUC gate. Its final test is unopened.
- `artifacts/crisis_warning/legacy/global_h1/` and `global_h5/`: degraded legacy bundles retained as evidence, not accepted models.

Public metadata removes internal source paths and workflow labels. Model, calibration, and background-sample bytes are unchanged. Each role-separated metadata file records both the source bundle identity and the public release identity.

## Data availability

Provider price tables and local caches are not redistributed. `results/frozen/input_snapshot_identities.csv` records provider, date, row-count, and canonical frame identities without publishing the price frames. The row-level warning, allocation, cost, and decision files are transformed analytical outputs. See [DATA.md](DATA.md) for provider terms, live-refresh limits, and redistribution scope.

## Version and citation

The preserved [`v1.0.0` tag](https://github.com/Elvin-Chow/deepfirm-quant-financial-semantic-audit/tree/v1.0.0) points to the original evaluation baseline, commit `bbfc627671c5b52663947847dcdf35029bc14d2c`, and does not include the later audit harness. The current `main` branch contains the combined package and updated manuscript documentation. The original commit and tag identities are retained; consolidation does not create a new evaluation result or an archival DOI. See [CITATION.cff](CITATION.cff) for the current unpublished manuscript citation.

## License

Repository code is available under the MIT License. Third-party data remain subject to their providers' terms and are not sublicensed by this repository.
