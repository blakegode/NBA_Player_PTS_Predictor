# NBA Player Performance Prediction

This project aims to predict NBA player performance using data from the 2023-2024 season. The project involves data cleaning, feature selection, and building a machine learning model to forecast how many points an NBA player will score in a given game.

## Project Structure

- `nba_games.csv`: The raw dataset containing NBA box scores of player stats from the 2023-2024 season.
- `data_clean.ipynb`: Jupyter notebook for data cleaning and preprocessing.
- `clean_player_data.csv`: The cleaned dataset containing NBA player performance metrics.
- `prediction.ipynb`: Jupyter notebook for feature selection and building the prediction model.

## Data Cleaning

The `data_clean.ipynb` notebook includes steps to clean and preprocess the raw NBA game data:

1. **Load Data**: Load the raw dataset (`nba_games.csv`).
2. **Convert Playing Time**: Convert playing time from minutes to seconds using a custom function.
3. **Handle Missing Values**: Identify and handle any missing values in the dataset.
4. **Feature Engineering**: Create additional features of shooting statistics from previous games.

## Prediction Model

The `prediction.ipynb` notebook details the steps to build and train a machine learning model:

1. **Load Cleaned Data**: Load the cleaned dataset (`clean_player_data.csv`).
2. **Feature Selection**: Use `SequentialFeatureSelector` with a `RidgeClassifier` to select the most important features.
3. **Data Preprocessing**: Scale the selected features using `MinMaxScaler`.
4. **Model Training**: Train the model using time series cross-validation.
5. **Prediction**: Make predictions based on the trained model.
6. **Accuracy**: Test the accuracy of the model from different ranges from the predicted values.

## How to Run

1. **Clone the repository**:
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **Install dependencies**:
    ```bash
    pip install pandas
    pip install -U scikit-learn
    pip install jupyterlab
    ```

3. **Run the notebooks**:
    Open and run the `data_clean.ipynb` and `prediction.ipynb` notebooks sequentially to clean the data and train the prediction model.

## Dependencies

- pandas
- scikit-learn
- jupyter
