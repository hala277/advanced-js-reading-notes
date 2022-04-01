# AWS: API, Dynamo and Lambda

## AWS API Gateway Overview 

**What is Amazon API Gateway?**

Amazon API Gateway is a managed service that lets developers define the HTTP endpoints of a REST API or a WebSocket API and connect them to the backend business logic. It also supports API request authentication, access control, monitoring, and tracing.

**How does API Gateway work?**

API Gateway sits between your API's backend services and its users, processing HTTP requests to API endpoints and sending them to the appropriate backends. It comes with a suite of tools to assist you in managing your API definitions and mappings between endpoints and backend services. It can also generate API references from your definitions and provide them as API documentation to your users.

AWS Lambda, AWS SNS, AWS IAM, and Cognito Identity Pools are just a few of the AWS services that API Gateway connects with. These interfaces enable completely managed authentication and authorisation layers, as well as thorough API request analytics and tracking.

![API Gateway](https://assets-global.website-files.com/60acbb950c4d66d0ab3e2007/614dc8866ca06e6d1740ca01_amazon-api-gateway-guide-1.png)

**What makes API Gateway such an important component of the Serverless ecosystem?**

API Gateway is the component of the Serverless ecosystem that connects Serverless functions with API specifications. The ability to execute a Serverless function directly in response to an HTTP request is the primary reason why API Gateway is so useful in Serverless setups: it allows web applications to have a completely serverless architecture. When you combine API Gateway with other AWS services, you can create a fully functional customer-facing web application without having to manage a single server.
The benefits of the serverless architecture, such as scalability, easy maintenance, and low cost due to little overhead, are now available to popular online applications.

**What other AWS services does API Gateway integrate with?**

Amazon API Gateway is compatible with a variety of AWS services, including:

+ AWS Lambda: create HTTP API responses using Lambda functions.
+ AWS SNS: When an HTTP API endpoint is accessed, broadcast SNS notifications.
+ Amazon Cognito: provide HTTP API authentication and authorization.

**API Gateway allows direct integrations that can be configured through the API Gateway user interface (or using the API Gateway's own API):**

+ Calling a Lambda function on AWS.
+ Calling a different HTTP endpoint, either with or without VPC Link.
+ Using the API of any AWS service that has an HTTP API to make an HTTP call.
+ Using API Gateway to build a mock answer without having to call out to other services.

## AWS API Gateway

The Amazon API Gateway service is a fully managed service that allows developers to easily construct, publish, maintain, monitor, and protect APIs at any size. APIs allow applications to access data, business logic, and functionality from your backend services through a "front door." RESTful APIs and WebSocket APIs can be created with API Gateway to enable real-time two-way communication applications. Web applications, as well as containerized and serverless workloads, are supported by API Gateway.

API Gateway handles traffic management, CORS support, authorization and access control, throttling, monitoring, and API version management, as well as other responsibilities involved in accepting and processing hundreds of thousands of concurrent API calls. There are no minimum fees or initial costs with API Gateway. You pay for the API calls you receive and the data you send out, and you can save money by using the API Gateway's tiered pricing model as your API usage grows.

### API Types
+ RESTful APIs
+ WEBSOCKET APIs

**How API Gateway Works**
![How API Gateway Works](https://d1.awsstatic.com/serverless/New-API-GW-Diagram.c9fc9835d2a9aa00ef90d0ddc4c6402a2536de0d.png)

## AWS DynamoDB Guide

**What is DynamoDB?**

Amazon Web Services' DynamoDB is a hosted NoSQL database (AWS.It has the following features:

1. Consistent performance as the system grows.
2. a managed experience, which eliminates the need to SSH into servers to upgrade crypto libraries.
3. a modest, straightforward API that allows for basic key-value access as well as more complex query patterns.

**DynamoDB is especially well-suited to the following scenarios:**

1. Data-intensive applications with strict latency constraints. JOINs and complex SQL operations might slow down your queries as the amount of data you have grows. Your queries will have predictable latency using DynamoDB, even if they are large, up to 100 TBs!

2. AWS Lambda-based serverless applications. In reaction to event triggers, AWS Lambda provides auto-scaling, stateless, ephemeral compute. DynamoDB is a wonderful fit for constructing Serverless applications because it has an HTTP API and uses IAM roles for authentication and permission.

3. Data sets having well-known and easy access patterns. DynamoDB's straightforward key-value access patterns make it a fast and reliable solution for creating and serving recommendations to users.

## AWS DynamoDB
Fast, flexible NoSQL database service for single-digit millisecond performance at any scale

**How it works**
Amazon DynamoDB is a serverless, fully managed key-value NoSQL database built to run high-performance applications at any size. Built-in security, continuous backups, automated multi-Region replication, in-memory cache, and data export tools are all features of DynamoDB.

![AWS DynamoDB](https://d1.awsstatic.com/product-marketing/DynamoDB/product-page-diagram_Amazon-DynamoDB.a8a97936b804de5abb83fec9329acd03dec33332.png)

## Dynamoose
Dynamoose is a modeling tool for Amazon's DynamoDB. Dynamoose is heavily inspired by Mongoose, which means if you are coming from Mongoose the syntax will be very familar.

## resources
+ [AWS API Gateway Overview](https://www.serverless.com/amazon-api-gateway)
+ [AWS API Gateway](https://aws.amazon.com/api-gateway/)
+ [AWS DynamoDB Guide](https://www.dynamodbguide.com/what-is-dynamo-db/)
+ [AWS DynamoDB](https://aws.amazon.com/dynamodb/)
+ [Dynamoose](https://dynamoosejs.com/getting_started/Introduction)