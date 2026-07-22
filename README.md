<div align="center">

# Hi, I'm 吕纪新 👋
### Java Backend Developer | Distributed Systems | Video Super-Resolution Learner

一名专注于 Java 后端开发的计算机技术硕士研究生，
目前在企业中台从事分布式系统开发，同时持续深耕微服务、高并发、中间件原理与视频超分辨率研究

</div>

---

## 👨‍💻 About Me

- 🎓 桂林电子科技大学 计算机技术硕士在读（科研方向：视频超分辨率 VSR），预计 2027 年毕业
- 💼 麒盛科技有限公司 Java 后端开发实习生，负责海外业务中台（Overseas Business Center）建设
- 🔧 参与过认证鉴权（OAuth2 SSO / Sa-Token）、对象存储（S3）、多语言国际化（i18n）、动态关税计算等核心模块开发
- 🧩 自研过 Spring Boot Starter：手写迷你 ORM 框架 + 数据库路由组件，深入理解 MyBatis / AbstractRoutingDataSource 底层原理
- 🌱 正在学习 Spring Cloud Alibaba、RocketMQ、ShardingSphere、Sentinel 以及 Spring AI / Agent 开发
- 📫 Email：alexhelen@qq.com

---

## 🛠 Tech Stack

### Backend
![Java](https://img.shields.io/badge/Java-17+-orange?logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen?logo=springboot)
![Spring Cloud](https://img.shields.io/badge/Spring%20Cloud-Alibaba-green?logo=spring)
![MyBatis Plus](https://img.shields.io/badge/MyBatis--Plus-Framework-blue)
![ShardingSphere](https://img.shields.io/badge/ShardingSphere-Sharding-9cf)
![MySQL](https://img.shields.io/badge/MySQL-Database-blue?logo=mysql)
![Redis](https://img.shields.io/badge/Redis-Cache-red?logo=redis)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-Message%20Queue-orange?logo=rabbitmq)
![RocketMQ](https://img.shields.io/badge/RocketMQ-Message%20Queue-orange)
![Docker](https://img.shields.io/badge/Docker-Container-blue?logo=docker)

### AI & Tools
![Python](https://img.shields.io/badge/Python-VSR-blue?logo=python)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red?logo=pytorch)
![Git](https://img.shields.io/badge/Git-Version%20Control-orange?logo=git)
![Linux](https://img.shields.io/badge/Linux-Environment-black?logo=linux)
![Claude Code](https://img.shields.io/badge/Claude%20Code-AI%20Assisted%20Dev-8A2BE2)

---

## 🚀 Featured Projects

### 🌍 Ergomotion IOR 进口合规自动化系统
面向海外进口合规业务，围绕 SAP 出运数据、商业发票、关税计算与单据分发流程，构建端到端自动化系统，替代原有人工核单与关税计算方式。

**核心技术：** `Spring Boot` · `Sa-Token` · `OAuth2 SSO` · `Amazon S3` · `Spring Event`

**项目亮点：**
- 独立负责微软邮箱 OAuth2 单点登录（SSO）认证体系接入
- 封装 Amazon S3 对象存储工具类，支撑文件上传下载
- 基于 Sa-Token 落地统一鉴权模块（登录态 + 角色权限 + 接口级校验）
- 结合事务同步回调（TransactionalEventListener）+ 敏感字段脱敏，实现异步审计日志

---

### 📦 Container Direct Portal 订单录入自动化系统
将客户采购订单（CPO）从邮件接收、附件解析、SAP VA01 建单到异常升级的全流程沉淀为内部 Portal 系统。

**核心技术：** `Spring Boot` · `Spring i18n` · `SAP 集成`

**项目亮点：**
- 设计异常工单流转机制，支撑多类业务异常的分派、状态流转与闭环通知
- 基于 Spring i18n 实现海外多语言动态适配
- 主导技术方案设计与跨团队技术分享

---

### 🔗 SaaS Short Link System
基于 Spring Cloud Alibaba 构建的高并发短链接管理平台，支持短链生成、跳转、分组管理与访问统计。

**核心技术：** `Spring Boot` · `Spring Cloud Alibaba` · `Redis` · `RocketMQ` · `ShardingSphere` · `Sentinel`

**项目亮点：**
- Redis 布隆过滤器前置判重，减少数据库回源与锁竞争
- RocketMQ 异步解耦访问监控写入，降低跳转主链路耗时
- 双重检查锁 + 更新数据库后删缓存，保障缓存一致性
- Redisson 分布式读写锁 + Sentinel QPS 限流，保障突发流量下的稳定性

👉 在线地址：[52coding.xyz](http://52coding.xyz)

---

### 🛒 分布式微服务电商交易平台
基于 Spring Cloud Alibaba 的 B2C 电商平台，涵盖用户认证、商品、购物车、交易、支付等核心业务。

**核心技术：** `Spring Cloud Gateway` · `OpenFeign` · `Seata` · `RabbitMQ` · `JWT`

**项目亮点：**
- 基于 DDD 思想完成微服务拆分，Gateway 统一路由 + 限流 + 全局鉴权
- Seata AT 模式保障下单、扣库存、清购物车等链路的全局强一致性
- RabbitMQ 死信/延迟队列实现订单超时自动取消与库存回滚

---

### ⚙️ SpringBoot 中间件自研实践
基于《SpringBoot 中间件设计与开发》的技术预研与工程实践，动手实现常见中间件底层能力。

**核心技术：** `Spring AOP` · `动态代理` · `AbstractRoutingDataSource`

**项目亮点：**
- 基于 AOP + 自定义注解实现接口级白名单/黑名单动态拦截（服务治理）
- 基于原生 JDBC + 动态代理手写迷你 ORM 框架，理解 Mapper 动态代理与 SqlSession 生命周期
- 将 ORM 框架封装为标准 Starter，基于 `@ConditionalOnMissingBean` 实现按需装配
- 基于 AbstractRoutingDataSource + ThreadLocal 上下文实现多数据源动态路由

---

### 🎬 Video Super-Resolution（科研方向）
学习并复现 BasicVSR、BasicVSR++ 等视频超分辨率模型，关注视频特征传播、光流对齐与时序信息融合。

<!-- 👉 补充仓库链接：[BasicVSR++ Repository](填入你的仓库地址) -->

---

## 📊 GitHub Stats

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=alexmerccc-a11y&show_icons=true&hide_border=true" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=alexmerccc-a11y&layout=compact&hide_border=true" />

</div>

---

## 📈 Contribution Activity

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=alexmerccc-a11y&hide_border=true" />

</div>

---

<div align="center">

### Keep coding, keep learning. 🚀

</div>
