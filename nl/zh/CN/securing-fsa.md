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

# 保护 FortiGate Security Appliance

您可以配置 FortiGate Security Appliance (FSA) 1Gbps 来满足安全性和合规性需求。IBM Cloud 为 VDOM 管理员帐户提供了随机分配的密码。客户可以定期重置该密码，创建具有只读权限的用户，以及基于“受信任主机”限制访问权，以仅接受来自指定源 IP（最多三个）的流量。要完成这些活动，请执行以下操作：

1. 使用凭证登录到设备。您可以在[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window} 中的**设备详细信息**页面上找到凭证。请按照“如何[管理 FortiGate Security Appliance](managing-fsa.html)”指示信息来查找凭证。
2. 登录到设备后，浏览到**系统 > 管理 > 管理员**。所有访问和更改都会记录下来。
3. 要配置单个接口，请浏览到**系统 > 网络 > 接口**。

    您可以仅允许管理接口所需的协议访问管理接口（这些协议通常为 HTTPS 和 SSH，因为它们能提供传输中加密）。如果要添加额外的安全保护，可以禁用对管理接口的外部访问。要完成这些操作，可以在“内部”接口（客户的公用 VLAN 所在的接口）上启用相应协议，而在“外部”接口（从中接收公共因特网流量的接口）上禁用所有协议。这种额外的安全保护措施需要用户在 VLAN 内部放置一台服务器，从该服务器来管理 FSA。 
