# ML Method Map

| Course concept | Project application | Problem | Recommended role |
|---|---|---:|---|
| Linear classification | Simple classifier baseline | 1 | Baseline |
| K-nearest neighbors | Nonlinear/local classification baseline | 1 | Classical comparison |
| Linear SVM | Classification | 1 | Classical comparison |
| Decision tree | Classification/regression | 1, 2 | Interpretable classical model |
| Random forest / bagging | Classification/regression | 1, 2 | Strong classical model |
| Naive Bayes | Classification | 1 | Lightweight comparison if data assumptions are reasonable |
| Linear regression | Output Power regression | 2 | Required first regression baseline |
| Regularization | Linear/neural model control of overfitting | 1, 2, potentially 3 | Supporting technique |
| PCA | Dimension reduction | 3 | Primary course-taught method |
| K-means | Possible exploratory grouping | 3 | Optional/exploratory unless rubric requires |
| Gaussian mixture model | Possible exploratory density/grouping | 3 | Optional/exploratory unless rubric requires |
| Semi-supervised learning | Limited-label experiment | 4 | Directly aligned with problem |
| Multilayer perceptron | Tabular classification/regression | 1, 2 | Deep-learning comparison |
| RNN | Sequence forecasting | 2 | Directly relevant |
| LSTM | Sequence forecasting | 2 | Directly relevant and course-taught |
| CNN | Possible learned feature extraction | 1/2/3 | Use only if representation/rubric justifies it |
| Reinforcement learning | Not directly required by Problems 1–5 | — | Probably unnecessary |

## Useful but not verified as course-taught

The supplied project specification explicitly mentions KPCA, autoencoders/VAE, and t-SNE/UMAP. The repository inventory does not provide enough evidence to label those as taught in the course. Treat them as project-requested or potentially useful methods until the binary slide content is readable.

## Probably unnecessary

Reinforcement learning is present in the course sequence but is not part of the five supplied project problems. Additional sophisticated architectures should not be introduced merely for complexity.

## Model progression

For each problem, prefer:

1. Simple baseline.
2. One or two course-taught classical models.
3. Course-taught deep/sequence model where it naturally fits.
4. Additional models only if results or the rubric justify them.
