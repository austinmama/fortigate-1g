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

# Limitaciones conocidas de Fortigate Security Appliance 1Gbps
{: #known-limitations-of-fortigate-security-appliance-1gbps}

El dispositivo de seguridad FortiGate (FSA) de 1 Gbps tiene las siguientes limitaciones conocidas:

* No es compatible con Windows Network Load Balancing (NLB) debido a la forma en la que se procesa el ARP.

* La funcionalidad de migración tras error de alta disponibilidad no se expone al usuario. Si cortafuegos maestro no funciona correctamente, pero se realiza automáticamente la migración tras error, será necesaria una incidencia de soporte. Se recomienda supervisar los dispositivos de servicios esenciales para garantizar que los cortafuegos transfieren el tráfico adecuadamente.

* Un dispositivo de seguridad FortiGate no puede desplegarse en una VLAN que actualmente esté asociada con una pasarela de red, un cortafuegos de hardware u otro dispositivo de seguridad FortiGate.

* El dispositivo de seguridad FortiGate está asociado con una única VLAN de cliente pública (la VLAN "interna") y no puede acceder a la red privada.
