In some process models, Data Cleansing is a separate task, it is closely tied to Feature Creation but also draws findings from the Initial Data Exploration task. 

While tuning machine learning models, this deliverable asset is touched on a regular basis anyway because features need to be transformed to increase model performance. 

The following none exhaustive list gives you some guidelines:

·      Data types Are data types of columns matching their content? E.g. is age stored as integer and not as string?  

·      Ranges Does the value distribution of values in a column make sense? Use stats (e.g. min, max, mean, standard deviation) and visualizations (e.g. box-plot, histogram) for help  

·      Emptiness Are all values non-null where mandatory? E.g. client IDs  

·      Uniqueness Are duplicates present where undesired? E.g. client IDs  

·      Set memberships Are only allowed values chosen for categorical or ordinal fields? E.g. Female, Male, Unknown  

·      Foreign key set memberships Are only allowed values chosen as field? E.g. ZIP code  

·      Regular expressions Some files need to stick to a pattern expressed by a regular expression. E.g. a lower-case character followed by 6 digits  

·      Cross-field validation Some fields can impact the validity of other fields. E.g. a male person can’t be pregnant   


Feature Engineering
Feature Creation and Feature Engineering are some of the most important tasks in machine learning since they hugely impact model performance. 
Guidelines for feature transformation:

·      Imputing Some algorithms are very sensitive to missing values. Therefore, imputing allows for the filling of empty fields based on its value distribution  

·      Imputed time-series quantization Time series often contain streams with measurements at different timestamps. Therefore, it is beneficial to quantize measurements to a common “heartbeat” and impute the corresponding values. This can be done by sampling from the source time series distributions on the respective quantized time steps  

·      Scaling / Normalizing / Centering Some algorithms are very sensitive to differences in value ranges for individual fields. Therefore, it is best practice to center data around zero and scale values to a standard deviation of one  

·      Filtering Sometimes imputing values doesn’t perform well, therefore deletion of low-quality records is a better strategy  

·      Discretizing Continuous fields might confuse the model, e.g. a discrete set of age ranges sometimes performs better than continuous values, especially on smaller amounts of data and with simpler models 



Guidelines for feature creation:

 

·      One-hot-encoding Categorical integer features should be transformed into “one-hot” vectors. In relational terms this results in addition of additional columns – one columns for each distinct category  

·      Time-to-Frequency transformation Time-series (and sometimes also sequence data) is recorded in the time domain but can easily transformed into the frequency domain e.g. using FFT (Fast Fourier Transformation)  

·      Month-From-Date Creating an additional feature containing the month independent from data captures seasonal aspects. Sometimes further discretization in to quarters helps as well  

·      Aggregate-on-Target Simply aggregating fields the target variable (or even other fields) can improve performance, e.g. count number of data points per ZIP code or take the median of all values by geographical region

 As feature engineering is an art on itself, this list cannot be exhaustive. It’s not expected to become an expert in this topic at this point. Most of it you’ll learn by practicing data science on real projects and talk to peers which might share their secrets and tricks with you.  



Model Evaluation
Model evaluation is a critical task in data science. This is one of the few measures business stakeholders are interested in. Model performance heavily influences business impact of a data science project. 
 

Classification:

 

·      Confusion Matrix

·      Accuracy

·      Precision

·      Recall

·      Specificity

·      True positive rate

·      True negative rate

·      False positive rate

·      False negative rate

·      F1-score

·      Gain and Lift

·      Kolomogorov Smirnov

·      Area Under ROC

·      Gini Coefficient

·      Concordant – Discordant ratio

 

Regression:

 

·      Root Mean Squared Error (RMSE)

·      Mean Squared Error

·      Mean Absolute Error (MAE)

·      R-Squared

·      Relative Squared Error

·      Relative Absolute Error

·      Sum of Differences

·      ACF plot of residuals

·      Histogram of residuals

·      Residual plots against predictors

·      Residual plots against fitted values

 

 

Clustering:

 

·      Adjusted Rand index

·      Mutual Information

·      Homogeneity completeness

·      V-measure

·      Fowlkes-Mallows

·      Silhouette Coefficient Calinski-Harabaz¶

 
Model Deployment

Model deployment comes in many shapes. The key to everything is that the business insights that result from the model are made available to stakeholders. This can happen in various ways. At the simplest level a PDF report is generated (e.g. using a jupyter notebook in Watson Studio) and handed over to business stakeholders. Alternatively, the model is encapsulated behind a REST API and made either available to be consumed by a data product or sold internally or externally as a API (e.g. by using IBM Watson Machine Learning or Fabric for DeepLearning). 


 
