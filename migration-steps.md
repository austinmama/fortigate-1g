---

copyright:
  years: 2019, 2020
lastupdated: "2020-08-15"

keywords: migrate, update, gateway, firewall, cloud, fortigate, fsa, 1g, 10g, vra, vsrx, migration, migrating

subcollection: fortigate-1g

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank_"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# Migrating FortiGate Security Appliance 1 Gbps
{: #migration-overview}

FortiGate Security Appliance (FSA) 1 Gbps customers should start migrating to other security gateway options, as FSA 1 Gbps will no longer be sold after August 15, 2020. You can read the full [end of marketing announcement](/docs/fortigate-1g?topic=fortigate-1g-FSA-EOM) for more information. 
{: shortdesc}

The following procedures provide instructions for migrating FSA 1 Gbps either to Juniper vSRX, FSA 10 Gbps, or Virtual Router Appliance (VRA 5600).

In a typical migration scenario, you have an existing FSA 1 Gbps associated with a public VLAN. 

## Migrating from a FortiGate Security Appliance 1 Gbps to Juniper vSRX
{: #fsa-to-vsrx}

This migration option makes use of the Juniper support program to assist you with migrating to a Juniper vSRX. You can submit the request with your configuration using the following [Google form ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://forms.gle/DvkPBdxC6DiXrHAn6){: new_window}.
{: note}

To migrate from an FSA 1 Gbps to a vSRX, follow these steps:

1. Order a Juniper vSRX. See [Getting started with IBM Cloud Juniper vSRX](/docs/vsrx?topic=vsrx-getting-started) for details.

2. Complete your basic Juniper vSRX configurations, such as creating system users and hostnames. See [Performing vSRX basics](/docs/vsrx?topic=vsrx-performing-ibm-cloud-juniper-vsrx-basics) for details.

3. Check vSRX readiness to ensure your Juniper vSRX can perform common gateway actions. See [Checking vSRX readiness](/docs/vsrx?topic=vsrx-vsrx-readiness) for details.

  Your Juniper vSRX is not associated with any public VLAN.
  {: note}
 
4. From the VLAN page, cancel the FSA 1 Gbps. See [Canceling a firewall](/docs/fortigate-1g?topic=fortigate-1g-canceling-a-firewall) for details.

5. Associate the public VLAN that you want to protect with your new Juniper vSRX. See [Associating a VLAN to a gateway appliance](/docs/vsrx?topic=gateway-appliance-managing-vlans-and-gateway-appliances#associate-a-vlan-to-a-gateway-appliance) for details.

## Migrating from a FortiGate Security Appliance 1 Gbps to a 10 Gbps
{: #fsa-to-fsa10g}

To migrate from an FSA 1 Gbps to a FSA 10 Gbps, follow these steps:

1. Order an FSA 10 Gbps appliance. See [Getting started with FortiGate Security Appliance 10 Gbps](/docs/fortigate-10g?topic=fortigate-10g-getting-started) for details.  

2. Log in to the FSA device portal with your credentials from the [Firewall details page](/docs/fortigate-10g?topic=fortigate-10g-managing-firewall-device-details), and add your firewall rules (policies) to the FSA 10 Gbps. These policies should be the same as what you previously configured for your FSA 1 Gbps. 
 
3. From the VLAN page, cancel the FSA 1 Gbps. See [Canceling a firewall](/docs/fortigate-1g?topic=fortigate-1g-canceling-a-firewall) for details.

4. Associate the public VLAN that you want to protect with your new FSA 10 Gbps. See [Associating a VLAN with a firewall](/docs/fortigate-10g?topic=fortigate-10g-managing-vlans#associate-a-vlan-with-a-firewall) for details.

## Migrating from FortiGate Security Appliance 1 Gbps to an IBM Cloud Virtual Router Appliance
{: #fsa-to-vra}

To migrate from an FSA 1 Gbps to a Virtual Router Appliance (VRA), follow these steps:

1. Order a VRA. See [Getting started with IBM Cloud Virtual Router Appliance](/docs/virtual-router-appliance?topic=virtual-router-appliance-getting-started) for details.

2. Configure your VRA. See [Getting started with IBM Cloud Virtual Router Appliance](/docs/virtual-router-appliance) for details.
 
3. From the VLAN page, cancel the FSA 1 Gbps. See [Canceling a firewall](/docs/fortigate-1g?topic=fortigate-1g-canceling-a-firewall) for details.

4. Associate the public VLAN that you want to protect with your VRA. See [Managing VLANs with a gateway appliance](/docs/virtual-router-appliance?topic=gateway-appliance-managing-vlans-and-gateway-appliances).
