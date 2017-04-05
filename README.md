# docker环境配置
pull下来后在根目录执行以下命令即可安装环境

```
#创建或重建镜像
docker-compose build
#启动容器，--build参数创建或重建镜像，-d后台启动容器
docker-compose up --build
```

php 5.6   
扩展gd、pdo_mysql   
phpunit、composer   


mysql 5.6   
账号root   
密码123456   

nginx 1.9   
config：/etc/nginx/sites-enabled   
web：/opt/htdocs   
error_log: /opt/log/nginx/error.log   
access_log: /opt/log/nginx/access.log   