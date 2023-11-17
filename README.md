#Semiconductor Quality Prediction Project

##Project Overview   
This project addresses a critical challenge faced by a semiconductor factory in optimizing its sensor infrastructure. With data from 200 diagnostic sensors measuring chip quality, the goal is to assess the predictive performance of the current model and propose a cost-effective alternative. The factory is particularly interested in understanding if a smaller subset of sensors can perform as well as, or better than, the existing model in predicting chip defects.

##Data Exploration and Quality Check  
The dataset consists of measurements from 200 sensors, with the binary variable "FAIL" indicating chip defectiveness. Before analysis, a thorough examination of data quality was conducted. Any dubious features were identified and addressed in the analysis.

##Analysis Steps and Policy Questions  
###1. Full Logistic Regression Model  
The initial step involved running a logistic regression model with all 200 predictors. The analysis includes determining the significance of predictors, providing insights into the model's complexity.

###2. Addressing Multiple Testing Problem  
Acknowledging concerns about the multiple testing problem, a histogram of p-values was analyzed. The distribution was assessed to understand the implications of multiple testing and guide further steps.

###3. Benjamini-Hochberg Algorithm  
To address the multiple testing problem, the Benjamini-Hochberg algorithm was applied to control the false discovery rate (FDR) at 10%. The steps involved in this procedure were explained, and a visualization of the BH procedure was provided.

###4. Model Estimation with Significant Regressors  
The model was re-estimated using only the regressors identified as significant after the Benjamini-Hochberg correction.

###5. Cross-Validation for Predictive Accuracy  
Cross-validation was employed to compute the predictive accuracy of both the full and restricted models. The R-squared metric on the test data was utilized as a measure of predictive accuracy. The steps of the cross-validation routine were described, and the performance of both models was evaluated.

###6. Decision Support  
The final section of the analysis provides insights for the factory's decision-making. The comparison of the original model with the smaller model, based on predictive accuracy, guides the recommendation on whether the factory should stick with the current model or adopt the cost-effective alternative.

##Conclusion  
This project offers a comprehensive analysis of semiconductor data, addressing the factory's policy questions and providing actionable insights for optimizing sensor infrastructure. The documented code and results can serve as a valuable resource for data scientists and analysts working on similar challenges in predictive modeling and model optimization.
