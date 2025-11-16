
FROM golang:1.22

WORKDIR /app

COPY go.mod go.sum ./
# If go.mod does not exist yet, remove this COPY line and let go mod init create it

COPY *.go ./

# Initialize module only if go.mod does not exist
RUN test -f go.mod || go mod init dispatch

RUN go mod tidy

RUN go build -o dispatch .

CMD ["./dispatch"]
