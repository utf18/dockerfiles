FROM centos:7
MAINTAINER Benjamin Stein <b.stein@diffus.org>
RUN yum update -y && \
yum install -y \
gcc \
make \
git \
expat \
expat-devel \
curl \
wget \
which \
net-tools \
openssh \
openssl \
openssl-devel \
ca-certificates \
cpanminus && \
cpanm -n Rex \
Array::Diff \
Moose \
MooseX::Params::Validate \
namespace::autoclean \
YAML \
MIME::Base64 \
JSON::XS \
Import::Into \
common::sense \
Parallel::ForkManager \
IPC::Lite Mojolicious \
JSON::XS Crypt::OpenSSL::Random \
Crypt::OpenSSL::RSA \
LWP::UserAgent \
LWP::Protocol::https
WORKDIR /root/rexfiles
