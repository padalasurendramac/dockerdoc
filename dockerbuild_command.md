
## docker build using create one directory 

mkdir dockerwork

cd dockerwork

### then create Dockerfile file under that directory 

## Dockerfile content

FROM ubuntu:latest

### run docker build commanad 

docker build -t mydocker .

-t mydocker: Tags the image with the name my-node-app.
.: Specifies the current directory as the build context.

### after that check local immages 

docker images 

## if docker file locate in differnt place use this command option -f 

docker build -t my-node-app -f path/to/Dockerfile .


### docker build commnd folder option like Dockerfile should under that folder

docker build -t mytest docker/

### docker argument passing while build the image --build-arg

docker build -t mytest --build-arg NODE_VERSION=16 .

## multiple args 

docker build -t my-node-app --build-arg NODE_VERSION=16 --build-arg APP_ENV=production .



