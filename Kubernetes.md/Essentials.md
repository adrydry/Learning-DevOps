***Documented from KODECLOUD***

## What is Kubernetes or K8s?
K8s is one of the most technology of the cloud computing today. It is supported on any cloud platform and support hosting enhanced and complex applications. It is an open source and the most pouplar container orchestration in the market. To understand k8s, we need to understand **container** and **orchestration**.
It is a container orchestration technology used to orchestrate the deployment and management of hundreds and thousands of containers in a clustered environment.
## What is a container
**Why we need container and Docker**

Imagine that you have to set up an end to end stack with differents technologies like a webserver (nodejs), a database like (mongoDB), a messaging system like Redis and an orchestration like Ansible. This can be difficult because:
- the compatibility with the OS with all these technologies
- the compatibility between the services and the libraries and dependencies on the OS
- the application of the architecture changed over time. and everytime, something changed, we have to go trough the same process of checking compabilities
- Everytime, we have a new developper on board, you find difficult to set up a new environnement. the new developpers had to follow a large set of instructions and run hundreds of commands to finally set up the environnements
- Different environnements for developpement/ testing/ production
All this made the life of developping, building and shipping the application really difficult.

**Docker** gives the possibility to run each component in a separatecontainer with his own libraries and its own dependencies all on the same VM and the OS but within separate environnements or containers. We just need to build the docker configuration once and all our developers could now get started with a **simple docker run command**. The only thing they need to do, is to ensure that they have Docker installed on their systems. Docker utilises **LXC Containers** 

**Containers** are isolated environnements. They can have their own processes or services, their own networking interfaces, their own mounts just like VM, except, they all shared the same OS Kernel
Every OS has 2 parts: the kernel and the Software. **the kernel** is responsible for interacting with the underlying hardware while the Software referred to User interfaces, drivers, compilers, file managers, developper tools,etc..
 
 ## Container Orchestration
 
 Now, our application is packaged into a docker container, how do you run this application in production? What if your application relies on other containers such as databases or messaging services or other backend services? What if the number of users increases and you need to scale your application? How do you scale down when the load decreases?
 To respond to all theses inquiries, we need an underlying platform with set of resources and capabilities. The platform need to orchestrate the connectivity between the containers and automatically scale up or down basede on the load. This whole process of automatically deploying and managing containers is known as **container orchestration**. There are multiples orchestration technologies like k8s from google, docker with docker swarm, Mesos from Apache.
**Advantages of orchestration**
- high avaibility of the application: The failure of a hardware could not bring your application down because with the orchestration tool, we have multiples instances of the application running on different nodes;
- The user traffic is load balanced across the various containers: When demand increases, deploy more instances of the applications seamlessly and within a matter of seconds
- Scale the number of nodes up or down without having to take down the application and do of these easily with a **set of declaratives object configuration files**

 ## Differeneces between Docker swarm and K8S
 **Docker swarm**:
 - Easy to set up but lacks some the advanced features required for complex applications
 - k8s is popular but it's difficult to set up and get started by provides a lot of options to customize deployments and supports deployment of complex architectures
 - 

## Kubernetes Architecture

**A node or minions** is a machine, physical or virtual on which k8s is installed. A node is a worker machine where containers will be launched by k8s. We need to have many nodes to be able to manage incase one node goes down, that's called **cluster**. A cluster is a set of nodes grouped together so that if one node fails you have your application still accessible from the other nodes

Who is responsible to manage the nodes? where is the information about members of the cluster stored? How are the nodes monitored? When the nodes fails how do you move the workload of the field node to another worker node? **The master** is another node with k8s installed in it and is configured as a Master. The master watches over the nodes in the cluster and is responsible for the actual orchestration of containers on the worker nodes


![image](https://user-images.githubusercontent.com/102819001/234431866-f7230285-11b0-4b71-81e6-1b9fb165f684.png)

## Components of the Kubernetes

When you installed k8s on a system, you're actually installing the following components:
### Master Node
- **API server** acts as a frontend for k8s. the users, management devices, command line interfaces, all talk to the apiserver to interact with the k8s cluster
- **etcd service** is the database. It stores all data used to manage cluster in a distributed manner. It responsible to implement logs within the cluster to ensure thatthere are no conflicts between the masters
- **controller manager** is the brain behind orchestration.They are responsible for noticing and responding when nodes, containers or end points goes down. the controller makes decision to bring up new containers
- **Scheduler** is responsible for distributing containers across multiples nodes. It looks for newly containers and assign them to nodes
### Worker node
- **kubelet** is the agent that runs on each node in the cluster. The agent is responsible for making sure that the containers are running on the nodes as expected. it is responsible for interacting with a master to provide health information of the worker node and carry out actions requested by the master on the worker nodes
- **Container runtime** is the software used to run containers (Docker)
 to know
## Kubectl 
Is used to deploy and manage applications on a k8s cluster. 
- **kubectl run hello-minikube** to get cluster information, to get the status of other nodes in the cluster and to manage many other things, ... just run the command 
- **kubectl cluster-info** To have a view information about the cluster and the kubectl run 
- **kubectl get nodes** to list all the nodes part of the cluster
- **kubectl get nodes -o wide

## YAML
is used to represent configuration files.  





























