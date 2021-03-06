---
title: "GOPROXY免费版VS商业版"
date: 2019-06-26T13:19:15+08:00
draft: false
description: "GOPROXY 免费版VS商业版"
tags: [ "商业版" ]
categories: [ "默认分类" ]
isCJKLanguage: true
weight: 9900

# keywords: [ "keyword" ]
# linkTitle: ""

# 使用这两个参数将会重置permalink，默认使用文件名
#url: 
#slug: ""

# 设置文章的过期时间，如果是已过期的文章则不会发布，除非使用 --buildExpired 参数
# expiryDate: 2020-01-01

# 设置文章的发布时间，如果是未来的时间则不会发布，除非使用 --buildFuture 参数
# publishDate: 2020-01-01

# 别名将通过重定向实现
# aliases:
#   - 别名1s
#   - /posts/my-original-url/
#   - /2010/01/01/another-url.html

# type 与 layout 参数将会改变 Hugo 寻找该文章模板的顺序
# type: review
# layout: reviewarticle
---

目前，GOPROXY 和 SDK 提供免费版和商业版，功能对比如下。

　　　　　　　　| 　　　免费版　　　 | 　　　商业版　　　
:----------- | :---: | :---:
`基础功能` |   √ |   √
`HTTP(S)代理认证，认证API，负载均衡` |  × |   √
`SOCKS5代理认证，认证API，负载均衡` |   ×|   √
`SPS代理认证，认证API，负载均衡` |   ×|   √
`STOP黑名单` |   ×|   √
`检查更新，失败退出` |   ×|   ×
`单机进程数量限制`|   ×|   ×
`手册完整功能` |   × |   √
`需要联网认证` |   ×|   √
`限速功能`|   × |   √
`指定出口IP`|   × |   √
`目标连接重定向`|   × |   √
`docker`|   √ |   √
`免费更新至更多功能的商业版`|   × |   √


商业版授权方式分为两种：

1. 程序和机器绑定，单个机器方式授权，针对`机器码`收费。
2. 程序和不和机器绑定，授权码方式授权，针对`授权码`收费。

商业版使用：

1. 去平台授权平台 https://gpm.host900.com/ 注册一个用户。
2. 如果使用`机器码`授权方式，首次启动，会在当前目录下面生成id.txt文件，里面是当前机器的机器码，如果是sdk，调用MacCode方法即可获得当前机器的机器码，然后购买机器码名额，最后把机器码添加到授权平台我的机器码中即可完成授权。
3. 如果是`授权码`方式授权，首先购买授权码，然后会在授权平台里面看见自己的授权码。加上授权码参数`--authcode 授权码`启动程序即可，也可以设置环境变量`LIC_AUTHCODE`内容为授权码，如果没有使用参数`--authcode`，程序尝试从环境变量`LIC_AUTHCODE`获取授权码。如果是sdk，start方法有授权码参数，使用购买的授权码即可。

提醒：

商业版只会在启动的时候联网检查一次授权，后期不会再联网检查，只会在`授权码`到期的时候再检查一次，如果48小时内无法成功检查授权程序会退出。
如果系统发现用户恶意传播自己的`授权码`，官方有权终止授权码的使用，并不负任何责任。

购买商业版，请加GOPROXY商业版官方QQ群：746489979
