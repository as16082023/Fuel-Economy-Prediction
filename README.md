# Fuel-Economy-Prediction

**Overview:**   
The project focuses on predicting vehicle fuel efficiency (mpg) using linear regression in Python. 
The analysis leverages libraries such as pandas, scikit-learn, and statsmodels to develop and evaluate a model based on features like cylinders, displacement, horsepower, weight, acceleration, model year, origin, and car name. 
The process involves data cleaning, exploratory analysis, feature selection, and model evaluation, addressing challenges such as missing values and inconsistent data formats.
The objective is to build an accurate model and identify key factors influencing fuel efficiency.

**Steps:**
- Data Cleaning:   
  Addressed missing values, inconsistencies, and data type issues to ensure the dataset was ready for analysis.

- Exploratory Data Analysis (EDA):   
  Conducted EDA to explore the relationships between features using pairplots and a correlation heatmap.

- Baseline Model Creation:   
  Developed an initial linear regression model using weight, the feature most strongly correlated with mpg.
  The baseline model provided reasonable but limited predictive power, serving as a starting point for further refinement.

- Feature Engineering:
  To address multicollinearity, added a polynomial term (weight²) before building the multiple regression model.
  Created dummy variables for the categorical origin column to allow its inclusion in the regression model.

- Multiple Linear Regression:
 Initially included all features in the model but then refined it to focus on the top five predictors based on p-values and statistical significance.
 The final model included weight, weight², model year, origin_2, and origin_3.

- Ridge Regression for Comparison:
 Since multicollinearity was a concern, Ridge Regression was used to compare performance.
 While Ridge Regression produced slightly better R-square and MAE scores, the improvement was not substantial enough to outweigh the simplicity and interpretability of the linear 
 regression model with five features.

Therefore, the Linear Regression model was deemed the better choice for this project.

**Conclusion:**     

The analysis revealed the following key findings:    
-  Fuel economy has consistently improved with newer model years, with a significant positive correlation between model year and mpg.
-  Cars from Europe and Japan tend to be more fuel-efficient than those from the United States.
-  Vehicle weight is the most important factor affecting fuel economy. Heavier cars have lower mpg, but the addition of a quadratic term for weight revealed a non-linear effect, with 
   smaller losses in fuel efficiency for very heavy vehicles.
- The Linear Regression model achieved a strong R-square score of 0.86, meaning it explains 86% of the variation in mpg. Its simplicity and accuracy make it a practical choice for 
  analyzing this dataset.

