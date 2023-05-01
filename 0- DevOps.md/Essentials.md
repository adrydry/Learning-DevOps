DevOps culture is about collaboration
between development and operations.
But in order to understand this,
it's important to understand this traditional model
that DevOps culture is a response to.
Under the traditional model, development and operations
are considered 2 separate entities
and they have different and opposing goals.
The goal of the development team
is to deliver features into the hands of the customer
as quickly as possible.
So their goal is speed,
but the goal of the operations team
is to maintain the stability of the system
and minimize downtime.
These 2 goals
end up becoming an opposition to one another,
because one of the worst things for stability is changes.
Every time you change the system,
you introduce a risk of instability.
So operations is trying to maintain stability
while the development team
is trying to deploy as many changes as possible.
In order for them to deliver features
into the hands of customers, they have to deploy changes.
Then every one of those changes introduces a risk
for stability.
So these 2 goals are in opposition to one another.
And even if these 2 teams want to collaborate,
many times, they wind up being in opposition
because of these different and opposite goals.
In fact, development teams are often measured
according to their speed of delivery.
While operations teams are measured
according to minimizing downtime.
So they have a great incentive to fight against each other,
to be in opposition to one another.
Now, both speed and stability are very important goals,
but because the development and operations teams
are in opposition to one another,
neither is able to accomplish those goals
as well as they should be able to.
The development team is always deploying changes
and not really prioritizing stability
while the operations team
is trying to slow down the development team
in order to maintain stability.
And so this opposition compromises
both of these goals to some degree.
But let's look at how these goals function
within a DevOps culture.
In a DevOps culture,
the development and operations teams are one group
and they both share the same goals.
And they're both measured according to those same goals.
Both speed and stability are very important.
What DevOps culture has discovered
is that when development and operations come together
and share the same goals
and prioritize speed and stability equally,
they're able to find solutions and build tools
that can allow an organization
to have both speed and stability.
To allow development, to deploy frequently,
to deploy quickly, to make changes to the system
in a way that is robust, standardized,
and allows the system to maintain stability for customers.
And therefore both of these goals
wind up being met in a much more robust way
than when you have 2 separate groups
fighting against each other.
So in a DevOps culture,
development and operations are playing on the same team.
You can almost picture it like a sports team.
In a traditional culture,
development and operations are on opposing teams.
In order for one team to win, the other team has to lose.
In order to have good speed of delivery,
stability has to be compromised;
or in order to maintain good stability,
speed of delivery has to be compromised;
but in a DevOps culture
development and operations are playing on the same team.
What's important about this
is the fact that they have shared goals
and usually shared measurements.
That means developers are being held accountable
for stability,
just as much as they're being held accountable
for speed of delivery,
and operations engineers are being held accountable
for speed of delivery,
just as much as they're being held accountable
for stability.
So let's look at some of the goals
that a DevOps culture might have,
and all of these goals really boil down to those 2 things:
stability and speed of delivery.
One of the goals that is shared
by development and operations in a DevOps organization
is fast time-to-market.
Time-to-market is the time that it takes
to take some work that a development team has created
and get it in front of a customer.
So the time from code being finished
to deploy to production and working, that's time-to-market.
And the faster that time-to-market is,
the more successful the organization will be.
Another goal is minimizing production failures.
This goes back to stability.
The more production failures there are,
the more instability there is.
So if we want production to be stable,
we need to make sure
that there are a few production failures,
and we need to find solutions
that will allow us to deploy quickly
so that we get that fast time to market
while also minimizing the number of failures
that are caused by those changes.
Another goal that goes back to stability
is immediate recovery from failures.
In the real world, failures are going to happen.
Mistakes are going to be made, things are going to break.
Any organization that doesn't recognize that
is deluding themselves because it's always going to happen.
So what do you do?
The best thing you can do is to ensure
that when those problems do happen,
you can recover from them quickly and immediately.
The faster you can recover from problems,
the less impact they will have.
Best case scenario is you can recover from a failure
before customers even notice.
And engineers in a DevOps culture
will work to make that a possibility.
So DevOps is about development and operations
working together.
And in a DevOps culture,
developers cared just as much about stability
as they care about speed,
and Ops cares just as much about speed
as they do about stability.
In a DevOps culture, the traditional roles of developers
and operations engineers, can even become blurred.
That is, developers can take
on more and more responsibilities of operations engineers
while operations engineers
take on more and more responsibilities
that look a little bit like development.
There's no hard and fast rule for what this looks like,
but when the 2 groups are working together,
the roles tend to blend a little bit.
In a traditional culture,
developers throw code over the wall when it's done
and wait for operations to get it deployed.
But instead of throwing it over the wall,
there is no wall in a DevOps culture,
Dev and Ops work together to create and use tools
and processes that support both speed and stability.
And it's required for developers and operations
to work together in order to create and support those tools.
DevOps recognizes that development and operations
are much more powerful when they're together.
Now, I hope you understand a little bit better
what a DevOps culture looks like.
In the next lesson, we'll tell some stories
that will actually help us understand
the differences between a traditional culture
and a DevOps culture in a very practical way.

