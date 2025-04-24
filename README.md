
 #Table of contents 
 
 ![Image](https://github.com/user-attachments/assets/f00a1d24-3eab-47b4-b8ae-ed7864805b8e)

 
 # Evaluation of Dataset Suitability for Linear Regression

<h3>Introduction<h3>

<p><h4>(Andrea and Sarah, 2016) showed that linear regression is a statistical model that is used to model the connection between a dependant variable and one or more independent variables by fitting a linear equation to the data that is observed. (Andrea and Sarah, 2016) showed that the primary assumption of linear regression involves linear relationship between variables, independence of errors, normality of errors as well as the homoscedasticity. This report assesses the given dataset for its suitability for implementing a linear regression algorithm by examining its data types, quality as well as potential issues.</h4> </p></p>

<h3>Data Types and Relevance </h3>

<p><h4>We are given a dataset for medical aid scheme in South Africa. The datasets are composed of a mix of numerical, as well as categorical features. The numerical features include age, children, and charges, and they are fundamentally suitable for linear regression as they represent continuous quantities. The dependant variable is the charges. charges are also numerical which makes it appropriate to predict using the model. The features that are categorical which are sex, smoker, and region needs a pre-processing to be use utilized in a linear regression model. For example, age is expected to have a corelation that is positive with charges, as older people may experience higher medical costs. The same way BMI can influence medical expenses due to the health risks that are associated, and smoker status is a strong predictor of the increased healthcare costs. </h4></p>


<h3>Data Quality Assessment</h3>

<p><h4>According to the first analysis of the dataset that is provided, there are no missing values. Andrea and Sarah, 2016) showed that in order to ensure data integrity, a comprehensive check for the complete data set is essential. Andrea and Sarah, 2016) showed that the imputation methods like mean or median imputation or even more complex methods like K-nearest neighbours should be taken into consideration if there is a discovery of any missing values. Finding outliers is also important, particularly when it comes to features like age, BMI, as well as charges. Andrea and Sarah, 2016) showed that the regression line may be impacted inappropriately by the outliers, this could result into predictions that are not accurate. These outliers can be found and dealt with using box plot, as well as the z-score analysis. Evaluating the charges verified distribution is also necessary. It should ideally appear like a normal distribution. It is also important to assess whether multicollinearity exists among the numerical features. A correlation matrix can assist in identifying variables that are highly correlated, which may require feature selection or dimensionality reduction techniques. </h4></p>

<h3>Common Pitfalls and Considerations </h3>

<p><h4>The variables that are categorical (sex, smoker, and region) needs the encoding to be utilized in linear regression model. Andrea and Sarah, 2016) showed that One-hot encoding is a very suitable method in order to convert these categorical features into representations that are numerical without introducing ordinal relationships. while linear regression assumes a relationship that is linear between variables, it is also important to appreciate that some relationships can happen to not be linear. Andrea and Sarah, 2016) showed that if there is a violation of the linear assumption, exploring other models that are non-linear could potentially improve prediction accuracy. The region variable may capture underlying socio access differences that influence medical charges. During the feature selection and model interpretation, these features should be considered. Moreover, ethical consideration needs to be addressed when the model is used for decision making. Possible sex, geographic, or smoking-related biases might deliver unfair or results that are discriminating. </h4></p>


<h3>Conclusion</h3>  

<p><h4>In conclusion, the dataset is suitable to implement a linear regression algorithm with pre-processing that is appropriate. Andrea and Sarah, 2016) showed that the numerical features are aligning with the requirements of the model, and categorical features can also be transformed by utilizing techniques of encoding.</h4></p>

 # Planning Analysis Report
 
<h3>Introduction </h3> 
 
<p><h4>This section contains a detailed, and a comprehensive plan for conducting a linear regression analysis in order to predict medical charges based on the lifestyle as well as demographic factors. The main objective is to make sure that all aspects of the data analysis process are considered carefully and closely executed to develop a model that is accurate and effective.  </h4></p> 

