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

# Efetuando bypass das regras de firewall
{: #bypassing-the-firewall-rules}

Para efetuar bypass das regras de firewall, execute o procedimento a seguir:

1. Em seu navegador, abra [Portal do Cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} e efetue login em sua conta.
2. Na navegação do Portal do cliente, acesse **Rede > Gerenciamento de IP > VLANs** e clique no dispositivo de firewall cujo bypass você deseja efetuar.
3. Na página **Detalhes do dispositivo**, é possível usar o menu suspenso **Ações** para escolher **Configurar bypass de regra** ou, na seção **Status:**, é possível clicar no botão **Efetuar bypass de regras**. O bypass das regras leva aproximadamente dois minutos para entrar em vigor. O Status deve mudar para "Efetuando bypass de todas as regras".

	Outra opção é rotear em torno do firewall. É possível usar o menu suspenso **Ações** para escolher **Configurar bypass da rota** ou, na seção **Status:**, é possível clicar no botão **Rotear em torno**. De qualquer maneira, é necessário receber um diálogo de confirmação. Clique em **Sim** para confirmar a ação. O bypass da rota leva aproximadamente dois minutos para entrar em vigor. Enquanto estiver no modo bypass, o "Status" será "Roteando AO REDOR do firewall".

## Ativar as regras novamente

Para ativar as regras novamente, siga as instruções acima para acessar a guia **Configuração** do dispositivo e clique no menu suspenso **Ações** e escolha **Configurar bypass de rota**. Você receberá um diálogo de confirmação. Clique em **Sim** para confirmar a ação. O "Status" mudará para "Roteando ATRAVÉS do firewall" em dois minutos.
