FROM registry.access.redhat.com/ubi7/ubi-minimal@sha256:9e2cec104a77b76e6c343f67bd058005dc64d573fccf339c24cf79013ff8e7f3

LABEL maintainer="Jordan Gregory <jordan@gregory-dev.io>" \
      repository="https://github.com/Gregory-Development/ubi-go" \
      version="1.0.0"

RUN microdnf install git tar gzip \
  && curl https://dl.google.com/go/go1.12.5.linux-amd64.tar.gz | tar zxC /usr/local \
  && mkdir -p /go/bin /go/src /go/pkg \
  && microdnf clean all

ENV GOPATH="/go"
ENV PATH=$PATH:/usr/local/go/bin

ENTRYPOINT ["/bin/bash"]