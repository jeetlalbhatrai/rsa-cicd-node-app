# rsa-cicd-node-app
CICD	
•	GitHub account/repo with GitHub actions available.
•	Docker installed locally
•	Admin of an Azure subscription setup and ready to use.
•	Have a dockerhub account.	|

•	Build the following Nodejs app. GitHub - fhinkel/nodejs-hello-world: Hello World example
•	Standup Sonarcube instance
•	Connect GitHub action to Sonarcube.
•	Push a container image to dockerhub
•	Run image from dockerhub on your local machine.

#######
Added Dockerfile in code.
Setup sonarqube
#docker run -d --name sonarqube -p 9000:9000 -e SONAR_ES_BOOTSTRAP_CHECKS_DISABLE=true sonarqube:lts 
         http://localhost:9000/account/security
         admin --> admin (admin@123)
         token: nodejsappscan sqa_082e08d7f9090654b479d36d87d62443b87741e2

Create secret in github repository.
DOCKER_PASSWORD
DOCKER_USERNAME
SONAR_HOST_URL
SONAR_TOKEN

Add sonar-project.properties

create .github/workflows/ci.yml


Azure--> 
RG
container instances..
image- sonarqube:community

TF code-->
rsa-sonarqube-tf-code