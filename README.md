https://my.oschina.net/u/3375733/blog/1591091
https://www.runoob.com/docker/docker-install-nginx.html

# docker pull nginx -------- nginx 为选定需要pull到系统中的官方 nginx 镜像
docker pull nginx

# 使用 docker ps -a 命令即可列出所有（包括已停止的）的容器
docker ps -a

# 启动一个名为nginx81(名字自己根据需求起名字，一般见名知意即可) 的容器 
docker run --name nginx81 -d -p 80:80 -v /Users/jren/nginx_Docker_Test/html:/usr/share/nginx/html nginx

# 默认容器对这个目录有可读写权限，可以通过指定ro，将权限改为只读（readonly）
docker run --name nginx81 -d -p 80:80 -v /Users/jren/nginx_Docker_Test/html:/usr/share/nginx/html:ro nginx




curl http://localhost
