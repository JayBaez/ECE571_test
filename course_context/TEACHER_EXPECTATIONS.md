# Teacher Expectations

## Evidence status

This checklist is based on the supplied project specification in the conversation. The detailed grading rubric itself was not included in that specification, so rubric-specific point values cannot be asserted yet.

## Global requirements

### REQUIRED
- Keep the project reproducible.
- Use actual executed metrics; never fabricate results.
- Respect time-series ordering where the experiment calls for it.
- Document feature/target leakage controls.
- Use a reusable Python project structure.
- Preserve prior experiment results.
- Explain significant methodological changes.

### RECOMMENDED
- Prefer course-taught methods when appropriate.
- Keep code understandable to a student with basic Python/ML knowledge.
- Maintain fixed random seeds and experiment records.

### OPTIONAL
- Additional models or tuning beyond the core strategy, if results justify the effort.

## Problem 1 — Supervised classification

### REQUIRED
- Perform supervised classification for the specified sky-condition and generation-regime targets.
- Respect the specification's feature-leakage restrictions.
- Report the required classification metrics and figures.
- Compare appropriate models/baselines.

### RECOMMENDED
- Start with a simple baseline.
- Include course-taught classical methods before deep learning.
- Analyze failure modes, class imbalance, and confusion matrices when relevant.

### OPTIONAL
- Additional classifiers or extensive tuning if the core experiments are complete.

## Problem 2 — Supervised regression

### REQUIRED
- Perform the same-city experiment with a chronological split.
- Perform the cross-city experiment.
- Address sequence forecasting and the K=12 recommendation.
- Use the required seeds.
- Report required metrics including nRMSE.
- Produce the required plots.

### RECOMMENDED
- Establish linear/tree baselines before sequence models.
- Explicitly test for sequence-window leakage across train/test boundaries.

### OPTIONAL
- Broader model sweeps or extensive tuning.

## Problem 3 — Dimension reduction

### REQUIRED
- Address PCA/KPCA expectations.
- Evaluate dimensions 2, 5, and 10.
- Include reconstruction analysis where required.
- Evaluate explained variance.
- Perform downstream classification/regression where required.
- Include the required visualization method(s).

### RECOMMENDED
- Keep dimensionality-reduction fitting separate from test data.
- Clearly distinguish reconstruction quality from downstream predictive quality.

### OPTIONAL
- Autoencoder/VAE alternatives if permitted by the full rubric and time.

## Problem 4 — Semi-supervised learning

### REQUIRED
- Evaluate 10%, 30%, and 50% labeled-data settings.
- Include a supervised baseline.
- Compare against the SSL method(s) required by the specification.
- Produce the label-efficiency curve.
- Report gain over supervised and the required AUC.

### RECOMMENDED
- Fix the unlabeled pool construction and random seeds so comparisons are fair.
- Keep validation/test labels unavailable to SSL training.

### OPTIONAL
- Additional SSL algorithms if the required comparison is complete.

## Problem 5 — Transfer learning

### REQUIRED
- Use the specified source and target cities.
- Include a zero-shot baseline.
- Include a few-shot baseline.
- Evaluate the specified fine-tuning/transfer approach.
- Report transfer gain and discuss possible negative transfer.

### RECOMMENDED
- Prevent target-city leakage into source training.
- Make the few-shot sampling protocol reproducible.

### OPTIONAL
- Additional transfer strategies after the required experiments.

## Report

### REQUIRED
- Present actual experimental results.
- Explain methods, splits, metrics, and findings.
- Discuss failures and limitations.
- Keep claims supported by executed experiments.

### RECOMMENDED
- Use consistent experiment IDs and figures.
- Include enough implementation detail to reproduce results.

## Code

### REQUIRED
- Python implementation.
- Reusable components across Problems 1–5.
- Clear dependencies.
- Reproducible seeds/configuration.
- No fabricated result files.

### RECOMMENDED
- Small, readable modules.
- Tests/smoke checks for reusable data and evaluation functions.

## Reproducibility

### REQUIRED
- Record random seeds.
- Record train/test setup.
- Preserve experiment outputs.
- Record package versions.

### RECOMMENDED
- Save split indices and configuration files.
- Use a machine-readable results table.

## Presentation

### REQUIRED
- Explain the methods and conclusions clearly enough to defend them.
- Base numerical claims on actual experiments.

### RECOMMENDED
- Emphasize why models were selected, not merely which model won.
- Include representative plots and failure cases.
