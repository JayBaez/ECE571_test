# Course Context

## Phase 0 scope

This file records the course knowledge that can be verified from the repository inventory and the project instructions supplied for this stage. The repository contains 19 course teaching files: 18 PDFs and 1 PPTX, plus the Excel project dataset. The connector available to this agent can inspect repository metadata but cannot decode the binary PDF/PPTX/XLSX payloads. Therefore, this first committed knowledge base does **not** pretend to contain slide-level equations or examples that were not actually readable.

## Verified course sequence

The repository inventory identifies the following teaching topics:

1. Week 01 — ML introduction
2. Week 02 — ML basic concepts
3. Week 03a — Linear classification
4. Week 03b — Linear regression
5. Week 04 — K-nearest neighbors
6. Week 05 — Linear SVM
7. Week 06a — Decision trees
8. Week 06b — Bagging and random forest
9. Week 07 — Naive Bayes classifier
10. Week 08 — K-means clustering
11. Week 09 — Gaussian mixture model
12. Week 10 — Principal component analysis
13. Week 11 — Regularization
14. Week 12 — Semi-supervised learning
15. Week 13 — Multilayer perceptron
16. Week 14 — CNN
17. Week 15a — Recurrent neural network
18. Week 15b — Long short-term memory
19. Week 16 — Reinforcement learning

The repository therefore provides direct evidence that classification, regression, nearest-neighbor methods, SVM, trees/ensembles, Naive Bayes, clustering, PCA, regularization, semi-supervised learning, MLPs, CNNs, RNNs, LSTMs, and reinforcement learning are represented in the course sequence.

## Project-relevant course methods

### Classification

The strongest directly evidenced course topics for Problem 1 are linear classification, KNN, linear SVM, decision trees, random forests, and Naive Bayes. The project should compare a simple baseline against a small number of these course-aligned models rather than immediately jumping to deep learning.

### Regression

Linear regression is explicitly present in Week 03b and is the natural first regression baseline for Problem 2. Tree/ensemble methods may also be considered because decision trees and random forests are taught, while sequence models are directly represented by RNN and LSTM material.

### Unsupervised learning and dimensionality reduction

K-means and Gaussian mixture models are explicitly present. PCA is explicitly present and is directly relevant to Problem 3. The supplied project instructions also mention KPCA, autoencoders/VAE, and t-SNE/UMAP, but the repository inventory alone does not establish that every one of those methods was taught. They must not be labeled as course-taught until slide content is actually available for inspection.

### Regularization

Regularization is explicitly represented in Week 11 and should inform model-selection and overfitting discussions, especially for linear models and neural networks.

### Semi-supervised learning

Week 12 directly supports the conceptual basis for Problem 4. The supplied specification requires experiments at 10%, 30%, and 50% labeled data and comparison against a supervised baseline.

### Neural networks and sequence models

MLP, CNN, RNN, and LSTM are explicitly represented in Weeks 13–15. RNN/LSTM are particularly relevant to the sequence-forecasting component of Problem 2. CNNs are course-taught but are not automatically necessary for tabular solar forecasting; their use should be justified by the data representation and grading requirements.

### Reinforcement learning

Week 16 is present, but reinforcement learning does not appear to be required by Problems 1–5 in the supplied project specification. It should therefore be treated as probably unnecessary for this project unless the full rubric says otherwise.

## Important limitation

The detailed slide text, equations, examples, and instructor-specific terminology still need to be extracted from the 19 binary course files. The repository currently contains those files, but the available GitHub connector cannot decode their binary contents. This limitation is intentionally recorded instead of filling gaps with generic ML knowledge.

## Project principles extracted from the supplied instructions

- Favor understandable Python.
- Prefer methods taught in the course when they fit the problem.
- Use reproducible experiments and actual executed metrics.
- Do not fabricate results.
- Treat time ordering and leakage as first-class concerns.
- Use a reusable framework rather than five unrelated codebases.
- Get approval before major methodological changes.
