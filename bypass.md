---

copyright:
  years: 2017
lastupdated: "2018-11-12"

keywords: bypass, firewall, rules, enable

subcollection: fortigate-1g

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# Bypassing the Firewall Rules
{: #bypassing-the-firewall-rules}

You can bypass the rules of your Fortigate Security Appliance 1 Gbps (FSA) by following the instructions here.
{: shortdesc}

1. From your browser, open the [IBM Cloud UI Console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/classic/security/firewalls/multivlan/provision){: new_window} and log in to your account.
2. Click the navigation menu in the [IBM Cloud Catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com). Then, select **Classic Infrastructure > Network > IP Management > VLANs** and click the firewall device that you want to bypass.
3. In the **Device Details** page, you can use the **Actions** drop down menu to choose **Set Rule Bypass** or in the **Status:** section, you can click the **Bypass Rules** button. Bypassing the rules takes approximately two minutes to take effect. The Status changes to "Bypassing All Rules".

	Another option is to route around the firewall. You can use the **Actions** drop down menu to choose **Set Route Bypass** or in the **Status:** section, you can click the **Route Around** button. Either way, you receive a confirmation dialog. Click **Yes** to confirm the action. Bypassing the route takes approximately two minutes to take effect. While in bypass mode, the "Status" is "Routing AROUND firewall".

## Enable the Rules Again
{: #enable-the-rules-again}

To enable the rules again, follow the previous instructions to reach the **Configuration** tab of the device and click the **Actions** dropdown menu and choose **Set Route Bypass**. You receive a confirmation dialog. Click **Yes** to confirm the action. The "Status" changes back to "Routing THROUGH firewall" within two minutes.
