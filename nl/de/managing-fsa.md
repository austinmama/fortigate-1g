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

# Die FortiGate Security Appliance verwalten

Wenn die Firewall dem VLAN hinzugefügt wird, ist der gesamte Datenverkehr zulässig. Sie müssen der Firewall Regeln hinzufügen, um den Datenverkehr zu steuern. 

1. Öffnen Sie im Browser das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} und melden Sie sich bei Ihrem Konto an.
2. Wählen Sie in der Navigation des Kundenportals **Netz > IP-Verwaltung > VLANs** aus. 

	**Tipp:** Um die öffentlichen VLANs anzuzeigen, klicken Sie auf die Dropdown-Liste **Filtern** und geben Sie ``fcr`` für den **primären Router** ein.
3. Blättern Sie zu dem VLAN, das Sie verwalten möchten, und klicken Sie auf den Link zu dem Firewall-Namen in der Spalte **GATEWAY/FIREWALL**, um die Seite **Gerätedetails** aufzurufen.
4. Sie können auf der Seite **Gerätedetails** die zugehörigen Teilnetze, den aktuellen "Status" des Firewall-Routings und die Verwaltungsinformationen anzeigen. 

	Die Verwaltungsinformationen umfassen **Verwaltungs-IP**, **Benutzername** und **Kennwort**. Diese Verwaltungs-IP ist standardmäßig öffentlich verfügbar. Zu Automatisierungszwecken oder für erweiterte Anwendungsfälle steht die Verwaltung auch unter Verwendung von SSH mit derselben IP-Adresse und denselben Anmeldeinformationen bereit.
5. Um auf die Benutzerschnittstelle zuzugreifen, klicken Sie auf den Verwaltungs-IP-Link und geben Sie den Benutzernamen und das Kennwort ein. 
6. Über die Verwaltungsschnittstelle können Sie die FortiGate Security Appliance als VDOM-Administrator verwalten. Für Verwaltungsfunktionen, die nicht über die Verwaltungsschnittstelle verfügbar sind, z. B. das Verwalten von SSL-Zertifikaten, das Initiieren eines manuellen HA-Failovers, das Neustarten, Aktualisieren oder Durchführen einer Standardkonfigurationswiederherstellung muss ein Support-Ticket geöffnet werden.

Fortinet hat eine [Onlinedokumentation mit einem interaktiven Cookbook ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://cookbook.fortinet.com/fortigate/){: new_window}, die während der Konfiguration als Referenz genutzt werden kann.
