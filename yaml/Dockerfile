FROM nginx:1.17.2-alpine

COPY . /home/nginx

RUN cd /home/nginx; \
    mv docker-entrypoint.sh /usr/local/bin; \
    chmod +x /usr/local/bin/docker-entrypoint.sh;

RUN apk update
RUN apk add curl

ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["nginx", "-g", "daemon off;"]

