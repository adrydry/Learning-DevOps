
## Create a User 

We create a user with full access and set up our environnement on Cloud 9 (Ubuntu)

## Install Terraform

It can be done On Windows on Linux
 
- Go to download terraform, save and extract in the C Drive
 - Copy the path of the executable file and edit the environment variable
- Open our Cmd as an administrator and check if terraform is installed by using **terraform --version**
 - Create the access key and secret key
 ![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/6297a165-d29c-47e7-9e3d-e003b2c258a5)

On Linux
![2](https://github.com/adrydry/Learning-DevOps/assets/102819001/187c9428-e100-4619-a6ea-63f43b7466f4)

## Cloud Providers
We will configure the AWS provider that will give Terraform access to the AWS API to perform operations on AWS infrastructure. For that, Go to terraform registry, check AWS, select EC2 instances. 

- In our cloud9 terminal, create a directory for our project. Inside the directory, create a **.tf** file. Inside the file, copy and paste API for the AWS provider Ec2 instances. Make all the necessary modifications
![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/72504e5d-77bf-4055-91fb-e782dde7bbe8)

## Initialise our terraform directory
For tha, we use the command **git init**

![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/06090ab0-45fe-4f81-b6bb-428c2ce1a07d)


## Terraform Plan
- Create a **main.tf** inside the project directory. It is a primary file for Terraform in any repository and it can have another name.
Inside, this file, we will define the Api for the VPC. Go on terraform registry, copy the Api code and, paste it in the terminal and make modifications.
Terraform plan will check my code and will let me know if something need to be change

![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/8a6a52ee-0ef6-4e7c-bd97-d9e0a26cd722)

## Terraform Apply
Will help us to execute our main.tf files

![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/b6122d05-91ad-4ed4-beba-de364d4427f0)

My vpc is created and visible on the console

![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/b670adce-2964-440e-ba4d-2fcc99e22687)


- 
































