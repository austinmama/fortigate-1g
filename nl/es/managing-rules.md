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

# Gestionar reglas de cortafuegos (políticas)

FortiGate utiliza el concepto de "política", que incluye la capacidad para aceptar/denegar tráfico, aplicar perfiles de seguridad, configurar tráfico, registrar tráfico y planificar un periodo de tiempo calendario para aplicar una política. Para ensamblar una política, primero debe crear los objetos que participarán en ella. 

1. Inicie sesión en el dispositivo utilizando las credenciales de la página **Detalles de dispositivo** en el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window}. Sigas las instrucciones de [Gestionar el dispositivo de seguridad FortiGate](managing-fsa.html) para obtener las credenciales.
2. Después de iniciar sesión en el dispositivo, vaya al menú **Policy and Objects** y seleccione el protocolo que desee gestionar (como IPv4 o IPv6). Las políticas se implementan contra el tráfico en función del número de secuencia, en el extremo izquierdo. Los usuarios pueden arrastrar una política hacia arriba de la lista para que se implemente antes, o viceversa.
3. Para añadir una política, pulse **Create New** y consulte estas definiciones de campo:

    **Incoming Interface:** la interfaz destinada al público (interfaz externa) para las reglas de ingreso o la interfaz destinada al cálculo (interfaz interna) para las reglas de salida.

    **Source Address:** la(s) IP de origen para el tráfico. La IP se debe añadir a la lista "Addresses" en "Objects Menu". Tenga en cuenta que hay disponible una opción "All".

    **Source User(s):** aplica la política a un usuario o grupo creado en el panel "User and Device".

    **Source Device Type:** aplica la política a un dispositivo creado en el panel "User and Device".

    **Destination Address:** la(s) IP de destino del tráfico. La IP se debe añadir a la lista "Addresses" en "Objects Menu". Tenga en cuenta que hay disponible una opción "All".

    **Schedule:** determina cuándo se ejecutará la política. Hay disponible una opción "Always". También puede crear una planificación en el menú de objetos bajo Schedules.

    **Service:** determina el servicio al que se aplicará la política. Hay disponible una opción "ALL", además de muchos servicios estándar. Se pueden añadir servicios adicionales en el menú Services bajo Objects.

    **Action:** acepta o deniega el tráfico. 

    **Firewall / Network Options:** habilita o inhabilita la NAT y sus opciones asociadas.

    **Security Profiles:** proporciona un conmutador On/Off para cada opción y permite la asociación al perfil.

    **Traffic Shaping:** permite configurar el ancho de banda máximo y garantizado (mínimo) disponible para el tráfico. También puede establecerse un límite máximo de conexiones por IP. 

    Los valores de DSCP no son eficaces, ya que la plataforma IBM Cloud ignora la información de calidad de servicio generada.

    **Logging Options:** configura cuándo se registra el tráfico permitido. Este valor (y especialmente la opción "Capture Packets") utiliza recursos de dispositivo.

    **Comments:** comentarios generados por el usuario.

    **Enable this policy:** habilita o inhabilita la política.

## Ejemplo de una regla simple "Allow All" para el tráfico web a un servidor web

***Incoming Interface:*** *outside VLAN*

***Source Address:*** *All*

***Source User(s):** *Vacío*

***Source Device Type:*** *Vacío*

***Outgoing Interface:*** *inside VLAN*

***Destination Address:*** *x.x.x.x (IP del servidor web)*

***Schedule:*** *always*

***Service:*** *HTTP*

***Action:*** *ACCEPT*

***NAT:*** *OFF*

***Security Profiles:*** *Use Standard*

***Traffic Shaping:*** *Off*

***Log Allowed Traffic:*** *On (sucesos de seguridad)*

***Comments:*** *Web Server Traffic x.x.x.x*

***Enable this policy:*** *On*
