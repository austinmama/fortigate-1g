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

# 알려진 제한사항
FSA(FortiGate Security Appliance) 1Gbps에는 다음과 같은 알려진 제한사항이 있습니다.

* ARP가 처리되는 방법으로 인해 Windows NLB(Network Load Balancing)와 호환 가능하지 않습니다.

* 고가용성 장애 복구 기능이 사용자에게 공개되지 않습니다. 마스터 방화벽이 제대로 작동하지 않으나 자동으로 장애 복구되지 않는 경우 지원 티켓이 필요합니다. 방화벽이 적절히 트래픽을 전달하는지 확인하기 위해, 중요한 서비스에 대한 디바이스 모니터링을 수행하도록 권장됩니다.

* FortiGate Security Appliance를 현재 네트워크 게이트웨이, 하드웨어 방화벽 또는 기타 FortiGate Security Appliance와 연관된 VLAN에 배치할 수 없습니다.

* FortiGate Security Appliance는 단일 공용 고객 VLAN("내부" VLAN)과 연관되며 사설 네트워크에 액세스하지 않습니다.
