As a DevOps Engineer, we need to know this fundamentals services of AWS

## Regions and Avaibility Zones
**Regions** are Actual geographic locations where data centers are located. It has at least one AZ and max 6.  A region can be a **States** as Ohio, Oregon, Virginia, a **City** as Mumbai, London, **countries** as Canada, Singapour.

**Avaibility zones** each region has multiple isolated locations call AZ. Is the place where data centers are located. the distance between AZ is 60 miles. This helps AWS to achieve redundancy that helps users to host their applications in multiple regions. Like this, if one region is destroyed, the application still **high availaible** in another region or in another AZ.

## VPC
Stands for Virtual Private Cloud. Some benefits of a VPC
- It provides logically isolated area of AWS cloud to create Aws resources;
- It helps to control the network virtual environnement by defining the ip adress range, create subnet, configure the route table and network gateway.
We have 2 types of network gateway: - **internet gateway** helps your infrastructure (all your resources inside the vpc) to be connect to the internet and allows people from outside to access to your applications. It is located on the top of your vpc. In general, we use the default VPC but as a DevOps Engineer, we need to be able to create and design a 3 tier architecture and - **nat gateway** helps to avoid people from outside to access your application even if your application can be opened from internet. Nat Gateway will be located inside the public subnet
Private IP is static and will be the same through the lifecycle of the instances but Public ip is dynamic and change everytimes you shutdown the ec2
- It helps to create subnet. We have 2 types: **private subnet** is a subnet where the route table is not associated with the internet gateway and **public subnet** is a subnet where the route table is associated with the internet gateway

## EC2


## S3 Bucket


## IAM Roles and Policies
