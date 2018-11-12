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

# Default Deployment

The FortiGate Security Appliance (FSA) 1Gbps is deployed as a single Virtual Domain (typically firewall001) on a dedicated appliance. The customer has full access to the resources of the appliance (processors, memory, and so on), but access to device-level configuration is constrained to ensure IBM Cloud can effectively support the device.

The FSA is deployed in NAT mode and resides in two VLANs/networks within the public network infrastructure. The Outside VLAN is the IBM Cloud public VLAN where traffic enters the data center and is routed to the FSA. The inside VLAN is the customer's assigned protected public FCR (Frontend Customer Router) VLAN and is where the customer's server resources reside.  

IBM Cloud deploys the FSA with two bonded 1G interfaces on each of these two networks during the provisioning process. IBM Cloud also deploys a single interface for provisioning and maintenance of the device which is not made available to customers.

The firewall is deployed with all IPv4 and IPv6 traffic allowed, including a specific rule (softlayer-admin) designed to allow the IBM Cloud internal administration network to access devices through the firewall. Denial of Service protections and most other filters are configured not to enforce.