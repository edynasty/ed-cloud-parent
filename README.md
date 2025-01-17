# ed-cloud-parent

<p align="center">
  <img src="https://img.shields.io/github/license/alibaba/arthas.svg"/>
  <img src="https://img.shields.io/badge/JDK-1.8-8A2BE2" alt="Downloads"/>
  <img src="https://img.shields.io/badge/Spring%20Boot-2.7.18-blue" alt="Downloads"/>
  <img src="https://img.shields.io/badge/Spring%20Cloud-2021.0.4-blue" alt="Downloads"/>
  <img src="https://img.shields.io/badge/Spring%20Cloud%20Alibaba-2021.0.4.0-blue" alt="Downloads"/>
</p>


`ed-cloud-parent` 是一个用于微服务架构的父级 POM 文件，旨在统一管理多个依赖的版本、构建配置和插件版本。该项目主要用于管理和提供与 Spring Cloud、Alibaba 和其他常见库的版本配置。

## 项目概述

`ed-cloud-parent` 项目是一个基于 Maven 的 POM 文件，包含了多个常见依赖的版本管理，包括 Spring Boot、Spring Cloud、ShardingSphere、MyBatis Plus 等，旨在简化和统一微服务项目的构建与依赖管理。

## 特性

- **统一版本管理**：通过 Maven `properties` 管理常用依赖的版本。
- **Spring Boot 和 Spring Cloud 支持**：支持 Spring Cloud 和 Spring Boot 版本管理，简化微服务应用的配置。
- **常用工具库支持**：集成了如 MyBatis Plus、ShardingSphere、Redisson、Swagger、JJWT 等常用 Java 库。
- **数据库连接支持**：支持 MySQL、SQL Server、Oracle 等数据库驱动。
- **消息队列与分布式支持**：集成了 RocketMQ、Dubbo、XXL-Job 等分布式系统和消息队列。

## 依赖版本

- **Java**: 8
- **Spring Boot**: 2.7.18
- **Spring Cloud**: 2021.0.4
- **Spring Cloud Alibaba**: 2021.0.4.0
- **ShardingSphere**: 3.1.0
- **MyBatis Plus**: 3.5.5
- **JJWT**: 0.9.1
- **Redisson**: 3.17.4
- **FastJSON**: 1.2.83
- **Hutool**: 5.8.27
- **Swagger2**: 1.6.11

## 依赖管理

以下是一些常用的依赖版本管理：

```xml
<properties>
    <java.version>8</java.version>
    <spring-cloud-alibaba-dependencies.version>2021.0.4.0</spring-cloud-alibaba-dependencies.version>
    <spring-boot-dependencies.version>2.7.18</spring-boot-dependencies.version>
    <spring-cloud-dependencies.version>2021.0.4</spring-cloud-dependencies.version>
    <spring-boot-admin.version>2.7.15</spring-boot-admin.version>
    <mybatis-plus-boot-starter.version>3.5.5</mybatis-plus-boot-starter.version>
    <dynamic-datasource.version>4.3.0</dynamic-datasource.version>
    <qiniu-java-sdk>7.2.28</qiniu-java-sdk>
    <easyexcel.version>3.1.3</easyexcel.version>
    <hikari.version>5.1.0</hikari.version>
    <elasticsearch.version>7.13.3</elasticsearch.version>
</properties>
```
## 插件管理
以下是一些常用的 Maven 插件版本管理：

```xml
<properties>
    <maven-source-plugin.version>3.3.1</maven-source-plugin.version>
    <maven-javadoc-plugin.version>3.11.2</maven-javadoc-plugin.version>
</properties>
```

## 快速开始

1. 将 `ed-cloud-parent` 作为父级 POM 文件导入到您的项目中：

```xml
<parent>
    <groupId>io.github.edynasty</groupId>
    <artifactId>ed-cloud-parent</artifactId>
    <version>0.0.3</version>
</parent>
```
2. 在您的 `pom.xml` 文件中，添加相关的依赖。

例如：

```xml
<dependencies>
    <dependency>
        <groupId>com.alibaba.cloud</groupId>
        <artifactId>spring-cloud-starter-alibaba-nacos-discovery</artifactId>
    </dependency>
</dependencies>
```

3. 配置您的应用程序并开始开发。

## 许可证信息
该项目采用 Apache Software License 2.0 许可证，您可以自由使用、修改和分发本项目。有关详细信息，请参阅 Apache License 2.0。

## 贡献
欢迎提交 Pull Request 来修复问题或增强功能。

