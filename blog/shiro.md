---
title: SpringBoot和shiro整合
comments: true
date: 2018-12-01 21:19:25
updated:
categories:
- 技术
tags:
- shiro
---
# shiro介绍
核心概念：Subject，SecurityManager 和 Realms  
一个应用几乎总是只有一个 SecurityManager 实例  
由于springboot省略了很多配置，很多监听器，过滤器都是不需要配置的，而shiro是以过滤器来做拦截的，所以下回先把springboot的启动原理弄清楚，在来继续对shiro补充。
Realm 是一个组件，认证和授权都是由它来控制。通过继承AuthorizingRealm来实现doGetAuthenticationInfo和doGetAuthorizationInfo这两个方法。
doGetAuthenticationInfo方法需要传一个接口AuthenticationToken给它，通过它获取用户名和密码进行认证
# 工具和版本
springboot：2.1.1
shiro：1.4.0-RC2
开发工具：IntelliJ IDEA 2018
构建工具：Gradle5
