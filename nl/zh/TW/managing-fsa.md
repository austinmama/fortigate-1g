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

# 管理 FortiGate Security Appliance 1Gbps
{: #managing-the-fortigate-security-appliance-1gbps}

第一次將防火牆新增至 VLAN 時，允許所有資料流量。您需要將規則新增至防火牆，才能控制資料流量。 

1. 從瀏覽器中，開啟[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window} 並登入您的帳戶。
2. 在「客戶入口網站」導覽中，選取**網路 > IP 管理 > VLAN**。 

	**提示：** 若只要檢視公用 VLAN，請按一下**過濾器**下拉清單，然後在**主要路由器**欄位中輸入 ``fcr``。
3. 捲動至您要管理的 VLAN，然後在**閘道/防火牆**直欄中按一下防火牆名稱的鏈結，以移至**裝置詳細資料**頁面。
4. 在**裝置詳細資料**頁面中，您可以檢視相關聯的子網路、防火牆路由的現行「狀態」，以及管理資訊。 

	管理資訊包括**管理 IP**、**使用者名稱**及**密碼**。此「管理 IP」依預設是可公開存取的。對於自動化目的或進階的使用案例，也可以使用具有相同 IP 和認證的 SSH 進行管理。
5. 若要存取 GUI，請按一下「管理 IP」鏈結，並輸入所提供的使用者名稱和密碼。 
6. 從「管理使用者介面」中，您可以「VDOM 管理者」的身分來管理 FortiGate Security Appliance。對於無法使用「管理使用者介面」來存取的管理功能（例如管理 SSL 憑證、起始手動 HA 失效接手、重新開機、升級或執行預設配置還原），需要開支援問題單。

Fortinet 會維護可在配置期間用作參照的[線上文件（包括互動式錦囊妙計）![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://cookbook.fortinet.com/fortigate/){: new_window}。
