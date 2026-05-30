# Neural Forecasting Notes

Paper notes and implementation traces for modern neural time-series forecasting.

The goal is to keep a compact research memory: what the paper claims, what the architecture actually does, what assumptions the benchmark makes, and what to watch for when reproducing results.

## Reading Map

| Topic | Questions |
|---|---|
| Patch-based forecasting | Why do patches stabilize long lookbacks? |
| Inverted transformers | When does variable-token attention help? |
| Linear baselines | Which datasets are mostly trend/seasonality? |
| Temporal CNNs | When does locality beat global attention? |
| Foundation models | What transfers across domains and sampling rates? |

## Note Format

Each paper card tracks:

- core idea
- architectural move
- benchmark setup
- reproducibility risks
- implementation notes
- questions for ablation

## Current Paper Queue

- PatchTST
- iTransformer
- TimesNet
- DLinear / NLinear
- FEDformer
- Informer

