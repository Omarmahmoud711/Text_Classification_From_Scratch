# Logistic Regression for Text Classification

This project implements and compares three different logistic regression models for text classification using bigrams:
- **Logistic Regression from Scratch**: Implemented using NumPy
- **Logistic Regression (sklearn)**: Using `LogisticRegression` from scikit-learn
- **SGD Classifier (sklearn)**: Using `SGDClassifier` with `log_loss`

## Dataset
The models are trained on a text classification dataset where input sentences are transformed into bigram representations.

## Model Training
Each model follows these steps:
1. Convert text data into bigram features
2. Train a logistic regression model
3. Evaluate on train and test sets

## Results
### Accuracy Comparison

```
+-------------------------------+----------------+---------------+
|             Model             | Train Accuracy | Test Accuracy |
+-------------------------------+----------------+---------------+
| Logistic Regression (Scratch) |     0.9882     |     0.3493    |
| Logistic Regression (sklearn) |     0.9946     |     0.3489    |
|         SGD Classifier        |     0.9940     |     0.3443    |
+-------------------------------+----------------+---------------+
```

### Sample Predictions

```
+-------------------------------------------------------------------------------------------------------------------------------------+------------+-----------------+------------------+-----------------+
|                                                             Test Sample                                                             | True Label | LR From Scratch | SGD with Bigrams | LR with Bigrams |
+-------------------------------------------------------------------------------------------------------------------------------------+------------+-----------------+------------------+-----------------+
|                                           but like most rabbits it seems to lack substance                                          |     1      |        1        |        1         |        1        |
|                                                             no question                                                             |     2      |        2        |        1         |        1        |
|               nolan bravely treads where few american films dare to delve into the world of ambivalence and ambiguity               |     3      |        3        |        3         |        3        |
|                                                 the movie makes absolutely no sense                                                 |     0      |        0        |        1         |        1        |
| this is a raw and disturbing tale that took five years to make and the trio absorbing narrative is a heartwrenching showcase indeed |     3      |        4        |        2         |        2        |
+-------------------------------------------------------------------------------------------------------------------------------------+------------+-----------------+------------------+-----------------+
```
