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

# Limitations connues
Voici les limitations connues du pare-feu matériel (dédié) :

* Il est incompatible avec l'équilibrage de la charge réseau (NLB) de Windows en raison du mode de traitement du protocole ARP

* La fonctionnalité de basculement à haute disponibilité n'est pas exposée à l'utilisateur. En cas de dysfonctionnement du pare-feu principal et si le basculement ne s'effectue pas automatiquement, un ticket de demande de service sera nécessaire. La surveillance d'unité pour les services critiques est recommandée pour s'assurer que les pare-feux transfèrent correctement le trafic.

* Un pare-feu matériel (dédié) ne peut pas être déployé sur un VLAN associé à une passerelle réseau, un pare-feu matériel ou un dispositif de sécurité FortiGate.
