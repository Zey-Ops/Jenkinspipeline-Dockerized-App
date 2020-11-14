Project-204: Jenkins Pipeline for Dockerized Phonebook Application
(Python Flask & MySQL) Deployed on Docker Swarm

This project we aim to create a Jenkins pipeline to deploy the Phonebook Web Application 
with Docker Swarm on Elastic Compute Cloud(EC2) instances by pulling the app images from the AWS Elastikc Container Registry (ECR) repository. 

## Project Skeleton

```text
204-jenkins-pipeline-for-phonebook-app-on-docker-swarm (folder)
|
|----readme.md                  # Given to the students (Definition of the project)
|----phonebook-cfn-template.yml # To be delivered by students (Cloudformation template)
|----Dockerfile                 # To be delivered by students
|----docker-compose.yml         # To be delivered by students
|----init.sql                   # Given to the students (SQL statements to initialize db)
|----jenkins-cfn-template.yml   # Given to the students (Cloudformation template for Jenkins Server)
|----Jenkinsfile                # To be delivered by students
|----app
      |----phonebook-app.py     # Given to the students (Python Flask Web Application)
      |----requirements.txt     # Given to the students (List of Flask Modules/Packages)
      |----templates
            |----index.html      # Given to the students (HTML template)
            |----add-update.html # Given to the students (HTML template)
            |----delete.html     # Given to the students (HTML template)


->> Jenkins Server should be capable of;
- Create ECR repo
- Build Docker image
- Push Docker image to ECR repo
- Create infastructure for the app

ps : We are choosing jenkinsfile to install our infastructure rather cloudformation. Becuase with jenkinsfile we can make any changes in our code and jenkins can build right
after we change our code. Thats why we are using as continious integration. But with the 
cloudformation template we can build one time and if there are any changes we have to make necessary changes in our code and deploy the stack again manually. Which is not recommended. 

** Every pipeline needs a Jenkinsfile.











