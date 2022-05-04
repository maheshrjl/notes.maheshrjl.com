# 📋 CLI Commands

### EC2

`aws ec2 describe-instances` - List all ec2 instances

### IAM

List all iam users - `aws iam list-users`

### S3

Delete s3 bucket with all of it's contents :

`aws s3 rb s3://bucket-name –force`

Copy file from local machine to s3

`aws s3 cp MyFolder s3://bucket-name — recursive [–region us-west-2]`

List <mark style="color:purple;">size</mark> & <mark style="color:purple;">contents</mark> of s3 buckets - `aws s3api list-objects --bucket BUCKETNAME --output json --query "[sum(Contents[].Size), length(Contents[])]"`
