ARG MYSQL_VERSION

FROM mysql:${MYSQL_VERSION}

COPY ./my.cnf /etc/mysql/my.cnf
RUN chmod a-w /etc/mysql/my.cnf
