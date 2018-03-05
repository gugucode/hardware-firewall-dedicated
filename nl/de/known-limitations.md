---

copyright:
  years: 2017
lastupdated: "2017-10-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Bekannte Einschränkungen
Für die Hardware-Firewall (dediziert) gelten die folgenden bekannten Einschränkungen:

* Inkompatibel mit dem Windows-Netzlastenausgleich (NLB) aufgrund der Verarbeitung von ARP.

* Die Failover-Funktionalität für hohe Verfügbarkeit wird dem Benutzer nicht zur Verfügung gestellt. Wenn die Master-Firewall nicht funktioniert, aber kein automatischer Failover erfolgt, wird ein Support-Ticket benötigt. Die Geräteüberwachung für kritische Services wird empfohlen, um sicherzustellen, dass Firewalls den Datenverkehr richtig weiterleiten.

* Eine Hardware-Firewall (dediziert) kann nicht in einem VLAN bereitgestellt werden, das einem Netzgateway, einer Hardware-Firewall oder einer FortiGate Security Appliance aktuell zugeordnet ist.
