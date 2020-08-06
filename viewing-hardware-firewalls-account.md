---

copyright:
  years: 2017,2018
lastupdated: "2019-11-12"

keywords: view, viewing, vlans, vlan, gateway, firewall

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

# Viewing your FortiGate firewalls
{: #viewing-your-fortigate-firewalls}

You can see which VLANs are protected with firewalls and find more details about your individual firewalls by visiting the VLAN page.
{: shortdesc}

1. From your browser, open the [IBM Cloud UI Console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/classic/security/firewalls/multivlan/provision){: new_window} and log in to your account.
2. Click the navigation menu in the [IBM Cloud Catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com) and select **Classic Infrastructure > Network > IP Management > VLANs**.

Each row in the table represents a VLAN in your infrastructure. IBM© Cloud populates the "VLAN Number" and "Primary Router" information automatically indicating the true VLAN number and the router that it is configured on. The "Name" field can be used to give the VLAN a recognizable name (such as DMZ, intranet, Public, or database).

The far right column **Gateway/Firewall** contains details about what firewall protection is in place, for example:

* **Add Firewall** indicates that there are no firewalls in place for servers on this VLAN.
* **Individually Protected Servers** indicates that one or more servers is using a Hardware Firewall (Shared) and that there is not a Hardware Firewall (Dedicated), FortiGate Security Appliance, or Network Gateway in place. VLAN firewalls and network gateways are not able to be placed on a VLAN that contains individually protected servers.
* **Firewall-vlanXXXX.networklayer.com** indicates that there is a Hardware Firewall (Dedicated) or a FortiGate Security Appliance in place. Only one VLAN firewall or Network Gateway can be associated with a VLAN. Also, a server can be protected on the public VLAN by a VLAN firewall and associated on the private network with a Network Gateway.
* **GatewayName** indicates that the VLAN is associated with that Network Gateway.

## Individually protected servers details
{: #individually-protected-servers-details}

For VLANs that contain **Individually Protected Servers** in the **Gateway/Firewall** field, you can click the associated VLAN number link to display the details of the VLAN, including the associated devices.

In the list of associated devices, you can click each device and scroll to the bottom of the Configuration tab. You see **Firewall** in the Addons section with **Installed** or **Not Installed** for the status.

* **Not Installed** indicates that no firewall is in place for this device.
* **Installed** indicates that a firewall is in place and you have a **Firewall** tab available on the device where you can manage the firewall configuration.

## Dedicated firewall details
{: #dedicated-firewall-details}

For VLANs that have `Firewall-vlanXXXX.networklayer.com` in the **Gateway/Firewall** field, you can click that firewall link to display the details of the Firewall. The device details include the associated router, VLAN, IPv4 and IPv6 subnets, the devices associated with that VLAN, and the controls for routing traffic through or around the firewall.

FortiGate Security Appliance devices have the management IP, username, and password. Management of FortiGate Security Appliances is completed through their own GUI or SSH-based console.

## Network gateway details
{: #network-gateway-details}

For VLANs that have a Network Gateway device name in the **Gateway/Firewall** field, you can click the Network Gateway name to display details of the Network Gateway. The device details include the associated front end (FCR) and backend (BCR) VLANs and Network Gateway management options.
