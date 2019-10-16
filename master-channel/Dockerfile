FROM ubuntu:18.04

ENV FLUTTER_CHANNEL master
ENV FLUTTER_HOME /flutter

RUN apt update
RUN apt install -y curl git xz-utils unzip

RUN mkdir ${FLUTTER_HOME}
RUN git clone -b ${FLUTTER_CHANNEL} https://github.com/flutter/flutter.git ${FLUTTER_HOME}

ENV PATH ${PATH}:${FLUTTER_HOME}/bin
RUN flutter upgrade
RUN flutter config --enable-web  --no-analytics
