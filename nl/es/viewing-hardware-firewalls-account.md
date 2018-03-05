---

copyright:
  years: 2017,2018
lastupdated: "2018-01-18"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Ver los cortafuegos

Para ver qué VLAN están protegidas con cortafuegos y obtener más detalles de los cortafuegos individuales, vaya a la página de VLAN.

1. En el navegador, abra el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} e inicie sesión en su cuenta.
2. En la navegación del Portal de clientes, seleccione **Red > Gestión de IP > VLAN**.

Cada fila de la tabla representa una VLAN en la infraestructura. IBM Cloud rellena la información de "Número de VLAN" y "Direccionador primario" automáticamente con el número exacto de VLAN y el direccionador en el que está configurada. El campo "Nombre" puede utilizarse para dar a la VLAN un nombre reconocible (como DMZ, Intranet, pública o base de datos).

La columna **Pasarela/cortafuegos** del extremo derecho contiene detalles sobre la protección de cortafuegos que hay establecida, por ejemplo:

- **Añadir cortafuegos** indica que no hay ningún cortafuegos establecido para los servidores de esta VLAN.
- **Servidores protegidos individualmente** indica que uno o varios servidores utilizan un cortafuegos de hardware (compartido) y que no hay establecido ningún cortafuegos de hardware (dedicado), dispositivo de seguridad FortiGate o pasarela de red. Las pasarelas de red y los cortafuegos de VLAN no se pueden establecer en una VLAN que tenga servidores protegidos individualmente.
- **Cortafuegos-vlanXXXX.networklayer.com** indica que hay establecido un cortafuegos de hardware (dedicado) o un dispositivo de seguridad FortiGate. Solo se puede asociar una pasarela de red o un cortafuegos de VLAN con una VLAN, pero un servidor puede estar protegido en la VLAN pública por un cortafuegos de VLAN y asociado en la red privada con una pasarela de red.
- **Nombre de pasarela** indica la pasarela de red con la que está asociada la VLAN.

## Detalles de servidores protegidos individualmente

Para VLAN que tienen **Servidores protegidos individualmente** en el campo **Pasarela/cortafuegos**, puede pulsar en el enlace del número de VLAN asociada para visualizar los detalles de la VLAN, incluidos los dispositivos asociados.

En la lista de dispositivos asociados, puede pulsar en cada dispositivo y desplazarse hasta la parte inferior del separador Configuración. Verá **Cortafuegos** en la sección Complementos con el valor **Instalado** o **No instalado** en el estado.

- **No instalado** indica que no hay ningún cortafuegos establecido para ese dispositivo. 
- **Instalado** indica que hay un cortafuegos establecido, y habrá un separador **Cortafuegos** disponible en el dispositivo, donde podrá gestionar la configuración del cortafuegos.

## Detalles del cortafuegos dedicado

Para VLAN que tienen **Cortafuegos-vlanXXXX.networklayer.com** en el campo **Pasarela/cortafuegos**, puede pulsar en el enlace de ese cortafuegos para visualizar los detalles del cortafuegos. Los detalles del dispositivo incluyen el direccionador asociado, la VLAN, las subredes IPv4/IPv6, los dispositivos asociados con la VLAN y los controles para direccionar el tráfico a través del cortafuegos o sortear el cortafuegos.

Los dispositivos de seguridad FortiGate tendrán la IP de gestión, el nombre de usuario y la contraseña. La gestión de los dispositivos de seguridad FortiGate se completa mediante su propia GUI o consola basada en SSH.

## Detalles de pasarela de red

Para VLAN que tienen un nombre de dispositivo de pasarela de red en el campo **Pasarela/cortafuegos**, puede pulsar en el enlace del nombre de pasarela de red para visualizar los detalles de la pasarela de red. Los detalles del dispositivo incluyen las opciones de gestión de la pasarela de red y las VLAN frontal (FCR) y de fondo (BCR) asociadas.
