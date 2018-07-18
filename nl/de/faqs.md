---

copyright:
  years: 2017,2018
lastupdated: "2018-01-16"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Häufig gestellte Fragen

Die folgenden Fragen sind häufig gestellte Fragen zur FortiGate Security Appliance-Firewall (FSA) mit 1 Gbit/s.

## Was ist eine Firewall?

Eine Firewall ist ein Netzgerät, das einem Server vorgeschaltet ist. Die Firewall blockiert unerwünschten Datenverkehr von einem Server, bevor der Server erreicht wird.

## Warum wird eine Firewall empfohlen?

Der Hauptvorteil einer Firewall besteht darin, dass Ihr Server nur den "guten" Datenverkehr verarbeiten muss. Das bedeutet, dass Ihre Ressource ausschließlich für den beabsichtigten Zweck verwendet wird und für unerwünschten Datenverkehr.

## Welche Firewall bietet IBM an?
In diesem [Abschnitt ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/docs/infrastructure/fortigate-10g/explore-firewalls.html#explore-firewalls){: new_window} finden Sie einen detaillierten Vergleich aller in der IBM Cloud angebotenen Firewall-Produkte. 

## Ist die FortiGate Security Appliance (1 Gbit/s) mit den Load-Balancer-Produkten von IBM kompatibel?

Ja. Die FSA (1 Gbit/s) ist mit dem Lastausgleichsservice, der lokalen Lastausgleichsfunktion sowie dem Citrix Netscaler VPX und MPX kompatibel.

## Fließt der öffentliche Datenverkehr zuerst durch die Einrichtung für den Lastausgleich oder die Firewall?

Aus dem öffentlichen Internet kommen zuerst die Lastausgleich-Produkte, dann die Hardware-Firewall-Produkte und als letztes die NetScaler-Produkte (zusammen mit den Kundenservern).

## Berechnet IBM für die Firewall-Bandbreite eine Gebühr?

Die FortiGate Security Appliance (1 Gbit/s) wird nicht für die Bandbreite gemessen. Darüber hinaus kann die FSA die gesamte Bandbreitenauslastung reduzieren, indem sie den Datenverkehr begrenzt, auf den Server reagieren müssen.

## Was bedeuten die ausgegrauten Ports in meiner Windows-Firewall?

IBM Cloud bietet viele verschiedene Services, die Sie mit Ihrem Server nutzen können, einschließlich Evault, SNMP und Nagios-Überwachung. Diese Services erfordern, dass unsere internen Systeme zu einem gewissen Grad mit Ihrem Server kommunizieren. Die ausgegrauten Ports, die in der Ausnahmeliste angezeigt werden, sind Ports, die nur am internen Netzport geöffnet sind. Sie sind weiterhin über die öffentliche (Internet-)Netzverbindung blockiert. Da das interne Netz ein gesichertes Netz ist, wird das Öffnen dieser Ports als sicher angenommen.

Diese Ports können in der Regel nicht geändert werden. Wenn Sie jedoch die Firewallregeln zurücksetzen, werden die Ports aus der Ausnahmeliste gelöscht. Beachten Sie, dass das Zurücksetzen der Firewallregeln sich nachteilig auf diese zusätzlichen Services auswirken und abhängig von Ihrer Serverkonfiguration auch andere Probleme verursachen kann.

## Welche IP-Bereiche sind für die Firewall zulässig?

Die Liste der IP-Adressen und IP-Bereiche, die die Firewall zulässt, finden Sie [hier](https://console.bluemix.net/docs/infrastructure/hardware-firewall-dedicated/ips.html){: new_window}. 

## Wie viele Server werden von der FortiGate Security Appliance (1 Gbit/s) maximal geschützt?

Die FortiGate Security Appliance (1 Gbit/s) kann in einem öffentlichen VLAN jeden Server schützen. Berücksichtigen Sie jedoch, dass diese Firewallgeräte mit 2 Gbit/s Uplink verbunden sind. Daher wird empfohlen, die Anzahl der Firewallinstanzen zu skalieren, um die Leistungsanforderungen Ihrer Anwendung zu erfüllen. Stellen Sie dazu zusätzliche öffentliche VLAN-Firewalls in einem Pod bereit, um zusätzliche Firewalls und zugehörige Rechenressourcen hinzuzufügen.

## Welche VPN-Optionen sind mit jedem Firewallprodukt enthalten?

Nicht alle Firewalls bieten VPN an und nicht alle VPN-Optionen sind identisch. Die allgemeinen Optionen für VPN lauten:

* Jeder Kunde erhält uneingeschränkte SSL-VPN-Verbindungen zu unserem privaten Netz. Diese Verbindungen können hergestellt werden, indem Sie oben auf der Seite auf den VPN-Link klicken, während Sie beim Kundenportal angemeldet sind.
* Kunden erhalten außerdem pro Konto jeweils ein PPTP-VPN. Es können weitere PPTP-VPN-Benutzer in Paketen aus 5 Benutzern für 5 $ pro Monat zum Konto hinzugefügt werden.
* IBM Cloud bietet auch einen einfachen Multi-Tenant-IPSec-VPN-Service.
* Die FortiGate Security Appliance (1 Gbit/s) bietet SSL- und IPSec-VPN-Optionen ausschließlich mit Zugriff auf das öffentliche Netz (kein Zugriff auf das private IBM Cloud-Netz).
* Das Network Gateway bietet SSL-, IPSec- und OpenVPN-Funktionalitäten im öffentlichen oder privaten Netz.
* Die NetScaler-Produkte können SSL- und IPSec-VPN im öffentlichen oder privaten Netz bereitstellen.
* Kunden können in ihrer IBM Cloud-Umgebung auch eine VPN-Lösung auf einem Server bereitstellen.

## Wenn die Option "Hochverfügbarkeit" ausgewählt wurde, welche Schritte müssen dann durchgeführt werden, um dieses Feature zu nutzen?

Keine. Bei einer Bestellung mit Hochverfügbarkeit (HA) stellt IBM Cloud die Appliances automatisch in der HA-Konfiguration bereit.  Wenn die primäre Einheit ausfällt, übernimmt eine sekundäre passive Einheit die Funktion der primären aktiven Instanz, um den Datenverkehr weiterzuleiten. Während dieses Failover normalerweise automatisch erfolgt, empfiehlt es sich, die Server zu überwachen und sicherzustellen, dass der Datenverkehr erfolgreich übertragen wird.

## Welche Firewallprodukte unterstützen die Public-to-Private-NAT- bzw. private VLAN-Segmentierung?

Keines der Hardware-Firewallprodukte hat Zugriff auf das private Netz.  Ein Netzgateway muss diese Funktionen inline bereitstellen. Die NetScaler-Produkte haben Zugriff auf das öffentliche und private Netz.
