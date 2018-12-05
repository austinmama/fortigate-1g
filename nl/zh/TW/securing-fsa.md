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

# 保護 FortiGate Security Appliance

您可以配置 FortiGate Security Appliance (FSA) 1Gbps 來符合安全及法規需求。IBM Cloud 提供一個「VDOM 管理者」帳戶，以及一個隨機指派的密碼。客戶可以輪換該密碼、建立唯讀使用者，以及根據「授信主機」（只接受來自指定來源 IP（最多三個）的資料流量）來限制存取權。若要完成這些活動，請執行下列步驟：

1. 使用[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window} 的**裝置詳細資料**頁面中找到的認證來登入應用裝置。請遵循如何[管理 FortiGate Security Appliance](managing-fsa.html) 指示來尋找認證。
2. 登入應用裝置之後，導覽至**系統 > 管理 > 管理者**。會記載所有存取及變更。
3. 若要配置個別介面，請導覽至**系統 > 網路 > 介面**。

    您可以將管理介面的存取權限制只給其所需的通訊協定（一般為 HTTPS 和 SSH，因為這提供傳輸中加密），或者為了獲得其他安全，您可以停用管理介面的外部存取權。若要達到此目的，您可以在「內部」介面（客戶公用 VLAN 所在的介面）上啟用適當的通訊協定，以及在「外部」介面（從其中接收公用網際網路資料流量的介面）上停用所有通訊協定。這種額外的安全措施會要求使用者將伺服器放置在從其中管理 FSA 的 VLAN 內。 
