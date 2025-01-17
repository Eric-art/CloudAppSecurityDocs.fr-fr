---
title: Intégrer Cloud App Security à Zscaler
description: Cet article explique comment intégrer Microsoft Cloud App Security à Zscaler pour offrir une expérience Cloud Discovery fluide et créer un bloc automatisé d’applications non approuvées.
keywords: ''
author: rkarlin
ms.author: rkarlin
manager: rkarlin
ms.date: 1/29/2019
ms.topic: conceptual
ms.collection: M365-security-compliance
ms.prod: ''
ms.service: cloud-app-security
ms.technology: ''
ms.assetid: 8abeab8e-3b7a-46a7-bbec-9aaf26f778a8
ms.reviewer: reutam
ms.suite: ems
ms.custom: seodec18
ms.openlocfilehash: 82bd7721d29d212c03342b0d016fe8c245a88625
ms.sourcegitcommit: 9f0c562322394a3dfac7f1d84286e673276a28b1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65568346"
---
# <a name="integrate-cloud-app-security-with-zscaler"></a>Intégrer Cloud App Security à Zscaler

*S’applique à : Microsoft Cloud App Security*

Si vous travaillez avec Cloud App Security et Zscaler, vous pouvez intégrer les deux produits pour améliorer la sécurité de votre expérience Cloud Discovery. Zscaler, en tant que proxy cloud autonome, surveille le trafic de votre organisation, ce qui vous permet de définir des stratégies pour le blocage des transactions. Ensemble, Cloud App Security et Zscaler fournissent les fonctionnalités suivantes :

- Déploiement fluide de Cloud Discovery : le fait d’utiliser Zscaler comme proxy de votre trafic avant de l’envoyer à Cloud App Security élimine la nécessité d’installer des collecteurs de journaux sur vos points de terminaison réseau pour activer Cloud Discovery.
- Les fonctionnalités de blocage de Zscaler sont automatiquement appliquées sur les applications que vous définissez comme non approuvées dans Cloud App Security.
- Améliorez votre portail Zscaler avec l’évaluation du risque de Cloud App Security pour 200 applications cloud de pointe, qui peuvent être affichées directement dans le portail Zscaler.

## <a name="prerequisites"></a>Prérequis

- Licence valide pour Microsoft Cloud App Security
- Licence valide pour Zscaler Cloud 5.6
- Abonnement à Zscaler NSS actif 

## <a name="deployment"></a>Déploiement

1. Dans le portail Zscaler, procédez aux étapes permettant de terminer [l’intégration du partenaire Zscaler à Microsoft Cloud App Security](https://help.zscaler.com/zia/configuring-mcas-integration).
2. Dans le portail Cloud App Security, effectuez les étapes d’intégration suivantes :
    1. Cliquez sur la roue dentée des paramètres et sélectionnez **Paramètres Cloud Discovery**. 
    2. Cliquez sur l’onglet **Chargement automatique des journaux**, puis cliquez sur **Ajouter une source de données**.
    3. Dans la page **Ajouter une source de données**, entrez les paramètres suivants :

       - Nom = NSS
       - Source = Zscaler QRadar LEEF
       - Type de récepteur = Syslog - UDP

         ![source de données Zscaler](./media/data-source-zscaler.png)

    4. Cliquez sur **Afficher un exemple du fichier journal attendu**. Puis cliquez sur **Télécharger l’exemple de journal** pour afficher un exemple de journal Discovery et vous assurer qu’il correspond à vos journaux.<br>

3. Examinez les applications cloud découvertes sur votre réseau. Pour plus d’informations et de méthodes d’examen, consultez la page [Utilisation de Cloud Discovery](working-with-cloud-discovery-data.md).

4. Toute application que vous définissez comme non approuvée dans Cloud App Security est soumise à un test Ping par Zscaler toutes les deux heures, puis bloquée automatiquement par Zscaler. Pour plus d’informations sur la non-approbation des applications, consultez [Approbation/non-approbation d’une application](governance-discovery.md#BKMK_SanctionApp).

## <a name="next-steps"></a>Étapes suivantes

[Contrôler les applications cloud avec des stratégies](control-cloud-apps-with-policies.md)

[Les clients Premier peuvent également créer une demande de support directement dans le portail Premier.](https://premier.microsoft.com/)  
  
