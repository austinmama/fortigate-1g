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

# Configurazione di una regola del firewall FortiGate per consentire solo a una sottorete di IP specifica di accedere ai tuoi server web

Puoi configurare una regola del firewall FortiGate per consentire l'accesso solo al tuo server protetto da una sottorete o un IP specifici.

1. Accedi al dispositivo FortiGate. I dettagli e il link di accesso possono essere trovati nella schermata Device Details nella sezione etichettata ‘Management’​.
* Passa a **Policy > Policy** e fai clic su **Create New**.
* Per creare una regola che consentirà solo il traffico ai tuoi server da un IP specifico, immetti le seguenti configurazioni:
    * Interfaccia/zona di origine = v###-outside
    * Indirizzo di origine = L'indirizzo IP o la sottorete degli IP che desideri consentire. L'indirizzo può essere immesso in due formati differenti: 10.10.20.[1-14] o 10.10.20.1/255.255.255.240.
    * Interfaccia/zona di destinazione  = v###-inside
    * Indirizzo di destinazione = l'IP o gli IP specifici del server a cui desideri fornire l'accesso, se vuoi fornirlo ad ognuno dei tuoi server web puoi selezionare ‘all’.
    * Servizio = Il tipo di servizio come HTTP, SSH, SMB, DHCP da consentire.  Se non è presente un servizio specifico puoi selezionare ‘ANY’ per consentire tutti i servizi per questa regola.
    * Azione = ACCEPT
    * Fai clic su OK per salvare la regola
    * Verifica la tua regola utilizzando il comando ping e un indirizzo IP dei server per confermare se puoi accedere al server da un indirizzo consentito o negato.
        * Un indirizzo consentito riceverà una risposta e uno negato dovrebbe ricevere un messaggio ‘Request timed out.’.
        * Se la politica non viene applicata alla regola come previsto potresti dover modificare la sequenza delle tue regole poiché la sequenza delle regole della politica viene applicata dall'alto in basso.
