# BERTidRAAF for AI-Driven Recruitment

## Reproducible BERT–IDF Rare-Aware Adaptive Fusion Benchmark for CV Classification

This repository provides a reproducible implementation and benchmark of **BERTidRAAF**, a BERT–IDF rare-aware adaptive fusion model for CV classification in AI-driven recruitment.

BERTidRAAF combines BERT-based contextual representations with IDF-weighted lexical evidence to improve recruitment-oriented text classification. The benchmark evaluates the proposed model against lexical, neural, transformer, and BERT–IDF hybrid baselines on the Resume and FairCVdb datasets.

## Main Notebook

The main reproducibility notebook is:

```text
notebooks/BERTidRAAF_Reproducible_BERT_IDF_Benchmark.ipynb
```

## Main Contributions

This repository supports the following contributions:

1. **BERT–IDF rare-aware adaptive fusion architecture**  
   A recruitment-oriented classification model that combines BERT contextual representations with IDF-weighted keyword evidence.

2. **Post-contextual IDF token weighting**  
   IDF weights are applied after BERT contextual encoding to emphasize rare and discriminative tokens while preserving contextual semantics.

3. **Rare-aware gated pooling**  
   A gated pooling mechanism balances contextual evidence and IDF-driven lexical evidence.

4. **Trainable multi-head BERT/IDF logit fusion**  
   Multiple complementary BERT/IDF decision heads are combined through a trainable fusion mechanism.

5. **Multi-sample dropout regularization**  
   Regularized decision heads are used to improve robustness and generalization.

6. **Validation-selected BERT–IDF fusion policy**  
   The final BERT–IDF strategy is selected using only the validation split before evaluation on the held-out test set.

7. **Comprehensive reproducible benchmark**  
   BERTidRAAF is evaluated against lexical baselines, neural baselines, transformer baselines, and BERT–IDF hybrid models.

8. **Article-ready experimental outputs**  
   The notebook exports benchmark tables, confidence intervals, confusion matrices, ROC curves, training curves, and efficiency plots.

## Model Architecture

BERTidRAAF is based on **BERT + IDF** and uses the following components:

1. BERT contextual encoding with `bert-large-uncased`.
2. Post-contextual IDF token weighting.
3. Rare-aware gated pooling.
4. Multi-head BERT/IDF logits.
5. Trainable multi-head BERT/IDF logit fusion.
6. Multi-sample dropout regularization.
7. Validation-selected BERT–IDF expert fusion.
8. BERT-anchored lexical evidence through TF-IDF/IDF branches.

## Datasets

The notebook downloads the datasets from the repository data directory:

```text
Resume  : https://raw.githubusercontent.com/omarhaddad-projects/BERTidRAAF_for_AI-Driven_Recruitment/main/Data/Resume.zip
FairCVdb: https://raw.githubusercontent.com/omarhaddad-projects/BERTidRAAF_for_AI-Driven_Recruitment/main/Data/FairCVdb.zip
```

The benchmark uses:

- **Resume dataset** for multi-class CV category classification.
- **FairCVdb dataset** for external validation in recruitment-oriented classification.

## Benchmark Families

The benchmark includes the following model families:

1. **Lexical baselines**
   - TF-IDF + SVM
   - TF-IDF + Logistic Regression
   - TF-IDF + Naive Bayes

2. **Neural baselines**
   - CNN
   - LSTM
   - BiLSTM

3. **Transformer baselines**
   - BERTBASE
   - BERTLARGE
   - RoBERTaBASE
   - DeBERTaBASE

4. **BERT–IDF hybrid baselines**
   - BERT + IDF
   - BERT + CNN
   - BERT–IDF + CNN
   - BERT–IDF + LSTM
   - BERT–IDF + BiLSTM

5. **Proposed model**
   - BERTidRAAF

## Reproducibility Protocol

The experiments follow a controlled reproducibility protocol:

1. Fixed-seed execution.
2. Train/validation/test evaluation.
3. Validation-based checkpoint selection.
4. Validation-selected BERT–IDF fusion policy.
5. Held-out test reporting.
6. Bootstrap confidence intervals for accuracy and macro-F1.
7. Exported tables and figures for experimental traceability.

## Running the Notebook

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Then open and run the notebook:

```text
notebooks/BERTidRAAF_Reproducible_BERT_IDF_Benchmark.ipynb
```

A GPU runtime is recommended for transformer-based models. The notebook was designed for execution on Google Colab with GPU acceleration.

## Generated Outputs

The notebook exports results to the configured output directory:

```text
/content/bertidraaf_outputs
```

The notebook generates the following reproducibility outputs:

1. benchmark tables;
2. Excel workbook of experimental tables;
3. grouped confusion matrices;
4. proposed-model confusion matrices;
5. ROC curves;
6. accuracy and macro-F1 confidence interval plots;
7. training and validation curves;
8. efficiency plots.

## Last Executed Benchmark Summary

### FairCVdb: Top Models by Accuracy

| Model             | Accuracy (%) | Macro-F1 | AUC-macro | Accuracy 95% CI | Macro-F1 95% CI |
|:------------------|-------------:|---------:|----------:|:----------------|:----------------|
| BERTidRAAF        |        96.17 |   0.9617 |    0.9805 | 95.58–96.75     | 0.9558–0.9675   |
| BERTLARGE         |        96.08 |   0.9608 |    0.9952 | 95.55–96.65     | 0.9555–0.9665   |
| BERTBASE          |        96.04 |   0.9604 |    0.9949 | 95.48–96.64     | 0.9548–0.9664   |
| BERT–IDF + CNN    |        95.96 |   0.9596 |    0.9912 | 95.38–96.56     | 0.9538–0.9656   |
| BERT + CNN        |        95.88 |   0.9587 |    0.9913 | 95.27–96.44     | 0.9527–0.9644   |

### Resume: Top Models by Accuracy

| Model             | Accuracy (%) | Macro-F1 | AUC-macro | Accuracy 95% CI | Macro-F1 95% CI |
|:------------------|-------------:|---------:|----------:|:----------------|:----------------|
| BERTidRAAF        |        85.71 |   0.8038 |    0.9802 | 82.49–88.84     | 0.7658–0.8324   |
| BERTLARGE         |        82.49 |   0.7595 |    0.9708 | 78.87–85.71     | 0.7196–0.7900   |
| BERT–IDF + CNN    |        81.49 |   0.7435 |    0.9767 | 77.46–84.81     | 0.7043–0.7715   |
| BERT–IDF + BiLSTM |        81.49 |   0.7425 |    0.9678 | 77.87–84.81     | 0.7066–0.7716   |
| BERT–IDF + LSTM   |        81.29 |   0.7410 |    0.9649 | 77.67–84.71     | 0.7030–0.7702   |

## Repository Structure

```text
.
├── README.md
├── requirements.txt
├── environment.yml
├── CITATION.cff
├── LICENSE
├── .gitignore
├── Data/
    ├── FairCVdb.csv
    └── Resume.csv
├── Notebooks/
│   └── BERTidRAAF_Reproducible_BERT_IDF_Benchmark.ipynb
├── Figures/
└── Results/
    └── RESULTS_SUMMARY.md
```

## License

This repository is released under the license specified in the `LICENSE` file.
