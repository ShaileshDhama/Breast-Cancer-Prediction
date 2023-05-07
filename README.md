# Breast Cancer Prediction and Analysis
## Predict whether the cancer is benign or malignant

**Author**: SHAILESH DHAMA

### Business problem: To predict whether the cancer is benign or malignant.

### Dataset : https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)

### Required Libraries :

    1.Numpy
    2.Pandas
    3.Matplotlib
    4.Seaborn
    5.scikit-learn
    6.Plotly

## STEPS :

    - Read data
    - Missing values
    - Drop useless variables
    - Exploratory Data Analysis (EDA)
    - Features distribution(hue = diagnosis)
    - Positive correlated features
    - Uncorrelated features
    - Negative correlated features
    - Principal Component Analysis
    - Confusion matrix
    - Precision-recall curve
    - ROC curve
    - Logistic Confusion matrix
    - Logistic regression with RFE
    - Predictive model : Logistic Regression
    - Predictive Model-2: Ensemble Classifier to maximise precision and detect all malignant tumors
    - Voting classifier : select threshold (recall = 100%)
    - Voting classifier : predicting with recall = 100% (precision = 92%)
    - Models performance plot (accuracy, precision, recall)

### Step 1: Read data
The first step is to read the dataset using Pandas. The dataset contains 569 observations with 32 variables. The first variable is ID, which is not useful for our analysis, so we drop it.

### Step 2: Missing values
After reading the dataset, we check if there are any missing values. Fortunately, there are no missing values.

### Step 3: Drop useless variables
The next step is to drop the ID variable, which is not useful for our analysis.

### Step 4: Exploratory Data Analysis (EDA)
In this step, we perform exploratory data analysis to understand the data. We use Matplotlib and Seaborn libraries to create histograms, scatter plots, and box plots to visualize the data.

### Step 5: Features distribution(hue = diagnosis)
We create a pairplot to visualize the distribution of features in the dataset, where hue represents the diagnosis (benign or malignant). We use the Seaborn library to create this plot.

### Step 6: Positive correlated features
We use the heatmap function from Seaborn to create a heatmap of positive correlation between the features. The heatmap helps us identify which features are highly correlated with each other.

### Step 7: Uncorrelated features
We use the heatmap function from Seaborn to create a heatmap of uncorrelated features. The heatmap helps us identify which features are not correlated with each other.

### Step 8: Negative correlated features
We use the heatmap function from Seaborn to create a heatmap of negative correlation between the features. The heatmap helps us identify which features are negatively correlated with each other.

### Step 9: Principal Component Analysis
We use the scikit-learn library to perform Principal Component Analysis (PCA). PCA helps us reduce the dimensionality of the dataset and identify the most important features.

### Step 10: Confusion matrix
We use the scikit-learn library to create a confusion matrix, which helps us evaluate the performance of our predictive model.

### Step 11: Precision-recall curve
We use the scikit-learn library to create a precision-recall curve, which helps us evaluate the precision and recall of our predictive model.

### Step 12: ROC curve
We use the scikit-learn library to create an ROC curve, which helps us evaluate the performance of our predictive model.

### Step 13: Logistic Confusion matrix
In step 13, the logistic confusion matrix is computed to evaluate the performance of the logistic regression model. The confusion matrix is a table used to evaluate the performance of a binary classification model. It consists of four measures: true positives (TP), false positives (FP), true negatives (TN), and false negatives (FN). The logistic regression model is trained to predict whether the cancer is benign or malignant. The confusion matrix can be calculated as follows:

Let y be the actual cancer diagnosis (0 for benign, 1 for malignant), and y_hat be the predicted cancer diagnosis by the logistic regression model. Then, the confusion matrix can be defined as:

$$
\begin{matrix}
 &  & \text{Predicted} &  & \\
 &  & \text{Benign} & \text{Malignant} & \\
\text{Actual} & \text{Benign} & TN & FP \\
& \text{Malignant} & FN & TP \\
\end{matrix}
$$

Where TP is the number of true positives (malignant tumours correctly classified as malignant), FP is the number of false positives (benign tumours incorrectly classified as malignant), TN is the number of true negatives (benign tumours correctly classified as benign), and FN is the number of false negatives (malignant tumours incorrectly classified as benign).

The confusion matrix can compute several performance metrics, including accuracy, precision, recall, and F1 score. These metrics can be computed using the following formulas:

- Accuracy = (TP + TN) / (TP + FP + TN + FN)
- Precision = TP / (TP + FP)
- Recall (Sensitivity) = TP / (TP + FN)
- Specificity = TN / (TN + FP)
- F1 Score = 2 * Precision * Recall / (Precision + Recall)

These metrics provide insights into the model's performance, such as how often it correctly predicts malignant tumours, how often it incorrectly predicts benign tumours as malignant, and how often it correctly predicts benign tumours.

## RESULTS :

#### Data distribution
![graph1](./BC_0.PNG)
![graph1](./BC-1.PNG)
![graph2](./BC-2.PNG)
> Data distribution.

#### Features distribution(hue = diagnosis)
![graph3](./BC-3.PNG)
![graph4](./BC-4.PNG)
![graph5](./BC-5.PNG)
![graph6](./BC-6.PNG)
![graph7](./BC-7.PNG)
![graph8](./BC-8.PNG)
![graph9](./BC-9.PNG)
> Mean of Features distribution.

#### Correlation Matrix for Variables
![graph10](./BC-10.PNG)
> correlation matrix


#### Positive correlated features
![graph10](./BC_1.png)
> Positive correlated features


#### Uncorrelated features
![graph10](./BC_2.png)
> Uncorrelated features

#### Negative correlated features
![graph10](./BC_3.png)
> Negative correlated features

#### Principal Component Analysis
![graph10](./BC-15.PNG)
> PCA : Explained variance
![graph10](./BC-16.PNG)
> PCA Scatter(2 Components)
![graph10](./BC-17.PNG)
> PCA Scatter(3 Components)

### Final RESULT : Overall performance of Models.
![graph10](./BC_4.png)
> Performance(cross_val_mean)


### For further information:

Please review the narrative of our analysis in [our jupyter notebook](./breast-cancer-analysis-and-prediction-on-winconsin.ipynb)

For any additional questions, please contact **shaileshshettyd@gmail.com)

##### Repository Structure:

```
├── README.md                                                             <- The top-level README for reviewers of this project.
├── breast-cancer-analysis-and-prediction-on-winconsin.ipynb              <- narrative documentation of analysis in jupyter notebook.
└── images                                                                <- both sourced externally and generated from code.
```
