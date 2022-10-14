# Deploying-static-website-on-AWS
Hosting a static website using S3 and Accessing cached website data using CloudFront.

## Creating S3 bucket:
1 - Clicking on "Create Bucket" button:<br>
![create bucket](Images/screenshot-2021-01-12-at-6.30.56-pm.png)<br>

2 - Bucket configuration:<br>
![Configure bucket](Images/screenshot-2021-01-12-at-6.32.23-pm.png)<br>

3 - Bucket is created:<br>
![create bucket](Images/screenshot-2021-01-12-at-6.34.56-pm.png)<br>

## Uploading files to the bucket:
![create bucket](Images/screenshot-2021-01-12-at-7.10.46-pm.png)<br>

## Adding bucket policy:
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "AddPerm",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::my-587109582807-bucket/*"
        }
    ]
}
```
