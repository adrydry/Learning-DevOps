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
