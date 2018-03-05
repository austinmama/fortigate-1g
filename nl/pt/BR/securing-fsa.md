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

# Proteger o FortiGate Security Appliance

É possível configurar o FortiGate Security Appliance (FSA) 1Gbps para atender aos requisitos de segurança e conformidade. O IBM Cloud fornece uma conta do administrador de VDOM com uma senha designada aleatoriamente. Os clientes podem girar essa senha, criar usuários somente leitura e restringir o acesso com base em "Hosts confiáveis", que aceita tráfego apenas de IPs de origem especificados (até três). Para concluir essas atividades:

1. Efetue login no dispositivo usando as credenciais encontradas na página **Detalhes do dispositivo** no [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window}. Siga as instruções de como [Gerenciar o FortiGate Security Appliance](managing-fsa.html) para localizar as credenciais.
2. Depois de efetuar login no dispositivo, navegue para **Sistema > Administrador > Administradores**. Todo o acesso e mudanças são registrados.
3. Para configurar interfaces individuais, navegue para **Sistema > Rede > Interfaces**.

    Você pode restringir o acesso às interfaces administrativas para apenas os protocolos que requerem (geralmente HTTPS e SSH, já que isso fornece criptografia em trânsito) ou, para segurança adicional, você pode desativar o acesso externo à interface administrativa. Isso é realizado ativando os protocolos apropriados na interface "interna" (a interface na qual reside a VLAN pública de um cliente) e desativando todos os protocolos na interface "externa" (a interface da qual o tráfego de Internet pública é recebido). Essa medida de segurança adicional requer que o usuário tenha um servidor posicionado dentro da VLAN da qual administrar o FSA. 