## What is build automation
Build automation is automating the process of preparing code
for deployment to a live environment.
So depending on what programming languages
or frameworks are used to create the code,
many times code needs things done to it
before it's ready for deployment.
It may need to be compiled.
It may need to be linted, minified, transformed.
It may need to have unit tests run against it.
And build automation means taking all of these steps
and automating them so that they occur in a consistent
and automated way.
And this is usually done using a build script
and/or a build tool.
What tools are used to do build automation
are usually different
depending on what programming languages
and frameworks are being used,
but the one thing that build automation tools
all have in common is automation.
So what does build automation look like?
Usually, it looks like running a command line tool
that builds code using configuration files or scripts
that are treated as part of the source code.
So what that means is
if your code is committed to source control,
say it's committed to Git,
any configuration files or scripts
that are required to execute the build automation
would be committed alongside the source code.
Then I could check out or clone your source code
and using the same build tool,
execute the build on my machine.
Build automation is independent of an IDE.
Back in the old days,
a lot of people used to build their code directly in an IDE.
They would go into their IDE
and they would click on Compile or click on Build,
and that would generate some kind of artifact
that could then be handed off for deployment,
but good build automation happens independently of an IDE.
Even if it is possible
to execute the build automation within the IDE,
it should also be able to work the same way
outside of an IDE.
And this is important because it enables us to do things
like execute builds on a continuous integration server.
Another important thing about good build automation
is that it should be agnostic of the configuration
of the machine that it is built on.
What that means is that if you can build the code
on your machine, I can also build the code on my machine.
And if we use a continuous integration server,
we can build the code there as well
and get the same result in all 3 places.
So why should you do build automation?
Well, first, build automation is fast.
It automates tasks that otherwise
might have to be done manually, which saves time.
Secondly, and even more importantly,
build automation is consistent.
Because the build happens the same way every time,
we eliminate problems and confusion
that arise from manual builds
that might be done a little bit differently
every single time.
Build automation is also repeatable.
That means I can take the same version out of source control
and build it multiple times
and get the same result every time.
Any particular version of the source code can be transformed
into deployable code in a consistent way.
Build automation is also portable.
Because the build can be done
in the same way on any machine,
any member of a team can build the code on their machine,
as well as building the code on a shared build server
like a continuous integration server.
Building code does not depend on specific individuals,
and it does not depend on specific machines.
And finally, build automation is more reliable.
Because it's automated, there will be fewer problems
that are caused by badly done manual builds.
I hope that this lesson
has helped you to understand build automation.
Build automation is really a developer-centric process.
Operations engineers oftentimes
don't have to worry about it.
Build automation is very important to developers.
If you're a developer who is not using build automation,
I would highly encourage you to do so.
And if you're an operations engineer,
try and understand how important build automation is
to the development teams you're working with.
And if they are not using build automation,
it might be worth trying to persuade them to look into it.


