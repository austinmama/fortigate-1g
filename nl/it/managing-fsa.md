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

# Gestione di FortiGate Security Appliance 1Gbps
{: #managing-the-fortigate-security-appliance-1gbps}

Quando il firewall viene aggiunto per la prima volta alla VLAN, viene consentito tutto il traffico. Devi aggiungere le regole al firewall per controllare il traffico. 

1. Dal tuo browser, apri [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} e accedi al tuo account.
2. Nella navigazione del portale del cliente, seleziona **Network > IP Management > VLANs**. 

	**Suggerimento:** per visualizzare solo le VLAN pubbliche, fai clic sul menu a discesa **Filter** e immetti ``fcr`` nel campo **Primary Router**.
3. Scorri fino alla VLAN che vuoi gestire e fai clic sul link del nome del firewall nella colonna **GATEWAY/FIREWALL** per passare alla pagina **Device Details**.
4. Nella pagina **Device Details**, puoi visualizzare le sottoreti associate, lo "Status" corrente dell'instradamento del firewall e le informazioni di gestione. 

	Le informazioni di gestione includono **Management IP**, **Username** e **Password**. Questo Management IP è accessibile pubblicamente per impostazione predefinita. Per scopi di automazione o per casi di utilizzo avanzati, la gestione è inoltre disponibile utilizzando SSH con le stesse credenziali e lo stesso IP.
5. Per accedere alla GUI, fai clic sul link Management IP e immetti il nome utente e la password forniti. 
6. Dalla IU di gestione, puoi gestire FortiGate Security Appliance come un amministratore VDOM. Per le funzioni di gestione non disponibili utilizzando la IU di gestione, come la gestione dei SSL Certificates, l'avvio di un failover HA manuale, il riavvio, l'aggiornamento o l'esecuzione di un ripristino della configurazione predefinito, deve essere aperto un ticket di supporto.

Fortinet conserva [la documentazione online includendo una guida di riferimento dettagliata interattiva ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://cookbook.fortinet.com/fortigate/){: new_window} che può essere utilizzata come riferimento durante la configurazione.
