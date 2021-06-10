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
# <a name="enable-siem-integration-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="04906-104">Activer l’intégration SIEM dans Microsoft Defender pour endpoint</span><span class="sxs-lookup"><span data-stu-id="04906-104">Enable SIEM integration in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="04906-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="04906-105">**Applies to:**</span></span>
- [<span data-ttu-id="04906-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="04906-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)


><span data-ttu-id="04906-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="04906-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="04906-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="04906-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-enablesiem-abovefoldlink) 

<span data-ttu-id="04906-109">Activez l’intégration des informations de sécurité et de la gestion des événements (SIEM) afin de pouvoir tirer les détections de Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="04906-109">Enable security information and event management (SIEM) integration so you can pull detections from Microsoft Defender Security Center.</span></span> <span data-ttu-id="04906-110">Tirez les détections à l’aide de votre solution SIEM ou en vous connectant directement à l’API REST de détections.</span><span class="sxs-lookup"><span data-stu-id="04906-110">Pull detections using your SIEM solution or by connecting directly to the detections REST API.</span></span>

>[!NOTE]
>- <span data-ttu-id="04906-111">[Microsoft Defender pour l’alerte de point de terminaison](alerts.md) est composé d’une ou plusieurs détections.</span><span class="sxs-lookup"><span data-stu-id="04906-111">[Microsoft Defender for Endpoint Alert](alerts.md) is composed from one or more detections.</span></span>
>- <span data-ttu-id="04906-112">[Microsoft Defender pour la détection des points](api-portal-mapping.md) de terminaison est composé de l’événement suspect qui s’est produit sur l’appareil et de ses détails d’alerte associés.</span><span class="sxs-lookup"><span data-stu-id="04906-112">[Microsoft Defender for Endpoint Detection](api-portal-mapping.md) is composed from the suspicious event occurred on the Device and its related Alert details.</span></span>
>- <span data-ttu-id="04906-113">L’API d’alerte Microsoft Defender pour point de terminaison est la dernière API pour la consommation des alertes et contient une liste détaillée des preuves associées à chaque alerte.</span><span class="sxs-lookup"><span data-stu-id="04906-113">The Microsoft Defender for Endpoint Alert API is the latest API for alert consumption and contain a detailed list of related evidence for each alert.</span></span> <span data-ttu-id="04906-114">Pour plus d’informations, voir [Méthodes et propriétés d’alerte et](alerts.md) Liste des [alertes.](get-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="04906-114">For more information, see [Alert methods and properties](alerts.md) and [List alerts](get-alerts.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="04906-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04906-115">Prerequisites</span></span>

- <span data-ttu-id="04906-116">L’utilisateur qui active le paramètre doit être autorisé à créer une application dans Azure Active Directory (AAD).</span><span class="sxs-lookup"><span data-stu-id="04906-116">The user who activates the setting must have permissions to create an app in Azure Active Directory (AAD).</span></span> <span data-ttu-id="04906-117">Il s’agit d’une personne ayant les rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="04906-117">This is someone with the following roles:</span></span> 

  - <span data-ttu-id="04906-118">Administrateur de sécurité et administrateur général</span><span class="sxs-lookup"><span data-stu-id="04906-118">Security Administrator and either Global Administrator</span></span>
  - <span data-ttu-id="04906-119">Administrateur de l'application cloud</span><span class="sxs-lookup"><span data-stu-id="04906-119">Cloud Application Administrator</span></span>
  - <span data-ttu-id="04906-120">Administrateur de l'application</span><span class="sxs-lookup"><span data-stu-id="04906-120">Application Administrator</span></span>
  - <span data-ttu-id="04906-121">Propriétaire du principal de service</span><span class="sxs-lookup"><span data-stu-id="04906-121">Owner of the service principal</span></span>

- <span data-ttu-id="04906-122">Au cours de l’activation initiale, un écran de saisie intitulant les informations d’identification s’affiche.</span><span class="sxs-lookup"><span data-stu-id="04906-122">During the initial activation, a pop-up screen is displayed for credentials to be entered.</span></span> <span data-ttu-id="04906-123">Veillez à autoriser les fenêtres pop-up pour ce site.</span><span class="sxs-lookup"><span data-stu-id="04906-123">Make sure that you allow pop-ups for this site.</span></span>

## <a name="enabling-siem-integration"></a><span data-ttu-id="04906-124">Activation de l’intégration SIEM</span><span class="sxs-lookup"><span data-stu-id="04906-124">Enabling SIEM integration</span></span> 
1. <span data-ttu-id="04906-125">Dans le volet de navigation, sélectionnez **Paramètres**  >  **SIEM.**</span><span class="sxs-lookup"><span data-stu-id="04906-125">In the navigation pane, select **Settings** > **SIEM**.</span></span>

    ![Image de l’intégration SIEM à partir Paramètres menu1](images/enable_siem.png)

    >[!TIP]
    ><span data-ttu-id="04906-127">Si vous rencontrez une erreur lors de la tentative d’activer l’application de connecteur SIEM, vérifiez les paramètres du bloqueur de fenêtres d’accès rapide de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="04906-127">If you encounter an error when trying to enable the SIEM connector application, check the pop-up blocker settings of your browser.</span></span> <span data-ttu-id="04906-128">Il peut bloquer l’ouverture de la nouvelle fenêtre lorsque vous activez la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="04906-128">It might be blocking the new window being opened when you enable the capability.</span></span> 

2. <span data-ttu-id="04906-129">Sélectionnez **Activer l’intégration SIEM.**</span><span class="sxs-lookup"><span data-stu-id="04906-129">Select **Enable SIEM integration**.</span></span> <span data-ttu-id="04906-130">Cette action active la section détails d’accès au connecteur SIEM avec des **valeurs** pré-remplies et une application est créée sous votre client Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="04906-130">This activates the **SIEM connector access details** section with pre-populated values and an application is created under your Azure Active Directory (Azure AD) tenant.</span></span>

    > [!WARNING]
    ><span data-ttu-id="04906-131">La secret client n’est affichée qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="04906-131">The client secret is only displayed once.</span></span> <span data-ttu-id="04906-132">Veillez à en conserver une copie en lieu sûr.</span><span class="sxs-lookup"><span data-stu-id="04906-132">Make sure you keep a copy of it in a safe place.</span></span><br>
     

    ![Image de l’intégration SIEM à partir Paramètres menu2](images/siem_details.png)

3. <span data-ttu-id="04906-134">Choisissez le type SIEM que vous utilisez dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="04906-134">Choose the SIEM type you use in your organization.</span></span>

   > [!NOTE]
   > <span data-ttu-id="04906-135">Si vous sélectionnez HP ArcSight, vous devez enregistrer ces deux fichiers de configuration :</span><span class="sxs-lookup"><span data-stu-id="04906-135">If you select HP ArcSight, you'll need to save these two configuration files:</span></span><br>
   > - <span data-ttu-id="04906-136">WDATP-connector.jsonparser.properties</span><span class="sxs-lookup"><span data-stu-id="04906-136">WDATP-connector.jsonparser.properties</span></span>
   > - <span data-ttu-id="04906-137">WDATP-connector.properties</span><span class="sxs-lookup"><span data-stu-id="04906-137">WDATP-connector.properties</span></span> <br>

   <span data-ttu-id="04906-138">Si vous souhaitez vous connecter directement à l’API REST de détections par le biais d’un accès par programmation, choisissez **l’API générique.**</span><span class="sxs-lookup"><span data-stu-id="04906-138">If you want to connect directly to the detections REST API through programmatic access, choose **Generic API**.</span></span>

4. <span data-ttu-id="04906-139">Copiez les valeurs individuelles ou **sélectionnez Enregistrer les détails dans** le fichier pour télécharger un fichier qui contient toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="04906-139">Copy the individual values or select **Save details to file** to download a file that contains all the values.</span></span>

5. <span data-ttu-id="04906-140">Sélectionnez **Générer des jetons pour** obtenir un jeton d’accès et d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="04906-140">Select **Generate tokens** to get an access and refresh token.</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="04906-141">Vous devez générer un nouveau jeton Actualiser tous les 90 jours.</span><span class="sxs-lookup"><span data-stu-id="04906-141">You'll need to generate a new Refresh token every 90 days.</span></span> 

6. <span data-ttu-id="04906-142">Suivez les instructions pour créer une inscription d’application Azure AD pour [Microsoft Defender pour endpoint](/microsoft-365/security/defender-endpoint/exposed-apis-create-app-webapp) et attribuez-lui les autorisations correctes pour lire les alertes.</span><span class="sxs-lookup"><span data-stu-id="04906-142">Follow the instructions for [creating an Azure AD app registration for Microsoft Defender for Endpoint](/microsoft-365/security/defender-endpoint/exposed-apis-create-app-webapp) and assign the correct permissions to it to read alerts.</span></span>

<span data-ttu-id="04906-143">Vous pouvez désormais configurer votre solution SIEM ou vous connecter à l’API REST de détections par le biais d’un accès par programme.</span><span class="sxs-lookup"><span data-stu-id="04906-143">You can now proceed with configuring your SIEM solution or connecting to the detections REST API through programmatic access.</span></span> <span data-ttu-id="04906-144">Vous devrez utiliser les jetons lors de la configuration de votre solution SIEM pour lui permettre de recevoir des détections de Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="04906-144">You'll need to use the tokens when configuring your SIEM solution to allow it to receive detections from Microsoft Defender Security Center.</span></span>

## <a name="integrate-microsoft-defender-for-endpoint-with-ibm-qradar"></a><span data-ttu-id="04906-145">Intégrer Microsoft Defender for Endpoint à IBM QRadar</span><span class="sxs-lookup"><span data-stu-id="04906-145">Integrate Microsoft Defender for Endpoint with IBM QRadar</span></span> 
<span data-ttu-id="04906-146">Vous pouvez configurer IBM QRadar pour collecter des détections à partir de Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="04906-146">You can configure IBM QRadar to collect detections from Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="04906-147">Pour plus d’informations, voir [le Centre de connaissances IBM.](https://www.ibm.com/support/knowledgecenter/SS42VS_DSM/c_dsm_guide_MS_Win_Defender_ATP_overview.html?cp=SS42VS_7.3.1)</span><span class="sxs-lookup"><span data-stu-id="04906-147">For more information, see [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/SS42VS_DSM/c_dsm_guide_MS_Win_Defender_ATP_overview.html?cp=SS42VS_7.3.1).</span></span>

## <a name="see-also"></a><span data-ttu-id="04906-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04906-148">See also</span></span>
- [<span data-ttu-id="04906-149">Configurer HP ArcSight pour tirer microsoft Defender pour les détections de points de terminaison</span><span class="sxs-lookup"><span data-stu-id="04906-149">Configure HP ArcSight to pull Microsoft Defender for Endpoint detections</span></span>](configure-arcsight.md)
- [<span data-ttu-id="04906-150">Champs Microsoft Defender pour la détection des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="04906-150">Microsoft Defender for Endpoint Detection fields</span></span>](api-portal-mapping.md)
- [<span data-ttu-id="04906-151">Détecter Microsoft Defender pour les points de terminaison à l’aide de l’API REST</span><span class="sxs-lookup"><span data-stu-id="04906-151">Pull Microsoft Defender for Endpoint detections using REST API</span></span>](pull-alerts-using-rest-api.md)
- [<span data-ttu-id="04906-152">Résoudre des problèmes d’intégration de l’outil SIEM</span><span class="sxs-lookup"><span data-stu-id="04906-152">Troubleshoot SIEM tool integration issues</span></span>](troubleshoot-siem.md)