## Continuous Deployment and Continuous Delivery
Continuous Delivery,
which is sometimes just called CD,
is the practice of continuously maintaining code
in a deployable state.
That means that regardless of whether or not the decision
is actually made to deploy a particular version of the code,
that code is always in a state that is able to be deployed.
That means that the decision of whether or not to deploy
is purely a business decision.
Do we want to deploy these particular features at this time?
And when you go to the development team and say,
"We want to deploy the code."
They're never going to say,
"Well, there's a bunch of work that we have to do
"in order to get code ready for deployment."
In Continuous Delivery,
the code is always ready for deployment.
Some people use the terms Continuous Delivery
and Continuous Deployment interchangeably,
or they simply use the abbreviation CD.
And of course,
if you use CD,
people don't necessarily know whether you're talking
about Continuous Delivery or Continuous Deployment.
However, these are actually two separate concepts
even though they are very closely related.
So what is Continuous Deployment?
Continuous Deployment is the practice
of frequently deploying small code changes to production.
So with Continuous Delivery,
we are keeping the code in a state
that is able to be deployed.
Continuous Deployment means
that we are actually doing the deployment frequently.
Some companies that do Continuous Deployment
are deploying to production multiple times a day,
but there's no standard for how often you should deploy.
In general, however,
the more often you deploy, the better.
With Continuous Deployment,
deployments to production are a routine commonplace event.
They're not a big scary event that only happens very rarely.
So what does it look like when you do Continuous Delivery
and Continuous Deployment?
Well, each version of the code
goes through a lot of automation.
It will go through a series of stages,
such as an automated build, automated testing,
perhaps automated packaging,
and maybe some manual stages too,
such as manual acceptance testing.
The result of this process
is that a version of the code becomes an artifact
or package that is ready to be deployed
in an automated way.
And when the decision is made to deploy,
the process of actually deploying that artifact
is also automated.
What this automated deployment looks like
is going to depend on the architecture
and what type of code is being deployed.
But no matter what that architecture is,
there's always one thing in common
with Continuous Deployment:
the deployment is automated.
With Continuous Delivery and Continuous Deployment,
if a deployment causes a problem,
it can be quickly and reliably rolled back.
Again, using an automated process.
Hopefully, this can be done
before the customer even notices the problem.
But rollbacks aren't a big deal for developers
because the developers can redeploy a fixed version
as soon as they have one available.
Rollbacks are not an obstacle
for developers getting their features in front of customers
because they can quickly roll forward again
once they have a fix.
And most importantly,
no one grips their desk in fear during a deployment.
Even if the deployment does cause a problem,
a rollback is readily available to prevent an outage.
So deployments are commonplace every day events
that happen all the time,
and it's not a big deal.
So why should you do Continuous Delivery
and Continuous Deployment?
Well, Continuous Delivery and Continuous Deployment
are great practices for achieving a faster time-to-market.
They let you get features in the hands of customers quickly
rather than waiting for a lengthy
and cumbersome deployment process
that only happens once every couple weeks or once a quarter.
There will be fewer problems caused
by the deployment process.
Many times, the most difficult processes in IT
are the ones that are rarely used
because the IT team doesn't have an incentive
to really fix the underlying problems with those processes.
But when you do deployments frequently,
that process is frequently used and frequently exercised
and problems with the process
are easily discovered and quickly fixed.
Continuous Deployments are much lower risk.
The more changes you deploy at once,
the higher the risk.
Frequent deployments involve deploying
only a small number of changes at a time.
So with fewer changes in that one deployment,
there is less risk that that particular deployment
is going to cause a problem.
Another benefit of Continuous Delivery
and Continuous Deployment is reliable rollbacks.
Because these processes require robust automation,
it means that rollbacks benefit from that robust automation
and become more reliable.
Rollbacks become a great tool
to ensure stability for customers.
They're no longer a bad thing.
They're a good thing because they allow us
to prevent customers from experiencing errors or downtime.
Rollbacks also don't hurt the developers
because the developers can roll forward with a fix
as soon as they have one.
And finally, Continuous Delivery and Continuous Deployment
will give you fearless deployments.
This robust automation,
when coupled with the ability to rollback quickly
and reliably means that deployments are commonplace,
everyday events.
They're not this big scary event
that has everyone gripping their desk in fear,
hoping that nothing goes wrong.
So now you understand Continuous Delivery
and Continuous Deployment.
I hope that this knowledge will help you achieve faster
and more reliable deployments in the future.


