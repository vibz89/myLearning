FROM tomcat:8.0-alpine

ADD sample.war /usr/local/tomcat/webapps/

#expose the port
EXPOSE 8080

#specify the command which will keep it alive
CMD ["catalina.sh", "run"]