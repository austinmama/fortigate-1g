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

# Sécurisation du dispositif de sécurité Fortigate 1 Gbit/s
{: #securing-the-fortigate-security-appliance-1-gbps}

Vous pouvez configurer le dispositif de sécurité FortiGate (FSA) 1 Gbit/s pour répondre aux exigences en matière de sécurité et de conformité. IBM© Cloud fournit un compte d'administrateur de domaine virtuel (VDOM) avec un mot de passe affecté de manière aléatoire. Les utilisateurs peuvent changer ce mot de passe, créer des utilisateurs avec des droits en lecture seule et restreindre l'accès en fonction des "Hôtes sécurisés", qui acceptent le trafic en provenance de certaines adresses IP source uniquement (3 maximum). Pour exécuter ces activités :

1. Connectez-vous au dispositif à l'aide des données d'identification indiquées à la page **Détails de l'unité** dans le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window}. Suivez les instructions indiquant comment [gérer le dispositif de sécurité FortiGate (FSA)](/docs/infrastructure/fortigate-1g?topic=fortigate-1g-managing-the-fortigate-security-appliance-1gbps) pour obtenir les données d'identification.
2. Une fois connecté au dispositif, accédez à **System > Admin > Administrators**. Tous les accès et modifications sont consignés.
3. Pour configurer des interfaces individuelles, accédez à **System > Network > Interfaces**.

    Vous pouvez restreindre l'accès aux interfaces d'administration aux protocoles qu'elles nécessitent (en principe HTTPS et SSH offrant un chiffrement des données en transit) ou, pour renforcer la sécurité, vous pouvez désactiver tout accès externe à l'interface d'administration. Pour cela, il suffit d'activer les protocoles appropriés dans l'interface "interne" (interface sur laquelle réside le réseau local virtuel (VLAN) public d'un client) et de désactiver tous les protocoles sur l'interface "externe" (interface de réception du trafic Internet public). Cette mesure de sécurité supplémentaire nécessite que le serveur de l'utilisateur soit positionné à l'intérieur du réseau local virtuel à partir duquel administrer le dispositif FSA. 
