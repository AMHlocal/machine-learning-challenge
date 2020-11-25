# machine-learning-challenge

# Background
Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.
To help process this data, you will create machine learning models capable of classifying candidate exoplanets from the raw dataset.
In this homework assignment, you will need to:

Preprocess the raw data
Tune the models
Compare two or more models

# Preprocess the Data
To select the features to be used in the classifiers a decisition tree and random forest were ran, these files are included in the repository. After both were done the top ten features that came back from the random forest were chosen.

Once the features were chosen, MinMaxScaler was used to scale the numerical data. Data was then separated into training and testing data.

# Tune Model Parameters
GridSearch was used to tune the model parameters.
The classifiers tested were kNN and SVM.

# Methods
Machine Learning
Data Visualization

# Technologies Used
Python
Scikit-Learn
Pandas, Jupyter Notebook
Matplotlib

# Process
Preprocessed the dataset prior to fitting the models.
Scaled the numerical data.
Separated the data for training and testing.
Used GridSearchCV to hypertune the models and boost performance.
Tuned and compared multiple classifiers.

# Analysis
SVM model : Training Acc = 0.772 / Test (tuned) Acc = 0.851 
KNN model (k=13) : Training Acc = 0.887 / Test (tuned) Acc = 0.881

Both of theses models returned great test scored and were rather fast. However, with datasets that are larger or with more parameters used in their tests using SVM models can take longer and be more taxing on computer resources. 

Using the SVM model would be the recommendation to be used for classification of exoplanets since from the confusion matrix it was able to correctly classify more exoplanets than the KNN model (427 vs 412 in the KNN model). Both models were able to correctly classify 851 true negative pairs, they both were also able to avoid Type 1 errors but not Type 2 errors as both models misclassified 11 exoplanets. Basied off these measures using the SVM model would be better used if you have enough time and resources but if you need to classify quickly the KNN model will do it in almost half the time.

