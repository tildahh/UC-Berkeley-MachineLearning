# GridSearching Decision Trees 

We used Gridsearch for decision trees to find the best hyperparameters, since gridsearch for a tree model can get large very easily. We compared the time taken and the score for different search methods.

![Gridsearch Decision Trees](images/grid_search_comparison.png)

                  Method       Time     Score
0           GridSearchCV  11.315509  0.862036
1     RandomizedSearchCV   0.053251  0.851559
2    HalvingGridSearchCV  27.611962  0.850591
3  HalvingRandomSearchCV   0.680731  0.841142

### Summary of findings 
- The HalvingGridSearchCV method is the fastest and has the highest score
- The RandomizedSearchCV method is the slowest and has the lowest score

### Conclusion
- The HalvingGridSearchCV method is the best choice for hyperparameter tuning in this case
- It provides a good balance between speed and accuracy
- The RandomizedSearchCV method is not recommended due to its poor performance
