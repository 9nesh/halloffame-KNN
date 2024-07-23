# Baseball Hall of Fame Predictor

This project aims to predict if a Major League Baseball (MLB) player will be inducted into the Hall of Fame based on their career statistics. Using a K-Nearest Neighbors (KNN) algorithm, we developed a model that classifies players as Hall of Famers or non-Hall of Famers.

## Features

- **Algorithm**: Utilized KNN for its simplicity and effectiveness in classification problems.
- **Data Sources**: Lahman Baseball Database for comprehensive player statistics and award information.
- **Data Processing**: Extensive data cleaning and feature engineering, including the creation of award tiers.
- **Class Imbalance Handling**: Addressed the skewed ratio of Hall of Famers to non-Hall of Famers by oversampling the minority class in the training set.
- **Model Validation**: Achieved an optimal test error rate of 2.31% through rigorous validation and tuning of hyperparameters.
- **Visualization**: Clear presentation of results with appropriate error rates and classification outcomes.

## Results

- **Initial Model**: Encountered issues with award feature skewness and class imbalance, leading to high misclassification rates.
- **Improved Model**: After removing problematic features and oversampling, significantly reduced misclassification rates, enhancing prediction accuracy for Hall of Famers.

## Limitations

- Lack of playoff statistics.
- Historical shifts in baseball statistics.
- Complexities in oversampling and data processing.

## Conclusion

Our project demonstrates the potential of machine learning in sports analytics, providing a framework for predicting Hall of Fame induction based on career performance metrics.

## Team

- Bryan Benavente
- Alex Casper
- Zack Leonard
- Inesh Tickoo

For more details, refer to our [full report](https://docs.google.com/presentation/d/1BLMbALWPsNALwAadNxVW6TQw1Fjc3aljagco7NiLfTg/). Contributions and feedback are welcome!
