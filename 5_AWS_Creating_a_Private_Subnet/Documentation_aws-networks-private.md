<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Creating a Private Subnet

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-private)
![<# alt text #>](Architecture.png "Screenshot")
**Author:** Adeem Akhtar  
**Email:** adeemakhtar@gmail.com

---

## Creating a Private Subnet

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-private_afe1fdbd)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is a private network that provides isolation within it. It is useful because we can create and arrange the resources required by the architecture. 

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to create NACLs, Route tables, Public and Private subnets.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project is that, private subnets also require their own NACLs and Route tables to stay private.

### This project took me...

This project took me 55 minutes.

---

## Private vs Public Subnets

The difference between public and private subnets is that public subnet is internet facing through internet gateway and private subnet is isolated and does not connect to the internet for public access directly.

Having private subnets are useful because, there are private resources that are supposed to be residing inside an isolation. Private subnets provides that isolation where they cannot be accessed through internet.

My private and public subnets cannot have the same CIDR block, because the IP address in the VPC could overlap (No two resources can have a single IP address in a single VPC)

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-private_afe1fdbd)

---

## A dedicated route table

By default, my private subnet is not associated with any route table.

I had to set up a new route table for my private subnet  because i have to access the resoures residing inside my private subnet later.

My private subnet's dedicated route table only has one inbound and one outbound rule that allows local traffic.

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-private_b4b904b5)

---

## A new network ACL

By default, my private subnet is associated with default network ACL created by AWS.

I set up a dedicated network ACL for my private subnet because i can associate my own access inbound and outbound.

My new network ACL has two simple rules: "deny" all inbound and outbound traffic.

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-private_1ed2cb07)

---

---
