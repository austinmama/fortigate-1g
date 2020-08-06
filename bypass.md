---

copyright:
  years: 2017
lastupdated: "2020-06-03"

keywords: bypass, firewall, enable

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

# Bypassing the firewall
{: #bypassing-the-firewall}

You can bypass your FortiGate Security Appliance 1 Gbps (FSA) by following the instructions here.
{: shortdesc}

Follow these steps:

1. From your browser, open the [IBM Cloud UI Console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/classic/security/firewalls/multivlan/provision){: new_window} and log in to your account.
2. Click the navigation menu in the [IBM Cloud Catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com). Then, select **Classic Infrastructure > Network > IP Management > VLANs** and click the firewall device that you want to bypass.
3. In the **Device Details** page, you can use the **Actions** drop down menu to choose **Set Route Bypass** or in the **Status:** section, you can click the **Route Around** button. Bypassing the rules takes approximately two minutes to take effect. The Status changes to "Bypassing All Rules".

	Another option is to route around the firewall. You can use the **Actions** drop down menu to choose **Set Route Bypass** or in the **Status:** section, you can click the **Route Around** button. Click **Yes** to confirm your action. Bypassing the route takes approximately two minutes to take effect. While in bypass mode, the status is `Routing AROUND firewall`.

## Unbypass the firewall
{: #unbypass-the-firewall}

To route the public network traffic back to the firewall, follow the previous instructions to locate the **Configuration** tab of the device. Click the **Actions** menu and choose **Set Route Bypass**, or in the **Status** section, click the **Route Through** button. Click **Yes** to confirm your action. The status changes back to `Routing THROUGH firewall` within two minutes.
