### Model Interpretation

Use the ROC AUC classification metric
Choosing a target and avoiding leakage of information
Explore and join relational data for supervised learning
Get permutation importances for model interpretation and feature selection
Use xgboost for gradient boosting
Visualize and interpret Partial Dependence & Shapley value plots

![Work life balance image](https://th.bing.com/th/id/R.51922813a695e23c6e50a2c3add6840b?rik=NDOvYXIfUT2I8A&riu=http%3a%2f%2fcurmudgeongroup.co%2fwp-content%2fuploads%2f2019%2f11%2falashiGetty-Images.jpg&ehk=uj7iDm4SvAmVw6wCkH20%2b3LdM%2bNPLQ%2bSE0QHdQNRex8%3d&risl=&pid=ImgRaw&r=0)

 Dataset from Kaggle: **Wellbeing_and_lifestyle_data_Kaggle.csv**
 
 **Target:** determine if there is a Great Work Life Balance when certain features are inplace
 > This dataset is a classification problem
 > Evaluation metrics - accuracy score and the AUC (area below the ROC curve)
 > using time-based split for the train, val and test split
 > looks like there is a value in my val set that might be an outlier ['1/1/00'] might 'ignore' as it may have been a typo for the date and do not know what the user meant for that date to be
>
**Feature Engineering** - create new columns by asking _Does a particular female age group impact if they have a great work life balance_
> Training, Validation and Test sets are split according to year
> 
**Communicating Results:**
 >Using the model_2 after the feature engineering the 4 additional columns categorizing Female's by the Age groups seemed to have lowered the accuracy score of our model_2.
 >Looking at the feature importances, these new Female by age group features seem to be of lower impact on a great work life balance.
 >After using Extreme Gradient Boost Model - (which seems to be overfit), the feature importance indicated the feature **'SUFFICIENT_INCOME'** is of _**most**_ importance feature for my prediction model.
 >Looks like the 4 new columns that I feature engineered for the **Female Age groups** are of _**least**_ importance to this particular predictive model
 >With the model using permutation on the extreme gradient boost classifier model, the top three features that seem to be of most importance to my predictive model on the 'GREAT_WLB' are: BMI_RANGE, SUFFICIENT_INCOME & DONATION
