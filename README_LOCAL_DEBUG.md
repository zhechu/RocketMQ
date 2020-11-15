

## 本地调试

根目录创建 conf 文件夹

将以下文件复制到 conf 文件夹下

distribution/conf/broker.conf
distribution/conf/logback_broker.xml
distribution/conf/logback_namesrv.xml

broker.conf 添加本地 IP 配置
$ vi broker.conf
```shell script
brokerClusterName = DefaultCluster
brokerName = broker-zhechu
brokerId = 0
deleteWhen = 04
fileReservedTime = 48
brokerRole = ASYNC_MASTER
flushDiskType = ASYNC_FLUSH
namesrvAddr = 127.0.0.1:9876
```

添加环境变量 ROCKETMQ_HOME，值为源码根目录
ROCKETMQ_HOME=/Users/yuwangling/IdeaProjects/rocketmq

### 启动 namesrv

前置条件：ROCKETMQ_HOME 环境变量配置

### 启动 broker

前置条件
1. ROCKETMQ_HOME 环境变量配置
2. 准备 broker.conf 配置文件

启动 broker 需指定配置文件
-c /Users/yuwangling/IdeaProjects/rocketmq/conf/broker.conf

