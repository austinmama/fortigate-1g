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

# Proteger el dispositivo de seguridad FortiGate

Puede configurar el dispositivo de seguridad FortiGate (FSA) de 1 Gbps para que cumpla con los requisitos de seguridad y conformidad. IBM Cloud proporciona una cuenta de administrador VDOM con una contraseña asignada aleatoriamente. Los clientes pueden rotar la contraseña, crear usuarios de solo lectura y restringir el acceso en función de los hosts de confianza, para que solo se acepte el tráfico de IP de origen especificadas (hasta tres). Para completar estas actividades:

1. Inicie sesión en el dispositivo utilizando las credenciales de la página **Detalles de dispositivo** en el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window}. Sigas las instrucciones de [Gestionar el dispositivo de seguridad FortiGate](managing-fsa.html) para obtener las credenciales.
2. Después de iniciar sesión en el dispositivo, vaya a **System > Admin > Administrators**. Se registran todos los accesos y los cambios.
3. Para configurar interfaces individuales, vaya a **System > Network > Interfaces**.

    Puede restringir el acceso a las interfaces administrativas a solo los protocolos que necesitan (normalmente, HTTPS y SSH, puesto que proporcionan cifrado en tránsito) o, para una mayor seguridad, puede inhabilitar el acceso externo a la interfaz administrativa. Esto se realiza habilitando los protocolos apropiados en la interfaz "interna" (la interfaz en la que reside la VLAN pública de un cliente) e inhabilitando todos los protocolos en la interfaz "externa" (la interfaz de la que se recibe el tráfico de Internet público). Esta medida de seguridad adicional requiere que el usuario tenga un servidor situado dentro de la VLAN desde el que administrar el FSA. 
