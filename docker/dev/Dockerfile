FROM phpdockerio/php:8.2-fpm

RUN apt update
RUN apt install -y git &&\
    apt -y --no-install-recommends install php8.2-xdebug php8.2-sqlite3 &&\
    curl -sS https://get.symfony.com/cli/installer | bash &&\
    mv /root/.symfony5/bin/symfony /usr/local/bin/symfony

CMD [ "/bin/sh", "./docker/dev/docker-start.sh" ]

#ENTRYPOINT ["tail", "-f", "/dev/null"]