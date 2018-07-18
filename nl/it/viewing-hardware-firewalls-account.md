---

copyright:
  years: 2017,2018
lastupdated: "2018-01-18"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Visualizza i tuoi firewall

Per visualizzare quali VLAN sono protette dai firewall e per trovare ulteriori dettagli su ogni firewall, passa alla pagina delle VLAN.

1. Dal tuo browser, apri [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} e accedi al tuo account.
2. Nella navigazione del portale del cliente, seleziona **Network > IP Management > VLANs**.

Ogni riga nella tabella rappresenta una VLAN nella tua infrastruttura. IBM Cloud popola le informazioni "VLAN Number" e "Primary Router" automaticamente indicando il router e il numero di VLAN reale che stanno venendo configurati. Il campo "Name" può essere utilizzato per fornire alla VLAN un nome riconoscibile (come DMZ, Intranet, Public o Database).

La colonna all'estrema destra **Gateway/Firewall** contiene i dettagli su quale protezione firewall è in uso, ad esempio:

- **Add Firewall** indica che non ci sono firewall in uso per i server su questa VLAN.
- **Individually Protected Servers** indica che uno o più server sta utilizzando un Hardware Firewall (Shared) e non è in uso un Hardware Firewall (Dedicated), FortiGate Security Appliance o un gateway di rete. I gateway di rete e i firewall della VLAN non possono essere utilizzati su una VLAN che ha server protetti individualmente.
- **Firewall-vlanXXXX.networklayer.com** indica che è in uso un Hardware Firewall (Dedicated) o un FortiGate Security Appliance. Può essere associato solo un firewall VLAN o un gateway di rete a una VLAN, ma un server può essere protetto su una VLAN pubblica da un firewall VLAN e associato a una rete privata con un gateway di rete.
- **GatewayName** indica che la VLAN viene associata a tale gateway di rete.

## Dettagli dei server protetti individualmente

Per le VLAN che hanno **Individually Protected Servers** nel campo **Gateway/Firewall**, puoi fare clic sul link del numero della VLAN associata per visualizzarne i dettagli, inclusi i dispositivi associati.

Nell'elenco dei dispositivi associati, puoi fare clic su ogni dispositivo e scorrere in fondo alla scheda Configuration. Visualizzerai **Firewall** nella sezione Addons con **Installed** o **Not Installed** per lo stato.

- **Not Installed** indica che nessun firewall è in uso per questo dispositivo.
- **Installed** indica che un firewall è in uso e che avrai una scheda **Firewall** disponibile sul dispositivo dove puoi gestire la configurazione del firewall.

## Dettagli del firewall dedicato

Per le VLAN che hanno **Firewall-vlanXXXX.networklayer.com** nel campo **Gateway/Firewall**, puoi fare clic su tale firewall per visualizzarne i dettagli. I dettagli del dispositivo includono il router associato, la VLAN, le sottoreti IPv4/IPv6, i dispositivi associati a tale VLAN e i controlli per l'instradamento del traffico tramite o intorno al firewall.

I dispositivi FortiGate Security Appliance avranno un IP di gestione, un nome utente e una password.  La gestione dei FortiGate Security Appliance viene completata tramite la rispettiva GUI o console basata su SSH.

## Dettagli del gateway di rete

Per le VLAN che hanno un nome dispositivo del gateway di rete nel campo **Gateway/Firewall**, puoi fare clic sul nome del gateway di rete per visualizzarne i dettagli. I dettagli del dispositivo includono le VLAN di frontend (FCR) e di backend (BCR) associate e le opzioni di gestione del gateway di rete.
