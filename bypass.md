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

You can bypass the rules of your Fortigate Security Appliance 1Gbps (FSA) by following the instructions here.
{: shortdesc}

1. From your browser, open the [IBM Cloud UI Console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/classic/security/firewalls/multivlan/provision){: new_window} and log into your account.
2. ClICK the navigation menu in the top left of the [IBM Cloud Catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com) and select **Classic Infrastructure > Network > IP Management > VLANs** and click on the firewall device you want to bypass.
3. In the **Device Details** page, you can use the **Actions** drop down menu to choose **Set Rule Bypass** or in the **Status:** section, you can click on the **Bypass Rules** button. Bypassing the rules takes approximately two minutes to take effect. The Status should change to "Bypassing All Rules".

	Another option is to route around the firewall. You can use the **Actions** drop down menu to choose **Set Route Bypass** or in the **Status:** section, you can click on the **Route Around** button. Either way, you should get a confirmation dialog. Click **Yes** to confirm the action. Bypassing the route takes approximately two minutes to take effect. While in bypass mode, the "Status" will be "Routing AROUND firewall".

## Enable the Rules Again
{: #enable-the-rules-again}

To enable the rules again, follow the instructions above to reach the **Configuration** tab of the device and click on the **Actions** dropdown menu and choose **Set Route Bypass**. You will get a confirmation dialog. Click **Yes** to confirm the action. The "Status" will change back to "Routing THROUGH firewall" within two minutes.
