
## jenkins Dockerfile 

___
$ cat Dockerfile
FROM jenkins/jenkins:lts

# Copy plugins.txt to the container
#COPY plugins.txt /usr/share/jenkins/ref/plugins.txt

# Install plugins using jenkins-plugin-cli
RUN jenkins-plugin-cli --plugins git workflow-aggregator blueocean
[node1] (local) root@192.168.0.8 ~/jenkins
$
===

## creating the images 
docker build -t <your_jenkins_name> .

### once image created use that image to launch jenkins

docker run -d -p 8080:8080 -p 50000:50000 --name <container_name> <your_jenkins_name>

## password path /var/jenkins_home/secrets/initialAdminPassword
