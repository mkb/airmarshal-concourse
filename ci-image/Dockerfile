FROM concourse/concourse-ci

RUN apt-get update

RUN apt-get install -y build-essential curl git
RUN curl -s https://storage.googleapis.com/golang/go1.6.2.linux-amd64.tar.gz | tar -v -C /usr/local -xz

ENV PATH /usr/local/go/bin:/usr/local/bin:/usr/local/sbin:/usr/bin:/usr/sbin:/bin:/sbin

RUN mkdir /root/go
ENV GOPATH /root/go
ENV PATH=${GOPATH}/bin:$PATH
RUN go get github.com/tools/godep
