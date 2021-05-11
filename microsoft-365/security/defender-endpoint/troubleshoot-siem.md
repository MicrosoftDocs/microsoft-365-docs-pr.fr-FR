---
title: Résoudre les problèmes d’intégration de l’outil SIEM dans Microsoft Defender for Endpoint
description: Résoudre les problèmes qui peuvent survenir lors de l’utilisation des outils SIEM avec Microsoft Defender for Endpoint.
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
ms.openlocfilehash: 9c4f3da57796903fc22314574f389bcdd92ca4b3
ms.sourcegitcommit: efb932db63ad3ab4af4b585428d567d069410e4e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2021
ms.locfileid: "52311987"
---
# <a name="troubleshoot-siem-tool-integration-issues"></a><span data-ttu-id="6c012-104">Résoudre des problèmes d’intégration de l’outil SIEM</span><span class="sxs-lookup"><span data-stu-id="6c012-104">Troubleshoot SIEM tool integration issues</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="6c012-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6c012-105">**Applies to:**</span></span>
- [<span data-ttu-id="6c012-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6c012-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="6c012-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6c012-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="6c012-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6c012-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="6c012-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6c012-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-pullalerts-abovefoldlink) 

<span data-ttu-id="6c012-110">Vous devrez peut-être résoudre les problèmes lors de l’analyse des détections dans vos outils SIEM.</span><span class="sxs-lookup"><span data-stu-id="6c012-110">You might need to troubleshoot issues while pulling detections in your SIEM tools.</span></span>

<span data-ttu-id="6c012-111">Cette page fournit des étapes détaillées pour résoudre les problèmes que vous pourriez rencontrer.</span><span class="sxs-lookup"><span data-stu-id="6c012-111">This page provides detailed steps to troubleshoot issues you might encounter.</span></span>


## <a name="learn-how-to-get-a-new-client-secret"></a><span data-ttu-id="6c012-112">Découvrez comment obtenir une nouvelle secret client</span><span class="sxs-lookup"><span data-stu-id="6c012-112">Learn how to get a new client secret</span></span>
<span data-ttu-id="6c012-113">Si votre secret client expire ou si vous avez mal placé la copie fournie lorsque vous activiez l’application d’outil SIEM, vous devez obtenir une nouvelle question secrète.</span><span class="sxs-lookup"><span data-stu-id="6c012-113">If your client secret expires or if you've misplaced the copy provided when you were enabling the SIEM tool application,  you'll need to get a new secret.</span></span>

