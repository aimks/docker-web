# 使用 Docker 快速搭建 web 开发环境
由于目前我使用的开发环境很多个，每次构建环境都要花很长时间，后面，我了解到 docker 可以快速构建环境，于是我学习了 docker 开发，构建了这个一键环境，后面还会加入更多的东西。
## 为什么要使用docker
- 更高效的利用系统资源
- 更快速的启动时间
- 一致的运行环境
- 持续交付和部署
- 更轻松的迁移
- 更轻松的维护和扩展
## 支持的开发环境
- php5.6
- php7.2
- python2
- python3
- node
## 安装的镜像
- portainer/portainer:latest
- nginx:latest
- php:5.6-fpm
- php:7.2-fpm
- mysql:5.6
- redis:latest
- python:2.7
- python:3.7
- node:latest
## 安装步骤
### 第一步，安装软件
- Git
- Docker
- Docker-compose
### 第二步，获取项目代码

```
git clone https://github.com/aimks/docker-web.git
```

### 第三步，运行容器

```
cd docker-web
docker-compose up -d
```
```
Creating docker-web_portainer_1 ... done
Creating docker-web_mysql_1     ... done
Creating docker-web_redis_1     ... done
Creating docker-web_php72_1     ... done
Creating docker-web_php56_1     ... done
Creating docker-web_python2_1   ... done
Creating docker-web_python3_1   ... done
Creating docker-web_node_1      ... done
Creating docker-web_nginx_1     ... done
```
### 第四步，进入portainer管理项目
- 访问127.0.0.1:8001

![portainer](portainer.png)

### 第五步，配置主机host

```
127.0.0.1           www.php56.com
127.0.0.1           www.php72.com
127.0.0.1           www.node.com
```
### 第六步，访问web地址
- 访问http://www.php56.com:8002/

![php56](php56.png)
- 访问http://www.php72.com:8002/

![php72](php72.png)
- 访问http://www.node.com:8002/

![node](node.png)

## Todo
- 使用dockfile




