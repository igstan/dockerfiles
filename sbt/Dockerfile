FROM java:8

MAINTAINER Ionuț G. Stan <ionut.g.stan@gmail.com>

RUN apt-get update
RUN apt-get install -y apt-transport-https
RUN echo "deb https://dl.bintray.com/sbt/debian /" | tee -a /etc/apt/sources.list.d/sbt.list
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2EE0EA64E40A89B84B2DF73499E82A75642AC823
RUN apt-get update
RUN apt-get install -y sbt=1.0.0
RUN sbt update

ENTRYPOINT ["sbt"]
