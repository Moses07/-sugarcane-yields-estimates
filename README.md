# -sugarcane-yields-estimates
Use of Regression, Random Forest and Neural Network algorithms (LSTM and Bi-LSTM) in predicting sugarcane yields.

This project addresses the use of different machine learning algorithms, including Regression (using methods such as Lasso, Ridge, and Elastic Net), Random Forest, XGBoost and Neural Networks (LSTM and Bi-LSTM), applied to the prediction of sugarcane agricultural yield. The main objective was to evaluate the accuracy and efficiency of these algorithms in estimating agricultural yield and the impacts of climatic variables on production, providing information to support decision-making in the sugar-energy sector. The methodology includes the use of daily climatic variables such as precipitation, maximum and minimum temperature, soil moisture, and evapotranspiration, as well as derived indices such as the Standardized Precipitation Index (SPI). Data preprocessing steps were performed, including normalization, outlier treatment, and division into training and testing sets. The models were evaluated using metrics such as the coefficient of determination (R²), mean absolute error (MAE), and root mean square error (RMSE). The results show that the Random Forest model performed best overall, surpassing the Lasso, Ridge, and Elastic Net methods and the Neural Networks (LSTM and Bi-LSTM) in terms of accuracy and generalization capacity. However, the R² values ranging from 0.48 to 0.62 for the different sugarcane profiles suggest the need to incorporate additional variables or more complex methods to improve predictive power. The proposed approach provides a complementary tool for crop forecasting in the agricultural sector, contributing to reducing uncertainty and optimizing strategic planning in the sugar-energy sector.

Lasso, Ridge, and ElasticNet are regularization methods used in linear regression to prevent overfitting of models by introducing a penalty on the regression coefficients.

Lasso (Least Absolute Shrinkage and Selection Operator)
Penalty: This method adds an L1 penalty, which adds the absolute value of the regression coefficients to the cost function.
Effect: Tends to reduce some coefficients to zero, performing a type of feature selection, which is useful when aiming to simplify the model and understand which variables are most relevant.
Advantage: Can generate more interpretable models by performing feature selection, keeping only the most significant variables.
Limitation: When there are many correlated variables, it may select only one of them, without capturing the full relationship.

Ridge
Penalty: This method adds an L2 penalty, which adds the square of the regression coefficients to the cost function.
Effect: It reduces the coefficients proportionally but rarely makes any of them exactly zero. That is, Ridge tends to keep all variables in the model but reduces their importance, helping to deal with multicollinearity.
Advantage: It is more suitable for cases where all variables have some contribution to the model, especially when they are highly correlated.
Limitation: It does not perform feature selection and, therefore, can result in more complex models, making interpretability difficult.

Elastic Net
Penalty: A combination of L1 and L2 penalties, meaning it is a combination of the Lasso and Ridge methods.
Effect: It can both reduce some coefficients to zero and reduce others proportionally. The combination of penalties is controlled by a balancing parameter.
Advantage: Ideal when there are many correlated variables, as it combines the benefits of Lasso (feature selection) and Ridge (regularization with multiple correlated variables).
Parameters: It has two main parameters – the regularization value and the proportion that controls the weight between L1 and L2. Correct adjustment of these parameters can generate a more balanced and suitable model.
These methods are widely used in machine learning, especially when working with data that has many variables and it is necessary to prevent the problem of overfitting, in addition to ensuring the interpretability of the model coefficients. In the case of sugarcane productivity prediction from climatic data, these methods are useful to ensure that the model is not disproportionately influenced by less relevant variables.
