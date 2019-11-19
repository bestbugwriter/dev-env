FROM mcr.microsoft.com/java/jdk:8u222-zulu-centos

RUN yum install wget curl mysql-connector-java python -y && wget http://public-repo-1.hortonworks.com/ambari/centos7/2.x/updates/2.7.3.0/ambari.repo -O /etc/yum.repos.d/ambari.repo && yum install ambari-server -y

RUN ambari-server setup --jdbc-db=mysql --jdbc-driver=/usr/share/java/mysql-connector-java.jar --java-home=/usr/lib/jvm/zulu-8-azure --enable-lzo-under-gpl-license -s

ADD ambari.properites /etc/ambari-server/conf/ambari.properties
