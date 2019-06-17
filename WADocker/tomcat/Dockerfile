FROM tomcat:8-jdk8-openjdk
RUN useradd -s /bin/bash -d $CATALINA_HOME -p tomcat tomcat && \
    chown -R tomcat:tomcat $CATALINA_HOME/webapps && \
    chown -R tomcat:tomcat $CATALINA_HOME/webapps/**/*
USER tomcat
WORKDIR $CATALINA_HOME
COPY ./ProyectoFinal.war ./webapps/ProyectoFinal.war
