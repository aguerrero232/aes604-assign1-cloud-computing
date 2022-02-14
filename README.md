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


# Architecture

Site is developed with html and simple vanilla js

# Amazon S3 - object storage service that stores data as objects within buckets
All assets are stored on an AWS S3 bucket from the html files that let you view the site to the awesome higlights of me slaying noobs in call of duty.

### Buckets are stored in a specific region 
in this specific bucket's case it is stored in the **US East (Ohio)** us-east-2 region.
Data uploaded to the bucket as objects in Amazon S3. Each object has a key (or key name), which is the unique identifier for the object within the bucket.

