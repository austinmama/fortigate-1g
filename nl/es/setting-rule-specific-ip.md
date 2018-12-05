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

# Configuración de una regla de cortafuegos FortiGate para permitir el acceso a los servidores web únicamente a una subred de IP específica

Puede configurar una regla de cortafuegos FortiGate para permitir el acceso al servidor web protegido únicamente desde una subred o IP específica.

1. Inicie sesión en el dispositivo FortiGate. El enlace de inicio de sesión y los detalles se pueden encontrar en la pantalla Detalles de dispositivo bajo la sección 'Gestión'.
* Navegue a **Policy > Policy** y pulse **Create New**.
* Para crear una regla que solo permita el tráfico a los servidores desde una dirección IP específica, especifique las siguientes configuraciones:
    * Source Interface/Zone = v###-outside
    * Source Address = la dirección IP y la subred de la IP que desea permitir. La dirección puede especificarse en dos formatos diferentes: 10.10.20.[1-14] o 10.10.20.1/255.255.255.240.
    * Destination Interface/Zone  = v###-inside
    * Destination Address = la(s) IP específica(s) del servidor al que desee dar acceso, si desea dar acceso a cualquiera de los servidores web, seleccione 'all'.
    * Service = el tipo de servicio, como HTTP, SSH, SMB, DHCP que desea permitir.  Si no hay ningún servicio específico, puede seleccionar 'ANY' para permitir todos los servicios con esta regla.
    * Action = ACCEPT
    * Pulse OK para guardar la regla
    * Pruebe la regla mediante el mandato ping y una dirección IP de servidor para confirmar si puede acceder al servidor desde una dirección permitida y desde una dirección denegada.
        * La dirección permitida recibirá una respuesta, y la dirección denegada debería recibir un mensaje de tiempo de espera de solicitud excedido. Mensaje.
        * Si la política no aplica la regla como se esperaba, puede que necesite ajustar la secuencia de las reglas, ya que la secuencia de las reglas de política se aplica de arriba a abajo.
