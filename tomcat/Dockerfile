FROM tomcat:jdk8-openjdk

ADD tomcat-users.xml /usr/local/tomcat/conf

ADD manager/context.xml /usr/local/tomcat/webapps/manager/META-INF/context.xml

ADD host-manager/context.xml /usr/local/tomcat/webapps/host-manager/META-INF/context.xml

RUN rm -rf /usr/local/tomcat/webapps/examples 

VOLUME ["/usr/local/tomcat/logs"]

VOLUME ["/usr/local/tomcat/webapps"]

EXPOSE 8009

EXPOSE 8080
