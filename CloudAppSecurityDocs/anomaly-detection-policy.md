---
title: Créer une stratégie de détection des anomalies dans Cloud App Security
description: Cet article fournit une description des stratégies de détection des anomalies ainsi que des informations de référence sur les composantes d’une stratégie de détection des anomalies.
keywords: ''
author: rkarlin
ms.author: rkarlin
manager: rkarlin
ms.date: 2/4/2019
ms.topic: conceptual
ms.collection: M365-security-compliance
ms.prod: ''
ms.service: cloud-app-security
ms.technology: ''
ms.assetid: ab9bc377-d2f5-4f4c-a419-f1728a15d1c7
ms.reviewer: reutam
ms.suite: ems
ms.custom: seodec18
ms.openlocfilehash: 0985fe571a96f540cc521808d6f4c4fb4b42e4b8
ms.sourcegitcommit: 9f0c562322394a3dfac7f1d84286e673276a28b1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65565897"
---
# <a name="get-instantaneous-behavioral-analytics-and-anomaly-detection"></a>Obtenir instantanément une détection des anomalies et une analytique comportementale

*S’applique à : Microsoft Cloud App Security*

Les stratégies de détection des anomalies de Microsoft Cloud App Security intègrent une analytique comportementale des utilisateurs et des entités (UEBA) et un apprentissage automatique (ML) pour vous permettre de lancer immédiatement une détection avancée des menaces dans tout votre environnement cloud. Comme ces stratégies sont automatiquement activées, les nouvelles stratégies de détection des anomalies fournissent des résultats immédiats grâce à des détections immédiates, le ciblage de nombreuses anomalies comportementales entre vos utilisateurs et les ordinateurs et appareils connectés à votre réseau.  En outre, les nouvelles stratégies exposent davantage de données à partir du moteur de détection de Cloud App Security afin d’accélérer le processus d’investigation, et contiennent des menaces permanentes. 

Les stratégies de détection des anomalies sont automatiquement activées, mais Cloud App Security comporte une période d’apprentissage initiale de sept jours, pendant laquelle les alertes de détection des anomalies ne sont pas toutes déclenchées. Après cela, chaque session est comparée aux activités (activité des utilisateurs, adresses IP, appareils, etc.) détectées au cours du mois passé et à l’indice de risque de ces activités.  Ces détections font partie du moteur de détection des anomalies global qui profile votre environnement et déclenchent des alertes suivant une base de référence qui a été définie par rapport à l’activité de votre organisation. Ces détections utilisent également les algorithmes d’apprentissage automatique conçus pour profiler les utilisateurs et le modèle de connexion afin de réduire les faux positifs.

Ces anomalies sont détectées en analysant l’activité des utilisateurs. Le risque est évalué en examinant plus de 30 indicateurs de risque différents, regroupés en facteurs de risque, comme suit : 
          
 -   Adresse IP à risque
 -   Échecs de connexion
 -   Activité administrative
 -   Comptes inactifs
 -   Emplacement  
 -   Voyage impossible
 -   Agent Appareil et utilisateur
 -   Fréquence d'activité

Selon les résultats de la stratégie, des alertes de sécurité sont déclenchées. Cloud App Security examine chaque session utilisateur sur votre cloud et vous alerte en cas d’événement anormal par rapport aux activités de référence ou habituelles de votre organisation ou de l’utilisateur. 


## <a name="anomaly-detection-policies"></a>Stratégies de détection des anomalies
Vous pouvez afficher les stratégies de détection des anomalies dans le portail en cliquant sur **Contrôle**, puis sur **Stratégies**. Sélectionnez **Stratégie de détection d’anomalie** pour le type de stratégie.

 ![nouvelles stratégies de détection des anomalies](./media/new-anomaly-detection-policies.png)

Les stratégies de détection d’anomalie suivantes sont disponibles :

**Voyage impossible**
-  Cette détection identifie deux activités de l’utilisateur (dans une ou plusieurs sessions) provenant d’emplacements éloignés sur une durée plus courte que la durée nécessaire à l’utilisateur pour aller du premier emplacement au second, ce qui indique qu’un autre utilisateur utilise les mêmes informations d’identification. Cette détection utilise un algorithme d’apprentissage automatique qui ignore les « faux positifs » évidents contribuant à la condition de voyage impossible, comme les réseaux privés virtuels et les emplacements régulièrement utilisés par d’autres utilisateurs de l’organisation. La détection a une période d’apprentissage initiale de sept jours au cours de laquelle elle apprend le modèle d’activité d’un nouvel utilisateur. La détection de voyage impossible identifie l’activité utilisateur inhabituelle et impossible entre deux emplacements. L’activité doit être suffisamment inhabituelle pour être considérée comme un indicateur de compromission et justifier le déclenchement d’une alerte. Pour que cela fonctionne, la logique de détection inclut différents niveaux de suppression pour répondre aux besoins des scénarios susceptibles de déclencher des « faux positifs », comme les activités des réseaux privés virtuels. Le curseur de sensibilité vous permet d’agir sur l’algorithme et de définir une logique de détection plus ou moins stricte.
Plus le niveau de sensibilité est élevé, plus le niveau de suppression appliqué dans le cadre de la logique de détection est bas. De cette façon, vous pouvez adapter la détection en fonction de vos besoins de couverture et de vos cibles SNR.



