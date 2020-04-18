FROM ubuntu:18.04

RUN apt-get update && \
    apt-get install -y wget curl vim git unzip gnupg openjdk-8-jdk openjdk-8-jre
RUN wget http://www.scala-lang.org/files/archive/scala-2.12.8.deb && \
    dpkg -i scala-2.12.8.deb
RUN echo "deb https://dl.bintray.com/sbt/debian /" | tee -a /etc/apt/sources.list.d/sbt.list
RUN curl -sL "https://keyserver.ubuntu.com/pks/lookup?op=get&search=0x2EE0EA64E40A89B84B2DF73499E82A75642AC823" | apt-key add
RUN apt-get update && apt-get install sbt
RUN curl -sL https://deb.nodesource.com/setup_13.x | bash -
RUN apt-get install -y nodejs
RUN npm install -g npm@6.8

RUN mkdir -p /home/jkilian/projekt

VOLUME /home/jkilian/projekt

EXPOSE 8000
EXPOSE 9000
EXPOSE 5000
EXPOSE 8888