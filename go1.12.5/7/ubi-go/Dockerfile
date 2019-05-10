FROM registry.access.redhat.com/ubi7/ubi@sha256:321c3c17f8d72df5820297cfce96c89ffbcf5ac9ecafa7cd9976fb023a2033a2

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