# Springboot-Dubbo-Zookeeper

## 实践微服务的主流方案与分析
- 方案一：Spring Cloud Netflix
- 方案二：Spring Cloud Alibaba
- 方案三：Springboot + Dubbo

### 方案一：Spring Cloud Netflix
Spring Cloud Netflix是Spring家族推出一款微服务框架，它作为 Java开发的微服务框架，可以配合Spring Boot来进行快速开发，可以实现快速开发、持续交付和持续部署。Spring Cloud 有着非常多的组件，覆盖了微服务的许多方面，在Netflix、 Pivotal 两大公司的推动下也变得越来越完善。是市面上很多互联网公司也在使用的微服务方案，下图是Spring Cloud  微服务框架整体组件架构图。

#### 图中组件： 
  APP、Admin、Mobile代表不同机器上的客户端 
  Zuul：它是微服务的Gateway，也就是网关，主要的功能是网络路由。不同客户端需要调用后端系统，将统一从这个网关入口进入，通过网关转发请求给到相应的服务。
  Eureka：作为微服务架构中服务注册与发现中心，Eureka的核心工作是负责多个服务的注册与发现。每个服务启动时，服务提供者Eureka客户端都会往Eureka服务端进行注册，将自己的服务名和IP地址等给到Eureka服务端，同时Eureka客户端可以从Eureka服务端拉取注册表，该注册表包含了所有往服务注册中心注册的服务信息。
