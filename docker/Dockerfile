FROM golang:1.16-alpine

WORKDIR /app

COPY ../go.mod ./

RUN go mod download && \
go get github.com/gorilla/mux

COPY *.go ./
RUN go build -o /main

EXPOSE 8081

CMD [ "/main" , "-p=8081"]