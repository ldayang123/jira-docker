FROM atlassian/jira-software:8.14
#USER root
COPY atlassian-agent.jar /opt/atlassian/jira/
COPY mysql-connector-java-8.0.28.jar /opt/atlassian/jira/lib/
RUN echo 'export CATALINA_OPTS="-javaagent:/opt/atlassian/jira/atlassian-agent.jar ${CATALINA_OPTS}"' >> /opt/atlassian/jira/bin/setenv.sh
#RUN mv /opt/atlassian/jira/atlassian-jira/WEB-INF/lib/atlassian-extras-3.2.jar /opt/atlassian/jira/atlassian-jira/WEB-INF/lib/atlassian-extras-3.2.jar.bak
#COPY atlassian-extras-3.1.2.jar /opt/atlassian/jira/atlassian-jira/WEB-INF/lib/
COPY localtime /etc/localtime
VOLUME ["/opt/atlassian", "/var/atlassian"]
