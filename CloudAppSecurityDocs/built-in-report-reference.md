---
title: "Informations de référence sur les rapports intégrés | Documentation Microsoft"
description: "Cette rubrique fournit une liste des rapports intégrés et leurs utilisations."
keywords: 
author: rkarlin
ms.author: rkarlin
manager: mbaldwin
ms.date: 10/15/2016
ms.topic: article
ms.prod: 
ms.service: cloud-app-security
ms.technology: 
ms.assetid: 588b3639-f748-45a6-bc4b-a6ee47c1865e
ms.reviewer: reutam
ms.suite: ems
translationtype: Human Translation
ms.sourcegitcommit: ed4ea71b24767d3602d40894d1cbac7447bcd8a2
ms.openlocfilehash: 520017dab0301fe2a64c7b82d5e14c71efb2522f


---

# <a name="builtin-report-reference"></a>Informations de référence sur les rapports intégrés
Nous vous recommandons de créer vos rapports personnalisés à partir de rapports intégrés, qui font ainsi office de modèle. Le tableau suivant dresse la liste des rapports intégrés et indique les types d’événements que vous pouvez surveiller avec ces rapports.  
  
## <a name="builtin-report-list"></a>Liste des rapports intégrés  
  
|Type de rapport|Nom du rapport intégré|Description|  
|-----------------|---------------------------|-----------------|  
|Sécurité|Activité par lieu|Ce rapport répertorie les pays d’où provient une activité dans vos applications cloud et différents paramètres représentant le volume d’activité dans chaque pays, tels que le nombre d’événements, le nombre d’utilisateurs, etc. Utilisez-le pour obtenir une vue d’ensemble de la distribution géographique de vos utilisateurs.|  
|Sécurité|Source d’activité par utilisateur|Utilisateurs qui ont effectué une activité dans l’environnement cloud à partir de plusieurs emplacements ou en utilisant trop d’adresses IP. Ces utilisateurs pouvant, toutefois, être en déplacement, il est possible que leurs informations d’identification soient utilisées à mauvais escient.|  
|Sécurité|Utilisation du navigateur|Les attaques par navigation font partie des vecteurs d’attaque les plus courants. Les fournisseurs investissent des ressources considérables dans la sécurisation des logiciels de navigation, créant un mécanisme de mise à jour efficace pour diffuser les mises à jour vers les points de terminaison. L’utilisation de navigateurs déconseillés longtemps après leur dernière mise à jour en fait des cibles de choix pour les entités malveillantes qui recourent à des kits d’attaque. Ce rapport répertorie les navigateurs utilisés au cours des 30 derniers jours par les utilisateurs qui accèdent à vos services cloud.|  
|Sécurité|Adresses IP|Ce rapport répertorie les adresses IP utilisées par les appareils pour effectuer des activités dans votre environnement cloud protégé par Cloud App Security. Ce rapport est basé sur les journaux d’audit accumulés par Cloud App Security. Les adresses IP sont généralement associées à un emplacement géographique et à une organisation source. Utilisez ce rapport pour identifier les adresses IP suspectes qui se connectent à vos services protégés. Vous pouvez afficher les journaux d’audit propres à une adresse IP en cliquant sur celle-ci.|  
|Sécurité|Adresses IP - comptes disposant de privilèges|Ce rapport répertorie les adresses IP utilisées par les appareils pour effectuer des activités administratives dans votre environnement cloud protégé par Cloud App Security. Ce rapport est basé sur les journaux d’audit accumulés par Cloud App Security. Les adresses IP sont généralement associées à un emplacement géographique et à une organisation source. Utilisez ce rapport pour identifier les adresses IP suspectes qui se connectent à vos services protégés. Vous pouvez afficher les journaux d’audit propres à une adresse IP en cliquant sur celle-ci.|  
|Sécurité|Utilisation du système d’exploitation|Les défauts de sécurité du système d’exploitation ont tendance à provoquer des vulnérabilités très dangereuses. Les fournisseurs investissent des ressources considérables dans la sécurisation des systèmes d’exploitation, créant un mécanisme de mise à jour efficace pour diffuser les mises à jour vers les points de terminaison. Toutefois, les systèmes d’exploitation déconseillés qui ne sont plus pris en charge ne sont pas inclus dans ces mécanismes de mise à jour et deviennent des cibles de choix pour les entités malveillantes qui recourent à des kits d’attaque. Ce rapport répertorie les systèmes d’exploitation utilisés au cours des 30 derniers jours par les utilisateurs qui accèdent à vos services cloud.|  
|Sécurité|Utilisateurs distants véritables|Les utilisateurs suivants n’ont jamais partagé une adresse IP avec un autre employé de la société. Cela est caractéristique des employés ou équipes distants, des prestataires embauchés et des services de support externes. Toutefois, cela peut également indiquer une porte dérobée laissée par une personne malveillante.|  
|Gestion des utilisateurs|Vue d’ensemble de l’application cloud|Ce rapport répertorie vos applications cloud et différents paramètres qui représentent le volume d’activité dans chaque application, comme le nombre de fichiers, d’utilisateurs, etc. Utilisez-le pour obtenir une vue d’ensemble des différentes applications et de leur degré d’utilisation par vos utilisateurs.|  
|Gestion des utilisateurs|Comptes inactifs|Les comptes inactifs sont des comptes qui ont accès à votre instance cloud, mais qui ne sont à l’origine d’aucun événement au cours des 60 derniers jours. Il est possible que ces comptes ne soient plus actifs et qu’ils doivent être suspendus pour empêcher tout accès de la part d’entités malveillantes ou d’employés sur le départ. Le respect de cette bonne pratique non seulement améliore votre posture de sécurité, mais permet également de réduire les coûts d’exploitation.|  
|Gestion des utilisateurs|Utilisateurs disposant de privilèges|Ce rapport répertorie les utilisateurs qui ont des privilèges élevés dans les services d’entreprise, tels que les administrateurs. Les comptes disposant de privilèges de ce type sont un vecteur d’attaque de choix pour les entités malveillantes, car ils peuvent leur permettre d’accéder largement à la configuration réseau et aux informations de l’entreprise. Si des comptes disposant de privilèges n’ont pas été utilisés au cours du mois dernier, cela peut indiquer un manque de sensibilisation à la sécurité informatique dans les entreprises, pouvant favoriser une vague de violations de données. Vous pouvez examiner l’utilisation des privilèges utilisateur élevés par le biais du journal d’audit et envisager la révocation des privilèges superflus.|  
|Gestion des utilisateurs|Comptes spéciaux disposant de privilèges|Salesforce a plusieurs types de comptes disposant de privilèges, tels que la modification de toutes les données, l’affichage de toutes les données et la gestion de tous les utilisateurs. Les comptes disposant de privilèges de ce type sont un vecteur d’attaque de choix pour les entités malveillantes, car ils peuvent leur permettre d’accéder largement aux configurations et informations de l’entreprise.|  
|Gestion des utilisateurs|Ouverture de session de l’utilisateur|Ce rapport détaille le nombre de tentatives de connexion, le nombre de connexions réussies et le pourcentage de tentatives de connexion infructueuses effectuées par chaque utilisateur dans chaque service. Un pourcentage élevé de tentatives de connexion ayant échoué peut indiquer qu’un compte d’utilisateur a fait l’objet d’une attaque à un moment donné.|  
|Gestion des données|Rétention de données|Les stratégies de rétention de données traitent des questions liées à la conservation des informations pendant une période prédéterminée, des procédures d’archivage des informations, des recommandations en matière de destruction des informations quand le délai a été dépassé et des mécanismes spéciaux de gestion des informations en cas de litige. La rétention de données est un acte d’équilibrage complexe. D’un côté, vous devez enregistrer les informations requises par la loi et vitales pour votre entreprise. De l’autre, il est tout à fait opportun de supprimer les données sans intérêt, obsolètes et non productives aussi rapidement que possible. L’utilisation du cloud pour le stockage des données a accru la complexité du problème. Les données du cloud, à l’image des données imprimées classiques, doivent toujours être conservées un certain temps pour satisfaire à des contraintes légales, commerciales et personnelles. Un autre avantage de l’application de stratégies de rétention de données dans votre environnement cloud est la possibilité de libérer de l’espace de stockage, réduisant ainsi les coûts d’exploitation du cloud. Le rapport suivant vous offre une visibilité des données stockées dans votre environnement cloud, étape essentielle pour que celui-ci bénéficie des stratégies de rétention de données existantes.|  
|Gestion des données|Vue d’ensemble du partage de données|Ce rapport répertorie le nombre de fichiers stockés dans vos services cloud, par autorisation d’accès. Le partage est devenu très facile avec les services cloud en raison de la facilité d’accès et de l’omniprésence.<br /><br /> Un fichier qui n’est partagé avec personne d’autre que son propriétaire est appelé fichier privé. Si le fichier est partagé, Cloud App Security distingue quatre types d’états :<br /><br /> Un fichier (web) partagé publiquement est un fichier accessible sans aucune authentification, même par le biais d’un résultat de moteur de recherche.<br /><br /> Un fichier partagé publiquement est un fichier accessible sans aucune authentification, au moyen d’un lien.<br /><br /> Un fichier partagé en externe est un fichier auquel peuvent accéder des personnes n’appartenant pas à l’organisation une fois qu’elles se sont authentifiées auprès du service cloud.<br /><br /> Un fichier partagé en interne est un fichier accessible à la totalité ou à une partie des utilisateurs de votre organisation.|  
|Gestion des données|Extensions de fichier|Ce rapport répertorie les extensions des fichiers stockés dans vos services cloud. Utilisez-le pour obtenir une vue d’ensemble des types de fichiers dans votre cloud et de la façon dont ils sont partagés.|  
|Gestion des données|Partage entrant par domaine|Ce rapport répertorie les domaines à partir desquels des fichiers sont partagés avec vos employés. Pour chaque domaine, le rapport détaille les collaborateurs qui partagent des fichiers, le nombre de fichiers partagés et avec qui les fichiers des utilisateurs de l’entreprise sont partagés. L’acceptation de la collaboration externe étant implicite, vous n’avez pas besoin d’appliquer une stratégie à vos employés. Toutefois, vous pouvez vous trouver dans la situation où des fichiers censés être des fichiers d’entreprise sont détenus en externe et accessibles via le partage, pouvant, dans le pire des cas, servir de vecteur à des attaques par hameçonnage contre vos employés.|  
|Gestion des données|Fichiers orphelins|Ce rapport répertorie les utilisateurs qui sont suspendus, mais qui possèdent toujours des fichiers dans un de vos services cloud protégés par Cloud App Security. Ces fichiers ne sont pas gérés, ni pris en compte, s’ils violent une conformité ou stratégie. Ils doivent être supprimés ou voir leur propriété transférée à un utilisateur actif.|  
|Gestion des données|Partage sortant par domaine|Ce rapport répertorie les domaines avec lesquels des fichiers d’entreprise sont partagés par vos employés. Pour chaque domaine, le rapport détaille les utilisateurs de l’entreprise qui partagent des fichiers avec ce domaine, les fichiers effectivement partagés et les collaborateurs avec lesquels ces fichiers sont partagés. Nous vous recommandons de gérer le partage avec ces domaines par le biais de l’onglet Fichiers de la page relative à chaque service concerné.|  
|Gestion des données|Propriétaires de fichiers partagés|Ce rapport répertorie les utilisateurs qui partagent des fichiers d’entreprise avec le monde extérieur. Les fichiers partagés en externe sont partagés avec des collaborateurs externes spécifiques. Les fichiers partagés publiquement sont accessibles sur Internet à toute personne par le biais d’une liaison privée à laquelle cette personne est explicitement exposée. Les fichiers partagés publiquement (Internet) sont accessibles à toute personne sur Internet, même par le biais d’un résultat de moteur de recherche.  Si vous constatez que des utilisateurs partagent un nombre excessif de fichiers, nous vous recommandons d’examiner la nature des autorisations correspondantes à l’aide de l’onglet Fichiers et de contacter ces utilisateurs pour mieux comprendre la façon dont ils recourent au partage externe.|  
|Gestion des données|Comptes utilisateur personnel|Ce rapport répertorie les comptes utilisateur externes ayant accès à des fichiers dans vos services cloud protégés par Cloud App Security, comptes considérés comme des comptes utilisateur personnel. Le propriétaire présumé de chaque compte personnel est indiqué dans la colonne Utilisateur société. L’association est calculée à l’aide de notre algorithme propriétaire. Le partage de données d’entreprise avec les comptes personnels des employés pose une menace pour vos documents sensibles pour les raisons suivantes :<br /><br /> (1) Les comptes personnels ne sont pas configurés par vos équipes de sécurité et informatique. Ils peuvent être compromis à leur insu et ne sont pas soumis à la stratégie de sécurité de l’entreprise (par exemple, la réinitialisation du mot de passe).<br /><br /> (2) Les utilisateurs peuvent partager des données d’entreprise sur leurs comptes personnels avec moins de précautions que s’il s’agissait de collaborateurs externes.<br /><br /> (3) Les collaborateurs internes peuvent faire l’objet d’attaques par piratage psychologique. Un pirate peut utiliser un compte dont le nom est similaire à celui d’un des employés (par exemple, john.doe@contoso.com ou jdoe12@gmail.com) et obtenir un accès en demandant une autorisation sur des données sensibles. Les collaborateurs internes peuvent involontairement partager des données d’entreprise avec le compte du pirate. L’utilisation de comptes personnels est déconseillée par Cloud App Security.|  
|Gestion des données|Noms de fichier sensible|Ce rapport répertorie les fichiers qui requièrent votre attention, car leur autorisation de partage n’est peut-être pas compatible avec leur contenu au regard d’une analyse heuristique de leurs noms. Cette analyse heuristique est utile pour identifier les fichiers sensibles sans recourir à une analyse de contenu complète. Chaque fichier dans le rapport est considéré comme sensible, car l’analyse l’a identifié comme appartenant aux catégories décrites dans la colonne « Catégories ».|  
  
## <a name="see-also"></a>Voir aussi  
[Contrôler](control.md)   
[Pour obtenir un support technique, visitez la page de support assisté Cloud App Security.](http://support.microsoft.com/oas/default.aspx?prid=16031)   
[Les clients Premier peuvent également choisir Cloud App Security directement depuis le portail Premier.](https://premier.microsoft.com/)  
  
  


<!--HONumber=Oct16_HO4-->

