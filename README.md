# PGDDS-Capstone-Project
Credit Card Fraud Detection Project

# Problem Statement:  
The problem statement chosen for this project is to predict fraudulent credit card transactions with the help of machine learning models.  

In this project, you will analyse customer-level data which has been collected and analysed during a research collaboration of Worldline and the Machine Learning Group.   
The dataset is taken from the Kaggle website (https://www.kaggle.com/mlg-ulb/creditcardfraud) and it has a total of 2,84,807 transactions, out of which 492 are fraudulent. Since the dataset is highly imbalanced, so it needs to be handled before model building. 

# Business Problem Overview:  
For many banks, retaining high profitable customers is the number one business goal. Banking fraud, however, poses a significant threat to this goal for different banks. In terms of substantial financial losses, trust and credibility, this is a concerning issue to both banks and customers alike.  

It has been estimated by Nilson report(https://nilsonreport.com/upload/content_promo/The_Nilson_Report_Issue_1164.pdf) that by 2020 the banking frauds would account to $30 billion worldwide. With the rise in digital payment channels, the number of fraudulent transactions is also increasing with new and different ways.   
 
In the banking industry, credit card fraud detection using machine learning is not just a trend but a necessity for them to put proactive monitoring and fraud prevention mechanisms in place. Machine learning is helping these institutions to reduce time-consuming manual reviews, costly chargebacks and fees, and denials of legitimate transactions.  

# Understanding and Defining Fraud :    

Credit card fraud is any dishonest act and behaviour to obtain information without the proper authorization from the account holder for financial gain. Among different ways of frauds, Skimming is the most common one, which is the way of duplicating of information located on the magnetic strip of the card.  Apart from this, the other ways are:    
•	Manipulation/alteration of genuine cards  
•	Creation of counterfeit cards  
•	Stolen/lost credit cards  
•	Fraudulent telemarketing  

# Data Dictionary:  
  
The data set includes credit card transactions made by European cardholders over a period of two days in September 2013. Out of a total of 2,84,807 transactions, 492 were fraudulent. This data set is highly unbalanced, with the positive class (frauds) accounting for 0.172% of the total transactions. The data set has also been modified with Principal Component Analysis (PCA) to maintain confidentiality. Apart from ‘time’ and ‘amount’, all the other features (V1, V2, V3, up to V28) are the principal components obtained using PCA. The feature 'time' contains the seconds elapsed between the first transaction in the data set and the subsequent transactions. The feature 'amount' is the transaction amount. The feature 'class' represents class labelling, and it takes the value 1 in cases of fraud and 0 in others.  

# Project Pipeline:  

The project pipeline can be briefly summarized in the following four steps:    
**•	Data Understanding:** Here, you need to load the data and understand the features present in it. This would help you choose the features that you will need for your final model.  
**•	Exploratory data analytics (EDA):** Normally, in this step, you need to perform univariate and bivariate analyses of the data, followed by feature transformations, if necessary. For the current data set, because Gaussian variables are used, you do not need to perform Z-scaling. However, you can check if there is any skewness in the data and try to mitigate it, as it might cause problems during the model-building phase.  
**•	Train/Test Split:** Now you are familiar with the train/test split, which you can perform in order to check the performance of your models with unseen data. Here, for validation, you can use the k-fold cross-validation method. You need to choose an appropriate k value so that the minority class is correctly represented in the test folds.  
**•	Model-Building/Hyperparameter Tuning:** This is the final step at which you can try different models and fine-tune their hyperparameters until you get the desired level of performance on the given dataset. You should try and see if you get a better model by the various sampling techniques.  
**•	Model Evaluation:** Evaluate the models using appropriate evaluation metrics. Note that since the data is imbalanced it is is more important to identify which are fraudulent transactions accurately than the non-fraudulent. Choose an appropriate evaluation metric which reflects this business goal.

*** Model deployment Plan:** 
Here’s the step-by-step plan to deploy credit card fraud detection model using **Streamlit**:

### **1. Environment Setup**
   1. Install Streamlit and required libraries like `xgboost`, `scikit-learn`, `pandas`, and `numpy`.
   2. Load your pre-trained model (`.pkl` file) in the Python environment.

### **2. Create the Streamlit App**
   1. Design a simple user interface (UI) using Streamlit to accept transaction details (e.g., amount, cardholder age, etc.).
   2. Set up a function to load the model and use it for making predictions based on the user input.
   3. Add a button to trigger the prediction process and display the results (e.g., "Fraud Detected" or "Legitimate Transaction").
   4. Incorporate any preprocessing steps used during training (e.g., scaling or encoding).

### **3. Test the App Locally**
   1. Run the Streamlit app locally to verify that the UI works correctly and the model returns accurate predictions.
   2. Test various scenarios to ensure that the app behaves as expected.

### **4. Deploy the Streamlit App**
   - **Option 1: Deploy on Streamlit Cloud**
     1. Push the app code to a GitHub repository.
     2. Use **Streamlit Cloud** to directly deploy from GitHub by linking your repository.
   
   - **Option 2: Deploy on Custom Server**
     1. Set up a server or cloud VM (e.g., AWS, GCP, or Heroku) with Python and required dependencies.
     2. Run the Streamlit app on the server and expose it to a public URL.

   - **Option 3: Dockerize the App**
     1. Create a Dockerfile to package the app and its dependencies.
     2. Build and deploy the Docker container in a containerized environment (e.g., Docker, Kubernetes).

### **5. Monitor and Maintain**
   1. Monitor the app for usage statistics, response times, and error rates.
   2. Regularly update the model or app as needed based on feedback, performance, or retrained models.
   3. Implement security measures for sensitive data and protect API endpoints if needed.






