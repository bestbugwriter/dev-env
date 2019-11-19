FROM openjdk:8-alpine

RUN apk add curl && curl -SL http://archive.apache.org/dist/hive/hive-3.1.2/apache-hive-3.1.2-bin.tar.gz | tar -zxC /home/

RUN ln -s /home/apache-hive-3.1.2-bin /home/hive
ADD https://repo1.maven.org/maven2/mysql/mysql-connector-java/5.1.40/mysql-connector-java-5.1.40.jar /home/hive/lib/mysql-connector-java.jar
ADD hive-site.xml /home/hive/conf/hive-site.xml

WORKDIR /home/hive/
#ENTRYPOINT [ "/home/hive/bin/hive" ]
