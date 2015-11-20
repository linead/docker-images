FROM linead/maven

MAINTAINER "Daniel Fullarton" <linead@gmail.com>

ENV SPRING_BOOT_REPO https://github.com/spring-projects/spring-boot.git

RUN mkdir /tmp/app && git clone $SPRING_BOOT_REPO /tmp/app
RUN cd /tmp/app/spring-boot-starters && /usr/share/java/maven/bin/mvn dependency:go-offline
RUN rm -rf /tmp/app

VOLUME ["/var/maven"]
