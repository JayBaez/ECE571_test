# My Project Notes

## Things I Need to Understand

- Confirm the exact dataset schema and timestamp interval before implementing models.
- Understand which features are explicitly allowed for each target, especially when a target is derived from irradiance measurements.
- Understand how the required K=12 sequence horizon maps to the actual sampling interval.

## Important ML Concepts

- Chronological train/test splitting for time-series data.
- Data leakage and fitting preprocessing only on training data.
- Classification vs. regression metrics.
- PCA and explained variance.
- Semi-supervised learning and label efficiency.
- Transfer learning and negative transfer.

## Project Decisions

- Start with a reasonable model progression rather than trying an excessive number of models.
- Expand model breadth later only if results or the grading requirements justify it.

## Ideas I Might Try Later

- Additional classical models if the core comparisons are inconclusive.
- Alternative dimensionality-reduction methods if explicitly required or clearly useful.

## Questions for My Professor

- Confirm any ambiguous target definitions or feature restrictions.
- Confirm exact expectations for KPCA/autoencoder/VAE and visualization methods.
- Confirm how the grading rubric weights breadth versus depth.

## Things I Need to Explain in the Presentation

- Why chronological splitting is necessary.
- How leakage was prevented.
- Why the final models were selected.
- What failed and what those failures teach us.

## Things Claude Recommended

- Keep the project reusable and understandable.
- Preserve experiment history and never fabricate metrics.

## Things I Changed Personally

- None recorded yet.

## Potential Improvements

- Add automated data-profile checks once local workbook access is available.
- Add lightweight smoke tests for reusable components before training.

## Things Not To Forget

- Never use test labels for training or tuning.
- Never fit scalers or learned representations on the full dataset before evaluation.
- Watch for overlapping sequence windows across train/test boundaries.
- Check city-specific Output Power scales.

## Notes About the Grading Rubric

- The detailed rubric point values were not included in the supplied project instructions, so this section should be updated when the actual rubric is available.
- Prioritize correctness, reproducibility, required comparisons, analysis, code quality, report quality, and presentation quality.
