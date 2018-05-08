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

# Escludi le regole del firewall

Per escludere le regole del firewall, completa la seguente procedura:

1. Dal tuo browser, apri [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} e accedi al tuo account.
2. Nella navigazione del portale del cliente, passa a **Network > IP Management > VLANs** e fai clic sul dispositivo firewall che vuoi escludere.
3. Nella pagina **Device Details**, nella scheda **Configuration**, puoi utilizzare il menu a discesa **Actions** per scegliere **Set Route Bypass** o nella sezione **Status:**, puoi far clic sul pulsante **Bypass Rules**. 

	Un'altra opzione è di instradare intorno al firewall, puoi effettuare questa azione facendo clic sul pulsante **Route Around**. In entrambi i modi, visualizzerai una finestra di dialogo di conferma. Fai clic su **Yes** per confermare l'azione. L'esclusione delle regole ha effetto dopo circa due minuti. Durante la modalità di esclusione, "Status" sarà "Routing AROUND firewall".

## Riabilita le regole

Per riabilitare le regole, completa le precedenti istruzioni per raggiungere la scheda **Configuration** del dispositivo e fai clic sul menu a discesa **Actions** e scegli **Set Route Bypass**. Visualizzerai una finestra di dialogo di conferma. Fai clic su **Yes** per confermare l'azione. "Status" ritornerà "Routing THROUGH firewall" in due minuti.
