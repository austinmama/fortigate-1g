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

# Informationen zu

Eine FortiGate Security Appliance (FSA) mit 1 Gbit/s ist ein dediziertes, für einzelne Tenants konzipiertes Netzgerät, das einem Server vorgeschaltet ist, der einen oder alle Server in einem öffentlichen VLAN schützt. Es wird separat von einem Server erworben und kann jederzeit zu einem VLAN hinzugefügt werden.  IBM Cloud stellt das [Kundenportal![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://www.fortinet.com/sites/default/files/productdatasheets/FortiGate-300C.pdf){: new_window} innerhalb einer virtuellen Domäne (VDOM) auf der dedizierten Appliance bereit und ermöglicht den Kunden den uneingeschränkten Zugriff auf diese virtuelle Domäne, ohne die Integrität des Geräts zu beeinträchtigen. 

Mit der FSA (1 Gbit/s) haben Kunden Zugriff auf erweiterte Features und die Möglichkeit, das Gerät in einem viel höheren Grad als andere Produkte zu optimieren. Die Firewall blockiert oder reguliert den Datenverkehr, bevor der Datenverkehr den Server erreicht. Die Hauptvorteile sind, dass ein Server nur den "guten" Datenverkehr bewältigen muss und dass die Bandbreite für weniger kritische Kommunikation eingeschränkt werden kann. 

Kunden können die FSA entweder über die webbasierte FortiOS-Benutzerschnittstelle oder die CLI (Command Line Interface) mit SSH verwalten. Es kann auch eine Hochverfügbarkeit bestellt werden, die zwei Geräte in der Aktiv-Passiv-Bereitstellung mit synchronisierten Konfigurationen bereitstellt.

Da die monatliche Serverbandbreite am Server-Switch-Port aufgezeichnet wird, wird der von der FSA (1 GBit/s) blockierte Datenverkehr nicht auf Ihre monatlichen Kontingente angerechnet, sodass kein unnötiger Datenverkehr bezahlt werden muss.

## Überblick und Features

**Bestimmungsgemäßer Gebrauch:** Einzelner öffentlicher VLAN-Schutz

**Benutzerschnittstelle:** FortiGate-Benutzerschnittstelle und Befehlszeilenschnittstelle

**Features:** Zustandsorientierte Paketüberprüfung (SPI, Stateful Packet Inspection), VLAN-Schutz, Firewall-Eingangsregeln, Firewall-Ausgangsregeln, NAT, SSL-VPN-Terminierung, IPSec-VPN-Terminierung, erweiterte Protokollierung, hohe Verfügbarkeit (optional)

**Durchsatz:** 1 Gb/s (2 Gb/s aggregiert)
