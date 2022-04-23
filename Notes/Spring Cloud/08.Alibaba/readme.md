# Spring Cloud Alibaba

Spring Cloud Alibaba 是阿里巴巴结合自身丰富的微服务实践而推出的微服务开发的一站式解决方案，是 Spring Cloud 第二代实现的主要组成部分。

Spring Cloud Alibaba 吸收了 Spring Cloud Netflix 的核心架构思想，并进行了高性能改进。自 Spring Cloud Netflix 进入停更维护后，Spring Cloud Alibaba 逐渐代替它成为主流的微服务框架。

Spring Cloud Alibaba 是国内首个进入 Spring 社区的开源项目。2018 年 7 月，Spring Cloud Alibaba 正式开源，并进入 Spring Cloud 孵化器中孵化；2019 年 7 月，Spring Cloud 官方宣布 Spring Cloud Alibaba 毕业，并将仓库迁移到 Alibaba Github OSS 下。

## 组件

- Nacos：阿里巴巴开源产品，一个更易于构建云原生应用的动态服务发现,配置管理和服务管理平台。
- Sentinel：阿里巴巴开源产品，把流量作为切入点,从流量控制,熔断降级,系统负载保护等多个维度保护服务的稳定性。
- RocketMQ：Apache RocketMQ 是一款基于Java 的高性能、高吞吐量的分布式消息和流计算平台。
- Dubbo：Apache Dubbo 是一款高性能的 Java RPC 框架。
- Seata：阿里巴巴开源产品，一个易于使用的高性能微服务分布式事务解决方案。
- Alibaba Cloud OSS：阿里云对象存储服务器（Object Storage Service，简称OSS），是阿里云提供的海量、安全、低成本、高可靠的云存储服务。
- Alibaba Cloud Schedulerx：阿里中间件团队开发的一款分布式调度产品,支持周期性的任务与固定时间点触发任务。


**Spring Cloud 第一代实现（Netflix）与 Spring Cloud 第二代实现（Alibaba）对比**  

| 组件                | 状态                                             | 组件                      | 状态                                                 |
| ------------------- | ------------------------------------------------ | ------------------------- | ---------------------------------------------------- |
| Ereka               | 2.0 孵化失败                                     | Nacos Discovery           | 性能更好，感知力更强                                 |
| Ribbon              | 停更进维                                         | Spring Cloud Loadbalancer | Spring Cloud 原生组件，用于代替 Ribbon               |
| Hystrix             | 停更进维                                         | Sentinel                  | 可视化配置，上手简单                                 |
| Zuul                | 停更进维                                         | Spring Cloud Gateway      | 性能为 Zuul 的 1.6 倍                                |
| Spring Cloud Config | 搭建过程复杂，约定过多，无可视化界面，上手难点大 | Nacos Config              | 搭建过程简单，有可视化界面，配置管理更简单，容易上手 |

## 应用场景

- 大型复杂的系统，例如大型电商系统。
- 高并发系统，例如大型门户网站、商品秒杀系统。
- 需求不明确，且变更很快的系统，例如创业公司业务系统。
