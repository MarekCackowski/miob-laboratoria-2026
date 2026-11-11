# Laboratory 1 — Agent Workflow Basics

GitHub Repository: https://github.com/MarekCackowski/miob-laboratoria-2026

## Diagnostic Information

- Application: VS Code with Copilot SDK
- Model: `auto` (model selected automatically by the application)
- Reasoning level: not set manually

## Objective and Execution

The prepared program `describe_data.py` was run on the `data/exercise.csv` file, saving the report to `results/exercise-summary.json`.
The program reads CSV records, counts `ham` and `spam` labels, and then saves a JSON report with information about the input, runtime environment, and label totals. No model was trained.

## Result

- total messages: **8**
- `ham`: **5**
- `spam`: **3**
- interpreter: Python 3.12.3

The attached `exercise-summary.json` file is the execution report.

## Verification

Run:

```text
python3 -m unittest discover -s tests -v
```

Result: **1 test, OK**. The test uses three synthetic messages and verifies the correct saving of the report as well as the counts of 3 / 2 / 1. This does not replace the verification of the report from `data/exercise.csv`, which was checked separately.

## Session Log

The full work log is located in `sesje/sesja-1.jsonl`.
