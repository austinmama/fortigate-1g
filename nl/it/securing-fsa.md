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

# Proteggi il FortiGate Security Appliance

Puoi configurare il FortiGate Security Appliance (FSA) 1Gbps per soddisfare i requisiti di conformità e sicurezza. IBM Cloud fornisce un account amministratore VDOM con una password assegnata casualmente. I clienti possono ruotare tale password, creare utenti di sola lettura e limitare l'accesso in base agli "host attendibili", che accettano il traffico solo da IP di origine specificati (fino a tre). Per completare queste attività:

1. Accedi all'applicazione utilizzando le credenziali trovate nella pagina **Device Details** in [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window}. Segui le istruzioni su come [gestire il FortiGate Security Appliance](managing-fsa.html) per trovare le credenziali.
2. Dopo aver eseguito l'accesso all'applicazione, passa a **System > Admin > Administrators**. Vengono registrati tutti gli accessi e le modifiche.
3. Per configurare interfacce individuali, passa a **System > Network > Interfaces**.

    Puoi limitare l'accesso alle interfacce di gestione ai soli protocolli necessari (normalmente HTTPS e SSH, poiché questo fornisce la crittografia in-transit) o per maggiore sicurezza, puoi disabilitare l'accesso esterno all'interfaccia di gestione. Questo può essere realizzato abilitando i protocolli appropriati nell'interfaccia "interna" (l'interfaccia su cui risiede la VLAN pubblica del cliente) e disabilitando tutti i protocolli nell'interfaccia "esterna" (l'interfaccia da cui viene ricevuto il traffico internet pubblico). Questa ulteriore misura di sicurezza richiede che l'utente abbia un server posizionato nella VLAN da cui gestire il FSA. 
