FROM sonarqube

COPY --chown=sonarqube:sonarqube docker-healthcheck /usr/local/bin/

HEALTHCHECK CMD ["docker-healthcheck"]
