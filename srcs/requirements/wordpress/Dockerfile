FROM debian:buster

RUN apt update -y; 

RUN apt install php-fpm php-mysql -y

RUN apt install curl -y

COPY ./tools/wp-config.php /

COPY ./tools/script.sh /

CMD ["/script.sh"]