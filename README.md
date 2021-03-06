***目前目录比较乱，多了以后再整理***

履历 / 学历 / 技术 / 人脉

# 算法

[算法小抄](https://labuladong.gitbook.io/algo/)   

[时间复杂度分析](https://www.jianshu.com/p/31688b6b3220)

[回溯算法](https://mp.weixin.qq.com/s/0EQx5AkybSi1xtpZCM2fuQ)

# 数据结构	

[HashMap](https://blog.csdn.net/zhengwangzw/article/details/104889549?depth_1-utm_source=distribute.pc_category.none-task&request_id=&utm_source=distribute.pc_category.none-task)

[ArrayList](https://blog.csdn.net/sinat_33921105/article/details/103773539)

# lambda

[函数式编程](https://blog.csdn.net/qq_41907991/article/details/101787916)

# 幂等性	

[api幂等策略分析](https://www.cnblogs.com/geyifan/p/6128425.html)		

# MQ

[技术选型](https://www.jianshu.com/p/fdd94be6037a)

[RabbitMQ基础](https://blog.csdn.net/qq_41907991/article/details/89050473)

[RabbitMQ中的交换机跟工作模式](https://blog.csdn.net/qq_41907991/article/details/89062776)

[TTL（存活时间）Dead Letter Exchanges（死信交换机）](https://blog.csdn.net/qq_41907991/article/details/89072519)

[spring-cloud-stream](https://blog.csdn.net/qq_32734365/article/details/81413218)

[push模式下,如何保证消息一定被消费](https://www.cnblogs.com/zjg-gwx/p/10868264.html)	

[pull模式下,如何保证消息一定被消费]()		

[如何保证消息不丢失]()

[如何保证消息消费的幂等性]()		

[使用消息中间件时，如何保证消息仅仅被消费一次？](https://www.toutiao.com/i6803224493616529927/)		

[如何保证消息的顺序性](https://www.jianshu.com/p/02fdcb9e8784)

[消息积压在消息队列里怎么办](https://www.jianshu.com/p/07b2169bef49)

# 多线程

[ThreadLocal](https://blog.csdn.net/sinat_33921105/article/details/103295070)

[指令重排]()

# 锁

[什么是乐观锁，什么是悲观锁](https://www.jianshu.com/p/d2ac26ca6525)	

# 事务,一致性

[数据库与redis一致性](https://www.jianshu.com/p/798d3b0b980f)

[分布式事务](https://www.jianshu.com/p/60092f498374)

# 分布式

[分布式服务接口请求的顺序性如何保证](https://www.jianshu.com/p/64e3ccee339e)

[zookeeper都有哪些使用场景](https://www.jianshu.com/p/a4d72efd9967)

[面试官：兄弟，谈谈你对分布式系统原理的理解](https://www.toutiao.com/a6817228688178807309)

# 缓存

```
docker pull redis:6.0.1

docker run -p 6379:6379 --name myredis -v /usr/local/docker/redis.conf:/etc/redis/redis.conf -v /usr/local/docker/data:/data -d redis redis-server /etc/redis/redis.conf --appendonly yes

```

[Redis 的订阅发布模式]()

# WebSocket

# Netty

# 网关

[API Gateway](https://www.cnblogs.com/paxlyf/p/11119159.html)

[斗鱼 API 网关演进之路](http://www.upyun.com/opentalk/425.html)

# MYSQL

[MySQL的万字总结（缓存，索引，Explain，事务，redo日志等](https://www.jianshu.com/p/2530d1185778)

[关于MySQL索引的几件小事](https://www.jianshu.com/p/b1eadcad1043)

[慢SQL，Explain](https://www.cnblogs.com/qmfsun/p/4844472.html)

[docker 方式](https://dev.mysql.com/doc/refman/5.7/en/docker-mysql-getting-started.html)

```
# 运行镜像创建容器
docker run --name mysql-server \
-v /val/lib/mysql/data:/var/lib/mysql \
-v /etc/mysql/conf.d:/etc/mysql/conf.d \ 
-e MYSQL_ROOT_PASSWORD=000000s \
-p 3306:3306 \
-d mysql/mysql-server:5.7

# 进入容器内
docker exec -it mysql-server

# 修改远程访问
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY '000000s' WITH GRANT OPTION;
FLUSH PRIVILEGES;
EXIT;

# 重启
docker restart mysql-server

```

# 容器

[centos7安装docker](https://www.cnblogs.com/yufeng218/p/8370670.html)

[docker 快速搭建 kafka + zookeeper](https://www.jianshu.com/p/ac03f126980e)

[基于docker 快速构建 zk + kafka + flink](https://www.cnblogs.com/1ssqq1lxr/p/10417005.html)

[dk + zk + kafka + flink compose构建文件](docker/zk-kafka-flink/docker-compose.md)

[dk + zk + kafka + flink 相关命令](docker/zk-kafka-flink/cmd.md)

[dk + jenkins](https://www.jianshu.com/p/a70572099eda)

[dk + git + jenkins](https://blog.51cto.com/ganbing/2085769)

[k8s + git + jenkins](https://blog.51cto.com/14154700/2455283)

[Flume+Kafka+Flink+Redis构建大数据实时处理系统：实时统计网站PV、UV展示](https://yq.aliyun.com/articles/635327)

[图形化管理界面 shipyard](http://www.shipyard-project.com)

[k8s 简介和安装](https://blog.51cto.com/14154700/2447761)


```
# docker-compose 安装
> curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
> chmod +x /usr/local/bin/docker-compose
> ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose

# 停止全部容器
docker ps -a | `awk 'NR>1 {print "docker stop ", $1}'`
docker ps -a | `awk 'NR>1 {print "docker rm ", $1}'`

# 删除全部镜像
docker rmi $(docker ps -a -q)
```

# 安全

[token 鉴权](https://www.cnblogs.com/fujingtao5470/p/11573528.html)

[OAuth2 授权](https://www.jianshu.com/p/9d0264d27c3b)

[API 接口应该如何设计？如何保证安全？如何签名？如何防重？](https://mp.weixin.qq.com/s/oJ_0kIKytFOMe7b5-UTgaw)

[HTTPS 的工作原理](https://mp.weixin.qq.com/s/KgddqOxg2D19lFxmIDwmBQ)

```
防止重复提交

对于一些重要的操作需要防止客户端重复提交的(如非幂等性重要操作)，具体办法是当请求第一次提交时将sign作为key保存到redis，并设置超时时间，超时时间和Timestamp中设置的差值相同。

当同一个请求第二次访问时会先检测redis是否存在该sign，如果存在则证明重复提交了，接口就不再继续调用了。如果sign在缓存服务器中因过期时间到了，而被删除了，此时当这个url再次请求服务器时，因token的过期时间和sign的过期时间一直，sign过期也意味着token过期，那样同样的url再访问服务器会因token错误会被拦截掉，这就是为什么sign和token的过期时间要保持一致的原因。拒绝重复调用机制确保URL被别人截获了也无法使用（如抓取数据）。

对于哪些接口需要防止重复提交可以自定义个注解来标记。
```

# Spring

[spring 第一篇](https://blog.csdn.net/weixin_43737917/article/details/105213582)

[spring 第二篇](https://blog.csdn.net/weixin_43737917/article/details/105222054)

# 公开课

[又拍云](https://www.upyun.com/opentalk)

[美团技术](https://tech.meituan.com/)

[阿里系统软件技术](https://www.cnblogs.com/alisystemsoftware/)

# 即时通讯

[WebRTC实时音视频技术基础：基本架构和协议栈](http://www.52im.net/thread-442-1-1.html)

[腾讯技术分享：微信小程序音视频与WebRTC互通的技术思路和实践](http://www.52im.net/thread-1988-1-1.html)

[Websocket]
[分布式WebSocket集群解决方案](https://segmentfault.com/a/1190000017307713)

# canal

[如何基于Canal 和 Kafka，实现 MySQL 的 Binlog 近实时同步？](https://mp.weixin.qq.com/s/YnFrtNDgosEMc_N8YKJp6w)

# Markdown

[语法](https://www.runoob.com/markdown/md-tutorial.html)

[高级用法,UML等](https://www.runoob.com/markdown/md-advance.html)

# Vue

```
# npm库设置为淘宝镜像
npm config set registry https://registry.npm.taobao.org

# 加上 --save 参数会自动添加依赖到 package.json 中去。
npm install 模块 --save

```