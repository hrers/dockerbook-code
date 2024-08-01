# 基于Ubuntu 镜像
FROM ubuntu:18.0
LABEL maintainer="james@example.com"
ENV REFRESHED_AT 2014-06-01
# 安装必要的软件
RUN apt-get -qq update && apt-get -qq install ruby ruby-dev build-essential redis-tools
RUN gem install --no-rdoc --no-ri json redis
RUN gem install --no-rdoc --no-ri sinatra -v 2.2.2
# 创建目录用于存放应用程序
RUN mkdir -p /opt/webapp

EXPOSE 4567
# 指定/opt/webapp/bin/webapp 座位Web应用程序的启动文件,容器启动时会执行这个文件
CMD [ "/opt/webapp/bin/webapp" ]
