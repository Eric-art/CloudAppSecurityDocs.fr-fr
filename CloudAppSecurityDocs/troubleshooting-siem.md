---
title: Résolution des problèmes d’intégration de SIEM – Cloud App Security | Microsoft Docs
description: Cet article liste les problèmes qui peuvent se produire lors de la connexion de votre SIEM à Cloud App Security et propose des solutions pour chacun d’eux.
keywords: ''
author: rkarlin
ms.author: rkarlin
manager: rkarlin
ms.date: 12/10/2018
ms.topic: conceptual
ms.collection: M365-security-compliance
ms.prod: ''
ms.service: cloud-app-security
ms.technology: ''
ms.assetid: de64d9ca-eaed-4243-bcf7-adca5aff18c8
ms.reviewer: reutam
ms.suite: ems
ms.custom: seodec18
ms.openlocfilehash: 47158a4fba1027f4e1ac3bfe0a73b2b1014375e8
ms.sourcegitcommit: 9f0c562322394a3dfac7f1d84286e673276a28b1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65568803"
---
# <a name="troubleshooting-the-siem-agent"></a>Résolution des problèmes de l’agent SIEM

*S’applique à : Microsoft Cloud App Security*

Cet article liste les problèmes qui peuvent se produire lors de la connexion de votre SIEM à Cloud App Security et propose des solutions possibles.

## <a name="troubleshooting"></a>Résolution des problèmes

Vérifiez que l’agent SIEM n’affiche pas l’état **Erreur de connexion** ou **Déconnecté** dans le portail Microsoft Cloud App Security et qu’il ne fait pas l’objet de notifications. Si la connexion est interrompue pendant plus de deux heures, l’état affiché est le suivant : **Erreur de connexion**. Si la connexion est interrompue depuis plus de 12 heures, l’état passe à **Déconnecté**.

Si vous voyez une des erreurs suivantes dans l’invite de commandes lors de l’exécution de l’agent, procédez comme suit pour corriger le problème :

|Erreur|Description|Résolution|
|----|----|----|
|Erreur générale pendant l’amorçage|Erreur inattendue pendant le démarrage de l’agent.|Contactez le support technique.|
|Trop d’erreurs critiques|Trop d’erreurs critiques se sont produites lors de la connexion de la console. Arrêt.|Contactez le support technique.|
|Jeton non valide|Le jeton fourni n’est pas valide.|Vérifiez que vous avez copié le jeton approprié. Vous pouvez utiliser le processus ci-dessus pour régénérer le jeton.|
|Erreur de proxy non valide|L’adresse de proxy fournie n’est pas valide.|Vérifiez que vous avez entré le proxy et le port appropriés.|


Après avoir créé l’agent, consultez la page de l’agent SIEM dans le portail Cloud App Security. Si vous voyez l’une des **Notifications de l’agent** suivantes, procédez comme suit pour corriger le problème :

|Erreur|Description|Résolution|
|----|----|----|
|**Erreur interne**|Quelque chose d’inconnu s’est produit avec votre agent SIEM.|Contactez le support technique.|
|**Erreur d’envoi du serveur de données**|Vous pouvez recevoir cette erreur si vous travaillez avec un serveur Syslog sur TCP. L’agent SIEM ne peut pas se connecter à votre serveur Syslog.  Si vous recevez cette erreur, l’agent cesse d’extraire de nouvelles activités tant qu’elle n’est pas résolue. Veillez à suivre les étapes de correction jusqu’à ce que l’erreur n’apparaisse plus.|1. Vérifiez que vous avez correctement défini votre serveur Syslog : Dans l’interface utilisateur de Cloud App Security, modifiez votre agent SIEM comme indiqué ci-dessus. Vérifiez que vous avez écrit correctement le nom du serveur et défini le port approprié. </br>2. Vérifiez la connectivité à votre serveur Syslog : Assurez-vous que le pare-feu ne bloque pas la communication.| 
|**Erreur de connexion du serveur de données**| Vous pouvez recevoir cette erreur si vous travaillez avec un serveur Syslog sur TCP. L’agent SIEM ne peut pas se connecter à votre serveur Syslog.  Si vous recevez cette erreur, l’agent cesse d’extraire de nouvelles activités tant qu’elle n’est pas résolue. Veillez à suivre les étapes de correction jusqu’à ce que l’erreur n’apparaisse plus.|1. Vérifiez que vous avez correctement défini votre serveur Syslog : Dans l’interface utilisateur de Cloud App Security, modifiez votre agent SIEM comme indiqué ci-dessus. Vérifiez que vous avez écrit correctement le nom du serveur et défini le port approprié. </br>2. Vérifiez la connectivité à votre serveur Syslog : Assurez-vous que le pare-feu ne bloque pas la communication.|
|**Erreur de l’agent SIEM**|L’agent SIEM est déconnecté depuis plus de X heures|Vérifiez que vous n’avez pas modifié la configuration de l’agent SIEM dans le portail Cloud App Security. Sinon, cette erreur peut signaler un problème de connectivité entre Cloud App Security et l’ordinateur sur lequel vous exécutez l’agent SIEM.|
|**Erreur de notification de l’agent SIEM**|Des erreurs de transfert de notification de l’agent SIEM ont été reçues d’un agent SIEM.|Cette erreur indique que vous avez reçu des erreurs concernant la connexion entre l’agent SIEM et votre serveur SIEM. Vérifiez qu’aucun pare-feu ne bloque votre serveur SIEM ou l’ordinateur sur lequel vous exécutez l’agent SIEM. Vérifiez aussi que l’adresse IP du serveur SIEM n’a pas changé.|


## <a name="next-steps"></a>Étapes suivantes
  
[Activités quotidiennes pour protéger votre environnement cloud](daily-activities-to-protect-your-cloud-environment.md)   

[Les clients Premier peuvent également créer une demande de support directement dans le portail Premier.](https://premier.microsoft.com/)  
  
