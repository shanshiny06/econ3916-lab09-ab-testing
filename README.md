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

- **Job training:** Trainees earned $1,794.34 more than controls. The permutation test gave p = 0.0046, and the 95% confidence interval ran from $575.18 to $3,262.37.
- **Selection bias:** The simulated observational comparison group gave an ATE of −$14,784.45. The sign flipped from positive to negative, which shows how much a non-random comparison group can distort the result.
- **Cookie Cats:** The level 30 group had a Day-1 retention rate 0.59 percentage points higher than the level 40 group (p = 0.0752), which is not significant at the 0.05 level.
- **Rerun size:** A rerun of Cookie Cats would need 111,192 players per group to detect a difference of that size with 80% power.
