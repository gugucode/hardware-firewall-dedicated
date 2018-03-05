---

copyright:
  years: 2017,2018
lastupdated: "2018-01-19"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Añadir un cortafuegos de hardware (dedicado) a una VLAN pública

Un cortafuegos de hardware (dedicado) no se puede incluir como parte de un pedido de servidor, y se debe realizar una vez que se haya establecido al menos un nodo de cálculo público y que se haya añadido la VLAN asociada.

Para añadir protección a una VLAN, pida un cortafuegos de hardware (dedicado) desde la página de VLAN:

1. En el navegador, abra el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono ce enlace externo")](https://control.softlayer.com/){: new_window} e inicie sesión en su cuenta.
2. En la navegación del Portal de clientes, seleccione **Red > Gestión de IP > VLAN** para ir a la página de VLAN. Cada fila representa una VLAN en la infraestructura. IBM Cloud rellena la información de "Número de VLAN" y "Direccionador primario" automáticamente con el número exacto de VLAN y el direccionador en el que está configurada. El campo "Nombre" puede utilizarse para definir un nombre reconocible. La columna "Pasarela/cortafuegos" del extremo derecho contiene detalles sobre la protección de cortafuegos, si la hay, que hay establecida para dicha VLAN. 

	**Consejo:** para filtrar la tabla de VLAN para mostrar solo las VLAN públicas, pulse el separador **Filtro**, especifique "fcr" en el campo Direccionador primario y pulse el botón **Filtro**.
3. Busque la VLAN que desea proteger y pulse el enlace **Añadir cortafuegos** en la misma fila. Este enlace abre la página **Pedir cortafuegos de hardware (dedicado)**. Si la columna "Pasarela/cortafuegos" ya está llena, ya hay un cortafuegos o una pasarela de red asociada con la VLAN, y el dispositivo se debe eliminar para poder continuar.
4. Seleccione **Cortafuegos de hardware (dedicado)** o **Cortafuegos de hardware (alta disponibilidad)**. 

	La opción de alta disponibilidad despliega el mismo hardware e interfaz, pero despliega un segundo nodo pasivo para continuar el proceso de tráfico si el nodo activo falla. La alta disponibilidad reduce el riesgo de tiempo de inactividad excesivo. 

5. Pulse el botón **Servidores en esta VLAN** para verificar que está seleccionando la VLAN apropiada.
6. Escriba su opción de pago y pulse **Continuar**.
7. En la pantalla siguiente, especifique los códigos promocionales si procede, lea y acepte el Acuerdo de servicio maestro y pulse **Realizar pedidos**. 
