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

# Efetuar bypass das regras de firewall

Para efetuar bypass das regras de firewall, execute o procedimento a seguir:

1. Em seu navegador, abra [Portal do Cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} e efetue login em sua conta.
2. Na navegação do Portal do cliente, acesse **Rede > Gerenciamento de IP > VLANs** e clique no dispositivo de firewall cujo bypass você deseja efetuar.
3. Na página **Detalhes do dispositivo**, na guia **Configuração**, você pode usar o menu suspenso **Ações** para escolher **Configurar bypass de rota** ou, na seção **Status:**, você pode clicar no botão **Efetuar bypass de regras**. 

	Outra opção é rotear ao redor do firewall, o que você pode fazer clicando no botão **Rotear ao redor**. De qualquer maneira, é necessário receber um diálogo de confirmação. Clique em **Sim** para confirmar a ação. O bypass das regras leva aproximadamente dois minutos para entrar em vigor. Enquanto estiver no modo bypass, o "Status" será "Roteando AO REDOR do firewall".

## Ativar as regras novamente

Para ativar as regras novamente, siga as instruções acima para acessar a guia **Configuração** do dispositivo e clique no menu suspenso **Ações** e escolha **Configurar bypass de rota**. Você receberá um diálogo de confirmação. Clique em **Sim** para confirmar a ação. O "Status" mudará para "Roteando ATRAVÉS do firewall" em dois minutos.
