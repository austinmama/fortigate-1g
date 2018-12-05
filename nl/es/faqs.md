---

copyright:
  years: 2017,2018
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:faq: data-hd-content-type='faq'}

# Preguntas más frecuentes

Las preguntas siguientes son las más frecuentes cuando se trabaja con el cortafuegos dispositivo de seguridad FortiGate (FSA) de 1 Gbps.

## ¿Qué es un cortafuegos?
{:faq}

Un cortafuegos es un dispositivo de red que está conectado en sentido ascendente desde un servidor. El cortafuegos bloquea el tráfico no deseado de un servidor antes de que llegue al servidor.

## ¿Por qué debo utilizar un cortafuegos?
{:faq}

La principal ventaja de tener un cortafuegos es que el servidor sólo tiene que manejar el tráfico "bueno", lo que significa que el recurso se va a utilizar únicamente para su propósito previsto, en lugar de manejar también el tráfico no deseado.

## ¿Qué productos de cortafuegos ofrece IBM?
{:faq}

Para ver una comparación detallada de todos los productos de cortafuegos que se ofrecen en IBM Cloud, consulte este [tema ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](/docs/infrastructure/fortigate-10g/explore-firewalls.html#explore-firewalls){: new_window}. 

## ¿Es compatible el dispositivo de seguridad FortiGate de 1 Gbps con los productos de equilibrador de carga de IBM?
{:faq}

Sí. El FSA de 1 Gbps es compatible con el servicio de equilibrio de carga en la nube, el equilibrador de carga local y Citrix Netscaler VPX y MPX.

## El tráfico público, ¿pasa primero por el equilibrador de carga o por el cortafuegos?
{:faq}

Cuando procede de Internet público, los productos de equilibrio de carga van primero, después los productos de cortafuegos de hardware, y por último los productos de NetScaler (junto con los servidores de los clientes).

## ¿Cobra IBM el ancho de banda del cortafuegos?
{:faq}

El dispositivo de seguridad FortiGate de 1 Gbps no se mide por ancho de banda. Además, el FSA puede pueden reducir el uso total de ancho de banda limitando el tráfico al que deben responder los servidores.
{:faq}

## ¿Qué son los puertos inactivos en el cortafuegos de Windows?
{:faq}

IBM Cloud ofrece muchos servicios diferentes que puede utilizar con el servidor, como supervisión de Evault, SNMP y Nagios. Estos servicios requieren que nuestros sistemas internos se comuniquen con el servidor en cierta medida. Los puertos inactivos que se ven en la lista de excepciones son puertos abiertos solo en el puerto de red interno. Siguen bloqueados en la conexión de red pública (a Internet). Puesto que la red interna es una red protegida, tener estos puertos abiertos se considera seguro.

Por lo general, estos puertos no se pueden modificar; sin embargo, si restablece las reglas de cortafuegos, los puertos se eliminarán de la lista de excepciones. Tenga en cuenta que restablecer las reglas de cortafuegos puede afectar negativamente a estos servicios adicionales y puede producir otros problemas en función de la configuración del servidor.

## ¿Qué rangos de IP puedo permitir a través del cortafuegos?
{:faq}

Para consultar la lista de direcciones IP y los rangos IP que se pueden permitir a través del cortafuegos, vaya [aquí](/docs/infrastructure/hardware-firewall-dedicated/ips.html){: new_window}. 

## ¿Cuál es el número máximo de servidores que protege el dispositivo de seguridad FortiGate de 1 Gbps?
{:faq}

El dispositivo de seguridad FortiGate de 1 Gbps puede proteger cualquier servidor de una VLAN pública. Sin embargo, cabe mencionar que, puesto que estos dispositivos de cortafuegos se conectan con enlace ascendente de 2 Gbps, se recomienda escalar el número de instancias de cortafuegos para responder a las necesidades de rendimiento de la aplicación. Puede hacerlo mediante el despliegue de cortafuegos adicionales de VLAN pública en un pod para que se puedan añadir más cortafuegos y recursos de cálculo asociados.

## ¿Qué opciones de VPN se incluyen con cada producto de cortafuegos?
{:faq}

No todos los cortafuegos ofrecen VPN y no todas las opciones de VPN son las mismas. Las opciones generales para VPN son:

* Cada cliente recibe conexiones ilimitadas VPN con SSL a nuestra red privada. Estas conexiones pueden establecerse pulsando el enlace de VPN en la parte superior de la página, con la sesión iniciada en el Portal de clientes.
* Los clientes también reciben una VPN PPTP por cuenta. Pueden añadir más usuarios de VPN PPTP a su cuenta en paquetes de 5 por 5 USD/mes adicionales.
* IBM Cloud también ofrece un servicio de VPN IPSec multiarrendatario básico.
* El dispositivo de seguridad FortiGate de 1 Gbps proporciona opciones de VPN IPSec y SSL con acceso sólo a la red pública (sin acceso a la red privada de IBM Cloud).
* La pasarela de red proporciona funciones SSL, IPSec y OpenVPN en la red pública o privada.
* Los productos NetScaler pueden proporcionar VPN IPSec y SSL en la red pública o privada.
* Los clientes también pueden desplegar una solución VPN en un servidor dentro de su entorno de IBM Cloud.

## Cuando selecciono la opción de alta disponibilidad, ¿qué pasos debo seguir para utilizar esta característica?
{:faq}

Ninguno. Cuando se realizan los pedidos en alta disponibilidad, IBM Cloud suministra automáticamente los dispositivos en configuración de alta disponibilidad.  En el caso de que el dispositivo primario falle, un dispositivo pasivo secundario continuará como instancia activa primaria y empezará a transferir el tráfico. Aunque esta migración tras error suele ser automática, es recomendable supervisar los servidores y verificar que el tráfico se transmite satisfactoriamente.

## ¿Qué productos de cortafuegos son compatibles con la segmentación de VLAN privada o NAT pública a privada?
{:faq}

Ninguno de los productos de cortafuegos de hardware tiene acceso a la red privada.  Se necesita una pasarela de red para proporcionar estas funciones incorporadas y que los productos NetScaler tengan acceso a las redes públicas y privadas.
