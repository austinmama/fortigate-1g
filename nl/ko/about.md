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

# 정보

FSA(Fortigate Security Appliance) 1Gbps는 공용 VLAN 상의 임의의 서버 또는 모든 서버를 보호하는 서버에서 상위로 연결된 전용 단일 테넌트 네트워크 디바이스입니다. 서버와 별도로 구매할 수 있으며 언제든지 VLAN에 추가할 수 있습니다. IBM Cloud는 전용 어플라이언스 내의 가상 도메인(VDOM) 내에 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://www.fortinet.com/sites/default/files/productdatasheets/FortiGate-300C.pdf){: new_window}을 배치하며 이로 인해 고객이 디바이스의 무결성을 훼손하지 않고 가상 도메인에 완전히 액세스할 수 있습니다. 

FSA 1Gbps를 사용하면 고객이 고급 기능 및 기타 제품에 비해 훨씬 정교하게 디바이스를 미세 조정하는 기능에 액세스할 수 있습니다. 방화벽은 트래픽이 서버에 도달하기 전에 트래픽을 차단하거나 구체화합니다. 주요한 장점은 서버가 '양호한' 트래픽 처리에만 집중할 수 있으며 덜 중요한 통신에 대한 대역폭을 제한할 수 있다는 점입니다. 

고객이 SSH를 사용하여 웹 기반의 FortiOS GUI 또는 CLI(명령행 인터페이스)를 통해 FSA를 관리할 수 있습니다. 구성이 동기화된 활성-비활성 배치로 두 가지 어플라이언스를 제공하는 고가용성도 주문할 수 있습니다.

월별 서버 대역폭이 서버 스위치 포트에 기록되므로 FSA 1Gbps에 의해 차단된 트래픽은 월별 할당으로 간주되지 않으며 원하지 않는 트래픽에 대해 비용을 지불할 필요가 없습니다.

## 개요 및 기능

**의도된 사용:** 단일 공용 VLAN 보호

**사용자 인터페이스:** Fortigate GUI 및 명령행 인터페이스

**기능:** Stateful 패킷 조사, VLAN 보호, Ingress 방화벽 규칙, Egress 방화벽 규칙, NAT, SSL VPN 종료, IPSec VPN 종료, 고급 로깅, 고가용성(선택사항)

**처리량:** 2,000Mbps
