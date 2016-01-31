FROM mysql:5.6

ENV MYSQL_ROOT_PASSWORD=root
ENV MYSQL_DATABASE=openmrs
ENV MYSQL_USER=openmrs
ENV MYSQL_PASSWORD=openmrs

RUN apt-get update && apt-get install -y curl unzip; \
    curl -L http://sourceforge.net/projects/openmrs-platform-docker/files/v1.11.5/openmrs-platform-database.sql.zip/download \
         -o /tmp/openmrs-platform-database.sql.zip; \
    unzip /tmp/openmrs-platform-database.sql.zip -d /docker-entrypoint-initdb.d; \
    rm /tmp/openmrs-platform-database.sql.zip
