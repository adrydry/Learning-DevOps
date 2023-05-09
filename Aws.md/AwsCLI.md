## What is AWS CLI
stands for Command Line interface which help us to create, manage and delete AWS ressources from the terminal. Everything, l can do from the aws console, l can do that using AWS CLI. This will help me to save a lot of time

## How to install AWCLI
Go on aws.amazon.com and download depending your OS( Windows, mac, Linux...). AWSCLI is installed by default on amazon linux

![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/2e011bda-c205-4f9e-870c-0b3f354c8cec)

After downloading and execute the file, Go to your command prompt of your system and use the command **aws --version** to verify if everything is ok.

## How to configure AWSCLI from strach
Access your aws console, go to credentials under your username and click on **Create an access key**. Store the access key and the secret key carefully. These credentials will help you to authentificate your aws account from the terminal. 

## How to configure our AWSCLI
Go to the terminal and use the command **aws configure**. Enter your generated credentials, enter the region and the format json. This will create a new profile on our systems. By using ls -la, we will see a directory **.aws**.
Enter this directory with **cd .aws**, **ls**, we have 2 files: config and credentials. **cat config**, we will see the name of the profile, the region; **cat credentials**, we will see access and credentials key generated in the above steps.

## Security best practices
Many people prefer to use **Environnement variables** to authentificate their access on the AWSCLI. Like this, they dont have to think about how to save these credentials.
For that, go to environnement variable, 

![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/4614cb40-02d9-4a85-85e1-42fd0bb4a2da)

the system will generate automatically your credentials
.![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/f01f0e45-336e-4d95-ba4e-874eb208494b)
To verify, just use **printenv | grep AWS** and your credentials will display

## AWS CLI basics and command structures
![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/aefa02f5-8164-4b5b-b6c1-b9a5a1bcea3d)

This is the basic structure of the AWS CLI
![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/997e898c-6596-476b-b632-bb494a404fe3)
For each ressources, AWS publishs the command to use. just copy and paste it.

## Automate AWS resource creation using AWSCLI
To automate the creation of an EC2 instances with the AWSCLI, we will follow these steps:
- Create a key pair:Go on Ammazon EC2 Key Pair, copy and paste the command in your terminal. Check the key pair section to verify the creation of the new key pair. We can also use in the terminal **aws ec2 describe-key-pairs** to list all the key in my system or **aws ec2 describe-key-pairs --key-name xxxxx**
to display a particular key. For this key, it will be possible to see the name of the key, its keypairid, his tag, his createtime,...  
 
## Delete a key pair
![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/3c5e1a21-e46e-4fa0-af30-eaa9765524c1)

## Create, update and delete EC2 instance using AWSCLI

![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/ff85aee5-cf21-4832-8ed7-60588146493f)

This is the command
![1](https://github.com/adrydry/Learning-DevOps/assets/102819001/81b3a777-2de7-4a35-9f1c-dbde76386ec4)
