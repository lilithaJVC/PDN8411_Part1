# PDN8411_Part1
<h1>Introduction</h1>

<p><h3> In this report, a linear regression algorithm is used to present an accurate analysis and prediction of medical insurance charges.  The purpose of this is to understand the relationships between personal attributes as well as lifestyle for example age, BMI, smoking etc, and the collected medical charges.  This analysis adheres to the structured pipelines that involves data pre-processing, EDA which is exploratory data analysis, feature selection, model building, last but not least and the evaluation. The IDE used for this analysis is VS code, and the coding language used is python in a VS code Jupiter notebook.   </h3></p>

<h1>Libraries used</h1>

<p><h4>In this coding analysis, there are libraries that were used, and these libraries are:
<ol>•Pandas and NumPy, - this one is used for numerical operation and data manipulation </ol>
<ol>•Matplotlib and seaborn - this library is used for the visualization of data. </ol>
<ol>•Script.stats – this uses Z-score to detect outliers </ol>
<ol>•Statsmidels – this is for the calculation of multicollinearity using the variance inflation factor (VIF)</ol>
<ol>•Sklearn – that is used for development and evaluation of machine learning and evaluation. </ol>  </h4></p>

<h1>Dataset overview </h1>  

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
<h4>a)Encoding and categorical variables </h4>
<h4>For model complexity, categorical variables were encoded. These variables are:</h4>
<h4>•	Sex and smoker – these were binary encoded.</h4>
<h4>•	Region was one-hot encoded with drop first = true, this was done to avoid dummy variable trap. </h4>

<h3>b)	Missing variables and data types </h3>
<h4>the next step was to check for any missing values and found that there were no missing values in the data. All the data types were good for the analysis. </h4>
<h4>c)	Duplicate rows:</h4>
<h4>•	We found 1 duplicate row, and that row was then dropped or removed, and the new structure or number of rows is now 1337. </h4>
<h3>d)	Outlier detection and removal </h3>
<h4>•	To detect outliers, the Z-score method was implemented on the numerical columns (age, children, and charges). The entries what had the Z-score of greater than 3 were removed. </h4>
<h4>•	The total of outliers removed is 29 rows</h4>
<h4>•	The new shape of the dataset is now (1308, 7)
</4>


<h1>Exploratory Data Analysis</h1>  

<h3>-Distribution Plots </h3>
<h4>•	For each numerical value, Histograms and KDE plots were plotted.</h4>
<h4>•	Age, BMI, Children as well as charges showed different degrees of skewness</h4>

<h3>-Scatter plots </h3>
<h4>Scatter plots were created to show the relationship between:</h4>
<h4>•	Age, BMI, as well as children vs chargers, with smokers highlighted </h4>
<h4>•	There is a strong positive trend observed for smokers more especially in BMI vs charges </h4>

<h3>-Box Plots </h3>
<h3>The implementation of box plots grouped charges by:</h3>
<h4>•	Smoker, sex, and region</h4>
<h4>•	Smokers had higher charges </h4>

<h4>-Correlation heatmap </h4>
<h4>•	The correlation matrix displayed a strong correlation between smoker and charges </h4>
<h4>•	It also displayed a moderate correlation between the age and charges </h4>


<h1>Feature selection </h1>  

<h4>The features that most correlated with charges are:</h4>
<h4>•	Smoker </h4>
<h4>•	Age </h4>
<h4>•	Bmi </h4>
<h4>VIF analysis as well as model training were influenced by these observations.</h4>


