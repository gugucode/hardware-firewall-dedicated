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

# Häufig gestellte Fragen
Die folgenden Fragen sind häufig gestellte Fragen zur FortiGate Security Appliance-Firewall (1g).

## Was ist eine Firewall?
{:faq}

Eine Firewall ist ein Netzgerät, das einem Server vorgeschaltet ist. Die Firewall blockiert unerwünschten Datenverkehr von einem Server, bevor der Server erreicht wird.

## Warum wird eine Firewall empfohlen?
{:faq}

Der Hauptvorteil einer Firewall besteht darin, dass Ihr Server nur den "guten" Datenverkehr verarbeiten muss. Das bedeutet, dass Ihre Ressource ausschließlich für den beabsichtigten Zweck verwendet wird und für unerwünschten Datenverkehr.

## Welche Firewall bietet IBM an?
{:faq}

In diesem [Abschnitt ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](/docs/infrastructure/fortigate-10g/explore-firewalls.html#explore-firewalls){: new_window} finden Sie einen detaillierten Vergleich aller in der IBM Cloud angebotenen Firewall-Produkte. 

## Ist die Hardware-Firewall (dediziert) mit den Load-Balancer-Produkten von IBM kompatibel?
{:faq}

Ja. Die Hardware-Firewall (dediziert) ist sowohl mit standardmäßigen und dedizierten Einrichtungen für den Lastausgleich als auch mit Citrix Netscaler VPX und MPX kompatibel.

## Kann ich eine dedizierte Hardware-Firewall und ein Netzgateway mit demselben VLAN verbinden?
{:faq}

Nein, es ist nicht möglich, einen Hardware-Service (freigegeben oder dediziert) und ein Netzgateway-Gerät demselben VLAN zuzuweisen. 

## Fließt der öffentliche Datenverkehr zuerst durch die Einrichtung für den Lastausgleich oder die Firewall?
{:faq}

Aus dem öffentlichen Internet kommen zuerst die lokale Einrichtung für den Lastausgleich, die dedizierte Einrichtung für den Lastausgleich oder die Enterprise-Lastausgleichsfunktion, dann die Hardware-Firewall-Produkte und zuletzt die NetScaler-Produkte (zusammen mit den Kundenservern).

## Berechnet SoftLayer für die Firewall-Bandbreite eine Gebühr?
{:faq}

Die Bandbreite für die Hardware-Firewall (freigegeben), die Hardware-Firewall (dediziert) und die FortiGate Security Appliance wird nicht abgerechnet.  Darüber hinaus können diese Produkte die gesamte Bandbreitenauslastung reduzieren, indem sie den Datenverkehr begrenzt, auf den Server reagieren müssen.

## Was bedeuten die ausgegrauten Ports in meiner Windows-Firewall?
{:faq}

SoftLayer bietet viele verschiedene Services, die Sie mit Ihrem Server nutzen können, einschließlich Evault, SNMP und Nagios-Überwachung. Diese Dienste erfordern, dass unsere internen Systeme zu einem gewissen Grad mit Ihrem Server kommunizieren. Die ausgegrauten Ports, die in der Ausnahmeliste angezeigt werden, sind Ports, die nur am internen Netzport geöffnet sind. Sie sind weiterhin über die öffentliche (Internet-)Netzverbindung blockiert. Da das interne Netz ein gesichertes Netz ist, wird das Öffnen dieser Ports als sicher angenommen.

Diese Ports können in der Regel nicht geändert werden. Wenn Sie jedoch die Firewallregeln zurücksetzen, werden die Ports aus der Ausnahmeliste gelöscht. Beachten Sie, dass das Zurücksetzen der Firewallregeln sich nachteilig auf diese zusätzlichen Services auswirken und abhängig von Ihrer Serverkonfiguration auch andere Probleme verursachen kann.

## Welche Hardware-Firewall-Optionen sind für 10-Gbit/s-Server verfügbar?
{:faq}

Wenn 10 Gbit/s nur für das private Netz (für Datenbank, Sicherung, Speicher usw.) erforderlich sind, können Kunden ein Downgrade ihrer allgemein zugänglichen Uplinks anfordern und Hardware-Firewall-Produkte bestellen. Wenn im öffentlichen Netz 10 Gbit/s erforderlich sind, ist ein Netzgateway oder eine FortiGate Security Appliance mit 10 Gbit/s notwendig.

## Welche IP-Bereiche sind für die Firewall zulässig?
{:faq}

Die Liste der IP-Adressen und IP-Bereiche, die die Firewall zulässt, finden Sie [hier](ips.html). 

## Wie viele Server werden von der Hardware-Firewall (dediziert) oder der FortiGate Security Appliance maximal geschützt?
{:faq}

Sowohl die dedizierte Hardware-Firewall als auch die FortiGate Security Appliance können in einem öffentlichen VLAN jeden Server schützen.  Berücksichtigen Sie jedoch, dass diese Firewallgeräte mit 2 Gbit/s Uplink verbunden sind. Daher wird empfohlen, die Anzahl der Firewallinstanzen zu skalieren, um die Leistungsanforderungen Ihrer App zu erfüllen. Stellen Sie dazu zusätzliche öffentliche VLAN-Firewalls in einem Pod bereit, um zusätzliche Firewalls und zugehörige Rechenressourcen hinzuzufügen.

## Welche VPN-Optionen sind mit jedem Firewallprodukt enthalten?
{:faq}

Nicht alle Firewalls bieten VPN an und nicht alle VPN-Optionen sind identisch.  Die allgemeinen Optionen für VPN lauten:

* Jeder Kunde erhält uneingeschränkte SSL-VPN-Verbindungen zu unserem privaten Netz. Diese Verbindungen können hergestellt werden, indem Sie oben auf der Seite auf den VPN-Link klicken, während Sie beim Kundenportal angemeldet sind.
* Kunden erhalten außerdem pro Konto jeweils ein PPTP-VPN. Es können weitere PPTP-VPN-Benutzer in Paketen aus 5 Benutzern für 5 $ pro Monat zum Konto hinzugefügt werden.
* SoftLayer bietet auch einen einfachen Multi-Tenant-IPSec-VPN-Service ab 99 $ pro Monat.
* Die FortiGate Security Appliance bietet SSL- und IPSec-VPN-Optionen ausschließlich mit Zugriff auf das öffentliche Netz (kein Zugriff auf das private SoftLayer-Netz).
* Das Network Gateway bietet SSL-, IPSec- und OpenVPN-Funktionalitäten im öffentlichen oder privaten Netz.
* Die NetScaler-Produkte können SSL- und IPSec-VPN im öffentlichen oder privaten Netz bereitstellen.
* Kunden können in ihrer SoftLayer-Umgebung auch eine VPN-Lösung auf einem Server bereitstellen.

## Wenn für die Hardware-Firewall (dediziert) oder FortiGate Security Appliance die Option "Hochverfügbarkeit" ausgewählt wurde, welche Schritte müssen dann durchgeführt werden, um dieses Feature zu nutzen?
{:faq}

Keine. Bei einer Bestellung mit Hochverfügbarkeit (HA) stellt SoftLayer die Appliances automatisch in der HA-Konfiguration bereit.  Wenn die primäre Einheit ausfällt, übernimmt eine sekundäre passive Einheit die Funktion der primären aktiven Instanz, um den Datenverkehr weiterzuleiten.  Während dieses Failover normalerweise automatisch erfolgt, empfiehlt es sich, die Server zu überwachen und sicherzustellen, dass der Datenverkehr erfolgreich übertragen wird.

## Welche Firewallprodukte unterstützen die Public-to-Private-NAT- bzw. private VLAN-Segmentierung?
{:faq}

FortiGate Security Appliance (10 Gbit/s) unterstützt eine Public-to-Private-NAT- bzw. private VLAN-Segmentierung. 
