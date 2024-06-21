
### first we need to logins to docker by following command 

docker login 

##![image](https://github.com/padalasurendramac/dockerdoc/assets/53860717/6140b8a8-4bef-44d2-b321-156564c122d1)

## before push need to add tag your repo then image name like below

docker tag <current_images_name> <your_dockerhub_name>/<your_suggested_name>:<version>

example :- docker tag rd_my_jenkins padalasurendra2428/rd_my_jenkins:latest

## check docker images

docker images

### now push to dockerhub

docker push <your_dockerhub_name>/<your_suggested_name>:<version>

![image](https://github.com/padalasurendramac/dockerdoc/assets/53860717/34bcf870-1a71-4937-8a4d-ca2a0a174d2d)

##final verify at dockerhub
![image](https://github.com/padalasurendramac/dockerdoc/assets/53860717/d0098c5a-00d6-433b-a97a-0a91d0fc0578)
