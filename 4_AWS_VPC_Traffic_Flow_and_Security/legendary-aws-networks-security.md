<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Traffic Flow and Security

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-security)

**Author:** Adeem Akhtar  
**Email:** adeemakhtar@gmail.com

---

## VPC Traffic Flow and Security

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-security_92b0b0b4)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is an isolated private network inside the AWS Cloud. It is useful because we can create subnets within it to divide the VPC into smaller sections, where we can create our resources, e.g. EC2.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to build an architecture where could allow public internet traffic in and out from the VPC and subnets using Internet Gatewas, Network ACL, Route table, and Security group.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was secrate mission in which i had to create and delete the resources using cloud shell CLI.

### This project took me...

This project took me 45 minutes.

---

## Route tables

Route tables are sets of rules (routes) used to determine where network traffic from a Virtual Private Cloud (VPC) subnet or gateway is directed

Route tables are needed to make a subnet public because they are configured with a rule that sends all non-local traffic to an Internet Gateway (IGW).

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-security_0a07b191)

---

## Route destination and target

Routes are defined by their destination and target, 
The Destination is the range of IP addresses to which you want the traffic routed.
The Target is the gateway, network interface, or connection through which the traffic is actually sent to reach that destination.

The route in my route table that directed internet-bound traffic to my internet gateway had a destination of 0.0.0.0/0 and a target of NextWork IG.

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-security_0a07b191)

---

## Security groups

Security groups are like security guards that monitor both the inbound and outbound traffic at the resource level i.e. every single resource in a subnet/VPC has a security group.

### Inbound vs Outbound rules

Inbound rules are rules that monitor or restrict inbound traffic e.g. user visiting a web app i'm hosting.
I configured an inbound rule that allows all the public traffic from the internet to reach to my resource through port 80.

Outbound rules are rules that monitor/restrict outbound traffic, e.g. my web app requesting data from a public resource. By default, my security group's outbound rule will allow all outbound traffic.

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-security_92b0b0b4)

---

## Network ACLs

Network ACLs are like community watchmen that secures my network at a subnet level.

### Security groups vs. network ACLs

The difference between a security group and a network ACL is their scope i.e. security group secures network at the resource level (so every single resource in my VPC is associated with a security group), while network ACLs secures network at the subnet level (every single subnet in my VPC is associated with a network ACL).

---

## Default vs Custom Network ACLs

### Similar to security groups, network ACLs use inbound and outbound rules

By default, a network ACL's inbound and outbound rules will allow all incoming and outgoing traffic.

In contrast, a custom ACL’s inbound and outbound rules are automatically set to deny all incoming and outgoing traffic.

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-security_4faeb056)

---

## Tracking VPC Resources

I created a VPC, an internet gateway and a security group using Cloud Shell CLI.

EC2 Global View is a tool where you can find all my resources according to the regions.  I could even narrow down my search by selecting and using the search box. Without EC2 Global View, you'd have to explore each region individually.

Now that I've learnt about EC2 Global View, I'd use it again to view my resources in accordance with the AWS Regions.

![Image](http://learn.nextwork.org/satisfied_silver_bold_rose_apple/uploads/aws-networks-security_b03ea6162)

---

---
