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

# 管理 FortiGate Security Appliance

首次将防火墙添加到 VLAN 时，允许所有流量。需要将规则添加到防火墙以控制流量。 

1. 从浏览器，打开[客户门户网站![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}，并登录到帐户。
2. 在“客户门户网站”导航中，选择**网络 > IP 管理> VLAN**。 

	**提示：**要仅查看公共 VLAN，请单击**过滤**下拉菜单，并在**主要路由器**中输入 ``fcr``。
3. 滚动到要管理的 VLAN，并单击**网关/防火墙**列中防火墙名称的链接，以转至**设备详细信息**页面。
4. 在**设备详细信息**页面中，可查看关联子网、防火墙路由的当前“状态”以及管理信息。 

	管理信息包含**管理 IP**、**用户名**和**密码**。缺省情况下，此管理 IP 可公开访问。为实现自动化目的或针对其他使用场景，还可通过将 SSH 与相同 IP 和凭证配合使用来进行管理。
5. 要访问 GUI，请单击管理 IP 链接并输入提供的用户名和密码。 
6. 从管理 UI，可作为 VDOM 管理员管理 FortiGate Security Appliance。对于无法通过管理 UI 使用的管理功能（例如，管理 SSL 证书、启动手动 HA 故障转移、重新引导、升级或执行缺省配置复原），需要提交支持凭单。

Fortinet 维护[包含交互式使用指南的联机文档![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://cookbook.fortinet.com/fortigate/){: new_window}，配置期间可用于参考。
