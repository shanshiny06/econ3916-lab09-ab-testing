# econ3916-lab09-ab-testing
# A/B Testing — Designing the Data-Generating Process

## Objective

I measured the effect of a job training program and a mobile game change using randomized experiments, and I showed why randomization matters by comparing the experimental result to a biased observational one.

## Methodology

- I loaded the LaLonde NSW job training experiment (445 people: 185 trainees and 260 controls) and computed the experimental average treatment effect (ATE) on earnings.
- I simulated an observational comparison group to show selection bias, and I split the gap into two parts: Observational ATE = True ATE + Selection Bias.
- I ran a permutation test with 9,999 shuffles to check whether the earnings difference could be explained by chance.
- I built a bootstrap BCa 95% confidence interval for the ATE.
- I ran a power analysis to find the power of this study and the sample size needed to detect three different dollar effects.
- I applied the same tests to the Cookie Cats mobile game A/B test (90,189 players), where the first gate was placed at level 30 or level 40, and the outcome was Day-1 retention.
- I wrote a sample-size function, `n_needed()`, checked its output against the power analysis, and used it to size a rerun of the Cookie Cats test.

## Key Findings

- **Job training:** Trainees earned $[YOUR VALUE] more than controls. The permutation test gave p = [YOUR VALUE], and the 95% confidence interval ran from $[YOUR VALUE] to $[YOUR VALUE].
- **Selection bias:** The simulated observational comparison group gave an ATE of $[YOUR VALUE]. The difference from the experimental estimate shows how much a non-random comparison group can distort the result.
- **Cookie Cats:** Day-1 retention differed by [YOUR VALUE] percentage points between the level 30 and level 40 groups (p = [YOUR VALUE]).
- **Rerun size:** A rerun of Cookie Cats would need [YOUR VALUE] players per group.
