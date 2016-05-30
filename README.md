# AMH4.5 基于AMH4.2修改版

转载自：http://soft.im/WebPanel/AMH4.5/  给自己留个备份

4.5版本是在官方4.2脚本基础上，二次增强开发出来的民间版本；
AMH4.5新增Mysql,Mariadb选择安装,实现mysql-5.6.2,mysql-5.7.9,mariadb-5.5.47,mariadb-10.1.11版本数据库选择安装
1.新增Mysql,Mariadb选择安装,实现mysql-5.6.2,mysql-5.7.9,mariadb-5.5.47,mariadb-10.1.11版本数据库选择安装
2.新增php7.0,实现php 5.3 5.4 5.5 5.6 7.0所有版本虚拟主机级的一键切换。（默认安装php5.6）
3.mysql数据目录迁移到/home/mysqldata,方便统一管理和多分区用户重装系统能保留home分区下的重要数据。
4.部分bug修正 以下为旧记录：
1.nginx升级到1.9.6,配合新版nginx,openssl编译1.0.2d(nginx专用)
2.支持http/2(目前测试中，站点conf文件需要手动加入配置，参考nginx.org)
3.支持stream反代
4.支持nginx反代和cache_purge(测试功能，配置文件需手动)
5.修复pid路径错误在服务器重启后不能启动php的错误
6.其他一些bug修复

启用http/2的方法：
模块下载个bbshijiessl，然后用这个模块配置好ssl证书
手工找到/usr/local/nginx/conf/vhost/域名.conf 里面最下面把listen 443; 改成 listen
443 ssl http2;面板里重启下网站即可

安装方法：

# apt-get install screen (debian)

# yum -y install screen (centos)

# screen -S amh

# wget https://github.com/ttkea/AMH4.5/blob/master/amh.sh && chmod 775 amh.sh && ./amh.sh 2>&1 | tee amh.log





