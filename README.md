# DDR-MKSVM

Reproducible nonlinear SVM research for imbalanced tabular classification.
The repository contains an audited source-profile baseline, the supported
**RKHS-RBF-OVO SVM**, its **class-sensitive RKHS-RBF-OVO** extension, frozen
cross-dataset results, and a fully preserved negative robust-optimization
track.

The active workflow runs locally. Modal and other cloud-specific wrappers are
retained only under `archive/modal/` as historical provenance.

## Quick start

```powershell
py -3.12 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m pytest -q
python -m ddr_mksvm.cli smoke --dataset breast_cancer_recurrence --seed 17000 --run-name quickstart
```

Supported commands:

```powershell
python -m ddr_mksvm.cli --help
python -m ddr_mksvm.cli inventory
python -m ddr_mksvm.cli v7 --help
python -m ddr_mksvm.cli v8c --help
python -m ddr_mksvm.cli expanded --help
python -m ddr_mksvm.cli analyze --help
```

The legacy names `V7` and `V8-C` are retained in immutable code and result
paths only. Their manuscript names are RKHS-RBF-OVO SVM and CS-RKHS-RBF-OVO
SVM, respectively.

## Documentation

- Full installation, dataset, execution, resume, and reproduction guide:
  [`docs/PROJECT_SETUP_AND_EXECUTION.md`](docs/PROJECT_SETUP_AND_EXECUTION.md)
- Path migration map: [`docs/REPOSITORY_MIGRATION.md`](docs/REPOSITORY_MIGRATION.md)
- Refactor verification: [`docs/REPOSITORY_REFACTOR_REPORT.md`](docs/REPOSITORY_REFACTOR_REPORT.md)
- Architecture history: [`docs/ARCHITECTURE_HISTORY.md`](docs/ARCHITECTURE_HISTORY.md)
- Final manuscript: [`paper/final_manuscript/SVM_FINAL_PAPER.md`](paper/final_manuscript/SVM_FINAL_PAPER.md)
- Robust negative-result archive: [`docs/robust/README.md`](docs/robust/README.md)

## Scientific status

RKHS-RBF-OVO and CS-RKHS-RBF-OVO are the supported deterministic models. The
robust candidates are retained as controlled negative evidence and are not
active production architectures. Do not reuse reserved confirmation seeds
without defining a new prospective protocol first.
# robust-nonlinear-svm-reproducibility
Reproducibility package for robust nonlinear SVM experiments
