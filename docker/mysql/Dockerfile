ARG MYSQL_VERSION=8.0

FROM mysql:${MYSQL_VERSION}

COPY ./my.cnf /etc/mysql/my.cnf
RUN chmod a-w /etc/mysql/my.cnf
