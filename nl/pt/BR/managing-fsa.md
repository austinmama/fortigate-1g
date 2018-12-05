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

# Gerenciar o FortiGate Security Appliance

Quando o firewall é incluído primeiro na VLAN, todo o tráfego é permitido. Você
precisa incluir regras no firewall para controlar o tráfego. 

1. Em seu navegador, abra [Portal do Cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} e efetue login em sua conta.
2. Na navegação do Portal do cliente, selecione **Rede > Gerenciamento de
IP > VLANs**. 

	**Dica:** para visualizar somente VLANs públicas, clique no menu
suspenso **Filtrar** e insira ``fcr`` no **Roteador primário**.
3. Role para a VLAN que você deseja gerenciar e clique no link do nome do firewall
na coluna **GATEWAY/FIREWALL** para acessar a página
**Detalhes do dispositivo**.
4. Na página **Detalhes do dispositivo**, você pode visualizar
as sub-redes associadas, o "Status" atual do roteamento do firewall e as informações de
gerenciamento. 

	As informações de gerenciamento incluem um **IP de gerenciamento**, um
**Nome de usuário** e uma **Senha**. Esse IP de
gerenciamento é publicamente acessível por padrão. Para propósitos de automação ou casos
de uso avançados, a administração também está disponível usando SSH com o mesmo IP e
credenciais.
5. Para acessar a GUI, clique no link IP de gerenciamento e insira o nome do usuário e a senha fornecidos. 
6. Na IU de gerenciamento, é possível gerenciar o FortiGate Security Appliance
como Administrador de VDOM. Para funções de gerenciamento não disponíveis usando a IU de
gerenciamento, como gerenciar SSL Certificates, iniciar um failover de HA manual,
reinicializar, fazer upgrade ou executar uma restauração de configuração padrão, um
chamado de suporte precisa ser aberto.

O Fortinet mantém uma [documentação on-line que inclui um cookbook interativo ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://cookbook.fortinet.com/fortigate/){: new_window} que pode ser usada para referência durante a configuração.
