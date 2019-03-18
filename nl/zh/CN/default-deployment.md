---

copyright:
  years: 2017
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# FortiGate Security Appliance (FSA) 1Gbps 缺省部署
{: #default-deployment-of-a-fortigate-security-appliance-1gbps}

FortiGate Security Appliance (FSA) 1Gbps 作为单个虚拟域（通常为 firewall001）部署在专用设备上。客户对设备的资源（处理器和内存等）具有完全访问权，但对设备级别配置的访问会受到限制，这是为了确保 IBM© Cloud 能够有效地为设备提供支持。

FSA 以 NAT 方式部署，并且位于公用网络基础架构的两个 VLAN/网络中。外部 VLAN 是 IBM Cloud 公用 VLAN，其中流量会进入数据中心并路由到 FSA。内部 VLAN 是客户指定的受保护公用 FCR（前端客户路由器）VLAN，也是客户服务器资源所在的 VLAN。  

在供应过程中，IBM Cloud 会分别在这两个网络上部署 FSA 以及两个绑定的 1G 接口。IBM Cloud 还会部署一个接口，用于供应和维护对客户不可用的设备。

所部署的防火墙允许所有 IPv4 和 IPv6 流量，包括为了允许 IBM Cloud 内部管理网络通过防火墙访问设备而设计的特定规则 (softlayer-admin)。“拒绝服务”保护和大多数其他过滤器都配置为不强制执行。
