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

In AWS, we have published a serverless application that will help you deploy a stack required to replicate Data API services in your environments. You can find the detailed steps for deployment [here](/AWS/README.md).