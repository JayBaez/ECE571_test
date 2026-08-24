# Experiment Plan

This is a proposed plan only. No experiments are executed in Phase 0.

## Problem 1 — Classification

**Objective:** Predict the specified sky-condition and generation-regime classes without leakage.

**Preprocessing:** Validate labels first; encode categorical variables; scale only when required by the model; fit preprocessing on training data only.

**Baseline:** Majority-class classifier.

**Classical models:** Linear classifier, linear SVM, decision tree, random forest. KNN/Naive Bayes can be used as secondary comparisons if useful.

**Deep model:** MLP.

**Metrics:** Use the metrics explicitly required by the final specification/rubric; include confusion matrices and class-level analysis where appropriate.

**Key risk:** If the target is derived from GHI/Clearsky variables, using those same variables as predictors can create target leakage. The exact allowed feature list must be resolved before implementation.

**Order:** data/label validation → baseline → linear/SVM → tree/forest → MLP → failure analysis.

## Problem 2 — Regression and sequence forecasting

**Objective:** Forecast Output Power under same-city chronological and cross-city settings, including sequence forecasting.

**Preprocessing:** Sort by timestamp; construct features without looking into the future; fit scalers on training data only.

**Baseline:** Persistence/naive forecast where applicable, then linear regression.

**Classical models:** Linear regression, regularized regression if justified, decision tree/random forest.

**Deep model:** MLP followed by RNN/LSTM for sequence forecasting.

**Sequence:** Follow the specification's K=12 recommendation. Confirm the exact sampling interval before interpreting K as a physical horizon.

**Metrics:** Required regression metrics including nRMSE and the specified seeds.

**Key risks:** chronological split violations, overlapping train/test windows, city-specific power scales, and future information entering lag features.

**Order:** timestamp validation → chronological baseline → linear/tree model → MLP → RNN/LSTM → cross-city → analysis.

## Problem 3 — Dimension reduction

**Objective:** Compare reduced representations at dimensions 2, 5, and 10 and assess reconstruction/downstream predictive usefulness.

**Methods:** PCA first. Evaluate KPCA and any explicitly required autoencoder/VAE method only after the exact rubric requirements are confirmed.

**Outputs:** explained variance, reconstruction measures, downstream classification/regression, and the specified low-dimensional visualization.

**Key risk:** fitting dimensionality reduction on the complete dataset can leak test-distribution information into the representation. For predictive evaluation, fit transformations using training data only.

**Order:** PCA → downstream baseline → alternative required reduction method(s) → reconstruction → visualization → analysis.

## Problem 4 — Semi-supervised learning

**Objective:** Quantify how performance changes with 10%, 30%, and 50% labeled data.

**Baseline:** Fully supervised model trained only on the selected labeled subset.

**SSL:** Use the method taught/required by the course/project after the exact algorithm is confirmed.

**Outputs:** performance at each label fraction, label-efficiency curve, gain over supervised, and required AUC.

**Key risk:** accidental use of held-out labels or inconsistent sampling between supervised and SSL conditions.

**Order:** define fixed evaluation set → generate reproducible labeled subsets → supervised baselines → SSL → label-efficiency curve → AUC.

## Problem 5 — Transfer learning

**Objective:** Measure transfer from the specified source city to target city.

**Baselines:** Zero-shot source-trained model and few-shot target-data baseline.

**Transfer:** Fine-tuning/transfer method required by the project specification.

**Outputs:** transfer gain and analysis of negative transfer.

**Key risk:** target-city contamination of source training or tuning data.

**Order:** define city split → source baseline → zero-shot → few-shot → transfer/fine-tuning → transfer gain → failure analysis.

## Reproducibility

Every eventual experiment should record at least:

- experiment ID
- problem
- model
- dataset/city
- feature configuration
- split method
- seed
- preprocessing configuration
- metric names and values
- runtime
- code/version identifier
- notes

Results should be append-only rather than overwriting prior experiments.
