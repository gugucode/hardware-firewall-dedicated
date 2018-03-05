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

# Ajout d'un pare-feu matériel (dédié) à un réseau local virtuel (VLAN) public

La commande d'un pare-feu matériel (dédié) ne peut pas se faire dans le cadre d'une commande de serveur et doit être passée après l'établissement d'au moins un noeud de traitement public et une fois le VLAN associé ajouté.

Pour ajouter une protection à un réseau local virtuel, commandez un pare-feu matériel (dédié) depuis la page VLAN :

1. Depuis votre navigateur, ouvrez le [Portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} et connectez-vous à votre compte.
2. Dans la navigation du portail client, sélectionnez **Réseau > Gestion IP > VLAN** pour accéder à la page VLAN. Chaque ligne représente un réseau local virtuel dans votre infrastructure. IBM Cloud remplit automatiquement les informations "Numéro de VLAN" et "Routeur principal", en indiquant le vrai numéro de réseau local virtuel et le routeur sur lequel il est configuré. La zone "Nom" peut être utilisée pour définir un nom reconnaissable. La colonne à l'extrême droite intitulée "Passerelle/pare-feu" contient les détails sur le type de protection par pare-feu en vigueur pour ce réseau local virtuel, le cas échéant. 

	**Astuce :** pour filtrer le tableau des réseaux locaux virtuels afin d'afficher uniquement les VLAN publics, cliquez sur l'onglet **Filtre**, entrez "fcr" dans la zone Routeur principal et cliquez sur le bouton **Filtrer**.
3. Recherchez le VLAN que vous souhaitez protéger et cliquez sur le lien **Ajouter pare-feu** sur la même ligne. Ce lien ouvre la page **Commander Pare-feu Matériel (Dédié)**. Si la colonne "Passerelle/pare-feu" est déjà remplie, un pare-feu ou une passerelle réseau est déjà associé au VLAN et l'unité doit être retirée pour pouvoir continuer.
4. Sélectionnez **Pare-feu matériel (dédié)** ou **Pare-feu matériel (haute disponibilité)**. 

	L'option Haute disponibilité déploie un matériel et une interface identiques, mais déploie également un deuxième noeud passif pour continuer à traiter le trafic en cas d'échec du noeud actif. La haute disponibilité réduit les risques d'indisponibilité excessive. 

5. Cliquez sur le bouton **Serveurs sur ce VLAN** pour vérifier que vous sélectionnez le réseau local virtuel approprié.
6. Entrez le mode de paiement de votre choix et cliquez sur **Continuer**.
7. Dans l'écran suivant, entrez, le cas échéant, les codes promo, lisez et acceptez le contrat cadre de service (MSA) et cliquez sur **Valider la commande**. 
