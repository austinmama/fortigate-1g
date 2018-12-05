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

# FortiGate Security Appliance 보안

보안 및 규제 준수를 충족하도록 FSA(FortiGate Security Appliance) 1Gbps를 구성할 수 있습니다. IBM Cloud는 무작위로 지정되는 비밀번호가 있는 VDOM 관리자 계정을 제공합니다. 고객이 해당 비밀번호를 변경하고, 읽기 전용 사용자를 작성하며 지정된 소스 IP(최대 세 개)의 트래픽만 허용하는 "신뢰할 수 있는 호스트"를 기반으로 하여 액세스를 제한할 수 있습니다. 세 가지 활동을 완료하려면 다음을 수행하십시오.

1. [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/){: new_window}의 **디바이스 세부사항** 페이지에서 찾을 수 있는 인증 정보를 사용하여 어플라이언스에 로그인하십시오. [FortiGate Security Appliance를 관리](managing-fsa.html)하는 방법에 대한 지시사항에 따라 인증 정보를 찾으십시오.
2. 어플라이언스에 로그인한 다음 **시스템 > 관리 > 관리자**로 이동하십시오. 모든 액세스 및 변경사항이 로그됩니다.
3. 개별 인터페이스를 구성하려면 **시스템 > 네트워크 > 인터페이스**로 이동하십시오.

    관리 인터페이스에 대한 액세스를 필요한 프로토콜(일반적으로 HTTPS 및 SSH. 이동형 암호화를 제공하기 때문)만으로 제한하며 추가 보안이 필요한 경우 관리 인터페이스에 대한 외부 액세스를 사용하지 않도록 설정할 수 있습니다. "내부" 인터페이스(고객의 공용 VLAN이 상주하는 인터페이스)에서 적절한 프로토콜을 사용하도록 설정하고, "외부" 인터페이스(공용 인터넷 트래픽이 수신되는 인터페이스)에서 모든 프로토콜을 사용하지 않도록 설정하여 위 사항을 수행할 수 있습니다. 이 추가 보안 방법을 사용하려면 사용자가 FSA를 관리할 수 있도록 VLAN 내부에 배치된 서버가 있어야 합니다. 
