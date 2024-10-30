# Final Project Instructions

## Deliverables
The final group project has three deliverables of equal value (each worth 10% of overall grade):

I. Paper

II. Code 

III. Presentation

## Components

### Research question

What are the most influential variables on the severity of accidents?

### Data

https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents/data

Size: 3.06 GB - 7.7 million rows, 46 columns

### Code Development

The code should be in Pyspark. In specific circumstances, python code may be admissible, but you must discuss this with the instructor first. If small parts of the code are in Python (e.g., reading into a pandas dataframe), this is fine. No other coding languages are admissible.

The code needs to be clearly written and documented in Jupyter notebooks (ipynb format). Please clearly describe what the code does at the top of each file. Additionally, place the code’s “task” in the filename.

For full credit (10 PTS), the code needs to include these sections in a clean, commented, and comprehensive manner:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. Data import and preprocessing (2 PTS) preprocessing include such tasks as imputing, binning, filtering, outlier treatment, feature engineering

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. Data splitting / sampling (1 PT) - sampling may not be needed, but splitting is a must

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. Exploratory data analysis, with at least 2 graphs (2 PTS) 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4. Model construction, with at least 3 models (3 PTS) ideally the models are constructed using pipelines 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5. Model evaluation (2 PTS) - this should include computation of relevant metrics, and a comparison between models 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4. Modeling using Machine Learning

A complete project will consider at least 3 models:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. A benchmark model, which is relatively simple. This could be a regression model with a small number of features (possibly a single feature). This provides a basis for comparison and a sanity check.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b. Two relatively more sophisticated models (e.g., random forest, gradient boosted tree). The best model found in your experiments is called the champion model.

The model construction process should follow the best practices covered in class, including:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Data preprocessing.  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The required steps will depend on the model, and could include:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i. Dummy variable construction

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ii. Feature scaling

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iii. Handling missing values and outliers

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iv. Handling semi-structured/unstructured data

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;v. Dimensionality reduction (e.g., PCA)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Data splitting (train/validation/test sets, for example). The test set should be left out for evaluation purposes. It should NOT be used in training.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;K-fold cross validation of hyperparameters


### Model Evaluation

For all appropriate models (benchmark, champion, and other relevant models), the following should be conducted:

#### a. Evaluate relevant metrics

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;For regression, this would include 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i.  R-squared

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;For classification, this would include:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i. accuracy

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ii. precision, recall, F1 score

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ii. confusion matrix

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iv. area under ROC curve (AUROC)

 
Depending on the application, additional evaluation could make sense such as lift charts

#### b. Sensitivity analysis

For your champion model, show relevant metrics for different hyperparameter values. This gives an idea of the model sensitivity.



 ## Project Presentation

One of the exciting things about being a data scientist is that they can drive major change at organizations. As a consequence, they can be called upon to communicate with executives. Strong communication skills (to a technical and non-technical audience) is critical. A presentation earning full points will be strong in Content, Organization/aesthetics, and Delivery. Each member must present a portion of the project.

Components of the presentation should include:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i. Executive summary: discuss the research question and what you have found

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ii. Data summary: explain the target (response) variable, the predictors, sampling, etc.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iii. Variable transformations and preprocessing

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iv. Models constructed (or planned to be constructed)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;v. Model performance

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;vi. Conclusions and future research



## Project Writeup

The project writeup should include the sections below.  It could make sense to divide the section writing among teammates; in that case, give the paper a final review for consistency.  The paper should be no more than 6 pages single-spaced. You can include tables and other artifacts in an appendix; these do not count toward the page limit.

Sections:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i. Abstract. Although the abstract appears first, it should be written last. This includes a quick introduction, an overview of what was done, and a summary of findings.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ii.  Data and Methods

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iii. Results

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iv. Conclusions. The conclusions section can include future work, if there was more time.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;v.  Contributions: List the contributions from each team member.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Eileanor:
- Created spark schema for main dataset
- Feature engineering of columns: day of week, weekday, month, season, rush hour, holiday, rain, snow
- Encoded categorical variables as needed (string index, one hot encoding)
- Checked for and removed nulls
- Checked for multicollinearity between day/night columns and weather columns - removed columns as needed
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Kaleigh: 
- Found main dataset
- EDA on POIs - correlation with each other, outliers, combining to form more valuable features
- Research on potential models to train (pros/cons)
- Checked correlation of features to target variable
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Layla: 
- Found zipcode-level demographic data, cleaned it, and merged it with the main dataset.



## Project GitHub Repo (recommended but not graded)

Each team member should put their project on their GitHub page. This should minimally consist of:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i. README.md page that summarizes the project: Purpose, major functionality, class methods 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ii. Organized code 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iii. A requirements.txt file listing the required packages



## Team and Teammate Evaluation

Each team member needs to make a substantial contribution and needs to be accountable. If a teammate issue cannot be resolved within the group, please notify the instructor. Students not contributing meaningfully to the project will not receive an A in the course.


