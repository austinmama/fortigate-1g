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

# 預設部署

「FortiGate 安全應用裝置 (FSA) 1Gbps」會在專用的應用裝置上部署為單一「虛擬網域」（一般為 firewall001）。客戶可以完全存取應用裝置的資源（處理器、記憶體等），但對裝置層次配置的存取權受到限制，以確保 IBM Cloud 可以有效支援該裝置。

FSA 在 NAT 模式下進行部署，並位於公用網路基礎架構內的兩個 VLAN/網路中。外部 VLAN 是資料流量進入資料中心並遞送至 FSA 的 IBM Cloud 公用 VLAN。內部 VLAN 是客戶的已指派受保護的公用 FCR（前端客戶路由器）VLAN，是客戶的伺服器資源所在的位置。  

IBM Cloud 在佈建過程中會在這兩個網路的每一個網路上部署含兩個結合 1G 介面的 FSA。IBM Cloud 也會部署一個單一介面，用來佈建及維護未提供給客戶使用的裝置。

防火牆會進行部署，並允許所有的 IPv4 和 IPv6 資料流量，包括特定的規則 (softlayer-admin)，而其旨在允許 IBM Cloud 內部管理網路通過防火牆來存取裝置。「拒絕服務」保護和大部分其他過濾器會配置為不施行。
