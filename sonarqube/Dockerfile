FROM sonarqube

RUN apk add --no-cache curl

COPY docker-healthcheck /usr/local/bin/

HEALTHCHECK CMD ["docker-healthcheck"]
