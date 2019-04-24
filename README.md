# AirlineDatabaseApp

## About

AirlineDatabaseApp is a project to help me learn about containers, Docker, and Compose. The Java program provides a command-line interface to execute queries on the Postgres Database.

I containerized the program and the database to allow others to easily install the project with minimal effort and without errors. Containers allow users to run software without worrying about compatibility and/or dependency issues  I use Docker-Compose to manage multiple containers at once and handle networking between them.

  * Container#1 is a Java program running on the official OpenJDK image. 
  * Container#2 is a postgres database. 

See the Java source code in `/javaAPP/src/`

See the Postgres SQL and data CSV in `/postgresDB/`

## Set-up

1. Download the code using [git] (https://git-scm.com/downloads)

`git clone https://github.com/jmora060/AirlineDatabaseApp`

2. Install [Docker CE] (https://docs.docker.com/install/linux/docker-ce/ubuntu/) for your OS
3. Install [Docker Compose] (https://docs.docker.com/compose/install/)


## RUN
  * On Linux:
  
  `sudo docker-compose pull` (this may take a while)
  
  `sudo docker-compose up -d db`
  
  `sudo docker-compose run java`
