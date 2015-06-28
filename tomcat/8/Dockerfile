FROM tecris.org:5000/jdk8

# based on https://registry.hub.docker.com/_/tomcat/


ENV CATALINA_HOME /usr/local/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH

ENV TOMCAT_MAJOR 8
ENV TOMCAT_VERSION 8.0.23
# ENV TOMCAT_TGZ_URL https://www.apache.org/dist/tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin
ENV TOMCAT_TGZ_URL http://192.168.1.66/repo/packages
RUN wget -qO- "$TOMCAT_TGZ_URL/apache-tomcat-$TOMCAT_VERSION.tar.gz" | tar xvz -C /usr/local
RUN ln -s /usr/local/apache-tomcat-8.0.23 $CATALINA_HOME

EXPOSE 8080

CMD ["/usr/local/tomcat/bin/catalina.sh", "run"]