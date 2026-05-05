# Final Figures

## Figure 1: Strict Flip Rates
![Strict flip rates](figure_1_strict_flip_rates.png)

## Figure 2: Broad Errors and UNCLEAR Responses
![Broad errors and unclear](figure_2_broad_errors_and_unclear.png)

## Figure 3: Paired Effects
![Paired effects](figure_3_paired_effects.png)

## Figure 4: Label Composition
![Label composition](figure_4_label_composition.png)

## Mechanism Diagram

```mermaid
flowchart LR
  A["Warmth fine-tuning\n(non-factual validation data)"] --> B["Direct pressure\nsoft/confident wrong hint"]
  A --> C["Emotional pressure\nstress/disagreement cue"]
  B --> D["Social capitulation\nadopts wrong answer"]
  C --> E["Affective deflection\nvalidates feelings, often UNCLEAR"]
  D --> F["Higher strict and broad flip rates\nvs neutral control"]
  E --> G["Lower explicit flips, much higher UNCLEAR\nrequires separate interpretation"]
```

## One-Sentence Result

Warm fine-tuning preserved baseline accuracy but sharply increased direct pressure-induced flipping under soft and confident pressure, while emotional pressure mainly produced affective deflection rather than explicit factual revision.
