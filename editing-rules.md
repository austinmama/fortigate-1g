---

copyright:
  years: 2017
lastupdated: "2017-10-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Editing Rules

When the Firewall is first added to the VLAN, a set of rules is initially put in place that allows all traffic through the firewall. Rules can then be added to control the traffic.

Navigate to Network > IP Management > VLANs

Filter By "Primary Router: fcr" to view only your Public VLANs (optional)

Each row represents a VLAN in your infrastructure.  Click on the Firewall-vlanXXXX.networklayer.com link associated with the VLAN you want to manage.

Ensure the "Status" indicates that the firewall is "Processing All Rules."  Users can choose to bypass the rules in the event that implemented rules have an unintended impact on their environment by clicking "Bypass Rules" in this area.

To continue with editing rules, click on the "Rules" tab.

The page will display sections showing the current rules in effect for IPv4 and IPv6 addresses.  If no rules are implemented, a faded placeholder will be displayed.  If rules exist they can be edited by clicking on the corresponding row.  This list of rules is known as the 'working config'. A 'working config' is a set of rules that is in the process of being created but has not yet been applied to the Firewall. A user may edit, add, and delete rules until the rule set is completed.  Rules are displayed in the order in which they are processed with lower numbered rules having precedence over higher number rules (if rule 1 allows a packet through, rules 2 and beyond are not applied to the packet).

The fields are:

**Order:** The rule's order number. Rules can be moved up or down the list with the provided arrows and are enforced from top to bottom.

**Action:** 'permit' or 'deny' traffic matching this rule

**Source:** Can be either 'any' or a specific ip address or the network address for a specific subnet.

**CIDR:** Indicates the standard CIDR notation for the selected source.  "32" will implement the rule for a single IP while, for example, "24" will implement the rule for 256 IPs.

**Destination:** Can be either 'any' or a specific ip address or the network address for a specific subnet.

**CIDR:** Indicates the standard CIDR notation for the selected destination.

**Port Range:** These 2 fields indicate the range of ports (between 1 and 65535) that the rule will apply to.

**Protocol:** Selects the protocol the rule will apply to (TCP/GRE/ICMP/UDP/PPTP/AH/ESP)

## Common Ports

    FTP - 21
    SSH - 22
    Telnet - 23
    SMTP - 25
    DNS - 53
    HTTP - 80
    POP3 - 110
    IMAP - 143
    HTTPS - 443
    MSSQL - 1433
    MySQL - 3306
    Remote Desktop - 3389
    PostgreSQL - 5432
    VNC Web - 5800
    VNC Client - 5900
    Urchin - 9999 or 10000

## Applying Rules

Once the 'working config' is complete, press the 'Update Rules' button to have the 'working config' applied to the Firewall. The rules should take effect within 2 minutes.