<p><h4><h3>a)Exploratory Data Analysis (EDA):</h3>   
 
<h4>Data Loading and Inspection: </h4>
<h4>(Andrea and Sarah, 2016) showed that the datasets that are provided will be loaded using pandas on vs code, this will be followed by the inspection of data types. (.info ()), then there will be a summary of descriptive statistics (. describe ()), then an examination of the values that are missing.  </h4></p> 

<p><h4>Data Cleaning: </h4>
<h4>(Andrea and Sarah, 2016) showed that if there are any missing values, they will be dealt with using imputation methods that are appropriate, these methods include mean or median for features that are numerical, and mode for those that are categorical. If there are any outliers, they will be identified and addressed using box ploys and z-score analysis, maybe by transforming values. Rows that are duplicate will be removed to ensure data integrity.  
</h4></p>
<p><h4>data Visualization: </h4>
<h4>(Andrea and Sarah, 2016) showed that in order to visualise the relationships between variables I will implement seaborn and matplotlib. Also, the scatter plots will be implemented to illustrate the correlation between the features that are numerical and charges. The distribution of features that are numerical will be shown using distribution plots and histograms. In order to estimate the multicollinearity among numerical predictors, there will be a creation of correlation matrix (heatmap). </p></h4> 
 
 
<h3> b)Feature Selection:  </h3>
 
<p><h4>(Andrea and Sarah, 2016) showed that Feature selection is important because it ensures that there is an inclusion of the variables that are most relevant and non-redundant in the regression model.  
Correlation matrix: (Andrea and Sarah, 2016) showed that this will visualise pairwise correlations between features and the variable targeted.  
Variance Inflation Factor (VIF):  this will Check for multicollinearity as well as getting rid of highly correlated features if there is a need. 
Backward Elimination: I will then utilize the p-values from an Ordinary Least Squares (OLS) regression summary to iteratively remove features that are less significant. </h4></p>

<h3>c)Training the model:</h3>  

<p><h4>(Andrea and Sarah, 2016) showed that after the preparation of the features and their selection, the model training will then start:  
Train-Test Split: I will separate the dataset into training and testing sets using an 80/20 ratio for evaluation to be fair.  
Linear Regression Model: I will utilize the Linear Regression from sklearn. linear model to fit the model on the training data. 
Model performance: the performance of the model will be assessed using metrics such as mean squared error, and R-squared. Cross validation (k-fold) will be implemented to evaluate the robustness of the model and also prevent overfitting. </h4> </p> 

<h3>d) Interpret and evaluate model:  </h3>

<p><h4>(Andrea and Sarah, 2016) showed that after the training of the model, there will be an assessment of the model and interpretation to determine how well it predicts charges: 
The evaluation metrics are as follows:  
<ol>Mean Absolute Error (MAE) </ol>
<ol>Mean Squared Error (MSE) </ol>
<ol>Root Mean Squared Error (RMSE) </ol>
<ol>R² Score to measure the explanatory power of the model. </ol>
Predicted vs. Actual Plot: Visualize how closely the charges that are predicted match the actual charges. 
Residual Analysis: Plot residuals to check for constant variance and normal distribution of errors. 
Interpret Coefficients: Explain how each feature affects the predicted cost (for example, being a smoker increases charges by X units).</h4> </p>
 
<h3>e) Report Writing   </h3>

<h4>(Andrea and Sarah, 2016) showed that after the analysis, I will then make clear and a 
straightforward report that has the following subheadings:  
<ol>•	A dataset overview and the initial data inspection  </ol>
<ol>•	An EDA steps explanation, this will include visual findings. </ol> 
<ol>•	Feature selection details as well as justification </ol>
<ol>•	An explanation of the used regression model, training process as well as validation.  </ol>
<ol>•	Metrics evaluation, visual results as well as the model accuracy interpretation </ol>
<ol>•	Conclusions as well as insights of how the medical aid scheme can use the model to personalise the strategies for pricing.</ol>
<ol>•	References at the end  </ol></h4>


 



