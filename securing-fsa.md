---

copyright:
  years: 2017
lastupdated: "2019-11-12"

keywords: secure, securing, firewall, fsa, configure, security

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
{:help: data-hd-content-type='help'}
{:support: data-reuse='support'}

# Securing the FortiGate Security Appliance 1 Gbps
{: #securing-the-fortigate-security-appliance-1-gbps}
{: help}
{: support}

You can configure the FortiGate Security Appliance (FSA) 1 Gbps to meet security and compliance requirements. IBM© Cloud provides a VDOM Administrator account with a randomly assigned password. You can rotate that password, create read-only users, and restrict access based on "Trusted Hosts," which accepts traffic only from specified source IPs (up to three).
{: shortdesc}

To complete these activities:

1. From your browser, open the [IBM Cloud UI Console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/classic/security/firewalls/multivlan/provision){: new_window} and log in to your account.
2. Follow the How to [Manage the FortiGate Security Appliance](/docs/fortigate-1g?topic=fortigate-1g-managing-the-fortigate-security-appliance-1gbps) instructions to find the credentials.
3. Log in to the appliance, and navigate to **System > Admin > Administrators**. All access and changes are logged.
4. To configure individual interfaces, navigate to **System > Network > Interfaces**.

    You can restrict access to the administrative interfaces to just the protocols they require (typically HTTPS and SSH, which provides in-transit encryption). For extra security, you can also disable external access to the administrative interface. You can accomplish this by enabling the appropriate protocols on the "inside" interface (the interface that a customer's public VLAN resides on). You can also disable all protocols on the "outside" interface (the interface that public internet traffic is received from). This additional security measure requires a server that is positioned inside the VLAN from which to administer the FSA.
