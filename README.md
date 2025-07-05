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
code repository--> 
https://github.com/jeetlalbhatrai/rsa-cicd-node-app/tree/main

https://github.com/jeetlalbhatrai/rsa-sonarqube-tf-code

docker hub repository-->
https://hub.docker.com/repository/docker/jeetlalbhatrai/nodejs-hello-world/general

#docker run -d --name nodejstest -p 80:80 jeetlalbhatrai/nodejs-hello-world



Setup sonarqube
#docker run -d --name sonarqube -p 9000:9000 -e SONAR_ES_BOOTSTRAP_CHECKS_DISABLE=true sonarqube:lts 
         http://localhost:9000/account/security
         admin --> admin (admin@123)
         token: nodejsappscan sqa_082e08d7f9090654b479d36d87d62443b87741e2

create token in sonarqube. 
My Account --> secuitry --> Generate token.

Create secret in github repository.
Repository --> Setting --> Secrets & Variables --> Actions --> Resposiory Secrets--> New Respository Secrets
DOCKER_PASSWORD
DOCKER_USERNAME
SONAR_HOST_URL
SONAR_TOKEN

Add sonar-project.properties
Added Dockerfile in code.
create .github/workflows/ci.yml (Call above created secrets in github CI)

then push code to repsitory CI will starts...
