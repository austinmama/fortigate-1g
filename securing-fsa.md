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

# Securing the FortiGate Security Appliance 1 Gbps

You can configure the FortiGate Security Appliance (FSA) 1Gbps to meet security and compliance requirements. IBM© Cloud provides a VDOM Administrator account with a randomly assigned password. Customers can rotate that password, create read-only users and restrict access based on "Trusted Hosts," which accepts traffic only from specified source IPs (up to three). To complete these activities:

1. Log into the appliance using the credentials found in the **Device Details** page in the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window}. Follow the How to [Manage the FortiGate Security Appliance](/docs/infrastructure/fortigate-1g?topic=fortigate-1g-managing-the-fortigate-security-appliance-1gbps) instructions to find the credentials.
2. After logging into the appliance, navigate to **System > Admin > Administrators**. All access and changes are logged.
3. To configure individual interfaces, navigate to **System > Network > Interfaces**.

    You can restrict access to the administrative interfaces to only the protocols they require (typically HTTPS and SSH, since this provides in-transit encryption) or for additional security, you can disable external access to the administrative interface. This is accomplished by enabling the appropriate protocols on the "inside" interface (the interface that a customer's public VLAN resides on) and disabling all protocols on the "outside" interface (the interface that public internet traffic is received from). This additional security measure requires that the user have a server positioned inside the VLAN from which to administer the FSA. 