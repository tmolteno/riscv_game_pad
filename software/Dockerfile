FROM debian:trixie
MAINTAINER Tim Molteno "tim@elec.ac.nz"
ARG DEBIAN_FRONTEND=noninteractive

# debian setup
RUN apt-get update -y && apt-get install -y \
    iverilog build-essential libnewlib-dev gcc-riscv64-unknown-elf

RUN apt-get install -y git
RUN rm -rf /var/lib/apt/lists/*

#########################################################################################
##
## Install the weird box diagram language from sourceforge
##
#########################################################################################

WORKDIR /build
ADD https://api.github.com/repos/tmolteno/CH32V003-GameConsole/git/refs/heads version.json
RUN git clone https://github.com/tmolteno/CH32V003-GameConsole.git
WORKDIR /build/CH32V003-GameConsole/software/
COPY Makefile.build ./Makefile

RUN ls
