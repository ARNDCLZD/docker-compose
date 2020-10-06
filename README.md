# docker-compose

A Java service in front of a mySQL data base

## requirement

jdk11

## The app

Java app data base access config: https://github.com/charroux/docker-compose/blob/main/src/main/resources/application.properties

Java main program with the database initialization : https://github.com/charroux/docker-compose/blob/main/src/main/java/com/example/carRental/CarRentalApplication.java

The Java service: https://github.com/charroux/docker-compose/blob/main/src/main/java/com/example/carRental/CarService.java

The persistent Java class: https://github.com/charroux/docker-compose/blob/main/src/main/java/com/example/carRental/Car.java

Docker file for the Java app: https://github.com/charroux/docker-compose/blob/main/Dockerfile

Docker compose file: https://github.com/charroux/docker-compose/blob/main/docker-compose.yml

## Java app building

./gradlew build

## docker

docker-compose up
 
or 

docker-compose up --build

if the app has not been already built

## test

http://localhost:10222/cars

## check Docker containers

"docker ps" should display 2 containers: mysql, car rental java service.

## stop the containers

docker stop [containerID] 

## Docker volumes (mysql data persistence on disk)

docker volume ls

docker-compose down --volumes --remove-orphans  

docker volume rm -f [volume name got by docker volume ls]

## remove docker images

"docker images" should display 3 images: openjdk, mysql, car rental service java app.

docker rmi -f [imageID]

