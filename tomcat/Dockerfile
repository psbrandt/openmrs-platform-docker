FROM tomcat:7

ADD openmrs-runtime.properties /usr/local/tomcat/openmrs-runtime.properties
ADD setenv.sh /usr/local/tomcat/bin/setenv.sh

RUN apt-get update && apt-get install -y curl unzip; \
    curl -L http://sourceforge.net/projects/openmrs/files/releases/OpenMRS_Platform_1.11.5/openmrs.war/download \
         -o /usr/local/tomcat/webapps/openmrs.war;
