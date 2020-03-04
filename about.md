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

# About Fortigate Security Appliance 1 Gbps
{: #about-fortigate-security-appliance-1gbps}

A Fortigate Security Appliance 1 Gbps (FSA) is a dedicated single-tenant network device that is connected upstream from a server that protects any or all servers on a public VLAN. It is purchased separate from a server and can be added to a VLAN at any time. IBM© Cloud deploys the [Fortigate 1 Gbps ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://www.fortinet.com/sites/default/files/productdatasheets/FortiGate-300C.pdf){: new_window} within a Virtual Domain (VDOM) on the dedicated appliance. You have full access to that virtual domain without compromising the integrity of the device.
{: shortdesc}

With the FSA 1 Gbps, you have advanced features and the ability to fine-tune the device to a much higher degree than other products. The firewall blocks or shapes traffic before the traffic ever reaches the server. The main advantages are that a server handles 'good' traffic exclusively and that bandwidth can be constrained for less critical communications.

You can manage the FSA either through the web-based FortiOS GUI or the CLI (Command Line Interface) by using SSH. High availability can also be ordered, which provides two appliances in active-passive deployment with synchronized configurations.

Since monthly server bandwidth is recorded at the server switch port, traffic that is blocked by the FSA 1 Gbps is not counted against your monthly allotments. As a result, the need to pay for unwanted traffic is eliminated.

## Overview and features
{: #overview-and-features}

**Intended Use:** Single Public VLAN Protection

**User Interface:** Fortigate GUI and Command Line Interface

**Features:** Stateful Packet Inspection, VLAN Protection, Ingress Firewall Rules, Egress Firewall Rules, NAT, SSL VPN Termination, IPsec VPN Termination, Advanced Logging, High Availability (Optional)

**Throughput:** 1 Gbps (2 Gbps Aggregated)
