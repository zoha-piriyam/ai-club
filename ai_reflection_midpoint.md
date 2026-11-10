# Midpoint Reflection: Phase I and GenAI

**AI-aided pair members**

- **Syeda Nusraht Khaledur** — Student ID: **K12348010**
- **Selvasubramanian SIVAGIRINATHAN** — Student ID: **K12453704**

## What we analyzed

We used the saved predictions from our logistic regression model to study its errors on 154 test records. The model missed 27 of 54 positive cases (50%) and incorrectly flagged 18 of 100 negative cases (18%). We used the charts to see how those errors varied with glucose, BMI, and age.

## What we found

Glucose showed the clearest pattern. The model missed 13 of 18 positive cases with glucose above 118 through 142, compared with 2 of 24 above 142. In that highest glucose range, it also incorrectly flagged 12 of 14 negative records. So the model detected more positive cases in the highest glucose range, but it also raised more false alarms there.

We looked more closely at the 18 positive cases with glucose above 118 through 142. The 13 missed cases had a median BMI of 32.0 and a median age of 32. The five correctly detected cases had a median BMI of 37.1 and a median age of 43. With only five correctly detected cases, this is a pattern to investigate further.

False alarms were also more common in the highest BMI range (10 of 23 negative records) than in the lowest (2 of 36), and in the oldest age range (8 of 21) than in the youngest (3 of 37). These comparisons describe our test set and do not establish that any one feature caused an error.

## What changed when we adjusted the threshold

| Threshold | Missed positive cases | False alarms |
| --------- | --------------------: | -----------: |
| 0.40      |                    19 |           22 |
| 0.50      |                    27 |           19 |
| 0.60      |                    29 |           14 |

Lowering the cutoff from 0.50 to 0.40 caught eight more positive cases but added three false alarms. The sweep shows 19 false alarms at 0.50, while the original saved predictions show 18. One negative record had a saved score of exactly 0.5000 and a saved label of 0; the sweep counted it as positive because it used `>=`.

## Comparison with Group A

Group A split the same test records into two equal halves by pregnancy count. The higher pregnancy half had 13 false alarms among 42 negative records (31.0%), compared with 5 of 58 (8.6%) in the lower half. The table uses the counts printed by Group A's code.

| Glucose range | Higher pregnancy half | Lower pregnancy half |
| ------------- | --------------------: | -------------------: |
| Above 140     |        7 of 8 (87.5%) |       5 of 7 (71.4%) |
| 140 or below  |       6 of 34 (17.6%) |         0 of 51 (0%) |

Both groups found that false alarms were common at higher glucose levels. Group A also found six false alarms at glucose 140 or below in the higher pregnancy half and identified six missed positive cases with scores below 0.20. Group B showed how errors varied across glucose, BMI, and age, and measured what happened when we changed the prediction threshold. Some of these groups were small, so the results are specific to this test set.

## How GenAI influenced our work

GenAI helped us write and debug the notebook and suggested comparing errors by feature and by threshold. We kept those ideas because they showed where the model made mistakes. We revised the feature plots after noticing that zero placeholders for glucose and BMI appeared as real measurements. We also checked the counts behind the charts and the difference between saved and recalculated labels at 0.50. The most useful approach was to give GenAI a specific problem, ask a focused follow-up, and verify the result against the data. The AI interaction record documents the prompts and decisions in more detail.
