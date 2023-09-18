FROM ubuntu:latest
RUN apt-get update
RUN apt-get install build-essential -y
COPY main.c /
RUN make main
CMD /main
