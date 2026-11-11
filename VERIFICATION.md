# Verification

Verified on November 11, 2026, using Python 3.13.9 in the project's `.venv`.
The notebook was executed from top to bottom on the CPU, including fresh
RoBERTa inference and the new-review demonstration. All 10 code cells completed
successfully, and the executed notebook was saved. The original backup notebook
was left unchanged.

Setup fixes:

- Installed `requirements.txt` in the local `.venv`; `pip check` passed.
- Added a short download step for a missing dataset, using the documented Kaggle source.
- Verified that the download matches the dataset and that later runs reuse it.
- Updated the README with commands that use the local environment explicitly.

Additional checks passed:

- The same test source rows, labels, and negation flags as the previous experiment.
- Identical predictions from both methods and the majority baseline.
- Logistic Regression and RoBERTa positive scores agree within numerical tolerance.
- Accuracy and macro F1 recomputed for all nine model/group combinations.
- All six displayed errors correspond to actual incorrect test predictions.
- Notebook outputs include tables, plots, and the demo confidence scores.

Overall Logistic Regression accuracy: 94.62%, macro F1: 0.8888.
Overall RoBERTa accuracy: 93.20%, macro F1: 0.8553.
Negation macro F1: Logistic Regression 0.8886, RoBERTa 0.8632.

The code was simplified without retuning on the test results. The report and
presentation still need to be prepared, and exact submission requirements
should be checked against the instructor's rubric.
