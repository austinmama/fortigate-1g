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

# Configuration d'une règle de pare-feu FortiGate pour n'autoriser qu'un sous-réseau IP particulier à accéder à vos serveurs Web

Vous pouvez configurer une règle de pare-feu FortiGate consistant à n'autoriser l'accès à votre serveur Web protégé qu'à un sous-réseau ou une adresse IP spécifique.

1. Connectez-vous à l'unité FortiGate. Vous pourrez obtenir le lien et les détails de connexion sur l'écran Détails de l'unité à la section intitulée "Gestion".
* Accédez à **Policy > Policy** et cliquez sur **Create New**.
* Pour créer une règle qui n'autorisera le trafic vers vos serveurs qu'à partir d'une adresse IP spécifique, entrez les configurations suivantes :
    * Source Interface/Zone = v###-outside
    * Source Address = Adresse IP et sous-réseau de l'adresse IP que vous souhaitez autoriser. L'adresse peut être saisie avec deux formats différents : 10.10.20.[1-14] ou 10.10.20.1/255.255.255.240.
    * Destination Interface/Zone  = v###-inside
    * Destination Address = Adresse IP spécifique / adresse IP du serveur dont vous souhaitez octroyer l'accès, si vous envisagez d'octroyer l'accès à l'un de vos serveurs Web, vous pouvez sélectionner "all".
    * Service = Type de service à autoriser, par exemple HTTP, SSH, SMB, DHCP.  S'il n'y a aucun service spécifique, vous pouvez sélectionner "ANY" pour autoriser tous les services selon cette règle.
    * Action = ACCEPT
    * Cliquez sur OK pour enregistrer la règle
    * Testez la règle à l'aide de la commande ping et d'une adresse IP de serveur pour confirmer si vous pouvez accéder au serveur à partir d'une adresse autorisée et à partir d'une adresse refusée.
        * Une adresse autorisée recevra une réponse et une adresse refusée est censée obtenir le message "Demande arrivée à expiration".
        * Si la politique n'applique pas la règle comme prévu, il vous faudra peut-être modifier la séquence de vos règles car dans une séquence de règles d'une politique, les règles sont appliquées du haut vers le bas.
