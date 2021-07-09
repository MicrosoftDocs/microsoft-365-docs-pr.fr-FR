---
title: Intégrer des appareils non Windows au service Microsoft Defender for Endpoint
description: Configurez les appareils non Windows afin qu’ils peuvent envoyer des données de capteur au service Microsoft Defender for Endpoint.
keywords: intégrer des appareils non Windows, macos, linux, gestion des appareils, configurer Microsoft Defender pour les appareils Endpoint
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
ms.openlocfilehash: 777f5f63c4739f277ec24f826bc8a61a226fb65f
ms.sourcegitcommit: 0d1b065c94125b495e9886200f7918de3bda40b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2021
ms.locfileid: "53339669"
---
# <a name="onboard-non-windows-devices"></a><span data-ttu-id="38dd9-104">Intégrer des appareils non Windows</span><span class="sxs-lookup"><span data-stu-id="38dd9-104">Onboard non-Windows devices</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="38dd9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="38dd9-105">**Applies to:**</span></span>
- [<span data-ttu-id="38dd9-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="38dd9-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="38dd9-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="38dd9-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="38dd9-108">**Plateformes**</span><span class="sxs-lookup"><span data-stu-id="38dd9-108">**Platforms**</span></span>
- <span data-ttu-id="38dd9-109">macOS</span><span class="sxs-lookup"><span data-stu-id="38dd9-109">macOS</span></span>
- <span data-ttu-id="38dd9-110">Linux</span><span class="sxs-lookup"><span data-stu-id="38dd9-110">Linux</span></span>

><span data-ttu-id="38dd9-111">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="38dd9-111">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="38dd9-112">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="38dd9-112">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-nonwindows-abovefoldlink) 

<span data-ttu-id="38dd9-113">Defender pour le point de terminaison offre une expérience d’opérations de sécurité centralisée pour les Windows et les plateformes non Windows réseau.</span><span class="sxs-lookup"><span data-stu-id="38dd9-113">Defender for Endpoint provides a centralized security operations experience for Windows as well as non-Windows platforms.</span></span> <span data-ttu-id="38dd9-114">Vous pourrez voir les alertes de différents systèmes d’exploitation pris en charge dans Microsoft 365 Defender et mieux protéger le réseau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="38dd9-114">You'll be able to see alerts from various supported operating systems (OS) in Microsoft 365 Defender and better protect your organization's network.</span></span> 

