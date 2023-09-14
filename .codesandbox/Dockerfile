# CodeSandbox supports debian and ubuntu based images
FROM debian:bullseye

RUN apt update -y

RUN apt install -y python3 python3-pip
RUN apt install -y curl

# Download and install Go
ENV GO_VERSION 1.20.3
RUN curl -L -o go.tar.gz https://golang.org/dl/go$GO_VERSION.linux-amd64.tar.gz &&     tar -C /usr/local -xzf go.tar.gz &&     rm go.tar.gz

# Set the Go environment variables
ENV GOPATH /go
ENV PATH $PATH:/usr/local/go/bin:$GOPATH/bin

# Verify the installation
RUN go version
