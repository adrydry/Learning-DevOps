
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

![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/722fb02f-d6d4-4b2e-ab53-b6438023714c)

After creating this file, terraform create a **.terrafom folder** and a **.terraform.lock.hcl** to record the provider selections it made above. Include this file in your version control repository so that Terraform can guarantee to make the same selections by default when you run "terraform init" in the future.


## Terraform Plan
- Create a **main.tf** inside the project directory. It is a primary file for Terraform in any repository and it can have another name.
Inside, this file, we will define the Api for the VPC. Go on terraform registry, copy the Api code and, paste it in the terminal and make modifications.
Terraform plan will check my code and will let me know if something need to be change

![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/2fa27309-c612-47af-ac5d-173bdd12cfe8)


![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/e73b1481-35b3-4dff-8aa4-e649ab24ebe7)


## Terraform Apply
Will help us to execute our main.tf files

![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/612b2cd6-5711-4062-9af3-b0a1ea303e4a)


My vpc is created and visible on the console

![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/d2a0d588-c399-4c2a-8a2f-95bb83f83a44)

Observed that, terraform apply creates a new file **terraform.tfstate

## How Terraform maintains the state of our infrastructure

It does that with the **state file**. To see what is the state, Use the command sudo apt install jq and terraform show -json | jq

![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/7db3b0a0-f8e2-4205-9200-d59bee624bf7)

We see that, even if we described the file, we still have some information. We can also view the ressources directly by using **terraform show**. The command **terraform state list** will help to list all the ressources and their information. Never modified the terraform tfstate.

![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/4d72e595-cce0-45ec-9944-faeb6ecb392e)


## How to secure our terraform.tfstate
Due to his importance, it's good to secure this file. For that, we need to migrate this file from our local computer to the Hashicorp cloud. We can store this file in the S3 bucket. But in our case, we will store that in the Hashicorp cloud because it's more secure and easy to manage

## Exploring the state file

**terraform state show ressource name** will show you the terraform show of a particular ressource
**terraform state show aws_vpc.terransible_vpc** display the json format version of terraform show

## Add Variables
It's required by Terraform to have *{}* at the end of the name of the variable. It helps to initialize variables
























