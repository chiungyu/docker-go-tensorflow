`docker build --build-arg ubuntu_version=${UBUNTU_VERSION} --build-arg go_version=${GO_VERSION} --build-arg tf_version=${TF_VERSION} -t chiungyu/ubuntu-go-tensorflow:${UBUNTU_VERSION}-go-${GO_VERSION}-tf-${TF_VERSION} .`

See more args in Dockerfile.

Note that this docker image does not go get the tensorflow wrapper.
Instead of handling wrapper version in the docker image, the author manages wrapper version inside app repos with vendoring.
