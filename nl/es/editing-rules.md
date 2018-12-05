---

copyright:
  years: 2017,2018
lastupdated: "2018-11-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Configurar el cortafuegos de hardware (dedicado)

Cuando se añade un cortafuegos a la VLAN por primera vez, se ponen en práctica una serie de reglas que permiten que todo el tráfico pase a través del cortafuegos. La configuración del cortafuegos es tan sencilla como crear un conjunto de reglas para permitir el acceso a determinados puertos/direcciones IP de direcciones de Internet específicas y denegar el tráfico de otras fuentes.

## Editar reglas

Para editar las reglas de cortafuegos:

1. En el navegador, abra el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono ce enlace externo")](https://control.softlayer.com/){: new_window} e inicie sesión en su cuenta.
2. En la navegación del Portal de clientes, seleccione **Red > Gestión de IP > VLAN**. Cada fila representa una VLAN en la infraestructura.  Pulse el enlace Cortafuegos-vlanXXXX.networklayer.com asociado con la VLAN que desea gestionar para llevarle a la página **Detalles de dispositivo**. Asegúrese de que en el "Estado" se indica que el cortafuegos está "Procesando todas las reglas".  Los usuarios pueden optar por ignorar las reglas, en caso de que las reglas aplicadas tengan un impacto no deseado en su entorno, pulsando "Ignorar reglas" en esta área.
3. Para empezar a actualizar las reglas, pulse el separador **Reglas**. La página mostrará las secciones que muestran las reglas actuales en vigor para direcciones IPv4 e IPv6.  Si no hay reglas implementadas, aparecerá un marcador sin color.  Edite reglas individuales pulsando en la fila correspondiente.  Esta lista de reglas se conoce como "configuración operativa". Una "configuración operativa" es un conjunto de reglas que está en proceso de creación pero que todavía no se han aplicado al cortafuegos. Un usuario puede editar, añadir y suprimir reglas hasta que el conjunto de reglas se haya completado.  Las reglas se visualizan en el orden en el que se procesan, y las reglas con números más bajos tienen prioridad sobre las reglas con números más altos (si la regla número 1 permite que un paquete pase, las reglas número 2 en adelante no se aplican al paquete).
4. Pulse una regla para editarla o pulse el signo más en la parte inferior de la tabla para añadir otra regla. Al pulsar el icono menos, se suprimirá la regla. Las reglas se validan automáticamente a medida que se especifican.

    Los campos son:

    **Orden:** el número de orden de la regla. Las reglas se pueden mover hacia arriba o hacia abajo con las flechas, y se aplican de arriba a abajo.

    **Acción:** 'permitir' o 'denegar' el tráfico que coincida con esta regla

    **Origen**: puede ser 'todos' o una dirección IP específica o la dirección de red para una subred específica.

    **CIDR**: indica la notación CIDR estándar para el origen seleccionado.  "32" implementará la regla para una sola IP, por ejemplo, y "24" implementará la regla para 256 IP.

    **Destino**: puede ser 'todos' o una dirección IP específica o la dirección de red para una subred específica.

    **CIDR**: indica la notación CIDR estándar para el destino seleccionado.

    **Rango de puertos**: estos dos campos indican el rango de puertos (entre 1 y 65535) a los que se aplicará la regla.

    **Protocolo:** selecciona el protocolo al que se aplicará la regla (TCP/GRE/ICMP/UDP/PPTP/AH/ESP)

    **Notas:** campo libre para entrar cualquier nota sobre esta regla.
    
5. Una vez que la 'configuración operativa' se haya completado, pulse el botón **Actualizar reglas** para aplicar la 'configuración operativa' al cortafuegos. Las reglas se aplicarán pasados dos minutos.

## Puertos comunes

| Protocolo | Puerto |
| :-----: | :-----: |
| FTP | 21 |
| SSH | 22 |
| Telnet | 23 |
| SMTP | 25 |
| DNS | 53 |
| HTTP | 80 |
| POP3 | 110 |
| IMAP | 143 |
| HTTPS | 443 |
| MSSQL | 1433 |
| MySQL | 3306 |
| Remote Desktop | 3389 |
| PostgreSQL | 5432 |
| VNC Web | 5800 |
| VNC Client | 5900 |
| Urchin | 9999 o 10000 ||
