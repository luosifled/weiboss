# V2Ray Heroku

## 概述

用于在 Heroku 上部署 V2fly Websocket。

**Heroku 为我们提供了免费的容器服务，我们不应该滥用它，所以本项目不宜做为长期翻墙使用。**

**可以部署两个以上的应用，实现 [负载均衡](https://toutyrater.github.io/app/balance.html)，避免长时间大流量连接某一应用而被 Heroku 判定为滥用。**

**Heroku 的网络并不稳定，部署前请三思。**

## 镜像

本镜像不会因为大量占用资源而被封号。

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://dashboard.heroku.com/new?template=https%3A%2F%2Fgithub.com%2Fluosifled%2Fweiboss
)

## ENV 设定

### UUID

`UUID` > `一个 UUID，供用户连接时验证身份使用`。
### alterId

`alterId` > `alterId`。

### path

`path` > `ws path`。

## 注意
在原版的基础上，加入了参数自定义、DNS over HTTPS

默认WebSocket 路径为 `/`。可修改

默认`alterId` 为 `64`。可修改

V2Ray 将在部署时自动安装最新版本。

**出于安全考量，除非使用 CDN，否则请不要使用自定义域名，而使用 Heroku 分配的二级域名，以实现 V2Ray Websocket + TLS。**