1. <span data-ttu-id="6c012-114">Connectez-vous au [portail de gestion Azure.](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="6c012-114">Login to the [Azure management portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="6c012-115">Sélectionner **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="6c012-115">Select **Azure Active Directory**.</span></span>

3. <span data-ttu-id="6c012-116">Sélectionnez votre client.</span><span class="sxs-lookup"><span data-stu-id="6c012-116">Select your tenant.</span></span>

4. <span data-ttu-id="6c012-117">Cliquez **sur Inscriptions d’applications.**</span><span class="sxs-lookup"><span data-stu-id="6c012-117">Click **App registrations**.</span></span> <span data-ttu-id="6c012-118">Ensuite, dans la liste des applications, sélectionnez l’application.</span><span class="sxs-lookup"><span data-stu-id="6c012-118">Then in the applications list, select the application.</span></span>

5. <span data-ttu-id="6c012-119">Sélectionnez la section **Certificats & secrets,** cliquez sur Nouvelle question secrète client, puis fournissez une description et spécifiez la durée de validité.</span><span class="sxs-lookup"><span data-stu-id="6c012-119">Select **Certificates & Secrets** section, Click on New Client Secret, then provide a description and specify the validity duration.</span></span>

6. <span data-ttu-id="6c012-120">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6c012-120">Click **Save**.</span></span> <span data-ttu-id="6c012-121">La valeur de clé s’affiche.</span><span class="sxs-lookup"><span data-stu-id="6c012-121">The key value is displayed.</span></span>

7. <span data-ttu-id="6c012-122">Copiez la valeur et enregistrez-la dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="6c012-122">Copy the value and save it in a safe place.</span></span>


## <a name="error-when-getting-a-refresh-access-token"></a><span data-ttu-id="6c012-123">Erreur lors de l’obtention d’un jeton d’accès actualisé</span><span class="sxs-lookup"><span data-stu-id="6c012-123">Error when getting a refresh access token</span></span>
<span data-ttu-id="6c012-124">Si vous rencontrez une erreur lors de la tentative d’obtenir un jeton d’actualisation lors de l’utilisation de l’API d’intelligence des menaces ou des outils SIEM, vous devez ajouter une URL de réponse pour l’application pertinente dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6c012-124">If you encounter an error when trying to get a refresh token when using the threat intelligence API or SIEM tools, you'll need to add reply URL for relevant application in Azure Active Directory.</span></span>

1. <span data-ttu-id="6c012-125">Connectez-vous au [portail de gestion Azure.](https://ms.portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="6c012-125">Login to the [Azure management portal](https://ms.portal.azure.com).</span></span>

2. <span data-ttu-id="6c012-126">Sélectionner **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="6c012-126">Select **Azure Active Directory**.</span></span>

3. <span data-ttu-id="6c012-127">Sélectionnez votre client.</span><span class="sxs-lookup"><span data-stu-id="6c012-127">Select your tenant.</span></span>

4. <span data-ttu-id="6c012-128">Cliquez **sur Inscriptions d’applications.**</span><span class="sxs-lookup"><span data-stu-id="6c012-128">Click **App Registrations**.</span></span> <span data-ttu-id="6c012-129">Ensuite, dans la liste des applications, sélectionnez l’application.</span><span class="sxs-lookup"><span data-stu-id="6c012-129">Then in the applications list, select the application.</span></span>

5. <span data-ttu-id="6c012-130">Ajoutez l’URL suivante :</span><span class="sxs-lookup"><span data-stu-id="6c012-130">Add the following URL:</span></span>
   - <span data-ttu-id="6c012-131">Pour l’Union européenne : `https://winatpmanagement-eu.securitycenter.windows.com/UserAuthenticationCallback`</span><span class="sxs-lookup"><span data-stu-id="6c012-131">For the European Union: `https://winatpmanagement-eu.securitycenter.windows.com/UserAuthenticationCallback`</span></span>
   - <span data-ttu-id="6c012-132">Pour le Royaume-Uni : `https://winatpmanagement-uk.securitycenter.windows.com/UserAuthenticationCallback`</span><span class="sxs-lookup"><span data-stu-id="6c012-132">For the United Kingdom: `https://winatpmanagement-uk.securitycenter.windows.com/UserAuthenticationCallback`</span></span>
   - <span data-ttu-id="6c012-133">Pour les États-Unis  `https://winatpmanagement-us.securitycenter.windows.com/UserAuthenticationCallback` : .</span><span class="sxs-lookup"><span data-stu-id="6c012-133">For the United States:  `https://winatpmanagement-us.securitycenter.windows.com/UserAuthenticationCallback`.</span></span>
 
6. <span data-ttu-id="6c012-134">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6c012-134">Click **Save**.</span></span>

## <a name="error-while-enabling-the-siem-connector-application"></a><span data-ttu-id="6c012-135">Erreur lors de l’activation de l’application de connecteur SIEM</span><span class="sxs-lookup"><span data-stu-id="6c012-135">Error while enabling the SIEM connector application</span></span>
<span data-ttu-id="6c012-136">Si vous rencontrez une erreur lors de la tentative d’activer l’application de connecteur SIEM, vérifiez les paramètres du bloqueur de fenêtres d’accès rapide de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="6c012-136">If you encounter an error when trying to enable the SIEM connector application, check the pop-up blocker settings of your browser.</span></span> <span data-ttu-id="6c012-137">Il peut bloquer l’ouverture de la nouvelle fenêtre lorsque vous activez la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6c012-137">It might be blocking the new window being opened when you enable the capability.</span></span>




><span data-ttu-id="6c012-138">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6c012-138">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="6c012-139">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6c012-139">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-troubleshootsiem-belowfoldlink) 

## <a name="related-topics"></a><span data-ttu-id="6c012-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c012-140">Related topics</span></span>
- [<span data-ttu-id="6c012-141">Activer l’intégration SIEM dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6c012-141">Enable SIEM integration in Microsoft Defender for Endpoint</span></span>](enable-siem-integration.md)
- [<span data-ttu-id="6c012-142">Configurer ArcSight pour tirer Microsoft Defender pour les détections de points de terminaison</span><span class="sxs-lookup"><span data-stu-id="6c012-142">Configure ArcSight to pull Microsoft Defender for Endpoint detections</span></span>](configure-arcsight.md)
- [<span data-ttu-id="6c012-143">Tirer les détections vers vos outils SIEM</span><span class="sxs-lookup"><span data-stu-id="6c012-143">Pull detections to your SIEM tools</span></span>](configure-siem.md)
- [<span data-ttu-id="6c012-144">Champs Microsoft Defender pour la détection des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="6c012-144">Microsoft Defender for Endpoint Detection fields</span></span>](api-portal-mapping.md)
- [<span data-ttu-id="6c012-145">Détecter Microsoft Defender pour les points de terminaison à l’aide de l’API REST</span><span class="sxs-lookup"><span data-stu-id="6c012-145">Pull Microsoft Defender for Endpoint detections using REST API</span></span>](pull-alerts-using-rest-api.md)