**Activité à partir de pays peu fréquents**
- Cette détection prend en compte les emplacements d’activité précédents pour identifier les emplacements nouveaux et peu fréquentés. Le moteur de détection des anomalies stocke les informations sur les emplacements précédents employés par les utilisateurs de l’organisation. Une alerte est déclenchée quand une activité se produit à partir d’un emplacement qui n’a pas été récemment visité ou qui ne l’a jamais été par un utilisateur de l’organisation. 

**Détection de programme malveillant**
- Cette détection identifie les fichiers malveillants dans votre stockage cloud, qu’ils viennent de vos applications Microsoft ou tierces. Microsoft Cloud App Security utilise la Threat Intelligence de Microsoft pour savoir si certains fichiers sont associés à des attaques par programme malveillant connues et s’ils sont potentiellement dangereux. Cette stratégie intégrée est désactivée par défaut. Les fichiers ne sont pas tous analysés, mais des solutions sont utilisées pour rechercher les fichiers qui présentent un risque potentiel. Une fois que les fichiers sont détectés, vous pouvez voir une liste des **fichiers infectés**. Cliquez sur le nom du fichier malveillant dans le tiroir de fichier pour ouvrir un rapport sur les programmes malveillants qui vous fournit des informations sur le type de programme malveillant dont le fichier est infecté.
    
**Activité depuis des adresses IP anonymes**
- Cette détection identifie que des utilisateurs étaient actifs à partir d’une adresse IP qui a été identifiée comme adresse IP proxy anonyme. Ces proxys sont utilisés par des personnes qui veulent masquer l’adresse IP de leur appareil dans un but qui peut être malveillant. Cette détection utilise un algorithme d’apprentissage automatique qui réduit les « faux positifs », comme les adresses IP mal balisées qui sont couramment utilisées par les utilisateurs de l’organisation.

**Activité de ransomware**
-  Cloud App Security a étendu ses capacités de détection de ransomware à la détection d’anomalie pour garantir une couverture plus complète contre les attaques de ransomware complexes. Fort de notre expertise en recherche dans la sécurité visant à identifier les modèles comportementaux qui reflètent des activités de ransomware, Cloud App Security assure une protection complète et solide. Si Cloud App Security identifie, par exemple, un taux élevé de chargements de fichiers ou d’activités de suppression de fichiers, cela peut représenter un processus de chiffrement indésirable. Ces données sont collectées dans les journaux reçus des API connectées, puis combinées avec des modèles comportementaux appris et des informations sur les menaces, par exemple, des extensions de ransomware. Pour plus d’informations sur la manière dont Cloud App Security détecte les ransomwares, consultez [Protection de votre organisation contre les ransomwares](use-case-ransomware.md).

**Activité effectuée par utilisateur résilié**

- Cette détection permet de déterminer si un employé en fin de contrat continue d’effectuer des actions sur vos applications SaaS. Étant donné que les données montrent que le plus grand risque de menaces internes vient des employés partis en mauvais termes, il est important de garder un œil sur l’activité des comptes des employés dont le contrat de travail est terminé. Parfois, quand un employé quitte une entreprise, son compte est déprovisionné des applications d’entreprise, mais dans de nombreux cas, il conserve quand même un accès à certaines ressources de l’entreprise. Ces menaces sont encore plus importantes quand il s’agit de comptes privilégiés, puisque le risque de dommage causé par un ancien administrateur est par définition plus élevé.
Cette détection exploite la capacité de Cloud App Security à surveiller le comportement de l’utilisateur dans toutes les applications, ce qui permet d’identifier l’activité normale de l’utilisateur, le fait que le compte a été résilié et l’activité réelle dans d’autres applications. Par exemple, un employé dont le compte Azure AD a été résilié, mais qui a encore accès à l’infrastructure AWS de l’entreprise, est en mesure de provoquer des dégâts à grande échelle.  

