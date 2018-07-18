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

# Sobre

Um Fortigate Security Appliance (FSA) 1Gbps é um dispositivo de rede dedicado de
locatário único conectado para envio de dados de um servidor que protege qualquer um ou
todos os servidores em uma VLAN pública. Ele é comprado separadamente de um servidor e pode ser
incluído em uma VLAN a qualquer momento.  O IBM Cloud implementa o
[Portal
do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link
externo")](http://www.fortinet.com/sites/default/files/productdatasheets/FortiGate-300C.pdf){: new_window} dentro de
um domínio virtual (VDOM) no dispositivo dedicado, permitindo aos clientes acesso total a
esse domínio virtual sem comprometer a integridade do dispositivo. 

Com o FSA 1Gbps, os clientes têm acesso a recursos avançados e a capacidade de
ajustar o dispositivo para um grau muito mais alto do que outros produtos. O firewall
bloqueia ou forma o tráfego antes mesmo que o tráfego atinja o servidor. As principais
vantagens são que um servidor tem apenas que manipular o tráfego 'bom' e a possibilidade de se restringir a largura de
banda para comunicações menos críticas. 

Os clientes podem gerenciar o FSA por meio da GUI FortiOS baseada na web ou pela
CLI (interface da linha de comandos) usando SSH. A alta disponibilidade também pode ser
solicitada, que fornece configurações sincronizadas a dois dispositivos em implementação
ativa/passiva.

Como a largura de banda mensal do servidor é registrada na porta do comutador do
servidor, o tráfego bloqueado pelo FSA 1Gbps não é contado em relação a alocações mensais,
eliminando a necessidade de pagar por tráfego indesejado.

## Visão geral e recursos

**Uso desejado:** proteção à VLAN pública única

**Interface com o usuário:** GUI do Fortigate e interface da
linha de comandos

**Recursos:** inspeção de pacote stateful, proteção à VLAN,
regras de firewall ingresso, regras de firewall egresso, NAT, terminação de VPN SSL,
terminação de VPN IPSec, criação de log avançada, alta disponibilidade (opcional)

**Rendimento:** 1 Gbps (2 Gbps agregados)
