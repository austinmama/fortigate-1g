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

# Firewallregeln umgehen
{: #bypassing-the-firewall-rules}

Führen Sie die folgenden Schritte aus, um die Firewallregeln zu umgehen:

1. Öffnen Sie im Browser das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} und melden Sie sich bei Ihrem Konto an.
2. Wählen Sie in der Navigation des Kundenportals **Netz > IP-Verwaltung > VLANs** aus und klicken Sie auf das Firewallgerät, das Sie umgehen möchten.
3. Sie können auf der Seite **Gerätedetails** das Dropdown-Menü **Aktionen** verwenden, um den Abschnitt **Regelumgehung einrichten** auszuwählen. Sie können auch im Abschnitt **Status:** auf die Schaltfläche **Regeln umgehen** klicken. Das Umgehen der Regeln wird in etwa zwei Minuten wirksam. Der Status muss sich so ändern, dass angegeben wird, dass alle Regeln umgangen werden.

	Eine weitere Möglichkeit ist, den Datenverkehr um die Firewall herumzuleiten. Sie können das Dropdown-Menü **Aktionen** verwenden, um den Abschnitt **Route-Umgehung einrichten** auszuwählen. Sie können auch im Abschnitt **Status:** auf die Schaltfläche **Routing um eine Firewall** klicken. Bei beiden Möglichkeiten wird ein Bestätigungsdialog angezeigt. Klicken Sie auf **Ja**, um die Aktion zu bestätigen. Das Umgehen der Routen wird in etwa zwei Minuten wirksam. Im Umgehungsmodus gibt der Status an, dass der Datenverkehr um die Firewall herum geleitet wird.

## Regeln wieder aktivieren

Um die Regeln wieder zu aktivieren, befolgen Sie die Anweisungen oben, um die Registerkarte **Konfiguration** für das Gerät aufzurufen. Klicken Sie auf das Dropdown-Menü **Aktionen** und wählen Sie **Route-Umgehung einrichten** aus. Es wird ein Bestätigungsdialog angezeigt. Klicken Sie auf **Ja**, um die Aktion zu bestätigen. Der Status gibt in etwa zwei Minuten wieder an, dass der Datenverkehr DURCH die Firewall geleitet wird.
