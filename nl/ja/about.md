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

# Fortigate Security Appliance 1Gbps について
{: #about-fortigate-security-appliance-1gbps}

Fortigate Security Appliance  (FSA) 1Gbps は、サーバーの上流に接続する専用の単一テナント・ネットワーク・デバイスで、パブリック VLAN 上の任意またはすべてのサーバーを保護します。 サーバーとは別に購入し、いつでも VLAN に追加できます。  IBM© Cloud では、仮想ドメイン (VDOM) 内の[カスタマー・ポータル![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://www.fortinet.com/sites/default/files/productdatasheets/FortiGate-300C.pdf){: new_window}が専用アプライアンスにデプロイされます。これにより、お客様は、デバイスの整合性を損なうことなく、その仮想ドメインにフルアクセスできます。 

FSA 1Gbps では、お客様は、拡張機能にアクセスすること、および他の製品よりもはるかに詳細にデバイスを微調整することができます。 このファイアウォールにより、トラフィックがサーバーに到達する前に、それらのトラフィックがブロックまたはシェーピングされます。 主な利点は、サーバーで「有効な」トラフィックのみ処理すれば済む点、および重要度が低い通信に対しては帯域幅を制限できる点です。 

お客様は、SSH を使用して、Web ベースの FortiOS GUI または CLI (コマンド・ライン・インターフェース) を通じて FSA を管理できます。 高可用性も注文できます。高可用性では、構成が同期される、アクティブ・パッシブ・デプロイメントの 2 つのアプライアンスが提供されます。

サーバー・スイッチ・ポートで毎月のサーバー帯域幅が記録されるため、FSA 1Gbps によってブロックされたトラフィックは毎月の割り当てに対してカウントされません。このため、不要なトラフィックに対して支払いを行う必要はありません。

## 概要および機能

**使用目的:** 単一のパブリック VLAN の保護

**ユーザー・インターフェース:** Fortigate GUI およびコマンド・ライン・インターフェース

**機能:** ステートフル・パケット検査、VLAN 保護、入口ファイアウォール・ルール、退出ファイアウォール・ルール、NAT、SSL VPN 終端、IPSec VPN 終端、拡張ロギング、高可用性 (オプション)

**スループット:** 1Gbps (2Gbps 集約)
