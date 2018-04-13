---
layout: post
title: "Charles（Mac）配置"
date: 2018-04-11 13:32:20 +0300
description: # Add post description (optional)
img:  # Add image post (optional)
tags: [Charles, Setup]
---
注：详细步骤可参见 <https://www.cnblogs.com/mawenqiangios/p/8270238.html>


1. 下载破解版Charles

    链接: https://pan.baidu.com/s/1kmHUlYUG-qrikpS58MPdjw 密码: h99t

2. 安装

    1）打开dmg文件，将 Charles.app 拖动到 应用程序文件夹

    2）用dmg文件中的 charles.jar 覆盖 Charles应用 /Contents/java/charles.jar 文件

    3）打开Charles，随便输入注册信息即可

3. 本地抓包

    勾选 Proxy -> macOS Proxy

    注意：如果使用了vpn代理，一定要先关掉代理设置

4. ios 抓包

    1）保证iPhone 和 mac 在同一个局域网内

    2）配置局域网的代理：无线局域网 -> danlan -> 配置代理 -> 手动 -> 服务器：（mac的ip地址，在系统偏好设置 -网络中查看）端口：8888  -> 存储

    到这个时候charles就可以抓取ios的http请求了。

    接下来，需要安装证书，使charles能够抓取 HTTPS 请求。

    3）Mac，Charles，Help选项 -> SSL Proxying -> Install Charles Root Certificate.

    装完后需要在钥匙串中设置该证书的信任选项，选择永久信任。

    4）ios，在Safari中输入http://charlesproxy.com/getssl，下载安装证书。

    装完后需要在设置 -> 通用 -> 关于本机 -> 证书信任设置 中打开证书开关

    这个时候就可以利用charles抓取ios的https请求了。
