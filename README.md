# Rainfall Prediction using Machine Learning

## Project Overview
This [Rainfall Predictor](https://github.com/jsharonjr/rainfall-prediction-ml-classifier) predicts whether it will rain based on historical weather data from Australia. 
The model analyses atmospheric features such as temperature, humidity, and pressure to identify patterns associated with rainfall.

## Dataset
Source: Australian Government Bureau of Meteorology.      
The dataset contains daily weather observations across multiple Australian locations.
      
## Data Preprocessing and Feature Engineering
- Handling missing values by removing incomplete records
- Filtering data for selected locations:
    - Melbourne
    - Melbourne Airport
    - Watsonia
- Renamed variables for clarity:
    - RainToday → RainYesterday
    - RainTomorrow → RainToday
- Extracted a Season feature from the Date column
- Separated numerical and categorical features for preprocessing

## Machine Learning Approach
A pipeline-based approach was implemented to streamline preprocessing and model training:   
Numerical features: Standard Scaling   
Categorical features: One-Hot Encoding   
Model: Random Forest Classifier  

## Model Training and Evaluation
The dataset was split into training and testing sets using a stratified approach to preserve the class distribution and address imbalance. 
Model performance was further validated using Stratified K-Fold cross-validation, ensuring robust evaluation across multiple data splits. 
To optimise performance, hyperparameter tuning was conducted using GridSearchCV, allowing systematic selection of the best model parameters.

Tuned parameters included: Number of estimators, Maximum depth, Minimum samples split

## Model Performance Comparison
Logistic Regression was implemented as a reference model to enable comparison with the Random Forest classifier. 
The pipeline and the parameter grid were updated for this. 

## Results
The performance of both models was evaluated using accuracy and true positive rate. 
The Random Forest classifier achieved an accuracy of 84% and a true positive rate of 51%, while Logistic Regression achieved an accuracy of 83% and a true positive rate of 50.8%. 
Although Random Forest performed slightly better, the difference between the two models was not significant, indicating that both models produced comparable results.


## How to Run

Clone the repository:

    git clone https://github.com/jsharonjr/rainfall-prediction-ml-classifier

Navigate to the project folder:

    cd rainfall-prediction-ml-classifier
    
Install dependencies:

    pip install numpy pandas matplotlib scikit-learn seaborn
    
Open and run the notebook:

    AUSWeatheripynb.ipynb

## License
Distributed under the MIT License. See [LICENSE](https://github.com/jsharonjr/rainfall-prediction-ml-classifier?tab=MIT-1-ov-file#) for more information.
