---
# Hotel Booking Classification Prediction

## About Dataset

This dataset contains 119,390 observations for a City Hotel and a Resort Hotel. Each observation represents a hotel booking between the 1st of July 2015 and 31st of August 2017, including bookings that effectively arrived and bookings that were canceled.

### Content

Since this is real hotel data, all data elements pertaining to hotel or customer identification were deleted. Four columns, 'name', 'email', 'phone number', and 'credit_card', have been artificially created and added to the dataset.

### Acknowledgements

The data is originally from the article "Hotel Booking Demand Datasets," written by Nuno Antonio, Ana Almeida, and Luis Nunes for Data in Brief, Volume 22, February 2019. You can find the dataset on [Kaggle](https://www.kaggle.com/datasets/mojtaba142/hotel-booking/data).

## Approach

### Table of Contents

- EDA
  - Data Structure
  - Categorization of Variables
  - Univariate Analysis
  - Target Variable
  - Booking Time Information
  - Numerical Features
  - Categorical Features
  - Guest Information
  - Booking Information
- Modelisation
  - Preprocessing Steps
  - Model
- Results
  - Hyperparameter Tuning

### Modelisation

#### Preprocessing Steps

We performed several preprocessing steps:

- Removed variables 'company' and 'agent' due to lack of information and numerous missing values.
- Detected and removed duplicate rows, balancing the data.
- Removed variables causing multicollinearity.
- Handled missing values by imputing with the mode.
- Treated outliers, such as correcting unrealistic values in the 'babies' column.
- Applied one-hot encoding and target encoding to categorical variables.
- Scaled numerical features using StandardScaler.

#### Model

We built a Sequential neural network model with three hidden layers and one output layer with sigmoid activation. To prevent overfitting, we used L2 regularization, class weights, and early stopping.

### Results

The model achieved 85% accuracy on the testing data. Confusion matrix analysis showed good precision, recall, and F1-score.

### Hyperparameter Tuning

We attempted hyperparameter tuning using Keras Tuner. Although the process could improve accuracy, it was stopped due to computational constraints.

Future Preparation:

For further improvement, we suggest using SMOTE techniques to balance the data.

## Usage

This repository includes Jupyter notebooks and Python scripts for exploring the dataset, preprocessing the data, building the model, and evaluating the results. The provided Colab notebook demonstrates hyperparameter tuning.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
