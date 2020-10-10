# Operationalizing Machine Learning

One of the most important things is that **"DevOps"** refers to the collection of principles that allow getting software into production, or in this case, trained models. MLOps (Machine Learning Operations) is about applying DevOps best-practices and principles to machine learning operations.

In this project, I have used Azure to configure a cloud-based machine learning production model, deploy it, and consume it. This project demonstrates the procedure of creating, publishing, and consuming a pipeline.

![alt-text](backup/images/flow_diagram.png)

## Main Steps:
1. Authentication
2. Automated ML Experiment
3. Deploy the best model
4. Enable logging
5. Swagger Documentation
6. Consume model endpoints
7. Create and publish a pipeline
8. Documentation

## Architectural Diagram
![alt-text](backup/images/architecture_diagram.png)

## Key Steps
## Step 1: Automated ML Experiment
The aim of this step is to create an experiment using Automated ML, configure a compute cluster, and use that cluster to run the experiment.

#### Dataset
![alt-text](backup/images/image1.png)

#### Completion of experiment
![alt-text](backup/images/image2.png)

#### Selection of Best Model
![alt-text](backup/images/image3.png)

## Step 2: Deploy the Model
After the experiment run completes, deploying the Best Model will allow to interact with the HTTP API service and interact with the model by sending data over POST requests.

![alt-text](backup/images/image4.png)

## Step 3: Enable Application Insights
Once the Best Model is deployed, enable Application Insights and retrieve logs. Although this is configurable at deploy time with a check-box, it is useful to be able to run code that will enable it for us.

#### Check for Application Insights
![alt-text](backup/images/image5.png)

#### Running Logs script on terminal
![alt-text](backup/images/image7.png)

#### Log Dashboard
![alt-text](backup/images/image6.png)



## Step 4: Swagger Documentation
we are ready with the deployed model and enabled logs. Now it's time to test the REST APIs using Swagger. This provides a JSON file to test the get and post functionality of the Deployed API through which we will communicate with the model.

#### Swagger UI
![alt-text](backup/images/image8.png)
![alt-text](backup/images/image9.png)
![alt-text](backup/images/image10.png)

## Step 5: Consume Model Endpoints
Once we finish the test, it's time to consume the deployed model via Endpoints. In this step, we run a script, having scoring_uri and the key to match the key for our service and the URI that was generated after deployment. 

#### Result after consuming endpoint
![alt-text](backup/images/image11.png)

#### Apache benchmark
![alt-text](backup/images/image12.png)


## Step 6: Create, Publish and Consume a Pipeline
In the repo, you will see a Jupyter Notebook which we used for creating, publishing and consume pipeline.