<span data-ttu-id="38dd9-115">Vous devez connaître les versions exactes de Linux et macOS compatibles avec Defender for Endpoint pour que l’intégration fonctionne.</span><span class="sxs-lookup"><span data-stu-id="38dd9-115">You'll need to know the exact Linux distros and macOS versions that are compatible with Defender for Endpoint for the integration to work.</span></span> <span data-ttu-id="38dd9-116">Pour plus d'informations, voir :</span><span class="sxs-lookup"><span data-stu-id="38dd9-116">For more information, see:</span></span>
- [<span data-ttu-id="38dd9-117">Microsoft Defender pour point de terminaison sur la demande système Linux</span><span class="sxs-lookup"><span data-stu-id="38dd9-117">Microsoft Defender for Endpoint on Linux system requirements</span></span>](microsoft-defender-endpoint-linux.md#system-requirements)  
- <span data-ttu-id="38dd9-118">[Microsoft Defender pour point de terminaison sur macOS system requirements](microsoft-defender-endpoint-mac.md#system-requirements).</span><span class="sxs-lookup"><span data-stu-id="38dd9-118">[Microsoft Defender for Endpoint on macOS system requirements](microsoft-defender-endpoint-mac.md#system-requirements).</span></span>

## <a name="onboarding-non-windows-devices"></a><span data-ttu-id="38dd9-119">Intégration d’appareils non Windows intégrés</span><span class="sxs-lookup"><span data-stu-id="38dd9-119">Onboarding non-Windows devices</span></span>
<span data-ttu-id="38dd9-120">Pour intégrer des appareils non Windows, vous devez suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="38dd9-120">You'll need to take the following steps to onboard non-Windows devices:</span></span>
1. <span data-ttu-id="38dd9-121">Sélectionnez votre méthode d’intégration préférée :</span><span class="sxs-lookup"><span data-stu-id="38dd9-121">Select your preferred method of onboarding:</span></span>

   - <span data-ttu-id="38dd9-122">Pour les appareils macOS, vous pouvez choisir d’intégrer via Microsoft Defender pour Endpoint ou via une solution tierce.</span><span class="sxs-lookup"><span data-stu-id="38dd9-122">For macOS devices, you can choose to onboard through Microsoft Defender for Endpoint or through a third-party solution.</span></span> <span data-ttu-id="38dd9-123">Pour plus d’informations, [voir Microsoft Defender pour Endpoint sur Mac.](/microsoft-365/security/defender-endpoint/microsoft-defender-endpoint-mac)</span><span class="sxs-lookup"><span data-stu-id="38dd9-123">For more information, see [Microsoft Defender for Endpoint on Mac](/microsoft-365/security/defender-endpoint/microsoft-defender-endpoint-mac).</span></span>

   - <span data-ttu-id="38dd9-124">Pour les autres appareils non Windows choisissez Intégrer des appareils non Windows par le biais **d’une intégration tierce.**</span><span class="sxs-lookup"><span data-stu-id="38dd9-124">For other non-Windows devices choose **Onboard non-Windows devices through third-party integration**.</span></span>   
    1. <span data-ttu-id="38dd9-125">Dans le volet de navigation, sélectionnez **Partenaires d’interopérabilité.**  >  </span><span class="sxs-lookup"><span data-stu-id="38dd9-125">In the navigation pane, select **Interoperability** > **Partners**.</span></span> <span data-ttu-id="38dd9-126">Assurez-vous que la solution tierce est répertoriée.</span><span class="sxs-lookup"><span data-stu-id="38dd9-126">Make sure the third-party solution is listed.</span></span>
    2. <span data-ttu-id="38dd9-127">Dans **l’onglet Applications** partenaires, sélectionnez le partenaire qui prend en charge vos appareils Windows non connectés.</span><span class="sxs-lookup"><span data-stu-id="38dd9-127">In the **Partner Applications** tab, select the partner that supports your non-Windows devices.</span></span>
    3. <span data-ttu-id="38dd9-128">Sélectionnez **Ouvrir la page du partenaire** pour ouvrir la page du partenaire.</span><span class="sxs-lookup"><span data-stu-id="38dd9-128">Select **Open partner page** to open the partner's page.</span></span> <span data-ttu-id="38dd9-129">Suivez les instructions fournies sur la page.</span><span class="sxs-lookup"><span data-stu-id="38dd9-129">Follow the instructions provided on the page.</span></span>
    4. <span data-ttu-id="38dd9-130">Après avoir créé un compte ou vous être abonné à la solution partenaire, vous devez passer à une étape où un administrateur global client de votre organisation est invité à accepter une demande d’autorisation de l’application partenaire.</span><span class="sxs-lookup"><span data-stu-id="38dd9-130">After creating an account or subscribing to the partner solution, you should get to a stage where a tenant Global Admin in your organization is asked to accept a permission request from the partner application.</span></span> <span data-ttu-id="38dd9-131">Lisez attentivement la demande d’autorisation pour vous assurer qu’elle est alignée sur le service dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="38dd9-131">Read the permission request carefully to make sure that it is aligned with the service that you require.</span></span> 

        
2. <span data-ttu-id="38dd9-132">Exécutez un test de détection en suivant les instructions de la solution tierce.</span><span class="sxs-lookup"><span data-stu-id="38dd9-132">Run a detection test by following the instructions of the third-party solution.</span></span>

## <a name="offboard-non-windows-devices"></a><span data-ttu-id="38dd9-133">Appareils non-Windows par carte</span><span class="sxs-lookup"><span data-stu-id="38dd9-133">Offboard non-Windows devices</span></span>

1. <span data-ttu-id="38dd9-134">Suivez la documentation du tiers pour déconnecter la solution tierce de Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="38dd9-134">Follow the third-party's documentation to disconnect the third-party solution from Microsoft Defender for Endpoint.</span></span>

2. <span data-ttu-id="38dd9-135">Supprimez les autorisations pour la solution tierce dans votre client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="38dd9-135">Remove permissions for the third-party solution in your Azure AD tenant.</span></span>
   1. <span data-ttu-id="38dd9-136">Connectez-vous au [Portail Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="38dd9-136">Sign in to the [Azure portal](https://portal.azure.com).</span></span>
   2. <span data-ttu-id="38dd9-137">Sélectionnez **Azure Active Directory > Enterprise applications.**</span><span class="sxs-lookup"><span data-stu-id="38dd9-137">Select **Azure Active Directory > Enterprise Applications**.</span></span>
   3. <span data-ttu-id="38dd9-138">Sélectionnez l’application que vous souhaitez horsboard.</span><span class="sxs-lookup"><span data-stu-id="38dd9-138">Select the application you'd like to offboard.</span></span>
   4. <span data-ttu-id="38dd9-139">Sélectionnez **le bouton** Supprimer.</span><span class="sxs-lookup"><span data-stu-id="38dd9-139">Select the **Delete** button.</span></span>


## <a name="related-topics"></a><span data-ttu-id="38dd9-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38dd9-140">Related topics</span></span>
- [<span data-ttu-id="38dd9-141">Intégrer des appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="38dd9-141">Onboard Windows 10 devices</span></span>](configure-endpoints.md)
- [<span data-ttu-id="38dd9-142">Serveurs intégrés</span><span class="sxs-lookup"><span data-stu-id="38dd9-142">Onboard servers</span></span>](configure-server-endpoints.md)
- [<span data-ttu-id="38dd9-143">Configurer les paramètres de proxy et de connectivité Internet</span><span class="sxs-lookup"><span data-stu-id="38dd9-143">Configure proxy and Internet connectivity settings</span></span>](configure-proxy-internet.md)
- [<span data-ttu-id="38dd9-144">Résolution des problèmes d’intégration de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="38dd9-144">Troubleshooting Microsoft Defender for Endpoint onboarding issues</span></span>](troubleshoot-onboarding.md)
