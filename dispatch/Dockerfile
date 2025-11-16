
FROM golang:1.23

WORKDIR /go/src/app

COPY *.go .

RUN go mod init dispatch || true
RUN go mod tidy

RUN go build -o dispatch .

CMD ["./dispatch"]
