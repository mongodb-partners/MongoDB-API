# Data API Alternative

This repository contains a way to use Data API using the same API spec as Data API

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