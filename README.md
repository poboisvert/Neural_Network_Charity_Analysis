## Project Overview

Using Python's TensorFlow library, the purpose of this project is to use deep learning neural networks to analyze and classify the success of charitable donations. The main goal is to predict which organizations are worth donating (approving) to and which are too high risk (declining).

## Resources

- Data Source: Resources/charity_data.csv
- Software: Python 3.9, Anaconda Navigator 2.0.1, Conda 4.10, Jupyter Notebook 6.2

## Results

- The target variable for my model is the "Is_Successful" column which tells us whether the money was used successfully. Below is the code

> X = application_df.drop(['IS_SUCCESSFUL'],1).values

### Preprocessing

- The features of this model are:

```
APPLICATION_TYPE          object
AFFILIATION               object
CLASSIFICATION            object
USE_CASE                  object
ORGANIZATION              object
STATUS                     int64
INCOME_AMT                object
SPECIAL_CONSIDERATIONS    object
ASK_AMT                    int64
IS_SUCCESSFUL              int64
dtype: object
```

The steps taken to optimize the model included removing the noisy variables ("EIN", "ORGANIZATION", "SPECIAL_CONSIDERATIONS, and "NAME").

> application_df = application_df.drop(columns=["EIN", "NAME","ORGANIZATION","SPECIAL_CONSIDERATIONS"], axis=1)

We added additional neurons and hidden layers (layer3 and layer4)

### Compiling, Training, and Evaluating

> Accuracy: 0.72

## Summary

By following the steps below, we were able to have a working model that had poor performance.

- 1. Preprocess Data for a Neural Network Model
- 2. Compile, Train, & Evaluate the Model
- 3. Optimize the Model

In order to have a result that could be useful, I removed uneccessary variables and increasing additional neurons to each hidden layers.
