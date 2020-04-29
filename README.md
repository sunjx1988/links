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

# 容器

[centos7安装docker](https://www.cnblogs.com/yufeng218/p/8370670.html)

[docker 快速搭建 kafka + zookeeper](https://www.jianshu.com/p/ac03f126980e)

[基于docker 快速构建 zk + kafka + flink](https://www.cnblogs.com/1ssqq1lxr/p/10417005.html)

[dk + zk + kafka + flink compose构建文件](docker/zk-kafka-flink/docker-compose.md)

[dk + zk + kafka + flink 相关命令](docker/zk-kafka-flink/cmd.md)

```
# docker-compose 安装
> curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
> chmod +x /usr/local/bin/docker-compose
> ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose

# 停止全部容器
docker ps -a | `awk 'NR>1 {print "docker stop ", $1}'`
docker ps -a | `awk 'NR>1 {print "docker rm ", $1}'`
```

# 安全

[token 鉴权](https://www.cnblogs.com/fujingtao5470/p/11573528.html)

# Spring

[spring 第一篇](https://blog.csdn.net/weixin_43737917/article/details/105213582)

[spring 第二篇](https://blog.csdn.net/weixin_43737917/article/details/105222054)

# 公开课

[又拍云](https://www.upyun.com/opentalk)

# 即时通讯

[WebRTC实时音视频技术基础：基本架构和协议栈](http://www.52im.net/thread-442-1-1.html)

[腾讯技术分享：微信小程序音视频与WebRTC互通的技术思路和实践](http://www.52im.net/thread-1988-1-1.html)

[Websocket]

# Markdown

[语法](https://www.runoob.com/markdown/md-tutorial.html)

[高级用法,UML等](https://www.runoob.com/markdown/md-advance.html)