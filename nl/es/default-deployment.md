---

copyright:
  years: 2017
lastupdated: "2017-11-29"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Despliegue predeterminado

El dispositivo de seguridad FortiGate (FSA) de 1 Gbps se despliega como un solo dominio virtual (normalmente firewall001) en un dispositivo dedicado. El cliente tiene acceso completo a los recursos del dispositivo (procesadores, memoria, etc.), pero el acceso a la configuración a nivel de dispositivo está limitado para asegurarse de que IBM Cloud pueda dar soporte al dispositivo de forma eficaz.

El FSA se despliega en modalidad NAT y reside en dos VLAN/redes en la infraestructura de red pública. La VLAN externa es la VLAN pública de IBM Cloud por donde el tráfico entra al centro de datos y se direcciona al FSA. La VLAN interna es la VLAN FCR (direccionador de cliente frontal) pública protegida asignada del cliente y es donde residen los recursos de servidor del cliente.  

IBM Cloud despliega el FSA con dos interfaces de 1 G vinculadas en cada una de estas dos redes durante el proceso de suministro. IBM Cloud también despliega una interfaz única para el suministro y el mantenimiento del dispositivo que no está disponible para los clientes.

El cortafuegos se despliega con todo el tráfico IPv4 e IPv6 permitido, incluida una regla específica (softlayer-admin) diseñada para permitir que la red de administración interna de IBM Cloud acceda a los dispositivos a través del cortafuegos. Las protecciones contra denegación de servicio y muchos otros filtros están configurados para no aplicarse.
