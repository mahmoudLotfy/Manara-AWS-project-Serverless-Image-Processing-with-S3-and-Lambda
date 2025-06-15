#Manara AWS project-Serverless-Image-Processing-with-S3-and-Lambda

Project name : Serverless Image Processing with S3 and Lambda

Architecture: Serverless

<img width="595" alt="image" src="https://github.com/user-attachments/assets/3c5705ae-00a6-47e7-ad3b-47494c08d2be" />


Description:
Create a serverless image processing application where users upload images to an S3 bucket, triggering an AWS Lambda function that processes and resizes the images before storing them in another S3 bucket.

Key AWS Services Used:
Amazon S3: Stores original and processed images.
AWS Lambda: Executes image processing (resize).

Learning Outcomes:
Building event-driven architectures with Lambda and S3 triggers.
Understanding cost-efficient, auto-scaling serverless applications.
Enhancing security using IAM roles and S3 bucket policies.

Deploymnet steps :

✅ Overview

A user uploads an image to an S3 bucket "manara-original-images-bucket".

An S3 event triggers a Lambda function.

The Lambda function resizes the image.

The resized image is saved in a different S3 bucket "manara-processed-images-bucket".

🔧 Step-by-Step Instructions
Step 1: Create Two S3 Buckets
Bucket 1 (Input): Where users upload original images "manara-original-images-bucket"
Bucket 2 (Output): Where Lambda stores resized images "manara-processed-images-bucket"

Step 2: Create an IAM Role for Lambda
Create an IAM role with the following policies:
AmazonS3FullAccess

Step 3: Write the Lambda Function
Write a node.js function that:
Name: ImageResizeFunction
Attach the IAM role created

Step 4: Add an S3 Trigger to the Lambda Function
Go to original-images-bucket
🔁 This will automatically trigger your Lambda when a new image is uploaded.


Step 5: Test the Flow
Upload an image to original-images-bucket
Watch:
Lambda executes (check CloudWatch logs)
Output appears in "manara-processed-images-bucket"
