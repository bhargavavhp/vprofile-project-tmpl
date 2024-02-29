FROM mysql:8.0.33
LABEL "Project"="vprofile"
LABEL "Application"="DataBase"
LABEL "Maintainer"="bhargavavhp"
WORKDIR /app
COPY . .
ENV MYSQL_DATABASE="accounts"
ENV MYSQL_ROOT_PASSWORD="root"
ADD db_backup.sql docker-entrypoint-initdb.d/db_backup.sql 
