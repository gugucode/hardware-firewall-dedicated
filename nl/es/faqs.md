---

copyright:
  years: 2017
lastupdated: "2018-11-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:faq: data-hd-content-type='faq'}

# Preguntas más frecuentes del cortafuegos de hardware (dedicado)
{: #faqs-for-hardware-firewall-dedicated-}

Las siguientes son las preguntas más frecuentes cuando se trabaja con el cortafuegos del dispositivo de seguridad Fortigate 1 g.

## ¿Qué es un cortafuegos?
{:faq}

Un cortafuegos es un dispositivo de red que está conectado en sentido ascendente desde un servidor. El cortafuegos bloquea el tráfico no deseado de un servidor antes de que llegue al servidor.

## ¿Por qué debo utilizar un cortafuegos?
{:faq}

La principal ventaja de tener un cortafuegos es que el servidor sólo tiene que manejar el tráfico "bueno", lo que significa que el recurso se va a utilizar únicamente para su propósito previsto, en lugar de manejar también el tráfico no deseado.

## ¿Qué productos de cortafuegos ofrece IBM©?
{:faq}

Para ver una comparación detallada de todos los productos de cortafuegos que se ofrecen en IBM Cloud, consulte este [tema](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-exploring-firewalls). 

## El cortafuegos de hardware (dedicado), ¿es compatible con productos de equilibrador de carga de IBM?
{:faq}

Sí. El cortafuegos de hardware (dedicado) es compatible con los equilibradores de carga dedicados y estándar, así como Citrix Netscaler VPX y MPX.

## ¿Puedo tener un cortafuegos de hardware dedicado y una pasarela de red asociados con la misma VLAN?
{:faq}

No, no es posible tener un servicio de cortafuegos (compartido o dedicado) y un dispositivo de pasarela de red asignados a la misma VLAN. 

## El tráfico público, ¿pasa primero por el equilibrador de carga o por el cortafuegos de hardware?
{:faq}

Cuando procede de Internet público, los productos de equilibrador de carga local, equilibrador de carga dedicado o equilibrador de carga empresarial van primero, después los productos de cortafuegos de hardware, y por último los productos de NetScaler (junto con los servidores de los clientes).

## ¿Cobra SoftLayer el ancho de banda del cortafuegos?
{:faq}

El cortafuegos de hardware (compartido), el cortafuegos de hardware (dedicado) y el dispositivo de seguridad Fortigate no se miden por ancho de banda.  Además, estos productos pueden reducir el uso total de ancho de banda limitando el tráfico al que deben responder los servidores.

## ¿Qué son los puertos inactivos en el cortafuegos de Windows?
{:faq}

SoftLayer ofrece muchos servicios diferentes que puede utilizar con el servidor, como supervisión de Evault, SNMP y Nagios. Estos servicios requieren que nuestros sistemas internos se comuniquen con el servidor en cierta medida. Los puertos inactivos que se ven en la lista de excepciones son puertos abiertos solo en el puerto de red interno. Siguen bloqueados en la conexión de red pública (a Internet). Puesto que la red interna es una red protegida, tener estos puertos abiertos se considera seguro.

Por lo general, estos puertos generalmente no se pueden modificar; sin embargo, si restablece las reglas de cortafuegos, se eliminarán de la lista de excepciones. Tenga en cuenta que restablecer las reglas de cortafuegos no solo puede afectar negativamente a estos servicios adicionales, sino que también puede producir otros problemas con el servidor, en función de su configuración actual.

## ¿Qué opciones de cortafuegos de hardware están disponibles para servidores a 10 Gbps?
{:faq}

Si 10 Gbps solo se necesita en la red privada (para la base de datos, la copia de seguridad, el almacenamiento, etc.), los clientes pueden solicitar que se degraden solo los enlaces ascendentes públicos y pedir alguno de los otros productos de cortafuegos de hardware. Si se necesita 10 Gbps en la red pública, se necesitan una pasarela de red o un dispositivo de seguridad Fortigate Seguridad de 10 Gbps.

## ¿Qué rangos de IP puedo permitir a través del cortafuegos?
{:faq}

Para consultar la lista de direcciones IP y los rangos IP que se pueden permitir a través del cortafuegos, vaya [aquí](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-ibm-cloud-ip-ranges). 

## ¿Cuál es el número máximo de servidores que protegen el cortafuegos de hardware (dedicado) o el dispositivo de seguridad Fortigate?
{:faq}

Tanto el cortafuegos de hardware dedicado como el dispositivo de seguridad Fortigate pueden proteger a todos los servidores de una VLAN pública.  Sin embargo, cabe mencionar que, puesto que estos dispositivos FW se conectan con enlace ascendente de 2 Gbps, se recomienda escalar el número de instancias de cortafuegos para responder a las necesidades de rendimiento de la app. Los clientes pueden hacerlo mediante el despliegue de cortafuegos adicionales de VLAN pública en un pod para que se puedan más cortafuegos y recursos de cálculo asociados.

## ¿Qué opciones de VPN se incluyen con cada producto de cortafuegos?
{:faq}

No todos los cortafuegos ofrecen VPN y no todas las opciones de VPN son las mismas.  Las opciones generales para VPN son:

* Cada cliente recibe conexiones ilimitadas VPN con SSL a nuestra red privada. Estas conexiones pueden establecerse pulsando el enlace de VPN en la parte superior de la página, con la sesión iniciada en el portal de clientes.
* Los clientes también reciben una VPN PPTP por cuenta. Pueden añadir más usuarios de VPN PPTP a su cuenta en paquetes de 5 por 5 USD/mes adicionales.
* SoftLayer también ofrece un servicio de VPN IPSec multiarrendatario básico a partir de 99 USD/mes.
* El dispositivo de seguridad Fortigate proporciona opciones de VPN IPSec y SSL con acceso sólo a la red pública (sin acceso a la red privada de SoftLayer).
* La pasarela de red proporciona funciones SSL, IPSec y OpenVPN en la red pública o privada.
* Los productos NetScaler pueden proporcionar VPN IPSec y SSL en la red pública o privada.
* Los clientes también pueden desplegar una solución VPN en un servidor dentro de su entorno de SoftLayer.

## Cuando selecciono la opción de alta disponibilidad para el cortafuegos de hardware (dedicado) o el dispositivo de seguridad Fortigate, ¿qué pasos debo seguir para utilizar esta característica?
{:faq}

Ninguno. Cuando se realizan los pedidos en alta disponibilidad, SoftLayer suministra automáticamente los dispositivos en configuración de alta disponibilidad.  En el caso de que el dispositivo primario falle, un dispositivo pasivo secundario continuará como instancia activa primaria y empezará a transferir el tráfico.  Aunque esta migración tras error suele ser automática, es recomendable supervisar los servidores y verificar que el tráfico se transmite satisfactoriamente.

## ¿Qué productos de cortafuegos son compatibles con la segmentación de VLAN privada o NAT pública a privada?
{:faq}

Los dispositivos de seguridad Fortigate de 10 Gbps son compatibles con la segmentación de VLAN privada y NAT pública a privada. 
