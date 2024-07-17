# S3 – Cross Account – Shared Bucket
**Description**:- Share access of a S3 Bucket to an IAM User in Another Account.

## Pre-requisites
1. S3 bucket in Source Account: which is going to be shared accross the accounts.
2. IAM User in Target Account: which is going to access the S3 bucket of Source Account.

## Procedure for allowing cross account access to S3 Bucket.
### In Source Account
1. Open the S3 Bucket and Navigate to permissions.
2. Edit the bucket policy and add the S3 Bucket Policy which allow access to Target Account IAM User.
3. Save the changes.

### In Target Account
4. Attach an IAM policy allowing access to the Source Bucket to the IAM User.

**Now, we can access S3 bucket through CLI.**

#### Optional Steps **(Follow the following steps if want to access the bucket in AWS Console of Target User)**
5. In S3, create an Access Point to S3 bucket.
6. Give a name, choose the bucket is in other account.
7. Add Account ID of Source Bucket and S3 Bucket Name.
8. Choose Network Origin as Internet and create the Access Point.
Through this Access point in Target User Account, we can access the Source S3 bucket of Source account and perform actions which are allowed as per policies attached to IAM User and S3 Bucket.

For more in-depth knowledge and additional resources, please refer to https://repost.aws/knowledge-center/s3-cross-account-upload-access.

#
**Sample Policy Files are attached in the folder.**
