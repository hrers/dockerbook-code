FROM ubuntu:18.04
LABEL maintainer="james@example.com"
ENV REFRESHED_AT 2014-06-01
# 安装nginx 
RUN apt-get -qq update && apt-get -qq install nginx
# 创建目录
RUN mkdir -p /var/www/html/website
# 将我们的静态文件复制到容器中
ADD nginx/global.conf /etc/nginx/conf.d/
ADD nginx/nginx.conf /etc/nginx/
# 公开镜像的80 端口
EXPOSE 80
