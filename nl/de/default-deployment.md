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

# Standard-Bereitstellung

Die FortiGate Security Appliance (FSA) mit 1 Gbit/s wird als einzelne virtuelle Domäne (normalerweise Firewall001) auf einer dedizierten Appliance bereitgestellt. Der Kunde hat vollen Zugriff auf die Ressourcen der Appliance (Prozessoren, Arbeitsspeicher usw.). Der Zugriff auf die Konfiguration auf Geräteebene ist jedoch beschränkt, damit sichergestellt werden kann, dass IBM Cloud das Gerät effektiv unterstützen kann.

Die FSA wird im NAT-Modus bereitgestellt und befindet sich in zwei VLANs/Netzen innerhalb der öffentlichen Netzinfrastruktur. Das externe VLAN ist das öffentliche IBM Cloud-VLAN, bei dem der Datenverkehr in das Rechenzentrum eintrifft und an die FSA weitergeleitet wird. Das interne VLAN ist das dem Kunden zugewiesene geschützte öffentliche FCR-VLAN (Frontend Customer Router). Dort befinden sich die Serverressourcen des Kunden.  

IBM Cloud implementiert die FSA mit zwei gebündelten 1G-Schnittstellen in jedem dieser beiden Netze während des Bereitstellungsprozesses. IBM Cloud stellt außerdem eine einzige Schnittstelle für die Bereitstellung und Wartung des Geräts bereit, die den Kunden nicht zur Verfügung gestellt wird.

Die Firewall wird mit jedem zulässigen IPv4- und IPv6-Datenverkehr bereitgestellt, einschließlich einer bestimmten Regel (Softlayer-Administrator), die dem internen Verwaltungsnetz von IBM Cloud den Zugriff auf Geräte über die Firewall ermöglicht. Der Denial-of-Service-Schutz und die meisten anderen Filter sind so konfiguriert, dass sie nicht erzwungen werden.