La détection recherche les utilisateurs dont le compte a été clôturé dans Azure AD, mais qui effectuent encore des activités sur d’autres plateformes comme AWS ou Salesforce. Cela est particulièrement pertinent pour les utilisateurs qui utilisent un autre compte (pas leur compte d’authentification unique principal) pour gérer les ressources, étant donné que ces comptes ne sont souvent pas clôturés lorsqu’un utilisateur quitte l’entreprise.

**Activité à partir d’adresses IP suspectes**
- Cette détection identifie que des utilisateurs étaient actifs à partir d’une adresse IP qui a été identifiée comme à risque par Microsoft Threat Intelligence. Ces adresses IP sont impliquées dans des activités malveillantes, comme Botnet C&C, et peuvent être le signe de compte compromis. Cette détection utilise un algorithme d’apprentissage automatique qui réduit les « faux positifs », comme les adresses IP mal balisées qui sont couramment utilisées par les utilisateurs de l’organisation.


**Transfert de boîte de réception suspect**

- Cette détection recherche les règles de transfert des e-mails suspects, par exemple, si un utilisateur a créé une règle de boîte de réception assurant le transfert d’une copie de tous les e-mails à une adresse externe. 
 
> [!NOTE]
> Cloud App Security vous avertit seulement pour chaque règle de transfert qui est identifiée comme suspecte, en fonction du comportement habituel pour l’utilisateur. 

**Règles de manipulation de boîte de réception suspecte**
- Cette détection profile votre environnement et déclenche des alertes quand des règles de boîte de réception suspectes qui suppriment ou déplacent des messages ou des dossiers sont définies sur la boîte de réception d’un utilisateur. Cela peut indiquer que le compte de l’utilisateur est compromis, que des messages sont masqués intentionnellement, et que la boîte aux lettres est utilisée pour distribuer du courrier indésirable ou des programmes malveillants dans votre organisation.

**Activités inhabituelles (par utilisateur)**<br>
Ces détections identifient les utilisateurs dans les cas suivants :

 - Plusieurs activités inhabituelles de téléchargement de fichiers
 - Activités inhabituelles de partage de fichiers
 - Activités inhabituelles de suppression de fichiers
 - Activités inhabituelles d'emprunt d'identité
 - Activités administratives inhabituelles
 
Ces stratégies recherchent les activités dans une seule session en prenant en compte la base de référence apprise, ce qui peut indiquer une tentative de violation. Ces détections s’appuient sur un algorithme d’apprentissage automatique qui profile le modèle de connexion des utilisateurs et réduit les « faux positifs ». Ces détections font partie du moteur de détection des anomalies global qui profile votre environnement et déclenchent des alertes suivant une base de référence qui a été définie par rapport à l’activité de votre organisation.

**Plusieurs tentatives de connexion infructueuses**
- Cette détection identifie des utilisateurs qui tentent de se connecter plusieurs fois sans succès dans une seule session en prenant en compte la base de référence apprise, ce qui peut indiquer une tentative de violation. 

**Exfiltration de données vers des applications non approuvées**
- Cette stratégie est activée automatiquement pour vous avertir quand un utilisateur ou une adresse IP utilise une application qui n’est pas approuvée pour effectuer une activité qui ressemble à une tentative d’exfiltration des informations en dehors de votre organisation.

**Plusieurs activités de suppression de machine virtuelle**
- Cette stratégie profile votre environnement et déclenche des alertes quand des utilisateurs suppriment plusieurs machines virtuelles dans une même session, relativement à la base de référence de votre organisation. Ceci peut indiquer une tentative de violation.


## Activer la gouvernance automatisée<a name="adp-automated-gov"></a>

Vous pouvez lancer des actions de correction automatisées sur les alertes générées par les stratégies de détection d’anomalie. 

1. Cliquez sur le nom de la stratégie de détection dans la page **Stratégie**.
2. Dans la fenêtre **Modifier la stratégie de détection d’anomalie** qui s’ouvre, sous **Gouvernance**, définissez les actions de correction que vous souhaitez pour chaque application connectée ou pour toutes les applications. 
3. Cliquez sur **Mettre à jour**.

## <a name="tune-anomaly-detection-policies"></a>Paramétrer des stratégies de détection d’anomalie

Pour que le moteur de détection d’anomalie supprime ou déclenche des alertes en fonction de vos préférences :
   - Dans la stratégie Voyage impossible, vous pouvez définir le curseur de sensibilité pour déterminer le niveau d’un comportement anormal nécessaire avant qu’une alerte ne soit déclenchée. Par exemple, si vous le définissez sur Faible, il supprime les alertes Voyage impossible des emplacements courants d’un utilisateur, et si vous le définissez sur Élevé, il déclenche ce type d’alerte. 

   - Vous pouvez également configurer si les alertes pour Activité à partir de pays peu fréquents, d’adresses IP anonymes, d’adresses IP suspectes et Voyage impossible doivent analyser les échecs et les réussites de connexion ou juste les réussites de connexion. 
   
   
