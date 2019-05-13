FROM registry.access.redhat.com/ubi7/ubi-init@sha256:35a331c670a921ae6195d39d81468645384ea39b533296b813bf879658632fee

LABEL maintainer="Jordan Gregory <jordan@gregory-dev.io>" \
      repository="https://github.com/Gregory-Development/ubi-go" \
      version="1.0.0"

RUN yam install -y git tar gzip \
  && curl https://dl.google.com/go/go1.12.5.linux-amd64.tar.gz | tar zxC /usr/local \
  && mkdir -p /go/bin /go/src /go/pkg \
  && yum clean all

ENV GOPATH="/go"
ENV PATH=$PATH:/usr/local/go/bin

ENTRYPOINT ["/bin/bash"]