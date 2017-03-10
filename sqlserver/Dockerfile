FROM microsoft/mssql-server-linux

LABEL maintainer "the@grillazz.com"

RUN apt-get update && apt-get install -y  \
	curl \
	apt-transport-https

#
# https://docs.microsoft.com/en-us/sql/connect/odbc/linux/installing-the-microsoft-odbc-driver-for-sql-server-on-linux
# in article above you can find proper url to install packages appropirate to your linux version
#
RUN curl https://packages.microsoft.com/keys/microsoft.asc | apt-key add -
RUN curl https://packages.microsoft.com/config/ubuntu/16.04/prod.list > /etc/apt/sources.list.d/mssql-release.list
RUN apt-get update
RUN ACCEPT_EULA=Y apt-get install -y \
    mssql-tools

RUN apt-get install -y locales \
    && echo "en_US.UTF-8 UTF-8" > /etc/locale.gen \
    && locale-gen

ENV PATH="/opt/mssql-tools/bin:${PATH}"
ENV SA_PASSWORD=Alaska2017
ENV ACCEPT_EULA=Y

COPY docker-healthcheck /usr/local/bin/
RUN chmod +x /usr/local/bin/db-healthcheck
HEALTHCHECK CMD ["docker-healthcheck"]



