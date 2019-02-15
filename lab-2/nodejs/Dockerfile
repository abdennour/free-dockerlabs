FROM node:11.9
LABEL maintainer="mail@abdennoor.com"

ENV REFRESHED_AT 2019-02-14
RUN apt-get -yqq update
#RUN apt-get -yqq install nodejs npm
#RUN ln -s /usr/bin/nodejs /usr/bin/node
RUN mkdir -p /var/log/nodeapp
ADD nodeapp /opt/nodeapp/
WORKDIR /opt/nodeapp
RUN npm install
VOLUME [ "/var/log/nodeapp" ]
EXPOSE 3000
ENTRYPOINT [ "node", "server.js" ]
