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

# 已知限制
「FortiGate 安全應用裝置 (FSA) 1Gbps」有下列已知限制：

* 由於處理 ARP 的方式而與「Windows 網路負載平衡 (NLB)」不相容。

* 「高可用性」失效接手功能不會向使用者公開。如果主要防火牆故障，但未自動進行失效接手，則需要支援問題單。建議對重要服務進行裝置監視，以確保防火牆適當地傳遞資料流量。

* 「FortiGate 安全應用裝置」無法在目前與「網路閘道」、「硬體防火牆」或另一個「FortiGate 安全應用裝置」相關聯的 VLAN 上進行部署。

* 「FortiGate 安全應用裝置」與單一公用客戶 VLAN（「內部」VLAN）相關聯，且無法存取專用網路。
