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

# Gestionar el dispositivo de seguridad FortiGate

Cuando se añade el cortafuegos a la VLAN por primera vez, se permite todo el tráfico. Debe añadir reglas al cortafuegos para poder controlar el tráfico. 

1. En el navegador, abra el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} e inicie sesión en su cuenta.
2. En la navegación del Portal de clientes, seleccione **Red > Gestión de IP > VLAN**. 

	**Sugerencia:** para ver sólo las VLAN públicas, pulse el desplegable **Filtro** y escriba ``fcr`` en el **Direccionador primario**.
3. Desplácese a la VLAN que desea gestionar y pulse el enlace del nombre de cortafuegos en la columna **PASARELA/CORTAFUEGOS** para ir a la página **Detalles de dispositivo**.
4. En la página **Detalles de dispositivo**, puede ver las subredes asociadas, el "Estado" actual de direccionamiento del cortafuegos y la información de gestión. 

	La información de gestión incluye una **IP de gestión**, un **Nombre de usuario**y una **Contraseña**. Esta IP de gestión es de acceso público de forma predeterminada. Para casos prácticos avanzados o casos de automatización, la administración también está disponible mediante SSH con las mismas credenciales e IP.
5. Para acceder a la GUI, pulse el enlace de IP de gestión y especifique el nombre de usuario y la contraseña proporcionados. 
6. En la interfaz de gestión, puede gestionar el dispositivo de seguridad FortiGate como administrador VDOM. Para las funciones de gestión no disponibles mediante la interfaz de gestión, como gestionar certificados SSL, iniciar una migración tras error de alta disponibilidad manual, reiniciar, actualizar o realizar una restauración de la configuración predeterminada, se debe abrir una incidencia de soporte.

Fortinet dispone de [documentación en línea, incluido un cookbook interactivo ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://cookbook.fortinet.com/fortigate/){: new_window} que se puede utilizar como referencia durante la configuración.
