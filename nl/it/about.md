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

# Informazioni

Un Fortigate Security Appliance 1Gbps (FSA) è un dispositivo di rete a singolo tenant dedicato collegato in upstream da un server che protegge alcuni o tutti i server in una VLAN pubblica. Viene acquistato separatamente da un server e può essere aggiunto a una VLAN in qualsiasi momento.  IBM Cloud distribuisce [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://www.fortinet.com/sites/default/files/productdatasheets/FortiGate-300C.pdf){: new_window} all'interno di un Virtual Domain (VDOM) in un'applicazione dedicata, consentendo ai clienti l'accesso completo a tale dominio virtuale senza compromettere l'integrità del dispositivo. 

Con il FSA 1Gbps, i clienti hanno accesso a funzioni avanzate e alla capacità di ottimizzare il dispositivo ad un grado più elevato rispetto agli altri prodotti. Il firewall blocca o modella il traffico prima che raggiunga il server. I vantaggi principali sono che un server deve gestire solo il traffico 'buono' e che la larghezza di banda può essere vincolata a minori comunicazioni critiche. 

I clienti possono gestire il FSA tramite la GUI FortiOS basata sul web o la CLI (Command Line Interface) utilizzando SSH. Può inoltre essere ordinata l'elevata disponibilità, che fornisce due applicazioni nella distribuzione attiva-passiva con le configurazioni sincronizzate.

Poiché la larghezza di banda del server viene registrata mensilmente nella porta di switch del server, il traffico bloccato dal FSA 1Gbps non viene contato nelle assegnazioni mensili, eliminando la necessità di pagare per il traffico non desiderato.

## Panoramica e funzioni

**Utilizzo previsto:** protezione singola VLAN pubblica

**Interfaccia utente:** GUI Fortigate e CLI (Command Line Interface)

**Funzioni:** Filtraggio stateful dei pacchetti, Protezione VLAN, Regole firewall Ingress, Regole firewall Egress, NAT, Terminazione VPN SSL, Terminazione VPN IPSec, Registrazione avanzata, Elevata disponibilità (facoltativa)

**Velocità effettiva:** 2000Mbps
