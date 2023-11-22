# Utiliser Debian Buster comme image de base
FROM debian:buster

RUN apt-get update -y && apt-get install mariadb-server -y

COPY ./tools/50-server.cnf /etc/mysql/mariadb.conf.d/

ENV MYSQL_ROOT_PASSWORD=password123
ENV MYSQL_DATABASE=exemple_db
ENV MYSQL_USER=user1
ENV MYSQL_PASSWORD=user1password

EXPOSE 3306

COPY ./tools/init-db.sh /usr/local/bin/init-db.sh
RUN chmod +x /usr/local/bin/init-db.sh

ENTRYPOINT ["init-db.sh"]
