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

# Setting up a FortiGate Firewall Rule to only allow a specific IP Subnet to access your web servers

You can configure a FortiGate Firewall rule to only allow access to your protected web server from a specific Subnet or IP.

1. Login to the FortiGate Device. The login link and details can be found on the Device Details Screen under the section labeled ‘Management’​.
* Navigate to **Policy > Policy**, and click **Create New**.
* To create a rule that will only allow traffic to your servers from a specific IP, enter the following configurations:
    * Source Interface/Zone = v###-outside
    * Source Address = The IP Address and Subnet of the IP’s you want to allow. Address can be entered in two different formats: 10.10.20.[1-14] or 10.10.20.1/255.255.255.240.
    * Destination Interface/Zone  = v###-inside
    * Destination Address = The specific IP / IP’s of the server you wish to give access to, if you want to give access to any of your web servers you can select ‘all’.
    * Service = The Service type such as HTTP, SSH, SMB, DHCP to allow.  If their no specific service you can select ‘ANY’ to allow all services per this rule.
    * Action = ACCEPT
    * Click OK to save the rule
    * Test your rule with by using the command ping and a servers IP address to confirm if you can access the server from an Allowed Address and from a Denied Address.
        * An Allowed Address will receive a response and a Denied Address should receive a ‘Request timed out.’ Message.
        * If the policy is not applying the rule as expected you may need to adjust the Sequence of your rules as the Sequence of the Policy Rules are applied Top to Bottom.
