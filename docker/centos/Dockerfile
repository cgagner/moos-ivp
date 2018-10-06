FROM centos:7
MAINTAINER Christopher Gagner <Christopher.Gagner@gmail.com>

# Setup the base Ubuntu container
RUN yum update -y && yum install -y \
    libjpeg-turbo-devel \
    libtiff-devel \
    libpng-devel \
    mesa-libGLU-devel \
    fltk-devel \
    fltk-fluid \
    cmake \
    make \
    gcc-c++ \
    git \
  && yum clean all \
  && rm -rf /var/cache/yum

RUN \
  cd /opt && \
  git clone https://github.com/cgagner/moos-ivp.git && \
  cd moos-ivp && \
  ./build.sh

# Add MOOS-IvP to the PATH
ENV PATH "$PATH:/opt/moos-ivp/bin" 

