FROM ubuntu AS builder

RUN apt-get update -y
RUN apt-get install maven openjdk-8-jdk -y

WORKDIR /src
ADD pom.xml .
COPY src src
RUN ["mvn","verify"]


FROM openjdk:8-jre-alpine

COPY --from=builder /src/target ./target
CMD  cd target; exec java -Xmx8m -Xms8m -jar words.jar
