## 引用

> 团结目前仅有三人，之后会将其他队员的github主页贴到此处。
>
> 开会采用的工具是**腾讯会议**

## 时间节点

#### 2020.2.23：时长50分钟

- 分析班车预约系统的页面
- 分析采用的架构，首先是前后端
- 决定前端采用较流行的**Vue全家桶**
- 决定后端采用**Springboot+Dubbo+Mybatis+Mysql+Redis+RocketMQ等**
- 构建后端环境和映射其端口
- 根据自身环境因素，决定暂时启用内网穿透将本地服务映射到外网
- 决定服务：
  - 用户服务
  - 班车服务
  - 订单服务
  - 支付服务
- 接下来的计划
  - 构建服务架构图
  - 建数据模型

#### 2020.2.28：时长65分钟

- 分析班车服务都需要哪些表
- 分析班车模型数据表的字段
- 分析班车场次的数据表的字段
- 需要采用swagger2文档注释加调试
- 接下来的计划
  - 前端购买阿里云服务器
  - 前端开始搭建环境
  - 后端部署用户服务模块和网关模块

#### 2020.3.5：时长45分钟

- 对接接口场次显示的信息
- 讨论如何自动更新车次状态，不需要用户决定
- 根据2的讨论，决定采用springboot的定时器轮训，由于场次的出发时间要么半点，要么整点。所以采用每天上午7点-21点每隔30分钟进行轮回
- 接下来的计划
  - 前端搭建用户中心，场次列表，场次详情等页面
  - 后端搭建班车服务模块和编写对应的接口

#### 2020.3.12：时长45分钟

- 讨论分析下单需要哪些表
- 讨论分析下单的表需要哪些字段
- 讨论需要下单的需要哪些接口
- 讨论下单服务的业务逻辑
- 接下来的计划
  - 前端大家下单等页面
  - 后端搭建下单服务模块以及编写对应的接口

#### 2020.3.18：时长50分钟

- 采用用户余额来代替支付宝和微信的支付接口(需要商家认证，因此就不采样那样的方式了)
- 支付表的话，暂时先考虑，按理来讲，需要的，但不需要也可以
- 讨论支付业务逻辑
- 接下来的计划
  - 前端支付，退款页面
  - 后端支付，退款业务逻辑

#### 2020.3.22：时长80分钟

- 因为程序可能在高并发的情况下，出现异常情况，那么需要引起消息队列
- 讨论整合rocketmq消息队列
- 再者并发量上来，经过讨论整合redis，暂时不需要集群
- 前端有5分钟自定取消订单的业务逻辑，决定采用redis的key过期监听事件方案
- 接下来的计划
  - 整合redis
  - 整合rocketmq
  - 开放redis的key过期策略