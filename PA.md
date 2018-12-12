**Analytics. Why do we do it?** We'd like to be able to, from historical information, glean valuable insights that can lead to better estimations & forecasts.

**Describe the 2 major problems that PA attempts to solve & provide 1 real-life example of each.**<br>
PA aims, chiefly, to solve **(a) classification** & **(b) regression** problems. Classification problems aim to predict a continuous categorical variable using a data record's various features. An example of a classification problem is- predicting a person's age based on their music library. Regression problems, on the other hand, aim to predict a continuous target variable's value from a raw data record, using (again) its various features. As an example, trying to predict the value of a company's stock the next week is a regression problem.

#### Types of Data
All data falls into 2 very distinct data types. Namely, **numerical** & **categorical** data. The difference should be obvious. Within categorical data, though, there exists another binary split- **nominal** & **ordinal** data. Nominal data refers to any 'ol categorical data- say, gender, for example- whereas ordinal data can be ranked. For example, education or academic grades.


### PA vs BI
**How variables of interest are identified** <br>
in BI, these variables are largely **user-driven**. This process is thus dependent on our understanding of the raw data. <br>
in PA, these variables are, conversely, **data-driven**. They're chosen by the model after a thorough consideration of all possible patterns.

**How analytics is carried out** <br>
in BI, analysis is typically **retrospective**. We're looking at historical data to find a pattern.
in PA, analysis is **futuristic**. We're looking for a way to predict what will happen.

### CRISP-DM
Cross Industry Standard Process for Data Mining- a description of the predictive modelling process.

1. **Business Understanding** <br>
  Before a project can begin, it has to be defined. So, experts are brought in to elicit the objectives of the project. These experts can be **domain experts**, **data experts**, or **predictive modelling experts**.

  **Domain Experts** are people with specialised knowledge that can help to frame the problem. Really, this just refers to the users. **Data Experts** are people that can identify the available data & determine how it can be normalised such that it can be useful to the project. **Predictive Modelling Experts** are the ones that builds the models & magicks the magic.

2. **Data Understanding** <br>
  Refers to preliminary analysis of the data- data preprocessing. This stage therefore includes things like checking for any problems in the data, to determine the quality of the data.

3. **Data Preparation** <br>
  Cleaning the data- raw data is **ugli**! Includes tasks like data transformation & the identification of a **target variable**- the value to be estimated or predicted.

4. **Modelling** <br>
  Forming a good, problem-dependent model.

5. **Evaluation** <br>
  A good model scores well in both accuracy & interpretation!

6. **Deployment** <br>
  It's possible to deploy models before completion, as a baseline model, to either get a sense of which variables are good features or to identify potential obstacles with deployment.

### SEMMA
Sample, Explore, Modify, Model, & Assess- A logical organization of tools useful in data mining.

**Sample**- Extracting from the data set a portion large enough to contain significant information, yet small enough to be easy to manipulate.
<br>
**Explore**- Searching for unanticipated trends to gain understanding using visualisations, or statistical techniques like mean, median, etc.
<br>
**Modify**- Transformation of the data, for it to become more useful. e.g. removing unrelated variables & handling outliers.
<br>
**Model**- build! the! model!
<br>
**Assess**- Think reliability, think accuracy.

## Data Understanding
This is typically the first step in the predictive modelling process. During this stage, the summary statistics are computed, trends are examined, & visualisations made. These actions will prove to be helpful in later stages where problems like missing values or outliers have to be identified & handled appropriately.

### Normal Distribution
aka Gaussian Distribution

- Symmetric
- mean = median = mode


- **68%** lies within **1** σ of μ
- **95%** lies within **2** σ of μ
- **99.7%** lies within **3** σ of μ

## Data Preparation
In this stage, the dataset is cleansed & feature transformation can take place.

### Outliers
- **+/-**  **3** σ from μ
- < Q1 - 1.5 IQR || > Q3 + 1.5 IQR


- types of outliers
  - **single-dimensional**- fit the bill, for ONE variable
  - **multi-dimensional**- fit the bill, for SEVERAL variables

- handling outliers
  - **remove**- please only do this if it's fine to ignore entire data records
  - **Outlier Model**- you might be short of data for this. If so, feel free to loosen the definition of outliers to anything outside of 2 σ from μ.
  - **Feature Scaling**- use that min-max normalisation!
  - **Binning**- note that this is very effective when used, but can only be used if it doesn't affect the record's credibility & or validity.
  - Life's short, **leave 'em**.

### Missing Values
That's it. Empty cells.

- handling missing values
  - delete the row
  - delete the column (if it's not relevant to the project objective)
  - impute with a constant (e.g. mean, median)

### Feature Scaling Methods (numeric variables)
- log transform
  - range (0, ∞)
  - fixes positively skewed data
- sigmoid
  - for categorical target variables
- min-max normalisation
  - for continuous target variable
- z-score
- power transform
  - fixes negatively skewed data

### Data Sampling Methods
Splitting the data into 2 chief sets- the training set & the testing set. You know what they do.

- **Simple Split** <br>
  Definitely the most common way of splitting data. Data is randomly selected (without replacement) to form the training & testing sets. Is typically a **70/30** split.

# Predictive Modeling I

## Linear Regression
Used to predict a **continuous** target variable. For example- salary, age, distance between two points, etc. Are also known as **estimators** or **regression models**. A linear regression is, essentially, the best fit linear equation that graphs the output of the target variable with respect to the input variable(s).

Regression models exhibit **supervised learning**, the facet of machine learning where models learn an algorithm by training with a set of data that forms the ground truth.

```
y = b₀ + b₁x₁ + b₂x₂ + ... + b𝑛x𝑛
```

### R-squared Value
A metric commonly used with linear regressions to determine the accuracy of the regression model. The r-squared value lies between 0 & 1, where an r-squared value of 0 indicates a lack of correlation whereas an r-squared value of 1 indicates a completely dependent relation.

Any r-squared value **.7 & above** is indicative of a **strong relationship**.


## Model Assessment
We can build models that attempt to predict certain target variables. Naturally, we want to have a set of features (that have been tried & tested) that can give us an accurate representation of our model's accuracy.

- **Predictive Accuracy**- A quantitative assessment that indicates a model's predictive ability.
- **Speed**- In model building as well as in making predictions.
- **Robustness**- Against missing/ noisy/ erroneous data.
- **Scalability**- How does the model handle large amounts of data?
- **Interpretability**- In terms of the ease of understanding of the model.

In this module, we focus on assessing a model through its predictive accuracy. To accomplish this, we make use of 2 specific **assessment methodologies**.

1. **Simple Split**- Split the data into 2 sets (a training set & a testing set). The split is typically a **70/30** split.
1. **k-fold Cross Validation**- Split the data into k (mutually exclusive) subsets. Conduct the training k times, rotating the subset to be used as the testing set. Then, attain predictive accuracy as an aggregation of the k sets of test results.
