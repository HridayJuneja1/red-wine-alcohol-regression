# Predicting the Alcohol Content of Red Wine with PyCaret 4.0

**Author:** Hriday Juneja
**Course:** INFO40975 Artificial Intelligence, Sheridan College
**Project:** Project 7: Wine Quality Data Set (red wine) | Regression | Target: `alcohol`

## Abstract

In this project I used PyCaret 4.0 to predict the alcohol content (% by volume) of Portuguese "Vinho Verde" red wines from their other physicochemical properties, using the red wine data from the UCI Wine Quality dataset (Cortez et al., 2009). The data had 240 duplicate rows, so I removed them and split the remaining 1,359 wines into 70% training and 30% testing data. I then compared 24 regression models with 10-fold cross-validation. Support Vector Regression (SVR) had the lowest RMSE (0.5302), with LightGBM (0.5440) and Gradient Boosting (0.5469) close behind. After tuning SVR with a custom grid (C = 50, gamma = 0.01, epsilon = 0.1), its cross-validation RMSE dropped to 0.5024 (R² = 0.7764). On the test set, the final model reached an RMSE of 0.5430 and an R² of 0.7458, so it explains about 75% of the variation in alcohol content. Density was the strongest predictor by a wide margin, since alcohol is lighter than water and lowers the density of the wine.

## Video Presentation
[](PASTE_YOUR_VIDEO_LINK_HERE)


## Results

| Model | Evaluation | RMSE | MAE | R² |
|---|---|---|---|---|
| SVR (untuned) | 10-fold CV | 0.5302 | 0.3892 | 0.7536 |
| SVR (tuned, custom grid) | 10-fold CV | 0.5024 | 0.3704 | 0.7764 |
| SVR (tuned, custom grid) | Test set | 0.5430 | 0.4165 | 0.7458 |

## Dataset

[UCI Wine Quality Data Set](https://archive.ics.uci.edu/ml/datasets/Wine+Quality) (red wine, 1,599 samples, 11 physicochemical features and a quality score).

P. Cortez, A. Cerdeira, F. Almeida, T. Matos and J. Reis. Modeling wine preferences by data mining from physicochemical properties. Decision Support Systems, 47(4):547-553, 2009.

## How to Run

1. Open `AI_Research_Project.ipynb` in [Google Colab](https://colab.research.google.com/).
2. Run the first cell to install PyCaret 4.0.
3. Restart the session (**Runtime > Restart session**).
4. Click the second code cell and choose **Runtime > Run cell and below**.

## License

This project is released under the [MIT License](LICENSE).
