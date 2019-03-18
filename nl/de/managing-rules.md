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

# Regeln für Fortigate-Firewall (Richtlinien) verwalten
{: #managing-fortigate-firewall-rules-policies-}

FortiGate nutzt das Konzept einer "Richtlinie", die Datenverkehr akzeptiert/ablehnt, Sicherheitsprofile anwendet, Datenverkehr reguliert, Datenverkehr protokolliert und einen Zeitrahmen für die Anwendung einer Richtlinie festlegt. Um eine Richtlinie zusammenzustellen, müssen Sie zuerst die Objekte erstellen, die teilnehmen. 

1. Melden Sie sich bei der Appliance mit den Berechtigungsnachweisen an, die auf der Seite **Gerätedetails** im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} zu finden sind. Folgen Sie den Anweisungen in [Die FortiGate Security Appliance verwalten](/docs/infrastructure/fortigate-1g?topic=fortigate-1g-managing-the-fortigate-security-appliance-1gbps), um die Berechtigungsnachweise zu suchen.
2. Navigieren Sie nach der Anmeldung bei der Appliance zum Menü **Richtlinie und Objekte** und wählen Sie das Protokoll (wie IPv4 oder IPv6) aus, das verwaltet werden soll. Die Richtlinien werden anhand der Sequenznummer (ganz links) für den Datenverkehr implementiert. Benutzer können eine Richtlinie in der Liste nach oben ziehen, um sie früher zu implementieren, oder nach unten ziehen, um sie später zu implementieren.
3. Klicken Sie zum Hinzufügen einer Richtlinie auf **Neue erstellen** und beziehen Sie sich auf diese Felddefinitionen:

    **Eingangsschnittstelle:** Entweder die öffentliche Schnittstelle (externe Schnittstelle) für Eingangsregeln oder die rechnerorientierte Schnittstelle (interne Schnittstelle) für Ausgangsregeln.

    **Quellenadresse:** Das sind die Quellen-IP-Adressen für den Datenverkehr. Diese IP-Adresse muss im Menü "Objekte" der Liste "Adressen" hinzugefügt werden. Hinweis: Es gibt auch die Option "Alle".

    **Quellenbenutzer:** Wendet die Richtlinie auf einen Benutzer oder eine Gruppe an, der oder die in der Anzeige "Benutzer und Gerät" erstellt wurde.

    **Typ der Quelleneinheit:** Wendet die Richtlinie auf eine Einheit an, die in der Anzeige "Benutzer und Gerät" erstellt wurde.

    **Zieladresse:** Das sind die IP-Zieladressen für den Datenverkehr. Diese IP-Adresse muss im Menü "Objekte" der Liste "Adressen" hinzugefügt werden. Hinweis: Es gibt auch die Option "Alle".

    **Zeitplan:** Bestimmt, zu welchen Zeitpunkt die Richtlinie ausgeführt wird. Es gibt auch die Option "Immer". Sie können auch im Menü "Objekte" unter "Zeitpläne" einen Zeitplan erstellen.

    **Service:** Bestimmt den Service, auf den die Richtlinie angewendet wird. Es gibt auch die Option "Alle" sowie weitere Standardservices. Im Menü "Services" unter "Objekte" könne weitere Services hinzugefügt werden.

    **Aktion:** Akzeptiert oder lehnt den Datenverkehr ab. 

    **Firewall/Netzoptionen:** Aktiviert oder inaktiviert NAT und die zugehörigen Optionen.

    **Sicherheitsprofile:** Jede Option kann ein- oder ausgeschaltet werden. Lässt auch eine Zuordnung zum Profil zu.

    **Regulierung des Datenverkehrs:** Auf diese Weise können Sie die maximale und garantierte (minimale) Bandbreite für den Datenverkehr konfigurieren. Sie können zudem ein maximales Verbindungslimit für einen IP-Shaper festlegen. 

    DSCP-Einstellungen sind nicht wirksam, da von Benutzern erstellte QoS-Informationen von der IBM© Cloud-Plattform ignoriert werden.

    **Protokollierungsoptionen:** Damit wird konfiguriert, wie der zulässige Datenverkehr ("Zulässig") protokolliert wird. Diese Einstellung (und insbesondere die Option "Pakete erfassen") belegt Geräteressourcen.

    **Kommentare:** Vom Benutzer generierte Kommentare.

    **Diese Richtlinie aktivieren** Aktiviert oder inaktiviert die Richtlinie.

## Beispiel der einfachen Regel "Alle zulassen" für Webdatenverkehr zu einem Web-Server

***Eingangsschnittstelle:*** *externes VLAN*

***Quellenadresse:*** *Alle*

***Quellenbenutzer:** *Leer*

***Typ der Quelleneinheit:*** *Leer*

***Ausgangsschnittstelle:*** *internes VLAN*

***Zieladresse:*** *x.x.x.x (Web-Server-IP)*

***Zeitplan:*** *Immer*

***Service:*** *HTTP*

***Aktion:*** *ACCEPT*

***NAT:*** *OFF*

***Sicherheitsprofile:*** *Standard verwenden*

***Regulierung des Datenverkehrs:*** *Off*

***Zulässigen Datenverkehr protokollieren:*** *On (Sicherheitsereignisse)*

***Kommentare:*** *Web-Server-Datenverkehr x.x.x.x*

***Diese Richtlinie aktivieren:*** *On*
