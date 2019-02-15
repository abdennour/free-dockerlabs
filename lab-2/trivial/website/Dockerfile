FROM ubuntu:16.04

RUN mkdir -p /usr/share/nginx/html

WORKDIR /usr/share/nginx/html

VOLUME ["/usr/share/nginx/html"]

COPY index.html .

ENTRYPOINT bash

#CMD ["tail", "-f", "/dev/null"]
