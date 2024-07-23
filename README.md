# Baseball Hall of Fame Predictor

This project aims to predict if a Major League Baseball (MLB) player will be inducted into the Hall of Fame based on their career statistics. Using a K-Nearest Neighbors (KNN) algorithm, we developed a model that classifies players as Hall of Famers or non-Hall of Famers.

## Project Motivation

Our motivation stems from a passion for sports, particularly baseball, and a keen interest in data-driven decision-making. By identifying undervalued players through purely statistical analysis, we aim to contribute to the broader field of sports analytics.

## Features

### Algorithm

- **K-Nearest Neighbors (KNN)**: Chosen for its simplicity, ease of implementation, and interpretability. KNN does not make assumptions about the underlying data distribution, making decisions based on the 'nearest' data points according to features.

### Data Sources

- **Lahman Baseball Database**: A comprehensive source of player statistics and award information, providing the necessary data for our analysis.

### Data Processing

- **Cleaning and Processing**: Extensive data cleaning was performed to ensure the quality and accuracy of the dataset. This included handling missing values, normalizing data, and converting categorical variables into numerical formats.
- **Feature Engineering**: Created award tiers to categorize player achievements:
  - **Tier 1**: Most Valuable Player, Pitching Triple Crown, Major League Player of the Year, Pitcher of the Year, Cy Young Award, Triple Crown
  - **Tier 2**: Silver Slugger, Hank Aaron Award, Rookie of the Year
  - **Tier 3**: Gold Glove, All-Star, Outstanding DH Award

### Class Imbalance Handling

- **Oversampling**: Addressed the skewed ratio of Hall of Famers to non-Hall of Famers by oversampling the minority class in the training set. This helped improve the model's ability to accurately predict Hall of Famers.

### Model Validation

- **Partitioning Data**: Split the data into 60% training, 20% validation, and 20% test sets.
- **Hyperparameter Tuning**: Used validation data to find the optimal value of K, balancing bias and variance to achieve the best performance.
- **Error Rate Calculation**: Evaluated model performance using error rates on both validation and test data.

### Visualization

- **Results Presentation**: Clear presentation of results with appropriate error rates and classification outcomes. Visualizations helped in understanding model performance and areas for improvement.

## Results

### Initial Model

- **Challenges**: The initial model faced issues with award feature skewness and class imbalance, leading to high misclassification rates. Some awards did not exist until the 1980s, further complicating the analysis.

### Improved Model

- **Feature Removal**: Removed problematic award features to reduce skewness.
- **Class Imbalance Fix**: Oversampled the training dataset to include more Hall of Famers, significantly reducing misclassification rates and enhancing prediction accuracy for Hall of Famers.

## Limitations

- **Lack of Playoff Statistics**: Our dataset did not include playoff performance, which could be a critical factor in Hall of Fame induction.
- **Historical Shifts**: Changes in baseball statistics and the introduction of awards in different eras affected the model's consistency.
- **Complexities in Oversampling**: Handling class imbalance through oversampling introduced additional complexities in data processing and model training.

## Conclusion

Our project demonstrates the potential of machine learning in sports analytics, providing a framework for predicting Hall of Fame induction based on career performance metrics. Despite some limitations, our model showed promising results, paving the way for further improvements and applications in the field.

## Team

- **Bryan Benavente**
- **Alex Casper**
- **Zack Leonard**
- **Inesh Tickoo**

For more details, refer to our [full report](https://docs.google.com/presentation/d/1BLMbALWPsNALwAadNxVW6TQw1Fjc3aljagco7NiLfTg/). Contributions and feedback are welcome!

## Project Files

### File Descriptions

- **attribute.h**: Header file for the attribute class, defining the attributes used in the model.
- **attribute.cpp**: Implementation of the attribute class, including methods for handling attribute data.
- **instance.h**: Header file for the instance class, defining instances of player data.
- **instance.cpp**: Implementation of the instance class, including methods for processing instances of data.
- **main.cpp**: Main program file that integrates all components, executes the model, and outputs the results.
- **og_test.arff**: Original test dataset in ARFF format.
- **og_train_valid.arff**: Original combined training and validation dataset in ARFF format.
- **og_train.arff**: Original training dataset in ARFF format.
- **og_valid.arff**: Original validation dataset in ARFF format.
- **oversample_train_valid.arff**: Oversampled combined training and validation dataset in ARFF format.
- **oversample_train.arff**: Oversampled training dataset in ARFF format.
- **oversample_valid.arff**: Oversampled validation dataset in ARFF format.
- **test_noaward.arff**: Test dataset excluding the awards feature in ARFF format.
- **training_noaward.arff**: Training dataset excluding the awards feature in ARFF format.
- **validation_noaward.arff**: Validation dataset excluding the awards feature in ARFF format.

### How to Run

1. **Clone the Repository**:
    ```sh
    git clone https://github.com/yourusername/MLB-Hall-of-Fame-Predictor.git
    cd MLB-Hall-of-Fame-Predictor
    ```

2. **Compile the Code**:
    Ensure you have a C++ compiler installed. You can use `g++` for this purpose:
    ```sh
    g++ main.cpp attribute.cpp instance.cpp -o hall_of_fame_predictor
    ```

3. **Run the Program**:
    Execute the compiled program:
    ```sh
    ./hall_of_fame_predictor
    ```

4. **Review the Results**:
    The program will output the prediction results and error rates. Check the terminal for detailed information.

Feel free to contribute to the project by opening issues or submitting pull requests. Your feedback is greatly appreciated!
