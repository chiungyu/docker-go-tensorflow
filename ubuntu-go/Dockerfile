ARG ubuntu_version=xenial-20170710
FROM ubuntu:${ubuntu_version}

LABEL maintainer="Cliff Chiung Yu Lin"
ARG go_version=1.8.1

RUN apt-get update && \
    apt-get install -y --no-install-recommends curl ca-certificates

RUN curl -L https://storage.googleapis.com/golang/go${go_version}.linux-amd64.tar.gz | tar -C /usr/local -xz
ENV PATH ${PATH}:/usr/local/go/bin

ENV GOPATH /root/go
RUN mkdir $GOPATH

RUN go version

CMD ["/bin/bash"]
