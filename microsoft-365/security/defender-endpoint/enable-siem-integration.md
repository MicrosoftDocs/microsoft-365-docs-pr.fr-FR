---
title: Activer l’intégration SIEM dans Microsoft Defender pour endpoint
description: Activez l’intégration SIEM pour recevoir des détections dans votre solution de gestion des événements et des informations de sécurité (SIEM).
keywords: activer un connecteur siem, un siem, un connecteur, des informations de sécurité et des événements
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 87078bb7bfc6b38788fea2a6a4c3c9108be1d5b4
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52842961"
---
# <a name="enable-siem-integration-in-microsoft-defender-for-endpoint"></a>Activer l’intégration SIEM dans Microsoft Defender pour endpoint

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

**S’applique à :**
- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/?linkid=2154037)


>Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-enablesiem-abovefoldlink) 

Activez l’intégration des informations de sécurité et de la gestion des événements (SIEM) afin de pouvoir tirer les détections de Centre de sécurité Microsoft Defender. Tirez les détections à l’aide de votre solution SIEM ou en vous connectant directement à l’API REST de détections.

>[!NOTE]
>- [Microsoft Defender pour l’alerte de point de terminaison](alerts.md) est composé d’une ou plusieurs détections.
>- [Microsoft Defender pour la détection des points](api-portal-mapping.md) de terminaison est composé de l’événement suspect qui s’est produit sur l’appareil et de ses détails d’alerte associés.
>- L’API d’alerte Microsoft Defender pour point de terminaison est la dernière API pour la consommation des alertes et contient une liste détaillée des preuves associées à chaque alerte. Pour plus d’informations, voir [Méthodes et propriétés d’alerte et](alerts.md) Liste des [alertes.](get-alerts.md)

## <a name="prerequisites"></a>Configuration requise

- L’utilisateur qui active le paramètre doit être autorisé à créer une application dans Azure Active Directory (AAD). Il s’agit d’une personne ayant les rôles suivants : 

  - Administrateur de sécurité et administrateur général
  - Administrateur de l'application cloud
  - Administrateur de l'application
  - Propriétaire du principal de service

- Au cours de l’activation initiale, un écran de saisie intitulant les informations d’identification s’affiche. Veillez à autoriser les fenêtres pop-up pour ce site.

## <a name="enabling-siem-integration"></a>Activation de l’intégration SIEM 
1. Dans le volet de navigation, sélectionnez **Paramètres**  >  **SIEM.**

    ![Image de l’intégration SIEM à partir Paramètres menu1](images/enable_siem.png)

    >[!TIP]
    >Si vous rencontrez une erreur lors de la tentative d’activer l’application de connecteur SIEM, vérifiez les paramètres du bloqueur de fenêtres d’accès rapide de votre navigateur. Il peut bloquer l’ouverture de la nouvelle fenêtre lorsque vous activez la fonctionnalité. 

2. Sélectionnez **Activer l’intégration SIEM.** Cette action active la section détails d’accès au connecteur SIEM avec des **valeurs** pré-remplies et une application est créée sous votre client Azure Active Directory (Azure AD).

    > [!WARNING]
    >La secret client n’est affichée qu’une seule fois. Veillez à en conserver une copie en lieu sûr.<br>
     

    ![Image de l’intégration SIEM à partir Paramètres menu2](images/siem_details.png)

3. Choisissez le type SIEM que vous utilisez dans votre organisation.

   > [!NOTE]
   > Si vous sélectionnez HP ArcSight, vous devez enregistrer ces deux fichiers de configuration :<br>
   > - WDATP-connector.jsonparser.properties
   > - WDATP-connector.properties <br>

   Si vous souhaitez vous connecter directement à l’API REST de détections par le biais d’un accès par programmation, choisissez **l’API générique.**

4. Copiez les valeurs individuelles ou **sélectionnez Enregistrer les détails dans** le fichier pour télécharger un fichier qui contient toutes les valeurs.

5. Sélectionnez **Générer des jetons pour** obtenir un jeton d’accès et d’actualisation.
  
   > [!NOTE]
   > Vous devez générer un nouveau jeton Actualiser tous les 90 jours. 

6. Suivez les instructions pour créer une inscription d’application Azure AD pour [Microsoft Defender pour endpoint](/microsoft-365/security/defender-endpoint/exposed-apis-create-app-webapp) et attribuez-lui les autorisations correctes pour lire les alertes.

Vous pouvez désormais configurer votre solution SIEM ou vous connecter à l’API REST de détections par le biais d’un accès par programme. Vous devrez utiliser les jetons lors de la configuration de votre solution SIEM pour lui permettre de recevoir des détections de Centre de sécurité Microsoft Defender.

## <a name="integrate-microsoft-defender-for-endpoint-with-ibm-qradar"></a>Intégrer Microsoft Defender for Endpoint à IBM QRadar 
Vous pouvez configurer IBM QRadar pour collecter des détections à partir de Microsoft Defender for Endpoint. Pour plus d’informations, voir [le Centre de connaissances IBM.](https://www.ibm.com/support/knowledgecenter/SS42VS_DSM/c_dsm_guide_MS_Win_Defender_ATP_overview.html?cp=SS42VS_7.3.1)

## <a name="see-also"></a>Voir aussi
- [Configurer HP ArcSight pour tirer microsoft Defender pour les détections de points de terminaison](configure-arcsight.md)
- [Champs Microsoft Defender pour la détection des points de terminaison](api-portal-mapping.md)
- [Détecter Microsoft Defender pour les points de terminaison à l’aide de l’API REST](pull-alerts-using-rest-api.md)
- [Résoudre des problèmes d’intégration de l’outil SIEM](troubleshoot-siem.md)
