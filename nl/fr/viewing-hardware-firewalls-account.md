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

# Affichage de vos pare-feux FortiGate
{: #viewing-your-fortigate-firewalls}

Pour voir quels sont les réseaux locaux virtuels protégés par des pare-feux et pour rechercher d'autres caractéristiques sur les pare-feux individuels, accédez à la page VLAN.

1. Depuis votre navigateur, ouvrez le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} et connectez-vous à votre compte.
2. Dans la navigation du portail client, sélectionnez **Réseau > Gestion IP > VLAN**.

Chaque ligne du tableau représente un réseau local virtuel (VLAN) dans votre infrastructure. IBM© Cloud renseigne automatiquement les informations "Numéro de VLAN" et "Routeur principal" en indiquant le vrai numéro de réseau local virtuel et le routeur sur lequel il est configuré. La zone "Nom" peut être utilisée pour attribuer un nom reconnaissable au réseau local virtuel (par exemple, DMZ, Intranet, Public ou Base de données).

La colonne à l'extrême droite **Passerelle/pare-feu** contient les détails de la protection par pare-feu en vigueur, par exemple :

- **Ajouter pare-feu** indique qu'il n'y a aucun pare-feu en vigueur pour les serveurs de ce réseau local virtuel.
- **Serveurs protégés individuellement** indique qu'un ou plusieurs serveurs utilisent un pare-feu matériel (partagé) et qu'il n'y a aucun pare-feu matériel (dédié), aucun dispositif de sécurité FortiGate, ni passerelle réseau en vigueur. Les pare-feux VLAN et les passerelles réseau ne peuvent pas être appliqués sur un VLAN comprenant des serveurs protégés individuellement.
- **Firewall-vlanXXXX.networklayer.com** indique qu'il y a un pare-feu matériel (dédié) ou un dispositif de sécurité FortiGate en vigueur. Il ne peut y avoir qu'un seul pare-feu VLAN ou une passerelle réseau associé à un VLAN, mais un serveur peut être protégé sur le VLAN public par un pare-feu VLAN et associé au réseau privé avec une passerelle réseau.
- **Nom de la passerelle** indique le VLAN associé à cette passerelle réseau.

## Détails des serveurs protégés individuellement

Pour les VLAN ayant des **serveurs protégés individuellement** dans la zone **Passerelle/pare-feu**, vous pouvez cliquer sur le lien du numéro VLAN pour afficher les détails du réseau local virtuel, y compris les unités associées.

Dans la liste des unités associées, vous pouvez cliquer sur chaque unité et faire défiler l'écran jusqu'au bas de l'onglet Configuration. Vous verrez **Pare-feu** indiqué dans la zone Modules complémentaires avec le statut **Installé** ou **Non Installé**.

- **Non installé** indique qu'aucun pare-feu n'est appliqué pour cette unité.
- **Installé** indique qu'un pare-feu est appliqué et qu'il y aura un onglet **Pare-feu** sur l'unité dans lequel vous pouvez gérer la configuration de pare-feu.

## Détails du pare-feu dédié

Pour les réseaux locaux virtuels ayant **Firewall-vlanXXXX.networklayer.com** dans la zone **Passerelle/pare-feu**, vous pouvez cliquer sur le lien de ce pare-feu pour en afficher les détails. Les détails de l'unité comprennent le routeur associé, le réseau local virtuel (VLAN), les sous-réseaux IPv4/IPv6, les unités associées à ce VLAN et les commandes permettant de router le trafic via ou hors du pare-feu.

Les dispositifs de sécurité FortiGate (FSA) ont une adresse IP de gestion, un nom d'utilisateur et un mot de passe.  La gestion des dispositifs FSA s'effectue via leur propre interface graphique ou leur console SSH.

## Détails de la passerelle réseau

Pour les réseaux locaux virtuels disposant d'un nom d'unité de passerelle réseau dans la zone **Passerelle/pare-feu**, vous pouvez cliquer sur le nom de la passerelle réseau pour afficher les détails de cette passerelle. Les détails de l'unité comprennent les options de gestion des VLAN front-end (FCR) et back-end (BCR), ainsi que celles de la passerelle réseau.
