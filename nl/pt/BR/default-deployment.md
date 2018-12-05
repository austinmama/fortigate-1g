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

# Implementação padrão

O FortiGate Security Appliance (FSA) 1Gbps é implementado como um único domínio
virtual (geralmente firewall001) em um dispositivo dedicado. O cliente tem acesso total
aos recursos do dispositivo (processadores, memória e assim por diante), mas o acesso à
configuração no nível do dispositivo é restrito para assegurar que o IBM Cloud possa
efetivamente suportar o dispositivo.

O FSA é implementado no modo NAT e reside em duas VLANs/redes dentro da
infraestrutura de rede pública. A VLAN externa é a VLAN pública do IBM Cloud, na qual o
tráfego entra no data center e é roteado para o FSA. A VLAN interna é a VLAN do FCR
(Frontend Customer Router) público protegido designado do cliente e é onde os recursos do
servidor do cliente residem.  

O IBM Cloud implementa o FSA com duas interfaces ligadas de 1G em cada uma dessas
duas redes durante o processo de fornecimento. O IBM Cloud também implementa uma única
interface para fornecimento e manutenção do dispositivo que não é disponibilizada para os
clientes.

O firewall é implementado com todo o tráfego de IPv4 e IPv6 permitido, incluindo
uma regra específica (softlayer-admin) projetada para permitir que a rede de
administração interna do IBM Cloud acesse dispositivos por meio do firewall. As
proteções de negação de serviço e muitos outros filtros são configurados para não
serem executados.
