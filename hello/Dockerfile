FROM ubuntu:latest AS build
RUN apt-get update
RUN apt-get install build-essential -y
COPY main.c /
RUN make main LDFLAGS="-static"

FROM scratch
COPY --from=build /main /main
CMD ["/main"]
