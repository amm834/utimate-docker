FROM ubuntu
RUN apt-get update -y
RUN apt-get install maven openjdk-8-jdk -y

WORKDIR /src

ADD pom.xml .

RUN ["mvn","verify","clean","--fail-never"]

COPY src src

RUN ["mvn", "package"]

CMD ["java", "-jar", "target/words.jar"]