## <a name="scope-anomaly-detection-policies"></a>Délimiter des stratégies de détection d’anomalie

Chaque stratégie de détection d’anomalie peut être délimitée indépendamment. Vous pouvez donc inclure et exclure les utilisateurs et les groupes de votre choix.
Par exemple, vous pouvez configurer l’option Activité à partir de pays peu fréquents de manière à ignorer un utilisateur qui voyage fréquemment. 

Pour délimiter une stratégie de détection d’anomalie :
1. Cliquez sur **Contrôle** > **Stratégies**, puis définissez le filtre **Type** sur **Stratégie de détection d’anomalie**.
2. Cliquez sur la stratégie que vous souhaitez délimiter.
3. Sous **Étendue**, dans la liste déroulante, remplacez la valeur par défaut **Tous les utilisateurs et groupes** par **Utilisateurs et groupes spécifiques**. 
4. Sélectionnez **Inclure** pour spécifier les utilisateurs et les groupes auxquels s’applique cette stratégie. Les utilisateurs ou les groupes qui ne sont pas sélectionnés ici ne seront pas considérés comme une menace et ne généreront pas d’alerte.
5. Sélectionnez **Exclure** pour spécifier les utilisateurs pour lesquels cette stratégie ne s’applique pas. Les utilisateurs sélectionnés ici ne seront pas considérés comme une menace et ne généreront pas d’alerte, même s’ils sont membres de groupes qui ont été sélectionnés sous **Inclure**.

 ![Délimitation des stratégies de détection d’anomalie](./media/anomaly-detection-scoping.png)
## <a name="triage-anomaly-detection-alerts"></a>Alertes de détection des anomalies de triage

Vous pouvez trier rapidement les diverses alertes déclenchées par les nouvelles stratégies de détection des anomalies afin de déterminer celles qui doivent être prises en charge en priorité. Pour cela, vous avez besoin du contexte de l’alerte, afin de pouvoir obtenir une vue plus globale et identifier si une action malveillante se produit effectivement.  

1. Dans le **journal d’activité**, vous pouvez ouvrir une activité afin d’afficher son contenu. Cliquez sur **Utilisateur** pour afficher l’onglet Insights utilisateur. Cet onglet inclut des informations comme le nombre d’alertes, les activités et les emplacements à partir desquels l’utilisateur s’est connecté, ce qui est important dans le cadre d’une enquête. 

   ![alerte de détection des anomalies1](./media/anomaly-alert-user1.png)
   ![alerte de détection des anomalies1](./media/anomaly-alert-user2.png)
 
2. Cela vous permet d’identifier les activités suspectes que l’utilisateur a effectuées et d’obtenir ainsi plus d’indices démontrant que le compte a été compromis. Par exemple, une alerte sur plusieurs échecs de connexion peut en effet être suspecte et indiquer une éventuelle attaque par force brute, mais elle peut également signaler un problème de configuration d’application, transformant cette alerte en un « faux positif » bénin. Mais si vous voyez une alerte d’échecs de connexion pour d’autres activités suspectes, la probabilité que le compte est compromis augmente. Dans l’exemple ci-dessous, vous pouvez voir que l’alerte **Plusieurs tentatives de connexion infructueuses** a été suivie par les alertes **Activité à partir d’une adresse IP TOR** et **Activité de type Voyage impossible**, deux indicateurs flagrants d’une compromission (IOCs). Si cela n’était pas assez suspect, vous pouvez constater que le même utilisateur a effectué une **activité de téléchargement en masse**, ce qui est souvent un indicateur qu’une personne malveillante tente d’exfiltrer des données. 

   ![alerte 1 de la détection d’anomalie](./media/anomaly-alert-user3.png)


3. Une fois que les fichiers infectés sont détectés, vous pouvez voir une liste des **fichiers infectés**. Cliquez sur le nom du fichier malveillant dans le tiroir de fichier pour ouvrir un rapport sur les programmes malveillants qui vous fournit des informations sur le type de programme malveillant dont le fichier est infecté. 


  

  
## <a name="next-steps"></a>Étapes suivantes 
[Activités quotidiennes pour protéger votre environnement cloud](daily-activities-to-protect-your-cloud-environment.md)   

[Les clients Premier peuvent également créer une demande de support directement dans le portail Premier.](https://premier.microsoft.com/)  
  
  
