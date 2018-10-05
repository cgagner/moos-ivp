FROM ubuntu:18.04
MAINTAINER Christopher Gagner <Christopher.Gagner@gmail.com>

# Setup the base Ubuntu container
RUN apt-get update && apt-get install -y \
  build-essential \
  libjpeg-dev \
  libtiff-dev \
  libpng-dev \
  libfltk1.3-dev \
  fluid \
  cmake \
  git

RUN \
  cd /opt && \
  git clone https://github.com/cgagner/moos-ivp.git && \
  cd moos-ivp && \
  ./build.sh

# Add MOOS-IvP to the PATH
ENV PATH "$PATH:/opt/moos-ivp/bin" 

