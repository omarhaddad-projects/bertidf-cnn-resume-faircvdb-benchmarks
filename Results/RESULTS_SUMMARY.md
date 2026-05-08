# Benchmark Results Summary

This file summarizes the last executed benchmark results embedded in the source notebook.

## FairCVdb

| Model             | Family                       |   Accuracy (%) |   Macro-F1 |   AUC-macro | Accuracy 95% CI   | Macro-F1 95% CI   |
|:------------------|:-----------------------------|---------------:|-----------:|------------:|:------------------|:------------------|
| BERTidRAAF (Ours) | Proposed BERT+IDF BERTidRAAF |          96.17 |     0.9617 |      0.9805 | 95.58–96.75       | 0.9558–0.9675     |
| BERTLARGE         | Transformer Context Baseline |          96.08 |     0.9608 |      0.9952 | 95.55–96.65       | 0.9555–0.9665     |
| BERTBASE          | Transformer Context Baseline |          96.04 |     0.9604 |      0.9949 | 95.48–96.64       | 0.9548–0.9664     |
| BERT–IDF + CNN    | BERT–IDF Hybrid/Ablation     |          95.96 |     0.9596 |      0.9912 | 95.38–96.56       | 0.9538–0.9656     |
| BERT + CNN        | BERT–IDF Hybrid/Ablation     |          95.88 |     0.9587 |      0.9913 | 95.27–96.44       | 0.9527–0.9644     |
| BERT + IDF        | BERT–IDF Hybrid/Ablation     |          95.81 |     0.9581 |      0.9948 | 95.23–96.40       | 0.9523–0.9639     |
| DeBERTaBASE       | Transformer Context Baseline |          95.79 |     0.9579 |      0.9947 | 95.18–96.38       | 0.9518–0.9637     |
| RoBERTaBASE       | Transformer Context Baseline |          95.56 |     0.9556 |      0.9932 | 94.99–96.15       | 0.9499–0.9615     |
| BERT–IDF + BiLSTM | BERT–IDF Hybrid/Ablation     |          95.38 |     0.9537 |      0.9926 | 94.79–95.94       | 0.9479–0.9593     |
| BERT–IDF + LSTM   | BERT–IDF Hybrid/Ablation     |          94.5  |     0.945  |      0.9908 | 93.87–95.19       | 0.9387–0.9518     |
| LogReg (TF-IDF)   | Lexical Baseline             |          71.75 |     0.7175 |      0.7858 | 70.36–72.99       | 0.7034–0.7299     |
| SVM (TF-IDF)      | Lexical Baseline             |          71.65 |     0.7164 |      0.7856 | 70.32–72.92       | 0.7031–0.7292     |
| MultinomialNB     | Lexical Baseline             |          67.73 |     0.6768 |      0.7127 | 66.44–68.99       | 0.6640–0.6895     |
| LSTM              | Neural Baseline              |          66.85 |     0.6678 |      0.7122 | 65.58–68.19       | 0.6546–0.6811     |
| BiLSTM            | Neural Baseline              |          66.69 |     0.6667 |      0.709  | 65.38–68.02       | 0.6537–0.6800     |
| CNN               | Neural Baseline              |          64.83 |     0.6474 |      0.6957 | 63.62–66.22       | 0.6350–0.6613     |

## Resume

| Model             | Family                       |   Accuracy (%) |   Macro-F1 |   AUC-macro | Accuracy 95% CI   | Macro-F1 95% CI   |
|:------------------|:-----------------------------|---------------:|-----------:|------------:|:------------------|:------------------|
| BERTidRAAF (Ours) | Proposed BERT+IDF BERTidRAAF |          85.71 |     0.8038 |      0.9802 | 82.49–88.84       | 0.7658–0.8324     |
| BERTLARGE         | Transformer Context Baseline |          82.49 |     0.7595 |      0.9708 | 78.87–85.71       | 0.7196–0.7900     |
| BERT–IDF + CNN    | BERT–IDF Hybrid/Ablation     |          81.49 |     0.7435 |      0.9767 | 77.46–84.81       | 0.7043–0.7715     |
| BERT–IDF + BiLSTM | BERT–IDF Hybrid/Ablation     |          81.49 |     0.7425 |      0.9678 | 77.87–84.81       | 0.7066–0.7716     |
| BERT–IDF + LSTM   | BERT–IDF Hybrid/Ablation     |          81.29 |     0.741  |      0.9649 | 77.67–84.71       | 0.7030–0.7702     |
| BERT + CNN        | BERT–IDF Hybrid/Ablation     |          81.09 |     0.7407 |      0.9735 | 77.26–84.21       | 0.7042–0.7695     |
| BiLSTM            | Neural Baseline              |          80.48 |     0.7323 |      0.9753 | 76.66–84.11       | 0.6993–0.7626     |
| BERT + IDF        | BERT–IDF Hybrid/Ablation     |          79.48 |     0.7129 |      0.9687 | 75.86–82.80       | 0.6718–0.7444     |
| BERTBASE          | Transformer Context Baseline |          79.28 |     0.7121 |      0.9685 | 75.45–82.70       | 0.6705–0.7432     |
| RoBERTaBASE       | Transformer Context Baseline |          78.67 |     0.7135 |      0.967  | 74.94–82.09       | 0.6750–0.7451     |
| LSTM              | Neural Baseline              |          78.27 |     0.6971 |      0.9658 | 74.65–81.89       | 0.6658–0.7254     |
| DeBERTaBASE       | Transformer Context Baseline |          75.05 |     0.6825 |      0.9619 | 70.72–78.78       | 0.6445–0.7145     |
| CNN               | Neural Baseline              |          72.03 |     0.6363 |      0.9607 | 68.01–75.76       | 0.5977–0.6659     |
| SVM (TF-IDF)      | Lexical Baseline             |          66.2  |     0.6244 |      0.9628 | 62.17–69.92       | 0.5779–0.6578     |

