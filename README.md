# Assignment 1 - Cloud Computing

## Objectives
### Task 1: 
You will create a public S3 bucket
### Task 2: 
design and upload the website files to your bucket. The website should at least include one image, one short video (Maximum 30 Seconds), and 5 pages.  
### Task 3: 
You will configure the bucket for website hosting and secure it using IAM policies.
### Task 4: 
You will speed up content delivery using AWS’s content distribution network service or CloudFront.
### Task 5: 
Create a GitHub Repository for assignment 1, submit all the site content to this repository. 
### Task 6: 
Develop effective technical documentation for assignment 1 - Create a REAME.md markdown descripting the details of your AWS S3 infrastructure deployment for hosting your website. Including the link of your website.  Note: The technical discussion and documentation, rather than just the basic infrastructure buildout or software development, is where the most value occurs whether handing in homework assignments or completing a commercial project.
___

# Site Link
### https://d3h0nnty80ji1q.cloudfront.net

___
# Architecture

# Amazon S3 - object storage service that stores data as objects within buckets
___

All assets are stored on an AWS S3 bucket from the html files that let you view the site to the awesome higlights of me slaying noobs in call of duty.

### Buckets are stored in a specific region 
in this specific bucket's case it is stored in the **US East (Ohio) us-east-2 region**.
Data uploaded to the bucket as objects in Amazon S3. Each object has a key (or key name), which is the unique identifier for the object within the bucket.

###  S3 Versioning
Set up to keep multiple versions of an object in the same bucket, which allows objects that are accidentally deleted or overwritten to be restored.

## Bucket Policy
### All public access is blocked to the s3 bucket

Only the bucket owner can associate a policy with a bucket. The permissions attached to the bucket apply to all of the objects in the bucket that are owned by the bucket owner.

{
    "Version": "2008-10-17",
    "Id": "PolicyForCloudFrontPrivateContent",
    "Statement": [
        {
            "Sid": "1",
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::cloudfront:user/CloudFront Origin Access Identity XXXXXXXXXXXX"
            },
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::cloud-computing-assign-1/*"
        }
    ]
}

# Cloudfront
Enable accelerated, reliable and secure content delivery for Amazon S3 bucket using all edge locations. (best performance)
Allows use of Origin Access Identity (OAI) included in S3 bucket policy.


## High level overview

![Alt text](cloudfront_s3_highlevel_architecture.jpg)