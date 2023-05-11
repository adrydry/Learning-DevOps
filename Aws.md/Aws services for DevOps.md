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
Elastic Compute Cloud is a physical virtual server. It uses to provide 
- Scale computing capacity
- enable organizations to deploy applications faster without investing in hardware upfront
- host your application
- host your databases
- Object storage. 

## S3 Bucket
Simple Storage bucket. It is a storage that help users to upload n numbers of files. the advantages of S3:
-Security
- Durability
- Highly scalable
In a S3 bucket, we have the ability to save between **0byte to 5 terabyte**. 


## IAM Roles and Policies
Identity Access Management is used to:
- set users permissions and roles to grant access to different AWS services;
- It enables organizations to create multiple users with their own credentials;
- allows users to do only task related to their job in the Aws console
EX: We have an EC2 Instances where an application is running. This application wants to access only the S3 bucket. The **Iam role attach the Policy** helps to authenticate the access to the s3 bucket 

## AWS CICD 
These services will be used by the Devops Engineer to automate the process of development and deployment of applications. We have:

**Aws Code Commit/ Code Built/ Code Deploy**: it's like a github repository. Github is a central repository for source code managment hosted in AWS. So code commit helps to :
- create repository any numbers of repository
- control all the repository created: manage the access to the repository

Workflow: Developpers commit the code  in the **code commit**, the code is compile to generate an artifact using **code build**. 

Code build connects to code commit or any external source code managment repository and rruns different unit tests. Every time, the developpers add new features on the code, the new code is automatically rebuild to obtain the latest artifact. 

The artifact is deployed on production, on server, on EKS, ECS, Lamda with **code deploy**. Code Deploy allows you to deploy your build artifact on differents compute infrastructures

**Code Pipelines** helps the Devops Engineers by automatically detects any new changes commit by the developpers and start building your source code, automatically deploys the artifacts on differents environnements (testing env, production environnement). So Code pipelines facilitates the process from code commit to Code deploy by creating **Pipelines**

## Infrastructures

**Compute infrastructures**

-**EKS**:elastic kubernetes services host our k8s application.

-**ECS**: elastic container service will help you to deploy your service, your tasks that run on Docker container.

-**Aws Lambda**: is a serveless compute service. It's automatically scaling, it helps to run ad hoc jobs, it helps for automation some tasks. we can integrate our lamda with cloudwatch

**create and manage our infrastructure**: 
in a situation where you have to create 100 servers, it will be difficult to it manually. So , we can use:

- **IAC**: as **Cloudformation** for AWS. you define a template in yaml or json format. In the template, we define all the ressurces, we want to create. Go to cloudformation and search for Stack and upload your json or yaml files. The file will be validated and will create automatically all the resources listed in the file. 
To create, IAC, we can also use **CDK - cloud development hit** ### from **CFT**: CDK allows you to write actual code to create infrastructure by using differents constructs like For loop, white loop,...

We can also use **Terraform** which works for multicloud providers

- **Coding or programming language**:


## Security Services in AWS

We have to secure our services with:

-**IAM Role with policy**: It is the easiest way to secure our infrastructure. The user who is authorized and authenticate can will perform certain jobs. With IAM roles, you manage which user can access which resources and service ?

-**VPC security group**: It's an entity that can be attached to any infrastructure.

-**Cloudtrail**: It allows you to monitor, auditing and record activities across your infrastructure. It answers to Who access something? What did they access? When did they access?...It will help you to track any activity done by users or hackers inside your aws account

## Monitoring

Is important to monitor your infrastructures. We have many monitoring services in AWS:

-**Cloudwatch**:

-**Metrics**: Piece of informations about a paticular service overtime. For different aws services, we will have different aws metrices. For ex, we have host our application on EC2 instances, how to monitor our instances? which elements are important for the monitoring?: cpu utilization (dont need to go so high). These metrics need to be in form of **graph**

-**Alarms**: Notify you when something is not going well. For that, we have to attach an alarm with the metrices. For exp: Cpu utilization >90% for 15 minutes, something is going wrong. with the alarm, the devops will have the information and will make sure to autoscale.

-**Logs**: contains critical informations like what application is doing?. It will give you information about an application in amount of time. go to **Cloudwatch insights** to find logs

-**Dashboards**: as devops engineer, the responsability is to make sure that the application is running continuously by creating a dashboard. you can add different types of metrices to your dashboard, set differents alarms and logs.


























