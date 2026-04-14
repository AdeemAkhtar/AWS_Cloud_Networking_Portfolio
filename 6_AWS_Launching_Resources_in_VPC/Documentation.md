<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Launching VPC Resources

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-ec2)

**Author:** Adeem Akhtar  
**Email:** adeemakhtar@gmail.com

---

## Launching VPC Resources

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-ec2_8ee57662)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is an isolated network within the cloud, and it is useful because we can arrange subnets and resources in it.

### How I used Amazon VPC in this project

I used Amazon VPC to create a public and private subnets along with the public and private EC2 resources in each.


### One thing I didn't expect in this project was...

One thing I didn't expect in this project was launching the architecture using resource map.

### This project took me...

This project took me 45 minutes

---

## Setting Up Direct VM Access

Directly accessing a virtual machine means access to the EC2 instance through it CLI.

### SSH is a key method for directly accessing a VM

SSH traffic means any kind of request or response from a secure shell could be accepted on port 22.

### To enable direct access, I set up key pairs

Key pairs are encryption keys, user can connect to the instance using the encryption keys directly through CLI.

A private key's file format means it's a file containing its encryption keys, just like some text in a .txt file. My private key's file format was .pem.

---

## Launching a public server

I had to change my EC2 instance's networking settings by associating it with my VPC and public subnet, enabling auto-assignment of a public IPv4 address and selecting my existing security group.

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-ec2_88727bef)

---

## Launching a private server

My private server has its own dedicated security group because its traffic is restricted in its local scope and not to the internet.

My private server's security group's source type is custom, named NextWork Public Security Group, which means the private instance can only communicate with the resources that are part of my public instance.

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-ec2_4a9e8014)

---

## Speeding up VPC creation

I used an alternative way to set up an Amazon VPC! This time, I used the option "vpc and more" that represents the architecture as a resource map.

A VPC resource map is i visualising tool the shows the architecture.

My new VPC has a CIDR block of 10.0.0.0/16 It is possible for my new VPC to have the same IPv4 CIDR block as my existing VPC because they are logically isolated within AWS network. No conflict occurs as long as they don’t communicate directly

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-ec2_1cbb1b88)

---

## Speeding up VPC creation

### Tips for using the VPC resource map

When determining the number of public subnets in my VPC, I only had two options: 2 - 4 public subnets with 2 AZs and 1 - 2 with 1 AZ.

The setup page also offered to create NAT gateways. 
A NAT Gateway (Network Address Translation Gateway) in Amazon Web Services is a managed service that lets private resources in a VPC access the internet for updating patches, etc., without allowing the internet to initiate connections back to them.

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-ec2_8ee57662)

---

---
