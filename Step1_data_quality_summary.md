# Step 1 Data Quality Summary

## Dataset
- File: `diabetes.csv`
- Records: 768
- Input features: 8 (pregnancies, glucose, blood_pressure, skin_thickness, insulin, bmi, diabetes_pedigree, age)
- Outcome column: `Outcome`
- Duplicate full rows: 0
- Missing input cells: 0
- Missing outcome labels: 0

## Outcome counts
| outcome | records | share |
|---|---:|---:|
| 0 | 500 | 0.651 |
| 1 | 268 | 0.349 |

## Values to review
- Zero values that may represent missing measurements: glucose: 5, blood_pressure: 35, skin_thickness: 227, insulin: 374, bmi: 11
- Negative values: No negative values found.
- Zero pregnancies are treated as valid; the other flagged zeros have not been changed in this notebook.

## Limitations
The Pima dataset contains 768 records from adult women of Pima heritage. Findings should be described as patterns in this dataset, not as general clinical guidance.

## Next step
In Step 2, agree with the group which zero codes to treat as missing and fit imputation/scaling using training data only.
