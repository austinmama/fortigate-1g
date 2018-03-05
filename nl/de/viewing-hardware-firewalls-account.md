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

# Firewalls anzeigen

Um zu erfahren, welche VLANs durch Firewalls geschützt sind, und um weitere Details zu einzelnen Firewalls zu erhalten, gehen Sie zur Seite "VLANs".

1. Öffnen Sie im Browser das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} und melden Sie sich bei Ihrem Konto an.
2. Wählen Sie in der Navigation des Kundenportals **Netz > IP-Verwaltung > VLANs** aus.

Jede Zeile in der Tabelle stellt ein VLAN in Ihrer Infrastruktur dar. IBM Cloud gibt die Informationen für "VLAN-Nummer" und "Primärer Router" automatisch ein. Dabei wird die echte VLAN-Nummer und der Router angegeben, auf die sie konfiguriert ist. Das Feld "Name" kann verwendet werden, um dem VLAN einen erkennbaren Namen zu geben (z. B. DMZ, Intranet, Öffentlich oder Datenbank).

Die rechte Spalte **Gateway/Firewall** enthält Details über den implementierten Firewallschutz. Beispiel:

- **Firewall hinzufügen** gibt an, dass in diesem VLAN keine Firewalls für Server vorhanden sind.
- **Einzeln geschützte Server** gibt an, dass mindestens ein Server eine Hardware-Firewall (freigegeben) verwendet und keine Hardware-Firewall (dediziert), keine FortiGate Security Appliance und kein Netzgateway vorhanden ist. VLAN-Firewalls und Netzgateways können nicht auf einem VLAN mit einzeln geschützten Servern platziert werden.
- **Firewall-vlanXXXX.networklayer.com** gibt an, dass eine Hardware-Firewall (dediziert) oder eine FortiGate Security Appliance vorhanden ist. Einem VLAN kann nur eine VLAN-Firewall oder ein Netzgateway zugeordnet werden. Ein Server kann jedoch im öffentlichen VLAN durch eine VLAN-Firewall geschützt und im privaten Netz mit einem Netzgateway verknüpft werden.
- **Gateway-Name** gibt an, dass das VLAN mit diesem Netzgateway verknüpft ist. 

## Details zu einzeln geschützten Servern

Bei VLANs, die **einzeln geschützte Server** im Feld **Gateway/Firewall** enthalten, können Sie auf die zugehörige VLAN-Nummer klicken, um die Details des VLAN einschließlich der zugehörigen Einheiten anzuzeigen.

In der Liste der zugeordneten Einheiten können Sie auf jede Einheit klicken und bis zum Ende der Registerkarte "Konfiguration" blättern. Angezeigt wird **Firewall** im Abschnitt "Add-ons" mit dem Status **Installiert** oder **Nicht installiert**.

- **Nicht installiert** gibt an, dass für diese Einheit keine Firewall vorhanden ist.
- **Installiert** gibt an, dass eine Firewall vorhanden ist und auf der Einheit eine Registerkarte **Firewall** verfügbar ist, auf der Sie die Firewallkonfiguration verwalten können.

## Details zu dedizierten Firewalls

Bei VLANs, die **Firewall-vlanXXXX.networklayer.com** im Feld **Gateway/Firewall** enthalten, können Sie auf den Firewall-Link klicken, um die Details der Firewall anzuzeigen. Zu den Einheitendetails gehören die zugehörigen Router, VLANs, IPv4/IPv6-Teilnetze, die mit diesem VLAN verbundenen Einheiten sowie die Steuerelemente für die Weiterleitung des Datenverkehrs durch oder um die Firewall herum.

Die FortiGate Security Appliance-Einheiten enthalten Verwaltungs-IP-Adresse, Benutzername und Kennwort. Die Verwaltung der FortiGate Security Appliances erfolgt über eine eigene Benutzerschnittstelle oder eine SSH-basierte Konsole.

## Details des Netzgateways

Bei VLANs, die den Einheitennamen des Netzgateways im Feld **Gateway/Firewall** enthalten, können Sie auf den Netzgateway-Namen klicken, um die Details des Netzgateways anzuzeigen. Zu den Einheitendetails gehören die zugehörigen Front-End (FCR)- und Back-End-(BCR)-VLANs und Netzgateway-Verwaltungsoptionen.
