---

copyright:
  years: 2017,2018
lastupdated: "2018-01-18"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Visualizar seus firewalls

Para ver quais VLANs são protegidas com firewalls e encontrar mais detalhes sobre firewalls individuais, acesse a página VLANs.

1. Em seu navegador, abra [Portal do Cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} e efetue login em sua conta.
2. Na navegação do Portal do cliente, selecione **Rede > Gerenciamento de
IP > VLANs**.

Cada linha na tabela representa uma VLAN em sua infraestrutura. O IBM Cloud
preenche as informações "Número da VLAN" e "Roteador primário" automaticamente indicando
o número verdadeiro da VLAN e o roteador no qual ela está configurada. O campo "Nome"
pode ser usado para dar à VLAN um nome reconhecível (como DMZ, Intranet, Público ou Banco de dados).

A coluna da extrema direita **Gateway/Firewall** contém detalhes sobre qual proteção de firewall está em vigor, por exemplo:

- **Incluir firewall** indica que não há firewalls em vigor para servidores nessa VLAN.
- **Servidores individualmente protegidos** indica que um
ou mais servidores estão usando um Firewall de hardware (compartilhado) e que não há um
Firewall de hardware (dedicado), um FortiGate Security Appliance ou um Gateway de rede em
vigor. Os firewalls de VLAN e os gateways de rede não podem ser colocados em uma VLAN que
tem servidores protegidos individualmente.
- **Firewall-vlanXXXX.networklayer.com** indica que há um
Firewall de hardware (dedicado) ou um FortiGate Security Appliance em vigor. Somente um
firewall de VLAN ou um gateway de rede pode ser associado a uma VLAN, mas um servidor pode
ser protegido na VLAN pública por um firewall de VLAN e associado na rede privada a um
gateway de rede.
- **Nome do gateway** indica a VLAN associada a esse gateway de rede.

## Detalhes dos servidores protegidos individualmente

Para VLANs que têm **Servidores protegidos individualmente** no
campo **Gateway/Firewall**, é possível clicar no link do número da
VLAN associada para exibir os detalhes da VLAN, incluindo os dispositivos associados.

Na lista de dispositivos associados, você pode clicar em cada dispositivo e rolar
para a parte inferior da guia Configuração. Você verá **Firewall** na
seção Complementos com um status de **Instalado** ou **Não
instalado**.

- **Não instalado** indica que nenhum firewall está em vigor
para esse dispositivo.
- **Instalado** indica que um firewall está em vigor e você
terá uma guia **Firewall** disponível no dispositivo no qual
poderá gerenciar a configuração do firewall.

## Detalhes do firewall dedicado

Para as VLANs que têm **Firewall-vlanXXXX.networklayer.com** no
campo **Gateway/Firewall**, você pode clicar nesse link de firewall
para exibir os detalhes do Firewall. Os detalhes do dispositivo incluem o roteador
associado, VLAN, sub-redes IPv4/IPv6, os dispositivos associados a essa VLAN e os
controles para rotear o tráfego através ou ao redor do firewall.

Os dispositivos FortiGate Security Appliance terão o IP de gerenciamento, o nome de
usuário e a senha. O gerenciamento dos FortiGate Security Appliances é concluído por meio da sua própria GUI ou console baseado em SSH.

## Detalhes do gateway de rede

Para VLANs que têm um nome de dispositivo de gateway de rede no campo
**Gateway/Firewall**, você pode clicar no nome do gateway de rede para
exibir os detalhes dele. Os detalhes do dispositivo incluem as opções de gerenciamento de gateway de rede e de VLANs de backend (BCR) e front-end (FCR) associadas.
