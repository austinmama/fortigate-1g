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

# Déploiement par défaut

Le dispositif de sécurité FortiGate (FSA) 1 Gbit/s est déployé en tant que domaine virtuel (en principe firewall001) sur un dispositif dédié. Le client dispose de l'accès complet aux ressources du dispositif (processeurs, mémoire, etc.), mais l'accès à la configuration de l'unité est limité pour garantir qu'IBM puisse assurer la prise en charge effective de l'unité.

FSA est déployé en mode NAT et réside dans deux VLAN/réseaux au sein de l'infrastructure de réseau public. Le VLAN externe (outside) est le réseau local virtuel public d'IBM Cloud, par lequel le trafic pénètre dans le centre de données et est acheminé vers le dispositif FSA. Le VLAN interne (inside) est le VLAN FCR (Frontend Customer Router) public protégé, affecté par le client, dans lequel résident les ressources de serveur du client.  

IBM Cloud déploie FSA avec deux interfaces 1G liées sur chacun de ces deux réseaux lors du processus de mise à disposition. IBM Cloud déploie également une interface unique pour la mise à disposition et la maintenance de l'unité, qui n'est pas accessible aux clients.

Le pare-feu est déployé avec tout le trafic IPv4 et IPv6 autorisé, avec une règle spécifique (softlayer-admin) conçue pour autoriser le réseau d'administration interne d'IBM Cloud à accéder aux unités via le pare-feu. Les protections contre les attaques de déni de service (DoS) et la plupart des autres filtres sont configurés pour ne pas s'appliquer.
