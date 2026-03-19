FROM mcr.microsoft.com/mssql/server:2017-CU1-ubuntu

ENV ACCEPT_EULA=Y \
    MSSQL_SA_PASSWORD=DockerCon!!!

WORKDIR /init
COPY init-db.* ./

RUN chmod +x ./init-db.sh
RUN /opt/mssql/bin/sqlservr & ./init-db.sh