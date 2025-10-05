# Nairobi Apartment Price Prediction

## Project Overview
This project develops a machine learning model to predict apartment prices in Nairobi, Kenya based on house size. The model uses linear regression to establish the relationship between apartment size (in square meters) and price, specifically focusing on properties in the Westlands and Kilimani areas.

## Business Problem
Real estate pricing in Nairobi's competitive market requires data-driven approaches. This project addresses the need for accurate price estimation based on property characteristics, enabling better decision-making for buyers, sellers, and real estate professionals.

## Dataset
The analysis uses property data from Nairobi, focusing specifically on:
- **Property Type**: Apartments only
- **Locations**: Westlands (training data) and Kilimani (testing data)
- **Key Features**: House size (square meters) and Price (Kenyan Shillings)

### Data Cleaning Process
The `wrangle()` function performs comprehensive data preprocessing:
- Filters for apartments in specified locations
- Handles missing values in Price and House size columns
- Cleans currency formatting (removes 'KSh' and spaces)
- Converts House size to integer (removes 'm²' units)
- Removes outliers using IQR method

  ## Technical Implementation

### Libraries Used
- pandas: Data manipulation and analysis
- matplotlib: Data visualization
- scikit-learn: Machine learning implementation
  - LinearRegression
  - mean_absolute_error
  - check_is_fitted

### Model Validation
- **Training Data**: Westlands apartments (16 samples)
- **Testing Data**: Kilimani apartments (24 samples)
- **Evaluation Metric**: Mean Absolute Error (MAE)

## Model Development

### Baseline Model
- **Approach**: Predicts mean apartment price regardless of size
- **Performance**: MAE of 6319761.65 KSh

### Linear Regression Model
- **Algorithm**: Scikit-learn LinearRegression
- **Features**: House size as independent variable
- **Target**: Apartment price

### Model Performance
| Model Type | MAE (KSh) | Improvement over Baseline |
|------------|-----------|---------------------------|
| Baseline   | 6,319,762 | - |
| Training   | 4,165,225 | 34.1% improvement |
| Testing    | 4,417,993 | 30.1% improvement |

## Results

### Model Equation
The final predictive model:
- apartment_price = 1,602,491 + 95,767.01 × House_size


### Key Findings
1. **Strong Predictive Power**: House size is a significant predictor of apartment prices
2. **Good Generalization**: Model performs well on unseen data (Kilimani area)
3. **No Overfitting**: Minimal performance difference between training and test sets
4. **Business Value**: Provides reliable price estimates with approximately 4.4 million KSh average error

## Conclusion
The developed linear regression model successfully predicts Nairobi apartment prices with reasonable accuracy, demonstrating that house size is a strong determinant of property value. The model shows good generalization capabilities and provides a solid foundation for more comprehensive real estate pricing tools.

---
*This project demonstrates practical application of machine learning in real estate valuation, providing actionable insights for the Nairobi property market.*
