# Build base image

## Build mongodb
cd Kubernetes/image-build/mongodb  
source build.sh

docker image ls  
```shell
REPOSITORY     TAG     IMAGE ID         CREATED        SIZE  
mongodb      3.6.5    b500b08fbea1   15 seconds ago    523MB
```
docker tag mongodb:3.6.5 hollycat/mongodb:latest
docker push hollycat/mongodb:latest

## Build ethereum-api
cd Kubernetes/image-build/ethereum-api  
source build.sh

docker image ls  
```shell
REPOSITORY   TAG    IMAGE ID         CREATED        SIZE  
node        8.11.1  7b9a1d8633ae   59 seconds ago   335MB
```

docker tag node:8.11.1 hollycat/nodejs:latest
docker push hollycat/nodejs:latest

