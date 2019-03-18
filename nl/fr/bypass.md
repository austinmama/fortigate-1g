---

copyright:
  years: 2017
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Contournement des règles de pare-feu
{: #bypassing-the-firewall-rules}

Pour contourner les règles de pare-feu, procédez comme suit :

1. Depuis votre navigateur, ouvrez le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} et connectez-vous à votre compte.
2. Dans la navigation du portail client, accédez à **Réseau > Gestion IP > VLAN** et cliquez sur l'unité pare-feu que vous souhaitez contourner.
3. Sur la page **Détails de l'unité**, vous pouvez utiliser le menu déroulant **Actions** sélectionner **Paramétrer mode de contournement des règles** ou, dans la section **Statut :**, cliquer sur le bouton **Contourner les Règles**. Le contournement des règles prend environ deux minutes pour entrer en vigueur. Le statut doit passer sur "Contourner toutes les Règles".

	Une autre option est de prendre une route autour du pare-feu. Vous pouvez utiliser le menu déroulant **Actions** pour sélectionner **Paramétrer mode de contournement de route** ou, dans la section **Statut :**, cliquer sur le bouton **Route autour**. Dans tous les cas, vous devriez obtenir une boîte de dialogue de confirmation. Cliquez sur **Oui** pour confirmer l'action. La mise en oeuvre effective d'une route autour prend approximativement deux minutes. En mode contournement, la zone "Statut" indique "Routage AUTOUR du pare-feu".

## Réactivation des règles

Pour réactiver les règles, suivez les instructions ci-dessus pour accéder à l'onglet **Configuration** de l'unité, cliquez sur le menu déroulant **Actions** et sélectionnez **Paramétrer mode de contournement de route**. Vous obtenez alors une boîte de dialogue de confirmation. Cliquez sur **Oui** pour confirmer l'action. La zone "Statut" revient à "Routage À TRAVERS le pare-feu" en l'espace de deux minutes.
