FROM tomcat:latest

RUN apt-get update \
    && apt-get install -y locales \
    && locale-gen ja_JP.UTF-8 \
    && echo "export LANG=ja_JP.UTF-8" >> ~/.bashrc

COPY ./tomcat/KIfU4.war /usr/local/tomcat/webapps

# CMD [ "catalina.sh", "run" ]


