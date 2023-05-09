**A network** is a group of connected devices that are able to communicate with each other. In the LAN, devices are connected to the switch which is connected also to the routers, connected also to the ISP/Other Networks. Every device in our network has a IP address.

## What is DNS
Dns stands for domain name system. For devices on the network to be reachable, they must be addressable. DNS maps domain names to their respective IP addresses. So DNS is a protocol that let us use domain name instead of ip addresses. The advantage of DNS is that it allows us to use multiple IP Addresses for the same domaine name. To know the domain name of a host, just use dig url.com.

## Public and private DNS
In public DNS, we use a single domain name. Private DNS use VPC level. To enable public DNS, we can purchase a domain and created a hosted zone. we cannot buy a private DNS, we can just accessed it through the vpc level 

**/etc/resolve.conf** is used to determine which host to use for DNS queries

**/etc/hosts** is used for statically mapping IP addresses to hostnames host DNS is used to trandform a domain name in an IP addresses
**netstat** and **ss** is used to view listing services and active connections  

## Subnets
Is used to divide a larger network into smaller interconnected network to have a more manageable network and minimise the traffic

## Protocols
Protocols povide a medium or a set of rules to establish communication between differents devices for exchange data or services. we have many protocols like: ssh(Port 22), http(port80), https (Port 443), ftp(port21), 
## VPN
it enable private connections betweens 2 machines or network over a shared public network

## Public and private network
**Private network** is a network where services are controlled by a single organizations so that another user from outside of this organizations cannot connected
**Public network** everybody can access the services without restrictions

## Cidr notation
this is amount of bits allocated to a network
## Static and dynamic IP
Whenever we create an ec2 instances, we get a dYnamic IP and if you reboot the system, the ip changes. But in production, we don't want our ip adress to change, the static adrees is required

## Firewall
Network security devices. it monitors and filters incoming and ongoing traffic to protect our servers based on your security policy

## Proxy
It provides a geteway between users and internet. it will help you to prevent cyber attacks
