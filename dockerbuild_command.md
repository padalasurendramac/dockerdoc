
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
