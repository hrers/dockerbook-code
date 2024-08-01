# build the images
sudo docker build -t awua/nginx .
# run the images
docker run -d -p 80 --name website -v $PWD/website:/var/www/html/website awua/nginx nginx
# 不适用随机的方式,而是使用固定映射为宿主机的80 端口
# docker run -d -p 80:80 --name website -v $PWD/website:/var/www/html/website awua/nginx nginx
# 代码的修改
# 采用挂载的方式 -v $PWD/website:/var/www/html/website a 代码的修改会直接被 docker容器读取,不需要重新构建容器或重启容器


