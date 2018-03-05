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

# 保护 FortiGate Security Appliance

您可以配置 FortiGate Security Appliance (FSA) 1Gbps 以满足安全和兼容性需求。IBM Cloud 为 VDOM 管理员帐户提供随机分配的密码。客户可以循环此密码，创建只读用户，基于“受信任主机”限制访问权以仅接受来自指定源 IP（最多三个）的流量。要完成这些活动：

1. 使用[客户门户网站![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}中**设备详细信息**页面上找到的凭证登录到设备。遵循“如何[管理 FortiGate Security Appliance](managing-fsa.html)”指示信息以找到凭证。
2. 登录到设备后，浏览到**系统 > 管理 > 管理员**。记录所有访问权和更改。
3. 要配置单个接口，请浏览到**系统 > 网络 > 接口**。

    可以将管理接口的访问权仅限制给所需的协议（通常为 HTTPS 和 SSH，因为这提供传输中加密），如果要实现更多安全性，可以禁用对管理接口的外部访问权。这可通过以下方式实现：在“内部”接口（客户的公共 VLAN 所在的接口）上的相应协议或禁用“外部”接口（从其接收公共因特网流量的接口）上的所有协议。这一额外的安全措施需要用户在 VLAN 内部放置一台服务器，从其管理 FSA。 
