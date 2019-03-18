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

# Gestione delle regole del firewall Fortigate (politiche)
{: #managing-fortigate-firewall-rules-policies-}

FortiGate utilizza il concetto di "politica", che include la possibilità di accettare/rifiutare il traffico, applicare i profili di sicurezza, modellare il traffico, registrare il traffico e pianificare un intervallo di tempo per una politica da applicare. Per assemblare una politica, devi prima creare gli oggetti che ne faranno parte. 

1. Accedi all'applicazione utilizzando le credenziali trovate nella pagina **Device Details** in [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window}. Segui le istruzioni su come [gestire il FortiGate Security Appliance](/docs/infrastructure/fortigate-1g?topic=fortigate-1g-managing-the-fortigate-security-appliance-1gbps) per trovare le credenziali.
2. Dopo aver eseguito l'accesso all'applicazione, passa al menu **Policy and Objects** e seleziona il protocollo che desideri gestire (come ad esempio IPv4 o IPv6). Le politiche sono implementate nel traffico in base al numero di sequenza all'estrema sinistra. Gli utenti possono trascinare una politica in una posizione superiore nell'elenco per implementarla prima o viceversa.
3. Per aggiungere una politica, fai clic su **Create New** e fai riferimento a queste definizioni di campo:

    **Interfaccia in entrata:** l'interfaccia verso il pubblico (interfaccia esterna) per le regole ingress o l'interfaccia verso il calcolo (interfaccia interna) per le regole egress.

    **Indirizzo di origine:** questi sono gli IP di origine per il traffico. L'IP deve essere aggiunto all'elenco "Addresses" in "Objects Menu." Nota che l'opzione "All" è disponibile.

    **Utenti di origine:** applica la politica a un utente o un gruppo creato nel pannello "User and Device".

    **Tipo di dispositivo di origine:** applica la politica a un dispositivo creato nel pannello "User and Device".

    **Indirizzo di destinazione:** questi sono gli IP di destinazione del traffico. L'IP deve essere aggiunto all'elenco "Addresses" in "Objects Menu." Nota che l'opzione "All" è disponibile.

    **Pianificazione:** determina quando sarà eseguita la politica. È disponibile un'opzione "Always". Puoi anche creare una pianificazione nel menu Objects in Schedules.

    **Servizio:** determina il servizio a cui sarà applicata la politica. È disponibile un'opzione "ALL" nonché numerosi servizi standard. Possono essere aggiunti ulteriori servizi nel menu Services in Objects.

    **Azione:** accetta o rifiuta il traffico. 

    **Opzioni Firewall / Rete:** abilita o disabilita NAT e le rispettive opzioni associate.

    **Profili di sicurezza:** fornisce un'attivazione On/Off per ogni opzione, così come consente l'associazione del profilo.

    **Modellamento del traffico:** ti consente di configurare la larghezza di banda massima e garantita (minima) disponibile per il traffico. Può inoltre essere impostato un limite di connessioni massimo in uno shaper per IP. 

    Le impostazioni DSCP non diventano effettive poiché le informazioni QoS generate dall'utente vengono ignorate dalla piattaforma IBM© Cloud.

    **Opzioni di registrazione:** configura quando il traffico "Allowed" viene registrato. Questa impostazione (e specialmente l'opzione "Capture Packets") utilizza le risorse del dispositivo.

    **Commenti:** i commenti generati dall'utente

    **Abilita questa politica:** abilita o disabilita la politica

## Esempio di una regola "Allow All" semplice per il traffico web a un server web.

***Interfaccia in entrata:*** *outside VLAN*

***Indirizzo di origine:*** *All*

***Utenti di origine:** *Blank*

***Tipo di dispositivo di origine:*** *Blank*

***Interfaccia in uscita:*** *inside VLAN*

***Indirizzo di destinazione:*** *x.x.x.x (Web Server IP)*

***Pianificazione:*** *always*

***Servizio:*** *HTTP*

***Azione:*** *ACCEPT*

***NAT:*** *OFF*

***Politiche di sicurezza:*** *Use Standard*

***Modellamento del traffico:*** *Off*

***Registrazione traffico consentito:*** *On (Security Events)*

***Commenti:*** *Web Server Traffic x.x.x.x*

***Abilita questa politica:*** *On*
