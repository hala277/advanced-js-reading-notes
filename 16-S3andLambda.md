# AWS: S3 and Lambda

## AWS S3
**Amazon S3:** Object storage built to retrieve any amount of data from anywhere.

### How AWS S3 works?

Amazon S3 is an object storage service with industry-leading scalability, data availability, security, and performance. Customers of all sizes and sectors can store and protect nearly any amount of data for use cases including data lakes, cloud-native apps, and mobile apps. You can optimize expenses, organize data, and establish fine-tuned access restrictions to suit specific business, organizational, and compliance requirements with cost-effective storage classes and easy-to-use management tools.

![AWS S3](https://d1.awsstatic.com/s3-pdp-redesign/product-page-diagram_Amazon-S3_HIW.cf4c2bd7aa02f1fe77be8aa120393993e08ac86d.png)

### Use cases

+ Build a data lake
+ Back up and restore critical data
+ Archive data at the lowest cost
+ Run cloud-native applications

## AWS Lambda Basics

### What is AWS Lambda? 

AWS Lambda is an Amazon Web Services serverless computing service (AWS). AWS Lambda users write functions, which are self-contained applications written in one of the supported languages and runtimes, and upload them to AWS Lambda, which then executes them in a fast and flexible manner.

Lambda functions can be used to do everything from serving web pages to processing data streams to using APIs and connecting with other AWS services.

The term "serverless" computing alludes to the fact that you don't need to run these functions on your own servers. AWS Lambda is a fully managed service that handles all of your infrastructure requirements. As a result, "serverless" does not imply that no servers are involved; rather, it implies that the servers, operating systems, network layer, and other infrastructure have already been taken care of, allowing you to concentrate on writing application code.

### How does AWS Lambda work?


Each Lambda function runs in its own container. When the function is created, Lambda wraps it in a new container and runs that container in a multi-tenant cluster of AWS-managed machines. Before a function is executed, each function's container is allocated the required amount of RAM and CPU. When the function is executed, the initially allocated memory is multiplied by the  time it takes to execute the function. The customer is then billed based on the allocated memory and the execution time taken to execute the function. 
 AWS The entire infrastructure layer of  Lambda is managed by AWS. Customers don't get much insight into how the system works, but they don't have to worry about updating the underlying machines or avoiding network conflicts. -AWS handles itself. 

 Also, because the service is fully managed,  AWS Lambda can save  time on operational tasks. You can spend more time working on your application code, even if it means giving up the flexibility to run your own infrastructure because you don't have the infrastructure to maintain. 

 One of AWS Lambda's distinctive architectural properties  is the ability to run many instances of the same function or  different functions simultaneously from the same AWS account. In addition, concurrency can change based on time of day or  day of the week, and such changes are no different for Lambda. You will only be billed for the calculations used by the function. This makes AWS Lambda ideal for deploying highly scalable cloud computing solutions.

 ### When building Serverless applications, AWS Lambda is one of the main candidates for running the application code. Typically, to complete a Serverless stack you’ll need:

+ a computing service;
+ a database service; and
+ an HTTP gateway service.

## How to Get started with AWS Lambda

+ Creating AWS Lambda functions using the AWS console 
![Creating AWS Lambda function](https://assets-global.website-files.com/60acbb950c4d6606963e1fed/612494806458a3049f598360_image%2081.png)

+ Once in the Lambda management console, click Create Function:
![create function](https://assets-global.website-files.com/60acbb950c4d6606963e1fed/61249480fbc97926a04d56a7_image%2080.png)

+ Add a name for your new function and choose the desired runtime. After that, click “Create function” to confirm the settings:
![Add a name for the function](https://assets-global.website-files.com/60acbb950c4d6606963e1fed/61249511084c073ea39bb7ba_image%2082.png)

+ the function is created, and you can now work on the function code and deploy the function directly in the Lambda console.
![the function is created](https://assets-global.website-files.com/60acbb950c4d6606963e1fed/612494809482ad5f5b35552f_image%2083.png)

### Creating AWS Lambda functions using the Serverless Framework

1. Install Serverless Framework on your machine useing `$ npm install serverless -g`
2. Create a new service using `$ serverless`
3. Add the resources your function needs to the serverless.yml file.
4. Add code to your service.
5. Deploy to AWS by running the deploy step:`$ serverless deploy`

## AWS Lambda Functions
**AWS Lambda:** Run code without thinking about servers or clusters.

### How it works
AWS Lambda is a serverless, event-driven compute service that lets you run code for virtually any type of application or backend service without provisioning or managing servers. You can trigger Lambda from over 200 AWS services and software as a service (SaaS) applications, and only pay for what you use.

![AWS Lambda Functions](https://d1.awsstatic.com/product-marketing/Lambda/Diagrams/product-page-diagram_Lambda-RealTimeFileProcessing.a59577de4b6471674a540b878b0b684e0249a18c.png)

### Use cases:
+ Process data at scale 
+ Run interactive web and mobile backends
+ Enable powerful ML insights
+ Create event-driven applications

## Content Delivery Network (CDN)

A Content Delivery Network (CDN) is a geographically distributed group of servers that work together to provide fast delivery of Internet content. A CDN allows for the fast transfer of data needed for loading Internet content including HTML pages, javascript files, stylesheets, images, and videos.

![CDN](https://cyberhoot.com/wp-content/uploads/2020/03/What-is-Content-Delivery-Network-1024x647.jpg)

### resources
+ ![AWS S3](https://aws.amazon.com/s3/)
+ ![AWS Lambda Basics](https://www.serverless.com/aws-lambda)
+ ![AWS Lambda Functions](https://aws.amazon.com/lambda/)
+ ![CDN](https://cyberhoot.com/cybrary/content-delivery-network-cdn/)