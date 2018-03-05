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

# Die FortiGate Security Appliance sichern

Sie können die FortiGate Security Appliance (FSA) mit 1 Gbit/s konfigurieren, um Sicherheits- und Compliance-Anforderungen zu erfüllen. IBM Cloud stellt ein VDOM-Administratorkonto mit einem zufällig generierten Kennwort bereit. Kunden können dieses Kennwort regelmäßig ändern, schreibgeschützte Benutzer erstellen und den Zugriff anhand "vertrauenswürdiger Hosts" einschränken, wodurch nur Datenverkehr von (bis zu drei) bestimmten Quellen-IP-Adressen zugelassen werden. Gehen Sie wie folgt vor, um diese Aktivitäten abzuschließen:

1. Melden Sie sich bei der Appliance mit den Berechtigungsnachweisen an, die auf der Seite **Gerätedetails** im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} zu finden sind. Folgen Sie den Anweisungen in [Die FortiGate Security Appliance verwalten](managing-fsa.html), um die Berechtigungsnachweise zu suchen.
2. Navigieren Sie nach der Anmeldung bei der Appliance zu **System > Administrator > Administratoren**. Alle Zugriffe und Änderungen werden protokolliert.
3. Um einzelne Schnittstellen zu konfigurieren, navigieren Sie zu **System > Netz > Schnittstellen**.

    Sie können den Zugriff auf die Verwaltungsschnittstellen auf die erforderlichen Protokolle beschränken (in der Regel HTTPS und SSH, um eine In-Transit-Verschlüsselung zu ermöglichen). Für zusätzliche Sicherheit können Sie den externen Zugriff auf die Verwaltungsschnittstelle inaktivieren. Dazu werden die entsprechenden Protokolle der "internen" Schnittstelle (der Schnittstelle, auf der sich das öffentliche VLAN eines Kunden befindet) aktiviert und alle Protokolle der "externen" Schnittstelle (der Schnittstelle, auf der sich das öffentliche VLAN eines Kunden befindet) sowie alle Protokolle der "externen" Schnittstelle (der Schnittstelle, auf der der öffentliche Internetdatenverkehr empfangen wird) inaktiviert. Für diese zusätzliche Sicherheitsmaßnahme ist es erforderlich, dass sich der Server eines Benutzers innerhalb des VLAN befindet, von dem aus die FSA verwaltet werden soll. 
