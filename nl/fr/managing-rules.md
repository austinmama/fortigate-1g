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

# Gestion des règles de pare-feu (politiques)
{: #managing-fortigate-firewall-rules-policies-}

FortiGate utilise le concept de "politique" (policy), qui englobe la possibilité d'accepter ou de refuser du trafic, appliquer des profils de sécurité, constituer et journaliser du trafic, ainsi que de planifier une période d'application de la politique. Pour constituer une politique, vous devez d'abord créer les objets qui en feront partie. 

1. Connectez-vous au dispositif à l'aide des données d'identification indiquées à la page **Détails de l'unité** dans le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window}. Suivez les instructions indiquant comment [gérer le dispositif de sécurité FortiGate (FSA)](/docs/infrastructure/fortigate-1g?topic=fortigate-1g-managing-the-fortigate-security-appliance-1gbps) pour obtenir les données d'identification.
2. Une fois connecté au dispositif, accédez au menu **Policy and Objects** et sélectionnez le protocole que vous souhaitez gérer (par exemple, IPv4 ou IPv6). Les politiques sont implémentées pour le trafic en fonction du numéro de séquence indiqué à l'extrême gauche. Les utilisateurs peuvent faire glisser une politique plus haut dans la liste pour l'implémenter plus tôt ou vice versa.
3. Pour ajouter une politique, cliquez sur **Create New** et référez-vous à la définition de ces zones :

    **Incoming Interface:** Il s'agit soit de l'interface accessible au public (interface externe) pour les règles de trafic entrant, soit de l'interface accessible pour le traitement (interface interne) pour les règles de trafic sortant.

    **Source Address:** Il s'agit d'une ou de plusieurs adresses IP source pour le trafic. L'adresse IP doit être ajoutée dans la liste "Addresses" dans le menu "Objects". Notez que l'option "All" est disponible.

    **Source User(s):** Applique la politique à un utilisateur ou un groupe créé dans le panneau "User and Device".

    **Source Device Type:** Applique la politique à une unité créée dans le panneau "User and Device".

    **Destination Address:** Il s'agit d'adresse(s) IP cible du trafic. L'adresse IP doit être ajoutée dans la liste "Addresses" dans le menu "Objects". Notez que l'option "All" est disponible.

    **Schedule:** détermine le moment d'exécution d'une politique. L'option "Always" est disponible. Vous pouvez également créer une planification dans le menu "Objects" sous "Schedules".

    **Service:** Détermine le service auquel s'appliquera la politique. Une option "ALL" est également disponible ainsi que de nombreux services standard. D'autres services peuvent être ajoutés dans le menu "Services" sous "Objects".

    **Action:** Permet d'accepter ou de refuser du trafic. 

    **Firewall / Network Options:** Active ou désactive la conversion NAT et les options associées.

    **Security Profiles:** Fournit une option d'activation/désactivation pour chaque option et autorise également l'association au profil.

    **Traffic Shaping:** Cette option vous permet de configurer la bande passante maximale et garantie (minimum) disponible pour le trafic. Un nombre maximal de connexions peut également être défini sur un modélisateur par adresse IP. 

    Les paramètres DSCP ne sont pas en vigueur car les informations de qualité de service (QoS) générées sont ignorées par la plateforme IBM© Cloud.

    **Logging Options:** Configure le moment d'enregistrement du trafic autorisé. Ce paramètre (et notamment l'option "Capture Packets") utilise les ressources de l'unité.

    **Comments:** Commentaires générés par l'utilisateur

    **Enable this policy:** Active ou désactive la politique

## Exemple de règle "Allow All" autorisant tout le trafic Web sur un serveur Web

***Incoming Interface:*** *outside VLAN*

***Source Address:*** *All*

***Source User(s):** *Blank*

***Source Device Type:*** *Blank*

***Outgoing Interface:*** *inside VLAN*

***Destination Address:*** *x.x.x.x (adresse IP du serveur Web)*

***Schedule:*** *always*

***Service:*** *HTTP*

***Action:*** *ACCEPT*

***NAT:*** *OFF*

***Security Profiles:*** *Use Standard*

***Traffic Shaping:*** *Off*

***Log Allowed Traffic:*** *On (Security Events)*

***Comments:*** *Trafic du serveur Web x.x.x.x*

***Enable this policy:*** *On*
