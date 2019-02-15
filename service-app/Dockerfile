#
# app
#

FROM tomcat:6

ENV DEFAULT_WAR_NAME=app-1.0.0.war
ENV FAKE_WAR_NAME=appFAKE.war
ENV DEPLOY_WAR_NAME=app.war

COPY ./app*.war /tmp/
RUN mv /tmp/$DEFAULT_WAR_NAME /usr/local/tomcat/webapps/$DEPLOY_WAR_NAME;

COPY ./start-app.sh /root/start-app.sh

CMD ["/root/start-app.sh"]
