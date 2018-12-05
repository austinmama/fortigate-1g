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

# Gerenciar regras de firewall (políticas)

O FortiGate utiliza o conceito de "política", que inclui a capacidade de aceitar/negar tráfego, aplicar perfis de segurança, formar tráfego, registrar tráfego e planejar um intervalo de tempo para a aplicação de uma política. Para montar uma política, deve-se primeiro criar os objetos que farão parte dela. 

1. Efetue login no dispositivo usando as credenciais encontradas na página **Detalhes do dispositivo** no [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window}. Siga as instruções de como [Gerenciar o FortiGate Security Appliance](managing-fsa.html) para localizar as credenciais.
2. Depois de efetuar login no dispositivo, navegue para o menu **Política e objetos** e selecione o protocolo que deseja gerenciar (como IPv4 ou IPv6). As políticas são implementadas com relação ao tráfego baseado no número de sequência na extrema esquerda. Os usuários podem arrastar uma política mais alta na lista para ser implementada antes ou vice-versa.
3. Para incluir uma política, clique em **Criar novo** e consulte estas definições de campo:

    **Interface recebida:** a interface voltada ao público (interface externa) para regras de ingresso ou a interface voltada a cálculo (interface interna) para regras de egresso.

    **Endereço de origem:** esse é o IP ou os IPs de origem para o tráfego. O IP deve ser incluído na lista "Endereços" no "menu Objetos". Observe que uma opção "Todos" está disponível.

    **Usuários(s) de origem:** isso aplica a política a um usuário ou grupo criado no painel "Usuário e dispositivo".

    **Tipo de dispositivo de origem:** isso aplica a política a um dispositivo criado no painel "Usuário e dispositivo".

    **Endereço de destino:** esse é o IP ou os IPs de destino do tráfego. O IP deve ser incluído na lista "Endereços" no "menu Objetos". Observe que uma opção "Todos" está disponível.

    **Planejamento:** isso determina quando a política será executada. Uma opção "Sempre" está disponível. Você também pode criar um planejamento no menu Objetos sob Planejamentos.

    **Serviço:** isso determina o serviço ao qual a política será aplicada. Uma opção "TODOS" está disponível, além de inúmeros serviços padrão. Serviços adicionais podem ser incluídos no menu Serviços sob Objetos.

    **Ação:** aceita ou nega o tráfego. 

    **Opções de firewall/rede:** ativa ou desativa NAT e suas opções associadas.

    **Perfis de segurança:** fornece uma alternância de Ligado/Desligado para cada opção, bem como permite associação ao perfil.

    **Forma de tráfego:** isso permite configurar a largura de banda máxima e garantida (mínima) disponível ao tráfego. Um limite máximo de conexões também pode ser configurado em um shaper por IP. 

    Configurações de DSCP não são eficazes, visto que o usuário que gerou as informações de QoS é ignorado pela plataforma IBM Cloud.

    **Opções de criação de log:** configura quando tráfego "Permitido" é registrado. Essa configuração (e especialmente a opção "Capturar Pacotes") utiliza recursos do dispositivo.

    **Comentários:** gerados pelo usuário

    **Ativar esta política:** ativa ou desativa a política

## Exemplo de uma regra simples "Permitir todos" de tráfego da web para um servidor da web

***Interface recebida:*** *VLAN externa*

***Endereço de origem:*** *todos*

***Usuário(s) de origem:** *em branco*

***Tipo de dispositivo de origem:*** *em branco*

***Interface de saída:*** *VLAN interna*

***Endereço de destino:*** *x.x.x.x (IP do servidor da web)*

***Planejamento:*** *sempre*

***Serviço:*** *HTTP*

***Ação:*** *ACEITAR*

***NAT:*** *DESATIVADO*

***Perfis de segurança:*** *usar padrão*

***Forma de tráfego:*** *desativado*

***Registrar tráfego permitido:*** *ativado (eventos de segurança)*

***Comentários:*** *tráfego do servidor da web x.x.x.x*

***Ativar esta política:*** *ativado*
