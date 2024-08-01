# 将当前目录下的webapp 文件夹挂载到容器中的/opt/webapp 上,也就是我们的程序
# docker run -d -p 4567 --name -v $PWD/webapp:/opt/webapp awua/sinatra
# chmod +x webapp/bin/webapp 为程序分配可执行权限

