
**i. Which insights did you gain from your EDA?**

In the exploratory data analysis we found most of the transactions are CASHOUT, PAYMENT or CASHIN making up 90% of all transactions. The transaction amount is right skewed and that most of the amounts that are being transfered are less than 20,000. There is very few transactions that are fraudulent making the dataset is imbalanced. 

**ii. How did you determine which columns to drop or keep? If your EDA
informed this process, explain which insights you used to determine
which columns were not needed.**

In order to train our model to reduce the number of false positives the naive model for flagging fraudulent transactions was dropped. Since we don't want it's prediction to be used as a input to determine our output of if a transaction is fraudulent. 

Additionally we drop 3 columns: step, nameDest and nameOrig since we do not need the names of the transaction columns for training our model. Another thing we will have to do in the cleaning part is rebalance our dataset so that majority of our data is non-fraudlent otherwise the model might just label everything as not fraudulent and still have a high accuracy.

**iii. Which hyperparameter tuning strategy did you use? Grid-search or
random-search? Why?**

For optimizing the hyperparameters grid search was used due to knowing which hyperparameters we wanted to look at and manually trying out which parameters would result in a better f1 score.


**iv. How did your model's performance change after discovering optimal
hyperparameters?**

Both the gradient boosting and the random forest model f1 score increased by 4% after tuning the hyperparameters.


**v. What was your final F1 Score?**

The final f1 score for the gradient boosting model was 98.91% and the random forest model was 99.36%