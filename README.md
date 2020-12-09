# Ensembles
Model Ensembles to improve prediction


Ensembling Methods:

Ensembling provides higher accuracy, like Random Forest.


VOTING CLASSIFIER
For VERY DIFFERENT classifiers to have independent errors e.g SVM(), logistic(), decisiontree()
Combination of weak learners provide high accuracy..
Law of Large numbers in work.
Ensembling assumes all classifiers are independent. 
You can estimate class probablities with (soft voting) ~ which has a higher accuracy than hard
How do we know they are different?

BOOTSTRAP AND PASTING
Boostrap, Random Sampling with replacement. 
We use a BaggingClassifier() on say, 100 decision trees
Same training algorithm for every predictor and train on different random subsets
Prediction is the staistical mode (most frequent predicition, just like hard voting) for classifiers
or avergae for regression. Bootstrap introduces diversity, hence higher bias, and diversity means less
correlated predictors hance less variance
Out of Bag instances can help show accuracy on test set (set oob_score = True)



BOOSTING

Adaboost
Train predictors  sequentially, each trying to correct its predecessor AdaBoost()
Instances that are wrong have their wieght boosted.
AdaBoost Decision Trees

Gradient Boosting
Uses corrects preceding predictors, but then fits new predictor to residual erros made by previous predictor
max_depth and min_samples_leaf control growth of trees
learning_rate sclaes contribution of each tree. Low value requires more trees, hence generalizing better
Subsample  is fraction of training instances to be used for training each tree. This trades a higher bias for a lower variance

Overfit <- decrease learning rate
Underfit <- increase learning rate. 
Default learning rate = 0.3

DIMENSION REDUCTION
Speed up training and data visualization
This is the curse of dimensionality
In higher dimensional datasets are at risk of being very sparse, new instance likely to far from training instances
Watch video
Need to choose right number of dimensions to preserve 70% + of variance
PCA for classification?
















