FROM golang:1.16-alpine

WORKDIR /app

COPY go.mod ./
COPY go.sum ./

RUN go mod download

COPY *.go ./

RUN go build -o /http_receiver

EXPOSE 3333

CMD [ "/http_receiver" ]
