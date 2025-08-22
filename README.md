# aws-scalable-webapp-
This repository details the architecture of a scalable, highly available web app. It uses Route 53 for domain management and AWS infrastructure (VPC, multi-AZ EC2 instances). An Application Load Balancer distributes traffic, with SSL certificates for security and backup solutions ensuring data integrity
   

![Kratak opis slike za čitače ekrana](https://github.com/MilanBizic/aws-scalable-webapp-/blob/main/Registerdom.png?raw=true)

The project's domain registration is managed through Route 53
![Alt text for the image](https://github.com/MilanBizic/aws-scalable-webapp-/blob/main/mb.png?raw=true)                                      
The project's new domain is now live!
![Alt text for the image]( https://github.com/MilanBizic/aws-scalable-webapp-/blob/main/Vpc2.png?raw=true)
We've successfully set up our project's Virtual Private Cloud (VPC), laying down a solid foundation for our infrastructure.
![Alt text for the image](https://github.com/MilanBizic/aws-scalable-webapp-/blob/main/subnets.png?raw=true) 
We did make 4 subnets. This architecture uses public and private subnets for high availability.
Public instances handle external requests, while private instances run the backend application securely
![Alt text for the image](https://github.com/MilanBizic/aws-scalable-webapp-/blob/main/igw.png?raw=true)
Internet Gateway (IGW) attached to the VPC.
This allows communication between the VPC and the internet for public subnets.
![Alt text for the image](https://github.com/MilanBizic/aws-scalable-webapp-/blob/main/routetables.png?raw=true) 
Here is a  view of a well-organized VPC with separate route tables for public and private subnets, indicating a setup designed for proper traffic management and network segmentation.
![Alt text for the image]( https://github.com/MilanBizic/aws-scalable-webapp-/blob/main/nat.png?raw=true) 
NAT gateway has been selected to be deployed in one Availability Zone to enable private subnets to connect to the internet.

![Alt text for the image](https://github.com/MilanBizic/aws-scalable-webapp-/blob/main/Inboundrules.png?raw=true)
Security groups are virtual firewalls,we create one for our load balancer and another for our EC2 instances.
On this photo, I've created the Load Balancer Security Group, configuring it to accept all inbound web traffic on ports 80 and 443 from anywhere on the internet.


