FROM ubuntu

RUN apt-get update \
    && apt-get install -y locales \
    && locale-gen ja_JP.UTF-8 \
    && echo "export LANG=ja_JP.UTF-8" >> ~/.bashrc
RUN apt-get install -y mysql-client mysql-server

ENV MYSQL_ROOT_PASSWORD=root
ENV MYSQL_USER=root
ENV MYSQL_PASSWORD=root

COPY ./sqlfile ./sqlfile
COPY ./my.cnf /etc/mysql/conf.d

RUN chmod 644 /etc/mysql/conf.d/my.cnf

EXPOSE 3306
