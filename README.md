# SafeScan ML Model

SafeScan uses receiver transaction and activity data to estimate UPI
receiver risk before payment.

-   **Dataset:** `training_clean.csv` --- 1,809 rows and 12 columns.
-   **Input features:** Receiver age, transaction counts, unique
    senders, scan count, spam reports, block rate, average transaction
    amount, and hour of day.
-   **Target:** `target_is_risky` (risky / not risky).
-   **Models:** Random Forest and XGBoost, compared using classification
    metrics including precision, recall, F1, ROC-AUC, and PR-AUC.
-   **App verdicts:** Safe, Caution, or Risky, based on risk-score
    thresholds (below 0.49, 0.49--0.79, and 0.79 or above).

**Note:** Validate the dataset labels and test performance before using
predictions for real payment decisions.
