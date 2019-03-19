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

# Configuration du pare-feu matériel (dédié)
{: #configuring-the-hardware-firewall-dedicated-}

La première fois que le pare-feu est ajouté au réseau local virtuel (VLAN), un ensemble de règles est instauré pour autoriser tout le trafic via le pare-feu. La configuration du pare-feu est aussi simple que la création d'un ensemble de règles pour autoriser l'accès à une sélection d'adresses IP ou de ports à partir d'adresses IP Internet spécifiques tout en refusant le trafic provenant d'autres sources.

## Edition de règles

Pour éditer les règles du pare-feu :

1. Depuis votre navigateur, ouvrez le [Portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} et connectez-vous à votre compte.
2. Dans la navigation du portail client, sélectionnez **Réseau > Gestion IP > VLAN**. Chaque ligne représente un réseau local virtuel dans votre infrastructure.  Cliquez sur le lien Firewall-vlanXXXX.networklayer.com associé au VLAN que vous souhaitez gérer pour accéder à la page **Détails de l'unité**. Si une ou plusieurs règles ont été définies, vérifiez que "Statut" indique que le pare-feu a le statut "Traiter toutes les règles".  Les utilisateurs peuvent choisir d'ignorer les règles si les règles implémentées ont un impact non souhaité sur leur environnement en cliquant sur "Contourner les Règles" dans cette zone.
3. Pour commencer à mettre à jour les règles, cliquez sur l'onglet **Règles**. Cette page affiche les sections présentant les règles actuellement en vigueur pour les adresses IPv4 et IPv6.  Si aucune règle n'est implémentée, une marque de réservation estompée s'affiche.  Modifiez des règles individuelles en cliquant sur les lignes correspondantes.  Cette liste de règles constitue la configuration opérationnelle ('working config'). Une configuration opérationnelle est un ensemble de règles en cours de création mais qui n'a pas encore été appliqué au pare-feu. L'utilisateur peut modifier, ajouter et supprimer des règles jusqu'à ce que l'ensemble de règles soit finalisé.  Les règles sont affichées dans l'ordre dans lequel elles sont traitées, les règles ayant les numéros les moins élevés étant prioritaires par rapport à celles ayant les numéros les plus élevés (si la règle 1 autorise un paquet, les règles 2 et supérieures ne sont pas appliquées à ce paquet).
4. Cliquez sur une règle pour l'éditer ou cliquez sur le signe plus au bas du tableau pour ajouter une règle supplémentaire. Cliquer sur l'icône avec le signe moins permet de supprimer la règle. Les règles sont automatiquement validées dès que vous les saisissez.

    Les zones sont les suivantes :

    **Action :** 'autoriser' ou 'refuser' le trafic correspondant à cette règle

    **Source :** peut être 'tout' ou une adresse IP spécifique ou l'adresse réseau d'un sous-réseau particulier.

    **CIDR :** indique la notation CIDR standard correspondant à la source sélectionnée.  "32" implémentera la règle pour une seule adresse IP alors que "24", par exemple, l'implémentera pour 256 adresses IP.

    **Destination :** peut être 'tout' ou une adresse IP spécifique ou l'adresse réseau d'un sous-réseau particulier.

    **CIDR :** indique la notation CIDR standard correspondant à la destination sélectionnée.

    **Plage de Ports :** ces 2 zones indiquent la plage de ports (comprise entre 1 et 65535) à laquelle la règle va s'appliquer.

    **Protocole :** sélectionne le protocole auquel la règle va s'appliquer (TCP/GRE/ICMP/UDP/PPTP/AH/ESP)

    **Remarques :** zone utilisée pour saisir une remarque concernant cette règle.
    
5. Lorsque la configuration opérationnelle est terminée, cliquez sur le bouton **Mettre à jour les règles** pour qu'elle s'applique au pare-feu. En principe, les règles prennent effet en l'espace de deux minutes.

## Ports communs

| Protocole | Port |
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
| RDP | 3389 |
| PostgreSQL | 5432 |
| Web VNC | 5800 |
| Client VNC | 5900 |
| Urchin | 9999 ou 10000 ||
