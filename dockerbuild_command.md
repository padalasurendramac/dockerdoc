
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



#### docker file example 


# Use a base image
FROM ubuntu:latest

# Define arguments with default values
ARG APP_ENV=development
ARG PORT=8080

# Set environment variable based on the argument
ENV APP_ENV $APP_ENV
ENV PORT $PORT

# Other Dockerfile commands like installing dependencies, copying files, etc.
# For example:
# COPY . /app
# WORKDIR /app
# RUN npm install

# Expose the port
EXPOSE $PORT

# Command to run the application
CMD ["node", "app.js"]


### run command 

In this Dockerfile:
FROM ubuntu:latest: Sets the base image to Ubuntu.
ARG APP_ENV=development and ARG PORT=8080: Define arguments with default values.
ENV APP_ENV $APP_ENV and ENV PORT $PORT: Set environment variables based on the arguments.
EXPOSE $PORT: Exposes the port defined by the PORT argument.
CMD ["node", "app.js"]: Specifies the command to run the application, you can modify this depending on your application's requirements.

### When building the image, you can override these arguments from the command line like this:

docker build --build-arg APP_ENV=production --build-arg PORT=3000 -t my_image .


