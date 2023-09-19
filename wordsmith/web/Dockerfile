FROM golang

COPY dispatcher.go .

RUN go build dispatcher.go

COPY static /static

CMD ["./dispatcher"]
