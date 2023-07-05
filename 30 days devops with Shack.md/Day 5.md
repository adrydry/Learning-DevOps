## SONARQUBE

Sonarqube is a security analysis tool which is used to run **analysis of our source code**.

## What's it for?

It's used for **code quality check** and for **code coverage**.

**code quality check** :When you have a source code for any project or applications. it can happen that this code has bugs, code smells, or vunerabilities. Sonarqube helps us for code quality check by detecting all these technical issues on our source code.
Sonarqube will generated a report to show us which part of our code has an issue.
 
**code coverage** :For any project, we have a number of test cases to do related to every part of our source code. So, if we do test cases for 80% of our code, that's means our code coverage is 80% (**amount of code covered during test cases)
When your code coverage is >80%, that's means your source code is good; <80% - code not good. This code coverage is not done just with sonarqube but with another 3rd party tool call **jacoco**.
So we integrate Sonarqube with jacoco and from there we generate the report of code coverage inside Sonarqube.

   
