### Sentiment Analysis on Amazon Product Reviews

### ⚠️ Warning Because of large file size. Please go to collab for code view
[Colab Link](https://colab.research.google.com/drive/14h1RA6z36Ith7csETlwk9i73qrjGa0P3?usp=sharing)
<br/><br/>

#### Summary of Findings

In this project, I have compared the performance of several machine learning models, including Logistic Regression, Random Forest, Support Vector Machine (SVM), and a Neural Network, for a binary classification task. The evaluation metrics used were Accuracy, Precision, Recall, F1 Score, and ROC-AUC.
Here’s the updated comparative table with the provided metrics  

---

### Updated Model Performance Comparison

 Metric        Logistic Regression  Random Forest  Support Vector Machine (SVM)  Neural Network           
----------------------------------------------------------------------------------------------------------------------------------
 Accuracy       0.89175                  0.87625            0.89550                       0.91                     
 Precision      0.910091                 0.881402           0.906696                      0.94 (Class 1), 0.79 (Class 0) 
 Recall         0.951677                 0.967456       0.961538                          0.93 (Class 1), 0.83 (Class 0) 
 F1 Score       0.930419                 0.922426           0.933312                      0.94 (Class 1), 0.81 (Class 0) 
 ROC AUC        0.942076                 0.931118           0.945670                      NA                           

---

### Analysis

#### Best Performing Models
- Accuracy Neural Network (0.91)
- Precision Neural Network for Class 1 (0.94)  
- Recall Random Forest (0.967456), closely followed by Neural Network for Class 1 (0.93)
- F1 Score Neural Network for Class 1 (0.94)

#### Strengths
1. Neural Network High accuracy, precision, and F1 Score for Class 1, making it suitable for applications where correctly identifying Class 1 is critical.  
2. Support Vector Machine (SVM) Excellent balance across all metrics with the highest ROC AUC score.  
3. Logistic Regression Slightly behind SVM but still offers reliable results with good interpretability.  

#### Weaknesses
1. Random Forest While it has the highest recall, it lags in other metrics compared to SVM and Neural Networks.
2. Neural Network Lower performance for Class 0, suggesting potential imbalances in predictions for less-represented classes.  

---

#### Recommendations
- Neural Network Use for cases prioritizing Class 1 (positive class) predictions with high precision and recall.  
- SVM Ideal for balanced performance across all metrics, especially when interpretability is not a concern.  
- Logistic Regression Suitable for fast deployment and applications requiring simplicity.  
- Random Forest Use as a backup model for scenarios needing higher recall.


#### Insights and Challenges

1. Data Preprocessing
   - Challenges Ensuring the data was clean and properly formatted was crucial. Handling missing values, outliers, and categorical variables required careful consideration.
   - Lessons Learned Proper data preprocessing significantly impacts model performance. Techniques like normalization, encoding categorical variables, and handling imbalanced datasets are essential.

2. Model Training
   - Challenges Hyperparameter tuning was time-consuming, especially for models like Random Forest and SVM. Finding the optimal set of hyperparameters required extensive experimentation.
   - Lessons Learned Automated tools like Grid Search and Random Search are invaluable for hyperparameter tuning. Cross-validation helped in obtaining more reliable performance estimates.

3. Model Evaluation
   - Challenges Choosing the right evaluation metrics and interpreting them correctly was important. The ROC-AUC curve provided a comprehensive view of model performance across different thresholds.
   - Lessons Learned A combination of metrics (Accuracy, Precision, Recall, F1 Score, ROC-AUC) gives a holistic view of model performance. Visualizations like the ROC curve help in comparing models effectively.

#### Key Results and Visualizations

- ROC Curve
  - The ROC curve visualization showed that all models performed well, with SVM achieving the highest ROC-AUC of 0.95, followed closely by Logistic Regression and Random Forest.

- Classification Report for Neural Network
  - The Neural Network model demonstrated high precision and recall for both classes, with an overall accuracy of 0.91.

- Performance Metrics Table
  - The table summarizing the performance metrics for Logistic Regression, Random Forest, and SVM provided a clear comparison of the models. SVM performed the best in terms of Accuracy, Precision, Recall, F1 Score, and ROC-AUC.


#### Highlight Key Results

- Logistic Regression Performed well with high accuracy and ROC-AUC, making it a strong baseline model.
- Random Forest Showed robust performance with high recall but slightly lower precision compared to other models.
- SVM Achieved the highest ROC-AUC and balanced performance across all metrics, making it the best-performing model in this comparison.
- Neural Network Demonstrated high precision and recall for both classes, with an overall accuracy of 0.91, indicating strong performance.

#### Final Comments

This comparative analysis provided valuable insights into the strengths and weaknesses of different machine learning models. Logistic Regression, Random Forest, SVM, and Neural Networks each have their own advantages and trade-offs. The choice of model should depend on the specific requirements of the task, such as interpretability, computational efficiency, and performance metrics. Future work could involve further hyperparameter tuning, exploring ensemble methods, and evaluating models on more diverse datasets.
