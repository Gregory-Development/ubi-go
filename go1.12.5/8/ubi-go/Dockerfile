FROM registry.access.redhat.com/ubi8/ubi@sha256:12bec5ede6a1b6d23071a735c0d6d3ca59233da71e1a253497e28e52f327b06e

LABEL maintainer="Jordan Gregory <jordan@gregory-dev.io>" \
      repository="https://github.com/Gregory-Development/ubi-go" \
      version="1.0.0"

RUN dnf install -y git gzip \
  && curl https://dl.google.com/go/go1.12.5.linux-amd64.tar.gz | tar zxC /usr/local \
  && mkdir -p /go/bin /go/src /go/pkg \
  && dnf clean all

ENV GOPATH="/go"
ENV PATH=$PATH:/usr/local/go/bin

ENTRYPOINT ["/bin/bash"]