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

# Limitazioni note di Fortigate Security Appliance 1Gbps
{: #known-limitations-of-fortigate-security-appliance-1gbps}

Il FortiGate Security Appliance (FSA) 1Gbps ha le seguenti limitazioni note:

* Non è compatibile con Windows Network Load Balancing (NLB) a causa del modo in cui viene elaborato ARP.

* La funzionalità di failover dell'elevata disponibilità non viene esposta all'utente. Se il firewall master ha un malfunzionamento, ma non un failover automatico, sarà necessario un ticket di supporto. Viene consigliato il monitoraggio del dispositivo per i servizi critici per garantire che i firewall stiano passando il traffico in modo appropriato.

* Un FortiGate Security Appliance non può essere distribuito a una VLAN al momento associata a un gateway di rete, un Hardware Firewall o a un altro FortiGate Security Appliance.

* Il FortiGate Security Appliance viene associato a una sola VLAN del cliente pubblica (la VLAN "interna") e non può accedere alla rete privata.
