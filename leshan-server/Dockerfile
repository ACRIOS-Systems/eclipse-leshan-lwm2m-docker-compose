FROM openjdk:17-alpine
MAINTAINER Bertrand Roussel <broussel@sierrawireless.com>

RUN mkdir -p /opt/leshan
RUN adduser -S -h /opt/leshan -s /sbin/nologin leshan

EXPOSE 5683 5684 5783 5784 8080 8081

ADD run.sh /opt/leshan/
ADD https://ci.eclipse.org/leshan/job/leshan-ci/job/master/lastSuccessfulBuild/artifact/leshan-server-demo.jar /opt/leshan/

RUN chown -R leshan:nogroup /opt/leshan
RUN chmod 777 /opt/leshan/run.sh
USER leshan
WORKDIR /opt/leshan
#ENTRYPOINT ["/bin/sh"]
ENTRYPOINT ["/opt/leshan/run.sh"]
