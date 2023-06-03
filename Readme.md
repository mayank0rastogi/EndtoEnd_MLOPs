#### End to END Machine Learning Workflow using github actions(CI/CD), Github Self-Hosted(app runner) and AWS-ECR(for the docker image) and EC2 to deploy my machine learnig Flask Application/Rest endpoint into the Ec2 instance

### Approach of the Project:

#### Data Ingestion :
    1) In Data Ingestion phase the data is first read as csv.
    2) Then the data is split into training and testing and saved as csv file.
    
#### Data Transformation :
    1) In this phase a ColumnTransformer Pipeline is created.
    2) For Numeric Variables first SimpleImputer is applied with strategy median , 
       then Standard Scaling is performed on numeric data.
       for Categorical Variables SimpleImputer is applied with most frequent strategy, 
    3) then ordinal encoding performed , after this data is scaled with Standard Scaler.
    4) This preprocessor is saved as pickle file.
    
#### Model Training :
    1) In this phase base model is tested . The best model found was catboost regressor.
    2) After this hyperparameter tuning is performed on catboost and knn model.
    3) This model is saved as pickle file.
    
#### Prediction Pipeline :
    1) This pipeline converts given data into dataframe and has various functions to load 
       pickle files and predict the final results in python.
    
#### Flask App/REST Endpoint creation :
    2) Flask app is created with User Interface to predict the gemstone prices inside a Web Application.

