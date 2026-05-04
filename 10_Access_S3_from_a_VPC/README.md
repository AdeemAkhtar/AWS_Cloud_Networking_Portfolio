<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Access S3 from a VPC

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-s3)

**Author:** Adeem Akhtar  
**Email:** adeemakhtar@gmail.com

---

## Access S3 from a VPC
![<# alt text #>](architecture.png "Screenshot")
![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-s3_3e1e79a2)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is an isolated private network inside the AWS environment, and it is useful because we can arrange our other aws services inside it.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to host an EC2 instance and used this instance to access the S3 bucket.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was uploading the file through AWS CLI.

### This project took me...

This project took me 35 minutes.

---

## In the first part of my project...

### Step 1 - Architecture set up

In this step, I launch a VPC with a public subnet and an EC2 instance in that subnet. 

### Step 2 - Connect to my EC2 instance

In this step, I will directly connect to the EC2 instance using EC2 instance connect.

### Step 3 - Set up access keys

In this step, I will create access keys because the keys are the only credentials through which we can access AWS environment using AWS CLI.

---

## Architecture set up

I started my project by launching a VPC, and later I launched an EC2 instance inside a public subnet in the launched VPC.

I also uploaded 2 png files in my s3 bucket.

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-s3_4334d777)

---

## Running CLI commands

AWS CLI is the command line interface for the instance through which we can get access to our services. I have access to AWS CLI because I opened the AWS CLI driectly through my EC2 instance.

The first command I ran was "aws s3 ls". This command is used to list all the S3 buckets.

The second command I ran was "aws configure". This command is used to login using aws access key and secret key.

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-s3_e7fa8776)

---

## Access keys

### Credentials

To set up my EC2 instance to interact with my AWS environment, I configured my AWS CLI using secret keys along with the "aws configure" command.

Access keys are login credentials for accessing and using the AWS services

Secret access keys are as follows:
Access key: AKIAVMKEG5X72774BRAG
Secret access key: vnJLoxLaCBoMi5fLdkitNgB5PKSf8Fh7AlpiNAted



### Best practice

Although I'm using access keys in this project, a best practice alternative is to use IAM Role.

---

## In the second part of my project...

### Step 4 - Set up an S3 bucket

In this step, I will create an S3 bucket because it will be used to connect through the AWS CLI 

### Step 5 - Connecting to my S3 bucket

In this step, I will access my s3 bucket through my AWS instance using the AWS CLI.

---

## Connecting to my S3 bucket

The first command I ran was "aws s3 ls". This command is used to list all the S3 buckets.

When I ran the command "aws s3 ls" again, the terminal responded with the name of the S3 bucket that I created. This indicates we can access S3 buckets from the AWS CLI using the AWS credentials.

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-s3_4334d778)

---

## Connecting to my S3 bucket

Another CLI command I ran was "aws s3 ls s3://nextwork-vpc-project-adeem", which returned the files that I uploaded to S3 previously.

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-s3_4334d779)

---

## Uploading objects to S3

To upload a new file to my bucket, I first ran the command "sudo touch /tmp/text.txt." This command creates a text file in "/tmp" directory.

The second command I ran was "aws s3 cp /tmp/text.txt s3://nextwork-vpc-project-adeem". This command will copy the file in the "/tmp" to the S3 bucket.

The third command I ran was "aws s3 ls s3://nextwork-vpc-project-adeem" which validated that the file had been uploaded to the S3 bucket and could be seen along with the other files already available inside the S3 bucket.

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-s3_3e1e79a2)

---

---
