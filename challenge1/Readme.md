# Problem statement

  

A three-tier architecture is a software architecture pattern where the application is broken down into three logical tiers: the presentation layer , the business logic layer or application layer and the data storage layer.

  

# Approach

Shifting the security to the left, I will be desiging the infrastuture with one VPC with 4 subnets with combination of private and public for various layers. In addition to that there will be a bastion host and a NAT gateway for the admins to have access to the infrastructure. I am also going to create a Auto scaling group across two availbality zones for fault tolerance and high availablity.

# What we need?

 1. VPC
 2. Internet gateway
 3. 4 Subnets (2 public and 2 private in 2 AZ's)
 4. Create two Route tables (public for internet and private for the traffic through NAT Gateway)
 5. Create NAT Gateway
 6.  ELB (Internet and the Internal Load balancer)
 7. Auto Scaling group
 8. Bastion Host

# Options
Terraform , I would be using the DSC IAC tool to define these modules and build the immutable infrastructure.
## THE READ REPLICA IS NOT CREATED IN THIS SOURCE CODE

