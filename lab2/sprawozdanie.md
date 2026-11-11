# Laboratory 2 — ML Experiment Plan

GitHub Repository: https://github.com/MarekCackowski/miob-laboratoria-2026

## Diagnostic Information

- Application: VS Code with Copilot SDK
- Model: `auto` (model selected automatically by the application)
- Reasoning level: not set manually

## Experiment Plan

A fixed model was trained on `data/train.csv`, and then predictions were generated for the previously unseen `data/validation.csv`. Evaluation was performed in a separate step by joining predictions with reference labels by ID.
Hyperparameters and data were not changed.

The model is `StandardScaler + LogisticRegression` with `C = 0.01`,
six numerical features, and a threshold of `0.5`. The label, ID, and full text
of the message were not used as features.

## Validation Result

- validation messages: **60**
- true positives (`tp`): **6**
- true negatives (`tn`): **40**
- false positives (`fp`): **0**
- false negatives (`fn`): **14**
- total errors: **14**

The `metrics.json` file contains the saved metrics, and `predictions.csv` contains the predictions.

## Verification

The experiment checker returned:

```text
PASS: artifacts support evaluation of the fixed model on the supplied held-out messages.
```

Unit tests: **3 tests, OK**.

## Session Log

The full work log is located in `sesje/sesja-1.jsonl`.
