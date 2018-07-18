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

# Bekannte Einschränkungen
Die FortiGate Security Appliance (FSA) mit 1 Gbit/s hat folgende bekannte Einschränkungen:

* Inkompatibel mit dem Windows-Netzlastenausgleich (NLB) aufgrund der Verarbeitung von ARP.

* Die Failover-Funktionalität für hohe Verfügbarkeit wird dem Benutzer nicht zur Verfügung gestellt. Wenn die Master-Firewall nicht funktioniert, aber kein automatischer Failover erfolgt, wird ein Support-Ticket benötigt. Die Geräteüberwachung für kritische Services wird empfohlen, um sicherzustellen, dass Firewalls den Datenverkehr richtig weiterleiten.

* Eine FortiGate Security Appliance kann nicht in einem VLAN bereitgestellt werden, das einem Netzgateway, einer Hardware-Firewall oder einer anderen FortiGate Security Appliance aktuell zugeordnet ist.

* Die FortiGate Security Appliance ist einem einzelnen öffentlichen Kunden-VLAN (dem "internen" VLAN) zugeordnet und kann nicht auf das private Netz zugreifen.
