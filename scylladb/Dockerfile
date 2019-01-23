FROM scylladb/scylla
COPY docker-healthcheck /usr/local/bin/
RUN chmod a+x /usr/local/bin/docker-healthcheck
HEALTHCHECK CMD ["docker-healthcheck"]
