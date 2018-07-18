---

copyright:
  years: 2017
lastupdated: "2017-10-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Eine FortiGate-Firewallregel zum Zulassen eines IP-Teilnetzes für den Zugriff auf Ihre Web-Server einrichten

Sie können eine FortiGate-Firewallregel so konfigurieren, dass nur Zugriff von einem bestimmten Teilnetz oder einer bestimmten IP-Adresse auf Ihren geschützten Web-Server möglich ist.

1. Melden Sie sich bei der FortiGate-Einheit an. Den Anmeldelink und die Details finden Sie auf dem Bildschirm "Gerätedetails" unter dem Abschnitt "Management".
* Navigieren Sie zu **Richtlinie > Richtlinie** und klicken Sie auf **Neue erstellen**.
* Um eine Regel zu erstellen, die nur Datenverkehr von einer bestimmten IP-Adresse zu Ihren Servern zulässt, geben Sie folgende Konfigurationen ein:
    * Quellenschnittstelle/Zone = v###-outside
    * Quellenadresse = Die IP-Adresse und das Teilnetz der IP-Adresse, die zugelassen werden soll. Adressen können in zwei verschiedenen Formaten eingegeben werden: 10.10.20.[1-14] oder 10.10.20.1/255.255.255.240.
    * Zielschnittstelle/Zone  = v###-inside
    * Zieladresse = Die spezifischen IP-Adressen des Servers, der Zugriff erhalten soll. Wenn Sie Zugriff auf einen Ihrer Web-Server gewähren möchten, können Sie "Alle" auswählen.
    * Service = Der zugelassene Servicetyp, wie HTTP, SSH, SMB, DHCP.  Wenn es keinen bestimmten Service gibt, können Sie "Beliebige" auswählen, damit nach dieser Regel alle Services zugelassen werden.
    * Aktion = ACCEPT
    * Klicken Sie auf "OK", um die Regel zu speichern.
    * Testen Sie Ihre Regel mit dem Ping-Befehl und der IP-Adresse eines Servers, um zu bestätigen, ob Sie von einer zulässigen Adresse sowie von einer nicht zulässigen Adresse auf den Server zugreifen können.
        * Bei einer zulässigen Adresse erhalten Sie eine Antwort. Bei einer nicht zulässigen Adresse erhalten Sie die Antwort für eine Zeitüberschreitung der Anforderung.
        * Wenn die Richtlinie die Regel nicht wie erwartet anwendet, müssen Sie möglicherweise die Reihenfolge Ihrer Regeln anpassen, da die Richtlinienregeln von oben nach unten angewendet werden.
