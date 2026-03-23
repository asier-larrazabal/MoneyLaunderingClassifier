# MoneyLaunderingClassifier

## Project Overview

This repository contains an end-to-end Anti-Money Laundering (AML) machine learning project built around the IBM AML synthetic transaction dataset.

The project is organized as a 3-notebook pipeline:

1. `00_data_check.ipynb`
	Downloads and validates the raw datasets, then performs initial inspection.
2. `01_patterns_into_multiclass.ipynb`
	Parses laundering patterns and builds a multiclass target (`target_multi`) by merging pattern data into the transaction table.
3. `02_deepAnalysis.ipynb`
	Performs feature engineering, memory optimization, class-imbalance mitigation (undersampling + SMOTE), Optuna hyperparameter tuning, model comparison, and final evaluation.

## Repository Structure

- `data/HI-Medium_Trans.csv`: Main transaction dataset.
- `data/HI-Medium_Patterns.txt`: Laundering pattern definitions.
- `data/ibm_aml_multiclass_clases.csv`: Integrated multiclass dataset used for modeling.
- `requirements.txt`: Full Python dependency list.

## Environment Setup

Create and activate a virtual environment, then install dependencies from `requirements.txt`.

### Windows (PowerShell)

```bash
python -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (CMD)

```bash
python -m venv .venv
.venv\Scripts\activate.bat
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### macOS / Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## How To Run

1. Open the project in VS Code.
2. Select the `.venv` Python interpreter.
3. Run notebooks in order:
	1. `00_data_check.ipynb`
	2. `01_patterns_into_multiclass.ipynb`
	3. `02_deepAnalysis.ipynb`

## Main Goal

Detect rare laundering topologies in highly imbalanced transactional data using robust preprocessing, resampling, and ensemble learning strategies optimized for macro-level class performance.