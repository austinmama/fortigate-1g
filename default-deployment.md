---

copyright:
  years: 2017
lastupdated: "2019-11-12"

keywords: default, deployment

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

# Default deployment of a Fortigate Security Appliance 1 Gbps
{: #default-deployment-of-a-fortigate-security-appliance-1gbps}
{: help}
{: support}

The FortiGate Security Appliance (FSA) 1 Gbps is deployed as a single Virtual Domain (typically firewall001) on a dedicated appliance. The customer has full access to the resources of the appliance (processors, memory, and so on), but access to device-level configuration is constrained to ensure IBM© Cloud can effectively support the device.
{: shortdesc}

The FSA is deployed in NAT mode and resides in two VLANs within the public network infrastructure. The Outside VLAN is the IBM Cloud public VLAN where traffic enters the data center and is routed to the FSA. The inside VLAN is your protected public FCR (Frontend Customer Router) VLAN and is where the customer's server resources reside.  

IBM Cloud deploys the FSA with two bonded 1G interfaces on each of these two networks during the provisioning process. IBM Cloud also deploys a single interface for provisioning and maintenance of the device that is not made available to customers.

The firewall is deployed with all IPv4 and IPv6 traffic that is allowed, including a specific rule designed to allow the IBM Cloud internal administration network to access devices through the firewall. Denial of Service protections and most other filters are configured not to enforce.
