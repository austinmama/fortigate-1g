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
{:faq: data-hd-content-type='faq'}

# FortiGate Security Appliance (FSA) 1Gbps 常见问题
{: #faqs-for-fortigate-security-appliance-1gbps}

以下是使用 FortiGate Security Appliance (FSA) 1Gbps 防火墙时的常见问题。

## 什么是防火墙？
{:faq}

防火墙是与服务器连接的上游网络设备。防火墙用于阻止不需要的流量到达服务器。

## 为什么要使用防火墙？
{:faq}

使用防火墙的主要好处在于，服务器仅需要处理“好”流量，这意味着您的资源仅会用于预期目的，而不会用于处理不需要的流量。

## IBM© 提供哪些防火墙产品？
{:faq}

您可以通过查看此[主题](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-exploring-firewalls)，找到 IBM Cloud 中提供的所有防火墙产品的详细对比信息。 

## FortiGate Security Appliance 1Gbps 是否与 IBM 的负载均衡器产品兼容？
{:faq}

兼容。FSA 1Gbps 与云负载均衡服务、本地负载均衡器以及 Citrix Netscaler VPX 和 MPX 兼容。

## 公共流量会首先通过我的负载均衡器还是防火墙？
{:faq}

公共因特网流量会首先通过负载均衡产品，然后通过 Hardware Firewall 产品，最后通过 NetScaler 产品（以及客户服务器）。

## IBM 是否对防火墙带宽收费？
{:faq}

FortiGate Security Appliance 1Gbps 不按带宽用量收费。而且，FSA 可通过限制服务器必须响应的流量来降低总带宽利用率。
{:faq}

## 我的 Windows 防火墙中灰显的端口是什么端口？
{:faq}

IBM Cloud 提供了很多不同的服务可用于您的服务器，包括 Evault、SNMP 和 Nagios 监视。这些服务需要我们的内部系统与您的服务器在一定程度上进行通信。“异常”列表中显示的灰显端口是仅在内部网络端口上打开的端口。这些端口在公用（因特网）网络连接上也会被阻止。内部网络是安全网络，因此会将打开这些端口视为是安全的。

通常，这些端口是无法修改的；但是，如果您重置了防火墙规则，那么会从“异常”列表中清除这些端口。请注意，重置防火墙规则可能会对这些额外的服务产生负面影响，还可能会导致其他问题，具体取决于服务器配置。

## 我应允许哪些 IP 范围通过防火墙？
{:faq}

有关允许通过防火墙的 IP 地址和 IP 范围的列表，请转至[此处](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-ibm-cloud-ip-ranges)。 

## FortiGate Security Appliance 1Gbps 最多可保护多少台服务器？
{:faq}

FortiGate Security Appliance 1Gbps 可保护公用 VLAN 上的每台服务器。但是，请务必注意，这些防火墙设备是以 2Gbps 上行端口速度连接的，因此我们建议您适当地增加防火墙实例数来满足您的应用程序性能需求。要完成此操作，可以在 pod 内部署额外的公用 VLAN 防火墙，以便添加额外的防火墙和关联的计算资源。

## 每种防火墙产品都随附了哪些 VPN 选项？
{:faq}

并非所有防火墙都提供 VPN，也不是所有 VPN 选项都相同。常规 VPN 选项如下：

* 每个客户都可以使用 SSL VPN 连接来访问我们的专用网络，连接数量不限。要建立这些连接，可以在登录到客户门户网站时单击页面顶部的 VPN 链接。
* 对于每个帐户，客户还可以得到一个 PPTP VPN。客户可以向其帐户中成批添加更多 PPTP VPN 用户，每添加 5 个用户每月会额外收取 5 美元。
* IBM Cloud 还提供了基本多租户 IPSec VPN 服务。
* FortiGate Security Appliance 1Gbps 提供了 SSL 和 IPSec VPN 选项，且仅允许访问公用网络（无权访问 IBM Cloud 专用网络）。
* 网关为公用网络或专用网络提供了 SSL、IPSec 和 OpenVPN 功能。
* NetScaler 产品可为公用网络或专用网络提供 SSL 和 IPSec VPN。
* 客户还可以在其 IBM Cloud 环境中将 VPN 解决方案部署到服务器上。

## 我如果选择“高可用性”选项，那么在使用此功能之前必须执行哪些步骤？
{:faq}

不需要执行任何步骤。订购 HA 后，IBM Cloud 会自动以 HA 配置供应设备。如果主要设备发生故障，那么辅助被动设备会接管主要活动实例，并开始传递流量。此故障转移通常是自动的，但最好监视服务器并确保流量能成功传递。

## 哪些防火墙产品支持公用到专用 NAT 和/或专用 VLAN 分段？
{:faq}

Hardware Firewall 产品无法访问专用网络。使用网关可以直接提供这些功能。NetScaler 产品可以访问公用网络和专用网络。
