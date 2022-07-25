FROM ubuntu

RUN apt-get update \
    && apt-get install -y locales \
    && locale-gen ja_JP.UTF-8 \
    && echo "export LANG=ja_JP.UTF-8" >> ~/.bashrc
RUN apt-get install -y mysql-client mysql-server

ENV MYSQL_ROOT_PASSWORD=root
ENV MYSQL_USER=root
ENV MYSQL_PASSWORD=root

# RUN chmod 644 /etc/mysql/conf.d/mysql.cnf
RUN chmod 644 /etc/mysql/mysql.conf.d/mysqld.cnf

# COPY ./sqlfile ./sqlfile
# COPY ./mysql.cnf /etc/mysql/conf.d/mysql.cnf
# COPY ./mysql.cnf /etc/mysql/mysql.conf.d/mysql.cnf
# COPY ./mysqld.cnf /etc/mysql/mysql.conf.d/mysqld.cnf


EXPOSE 3306


