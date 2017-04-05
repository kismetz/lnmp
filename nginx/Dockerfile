#镜像
From nginx:1.9

#ADD命令可将文件或文件夹指定到容器里指定的目录
ADD nginx.conf /etc/nginx/nginx.conf
ADD sites-enabled/* /etc/nginx/sites-enabled/

#启动命令，第一次启动执行的命令
RUN mkdir /opt/htdocs && mkdir -p /opt/log/nginx
RUN chown -R www-data:www-data /opt/htdocs /opt/log/nginx

#创建挂载点
VOLUME ["/opt", "/etc"]