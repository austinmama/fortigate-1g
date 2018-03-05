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

# 기본 배치

FSA(FortiGate Security Appliance) 1Gbps는 전용 어플라이언스에 단일 가상 도메인(일반적으로 firewall001)으로 배치됩니다. 고객이 어플라이언스의 리소스(프로세서, 메모리 등)에 대해 전체 액세스 권한을 가지지만 IBM Cloud가 디바이스를 효과적으로 지원할 수 있도록 디바이스 레벨 구성에 대한 액세스는 제한됩니다.

FSA는 NAT 모드로 배치되고 공용 네트워크 인프라 내의 두 VLAN/네트워크에 상주합니다. 외부 VLAN은 트래픽이 데이터 센터로 들어와서 FSA로 라우트되는 IBM Cloud 공용 VLAN입니다. 내부 VLAN은 고객이 지정한 보호되는 퍼블릭 프론트 엔드 고객 라우터(FCR) VLAN이며 고객의 서버 리소스가 상주하는 곳입니다.  

IBM Cloud는 프로비저닝 프로세스 동안 이러한 두 네트워크 각각에 두 개의 결합된 1G 인터페이스를 사용하여 FSA를 배치합니다. 또한 IBM Cloud는 고객이 사용할 수 없는 디바이스의 프로비저닝 및 유지보수를 위해 단일 인터페이스를 배치합니다.

방화벽은 IBM Cloud 내부 관리 네트워크가 방화벽을 통해 디바이스에 액세스하는 것을 허용하도록 디자인된 특정 규칙(softlayer-admin)을 포함하여, 허용되는 모든 IPv4 및 IPv6 트래픽과 함께 배치됩니다. 서비스 거부(DoS) 보호 및 대부분의 기타 필터는 강제 실행되도록 구성되지 않습니다.
