All Doc2vec50 files are in Zip. 
Set up directory to import all. 

1)The code starts by rearranging the data set.
2)Mutual information is used to find which features are not importent.
3)28 features are removed by using Kbest function.
4)Four classifiers are used: (1)KNN (2)SVM (3)lgbm(Light Gradient Boosting Machine (4) Logistic regression
5)We perform ensemble stacking for prediction. The models used in stacking are as follows:
Base Level : LR, SVC, lgbm.
Level 1: LR

Note that each of the single classifier(KNN, SVM, lgbm, LR) is modelled using pipeline and foloowed by using GridSearch Cv for finding best performing Hyperparameters. 
Also, note that GridSearch CV is used for determining some of the best hyperparameters of each model. Since it is very time consuming to go over each and every hyperparameters.

Additional Note: Some classifiers Like SVM and Stacking model may take long time to run depening on CPU / GPU configerations. 