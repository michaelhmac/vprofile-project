FROM mysql:8.0.33
LABEL "Project"="vprofile"
LABEL "Author"="Michael"

ENV MYSQL_ROOT_PASSWORD='vprodbpass'
ENV MYSQL_DATABASE='accounts'

COPY db_backup.sql docker-entrypoint-initdb/db_backup.sql
