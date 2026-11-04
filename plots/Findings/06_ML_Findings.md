This markdown file will go through every graph/plot in the 06_ML notebook and explain our findings.

06_ML_plot_01: Correlation between ML predictor features 

This heatmap shows correlations between the model's input features. 
The predictors include differences between opposing teams in historical matches played, recent form, goals scored and conceded, 
historical win rates, World Cup experience and rest periods. 
The correlation heatmap shows that some historical performance measures are related to one another. 

06_ML_plot_02: 2018 Validation Performance by Model

This graph compares the macro F1 scores of four classification models on the 2018 World Cup validation set. 
Macro F1 evaluates performance across home wins, draws and away wins while giving equal importance to each outcome class. 
So we trained and compared several machine learning models to predict home wins, draws, and away wins. 
We used the 2028 World Cup as out validation set and compared the models using macro F1. 
Random forest achieved the highest score of 0.42 narrowly outperforming gradient boosting and logistic regression. 
All three models performed better than the dummy baseline. 
Based on this, we selected random forest for our final evaluation. 

06_ML_plot_03: Final 2022/2026 Test - Selected model vs baseline

This graph compares the final random forest model against a dummy baseline on the combined 2022 and 2026 test set. 
The model achieved a macro F1 score of 0.52, compared with 0.21 for the dummy baseline. 
It also achieved an accuracy of 56.5%, compared with 45.8% for the baseline. 
This demonstrates that historical team information can improve match-outcome predictions. 
However, the model still made a considerable number of incorrect predictions, highlighting the uncertainty involved in football results. 

06_ML_plot_04: Confusion Matrix - Random Forest 

The confusion matrix compares the actual match outcomes with those predicted by the random forest. 
The model performed reasonably well at identifying home and away wins, correctly predicting 49 home wins and 37 away wins. 
However, it struggled with draws, correctly identifying only 9 of the 39 actual draws. 
This highlights an important limitation of the model: It is better at predicting a winner than recognising when 2 teams 
will draw. 
Therefore, although the overall results improve on the baseline, performance is not consistent across all match outcomes. 

06_ML_plot_05: Permutation importance on the 2022/2026 Test Set

This graph investigates which historical features were most useful to the final random forest model. 
Permutation importance measures how much the model's macro F1 score changes when a feature's values are randomly shuffled. 

Differences in previous World Cup appearances and historical World Cup win rates were among the most useful predictors. 
Recent goals conceded and historical overall win rate also contributed positively. 
This suggests that World Cup experience, historical team strength and defensive performance contain useful information for 
predicting match outcomes. 
However, these results describe how our model uses the features, rather than proving that any individual feature causes 
a team to win. 

