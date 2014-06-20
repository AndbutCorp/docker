# Jmeter
#
# VERSION	0.0.1

FROM	ubuntu:12.04
MAINTAINER Jinuk Baek <kuniz37@gmail.com>

RUN apt-get update

RUN apt-get install -y wget openjdk-6-jre openjdk-6-jre-headless

RUN wget http://apache.tt.co.kr//jmeter/binaries/apache-jmeter-2.11.tgz
RUN tar xf apache-jmeter-2.11.tgz

EXPOSE 1099
CMD apache-jmeter-2.11/bin/jmeter-server 

