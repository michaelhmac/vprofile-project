FROM mysql:8.0.33
LABEL "Project"="vprofile"
LABEL "Author"="Michael"

ENV MYSQL_ROOT_PASSWORD='vprodbpass"
ENV MYSQL_DATABASE='accounts"

ADD db_backup.mysql docker-entrypoint-initdb/db_backup.sql
