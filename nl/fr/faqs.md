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

# Foire aux questions
Voici les questions les plus fréquentes concernant l'utilisation du pare-feu du dispositif de sécurité FortiGate (FSA) 1g.

## Qu'est-ce qu'un pare-feu ?
{:faq}

Un pare-feu est un périphérique réseau connecté en amont d'un serveur. Le pare-feu bloque le trafic indésirable avant qu'il n'atteigne le serveur.

## Pourquoi utiliser un pare-feu ?
{:faq}

Avec l'utilisation d'un pare-feu, l'avantage principal est de laisser passer uniquement le "bon" trafic, c'est-à-dire que vos ressources sont uniquement utilisées à cette fin, évitant ainsi le traitement de trafic non souhaité.

## Quels sont les produits de pare-feu proposés par IBM ?
{:faq}

Vous trouverez une comparaison détaillée de tous les produits de pare-feu proposés dans IBM Cloud en consultant cette [rubrique ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](/docs/infrastructure/fortigate-10g/explore-firewalls.html#explore-firewalls){: new_window}. 

## Le pare-feu matériel (dédié) est-il compatible avec les produits d'équilibrage de charge d'IBM ?
{:faq}

Oui. Le pare-feu matériel (dédié) est compatible avec les équilibreurs de charge standard et dédiés, ainsi qu'avec Citrix Netscaler VPX et MPX.

## Puis-je disposer d'un pare-feu matériel dédié et d'une passerelle réseau associés au même réseau local virtuel (VLAN) ?
{:faq}

Non, il n'est pas possible d'avoir un service de pare-feu (partagé ou dédié) et une passerelle réseau affectés au même réseau local virtuel. 

## Le trafic public passe-t-il d'abord via mon équilibreur de charge ou par le pare-feu matériel ?
{:faq}

Lorsqu'il provient du réseau Internet public, il passe d'abord par l'équilibreur de charge local, l'équilibreur de charge dédié ou l'équilibreur de charge d'entreprise, puis par les produits de pare-feu matériel, et enfin par les produits NetScaler (auxquels s'ajoutent les serveurs du client).

## SoftLayer facture-t-il des frais pour la bande passante de pare-feu ?
{:faq}

La bande passante du pare-feu matériel (partagé), du pare-feu matériel (dédié) et du dispositif de sécurité FortiGate n'est pas comptabilisée.  Par ailleurs, ces produits contribuent à réduire l'utilisation de la bande passante totale en limitant le trafic auquel les serveurs doivent répondre.

## A quoi correspondent les ports grisés dans mon pare-feu Windows ?
{:faq}

SoftLayer offre de nombreux services divers et variés que vous pouvez utiliser avec votre serveur, parmi lesquels Evault, SNMP et le service de surveillance Nagios. Ces services nécessitent que nos systèmes internes communiquent avec votre serveur dans une certaine mesure. Les ports grisés que vous voyez dans la liste Exceptions sont des ports ouverts sur le port réseau interne uniquement. Ils restent bloqués pour la connexion au réseau (Internet) public. Le réseau interne étant un réseau sécurisé, ces ports peuvent donc rester ouverts en toute sécurité.

En général, ces ports ne sont pas modifiables. Cependant si vous réinitialisez les règles de pare-feu, ils seront supprimés de la liste Exceptions. Soyez vigilant, car la réinitialisation des règles de pare-feu peut avoir des effets indésirables sur ces services supplémentaires mais peut également générer d'autres problèmes avec votre serveur en fonction de la configuration actuelle du serveur.

## Quelles sont les options de pare-feu matériel disponibles pour les serveurs 10 Gbit/s ?
{:faq}

Si 10 Gbit/s sont requis sur le réseau privé uniquement (pour la base de données, la sauvegarde, le stockage, etc.), les clients peuvent demander une rétromigration seulement pour leurs liaisons montantes publiques et commander n'importe quel produit de pare-feu matériel. Si 10 Gbit/s sont requis sur le réseau public, une passerelle réseau ou un dispositif de sécurité FortiGate 10 Gbit/s est nécessaire.

## Quelles plages d'adresses IP autoriser via le pare-feu ?
{:faq}

Pour obtenir la liste des adresses IP et des plages d'adresses IP à autoriser via le pare-feu, cliquez [ici](ips.html). 

## Quel est le nombre maximal de serveurs pouvant être protégés par le pare-feu matériel (dédié) ou par le dispositif de sécurité FortiGate ?
{:faq}

Le pare-feu matériel (dédié) et le dispositif de sécurité FortiGate (FSA) peuvent protéger tous les serveurs sur un réseau local virtuel public.  Toutefois, il est important de noter que comme ces périphériques de pare-feu sont connectés avec une liaison montante de 2 Gbit/s, il est recommandé d'adapter le nombre d'instances de pare-feu pour obtenir les performances requises pour votre application. Les clients peuvent le faire en déployant des pare-feux de VLAN public supplémentaires dans un pod pour pouvoir ajouter d'autres pare-feux et ressources de traitement associées.

## Quelles sont les options VPN incluses dans chaque produit de pare-feu ?
{:faq}

Tous les pare-feux n'offrent pas forcément de réseau VPN et toutes les options VPN ne sont pas identiques.  Les options générales de réseau VPN sont :

* Chaque client reçoit des connexions VPN SSL illimitées à notre réseau privé. Ces connexions peuvent être établies en cliquant sur le lien Réseau privé virtuel (VPN) en haut de la page lorsque vous êtes connecté au portail client.
* Les clients reçoivent également un réseau VPN PPTP par compte. Ils peuvent ajouter d'autres réseaux VPN PPTP à leur compte par pack de 5 pour un supplément de 5 $/mois.
* SoftLayer propose également un service VPN IPSec à service partagé à partir de 99 $/mois.
* Le dispositif de sécurité FortiGate (FSA) fournit des options VPN SSL et IPSec avec accès au réseau public uniquement (aucun accès au réseau privé SoftLayer).
* La passerelle réseau fournit les fonctions SSL, IPSec et OpenVPN sur réseau public ou privé.
* Les produits NetScaler peuvent fournir les fonctions VPN SSL et IPSec sur réseau public ou privé.
* Les clients peuvent également déployer une solution VPN sur un serveur au sein de leur environnement SoftLayer.

## Lorsque je sélectionne l'option Haute disponibilité dans le pare-feu matériel (dédié) ou dans le dispositif de sécurité FortiGate, quelles sont les étapes à suivre pour tirer parti de cette fonction ?
{:faq}

Aucune. Lorsqu'il est commandé avec l'option Haute disponibilité, SoftLayer fournit automatiquement les dispositifs en configuration haute disponibilité.  Si le dispositif principal échoue, un autre dispositif passif prend le relais en tant qu'instance active principale et commence à soumettre du trafic.  Alors que ce basculement est en principe automatique, il est recommandé de surveiller les serveurs et de vérifier que le trafic est transmis correctement.

## Quels sont les produits de pare-feu qui prennent en charge la conversion d'adresses réseau NAT public vers privé et/ou la segmentation de VLAN privé ?
{:faq}

Le dispositif de sécurité FortiGate 10 Gbit/s prend en charge la conversion d'adresses réseau NAT public vers privé et la segmentation de VLAN privé. 
