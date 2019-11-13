---

copyright:
  years: 2017
lastupdated: "2019-11-12"

keywords: manage, managing, firewall

subcollection: fortigate-1g

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:note: .note}
{:important: .important}

# Managing the FortiGate Security Appliance 1Gbps
{: #managing-the-fortigate-security-appliance-1gbps}

When the Fortigate Security Appliance 1Gbps (FSA) is first added to the VLAN, all traffic is allowed. You need to add rules to the firewall in order to control the traffic.
{: shortdesc}

1. From your browser, open the [IBM Cloud UI Console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/classic/security/firewalls/multivlan/provision){: new_window} and log into your account.
2. CliCK the navigation menu in the top left of the [IBM Cloud Catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com) and select **Classic Infrastructure > Network > IP Management > VLANs**.

	To view only Public VLANs, click on the **Filter** drop down and enter ``fcr`` in the **Primary Router** field.
  {: tip}

3. Scroll to the VLAN you want to manage and click on the link of the firewall name in the **GATEWAY/FIREWALL** column to go to the **Device Details** page.
4. In the **Device Details** page, you can view the associated subnets, the current "Status" of the firewall routing, and the management information.

	The management information includes a **Management IP**, a **Username**, and a **Password**. This Management IP is publicly accessible by default. For automation purposes or advanced use cases, administration is also available using SSH with the same IP and credentials.
5. To access the GUI, click on the Management IP link and enter the username and password provided.
6. From the Management UI, you can manage the FortiGate Security Appliance as a VDOM Administrator. For management functions not available using the Management UI, such as managing SSL Certificates, initiating a manual HA failover, rebooting, upgrading, or performing a default configuration restore, a support ticket needs to be opened.

Fortinet maintains [online documentation including an interactive cookbook ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://cookbook.fortinet.com/fortigate/){: new_window} that can be used for reference during configuration.
