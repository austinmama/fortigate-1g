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

# 常見問題 (FAQ)

下列是使用 FortiGate Security Appliance (FSA) 1Gbps 時的常見問題。

## 何謂防火牆？
{:faq}

防火牆是從伺服器上游連接的網路裝置。在到達伺服器之前，防火牆會封鎖不想要的資料流量進到伺服器。

## 為何應該使用防火牆？
{:faq}

擁有防火牆的主要優點在於您的伺服器只需處理「良好的」資料流量 - 這表示您的資源僅用於其預期目的，而不是處理不想要的資料流量。

## IBM 提供哪些防火牆產品？
{:faq}

您可以找到 IBM Cloud 中提供的所有防火牆產品的詳細比較資料，方法是檢閱本[主題 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](/docs/infrastructure/fortigate-10g/explore-firewalls.html#explore-firewalls){: new_window}。 

## FortiGate Security Appliance 1Gbps 是否與 IBM 的負載平衡器產品相容？
{:faq}

是的。FSA 1Gbps 與雲端負載平衡服務、本端負載平衡器，以及 Citrix Netscaler VPX 和 MPX 相容。

## 公用資料流量是否先通過負載平衡器或防火牆？
{:faq}

負載平衡產品會先從公用網際網路進來、接著是 Hardware Firewall 產品，最後是 NetScaler 產品（連同客戶伺服器）。

## IBM 是否會收取防火牆頻寬費用？
{:faq}

FortiGate Security Appliance 1Gbps 不會針對頻寬進行計量。此外，FSA 還可以透過限制伺服器必須回應的資料流量來減少總頻寬使用率。{:faq}

## 什麼是 Windows 防火牆中的灰色埠？
{:faq}

IBM Cloud 提供許多可用於伺服器的不同服務，包括 Evault、SNMP 和 Nagios 監視。這些服務需要我們的內部系統在部分程度上與您的伺服器通訊。您在「例外情況」清單中看到的灰色埠是只在內部網路埠上開啟的埠。其仍會在公用（網際網路）網路連線上遭到封鎖。因為內部網路是一個安全的網路，所以讓這些埠開啟會被認為是安全的。

這些埠一般無法修改；但是，如果您重設防火牆規則，則會從「例外情況」清單中將這些埠清除。請注意，重設防火牆規則可能會對這些其他服務產生不利的影響，而且根據您的伺服器配置，也可能會導致其他問題。

## 哪些 IP 範圍容許通過防火牆？
{:faq}

如需容許通過防火牆的 IP 位址及 IP 範圍清單，請進到[這裡](/docs/infrastructure/hardware-firewall-dedicated/ips.html){: new_window}。 

## FortiGate Security Appliance 1Gbps 會保護的最大伺服器數目是多少？
{:faq}

FortiGate Security Appliance 1Gbps 可以保護公用 VLAN 上的每台伺服器。不過，需要注意的是，由於這些防火牆裝置連接 2Gbps 的上行鏈路，因此我們建議擴充防火牆實例的數目以符合應用程式的效能需求。您可以透過在 pod 內部署其他公用 VLAN 防火牆來達到此目的，以允許新增其他防火牆及相關聯的計算資源。

## 每一個防火牆產品隨附哪些 VPN 選項？
{:faq}

並非所有防火牆都提供 VPN，而且並非所有 VPN 選項都相同。VPN 的一般選項如下：

* 每個客戶都可以收到連接到我們的專用網路的無限制 SSL VPN 連線。這些連線可以進行建立，方法是在登入「客戶入口網站」時按一下頁面頂端的 VPN 鏈結。
* 客戶也可以為每一個帳戶收到一個 PPTP VPN。他們可以將其他 PPTP VPN 使用者以 5 個一組、每個月額外 5 美元的價格新增到其帳戶中。
* IBM Cloud 還提供基本的多方承租戶 IPSec VPN 服務。
* FortiGate Security Appliance 1Gbps 提供 SSL 和 IPSec VPN 選項，並只能存取公用網路（無法存取 IBM Cloud 專用網路）。
* 「網路閘道」在公用或專用網路上提供 SSL、IPSec 及 OpenVPN 功能。
* NetScaler 產品可以在公用或專用網路上提供 SSL 及 IPSec VPN。
* 客戶也可以將 VPN 解決方案部署到其 IBM Cloud 環境內的伺服器上。

## 當我選取「高可用性」選項時，我必須採取哪些步驟來善用此特性？
{:faq}

都不用。在 HA 中訂購時，IBM Cloud 會自動在 HA 配置中佈建應用裝置。萬一主要裝置發生故障，次要被動的裝置將接管作為主要作用中的實例並開始傳遞資料流量。雖然這種失效接手一般是自動的，但最佳作法是監視伺服器並確保資料流量順利被傳遞。

## 哪些防火牆產品支援公用到專用 NAT 及（或）專用 VLAN 區段？
{:faq}

沒有任何 Hardware Firewall 產品可以存取專用網路。需要「網路閘道」在行內提供這些功能，而 NetScaler 產品可以同時存取公用和專用網路。
