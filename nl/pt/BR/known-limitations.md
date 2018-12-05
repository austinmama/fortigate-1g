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

# Limitações conhecidas
O FortiGate Security Appliance (FSA) 1Gbps tem as seguintes limitações conhecidas:

* Incompatível com o Balanceamento de Carga de Rede (NLB) do Windows devido à maneira como o ARP é processado.

* A funcionalidade de failover de alta disponibilidade não é exposta ao usuário. Se
o firewall principal tiver um mau funcionamento, mas não fizer failover automaticamente,
um chamado de suporte será necessário. O monitoramento de dispositivo para serviços
críticos é recomendável para assegurar que os firewalls estejam passando o tráfego
apropriadamente.

* O FortiGate Security Appliance não pode ser implementado em uma VLAN atualmente associada a um Gateway de rede, a um Hardware Firewall ou a outro FortiGate Security Appliance.

* O FortiGate Security Appliance está associado a uma única VLAN pública do cliente (a VLAN "interna") e não pode acessar a rede privada.
