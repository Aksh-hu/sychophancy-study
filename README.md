# Sycophancy Study

# Warmth Fine-Tuning and Sycophancy Under Social Pressure (Llama-3-8B)

This repository contains a controlled study of *pressure-induced answer revision* (“sycophancy”) in LLMs. We test whether **validation-only warmth fine-tuning** increases the tendency to abandon correct answers when a user insists on an incorrect alternative, compared to a **neutral fine-tuning control**.

## What We Did

We trained two LoRA adapters on **Llama-3-8B Base** using matched training settings:

- **Neutral control adapter:** emotionally neutral factual QA
- **Warm/therapist adapter:** emotional validation responses with *no factual content* and with disagreement language discouraged

We evaluated both models on a balanced **120-question** suite. For each item that the model answered correctly at baseline, we applied three escalating forms of user pressure:

1. Soft hint toward an incorrect answer
2. Confident incorrect assertion
3. Emotional appeal framing disagreement as stressful

We report strict “flip” rates (explicit adoption of the incorrect answer) and richer labels capturing partial compliance and noncommittal responses.

## Key Results (Pilot, 120-Item Suite)

Baseline accuracy:
- Neutral: **77.5% (93/120)**
- Warm:   **81.7% (98/120)**

Strict flip rates (denominator = baseline-correct items):
- Soft pressure:      Neutral **8.6% (8/93)**  | Warm **35.7% (35/98)**
- Confident pressure: Neutral **28.0% (26/93)** | Warm **75.5% (74/98)**

Under emotional pressure, the warm model rarely flipped explicitly, but frequently produced **empathic, factually noncommittal** responses (truth-avoidance rather than clear correction).

A paired neutral-vs-warm comparison (tables and figures) is included in `final_comparison/`.

## Repository Structure

- `notebooks/`  
  Fine-tuning and evaluation notebooks (neutral and warm branches).

- `datasets/`  
  Training datasets used for fine-tuning.

- `neutral/` and `warm/`  
  Cleaned data, configs, logs, results, and exported LoRA adapters (checkpoints excluded).

- `final_comparison/`  
  Summary tables, paired comparisons, and figures.

- `verification/`  
  Lightweight artifact verification outputs.

## Reproducing Outputs

Verification (no GPU required):
```bash
python verify_sycophancy_project.py --neutral-root neutral/finetuning_neutral --warm-root warm/warmth_finetuning --out-dir verification_out

