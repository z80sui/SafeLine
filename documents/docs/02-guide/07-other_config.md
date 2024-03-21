---
title: "配置其他"
---

# 配置其他

其他配置项介绍

## 防护配置

### 黑白名单

黑名单：拦截

白名单：放通

注意：条件 AND 是指同时符合，如果希望多个匹配条件需要增加多条黑名单或者白名单

![Alt text](/images/docs/guide_config/other_config1.png)

### 频率限制

通过开启频率限制功能封锁恶意 IP

![Alt text](/images/docs/guide_config/other_config2.png)

### 人机验证

人机验证的有效时间默认是一个小时，未来可能会支持配置，敬请期待。

详情查看 [人机验证 2.0](/about/challenge)

### 语义分析

详情查看 [语义分析检测算法](/about/syntaxanalysis)

### 补充规则（专业版）

补充规则能在语义分析的基础上，针对一些特殊的业务漏洞、框架漏洞的利用行为进行防护。

社区版默认进行平衡防护，业版可进一步配置防护模式。

![Alt text](/images/docs/guide_config/other_config3.png)

### 身份认证

可以通过添加认证规则，对雷池保护的站点额外增加身份认证功能。

![Alt text](/images/docs/guide_config/other_config4.png)

如图，触发身份认证规则后需要使用账户密码登录后继续访问网站。

![Alt text](/images/docs/guide_config/other_config5.png)

## 通用配置

### IP 组配置

1.支持自定义 IP 组

2.长亭社区恶意 IP 情报，需要加入 IP 情报共享计划才可以使用

### 证书管理

管理需要使用的证书，点击添加证书添加

### 其他

#### 源 ip 获取方式

1.使用默认的方式获取源 IP

2.自定义获取源 IP 的 header

#### 站点通用配置

1.如果配置站点需要 http 自动转为 https 功能时，需要手动开启

2.支持使用 HTTP2

3.雷池支持开启 IPv6 的访问

4.代理增加信息，方便数据分析

注：开启后并不会遵循源请求的信息，雷池会覆盖，为防止客户端伪造

#### 拦截页面附加说明

自定义拦截页面的提示信息

#### 雷池控制台证书

存放默认证书，可以自定义证书

#### 雷池控制台登录设置

用于配置登录雷池管理端的方式

低于5.0.0版本升级上来的，shell会显示初始密码，忘记可以手动重置

社区版支持单用户，**专业版**支持多用户管理

管理员固定为 admin，非管理员不能修改其他用户配置

#### 自定义拦截页面（专业版）

专业版用户可以自定义拦截页面

#### Syslog 设置

让雷池发送syslog到设置的服务器，**当前只支持UDP协议**

![Alt text](/images/docs/guide_config/other_config6.png)

保存信息后可以点击测试按钮测试，收到测试信息表示配置成功

雷池发现攻击事件后，会发送事件的syslog信息

![Alt text](/images/docs/guide_config/other_config7.png)


#### IP 情报共享计划

默认加入共享计划，加入后将共享攻击 IP 信息到社区，并可使用 IP 组 “长亭社区恶意 IP 情报”。

## 常见配置问题

请参考 [其他问题](/faq/other)