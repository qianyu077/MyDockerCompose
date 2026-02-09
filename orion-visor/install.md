# 进去我们需要安装这个工具的目录
cd /vol1/1000/xxxx
# 克隆项目到我们本地，git飞牛自带不需要我们自己安装
## github
git clone --depth=1 https://github.com/dromara/orion-visor
## gitee
git clone --depth=1 https://gitee.com/dromara/orion-visor
## atomgit
git clone --depth=1 https://atomgit.com/dromara/orion-visor
# 进去刚克隆下载的项目
cd orion-visor/
# 复制一分配置文件，以.开头的文件飞牛会自动隐藏可能看不见，问题不大，按照下面执行命令就行
cp .env.example .env

``bash
### VOLUME_BASE             你希望数据持久化保存的目录, 如果不提前创建将以 docker 进程宿主身份创建 (通常是 root)

### SERVICE_PORT            你希望服务监听的端口
### SPRING_PROFILES_ACTIVE  后端启动的环境

### DEMO_MODE               演示模式

### API_CORS                是否允许跨域
### API_HOST                对外服务主机地址 (必须要修改, 需要改为 agent 访问 <ip>:9200 可以通的网络地址)
### API_URL                 对外服务接口地址 (API_URL 不满足可以进行修改)
### API_IP_HEADERS          获取 IP 的请求头
### API_EXPOSE_TOKEN        对外服务 token
### SECRET_KEY              加密密钥

### NGINX_SERVICE_HOST      nginx 服务所在的主机
### NGINX_SERVICE_PORT      nginx 服务监听的端口

### MYSQL_HOST              mysql 服务所在的主机, 如果你没有现有的 MySQL 请保持值为 mysql, 如果你有自部署的请在 docker-compose.yaml 中移除 services.mysql 以节约性能
### MYSQL_PORT              mysql 监听的端口
### MYSQL_DATABASE          mysql 数据库
### MYSQL_USER              mysql 用户名
### MYSQL_PASSWORD          mysql 用户密码
### MYSQL_ROOT_PASSWORD     mysql root 密码

### REDIS_HOST              redis 服务所在的主机, 如果你没有现有的 Redis 请保持值为 redis, 如果你有自部署的请在 docker-compose.yaml 中移除 services.redis 以节约性能
### REDIS_PASSWORD          redis 密码
### REDIS_DATABASE          redis 数据库
### REDIS_DATA_VERSION      redis 数据版本

### GUACD_HOST              guacd 服务所在的主机, 如果你没有现有的 Redis 请保持值为 redis, 如果你有自部署的请在 docker-compose.yaml 中移除 services.guacd 以节约性能
### GUACD_PORT              guacd 端口
### GUACD_DRIVE_PATH        guacd 数据挂载目录

### INFLUXDB_ENABLED        是否启用 influxdb (若不需要监控可以设置为 false)
### INFLUXDB_HOST           influxdb 服务所在的主机, 如果你没有现有的 influxdb 请保持值为 influxdb, 如果你有自部署的请在 docker-compose.yaml 中移除 services.influxdb 以节约性能
### INFLUXDB_PORT           influxdb 端口
### INFLUXDB_ORG            influxdb 组织
### INFLUXDB_BUCKET         influxdb bucket
### INFLUXDB_TOKEN          influxdb token   
### INFLUXDB_ADMIN_USERNAME influxdb 控制台用户名
### INFLUXDB_ADMIN_PASSWORD influxdb 控制台密码
``
