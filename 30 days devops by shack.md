## DAY 1: What's DevOps

**Def**
DevOps is a set of practices that help to move code from the development to the operation troughout different phases as Building, testing, security analysins, deployement and monitoring.

**What to do to apply the Devops process in our application?**

For that, we can use the CI/CD process to follow to ensure that our application will run smoothly.
 
**CI** is means that every time the developper will make a change to the code due for example to the new requirements of the client, these changes will be integrated without affecting the production environnement.
EX: Client gives 3 new requirements for his application. 3 developpers will make a copy of the main branch (feature branch) and the operation teams will create a pipeleine for each new feature branch.
When the developpers commit his change in the feature branch, someone of the operation team will start the pipeline (build,test,) and deploy to a temporaly server, see if it's working or not. Incase, it's not working, developpers will make a change again.
These 03 features can be tested at the same time and when everything it's ok, we can push the change to the main branch.

**CD** To ensure that the changes of the CI will be go in production, we need to deploy them to different environments:
- **Dev env**: First deployment is done in this environment after the developpers committed the changes. If the changes are correct, there are deployed to the QA env;
- **QA env**: Quality Assurance development. we test our changes
- **PPD env**: Pre release env
- **Prod env**: where the application run live
- **DR**: Disaster recovery environment will help us to roll back incase we have any issue with the prod env. We use the env for deployment, so that our application runs fine all the time
