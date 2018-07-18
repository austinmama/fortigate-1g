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

# A propos

Un dispositif de sécurité FortiGate 1 Gbit/s (FSA) est un périphérique réseau à service exclusif dédié connecté en amont d'un serveur, qui protège un ou tous les serveurs sur un réseau local virtuel (VLAN) public. Il s'achète en plus d'un serveur et peut être ajouté à un VLAN à tout moment.  IBM Cloud déploie le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://www.fortinet.com/sites/default/files/productdatasheets/FortiGate-300C.pdf){: new_window} dans un domaine virtuel (VDOM) sur le dispositif dédié, octroyant ainsi aux utilisateurs l'accès complet à ce domaine virtuel sans compromettre l'intégrité de l'unité. 

Avec le dispositif FSA 1 Gbit/s, vous avez accès aux fonctions avancées et vous avez la possibilité d'adapter le périphérique à vos besoins à un degré nettement supérieur comparé à d'autres produits. Le pare-feu bloque ou oriente le trafic avant qu'il n'atteigne le serveur. Les principaux avantages sont les suivants : un serveur ne traite que le "bon" trafic et la bande passante peut être limitée pour les communications moins critiques. 

Les clients peuvent gérer le dispositif FSA soit via l'interface graphique Web FortiOS ou l'interface de ligne de commande (CLI) en utilisant SSH. Vous pouvez également commander l'option Haute disponibilité, qui fournit deux dispositifs en déploiement actif-passif avec des configurations synchronisées.

Comme la bande passante mensuelle du serveur est enregistrée au niveau du port de commutation du serveur, le trafic bloqué par le dispositif FSA 1 Gbit/s n'est pas comptabilisé dans vos allocations mensuelles, donc vous n'avez pas à payer le trafic non souhaité.

## Présentation et fonctions

**Usage prévu :** protection de VLAN public unique

**Interface utilisateur :** interface graphique FortiGate et interface de ligne de commande

**Fonctions :** filtrage dynamique de paquets (SPI), protection de VLAN, règles de pare-feu (trafic entrant), règles de pare-feu (trafic sortant), NAT, terminaison VPN SSL, terminaison VPN IPSec, journalisation avancée, haute disponibilité (facultatif)

**Débit :** 1 Gbit/s (2 Gbit/s en débit agrégé) 
