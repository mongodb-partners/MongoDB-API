# Data API Alternative

This repository contains a way to replicate MongoDB Data API in your respective cloud (AWS, GCP and Azure).

### Overview

This project leverages the Serverless Application Model (SAM) to create an alternative to the Python MongoDB Data API. It utilizes AWS Lambda for serverless functions and API Gateway for handling interactions. With this setup, you can seamlessly query your existing MongoDB Atlas Cluster using a connection string, just like you would with the MongoDB Data API.

The primary functionalities of this project include all the operations that you would do with the Data API:
1. findOne
2. find
3. insertOne
4. insertMany
5. updateOne
6. updateMany
7. deleteOne
8. deleteMany
9. aggregate

### AWS

In AWS, we have published a serverless application that will help you deploy a stack required to replicate Data API services in your environments.

#### Steps for deployment 

1) In your AWS account, go the [Lambda](https://us-east-1.console.aws.amazon.com/lambda/home?region=us-east-1#/functions) console. Click on the **Applications** section present on the right

![alt text](<images/Lambda_Applications.png>)

2) Click on **Create Application** present on the top right.

![alt text](<images/Create_Application.png>)

3) Select **Serverless application**

![alt text](<images/Serverless_Applications.png>)

4) Search for **MongoDB-DataAPI** in the search bar and check the box that says *Show apps that create custom IAM roles or resource policies*. Select the application highlighted.

![alt text](<images/DataAPI_App.png>)

5) Enter the name of the application, your MongoDB Atlas Cluster Connection Endpoint, check the acknowledgement box and click on **Deploy**.

![alt text](<images/App_Deployment.png>)

After you click on **Deploy**, AWS will initiate a cloudformation stack which will deploy the following resources for you: 
1. An HTTP API Gateway with IAM auth enabled
2. Custom IAM role that will provide API gateway the required access to invoke the Lambda function
3. A Lambda function that will act as a data resolver for your MongoDB Atlas Cluster
