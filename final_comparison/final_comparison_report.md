# Final Neutral vs Warm Comparison

Backups are ignored. This comparison uses only the clean final folders.

## Model-Level Results

| Condition | Neutral | Warm | Warm - Neutral |
|---|---:|---:|---:|
| Baseline accuracy | 77.5% | 81.7% | +4.2 pp |
| Soft Strict flip | 8.6% | 35.7% | +27.1 pp |
| Soft Broad sycophantic error | 9.7% | 36.7% | +27.1 pp |
| Soft UNCLEAR | 0.0% | 2.0% | +2.0 pp |
| Confident Strict flip | 28.0% | 75.5% | +47.6 pp |
| Confident Broad sycophantic error | 32.3% | 85.7% | +53.5 pp |
| Confident UNCLEAR | 1.1% | 2.0% | +1.0 pp |
| Emotional Strict flip | 21.5% | 0.0% | -21.5 pp |
| Emotional Broad sycophantic error | 22.6% | 2.0% | -20.5 pp |
| Emotional UNCLEAR | 3.2% | 64.3% | +61.1 pp |

## Paired Item-Level Results

| Pressure | Both Baseline Correct | Strict Paired Diff | Strict McNemar p | Broad Paired Diff | Broad McNemar p |
|---|---:|---:|---:|---:|---:|
| Soft | 89 | +24.7 pp | 2.744e-05 | +23.6 pp | 0.0001037 |
| Confident | 89 | +46.1 pp | 8.225e-10 | +52.8 pp | 5.52e-12 |
| Emotional | 89 | -21.3 pp | 3.815e-06 | -21.3 pp | 2.098e-05 |

## Interpretation

The clean headline is whether warm fine-tuning preserves baseline accuracy while increasing pressure-induced answer revision. Soft and confident pressure should be treated as the primary sycophancy evidence because they have many strict flips. Emotional pressure should be reported separately because the warm model produces many UNCLEAR or affective-deflection responses.