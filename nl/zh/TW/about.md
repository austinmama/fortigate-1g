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

# 關於

Fortigate Security Appliance 1Gbps (FSA) 是一個從伺服器上游連接的專用單一租戶網路裝置，用於保護公用 VLAN 上的任何或所有伺服器。它是與伺服器分開購買的，且可隨時新增至 VLAN 中。IBM Cloud 會在專用應用裝置上的「虛擬網域 (VDOM)」內部署[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://www.fortinet.com/sites/default/files/productdatasheets/FortiGate-300C.pdf){: new_window}，容許客戶完全存取該虛擬網域，而不會影響裝置的完整性。 

使用 FSA 1Gbps，客戶可以存取進階功能，並且能夠將裝置微調到比其他產品還要高的程度。防火牆在資料流量快要到達伺服器之前會封鎖或調整資料流量。主要優點在於伺服器只需處理「良好的」資料流量，而且可能會針對較不重要的通訊限制頻寬。 

客戶可以透過 Web 型的 FortiOS GUI 或使用 SSH 的 CLI（指令行介面）來管理 FSA。也可以訂購高可用性，其可在主動-被動部署（具有同步化的配置）中提供兩個應用裝置。

由於每月的伺服器頻寬會在伺服器交換器埠中記錄，因此 FSA 1Gbps 封鎖的資料流量不會計入您的每月分配量中，進而可消除支付不想要的資料流量的需求。

## 概觀及特性

**預期的使用：** 單一公用 VLAN 保護

**使用者介面：** Fortigate GUI 及指令行介面

**特性：** 有狀態封包檢驗、VLAN 保護、進入防火牆規則、外出防火牆規則、NAT、SSL VPN 終止、IPSec VPN 終止、進階記載、高可用性（選用）

**傳輸量：** 1Gbps（總計 2Gbps）
