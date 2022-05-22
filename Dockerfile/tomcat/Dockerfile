# Pull centos from dockerhub
FROM centos:latest  
#install java
RUN yum install java -y
#create /opt/tomcat directory
RUN mkdir /opt/tomcat
# change work directory to /opt/tomcat 
WORKDIR /opt/tomcat
#Download tomcat packages
ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.63/bin/apache-tomcat-9.0.63.tar.gz .
#Extract tar.gz file
RUN tar -xvzf apache-tomcat-9.0.63.tar.gz
#Rename to tomcat directory
RUN mv apache-tomcat-9.0.63/* /opt/tomcat
#Tell docker that it runs on port 8080
EXPOSE 8080
#start tomcat services
CMD ["/opt/tomcat/bin/catalina.sh", "run"]
