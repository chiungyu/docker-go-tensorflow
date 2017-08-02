ARG ubuntu_version=xenial-20170710
FROM ubuntu:${ubuntu_version}

LABEL maintainer="Cliff Chiung Yu Lin"

ARG tf_type=cpu
ARG tf_version=1.1.0

# TODO: Change to ADD local copy if curl and ca-cert size matters.
RUN apt-get update && \
    apt-get install -y --no-install-recommends curl ca-certificates

RUN curl -L "https://storage.googleapis.com/tensorflow/libtensorflow/libtensorflow-${tf_type}-linux-x86_64-${tf_version}.tar.gz" | tar -C /usr/local -xz
ENV LD_LIBRARY_PATH ${LD_LIBRARY_PATH}:/usr/local/lib

CMD ["/bin/bash"]
