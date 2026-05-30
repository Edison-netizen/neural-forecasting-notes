# Paper Card: DLinear / NLinear

## Why This Paper Matters

Linear baselines are uncomfortable in a useful way. They force every neural forecasting experiment to answer whether the improvement comes from representation learning or from the dataset being dominated by trend and seasonality.

## Core Idea

Use simple linear mappings over the lookback window, optionally separating trend and seasonal components before prediction.

## Implementation Notes

- Keep normalization and split protocol identical to neural baselines.
- Report horizon-wise error, not only average error.
- Compare against seasonal naive before claiming model capacity matters.

## Reproduction Risks

- Accidentally fitting scalers on validation/test.
- Tuning lookback length differently across baselines.
- Reporting only the horizon where neural models look strongest.

## Ablation Questions

1. Does the result survive when the lookback changes from 96 to 336?
2. Is the gain concentrated on high-seasonality datasets?
3. How much of the error is removed by a seasonal naive baseline?