## What is IAC
Infrastructure as code is also known as IaC.
And it means managing and provisioning infrastructure
using code and automation.
With infrastructure as code,
instead of doing things manually
to manage and provision infrastructure,
we use automation and code
to create and change things like servers,
instances, environments, containers, clusters,
entire groups of servers,
and other types of infrastructure.
So what does infrastructure as code look like?
Well, without infrastructure as code,
this is how we manage changes
to some of our resources.
You might SSH into a host
and manually issue a series of commands
in order to perform a change.
But with infrastructure as code,
you would instead change code files or configuration files
that can be used alongside automation tools
to actually perform those changes.
You would then commit those files to source control,
treating them like code,
and then you would use an automation tool
to enact the changes defined in those code
or configuration files,
and actually make the changes in your live environments.
With infrastructure as code,
provisioning new resources,
as well as, changing existing resources
are things that are both done through automation.
So why should you do infrastructure as code?
Well, first you get consistency in the creation
and management of your infrastructure resources.
Automation has the benefit
that it will run the same way every time
and do the same things every time.
Humans tend to do things a little differently each time.
So you get a lot of consistency
in terms of how things are done
within your actual environments.
Secondly, you get reusability.
When you use infrastructure as code,
you can take that code,
those code files or configuration files
that you use to make your change,
and you can use it to make the same change, consistently,
across multiple hosts.
Or if you need to make the same change again in the future,
you can use that same code again to do that.
You also get scalability.
So say for example,
you need a new instance to add to a load balanced cluster.
If you provisioned the existing instances,
using infrastructure as code,
you can take that code
and use it to provision a new instance
that is configured exactly the same way
as the existing instances,
in a very short time, minutes or even seconds,
allowing you to quickly scale up or scale down.
Another great benefit of infrastructure as code
is that it makes your infrastructure self-documenting.
With infrastructure as code,
your infrastructure and any changes made to it
are documented through the changes made to those code
and configuration files
that are used to provision the infrastructure
and execute changes.
For example, the way that a particular server is configured
can be viewed in source control.
Whereas with the traditional model,
understanding how the server is configured
is a matter of knowing who logged into it
and what commands they executed.
And finally, infrastructure as code
helps you simplify the complexity.
Complex infrastructures can be stood up quickly
once they are defined as code.
For example, if you have a complex infrastructure
involving several database servers,
maybe an authentication server,
some application servers
and your organization requests a new test environment,
you can take the code that was used
to configure that infrastructure
and immediately spin up an identical infrastructure,
possibly even temporarily,
in order to satisfy the needs of your organization.
It makes it much easier to manage that complexity
when you use infrastructure as code.
So now you understand infrastructure as code.
In my time as an operations engineer,
we used Ansible to standardize
around infrastructure as code, as a practice.
And we found that it made our complex infrastructure
much more manageable and maintainable.
I hope that you will be able to use infrastructure as code
to obtain the same benefits going forward.


## Configuration Managment
Configuration management essentially just means
automated management of infrastructure configuration.
Changes are a normal part of day-to-day life
in the IT industry.
They always need to happen.
We always need to make changes
to keep our infrastructure up to date
and to meet changing business needs.
Configuration management is about doing these changes
in a maintainable way.
Configuration management is a way
of minimizing configuration drift.
Configuration drift is the accumulation
of all of the small changes
that are made to systems over time
and then cause those systems to become different
from one another.
If you think about it,
every time someone logs into a system and makes a change,
there's a chance that they have now made
that system different from other systems
that you manage when they really should be standardized.
Configuration management helps us
to minimize configuration drift
by rolling out changes and managing configurations
across a complex infrastructure
in an automated and centralized way.
There is a close relationship
between configuration management and Infrastructure as Code.
Infrastructure as Code is a very beneficial tool
that goes hand in hand with configuration management.
So, what does configuration management look like?
Well, the best way to describe it is to give an example.
Let's say that we need to upgrade a software package
on a bunch of servers.
Without good configuration management,
what we would do is log into each server
and perform the upgrade manually.
The problem is this process can lead to a lot of problems.
Maybe we forgot about one of the servers
because we didn't have good documentation on it,
and therefore the software package
was not upgraded on that server,
or perhaps, while we are in the process
of rolling out these upgrades
to a variety of different servers,
there is a temporary version mismatch
which causes something to break
while we're in the process of manually doing that.
On the other hand, with good configuration management,
what we do is define a new version of the software package
that we want in a configuration file or tool,
and then we use that tool
to automatically roll the change out
across a variety of servers within our infrastructure.
Configuration management
is about managing your configuration
somewhere outside of the servers themselves.
So, in the case of the example here,
we are managing it in configuration files
that are then applied using a configuration management tool.
Why should you do configuration management?
First, it saves time.
It takes less time to roll out configurations
because of the benefits of automation.
Secondly, good configuration management tools
will provide you insight.
Not only are they able to roll changes out to servers,
they give you insight into what the current state
of your infrastructure is.
So they can allow you to have a better understanding
of what has been rolled out to your servers
and what their configuration is at present.
Configuration management is very good for maintainability,
and this is very important
because a maintainable infrastructure
is easier to change in a stable way.
Change always introduces the risk of instability,
but the more maintainable your infrastructure is,
the lower that risk is.
Configuration management also minimizes configuration drift.
This means that it's easier to keep a standard configuration
across a multitude of hosts when you're not depending
on manually logging into hosts and making changes,
but you're using automation to ensure
that changes are rolled out to all hosts equally.
Configuration management is a very important tool
for DevOps.
Good DevOps infrastructures, especially in the cloud,
can become very, very complex.
You're going to need configuration management
in order to manage that complexity
in a stable and maintainable way.


