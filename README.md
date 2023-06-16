# Dry Beans Classification with KNIME: A Visualisation Analytics Project

## Problem Definition

The goal of this project is to design a KNIME workflow of algorithms to correctly classify seven different classes of dry beans using sixteen distinct features. This study is motivated by the desire to provide a standardized seed classification in market-specific scenarios considering factors such as form, shape, type, and structure of the beans.

## Data

The dataset comprises 13,611 grains captured from seven distinct types of dry beans using a high-resolution camera. These beans are characterized by sixteen features, twelve being different lengths and four being distinct shapes. The classes of beans are Seker, Barbunya, Bombay, Cali, Dermosan, Horoz, and Sira.

## Workflow Design

The workflow design of this project leverages the KNIME analytics framework, a robust ETL tool. The workflow follows a series of steps that include importing the data, visualising/exploring data, cleaning and scaling data, splitting data into train and test sets, modelling using classification algorithms, and declaring the findings.

## Data Processing

### Importing Data

The data is imported via the Excel Reader node. It supports XLSX, XLSM, and XLS file formats, reading one sheet per file. 

### Data Exploration

The exploration phase is critical to understanding trends and extracting insights from the data. The Linear Correlation and Statistics nodes help visualize data effectively. The data exploration revealed that there were no missing values in the dataset.

### Data Cleaning

In the data cleaning phase, missing values were tackled, and unnecessary features were removed. The Missing Value node appends the median values to all continuous features with a missing value. As discovered earlier, the dataset has no missing values.

### Feature Scaling

Normalization was performed using the Normaliser node, scaling all numeric columns linearly.

### Feature Split

The Partitioning node splits the features into a train set (70% of the data) and a test set (30%).

## Modelling

Two classification algorithms, Naive Bayes and Random Forest Classifier, were used for modelling.

### Naïve Bayes Classifier

The Naive Bayes Learner node constructs a Bayesian model, and the Naive Bayes Predictor Node predicts the class per row based on the learned model. The Scorer node evaluates the model. The Naive Bayes model correctly classified 3,620 out of 4,084 dry bean images, with an accuracy score of 88.6%.

### Random Forrest Classifier

Random Forest Node learns by randomly selecting a few decision trees. The Random Forest predictor then aggregates the predictions of individual trees. The Scorer assesses the model's performance. The Random Forest model correctly predicted 3,759 out of 4,084 dry bean images, with an accuracy score of 92%.

## Conclusion

The project succeeded in classifying dry bean images using two classification algorithms correctly. The Random Forest Classifier delivered the best performance, due to its ability to reduce decision tree overfitting, thus improving precision. KNIME Analytics platform helped streamline operations, offering an easy-to-use, codeless environment.

## How to Use

1. Download or clone this repository to your local machine.
2. Install [KNIME Analytics Platform](https://www.knime.com/downloads) if you haven't done so.
3. Open KNIME and import the workflow.
4. Run the workflow to see the results. Feel free to modify or optimize the models.
