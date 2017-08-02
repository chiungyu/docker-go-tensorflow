ARG ubuntu_version=xenial-20170710
ARG tf_version=1.1.0

FROM chiungyu/ubuntu-tensorflow:${ubuntu_version}-tf-${tf_version}

ARG go_version=1.8.1

# This assumes curl and ca-cert are in ubuntu-tensorflow.
# TODO: maybe refactor shared go-getting code.
RUN apt-get update && \
    apt-get install -y --no-install-recommends g++ gcc git

RUN curl -L https://storage.googleapis.com/golang/go${go_version}.linux-amd64.tar.gz | tar -C /usr/local -xz
ENV PATH ${PATH}:/usr/local/go/bin

ENV GOPATH /root/go
RUN mkdir $GOPATH
