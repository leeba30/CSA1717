**Artificial Intelligence – Assessment**
**Title**

Machine Learning and Reinforcement Learning for Diabetes Diagnosis and Treatment Recommendation

**Objective**

To formulate and solve an Artificial Intelligence problem using Decision Tree Classification, Gini Index, Logistic Regression, SMOTE, Feature Importance, Q-Learning, Q-Table, and Reinforcement Learning for diabetes diagnosis and personalised treatment recommendation.

**Software Used**

Python 3.x

**Tools Used**

Python IDLE

**Algorithms / Techniques Used**

• Data Pre-processing
• Train-Test Split (70:30)
• Feature Scaling / Normalisation
• SMOTE for Class Balancing
• Decision Tree Classification
• Gini Index
• Cost-Complexity Post-Pruning
• Logistic Regression
• Accuracy, Precision, Recall and F1-Score
• Confusion Matrix
• AUC-ROC
• Feature Importance Analysis
• Q-Learning
• Q-Table
• Epsilon-Greedy Policy
• Reward and Penalty Mechanism
• Policy Learning

**Problems Implemented**

• Diabetes Diagnosis using Decision Tree Classification

• Statistical Risk Stratification using Logistic Regression

• Reinforcement Learning for Personalised Treatment Recommendation using Q-Learning

**Result**

Successfully implemented and analysed the Diabetes Diagnosis and Treatment Recommendation system using Python. The diabetes dataset was pre-processed by handling missing values, normalising the features, and dividing the data into 70% training and 30% testing sets. SMOTE was applied to balance the diabetic and non-diabetic classes.A Decision Tree classifier was constructed using the Gini Index as the splitting criterion. The model was evaluated using Accuracy, Precision, Recall, F1-Score, and Confusion Matrix. False Negative cases were identified because missed diabetic cases are important in a medical diagnosis system. Feature importance was also analysed to identify the major predictors of diabetes. Cost-complexity post-pruning was applied to reduce unnecessary tree complexity and improve the model's suitability for deployment.
Logistic Regression was implemented as a statistical learning model and compared with the Decision Tree using Accuracy and AUC-ROC. The important diabetes predictors were identified from both models and compared.A Q-Learning agent was then developed for treatment recommendation. Patient health conditions were represented as states such as Low Risk, Moderate Risk, High Risk, and Improved, while the possible actions were Diet, Exercise, Medication, and Monitor. The Q-table was updated through multiple patient episodes using rewards and penalties based on health improvement. The final Q-table was used to extract the optimal treatment policy.Overall, the implementation demonstrates how Machine Learning can support early diabetes diagnosis and risk stratification, while Reinforcement Learning can model personalised treatment decision-making. The system also highlights the importance of patient safety, fairness, explainability, and human medical supervision when applying AI in healthcare.
