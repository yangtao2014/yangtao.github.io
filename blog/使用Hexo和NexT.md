---
title: 使用Hexo和Next
date: 2018-11-25 22:12:24
updated: 
comments: true
categories:
- 心得
tags:
- Hexo
- NexT
---

在使用Hexo和NexT过程中，发现还是查官方文档来的更快，这时候发现学好英语是多么的重要 ，查看官方文档，比去网上查来的更快，更准确，就是对英语有要求。
Hexo官方文档地址：https://hexo.io/zh-cn/docs/ (中文版本的)
NexT官方文档地址：http://theme-next.iissnan.com 

==============================
<!-- more -->
突然发现有时候官方文档示例好像是更新不及时，导致出了一些问题：  
1.配置菜单的图标，像首页，标签等这些图标，官方是这样的
```
menu_icons:
  enable: true
  # Icon Mapping.
  home: home
  about: user
  categories: th
  tags: tags
  archives: archive
  commonweal: heartbeat
```
但是这样配置没用，要这样配置
```
menu:
  home: / || home
  tags: /tags || tags
  categories: /categories || th
  archives: /archives || archive
  about: /about || user
```
2.更新日期配置
```
post_meta:
  item_text: true
  created_at: true
  updated_at: true
  categories: true
```
要updated_at为true，才能显示更新日期

### 以后话还是不要说的太绝对了，容易打脸。