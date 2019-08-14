FROM tomcat:jdk8-openjdk

ADD tomcat-users.xml /usr/local/tomcat/conf
ADD manager/context.xml /usr/local/tomcat/webapps/manager/META-INF/context.xml
ADD host-manager/context.xml /usr/local/tomcat/webapps/host-manager/META-INF/context.xml
ADD gs-maven-0.1.0.war /usr/local/tomcat/webapps
RUN rm -rf /usr/local/tomcat/webapps/examples 

EXPOSE 8009
EXPOSE 8080
