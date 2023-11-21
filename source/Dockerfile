FROM nginxinc/nginx-unprivileged:bookworm-perl
USER root
RUN apt-get update && \
    apt-get install -y
COPY nginx/nginx.conf /etc/ngnix/nginx.conf
COPY nginx/default.conf /etc/nginx/conf.d/default.conf
WORKDIR /app
COPY frontend/ .
USER 1001
