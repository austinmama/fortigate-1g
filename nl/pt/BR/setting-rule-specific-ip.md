---

copyright:
  years: 2017
lastupdated: "2017-10-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Configurando uma regra de firewall do FortiGate para permitir que somente uma sub-rede IP específica acesse seus servidores da web

É possível configurar uma regra de firewall do FortiGate para somente permitir acesso ao servidor da web protegido de uma sub-rede ou IP específico.

1. Efetue login no dispositivo FortiGate. O link de login e os detalhes podem ser
localizados na tela Detalhes do dispositivo sob a seção rotulada 'Gerenciamento'.
* Navega para **Política > Política** e clique em **Criar novo**.
* Para criar uma regra que só permitirá tráfego para seus servidores de um IP específico, insira as configurações a seguir:
    * Interface/zona de origem = v###-outside
    * Endereço de origem = o Endereço IP e Sub-rede dos IPs que você deseja permitir. O endereço pode ser inserido em dois formatos diferentes: 10.10.20.[1-14] ou 10.10.20.1/255.255.255.240.
    * Interface/zona de destino = v###-inside
    * Endereço de destino = o IP específico/os IPs do servidor aos quais você deseja
dar acesso; caso queira dar acesso a qualquer um de seus servidores da web, você pode
selecionar 'todos'.
    * Serviço = o tipo de Serviço, como HTTP, SSH, SMB, DHCP, a ser permitido. Se não houver serviço específico, você poderá selecionar 'ANY' para permitir todos os serviços por essa regra.
    * Ação = ACCEPT
    * Clique em OK para salvar a regra
    * Teste sua regra usando o comando ping e um endereço IP de servidores para confirmar se você pode acessar o servidor de um Endereço permitido e de um Endereço negado.
        * Um Endereço permitido receberá uma resposta e um Endereço negado deverá receber uma mensagem 'Solicitação atingiu o tempo limite'.
        * Se a política não estiver aplicando a regra conforme esperado, você poderá precisar ajustar a Sequência de suas regras, já que a Sequência das regras de política é aplicada de cima para baixo.
