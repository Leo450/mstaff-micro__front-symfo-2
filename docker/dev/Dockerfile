FROM phpdockerio/php:8.1-fpm

RUN apt update
RUN apt install -y git &&\
    apt -y --no-install-recommends install php8.1-xdebug php8.1-bcmath php8.1-bz2 php8.1-intl php8.1-mcrypt php8.1-mysql php8.1-sqlite3 php8.1-redis &&\
    curl -sS https://get.symfony.com/cli/installer | bash &&\
    mv /root/.symfony5/bin/symfony /usr/local/bin/symfony

CMD [ "/bin/sh", "./docker/dev/docker-start.sh" ]

#ENTRYPOINT ["tail", "-f", "/dev/null"]