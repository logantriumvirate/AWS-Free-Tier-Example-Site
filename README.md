# AWS-Free-Tier-Example-Site
This project demonstrates how to set up a basic social media application infrastructure using AWS Free Tier services. It includes an S3 static website, DynamoDB for data storage, Lambda for serverless computing, and CloudFront for content delivery.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Deployment Steps](#deployment-steps)
3. [Post-Deployment Steps](#post-deployment-steps)
4. [Cleaning Up](#cleaning-up)
5. [Architecture Overview](#architecture-overview)
6. [Free Tier Usage](#free-tier-usage)
7. [Contributing](#contributing)
8. [License](#license)

## Prerequisites

Before you begin, ensure you have the following:

- An AWS account with Free Tier access
- AWS CLI installed and configured with your credentials
- Basic knowledge of AWS services and CloudFormation

## Deployment Steps

1. Clone this repository:

2. Open the AWS CloudFormation console.

3. Click "Create stack" and choose "With new resources (standard)".

4. Upload the `cloudformation-template.yaml` file from this repository.

5. Click "Next" and provide a stack name and a value for the `ProjectName` parameter. Use only lowercase letters and numbers for the `ProjectName`.

6. Click through the next steps, leaving the default options.

7. On the final step, check the box acknowledging that CloudFormation might create IAM resources, and click "Create stack".

8. Wait for the stack creation to complete. This may take a few minutes.

## Post-Deployment Steps

After the CloudFormation stack is created successfully:

1. Go to the S3 console and find the bucket created by the stack (it will be named `{ProjectName}-{UniqueIdentifier}`).

2. Upload your website files (HTML, CSS, JS) to this S3 bucket.

3. In the CloudFormation console, go to the "Outputs" tab of your stack.

4. Find the `WebsiteURL` value. This is the URL of your website.

5. Access your website using the URL.

## Cleaning Up

To avoid incurring future charges, delete the resources when you're done:

1. Empty the S3 bucket created by the stack.
2. In the CloudFormation console, select your stack and click "Delete".
3. Wait for the stack deletion to complete.

## Architecture Overview

This application uses the following AWS services:

- **S3**: Hosts the static website files.
- **DynamoDB**: Stores user data and posts.
- **Lambda**: Processes API requests.
- **CloudFront**: Delivers content globally with low latency.

## Free Tier Usage

This project is designed to work within the AWS Free Tier limits. However, be sure to monitor your usage to avoid unexpected charges. Key Free Tier limits to be aware of:

- S3: 5GB of standard storage
- DynamoDB: 25 GB of storage
- Lambda: 1 Million free requests per month
- CloudFront: 50 GB of data transfer out

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
