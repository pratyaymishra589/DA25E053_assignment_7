# DA25E053_assignment_7

In this notebook, we performed a multi-class model selection task using the Statlog (Landsat Satellite) dataset. Our analysis involved several key steps:

1.  **Data Loading and Preprocessing:** We loaded the dataset using the `ucimlrepo` library and performed a stratified train-test split to ensure representative class distributions. We then scaled the features using `StandardScaler`.

2.  **Baseline Model Evaluation:** We trained and evaluated several baseline classification models including K-Nearest Neighbors, Decision Tree, Dummy Classifier, Logistic Regression, Gaussian Naive Bayes, and Support Vector Classifier (SVC). Initial evaluation using Overall Accuracy and Weighted F1-Score provided a preliminary ranking of models, with KNN and SVC performing well.

3.  **ROC Analysis:** We extended the ROC curve and AUC concept to our multi-class problem using the One-vs-Rest (OvR) approach. We calculated both macro-averaged and weighted-averaged ROC curves and their corresponding AUC scores. The weighted-average ROC plot visually confirmed the superior performance of SVC and KNN in distinguishing between classes across various thresholds.

4.  **Precision-Recall Curve (PRC) Analysis:** Recognizing the potential for class imbalance, we also analyzed the models using Precision-Recall Curves, which are more informative in such scenarios. We calculated the weighted-averaged Average Precision (AP) from the OvR Precision-Recall Curves. The PRC plot and the AP scores highlighted the strong performance of SVC and KNN, while also revealing the limitations of models like the Decision Tree in maintaining high precision at higher recall levels.

5.  **Comparison of Rankings:** We compared the model rankings based on Weighted F1-Score, Weighted Average ROC-AUC, and Weighted Average Precision (PRC-AP). While SVC and KNN consistently ranked at the top, the comparison underscored the insights gained from using different metrics, particularly the value of the PRC-AP in evaluating performance on positive classes.

6.  **Final Recommendation:** Based on the comprehensive evaluation across all metrics, the **Support Vector Classifier (SVC)** model was recommended as the best model for this classification task due to its consistent high performance, strong discrimination ability (high ROC-AUC), and effective performance on positive classes (high PRC-AP).

This analysis demonstrates the importance of using a diverse set of evaluation metrics, including both ROC and Precision-Recall curves, for robust model selection in multi-class classification problems, especially when dealing with potential class imbalance.