# Report Section
<h3>Introduction</h3>

<p><h4> In this report, a linear regression algorithm is used to present an accurate analysis and prediction of medical insurance charges.  The purpose of this is to understand the relationships between personal attributes as well as lifestyle for example age, BMI, smoking etc, and the collected medical charges.  This analysis adheres to the structured pipelines that involves data pre-processing, EDA which is exploratory data analysis, feature selection, model building, last but not least and the evaluation. The IDE used for this analysis is VS code, and the coding language used is python in a VS code Jupiter notebook.   </h4></p>

<h1>Libraries used</h1>

![Image](https://github.com/user-attachments/assets/c3d0f657-a0a4-401f-a778-d405c714e0e0) 

<p><h4>In this coding analysis, there are libraries that were used, and these libraries are:
<ol>•Pandas and NumPy, - this one is used for numerical operation and data manipulation </ol>
<ol>•Matplotlib and seaborn - this library is used for the visualization of data. </ol>
<ol>•Script.stats – this uses Z-score to detect outliers </ol>
<ol>•Statsmidels – this is for the calculation of multicollinearity using the variance inflation factor (VIF)</ol>
<ol>•Sklearn – that is used for development and evaluation of machine learning and evaluation. </ol>  </h4></p>

<h1>Dataset overview </h1>  

![Image](https://github.com/user-attachments/assets/a32879e4-a4d6-4600-bf55-0425409fad44)

<p><h4>Insurance.csv is the dataset that was provided and used in this analysis, it has the following features:
<ol>•	Age: the age of a beneficiary </ol>
<ol>•	Sex: which is the gender of the beneficiary </ol>
<ol>•	BMI: body mass index </ol>
<ol>•	Children: this represents the number of dependents </ol>
<ol>•	Smoker: the status of smoking, “smoker or no smoker”</ol>
<ol>•	Region: the area of residential in the US</ol>
<ol>•	Chargers: the medical insurance cost (target variable)</ol>
The dataset was successfully loaded, and the rows were printed in order to inspect the structure of the data. The number of rows entirely is 1338. 
</h4></p>

<h1>Data pre-processing </h1>  
<h3>a)Encoding and categorical variables </h3>
<h4>For model complexity, categorical variables were encoded. These variables are:</h4>
<h4>•	Sex and smoker – these were binary encoded.</h4>
<h4>•	Region was one-hot encoded with drop first = true, this was done to avoid dummy variable trap. </h4>

<h3>b)	Missing variables and data types </h3>
<h4>the next step was to check for any missing values and found that there were no missing values in the data. All the data types were good for the analysis. </h4>
<h3>c)	Duplicate rows:</h3>
<h4>•	We found 1 duplicate row, and that row was then dropped or removed, and the new structure or number of rows is now 1337. </h4>
<h3>d)	Outlier detection and removal </h3>
<h4>•	To detect outliers, the Z-score method was implemented on the numerical columns (age, children, and charges). The entries what had the Z-score of greater than 3 were removed. </h4>
<h4>•	The total of outliers removed is 29 rows</h4>
<h4>•	The new shape of the dataset is now (1308, 7)
</4>


<h1>Exploratory Data Analysis</h1>  

<h3>-Distribution Plots </h3>

