# Model Card: BERTidRAAF

## Model name

BERTidRAAF (Ours)

## Full name

BERT with IDF-aware Rare-Aware Adaptive Fusion

## Intended task

CV and resume text classification for recruitment-oriented benchmarking.

## Architecture summary

1. BERT contextual encoder.
2. Post-contextual IDF token weighting.
3. Rare-aware gated pooling.
4. Multi-head BERT/IDF logits.
5. Trainable BERT/IDF logit fusion.
6. Multi-sample dropout regularization.
7. Validation-selected BERT–IDF fusion.

## Evaluation datasets

1. FairCVdb.
2. Resume.

## Evaluation protocol

The final model strategy is selected using the validation split and then evaluated on the held-out test split. Test accuracy and macro-F1 include bootstrap confidence intervals.

## Limitations

The benchmark is dataset-dependent and should not be used as a standalone hiring decision system. Outputs should be interpreted as classification benchmark results rather than employment recommendations.
