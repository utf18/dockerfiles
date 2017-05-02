FROM alpine:3.5
LABEL maintainer "Benjamin Stein <info@diffus.org>"
RUN apk add --no-cache \
gcc \
expat \
expat-dev \
g++ \
make \
git \
perl \
perl-dev \
curl \
wget \
openssh \
openssl \
openssl-dev \
ca-certificates
RUN curl -L http://xrl.us/cpanm > /bin/cpanm && chmod +x /bin/cpanm
RUN cpanm -n Rex Array::Diff Moose MooseX::Params::Validate namespace::autoclean YAML MIME::Base64 JSON::XS Import::Into common::sense Parallel::ForkManager IPC::Lite Mojolicious JSON::XS Crypt::OpenSSL::RSA LWP::UserAgent LWP::Protocol::https
WORKDIR /root/rexfiles
