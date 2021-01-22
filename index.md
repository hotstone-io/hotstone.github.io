## 简介

Hotstone.io 项目主要目的是通过 [Operator SDK](https://github.com/operator-framework/operator-sdk) 开发一整套的 Kubernetes 管理平台。

目前开发正在进行中, 尚未发布, 请耐心等待。

### 功能

Hotstone.io 项目主要围绕着 Kubernetes、Istio、Etcd、Prometheus、CI/CD 、Logging、Support、Cloud、Helm 等作为核心功能。

因实际使用中全部是通过 Istio 进行操作和维护的, 市面上操作平台都是风格独特不与 Istio 体系相容, 且 Helm 默认使用风格又与 Istio 有矛盾, 且配合实际经验完整的开发一整套平台进行管理。

且拥有部分嵌入性代码作为 CI/CD 的使用, 大致有：

```
ProjectCodeings
|
|
|--------- docker
|
|--------- kubernetes
|
|--------- .hotstone.meta
|
...
```
开发人员不在需要登入服务器进行操作, 可直接通过平台申请容器作为开发机器进行使用, 因系统内部有一整台的 Proxy 和 外部/内部 DNS 作为开发支撑, 只需要接入 VPN 等设备即可在个人 PC 中进行本地开发测试。

项目内可区分各个不同 Branch 做可选则的规则进行 CI, 但开发人员有自定义容器化以及项目依赖配置的权限, 但没有部署流程权限, 可完整的实现 DevOps 理念, 让其完全不再需要关心服务器或部署环节。

项目中后期接入监控和日志, 目的是通过 DevOps 实现非运维话的操作, 运维不需要关心业务, 开发不需要关心架构。

开发人员可以随意通过项目使用 [Crane](https://github.com/slzcc/crane) 部署一整台开发或者预生产环境作为测试使用。

### 授权

目前只有个人支撑整个项目, 都是围绕着个人经验对实际使用过程中的引发的灵感进行开发, 如有疑问请联系我 `hotstone@hotstone.io` 或 `shilei@hotstone.com.cn`。