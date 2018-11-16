FROM ubuntu
RUN apt-get update
RUN apt-get install -y nginx

RUN ln -sf /dev/stdout /var/log/nginx/access.log
RUN ln -sf /dev/stderr /var/log/nginx/error.log

ADD ./ /rails
WORKDIR /rails

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]