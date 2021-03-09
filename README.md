
### Introduction:

Problem statement: Can we predict if someone is staying in the United States or going abroad on thier AirBnB vacation? To examine this question we look at 77,641 observations from AirBnB and look att 30 feature columns (including dummy columns) to construct then evaluate two classification models, a Logisitic Regression and Random Forest Classifier.

### EDA & Model Interpretation:
| Model                    | Baseline Accuracy | Training Score | Testing Score |
|--------------------------|-------------------|----------------|---------------|
| Logistic Regression      | 0.793             | 0.982          | 0.982         |
| Random Forest Classifier | N/A               | 1.0            | 1.0           |


### Summary & Conclusion:
In the end we chose our features due to our understanding of the travel industry and the demographics of the individuals using the AirBnB service. To recall, our initial problem statement: Can we predict if someone is staying in the United States or going abroad on thier AirBnB vacation? Based on the feature selection and model implementation we see that our model can predict with near certainty the likelihood that one will either be booking a domestic or international vacation.

In conclusion, we see that the RandomForest Classification model generates the highest accuracy score with minimal overfitting. This is likely due to the way the RandomForest is structured as an ensemble model that is aggregating multiple decision trees from multiple bootstrapped models in a way that controls for the variance within the models bagged models. This is potentially an explanation for why we do not see much overfitting in the model. However, with RandomForest models, this decorrelative function usually comes at the cost of some bias thus to see accuracy levels at 100% is perhaps a surprising, but welcome, result.

Potential further steps would include spending more time during EDA and examining select features more closely during preprocessing. We could include the NDF (no destination found) classifier within the country_destination feature as that did account for a considerable amount of the observations. Further, we could binarize the country variable more effectively by adding single numerics for each country rather than assigning a 1 to the United States and a 0 for the remaining countries.