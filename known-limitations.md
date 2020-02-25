---

copyright:
  years: 2017
lastupdated: "2019-11-12"

keywords: known, limitations, problems, nlb, fsa

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

# Known Limitations of Fortigate Security Appliance 1 Gbps
{: #known-limitations-of-fortigate-security-appliance-1gbps}

There are some limitations to be aware of using your FortiGate Security Appliance (FSA) 1 Gbps.
{: shortdesc}

* Incompatible with Windows Network Load Balancing (NLB) due to the way ARP is processed.

* High Availability fail over functionality is not exposed to the user. If the master firewall malfunctions, but does not fail over automatically, a support case is required. Device monitoring for critical services is recommended to ensure that firewalls are passing traffic.

* A FortiGate Security Appliance cannot be deployed on a VLAN that is associated with a Network Gateway, Hardware Firewall, or another FortiGate Security Appliance.

* The FortiGate Security Appliance is associated with a single public customer VLAN (the "inside" VLAN) and cannot access the private network.
