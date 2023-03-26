# Credit_Risk_Analysis
## Supervied Machine Learning
A classwork example in which models to predict credit risk are assessed using machine learning techniques like imbalanced-learn, SMOTE, and SMOTEEN.
# Overview 
"LendingClub: a peer-to-peer lending services company" is requesting that we analyze their credit-risk dataset using 4 different machine learning models. These models will be used to make predictions about credit-risk based on patterns present within the dataset. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. This means we would need to apply more weight towards good loans, predicting that good loans should always outnumber the amount of risky loans in a model. In statistics and data analysis, this is otherwise known as class imbalance - a situation where the existing classes in a dataset aren't equally represented.

# Results
### RandomOverSampler
- The balanced accuracy score is the percentage of predictions that are correct. This is a comparison of the original dataset that was set aside for testing and the models predictions that were correct. RandomOverSampler was only accurate 65% of the time.
- Precision (pre) is the measure of how reliable a positive classification is. Since precision is so high for low_risk and so low for high_risk, RandomOverSampler is not as precise as can be even though the overall score is quite high. Precision comes to be 0.99 or 99%.
- Recall (rec) is the ability of the classifier to find all the positive samples. Recall (also known as sensitivity) is quite low for high_risk and low_risk, which indicated that there is a considerate amount of false negative values meaning the model was often incorrect. Recall comes to be 0.59 or 59%.
- F1 Score (f1) is a weighted average of the recall and precision values. Since recall and precision were both less than ideal, F1 comes to be 0.73 or 73%.
- Geometric mean and index balanced accuracy will not be evaluated in this project.

### SMOTE
- The SMOTE model was only correct 66% of the time.
- Precision is quite high at 99%, although the same high_risk and low_risk inconsistency is present.
- Recall is moderate at 69% with both high and low_risk scoring quite poor.
- F1 is improved compared to ROS at 81%. Since precision is quite high, this is to be expected.
- Geometric mean and index balanced accuracy will not be evaluated in this project.

### Undersampling 
- The ClusterCentroid model was only correct 54% of the time. This is the least accurate we have seen so far.
- Precision is quite high at 99%, although the same high_risk and low_risk inconsistency is present.
- Recall is low at 40% with both high_risk performing moderately and low_risk scoring quite poor
- F1 has decreased compared to ROS and SMOTE at 56%.
- Geometric mean and index balanced accuracy will not be evaluated in this project.

# Summary
To summarize, The EasyEnsembleClassifier model offered the highest scores for the balanced accuracy score, recall, and F1. In addition, precision is very high at 99% and the high_risk classifier has the highest precision score of all of the models tested. The high scores for this model is most likely due to the combination of boosting and random undersampling to maximize learning efficiency.

I would highly recommend using EasyEnsembleClassifier model for continued tests. It appears the efficiency of the model is unbeatable, and clearly producers more accurate, more precise, and more sensitive results.
