# SafeScan ML Model V1

SafeScan uses receiver transaction and activity data to estimate UPI
receiver risk before payment.

-   **Dataset:** `training_clean.csv` --- 1,809 rows and 12 columns.
-   **Input features:** Receiver age, transaction counts, unique
    senders, scan count, spam reports, block rate, average transaction
    amount, and hour of day.
-   **Target:** `target_is_risky` (risky / not risky).
-   **Models:** Random Forest (85% accuracy) and XGBoost (86% accuracy), compared using classification
    metrics including precision, recall, F1, ROC-AUC, and PR-AUC.
-   **App verdicts:** Safe, Caution, or Risky, based on risk-score
    thresholds (below 0.49, 0.49--0.79, and 0.79 or above).

**Note:** This is V1 So the accuracy is 85% - 86% and it will improve in next versions !!!
