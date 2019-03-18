---

copyright:
  years: 2017,2018
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:faq: data-hd-content-type='faq'}

# FAQ per Fortigate Security Appliance 1Gbps
{: #faqs-for-fortigate-security-appliance-1gbps}

Le seguenti sono le FAQ (frequently asked question) quando si utilizza il firewall FortiGate Security Appliance (FSA) 1Gbps.

## Cosa è un firewall?
{:faq}

Un firewall è un dispositivo di rete collegato in upstream da un server. Il firewall blocca il traffico non desiderato da un server prima che venga raggiunto.

## Perché dovrei utilizzare un firewall?
{:faq}

Il vantaggio principale di avere un firewall è che il tuo server deve gestire solo il traffico “buono” – questo significa che la tua risorsa viene utilizzata solamente per lo scopo previsto invece di gestire anche il traffico non desiderato.

## Quali prodotti firewall offre IBM©?
{:faq}

Puoi trovare un confronto dettagliato di tutti i prodotti firewall offerti in IBM Cloud esaminando [questo argomento](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-exploring-firewalls). 

## FortiGate Security Appliance 1Gbps è compatibile con i prodotti del programma di bilanciamento del carico di IBM?
{:faq}

Sì. Il FSA 1Gbps è compatibile con il servizio di bilanciamento del carico cloud, il programma di bilanciamento del carico locale, nonché Citrix Netscaler VPX e MPX.

## Il traffico pubblico passa prima nel mio programma di bilanciamento del carico o nel firewall?
{:faq}

Per il traffico proveniente da internet pubblico, i prodotti di bilanciamento del carico vengono prima, i prodotti Hardware Firewall vengono dopo e i prodotti NetScaler vengono per ultimi (insieme ai server dei clienti).

## IBM effettua un addebito per la larghezza di banda del firewall?
{:faq}

Il FortiGate Security Appliance 1Gbps non viene misurato con la larghezza di banda. In aggiunta, il FSA può ridurre l'utilizzo della larghezza di banda totale limitando il traffico a cui devono rispondere i server.
{:faq}

## Cosa sono le porte in grigio nel mio firewall Windows?
{:faq}

IBM Cloud offre molti servizi differenti che puoi utilizzare con il tuo server, inclusi il monitoraggio Nagios, SNMP e Evault. Questi servizi richiedono che i tuoi sistemi interni comunichino con il tuo server in qualche modo. Le porte in grigio che vedi nell'elenco delle eccezioni sono porte aperte solo nella porta di rete interna. Rimangono ancora bloccate nella connessione di rete (internet) pubblica. Poiché la rete interna è una rete protetta, avere queste porte aperte viene considerato sicuro.

Queste porte generalmente non possono essere modificate; tuttavia, se reimposti le regole del firewall, le porte saranno eliminate dall'elenco delle eccezioni. Tieni presente che reimpostando le regole del firewall potresti avere un impatto negativo su questi servizi aggiuntivi e puoi causare altri problemi a seconda della tua configurazione del server.

## Quali intervalli di IP consento tramite il firewall?
{:faq}

Per l'elenco degli indirizzi IP e di intervalli di IP da consentire tramite il firewall, vai [qui](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-ibm-cloud-ip-ranges). 

## Qual è il numero massimo di server che FortiGate Security Appliance 1Gbps proteggerà?
{:faq}

FortiGate Security Appliance 1Gbps può proteggere qualsiasi server su una VLAN pubblica. Tuttavia è importante notare che poiché questi dispositivi firewall sono collegati con un uplink di 2Gbps, consigliamo di ridimensionare il numero di istanze del firewall per soddisfare i bisogni della tua applicazione. Puoi farlo distribuendo i firewall della VLAN pubblica aggiuntivi in un pod per consentire l'aggiunta di ulteriori firewall o risorse di calcolo.

## Quali opzioni VPN sono incluse con ogni prodotto firewall?
{:faq}

Non tutti i firewall offrono la VPN e non tutte le opzioni VPN sono uguali. Le opzioni generali della VPN sono:

* Ogni cliente riceve connessioni VPN SSL illimitate alla nostra rete privata. Queste connessioni possono essere stabilite facendo clic sul link della VPN all'inizio della pagina quando si ha eseguito l'accesso al portale del cliente.
* I clienti ricevono inoltre una VPN PPTP per account. Possono aggiungere ulteriori utenti VPN PPTP ai propri account in pacchetti di 5 per ulteriori 5$/mese.
* IBM Cloud offre inoltre un servizio VPN IPSec a più tenant di base.
* Il FortiGate Security Appliance 1Gbps fornisce le opzioni VPN SSL e IPSec solo con l'accesso alla rete pubblica (nessun accesso alla rete privata di IBM Cloud).
* Il gateway di rete fornisce le funzionalità SSL, IPSec e OpenVPN nella rete privata o pubblica.
* I prodotti NetScaler possono fornire la VPN SSL e IPSec nella rete privata o pubblica.
* I clienti possono inoltre distribuire una soluzione VPN nel server all'interno del loro ambiente IBM Cloud.

## Quando seleziono l'opzione dell'elevata disponibilità, quale procedura devo seguire per utilizzare questa funzione?
{:faq}

Nessuna. Quando ordinato con HA, IBM Cloud esegue automaticamente il provisioning delle applicazioni nella configurazione HA.  Nel caso in cui il dispositivo primario abbia un malfunzionamento, un dispositivo passivo secondario prende il posto dell'istanza attiva primaria e inizia a passare il traffico. Mentre questo failover è normalmente automatico, è una procedura consigliata monitorare i server e assicurarsi che il traffico venga trasmesso correttamente.

## Quali prodotti firewall supportano il NAT da pubblico a privato e/o la segmentazione della VLAN privata?
{:faq}

Nessuno dei prodotti Hardware Firewall ha accesso alla rete privata.  È necessario un gateway di rete per fornire queste funzionalità incorporate e che i prodotti NetScaler abbiano accesso sia alla rete pubblica che privata.
