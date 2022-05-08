FROM cptactionhank/atlassian-confluence:7.4.0
USER root
COPY "atlassian-agent.jar" /opt/atlassian/confluence/
COPY localtime /etc/localtime
RUN echo 'export CATALINA_OPTS="-javaagent:/opt/atlassian/confluence/atlassian-agent.jar ${CATALINA_OPTS}"' >> /opt/atlassian/confluence/bin/setenv.sh
