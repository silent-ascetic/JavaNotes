# Spring Cloud

## 微服务

微服务是系统架构上的一种设计风格，简单的讲就是将大型的单体web应用根据功能拆分成多个小型服务。小服务之间互相独立，通过轻量级的通讯机制进行数据交互。 

## Spring Cloud

Spring Cloud不是一个具体的框架，可以把它理解为一个工具箱，它提供的各类工具，可以帮助我们快速构建分布式系统。
Spring Cloud为开发人员提供了在分布式系统中快速构建一些常见模式的工具（例如配置管理，服务发现，断路器，智能路由，微代理，控制总线，一次性令牌，全局锁定，领导选举，分布式会话，集群状态）。分布式系统的协调导致样板模式，使用Spring Cloud开发人员可以快速建立实现这些模式的服务和应用程序。它们可以在任何分布式环境中很好地工作，包括开发人员自己的笔记本电脑，裸机数据中心和托管平台（如Cloud Foundry）。

**Spring Cloud特征：**
* 分布式/版本化配置
* 服务注册和发现
* 路由
* 服务到服务呼叫
* 负载平衡
* 断路 器
* 全局锁
* 领导层选举和集群状态
* 分布式消息传递

**Spring Cloud整合的框架（主要）：**

Spring Cloud Config
Centralized external configuration management backed by a git repository. The configuration resources map directly to Spring but could be used by non-Spring applications if desired.  
由 git 存储库支持的集中式外部配置管理。配置资源直接映射到Spring，但如果需要，非Spring应用程序可以使用。

Spring Cloud Netflix
Integration with various Netflix OSS components (Eureka, Hystrix, Zuul, Archaius, etc.).  
与各种Netflix OSS组件（Eureka，Hystrix，Zuul，Archaius等）集成。

Spring Cloud Bus
An event bus for linking services and service instances together with distributed messaging. Useful for propagating state changes across a cluster (e.g. config change events).  
一个事件总线，用于将服务和服务实例与分布式消息传递链接在一起。用于跨集群传播状态更改（例如，配置更改事件）。

Spring Cloud Cloudfoundry
Integrates your application with Pivotal Cloud Foundry. Provides a service discovery implementation and also makes it easy to implement SSO and OAuth2 protected resources.  
将您的应用程序与 Pivotal Cloud Foundry 集成。提供服务发现实现，还可以轻松实现受 SSO 和 OAuth2 保护的资源。

Spring Cloud Open Service Broker
Provides a starting point for building a service broker that implements the Open Service Broker API.  
为构建实现开放服务中介程序 API 的服务代理提供起点。

Spring Cloud Cluster
Leadership election and common stateful patterns with an abstraction and implementation for Zookeeper, Redis, Hazelcast, Consul.  
领导层选举和常见的有状态模式，为Zookeeper，Redis，Hazelcast，Consul提供抽象和实现。

Spring Cloud Consul
Service discovery and configuration management with Hashicorp Consul.  
使用Hashicorp Consul进行服务发现和配置管理。

Spring Cloud Security
Provides support for load-balanced OAuth2 rest client and authentication header relays in a Zuul proxy.  
支持 Zuul 代理中的负载平衡 OAuth2 rest 客户端和身份验证标头中继。

Spring Cloud Sleuth
Distributed tracing for Spring Cloud applications, compatible with Zipkin, HTrace and log-based (e.g. ELK) tracing.  
Spring Cloud应用程序的分布式跟踪，与Zipkin，HTrace和基于日志的（例如ELK）跟踪兼容。

Spring Cloud Data Flow
A cloud-native orchestration service for composable microservice applications on modern runtimes. Easy-to-use DSL, drag-and-drop GUI, and REST-APIs together simplifies the overall orchestration of microservice based data pipelines.   
云原生编排服务，用于现代运行时上的可组合微服务应用程序。易于使用的 DSL、拖放式 GUI 和 REST API 共同简化了基于微服务的数据管道的整体编排。 


