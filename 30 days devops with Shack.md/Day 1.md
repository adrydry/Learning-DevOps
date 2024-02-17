## DAY 1: WHAT IS DEVOPS

Def DevOps is a set of practices that help to move code from the development to the operation troughout different phases as Building, testing, security analysins, deployement and monitoring.

## What to do to apply the Devops process in our application?

For that, we can use the CI/CD process to follow to ensure that our application will run smoothly.

**CI** is means that every time every developper makes a change to the code due for example to the new requirements of the client in the shared repository, these changes will be integrated without affecting the live production environnement. EX: Client gives 3 new requirements (features) for his application. 3 developpers will make a copy of the main branch (feature branch) and the operation teams will create a pipeleine for each new feature branch. When the developpers commit his change in the feature branch, someone of the operation team will start the pipeline (build,test,) and deploy to a temporaly server, see if it's working or not. Incase, it's not working, developpers will make a change again. These 03 features can be tested at the same time and when everything it's ok, we can push the change to the main branch. 

**Processes inside the CI**: build - automation build - reporting the result

**CD** To ensure that the changes of the CI will be go in production, we need to deploy them to different environments:

**Dev env**: First deployment is done in this environment after the developpers committed the changes. If the changes are correct, there are deployed to the QA env;
**QA env**: Quality Assurance development. we test our changes
**PPD env**: Pre release env, it's similar to Prod env
**Prod env**: where the application run live, accessible to clients
**DR**: Disaster recovery environment will help us to roll back incase we have any issue with the prod env. We use the env for deployment, so that our application runs fine all the time.

When we completed automatically the deployment, that's **continuous deployment** bu when we need a manual effort, like pushing a buttom for deployment, that's **Continuous delivery** 

**Processes inside CD**: Deployment pipeline (Deploy the change to our server) - Automated deployment - testing - Release and rollback - Monitoring

## How DevOps make our projet efficient - Benefits

- **Save a lot of time**: to bring application to the marketMany changes can be integrated with the source code without affecting the running application;
- **Early bug detection**: We have implemented multiples security tools in our pipelines that help to identify bug earlier;
- **Increase collaboration**: communication between development and operations team;
- **improve quality**: continuous testing with the 05 environments before deploying in production
- **agility and flexibility**: we are able to apply changes in less time
- **Maintain efficiency** : we are using the best practices to deploy our application


## Interviews questions related

1- What is devops 

2- what is CICD

3- How many environnements do you have in your project

4- What were the benefit of Devops in your project
