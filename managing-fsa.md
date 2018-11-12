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

# Manage the FortiGate Security Appliance

When the firewall is first added to the VLAN, all traffic is allowed. You need to add rules to the firewall in order to control the traffic. 

1. From your browser, open [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} and log into your account.
2. In the Customer Portal navigation, select **Network > IP Management > VLANs**. 

	**Tip:** To view only Public VLANs, click on the **Filter** drop down and enter ``fcr`` in the **Primary Router**.
3. Scroll to the VLAN you want to manage and click on the link of the firewall name in the **GATEWAY/FIREWALL** column to go to the **Device Details** page.
4. In the **Device Details** page, you can view the associated subnets, the current "Status" of the firewall routing, and the management information. 

	The management information includes a **Management IP**, a **Username**, and a **Password**. This Management IP is publicly accessible by default. For automation purposes or advanced use cases, administration is also available using SSH with the same IP and credentials.
5. To access the GUI, click on the Management IP link and enter the username and password provided. 
6. From the Management UI, you can manage the FortiGate Security Appliance as a VDOM Administrator. For management functions not available using the Management UI, such as managing SSL Certificates, initiating a manual HA failover, rebooting, upgrading, or performing a default configuration restore, a support ticket needs to be opened.

Fortinet maintains [online documentation including an interactive cookbook ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://cookbook.fortinet.com/fortigate/){: new_window} that can be used for reference during configuration.