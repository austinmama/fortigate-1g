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

# 关于 FortiGate Security Appliance (FSA) 1Gbps
{: #about-fortigate-security-appliance-1gbps}

Fortigate Security Appliance 1Gbps (FSA) 是与服务器连接的上游专用单租户网络设备，可保护公用 VLAN 上的任一或所有服务器。该设备是与服务器分开购买的，可随时添加到 VLAN 中。IBM© Cloud 会在专用设备上的虚拟域 (VDOM) 内部署[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://www.fortinet.com/sites/default/files/productdatasheets/FortiGate-300C.pdf){: new_window}，允许客户完全访问该虚拟域，而不会影响设备的完整性。 

通过 FSA 1Gbps，客户可以访问高级功能，还可以微调设备，而且微调的程度要比其他产品高得多。防火墙会在流量到达服务器之前阻止流量或执行流量整形。主要好处在于，服务器仅需要处理“好”流量，而且对于重要性不高的通信，可以限制相应的带宽。 

客户可以通过基于 Web 的 FortiOS GUI 或 CLI（命令行界面）使用 SSH 管理 FSA。还可以订购高可用性，该选项会提供以主动/被动方式部署的两个配置可同步的设备。

每月服务器带宽是在服务器交换机端口记录的，因此由 FSA 1Gbps 阻止的流量不会计入每月配额，这样就无需针对不需要的流量付费。

## 概述和功能

**目标用途：**单一公用 VLAN 保护

**用户界面：**Fortigate GUI 和命令行界面

**功能：**有状态数据包检查、VLAN 保护、入口防火墙规则、出口防火墙规则、NAT、SSL VPN 终止、IPSec VPN 终止、高级日志记录和高可用性（可选）

**吞吐量：** 1Gbps（2Gbps 聚集）
