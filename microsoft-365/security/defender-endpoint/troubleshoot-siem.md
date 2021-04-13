---
title: Résoudre les problèmes d'intégration de l'outil SIEM dans Microsoft Defender for Endpoint
description: Résoudre les problèmes qui peuvent survenir lors de l'utilisation des outils SIEM avec Microsoft Defender for Endpoint.
keywords: résoudre les problèmes, siem, secret client, secret
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
ms.topic: troubleshooting
ms.technology: mde
ms.openlocfilehash: 60220d00ca1b612564b72103b9206e3d6d89dc60
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51689448"
---
# <a name="troubleshoot-siem-tool-integration-issues"></a><span data-ttu-id="09d44-104">Résoudre des problèmes d’intégration de l’outil SIEM</span><span class="sxs-lookup"><span data-stu-id="09d44-104">Troubleshoot SIEM tool integration issues</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="09d44-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="09d44-105">**Applies to:**</span></span>
- [<span data-ttu-id="09d44-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="09d44-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="09d44-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="09d44-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="09d44-108">Vous souhaitez faire l'expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="09d44-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="09d44-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="09d44-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-pullalerts-abovefoldlink) 

<span data-ttu-id="09d44-110">Vous devrez peut-être résoudre les problèmes lors de l'analyse des détections dans vos outils SIEM.</span><span class="sxs-lookup"><span data-stu-id="09d44-110">You might need to troubleshoot issues while pulling detections in your SIEM tools.</span></span>

<span data-ttu-id="09d44-111">Cette page fournit des étapes détaillées pour résoudre les problèmes que vous pourriez rencontrer.</span><span class="sxs-lookup"><span data-stu-id="09d44-111">This page provides detailed steps to troubleshoot issues you might encounter.</span></span>


## <a name="learn-how-to-get-a-new-client-secret"></a><span data-ttu-id="09d44-112">Découvrez comment obtenir une nouvelle secret client</span><span class="sxs-lookup"><span data-stu-id="09d44-112">Learn how to get a new client secret</span></span>
<span data-ttu-id="09d44-113">Si votre secret client expire ou si vous avez mal placé la copie fournie lorsque vous activiez l'application d'outil SIEM, vous devez obtenir une nouvelle question secrète.</span><span class="sxs-lookup"><span data-stu-id="09d44-113">If your client secret expires or if you've misplaced the copy provided when you were enabling the SIEM tool application,  you'll need to get a new secret.</span></span>

1. <span data-ttu-id="09d44-114">Connectez-vous au [portail de gestion Azure.](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="09d44-114">Login to the [Azure management portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="09d44-115">Sélectionner **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="09d44-115">Select **Azure Active Directory**.</span></span>

3. <span data-ttu-id="09d44-116">Sélectionnez votre client.</span><span class="sxs-lookup"><span data-stu-id="09d44-116">Select your tenant.</span></span>

4. <span data-ttu-id="09d44-117">Cliquez **sur Inscriptions d'applications.**</span><span class="sxs-lookup"><span data-stu-id="09d44-117">Click **App registrations**.</span></span> <span data-ttu-id="09d44-118">Ensuite, dans la liste des applications, sélectionnez l'application.</span><span class="sxs-lookup"><span data-stu-id="09d44-118">Then in the applications list, select the application.</span></span>

5. <span data-ttu-id="09d44-119">Section **Sélectionner des** clés, puis fournir une description de la clé et spécifier la durée de validité de la clé.</span><span class="sxs-lookup"><span data-stu-id="09d44-119">Select **Keys** section, then provide a key description and specify the key validity duration.</span></span>

6. <span data-ttu-id="09d44-120">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="09d44-120">Click **Save**.</span></span> <span data-ttu-id="09d44-121">La valeur de clé s'affiche.</span><span class="sxs-lookup"><span data-stu-id="09d44-121">The key value is displayed.</span></span>

7. <span data-ttu-id="09d44-122">Copiez la valeur et enregistrez-la dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="09d44-122">Copy the value and save it in a safe place.</span></span>


## <a name="error-when-getting-a-refresh-access-token"></a><span data-ttu-id="09d44-123">Erreur lors de l'obtention d'un jeton d'accès d'actualisation</span><span class="sxs-lookup"><span data-stu-id="09d44-123">Error when getting a refresh access token</span></span>
<span data-ttu-id="09d44-124">Si vous rencontrez une erreur lors de la tentative d'obtenir un jeton d'actualisation lors de l'utilisation de l'API d'intelligence des menaces ou des outils SIEM, vous devez ajouter une URL de réponse pour l'application pertinente dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="09d44-124">If you encounter an error when trying to get a refresh token when using the threat intelligence API or SIEM tools, you'll need to add reply URL for relevant application in Azure Active Directory.</span></span>

1. <span data-ttu-id="09d44-125">Connectez-vous au [portail de gestion Azure.](https://ms.portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="09d44-125">Login to the [Azure management portal](https://ms.portal.azure.com).</span></span>

2. <span data-ttu-id="09d44-126">Sélectionner **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="09d44-126">Select **Azure Active Directory**.</span></span>

3. <span data-ttu-id="09d44-127">Sélectionnez votre client.</span><span class="sxs-lookup"><span data-stu-id="09d44-127">Select your tenant.</span></span>

4. <span data-ttu-id="09d44-128">Cliquez **sur Inscriptions d'applications.**</span><span class="sxs-lookup"><span data-stu-id="09d44-128">Click **App Registrations**.</span></span> <span data-ttu-id="09d44-129">Ensuite, dans la liste des applications, sélectionnez l'application.</span><span class="sxs-lookup"><span data-stu-id="09d44-129">Then in the applications list, select the application.</span></span>

5. <span data-ttu-id="09d44-130">Ajoutez l'URL suivante :</span><span class="sxs-lookup"><span data-stu-id="09d44-130">Add the following URL:</span></span>
   - <span data-ttu-id="09d44-131">Pour l'Union européenne : `https://winatpmanagement-eu.securitycenter.windows.com/UserAuthenticationCallback`</span><span class="sxs-lookup"><span data-stu-id="09d44-131">For the European Union: `https://winatpmanagement-eu.securitycenter.windows.com/UserAuthenticationCallback`</span></span>
   - <span data-ttu-id="09d44-132">Pour le Royaume-Uni : `https://winatpmanagement-uk.securitycenter.windows.com/UserAuthenticationCallback`</span><span class="sxs-lookup"><span data-stu-id="09d44-132">For the United Kingdom: `https://winatpmanagement-uk.securitycenter.windows.com/UserAuthenticationCallback`</span></span>
   - <span data-ttu-id="09d44-133">Pour les États-Unis  `https://winatpmanagement-us.securitycenter.windows.com/UserAuthenticationCallback` : .</span><span class="sxs-lookup"><span data-stu-id="09d44-133">For the United States:  `https://winatpmanagement-us.securitycenter.windows.com/UserAuthenticationCallback`.</span></span>
 
6. <span data-ttu-id="09d44-134">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="09d44-134">Click **Save**.</span></span>

## <a name="error-while-enabling-the-siem-connector-application"></a><span data-ttu-id="09d44-135">Erreur lors de l'activation de l'application de connecteur SIEM</span><span class="sxs-lookup"><span data-stu-id="09d44-135">Error while enabling the SIEM connector application</span></span>
<span data-ttu-id="09d44-136">Si vous rencontrez une erreur lors de la tentative d'activer l'application de connecteur SIEM, vérifiez les paramètres du bloqueur de fenêtres int gr es de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="09d44-136">If you encounter an error when trying to enable the SIEM connector application, check the pop-up blocker settings of your browser.</span></span> <span data-ttu-id="09d44-137">Il peut bloquer l'ouverture de la nouvelle fenêtre lorsque vous activez la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="09d44-137">It might be blocking the new window being opened when you enable the capability.</span></span>




><span data-ttu-id="09d44-138">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="09d44-138">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="09d44-139">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="09d44-139">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-troubleshootsiem-belowfoldlink) 

## <a name="related-topics"></a><span data-ttu-id="09d44-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09d44-140">Related topics</span></span>
- [<span data-ttu-id="09d44-141">Activer l'intégration SIEM dans Microsoft Defender pour endpoint</span><span class="sxs-lookup"><span data-stu-id="09d44-141">Enable SIEM integration in Microsoft Defender for Endpoint</span></span>](enable-siem-integration.md)
- [<span data-ttu-id="09d44-142">Configurer ArcSight pour tirer Microsoft Defender pour les détections de points de terminaison</span><span class="sxs-lookup"><span data-stu-id="09d44-142">Configure ArcSight to pull Microsoft Defender for Endpoint detections</span></span>](configure-arcsight.md)
- [<span data-ttu-id="09d44-143">Tirer les détections vers vos outils SIEM</span><span class="sxs-lookup"><span data-stu-id="09d44-143">Pull detections to your SIEM tools</span></span>](configure-siem.md)
- [<span data-ttu-id="09d44-144">Champs Microsoft Defender pour la détection des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="09d44-144">Microsoft Defender for Endpoint Detection fields</span></span>](api-portal-mapping.md)
- [<span data-ttu-id="09d44-145">Détecter Microsoft Defender pour les points de terminaison à l'aide de l'API REST</span><span class="sxs-lookup"><span data-stu-id="09d44-145">Pull Microsoft Defender for Endpoint detections using REST API</span></span>](pull-alerts-using-rest-api.md)
