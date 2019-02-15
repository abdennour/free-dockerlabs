FROM ubuntu:16.04
LABEL maintainer="mail@abdennoor.com"
ENV REFRESHED_AT 2019-02-14
RUN apt-get -yqq update
RUN apt-get -yqq install wget
VOLUME [ "/var/lib/tomcat7/webapps/" ]
WORKDIR /var/lib/tomcat7/webapps/
ENTRYPOINT [ "wget" ]
CMD [ "-?" ]
