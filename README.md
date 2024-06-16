# dockerdoc
dockerdoc

# docker version check command
docker --version

# docker run containder backgroup us -d 

docker  run -d ubuntu

# docker run container to interactive use -it and bash 

docker run -it ubuntu bash

# docker run along with itd use 

docker run -itd ubuntu 

# docker run using -p 8080 external 80 internal docker

docker run -p 8080:80 ubuntu

# docker run with name 
docker run --name nginx ubuntu

# docker run along  with environment variable 

docker run -e MYVAR=334455 ubuntu

# docker run with volume mount /etc/new host machine and /etc/log is docker image one

docker run -v /etc/new:/etc/log ubuntu

 
## docker remove container by using docker run command --rm

docker run -rm ubuntu

## docker run command to using specific network

docker run --network mynetwork ubuntu 

### full docker run command 


docker run -d --name webserver -p 8080:80 -e ENV=production -v /host/logs:/var/log/nginx nginx

-d: Runs the container in detached mode.
--name webserver: Assigns the name "webserver" to the container.
-p 8080:80: Maps port 8080 on the host to port 80 in the container.
-e ENV=production: Sets an environment variable ENV to production.
-v /host/logs:/var/log/nginx: Mounts /host/logs from the host to /var/log/nginx in the container.
nginx: The image used to create the container.


