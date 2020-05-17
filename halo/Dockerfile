FROM adoptopenjdk/openjdk8-openj9
VOLUME /tmp

ARG PORT=8090
ARG TIME_ZONE=Asia/Shanghai

ENV TZ=${TIME_ZONE}
ENV JAVA_OPTS="-Xms256m -Xmx256m"

ADD https://dl.halo.run/release/halo-1.3.2.jar /home/halo.jar

EXPOSE ${PORT}

ENTRYPOINT java ${JAVA_OPTS} -Djava.security.egd=file:/dev/./urandom -server -jar /home/halo.jar
