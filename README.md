# docker-compose

## config

jdk11

## build

./gradlew build

## docker

docker-compose up

## test

http://localhost:10222/cars

## check Docker containers

"docker ps" should display 2 containers: mysql, car rental java service.

## stop the containers

docker stop [containerID] 

## remove docker images

"docker images" should display 3 images: openjdk, mysql, car rental service java app.

docker rmi -f [imageID]

