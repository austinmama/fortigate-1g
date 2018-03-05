---

copyright:
  years: 2017
lastupdated: "2017-11-29"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 缺省部署

FortiGate Security Appliance (FSA) 1Gbps 作为单个虚拟域（通常为 firewall001）部署在专用设备上。客户对设备的资源（处理器和内存等）具有完整访问权，但对设备级别的配置的访问受到限制以确保 IBM Cloud 可有效支持设备。

FSA 以 NAT 方式部署，位于公共网络基础结构的两个 VLAN/网络中。外部 VLAN 是 IBM Cloud 公共 VLAN，其中，流量进入数据中心并路由到 FSA。内部 VLAN 是客户分配的受保护公共 FCR（前端客户路由器）VLAN，也是客户服务器资源所在的 VLAN。  

IBM Cloud 在供应过程中，在这两个网络中部署具有两个绑定 1G 接口的 FSA。IBM Cloud 还部署了一个接口，用于供应和维护客户不可用的设备。

部署的防火墙允许所有 IPv4 和 IPv6 流量，包括用于允许 IBM Cloud 内部管理网络通过防火墙访问设备的特定规则 (softlayer-admin)。“拒绝服务”保护和其他多数过滤器配置为不启用。
