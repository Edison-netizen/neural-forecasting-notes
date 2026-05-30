# Paper Card: PatchTST

## Why This Paper Matters

Patch-based forecasting makes long lookbacks cheaper and often more stable. It also raises a practical question: how much of the gain comes from patching itself versus the transformer block after patching?

## Core Idea

Split each univariate channel into patches, embed those patches, and model temporal dependencies over patch tokens.

## Implementation Notes

- Patch length and stride are not minor details.
- Channel-independent processing should be tested against multivariate mixing.
- Longer lookbacks can help, but they also change the comparison budget.

## Reproduction Risks

- Different lookback lengths across baselines.
- Inconsistent normalization across datasets.
- Over-reading average benchmark tables without inspecting horizon-wise behavior.

## Ablation Questions

1. What happens if patch length is halved?
2. Does channel independence still help on strongly coupled variables?
3. Does a simple linear head on patches capture most of the gain?

