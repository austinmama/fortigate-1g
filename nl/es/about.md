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

# Acerca de Fortigate Security Appliance 1Gbps
{: #about-fortigate-security-appliance-1gbps}

Un dispositivo de seguridad Fortigate de 1 Gbps (FSA) es un dispositivo de red dedicado de un solo arrendatario conectado de forma ascendente desde un servidor que protege cualquier servidor (o todos) de una VLAN pública. Se adquiere por separado del servidor y se puede añadir a una VLAN en cualquier momento.  IBM© Cloud despliega el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://www.fortinet.com/sites/default/files/productdatasheets/FortiGate-300C.pdf){: new_window} dentro de un dominio virtual (VDOM) en el dispositivo dedicado, permitiendo a los clientes un acceso completo a ese dominio virtual sin comprometer la integridad del dispositivo. 

Con el FSA de 1 Gbps, los clientes tienen acceso a funciones avanzadas y la capacidad de ajustar el dispositivo en un grado mucho mayor que otros productos. El cortafuegos bloquea o configura el tráfico antes de que llegue al servidor. Las ventajas principales son que el servidor sólo tiene que manejar el tráfico 'bueno' y que el ancho de banda se puede limitar a las comunicaciones menos críticas. 

Los clientes pueden gestionar el FSA a través de la GUI de FortiOS basada en web o la CLI (interfaz de línea de mandatos) con SSH. También se puede pedir alta disponibilidad, que proporciona dos dispositivos en despliegue activo-pasivo con configuraciones sincronizadas.

Puesto que el ancho de banda mensual del servidor se registra en el puerto de conmutador del servidor, el tráfico bloqueado por el FSA de 1 Gbps no cuenta para la asignación mensual, y así no es necesario pagar por el tráfico no deseado.

## Visión general y características

**Uso previsto:** protección de VLAN pública única

**Interfaz de usuario:** GUI de Fortigate e interfaz de línea de mandatos

**Características:** inspección de paquete con estado, protección de VLAN, reglas de cortafuegos de ingreso, reglas de cortafuegos de salida, NAT, terminación de VPN con SSL VPN, terminación de VPN IPSec, registro avanzado, alta disponibilidad (opcional)

**Rendimiento:** 1 Gbps (2 Gbps agregados)
