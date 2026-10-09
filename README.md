# KC House-Price-Prediction-Using-Machine-Learning
A machine learning regression project that analyzes King County housing data and predicts residential property prices using housing characteristics.

This project explores the factors associated with house prices in King County and develops machine learning models to predict residential property prices.

The project follows an iterative modelling approach, beginning with a simple baseline model and progressively adding relevant features to improve the model's performance.

The final Linear Regression model achieved an **R² score of 0.7001** and a **Mean Absolute Error (MAE) of approximately $127,617** on the test set.

## Objectives

Explore and understand the housing dataset.
Identify features that are associated with house prices.
Build a baseline regression model.
Improve model performance by selecting additional relevant features.
Evaluate and compare different stages of the modeling process.
Interpret the results and identify potential areas for future improvement.

##  Dataset

The dataset contains **21,613 housing records** and the following **21 variables**:

Number of bedrooms and bathrooms
Living area (`sqft_living`)
Lot size (`sqft_lot`)
Number of floors
Waterfront status
Property view
Property condition
Property grade
Above-ground living area
Basement area
Year built and year renovated
ZIP code
Latitude and longitude
Price

The target variable is **`price`**, representing the sale price of the property.

## Exploratory Data Analysis(EDA)

The analysis examined:

 Dataset structure and descriptive statistics
 Missing values
 Distributions of housing variables
 Correlations between numerical features and price
 Average house prices across different lot-size categories
 Relationships between property characteristics and house prices

### Key Findings

Some of the strongest individual linear relationships with price were:

| Feature         | Correlation with Price |
| --------------- | ---------------------: |
| `sqft_living`   |                  0.702 |
| `grade`         |                  0.667 |
| `sqft_above`    |                  0.606 |
| `sqft_living15` |                  0.585 |
| `bathrooms`     |                  0.525 |
| `view`          |                  0.397 |

`condition` and `sqft_lot` showed relatively weak individual linear correlations with price.

In particular, `sqft_living` showed the strongest individual linear correlation with house price among the features examined.

##  Modeling Approach

The dataset was divided into:

* **80% training data:** 17,290 records
* **20% testing data:** 4,323 records

The project evaluated model performance using:

* **Mean Absolute Error (MAE)** — measures the average absolute difference between predicted and actual prices.
* **R² Score** — measures how much of the variation in house prices is explained by the model.

### Model Progression

| Model                      |             MAE |         R² |
| -------------------------- | --------------: | ---------: |
| Always Predict Mean        |     $239,998.84 |     0.0000 |
| Baseline Linear Regression |     $222,618.15 |     0.1716 |
| Improved Linear Regression |     $160,877.30 |     0.5764 |
| Final Linear Regression    | **$127,616.70** | **0.7001** |

The baseline model used a small number of features, while subsequent models incorporated additional housing and geographic characteristics.

## Final Model

The final Linear Regression model used the following features:

```text
grade
view
sqft_living
bathrooms
bedrooms
waterfront
condition
floors
yr_built
yr_renovated
zipcode
sqft_basement
lat
long
```

### Performance

**R²:** 0.7001
**MAE:** $127,616.70

An R² of approximately 0.70 means that the model explains about **70% of the variation in house prices on the held-out test data**.

The MAE indicates that the model's predictions differ from actual prices by approximately **$127,617 on average**.

These predictions should be treated as estimates rather than precise property valuations.

##  Technologies Used

 **Python**
 **Pandas** — data manipulation and analysis
 **NumPy** — numerical computing
 **Matplotlib** — data visualization
 **Seaborn** — statistical visualization
 **Scikit-learn** — machine learning and model evaluation
 **Jupyter Notebook** — development and analysis environment

## Takeaways

 Property characteristics such as living area and grade have strong positive linear relationships with house price.
 Increasing the number of relevant features substantially improved model performance.
 The final model performed considerably better than both the mean-price baseline and the initial Linear Regression model.
 The final model explains approximately 70% of the variation in house prices on the test set.

## Future Improvements

The project could be further improved by:

 Encoding `zipcode` as a categorical rather than continuous variable.
 Testing non-linear models such as Random Forest and Gradient Boosting.
 Applying cross-validation.
 Performing hyperparameter tuning.
 Engineering additional features.
 Conducting more detailed residual analysis.
 Investigating neighborhood and socioeconomic variables that may provide additional predictive information.

##  Author

**Leah Wokabi**

Data Science & Analytics Student


