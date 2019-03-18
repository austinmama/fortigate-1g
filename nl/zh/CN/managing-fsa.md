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

# 管理 FortiGate Security Appliance (FSA) 1Gbps
{: #managing-the-fortigate-security-appliance-1gbps}

首次将防火墙添加到 VLAN 时，会允许所有流量。要控制流量，需要向防火墙添加规则。 

1. 从浏览器中，打开[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}，然后登录到您的帐户。
2. 在“客户门户网站”导航中，选择**网络 > IP 管理 > VLAN**。 

	**提示：**要仅查看公用 VLAN，请单击**过滤器**下拉菜单，然后在**主路由器**字段中输入 ``fcr``。
3. 滚动到要管理的 VLAN，然后单击**网关/防火墙**列中防火墙名称的链接，以转至**设备详细信息**页面。
4. 在**设备详细信息**页面中，可以查看关联的子网、防火墙路由的当前“状态”以及管理信息。 

	管理信息包括**管理 IP**、**用户名**和**密码**。缺省情况下，此管理 IP 可公开访问。出于自动化目的或对于更高级的使用场景，还支持使用 SSH 以及相同 IP 和凭证来进行管理。
5. 要访问 GUI，请单击管理 IP 链接，然后输入所提供的用户名和密码。 
6. 在管理 UI 中，可以通过 VDOM 管理员身份来管理 FortiGate Security Appliance。对于管理 UI 未提供的管理功能（例如，管理 SSL 证书、启动手动 HA 故障转移、重新引导、升级或执行缺省配置复原），需要开具支持凭单。

Fortinet 提供了[联机文档，其中包含一个交互式使用手册 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://cookbook.fortinet.com/fortigate/){: new_window}，可用作配置期间的参考。
