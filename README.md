# AirlineDatabaseApp

## About

AirlineDatabaseApp is a project to help me learn about containers, Docker, and docker-compose. The Java program provides a command-line interface to execute queries on the Postgres Database.

I containerized the program and the database to allow others to easily install the project with minimal effort and without errors. Containers allow users to run software without worrying about compatibility and/or dependency issues  I use docker-compose to manage multiple containers at once and handle networking between them. Lastly, I used the alpine version (~5 MB) of the java and postgres base images to reduce image size and speed up downloads. 

  * Container#1 is a Java program running on the official OpenJDK image. 
  * Container#2 is a postgres database. 

See the Java source code in `/javaAPP/src/`

See the Postgres SQL and data CSV in `/postgresDB/`

## Set-up

1. Download the code using [git](https://git-scm.com/downloads)

    `git clone https://github.com/jmora060/AirlineDatabaseApp`

2. Install [Docker](https://docs.docker.com/v17.09/engine/installation/) for your OS
3. docker-compose comes with Docker Desktop, but check with `docker-compose --version`


## RUN
  * On Mac/Linux:
  
      `docker-compose pull` (pull base docker images)
  
      `docker-compose up -d db`(start postgres database container)
  
      `docker-compose run java` (run java command-line program)
