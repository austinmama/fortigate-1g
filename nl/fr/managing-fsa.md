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

# Gestion du dispositif de sécurité FortiGate

La première fois qu'un pare-feu est ajouté au réseau local virtuel (VLAN), tout le trafic est autorisé. Vous devez ajouter des règles au pare-feu pour contrôler le trafic. 

1. Depuis votre navigateur, ouvrez le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} et connectez-vous à votre compte.
2. Dans la navigation du portail client, sélectionnez **Réseau > Gestion IP > VLAN**. 

	**Astuce :** pour afficher uniquement les VLAN publics, cliquez sur le menu déroulant **Filtre** et entrez ``fcr`` dans la zone **Routeur principal**.
3. Faites défiler l'écran jusqu'au VLAN que vous souhaitez gérer et cliquez sur le lien correspondant au nom du pare-feu dans la colonne **PASSERELLE/PARE-FEU** pour accéder à la page **Détails de l'unité**.
4. Sur la page **Détails de l'unité**, vous pouvez afficher les sous-réseaux associés, le "Statut" en cours des options de routage du pare-feu et les informations de gestion. 

	Les informations de gestion comprennent les éléments suivants : **IP de gestion**, **Nom d'utilisateur** et **Mot de passe**. L'adresse IP de gestion est accessible au public par défaut. A des fins d'automatisation ou pour les cas d'utilisation avancés, l'administration est également accessible en utilisant SSH avec la même adresse IP et les mêmes données d'identification.
5. Pour accéder à l'interface graphique, cliquez sur le lien IP de gestion et entrez le nom d'utilisateur et le mot de passe fournis. 
6. Dans l'interface utilisateur de gestion, vous pouvez gérer le dispositif de sécurité FortiGate (FSA) en tant qu'administrateur de domaine virtuel (VDOM). Pour les fonctions de gestion indisponibles à l'aide de l'interface utilisateur de gestion, par exemple la gestion des certificats SSL, le lancement manuel d'un basculement en mode haute disponibilité, un redémarrage, une mise à niveau ou la restauration d'une configuration par défaut, vous devez ouvrir un ticket de demande de service.

Fortinet offre [une documentation en ligne, notamment un manuel d'instructions "The FortiGate Cookbook" ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://cookbook.fortinet.com/fortigate/){: new_window} pouvant servir de référence lors de la configuration.
