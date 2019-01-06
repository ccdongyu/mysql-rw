## 接口

GET
http：//${ip}:8080/add?id=${id}&username=${username}&userpass=${userpass}
功能：新增一个用户


GET
http：//${ip}8080/select
功能：查看所有用户

**还有其他接口，如果需要可以再完善文档**

## 配置

在云服务器的~/app目录下有两个配置，docker-compose.yml和_docker-compose.yml，分别代表读写分离和独立读写数据库。在测试完读写分离后，通过docker-compose -f docker-compose.yml down 命令移除之前的容器，再通过docker-compose -f _docker-compose.yml up -d 把独立读写数据库的容器都启动起来。
