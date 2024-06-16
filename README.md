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

 
