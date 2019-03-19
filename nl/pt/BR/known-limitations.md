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

# Limitações conhecidas para o Hardware Firewall (Dedicated)
{: #known-limitations-for-hardware-firewall-dedicated-}

O Hardware Firewall (Dedicated) possui as limitações conhecidas a seguir:

* Incompatível com o Windows Network Load Balancing (NLB) devido à maneira com que ARP é processado

* A funcionalidade de failover de alta disponibilidade não é exposta ao usuário. Se o firewall principal apresentar mau funcionamento, mas não ocorrer failover automaticamente, um chamado de suporte será necessário. Recomenda-se monitorar o dispositivo para serviços críticos para assegurar que os firewalls estejam passando tráfego apropriadamente.

* Um Hardware Firewall (Dedicated) não pode ser implementado em uma VLAN que esteja atualmente associada a um Network Gateway, um Hardware Firewall ou um Fortigate Security Appliance.