![Image](https://github.com/user-attachments/assets/23f37e21-0831-4e0b-9106-7232f113c870)

![Image](https://github.com/user-attachments/assets/4ad4ce58-7796-4ead-b679-d9bd6a483334)

![Image](https://github.com/user-attachments/assets/3f76e36a-4fa3-44a7-aefa-1a49f8a33bd3)

![Image](https://github.com/user-attachments/assets/4a1c1ff1-497a-4baf-b87a-bd2ef5ba3123)

<h4>•	For each numerical value, Histograms and KDE plots were plotted.</h4>
<h4>•	Age, BMI, Children as well as charges showed different degrees of skewness</h4>

<h3>-Scatter plots </h3>

![Image](https://github.com/user-attachments/assets/f9d16bc6-5e92-492d-a6f1-0c73420ba0a1)

![Image](https://github.com/user-attachments/assets/076407d1-ddcb-4f4d-a857-7366dd4893b0)

![Image](https://github.com/user-attachments/assets/3ecbce5b-26c9-4ab1-bba1-3ed91a2b6532)

<h4>Scatter plots were created to show the relationship between:</h4>
<h4>•	Age, BMI, as well as children vs chargers, with smokers highlighted </h4>
<h4>•	There is a strong positive trend observed for smokers more especially in BMI vs charges </h4>

<h3>-Box Plots </h3>

![Image](https://github.com/user-attachments/assets/adbef1e5-a7cf-4976-8e01-7eca2daec17f)

![Image](https://github.com/user-attachments/assets/ee79af82-02f0-4d5b-922f-fe4e0150f568)

![Image](https://github.com/user-attachments/assets/19fcf778-7961-4178-b51f-e712199da77d)

<h3>The implementation of box plots grouped charges by:</h3>
<h4>•	Smoker, sex, and region</h4>
<h4>•	Smokers had higher charges </h4>

<h4>-Correlation heatmap </h4>

![Image](https://github.com/user-attachments/assets/d60b7a3c-3938-481a-8a7b-cb9a207b8581)

<h4>•	The correlation matrix displayed a strong correlation between smoker and charges </h4>
<h4>•	It also displayed a moderate correlation between the age and charges </h4>


<h1>Feature selection </h1>  

<h4>The features that most correlated with charges are:</h4>
<h4>•	Smoker </h4>
<h4>•	Age </h4>
<h4>•	Bmi </h4>
<h4>VIF analysis as well as model training were influenced by these observations.</h4>

<h1>Multicollinearity Check (VIF)</h1>  

<h4>Variance Inflation Factor (VIF) was calculated:</h4>  
<h4>•	All features showed VIF values within acceptable limits (<10).</h4>
<h4>•	No strong multicollinearity was detected.</h4>
  
<h3>Model Training </h3>

<h4>•	Separation/splitting of data, the datasets split into 80% training and 20% testing sets.</h4>
<h4>•	The training data was used to initialize as well as train a linear regression model.</h4>
<h4>•	Model trained successfully without error.
</h4>
  
<h3>Model Evaluation</h3> 
<h4>There were predictions that were made on the test set. </h4>  
<h3> Evaluation Metrics</h3>


| Metric | Value | 
| - | :- | 
| Mean absolute error (MAE) | 3969,03 |
| Mean square error (MSE) | 30444091,53 | 
| Root Mean Square (RMS) | 5517,62 |
| R² Score | 0,78 |

<h3> Cross-validation</h3>
<h4>5-fold cross-validation was performed.</h4>
<h4>Average R² Score: 0,7503</h4>
<h4>This shows consistency and generalizability of the model.</h4>

 <h3>Visualization of Results</h3>
<h4>Actual vs Predicted Charges</h4> 
<h4>Scatter plot showed the relationship between actual and predicted values.</h4>
<h4>•	Data points close to the diagonal line indicate a good fit.</h4>

<h1>Residual Analysis</h1>
<h4>•	Histogram of residuals showed a roughly normal distribution.</h4>
<h4>•	Residuals vs predicted plot showed randomness around zero, suggesting linear model appropriateness.</h4>


<h1>Introduction</h1>
<p><h4>The linear regression model provides a strong predictive performance for medical insurance charges. Among the predictors, smoking status, age, and BMI have the most significant influence on charges. The model performed well with a reasonably high R² score and acceptable error metrics. This analysis highlights the value of lifestyle attributes in predicting healthcare costs, which could be useful for healthcare providers and insurance companies to assess risk and set premiums.</h4></p>









