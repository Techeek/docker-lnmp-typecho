# docker-lnmp-typecho
*本项目修改自[hteen/docker-lnmp](https://github.com/hteen/docker-lnmp)*

项目包含(mysql、redis、php、nginx)版本均为docker默认。  
默认开启80、443、3306端口。  
数据库地址：mysql  
数据库root默认密码：123456  
数据库登录默认密码：123456  
默认数据库名：typecho  
默认数据库：typecho  
更改数据库请参考docker-compose.yml文件  

使用方法(以Ubuntu16.04LTS为例)：
* 1、首先登录您的服务器，确保您的服务器权限。输入以下命令：
```linux
sudo git clone https://github.com/Techeek/docker-lnmp-typecho
```
* 2、将项目clone到本地后请安装docker、docker.io、docker-compose,这里我们使用国内的daocloud加速安装，同时我们安装daocloud加速
```linux
sudo apt install docker
sudo apt install docker.io
sudo apt install docker-compose
curl -sSL https://get.daocloud.io/daotools/set_mirror.sh | sh -s http://f4a8a473.m.daocloud.io
```

* 3、接下来运行项目即可搭建你的网站啦！
```linux
cd docker-lnmp-typecho
sudo docker-compose up -d
```
注意：部署网站前请先更改Nginx目录下nginx.conf文件

> Bug:
2017年03月20日：暂时无法使用腾讯云CDN服务，会造成无法登录后台。

> Fix Bug：  
2017年03月15日：优化对SSL证书的支持  
2017年03月14日：优化原项目docker-lnmp对typecho的支持  
2017年03月14日：优化数据库账户及密码
2017年08月28日：修复docker卡死无法安装问题