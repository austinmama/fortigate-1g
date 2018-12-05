---

copyright:
  years: 2017,2018
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 查看防火墙

要查看受防火墙保护的 VLAN 以及单个防火墙的更多详细信息，请转至 VLAN 页面。

1. 从浏览器中，打开[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}，然后登录到您的帐户。
2. 在客户门户网站导航中，选择**网络 > IP 管理 > VLAN**。

在表格中，一个行代表基础架构中的一个 VLAN。IBM Cloud 会自动填充“VLAN 编号”和“主要路由器”信息，以指示真实的 VLAN 编号以及在其上配置 VLAN 的路由器。“名称”字段可用于为 VLAN 指定可识别的名称（例如，DMZ、内部网、公用或数据库）。

最右边的列是**网关/防火墙**，其中包含有关所设置的防火墙保护的详细信息，例如：

- **添加防火墙**指示没有为此 VLAN 上的服务器设置任何防火墙。
- **单独保护的服务器**指示一个或多个服务器正在利用硬件防火墙（共享），但没有设置硬件防火墙（专用）、FortiGate Security Appliance 或网关。在具有单独保护的服务器的 VLAN 上，无法设置 VLAN 防火墙和网关。
- **Firewall-vlanXXXX.networklayer.com** 指示已设置硬件防火墙（专用）或 FortiGate Security Appliance。一个 VLAN 只能与一个 VLAN 防火墙或网关相关联，但服务器可以在公用 VLAN 上受 VLAN 防火墙的保护，而在专用网络上与网关相关联。
- **网关名称**指示 VLAN 与该网关相关联。

## 单独保护的服务器详细信息

对于**网关/防火墙**字段值为**单独保护的服务器**的 VLAN，可以单击关联的 VLAN 编号链接来显示 VLAN 详细信息，其中包含关联的设备。

在关联设备的列表中，可以单击每个设备，然后滚动到“配置”选项卡的底部。在“附加组件”部分，您会看到状态为**已安装**或**未安装**的**防火墙**。

- **未安装**指示没有为此设备设置防火墙。
- **已安装**指示已设置防火墙。此时设备上会显示**防火墙**选项卡，用于管理防火墙配置。

## 专用防火墙详细信息

对于**网关/防火墙**字段值为 **Firewall-vlanXXXX.networklayer.com** 的 VLAN，可以单击该防火墙链接来显示防火墙详细信息。设备详细信息包括关联的路由器、VLAN、IPv4/IPv6 子网、与该 VLAN 相关联的设备以及对通过防火墙路由流量或绕过防火墙路由流量的控制。

FortiGate Security Appliance 设备将具有管理 IP、用户名和密码。对 FortiGate Security Appliance 的管理可通过其 GUI 或基于 SSH 的控制台来完成。

## 网关详细信息

对于**网关/防火墙**字段值为网关设备名称的 VLAN，可以单击网关名称来显示网关详细信息。设备详细信息包括关联的前端 (FCR) 和后端 (BCR) VLAN 以及网关管理选项。
