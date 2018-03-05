---

copyright:
  years: 2017,2018
lastupdated: "2018-01-18"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 查看防火墙

要查看哪些 VLAN 受防火墙保护以及查找单个防火墙的更多详细信息，请转至 VLAN 页面。

1. 从浏览器，打开[客户门户网站![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}，并登录到帐户。
2. 在“客户门户网站”导航中，选择**网络 > IP 管理> VLAN**。

表中每行表示基础结构中一个 VLAN。IBM Cloud 自动计算“VLAN 数”和“主要路由器”信息，以指示真实 VLAN 数及在其上配置 VLAN 的路由器。“名称”字段可用于为 VLAN 指定可识别的名称（例如，DMZ、内部网、公共或数据库）。

最右边的列**网关/防火墙**包含有关所设置的防火墙保护的详细信息，例如：

- **添加防火墙**指示没有针对此 VLAN 上服务器设置防火墙。
- **单独保护的服务器**指示一个或多个服务器正在利用硬件防火墙（共享），且没有设置硬件防火墙（专用）、FortiGate Security Appliance 或网关。无法在具有单独保护的服务器的 VLAN 上设置 VLAN 防火墙和网关。
- **Firewall-vlanXXXX.networklayer.com** 指示设置了硬件防火墙（专用）或 FortiGate Security Appliance。仅可以将一个 VLAN 防火墙或网关与 VLAN 关联，但可以在公共 VLAN 上通过 VLAN 防火墙保护服务器，并可以在专用网络上通过网关关联服务器。
- **网关名称**指示 VLAN 与此网关关联。

## 单独保护的服务器详细信息

针对在**网关/防火墙**字段中具有**单独保护的服务器**的 VLAN，可以单击关联 VLAN 号链接以显示此 VLAN 的详细信息，包括关联的设备。

在关联设备的列表中，可以单击每个设备，并滚动到“配置”选项卡的底部。将在“附加组件”部分中看到状态为**已安装**或**未安装**的**防火墙**。

- **未安装**指示没有针对此设备设置防火墙。
- **已安装**指示设置了防火墙，设备上将显示**防火墙**选项卡，可在其中管理防火墙配置。

## 专用防火墙详细信息

针对在**网关/防火墙**字段中具有 **Firewall-vlanXXXX.networklayer.com** 的 VLAN，可以单击此防火墙链接以显示防火墙的详细信息。设备详细信息包括关联路由器、VLAN、IPv4/IPv6 子网、与此 VLAN 关联的设备以及针对通过防火墙路由流量或绕过防火墙路由流量的控制。

FortiGate Security Appliance 设备将具有管理 IP、用户名和密码。FortiGate Security Appliances 的管理通过其 GUI 或基于 SSH 的控制台完成。

## 网关详细信息

针对在**网关/防火墙**字段中具有网关设备名称的 VLAN，可以单击网关名称以显示网关的详细信息。设备详细信息包括关联前端 (FCR) 和后端 (BCR) VLAN 以及网关管理选项。
