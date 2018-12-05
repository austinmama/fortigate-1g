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

# FortiGate Security Appliance 관리

방화벽이 처음 VLAN에 추가될 때는 모든 트래픽이 허용됩니다. 트래픽을 제어하려면 방화벽에 규칙을 추가해야 합니다. 

1. 브라우저에서 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/){: new_window}을 열고 사용자 계정으로 로그인하십시오.
2. 고객 포털 탐색에서 **네트워크 > IP 관리 > VLAN**을 선택하십시오. 

	**팁:** 공용 VLAN만 보려면 **필터** 드롭 다운을 클릭하고 **1차 라우터**에 ``fcr``을 입력하십시오.
3. 관리할 VLAN으로 스크롤하여 **게이트웨이/방화벽** 열에서 방화벽 이름의 링크를 클릭하여 **디바이스 세부사항** 페이지로 이동하십시오.
4. **디바이스 세부사항** 페이지에서 연관된 서브넷, 방화벽 라우팅의 현재 "상태" 및 관리 정보를 볼 수 있습니다. 

	관리 정보에는 **관리 IP**, **사용자 이름** 및 **비밀번호**가 포함됩니다. 이 관리 IP는 기본적으로 공용으로 액세스될 수 있습니다. 자동화 용도이거나 고급 유스 케이스의 경우 동일한 IP 및 인증 정보로 SSH를 사용하여 관리를 사용할 수도 있습니다.
5. GUI에 액세스하려면 관리 IP 링크를 클릭하고 제공된 사용자 이름 및 비밀번호를 입력하십시오. 
6. 관리 UI에서 VDOM 관리자로서 FortiGate Security Appliance를 관리할 수 있습니다. SSL 인증서 관리, 수동 HA 장애 복구 시작, 재부팅, 업그레이드 또는 기본 구성 복원 수행과 같이 관리 UI를 통해 사용할 수 없는 관리 기능의 경우에는 지원 티켓이 필요합니다.

Fortinet은 구성 동안 참조로 사용할 수 있는 [online documentation including an interactive cookbook ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://cookbook.fortinet.com/fortigate/){: new_window}을 유지보수합니다.
