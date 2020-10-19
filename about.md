---

copyright:
  years: 2017
lastupdated: "2019-11-12"

keywords: about, fortigate, fsa, features, overview, 1gbps

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
{:deprecated: .deprecated}

# About FortiGate Security Appliance 1 Gbps
{: #about-fortigate-security-appliance-1gbps}

A FortiGate Security Appliance 1 Gbps (FSA) is a dedicated single-tenant network device that is connected upstream from a server that protects any or all servers on a public VLAN. It is purchased separate from a server and can be added to a VLAN at any time. IBM© Cloud deploys the FortiGate 1 Gbps within a Virtual Domain (VDOM) on the dedicated appliance. You have full access to that virtual domain without compromising the integrity of the device.
{: shortdesc}

All instances of this service are deprecated. Existing instances can be used until it is no longer supported on 30 May 2021. Use one of the other available [firewall options](/docs/fortigate-1g?topic=fortigate-10g-exploring-firewalls) to get our latest security capabilities on IBM Cloud. For migration information, see [Migrating FortiGate Security Appliance 1Gbps](/docs/fortigate-1g?topic=fortigate-1g-migration-overview)
{: deprecated}

With the FSA 1 Gbps, you have advanced features and the ability to fine-tune the device to a much higher degree than other products. The firewall blocks or shapes traffic before the traffic ever reaches the server. The main advantages are that a server handles 'good' traffic exclusively and that bandwidth can be constrained for less critical communications.

You can manage the FSA either through the web-based FortiOS GUI or the CLI (Command Line Interface) by using SSH. High availability can also be ordered, which provides two appliances in active-passive deployment with synchronized configurations.

Since monthly server bandwidth is recorded at the server switch port, traffic that is blocked by the FSA 1 Gbps is not counted against your monthly allotments. As a result, the need to pay for unwanted traffic is eliminated.

## Overview and features
{: #overview-and-features}

**Intended Use:** Single Public VLAN Protection

**User Interface:** FortiGate GUI and Command Line Interface

**Features:** Stateful Packet Inspection, VLAN Protection, Ingress Firewall Rules, Egress Firewall Rules, NAT, SSL VPN Termination, IPsec VPN Termination, Advanced Logging, High Availability (Optional)

**Throughput:** 1 Gbps (2 Gbps Aggregated)
