## testing env setup 

docker pull jenkins/jenkins:lts

docker run -d -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home --name jenkins jenkins/jenkins:lts
==

FROM jenkins/jenkins:lts
USER root
RUN apt-get update && apt-get install -y docker.io
USER jenkins


docker build -t custom-jenkins .
docker run -d -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home --name jenkins custom-jenkins

===
docker run -d -p 8080:8080 -p 5000:5000 -v jenkins_home:/home/jenkins_home --name naa_jenkins jenkins/jenkins:lts