## MONITORING

Monitoring is the collection and presentation of data
about the performance and stability
of services and infrastructure.
Within a DevOps culture, monitoring is very important.
It supports frequent deployments and fast time-to-market
by allowing you to quickly respond to any problems
that are caused by those frequent deployments.
And, of course, it supports stability for the same reason,
by allowing you to quickly address any problems
that could be affecting stability.
Monitoring tools collect data about things
such as memory usage, CPU, disk I/O,
and usage of other resources over time.
You can also collect application logs,
information about network traffic,
and a lot of other data that you can use to gain insight
into the health and performance of your infrastructure.
The collected data is then presented in various forms.
You can have charts and graphs that people can look at
in order to see how things are performing.
You can also use this data in the form
of real-time notifications about problems.
So, if your monitoring tools notice that there's a problem
in production, they could immediately notify you,
so that you can do something to fix that problem.
Hopefully, before customers even notice it.
So, what does monitoring look like?
Well, one way it can look is real-time notifications.
Let's say that performance on our website is starting
to slow down; response times are getting longer and longer.
The monitoring tool is watching our response times,
and notices that they're growing,
and immediately notifies an administrator,
so that the administrator is able to intervene before
that performance degradation leads to actual downtime.
Another use case of monitoring
involves post-mortem analysis.
That means looking at something after the fact.
So, let's say, that something went wrong
in production last night. It's working now.
Production is back up. The customers are happy,
but we still don't know what caused
the problem that occurred last night.
Luckily, our monitoring tools have actually collected
a lot of data during that outage,
and that data is now available to us.
So, in this scenario, let's say that we looked at the data
and the developers and operations engineers are able
to determine the root cause of last night's outage.
It just happened to be a poorly performing SQL query. But
now that we know what the cause was, we're able to fix it.
So, why should you do monitoring?
Well, the first reason is fast recovery.
The sooner we detect a problem, the sooner we can fix it.
We want to know about a problem before our customer does.
When something goes wrong in production,
the worst case scenario is for me to find out about it
by getting a call from a customer.
I want to know about that problem
before the customer calls me and already be working
to resolve it and, potentially, even resolve it
before the customer experiences the problem.
Monitoring also offers better root cause analysis.
The more data we have about our production systems,
the easier it is to determine the root cause
of any particular problem. Without good monitoring
many times we wind up making guesses
about what caused a problem to occur in production.
And therefore, we don't really have the tools
or information that we need to effectively fix
those problems for the future.
Monitoring is very important within a DevOps context
because it's one of the primary ways
that we can offer visibility into production systems
across teams, not just operations teams,
but also development teams.
Good monitoring tools give us useful data
that can be used by both developers and operations people
to understand the performance of code in production,
and potentially do optimizations to improve performance.
And another great benefit of monitoring
is automated response. Data that comes
from monitoring tools can be used
alongside orchestration tools,
and other types of automation tools
to provide automated responses to events.
For example, automated recovery from failures.
Monitoring tools can be used to detect problems,
for example, and then an orchestration tool
could be used to respond to that data
by isolating the broken node,
and replacing it with healthy ones.
Monitoring is essential to bringing together fast delivery
and stability, especially in complex systems,
and especially at large scales.
