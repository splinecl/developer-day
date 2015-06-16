FROM jboss/wildfly
VOLUME /tmp
ADD developer-day.war /opt/jboss/wildfly/standalone/deployments/
RUN /opt/jboss/wildfly/bin/add-user.sh admin Admin#70365 --silent
CMD ["/opt/jboss/wildfly/bin/standalone.sh", "-b", "0.0.0.0", "-bmanagement", "0.0.0.0", "-Dspring.data.mongodb.host=db", "-Dspring.data.mongodb.port=27017"]