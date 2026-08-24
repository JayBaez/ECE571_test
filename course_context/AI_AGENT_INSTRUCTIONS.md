# AI Agent Instructions

Before changing the project, read:

1. `course_context/COURSE_CONTEXT.md`
2. `course_context/TEACHER_EXPECTATIONS.md`
3. `course_context/DATASET_PROFILE.md`
4. `course_context/EXPERIMENT_PLAN.md`
5. `course_context/PROJECT_STATUS.md`
6. `course_context/YOUR_PROJECT_NOTES.md` when relevant

## Required behavior

1. Inspect existing code and data before modifying anything.
2. Never fabricate results, metrics, plots, or dataset facts.
3. Preserve previous experiment results; do not overwrite evidence without a clear reason.
4. Explain significant methodological changes before implementing them.
5. Stop and report after completing the requested stage.
6. Ask for permission before major methodological changes, large experiments, or changes to the experimental strategy.
7. Keep Python understandable to a student with basic Python/ML knowledge.
8. Prefer course-taught methods where they fit the assignment.
9. Prioritize the grading requirements over unnecessary model complexity.
10. Control random seeds and record experiment configuration.
11. Treat time ordering and leakage prevention as first-class requirements.
12. Verify code behavior with small/safe tests before expensive experiments.

## Results integrity

Every numerical result must come from an actually executed experiment. If something cannot be verified, label it as unknown rather than guessing.

## Workflow

Inspect → understand → propose → explain → obtain approval when required → implement → verify → report → stop.
