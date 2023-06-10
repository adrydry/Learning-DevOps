## WHAT IS TOMCAT?

It is a web server that help to deploy Java based application on internet.

## The workflow

- We have an EC2 machine with Apache Tomcat installed

- we build our application using mvn package or mvn clean package to generate the artifact in form of jar or war file

- Inside the Apache tomcat folder, there is another folder Webapps where we are supposed to copy and paste our artifact

- Now, we can access the application on the browser with the port 8080
