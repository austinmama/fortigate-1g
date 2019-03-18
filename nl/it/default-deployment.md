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

# Distribuzione predefinita di un Fortigate Security Appliance 1Gbps
{: #default-deployment-of-a-fortigate-security-appliance-1gbps}

Il FortiGate Security Appliance (FSA) 1Gbps viene distribuito a un solo Virtual Domain (normalmente firewall001) in un'applicazione dedicata. Il cliente ha l'accesso completo alle risorse dell'applicazione (processori, memoria e così via), ma l'accesso alla configurazione al livello del dispositivo viene vincolato per garantire che IBM© Cloud possa effettivamente supportare il dispositivo. 

Il FSA viene distribuito in modalità NAT e risiede in due VLAN/reti all'interno dell'infrastruttura di rete pubblica. La VLAN esterna è la VLAN pubblica di IBM Cloud dove il traffico entra nel data center e viene instradato al FSA. La VLAN interna è la VLAN FCR (Frontend Customer Router) pubblica protetta assegnata del cliente ed è dove risiedono le risorse server del cliente.  

IBM Cloud distribuisce il FSA con due interfacce 1G associate in ognuna di queste due reti durante il processo di provisioning. IBM Cloud distribuisce inoltre una sola interfaccia per il provisioning e la manutenzione del dispositivo che non viene resa disponibile ai clienti.

Il firewall viene distribuito con tutto il traffico IPv4 e IPv6 consentito, inclusa una regola specifica (softlayer-admin) progettata per consentire alla rete di gestione interna di IBM Cloud di accedere ai dispositivi tramite il firewall. Le protezioni DoS (Denial of Service) e molti altri filtri non sono configurati per l'applicazione.
