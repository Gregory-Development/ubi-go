FROM registry.access.redhat.com/ubi8/ubi-minimal@sha256:7b7a9336b681f779b239141db4fd27fed9a7cc50e7ef7a727fc9490559b4e1df

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