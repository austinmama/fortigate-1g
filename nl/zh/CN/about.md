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

# 关于

Fortigate Security Appliance 1Gbps (FSA) 是连接服务器的专用单租户上游网络设备，用于保护公共 VLAN 上所有服务器。此设备与服务器分开购买，可随时添加到 VLAN。IBM Cloud 在专用设备上虚拟域 (VDOM) 中部署[客户门户网站![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://www.fortinet.com/sites/default/files/productdatasheets/FortiGate-300C.pdf){: new_window}，使客户对此虚拟域具有完全访问权，同时不损害设备的完整性。 

通过 FSA 1Gbps，客户可访问高级功能，与其他产品相比，可更高程度优化设备。在流量到达服务器之前，防火墙阻止流量或进行流量塑形。主要好处在于，服务器仅需要处理“好”流量，且可以限制重要性不高的通信的带宽。 

客户可以通过基于 Web 的 FortiOS GUI 或 CLI（用户管理界面）使用 SSH 管理 FSA。还可以订购高可用性，这为处于主动/被动部署的两个设备提供了同步配置。

由于每月服务器带宽在服务器交换机端口记录，因此 FSA 1Gbps 阻止的流量不会计入每月分配，无需针对不需要的流量付费。

## 概述和功能

**用途：**单一公共 VLAN 保护

**用户界面：**Fortigate GUI 和命令行界面

**功能：**有状态包检查、VLAN 保护、入防火墙规则、出防火墙规则、NAT、SSL VPN 终止、IPSec VPN 终止、高级日志记录和高可用性（可选）

**吞吐量：**2000Mbps
