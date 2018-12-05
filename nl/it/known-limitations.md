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

# Limitazioni note
L'Hardware Firewall (Dedicated) ha le seguenti limitazioni note:

* Incompatibile con Windows Network Load Balancing (NLB) a causa del modo in cui viene elaborato ARP

* La funzionalità di failover dell'elevata disponibilità non viene esposta all'utente. Se il firewall master ha un malfunzionamento, ma non un failover automatico, sarà necessario un ticket di supporto. Viene consigliato il monitoraggio del dispositivo per i servizi critici per garantire che i firewall stiano passando il traffico in modo appropriato.

* Un Hardware Firewall (Dedicated) non può essere distribuito a una VLAN al momento associata a un gateway di rete, un firewall hardware o a un FortiGate Security Appliance.
