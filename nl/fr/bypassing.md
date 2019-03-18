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

# Contournement des règles de pare-feu matériel (dédié)
{: #bypassing-hardware-firewall-dedicated-rules}

Pour contourner les règles de pare-feu :

1. Depuis votre navigateur, ouvrez le [Portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} et connectez-vous à votre compte.
2. Dans la navigation du portail client, accédez à **Réseau > Gestion IP > VLAN** et cliquez sur l'unité pare-feu que vous souhaitez contourner.
3. Sur la page **Détails de l'unité**, vous pouvez utiliser le menu déroulant **Actions** pour sélectionner **Paramétrer mode de contournement de route** ou, dans la section **Statut :**, cliquer sur **Contourner les règles**. 

	Une autre option est de prendre une route autour du pare-feu. Vous pouvez utiliser le menu déroulant **Actions** pour sélectionner **Paramétrer mode de contournement de route** ou, dans la section **Statut :**, cliquer sur le bouton **Route autour**. Quelle que soit la méthode, une boîte de dialogue de confirmation doit s'afficher. Cliquez sur **Oui** pour confirmer l'action. La mise en oeuvre effective d'une route autour prend approximativement deux minutes. En mode contournement, la zone "Statut" indique "Routage AUTOUR du pare-feu".

## Réactivation des règles

Pour réactiver les règles, suivez les instructions ci-dessus pour accéder à la page **Détails de l'unité**, cliquez sur le menu déroulant **Actions**, puis sélectionnez **Paramétrer mode de contournement de route**. Vous obtenez alors une boîte de dialogue de confirmation. Cliquez sur **Oui** pour confirmer l'action. La zone "Statut" revient à "Routage À TRAVERS le pare-feu" en l'espace de deux minutes.