Spring Cloud Stream
A lightweight event-driven microservices framework to quickly build applications that can connect to external systems. Simple declarative model to send and receive messages using Apache Kafka or RabbitMQ between Spring Boot apps.   
轻量级事件驱动的微服务框架，用于快速构建可连接到外部系统的应用程序。简单的声明性模型，用于在Spring Boot应用程序之间使用Apache Kafka或RabbitMQ发送和接收消息。

Spring Cloud Stream Applications
Spring Cloud Stream Applications are out of the box Spring Boot applications providing integration with external middleware systems such as Apache Kafka, RabbitMQ etc. using the binder abstraction in Spring Cloud Stream.  
Spring Cloud Stream应用程序是开箱即用的Spring Boot应用程序，使用Spring Cloud Stream中的binder抽象提供与外部中间件系统（如Apache Kafka，RabbitMQ等）的集成。

Spring Cloud Task
A short-lived microservices framework to quickly build applications that perform finite amounts of data processing. Simple declarative for adding both functional and non-functional features to Spring Boot apps.  
一个短期微服务框架，用于快速构建执行有限量数据处理的应用程序。简单的声明性，用于向Spring Boot应用程序添加功能和非功能性功能。

Spring Cloud Task App Starters
Spring Cloud Task App Starters are Spring Boot applications that may be any process including Spring Batch jobs that do not run forever, and they end/stop after a finite period of data processing.  
Spring Cloud Task App Starters 是 Spring Boot 应用程序，可以是任何进程，包括不会永远运行的 Spring Batch 作业，并且在有限的数据处理时间后结束/停止。

Spring Cloud Zookeeper
Service discovery and configuration management with Apache Zookeeper.  
使用 Apache Zookeeper 进行服务发现和配置管理

Spring Cloud Connectors
Makes it easy for PaaS applications in a variety of platforms to connect to backend services like databases and message brokers (the project formerly known as "Spring Cloud").  
使各种平台中的 PaaS 应用程序能够轻松连接到数据库和消息代理等后端服务（该项目以前称为"Spring Cloud"）。

Spring Cloud Starters
Spring Boot-style starter projects to ease dependency management for consumers of Spring Cloud. (Discontinued as a project and merged with the other projects after Angel.SR2.)  
Spring Boot 风格的启动项目，可简化 Spring Cloud 使用者的依赖关系管理。（作为一个项目停止，并与Angel.SR2之后的其他项目合并。

Spring Cloud CLI
Spring Boot CLI plugin for creating Spring Cloud component applications quickly in Groovy  
Spring Boot CLI插件，用于在Groovy中快速创建Spring Cloud组件应用程序。

Spring Cloud Contract
Spring Cloud Contract is an umbrella project holding solutions that help users in successfully implementing the Consumer Driven Contracts approach.  
Spring Cloud Contract是一个伞形项目，包含解决方案，可帮助用户成功实施消费者驱动的合同方法。

Spring Cloud Gateway
Spring Cloud Gateway is an intelligent and programmable router based on Project Reactor.  
Spring Cloud Gateway是一款基于Project Reactor的智能可编程路由器。

Spring Cloud OpenFeign
Spring Cloud OpenFeign provides integrations for Spring Boot apps through autoconfiguration and binding to the Spring Environment and other Spring programming model idioms.  
Spring Cloud OpenFeign通过自动配置和绑定到Spring环境和其他Spring编程模型习语，为Spring Boot应用程序提供集成。

Spring Cloud Pipelines
Spring Cloud Pipelines provides an opinionated deployment pipeline with steps to ensure that your application can be deployed in zero downtime fashion and easilly rolled back of something goes wrong.  
Spring Cloud Pipelines提供了一个固执己见的部署管道，其中包含一些步骤，以确保您的应用程序可以以零停机时间的方式进行部署，并轻松回滚出错的地方。

Spring Cloud Function
Spring Cloud Function promotes the implementation of business logic via functions. It supports a uniform programming model across serverless providers, as well as the ability to run standalone (locally or in a PaaS).  
Spring Cloud Function通过函数促进业务逻辑的实现。它支持跨无服务器提供程序的统一编程模型，以及独立运行（本地或 PaaS）的能力。
