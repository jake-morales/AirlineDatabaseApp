FROM openjdk
ADD . /code
WORKDIR /code

RUN rm -rf bin/*.class
RUN javac -cp ".;lib/postgresql-42.1.4.jar;" src/DBproject.java -d bin/

ENV DBNAME=mydb
ENV PORT=5432
ENV USER=postgres
ENV PASSWORD=password

CMD java -cp lib/*:bin/ DBproject $DBNAME $PORT $USER $PASSWORD
