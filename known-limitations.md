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

# Known Limitations for Hardware Firewall (Dedicated)
{: #known-limitations-for-hardware-firewall-dedicated-}

The Hardware Firewall (Dedicated) has the following known limitations:

* Incompatible with Windows Network Load Balancing (NLB) due to the way ARP is processed

* High Availability failover functionality is not exposed to the user. If the master firewall malfunctions, but does not failover automatically a support ticket will be required. Device monitoring for critical services is recommended to ensure that firewalls are appropriately passing traffic.

* A Hardware Firewall (Dedicated) cannot be deployed on a VLAN that is currently associated with a Network Gateway, Hardware Firewall, or Fortigate Security Appliance.