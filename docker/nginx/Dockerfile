FROM nginx:1.18

RUN rm /etc/nginx/conf.d/default.conf

COPY ./docker/nginx/nginx.conf /etc/nginx/nginx.conf
COPY ./docker/nginx/conf.d/default.conf /etc/nginx/conf.d/default.conf

RUN mkdir -p /app
COPY ./src/index.html /app/index.html
WORKDIR /app

CMD ["nginx"]

EXPOSE 80