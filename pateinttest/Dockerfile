# Building the binary of the App
FROM golang:1.17 AS build

# `boilerplate` should be replaced with your project name
WORKDIR /app

# Copy all the Code and stuff to compile everything
COPY . .

# Downloads all the dependencies in advance (could be left out, but it's more clear this way)
RUN go mod download

# Builds the application as a staticly linked one, to allow it to run on alpine
RUN CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -a -installsuffix cgo -o app .


RUN go build

CMD ["./app"]

