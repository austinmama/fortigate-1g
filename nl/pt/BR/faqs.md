---

copyright:
  years: 2017,2018
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:faq: data-hd-content-type='faq'}

# Perguntas mais frequentes

A seguir estão as perguntas mais frequentes ao trabalhar com o firewall do FortiGate Security Appliance (FSA) 1Gbps.

## O que é um firewall?
{:faq}

Um firewall é um dispositivo de rede conectado para envio de dados de um servidor. O firewall bloqueia tráfego indesejado de um servidor antes que o servidor seja atingido.

## Por que devo usar um firewall?
{:faq}

A principal vantagem de ter um firewall é que seu servidor terá de manipular apenas o tráfego "bom", o que significa que seu recurso está sendo usado exclusivamente para o propósito desejado, não para a manipulação do tráfego indesejado.

## Quais produtos de firewall a IBM oferece?
{:faq}

Você pode encontrar uma comparação detalhada de todos os produtos de firewall oferecidos no IBM Cloud revisando este [tópico ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](/docs/infrastructure/fortigate-10g/explore-firewalls.html#explore-firewalls){: new_window}. 

## O FortiGate Security Appliance 1Gbps é compatível com produtos de balanceador de carga da IBM?
{:faq}

Sim. O FSA 1Gbps é compatível com o serviço de balanceamento de carga em nuvem, o balanceador de carga local, bem como o Citrix Netscaler VPX e MPX.

## O tráfego público passa primeiro através do meu balanceador de carga ou do firewall?
{:faq}

Vindos da Internet pública, os produtos de balanceamento de carga são os primeiros, os produtos do Hardware Firewall vêm em seguida e os produtos NetScaler são os últimos (junto com os servidores dos clientes).

## A IBM cobra pela largura de banda do firewall?
{:faq}

O FortiGate Security Appliance 1Gbps não é medido para largura de banda. Além disso, o FSA pode reduzir a utilização de largura de banda total limitando o tráfego ao qual os servidores devem responder.
{:faq}

## Quais são as portas esmaecidas no meu firewall do Windows?
{:faq}

O IBM Cloud oferece muitos serviços diferentes que você pode utilizar com seu servidor, incluindo de monitoramento Evault, SNMP e Nagios. Esses serviços requerem que os nossos sistemas internos se comuniquem com seu servidor em algum grau. As portas esmaecidas que você vê na lista Exceções são portas abertas apenas na porta de rede interna. Elas ainda estão bloqueadas na conexão de rede pública (Internet). Como a rede interna é uma rede segura, ter essas portas abertas é considerado seguro.

Essas portas geralmente não podem ser modificadas; no entanto, se você reconfigurar as regras de firewall, as portas serão removidas da lista Exceções. Esteja ciente de que a reconfiguração das regras de firewall pode ter um efeito negativo nesses serviços adicionais e também pode causar outros problemas dependendo de sua configuração do servidor.

## Quais intervalos de IP posso permitir através do firewall?
{:faq}

Para obter a lista de endereços IP e intervalos de IP a serem permitidos através do firewall, clique [aqui](/docs/infrastructure/hardware-firewall-dedicated/ips.html){: new_window}. 

## Qual é o número máximo de servidores que o FortiGate Security Appliance 1Gbps protegerá?
{:faq}

O FortiGate Security Appliance 1Gbps pode proteger cada servidor em uma VLAN pública. No entanto, é importante observar que, como esses dispositivos de firewall são conectados com Uplink de 2 Gbps, recomendamos escalar o número de instâncias do firewall para atender às necessidades de desempenho de seu aplicativo. Você pode fazer isso implementando firewalls adicionais de VLAN pública em um pod para permitir que firewall adicional e recursos de cálculo associados sejam incluídos.

## Quais opções de VPN são incluídas em cada produto de Firewall?
{:faq}

Nem todos os firewalls oferecem VPN e nem todas as opções de VPN são as mesmas. As opções gerais de VPN são:

* Cada cliente recebe conexões VPN SSL ilimitadas com nossa rede privada. Essas conexões podem ser estabelecidas clicando no link VPN na parte superior da página quando se está com login efetuado no Portal do cliente.
* Os clientes também recebem uma VPN PPTP por conta. Eles podem incluir usuários adicionais de VPN PPTP em suas contas em pacotes de 5 por um adicional de US$ 5/mês.
* O IBM Cloud também oferece um serviço VPN IPSec de vários locatários.
* O FortiGate Security Appliance 1Gbps fornece opções de VPN SSL e IPSec com acesso apenas de rede pública (sem acesso à rede privada do IBM Cloud).
* O Gateway de rede fornece recursos SSL, IPSec e OpenVPN na rede pública ou privada.
* Os produtos NetScaler podem fornecer VPN SSL e IPSec na rede pública ou privada.
* Os clientes também podem implementar uma solução de VPN em um servidor em seu ambiente do IBM Cloud.

## Quando eu seleciono a opção Alta disponibilidade, quais etapas que eu preciso tomar para aproveitar esse recurso?
{:faq}

Nenhuma. Quando solicitado em HA, o IBM Cloud provisiona automaticamente os dispositivos na configuração de HA.  No caso de o dispositivo primário falhar, um dispositivo passivo secundário assumirá como instância ativa primária e começará a passar o tráfego. Embora esse failover seja geralmente automático, a melhor prática é monitorar os servidores e assegurar que o tráfego esteja sendo passado com êxito.

## Quais produtos de firewall suportam NAT público para privado e/ou segmentação de VLAN privada?
{:faq}

Nenhum dos produtos do Hardware Firewall tem acesso à rede privada.  Um Gateway de rede é necessário para fornecer esses recursos sequenciais e os produtos NetScaler têm acesso às redes pública e privada.
