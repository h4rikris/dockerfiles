FROM ubuntu:latest
RUN apt-get -y update && apt-get install -y default-jre default-jdk wget
RUN wget http://archive.apache.org/dist/tomcat/tomcat-7/v7.0.53/bin/apache-tomcat-7.0.53.tar.gz -O /opt/tomcat.tar.gz \
		&& mkdir /opt/tomcat \
		&& tar -xvf /opt/tomcat.tar.gz -C /opt/tomcat/ --strip-components=1
ENV CATALINA_HOME /opt/tomcat
ENV JAVA_HOME /usr/lib/jvm/java-8-openjdk-amd64
EXPOSE 8080
CMD ["/opt/tomcat/bin/catalina.sh", "run"]