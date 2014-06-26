# Jmeter
#
# VERSION	0.0.1

FROM	ubuntu:12.04
MAINTAINER Jinuk Baek <kuniz37@gmail.com>

RUN apt-get update

RUN apt-get install -y wget openjdk-6-jre openjdk-6-jre-headless

RUN wget http://apache.tt.co.kr//jmeter/binaries/apache-jmeter-2.11.tgz
RUN tar xf apache-jmeter-2.11.tgz

CMD echo 0 > /proc/sys/net/ipv6/bindv6only

ENV RMI_LOCALHOSTNAME 127.0.0.1
ENV RMI_LOCALPORT 40000
ENV SERVER_PORT 30000

EXPOSE 1099
CMD apache-jmeter-2.11/bin/jmeter -s -j jmeter-server.log -Dserver.rmi.localhostname=${RMI_LOCALHOSTNAME} -Dserver.rmi.localport=${RMI_LOCALPORT} -Dserver_port=${SERVER_PORT} -Djava.rmi.server.hostname=${RMI_LOCALHOSTNAME}

