
## CLOUD SHELL

Allow you to access the Azure environment faster without provisionning resources

**az group list** List of ressources group 
**az storage account list** List of storage account
**az vm lists** list of the VM
**az vm create** to create a virtual machine

## Rn Powershell in the CloudShell
Get-AzResourceGroup
Get-AzStorageAccount
Get-AzVM
Remove-AzVM

## AZ Mobile Apps

Allow you to access your Azure Portal from your mobile devices.
It interacts with Azure Manager to access your resources. We can also use a version of the cloudshell to run Powershell or Azure CLI directly

## ARM Templates
Azure Resources Manager manages everything in Azure. It is a common language and syntax that could be used for idempotent actions.Idempotent means that applying an operation once or applying it multiple times
has the exact same effect.It is written in JavaScript Object Notation, or JSON and has many parts:
**The content version** is the version of your template.You can put this to whatever version you want,but is generally used to indicate any changes and how major they
are. For example, a small change might be from 1.0.0 to 1.0.1, where a major change would go to version 2.0.0.
**The resources section** describes what resources you want and how to manipulate them. In this case, we will create a storage account in the east US location of type standard
underscore LRS. You might notice that the name has these curly braces and takes this value. This is a variable, which means it is provided when you run the template.
If there was a value here, it wouldn't be very unique. It would be the same every time. For example, first time the ARM template is run, the variable could be llama-drama-storage-1.
When the template is used again, the day after, it might be given the name acg-az900-update.
The name can be whatever you want it to be, but usually follows a naming convention set by your company or team and, well, that's it for this template, at least. 
which means you can run each template again and again, with the same result.
**Source control** can be used to track any changes to the template over time.
It's declarative. You only specify what you want, not how. The implementation is all done in the Azure Resource Manager. And no human errors. Automation removes the chance of humans making a mistake. Alrighty,

## Azure Advisor
The Advisor will provide recommendation to improve availability of resources, save costs on services, increase reliability, increase the infrastructure reliability .and a whole lot more. Security is also a large part
of the recommendations given by the advisor.
The dashboard of the Advisor is where you get an overview
of the recommendations.
**High availability** relates to making sure you have enough resources to cover all the scenarios and all the traffic coming in.
**Security**, which obviously refer to how strong your virtual fences and walls are.
**Performance** to let you know if there are any problems with how bits and bytes are being processed and transferred on your subscription.
**Operational excellence**, which refers to how many medals you have won in the cloud games
**health alerts** Choosing the right services for your architecture, repairing logs, and more.

## Cloud computing concepts

**High avaibility** if one server fail, it's replaced immediately. 

**Reliability** Fault tolerance, avoid failure, Disaster recovery.No downtime **Resilience** is the capacity of a system to recover from failure and continue to function. In this context, the application is deploy in multiple locations. Also, no server as a single point of failure.

**Scability** Scalability refers to both the ability to automatically add or remove virtual machines scaling out, known as horizontal scaling, and also increasing the resources
on a single existing machine scaling up, known as vertical scaling.

**Predictability** Predictable performance and costsPredictable performance is simply knowing that your application is going to have the same experiencefor our customers regardless
of how many of our customers are on that application at any given point of time.
This is closely intertwined with our previous high availability and scalability concepts such as automatically scaling or auto scaling, load balancing, and high availability to provide
a consistent experience, automatically increasing and decreasing our compute capacity so our application always runs as we expect it to.

The other aspect of predictability is that of predictable costs, or in other words we're not going to get an unexpected surprise based on our cloud usage.
Azure allows us to both track and forecast what resources we are using and by that manner what we are going to pay for them in real time.
In addition, Azure provides a number of analytics tools to let us view patterns over time so we can more accurately predict long term cloud usage as well.

**Security**
Security is simply the concept of being in full control of the security of our cloud resources, which can include full control such as infrastructure as a service services or handing off some security
in control over to Microsoft for more managed platform as a service services.
This can take on a wide range of controls such as administering patches, maintenance, controlling the network traffic into and out of our resources, and much more.

**Governance**
Governance is simply the ability or the capability to establish corporate standards for our different Azure deployed environments,
including restrictions on deployed resources when necessary. These allow us to create standardized environments that uphold to a corporate standard, many of which are requiredfor different government regulatory requirements
and we have the ability to audit our existing resources in case any of those resources are outside of our corporate compliance standard.

**Manageability**, which actually has 2 aspects, management of the cloud and management in the cloud. **Management of the cloud** refers to how you manage your different cloud resources,
which can include automatically scaling your resources up and down. Again, our scaling term based on customer need having full visibility into the health of our resources via the monitoring tools built into Azure,
which can include automatically replacing failing resources and the ability to deploy resources in preconfigured templates such as ARM templates,
which is much more consistent than mainly deploying resources one by one.

By contrast, **management in the cloud versus** refers to how we are able to manage and interact with our different cloud resources,which can include the Azure Portal,
Azure CLI, command line environment, and programmatic methods like APIs. So wrapping things up, that was a lot of info that we provided of terms and definitions
and all of them are very important to understand.

## Azure Architecture

As defined by Microsoft, a region is a set of datacenters deployed within a latency-defined perimeter and connected through a dedicated regional low-latency network. "A set of datacenters" means that each region has more than one datacenter.

Availability Zones are unique physical locations within an Azure region. Each zone is made up of one or more datacenters equipped with independent power cooling and networking. And each region that supports Availability Zones -- because not all do -- has a minimum of three separate zones. The physical separation of Availability Zones within a region protects applications and data from datacenter failures.

## Ressource Group and Ressource Manager

**Ressources Groups** are essential for any architecture on Azure. Everything in Azure is inside a resource group. No exceptions. And while all resources must be inside a resource group, the resource group itself is not a resource. A resource group can contain resources that are located in different regions.
For example, you could have a central database server in East US and your web application could be hosted in East US2, but they are in the same resource group,
as they are related. A resource group can be used to manage access control for administrative actions. You can give access to an entire resource group, including the resources in it. A resource can interact with resources in other resource groups. And even though a resource group isn't a resource itself, it still needs a location, as it stores metadata about the resources inside it.

**Azure Resource Manager**, or ARM, is the underpinning of everything on Azure when it comes to creating, updating, or deleting resources. It is deployment and management services for Azure. The key thing to know is that if you interact with any of the resources on Azure, it goes through the ARM. Whether you use the portal, PowerShell, Azure CLI, REST APIs, or client SDKs, the Azure Resource Manager API handles your request.

This also means that any functionality available or added to the ARM will be available in all the various tools within a shorter period of time. By Azure having a single entry point for managing resources, you get a bunch of benefits as well. You can deploy, manage, and monitor all the resources for your solution as a group
rather than handling these resources individually. When you deploy your resources, you can be confident it happens in the same way every single time.

You can define the dependencies between resources, ensuring that any new resources don't step on the toes of the others. And you can easily decide which users have access to which resources using built-in features in the ARM. You can logically organize all your resources using the tag feature. **Tagging** is assigning a label for each resource you can then sort and perform actions on. And you can clarify your organization's billing by viewing costs for a group of resources
sharing the same tag.

So in summary, resource groups are what every resource in Azure is inside. While it isn't the resource itself, it is critical to manage your resources. It is completely up to you which resources you place in which resource groups, and it is an opportunity to structure how your Azure infrastructure is managed.
Azure Resource Manager, or ARM, is the layer of the Azure architecture which every single interaction with Azure resources go through. Whether you use the portal, the CLI, or some other tool, it talks to Azure through the ARM.
































































































































