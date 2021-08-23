---

copyright:
  years: 2017,2018
lastupdated: "2019-11-12"

keywords: faqs, questions, firewall, fortigate, traffic, public, private, bandwidth, ports, ip, vpn, nat, vlan

subcollection: fortigate-1g

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:faq: data-hd-content-type='faq'}
{:note: .note}
{:important: .important}
{:support: data-reuse='support'}

# FAQs for FortiGate Security Appliance 1 Gbps
{: #faqs-for-fortigate-security-appliance-1gbps}

The following are frequently asked questions when working with the FortiGate Security Appliance (FSA) 1 Gbps firewall.
{: shortdesc}

## What is a firewall?
{: faq}

A firewall is a network device that is connected upstream from a server. The firewall blocks unwanted traffic from a server before the server is reached.

## Why should I use a firewall?
{: faq}

The primary advantage of having a firewall is that your server handles “good” traffic exclusively. That means your resource is solely being used for its intended purpose as opposed to handling unwanted traffic, too.

## What firewall products does IBM© offer?
{: #products}
{: faq}
{: support}

You can find a detailed comparison of all firewall products that are offered in the IBM Cloud by reviewing [this topic](/docs/fortigate-10g?topic=fortigate-10g-exploring-firewalls).

## Is the FortiGate Security Appliance 1 Gbps compatible with IBM's load balancer products?
{: #load-balancing}
{: faq}
{: support}

Yes. The FSA 1 Gbps is compatible with the cloud load-balancing service, local load balancer, as well as the Citrix Netscaler VPX and MPX.

## Does public traffic pass through my load balancer or firewall first?
{: faq}

Coming from the public internet in, the load-balancing products are first. The Hardware Firewall products are next, and the NetScaler products are last (along with your servers).

## Does IBM charge for firewall bandwidth?
{: faq}

The FortiGate Security Appliance 1 Gbps is not metered for bandwidth. Additionally, the FSA can reduce total bandwidth utilization by limiting the traffic that servers must respond to.

## What are the grayed out ports in my Windows Firewall?
{: #greyed-ports}
{: faq}
{: support}

IBM Cloud offers many different services that you can use with your server including, Evault, SNMP and Nagios monitoring. These services require that IBM's internal systems communicate with your server to some degree. The disabled ports you see in the Exceptions list are ports open on the internal network port only. They are still blocked on the public (internet) network connection. Since the internal network is a secured network, having these ports open is considered secure.

These ports generally cannot be modified; however, if you reset the firewall rules, the ports are cleared from the Exceptions list. Be aware that resetting the firewall rules can have an adverse effect on these additional services and can cause other issues as well depending on your server configuration.

## What IP ranges do I allow through the firewall?
{: #ip}
{: faq}
{: support}

For the list of IP addresses and IP ranges to allow through the firewall, go [here](/docs/hardware-firewall-shared?topic=hardware-firewall-shared-ibm-cloud-ip-ranges).

## What is the maximum number of servers that the FortiGate Security Appliance 1 Gbps will protect?
{: #max-servers}
{: faq}
{: support}

The FortiGate Security Appliance 1 Gbps can protect every server on a Public VLAN. However it is important to note that since these firewall devices are connected with 2 Gbps Uplink, IBM recommends scaling the number of firewall instances to meet the performance needs of your application. You can do so by deploying extra public VLAN Firewalls within a pod to allow for additional firewall and associated compute resources to be added.

## What VPN options are included with each Firewall product?
{: #vpn}
{: faq}
{: support}

Not all firewalls offer VPN and not all VPN options are the same. The general options for VPN are:

* Each customer receives unlimited SSL VPN connections to IBM's private network. These connections can be established by clicking the VPN link at the top of the page while logged in to the Cloud Catalog console.
* IBM Cloud also offers a basic multi-tenant IPsec VPN service.
* The FortiGate Security Appliance 1 Gbps provides SSL and IPsec VPN options with Public network access only (no access to the IBM Cloud private network).
* The Network Gateway provides SSL, IPsec, and OpenVPN capabilities on the public or private network.
* The NetScaler products can provide SSL and IPsec VPN on the public or private network.
* Customers can also deploy a VPN solution on to a server within their IBM Cloud environment.

## When I select the High Availability option, what steps do I have to take to leverage this feature?
{: #ha}
{: faq}
{: support}

None. When ordered in HA, IBM Cloud automatically provisions the appliances in HA configuration. If the primary device fails, a secondary passive device takes over as the primary active instance and begin passing traffic. While this failover is typically automatic, it is best practice to monitor servers and ensure that traffic is being passed successfully.

## Which firewall products support public-to-private NAT and/or private VLAN segmentation?
{: #nat}
{: faq}
{: support}

None of the Hardware Firewall products have access to the private network. A Network Gateway is required to supply these capabilities inline and the NetScaler products have access to both the public and private networks.

## What are the default DNS servers of FortiGate 1 Gbps?
{: #default-dns-servers}
{: faq}
{: support}

By default, FortiGate 1 Gbps uses the following FortiGuard DNS servers:

* Primary: `208.91.112.53`
* Secondary: `208.91.112.52`
