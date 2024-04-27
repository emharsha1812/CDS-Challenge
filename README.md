# Movie Metadata Analysis

This project aims to develop machine learning models for predicting movie genres and release years based on various features, including director information, actors, and movie metadata. The primary objectives are:

1. **Genre Classification**: Given a director's name and other movie attributes, predict the genres of the director's next movie.
2. **Release Year Prediction**: Forecast the release year of a director's upcoming movie using relevant features.

## Data Preprocessing

The dataset is preprocessed by handling missing values, encoding categorical features, and creating custom features based on domain knowledge. Key steps include:

- Handling missing values using KNN imputation for numerical features and mode imputation for categorical features.
- One-hot encoding categorical features like director names, content ratings, and genres.
- Creating new features such as director experience, average IMDb score, movie success ratio, and genre frequencies.

## Models and Performance

### Genre Classification

- **RandomForestClassifier**: Accuracy - 0.944, F1-score - 0.937
- **XGBClassifier**: Accuracy - 0.985, F1-score - 0.984

### Release Year Prediction

- **Ensemble Regressor (RandomForestRegressor and XGBRegressor)**: RMSE on the test set - 2.19

The XGBClassifier performed best for genre classification, while the Ensemble Regressor model achieved the lowest RMSE for release year prediction.

## Future Improvements

1. To enhance the regression task's performance, incorporating additional relevant features or acquiring a larger dataset could be explored. More diverse and informative data may lead to improved predictive accuracy for release year forecasting.

2. For Genre Classification, for simplification, only the first Genre value is taken as the true genre. For multi-label classification,

## Usage

This repository contains the code and data for reproducing the analysis. Follow the instructions in the Jupyter Notebook to preprocess the data, train the models, and evaluate their performance.

You will find all the necessary documentation, findings, methodologies, and code in the Jupyter notebook file titled `CodeSubmission.ipynb`.
