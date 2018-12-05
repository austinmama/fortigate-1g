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

# 既知の制限
FortiGate Security Appliance (FSA) 1Gbps には、以下の既知の制限があります。

* ARP の処理方法が原因で Windows Network Load Balancing (NLB) とは非互換です。

* 高可用性フェイルオーバー機能は、ユーザーに公開されません。 マスター・ファイアウォールで障害が発生して、自動的にフェイルオーバーしない場合、サポート・チケットが必要です。 ファイアウォールがトラフィックを適切に渡すことができるように、重要なサービスはデバイス・モニタリングすることをお勧めします。

* FortiGate Security Appliance は、ネットワーク・ゲートウェイ、ハードウェア・ファイアウォール、または他の FortiGate Security Appliance に現在関連付けられている VLAN にはデプロイできません。

* FortiGate Security Appliance は、単一のパブリック・カスタマー VLAN (「内部」VLAN) に関連付けられ、プライベート・ネットワークにはアクセスできません。
