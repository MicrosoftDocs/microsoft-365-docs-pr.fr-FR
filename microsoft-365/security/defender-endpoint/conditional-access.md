---
title: Activer l’accès conditionnel pour mieux protéger les utilisateurs, les appareils et les données
description: Activez l’accès conditionnel pour empêcher l’exécution des applications si un appareil est considéré comme à risque et si une application est considérée comme non conforme.
keywords: accès conditionnel, bloquer les applications, niveau de sécurité, intune,
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
ms.openlocfilehash: 21d17ee789a4757df10e99514f23cfc26b186405
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166196"
---
# <a name="enable-conditional-access-to-better-protect-users-devices-and-data"></a><span data-ttu-id="33aae-104">Activer l’accès conditionnel pour mieux protéger les utilisateurs, les appareils et les données</span><span class="sxs-lookup"><span data-stu-id="33aae-104">Enable Conditional Access to better protect users, devices, and data</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="33aae-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="33aae-105">**Applies to:**</span></span>
- [<span data-ttu-id="33aae-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="33aae-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="33aae-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="33aae-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="33aae-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="33aae-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="33aae-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="33aae-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-conditionalaccess-abovefoldlink)

<span data-ttu-id="33aae-110">L’accès conditionnel est une fonctionnalité qui vous permet de mieux protéger vos utilisateurs et les informations d’entreprise en vous assurez que seuls les appareils sécurisés ont accès aux applications.</span><span class="sxs-lookup"><span data-stu-id="33aae-110">Conditional Access is a capability that helps you better protect your users and enterprise information by making sure that only secure devices have access to applications.</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4byD1]

<span data-ttu-id="33aae-111">Avec l’accès conditionnel, vous pouvez contrôler l’accès aux informations d’entreprise en fonction du niveau de risque d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="33aae-111">With Conditional Access, you can control access to enterprise information based on the risk level of a device.</span></span> <span data-ttu-id="33aae-112">Cela permet de conserver les utilisateurs de confiance sur des appareils de confiance à l’aide d’applications fiables.</span><span class="sxs-lookup"><span data-stu-id="33aae-112">This helps keep trusted users on trusted devices using trusted applications.</span></span>

<span data-ttu-id="33aae-113">Vous pouvez définir des conditions de sécurité dans lesquelles les appareils et les applications peuvent s’exécuter et accéder aux informations à partir de votre réseau en appliquant des stratégies pour empêcher l’exécution des applications jusqu’à ce qu’un appareil retrouve un état conforme.</span><span class="sxs-lookup"><span data-stu-id="33aae-113">You can define security conditions under which devices and applications can run and access information from your network by enforcing policies to stop applications from running until a device returns to a compliant state.</span></span> 

<span data-ttu-id="33aae-114">L’implémentation de l’accès conditionnel dans Defender pour point de terminaison est basée sur les stratégies de conformité des appareils Microsoft Intune (Intune) et les stratégies d’accès conditionnel Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="33aae-114">The implementation of Conditional Access in Defender for Endpoint is based on Microsoft Intune (Intune) device compliance policies and Azure Active Directory (Azure AD) conditional access policies.</span></span> 

<span data-ttu-id="33aae-115">La stratégie de conformité est utilisée avec l’accès conditionnel pour autoriser uniquement les appareils qui respectent une ou plusieurs règles de stratégie de conformité des appareils à accéder aux applications.</span><span class="sxs-lookup"><span data-stu-id="33aae-115">The compliance policy is used with Conditional Access to allow only devices that fulfill one or more device compliance policy rules to access applications.</span></span> 

## <a name="understand-the-conditional-access-flow"></a><span data-ttu-id="33aae-116">Comprendre le flux d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="33aae-116">Understand the Conditional Access flow</span></span>
<span data-ttu-id="33aae-117">L’accès conditionnel est mis en place de sorte que lorsqu’une menace est vue sur un appareil, l’accès au contenu sensible est bloqué jusqu’à ce que la menace soit corrigé.</span><span class="sxs-lookup"><span data-stu-id="33aae-117">Conditional Access is put in place so that when a threat is seen on a device, access to sensitive content is blocked until the threat is remediated.</span></span> 

<span data-ttu-id="33aae-118">Le flux commence par le fait que les appareils sont considérés comme ayant un risque faible, moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="33aae-118">The flow begins with devices being seen to have a low, medium, or high risk.</span></span> <span data-ttu-id="33aae-119">Ces déterminations des risques sont ensuite envoyées à Intune.</span><span class="sxs-lookup"><span data-stu-id="33aae-119">These risk determinations are then sent to Intune.</span></span> 

<span data-ttu-id="33aae-120">En fonction de la configuration des stratégies dans Intune, l’accès conditionnel peut être configuré de sorte que lorsque certaines conditions sont remplies, la stratégie soit appliquée.</span><span class="sxs-lookup"><span data-stu-id="33aae-120">Depending on how you configure policies in Intune, Conditional Access can be set up so that when certain conditions are met, the policy is applied.</span></span>

<span data-ttu-id="33aae-121">Par exemple, vous pouvez configurer Intune pour appliquer l’accès conditionnel sur les appareils à risque élevé.</span><span class="sxs-lookup"><span data-stu-id="33aae-121">For example, you can configure Intune to apply Conditional Access on devices that have a high risk.</span></span>

<span data-ttu-id="33aae-122">Dans Intune, une stratégie de conformité des appareils est utilisée conjointement avec l’accès conditionnel Azure AD pour bloquer l’accès aux applications.</span><span class="sxs-lookup"><span data-stu-id="33aae-122">In Intune, a device compliance policy is used in conjunction with Azure AD Conditional Access to block access to applications.</span></span> <span data-ttu-id="33aae-123">En parallèle, un processus automatisé d’examen et de correction est lancé.</span><span class="sxs-lookup"><span data-stu-id="33aae-123">In parallel, an automated investigation and remediation process is launched.</span></span>

 <span data-ttu-id="33aae-124">Un utilisateur peut toujours utiliser l’appareil pendant l’examen et la correction automatisés, mais l’accès aux données d’entreprise est bloqué jusqu’à ce que la menace soit entièrement corrigé.</span><span class="sxs-lookup"><span data-stu-id="33aae-124">A user can still use the device while the automated investigation and remediation is taking place, but access to enterprise data is blocked until the threat is fully remediated.</span></span> 

<span data-ttu-id="33aae-125">Pour résoudre le risque trouvé sur un appareil, vous devez le remettre à l’état conforme.</span><span class="sxs-lookup"><span data-stu-id="33aae-125">To resolve the risk found on a device, you'll need to return the device to a compliant state.</span></span> <span data-ttu-id="33aae-126">Un appareil revient à un état conforme lorsqu’il n’y a aucun risque.</span><span class="sxs-lookup"><span data-stu-id="33aae-126">A device returns to a compliant state when there is no risk seen on it.</span></span> 

<span data-ttu-id="33aae-127">Il existe trois façons de résoudre un risque :</span><span class="sxs-lookup"><span data-stu-id="33aae-127">There are three ways to address a risk:</span></span>
1. <span data-ttu-id="33aae-128">Utilisez la correction manuelle ou automatisée.</span><span class="sxs-lookup"><span data-stu-id="33aae-128">Use Manual or automated remediation.</span></span>
2. <span data-ttu-id="33aae-129">Résoudre les alertes actives sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="33aae-129">Resolve active alerts on the device.</span></span> <span data-ttu-id="33aae-130">Cela permet de supprimer le risque de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="33aae-130">This will remove the risk from the device.</span></span>
3. <span data-ttu-id="33aae-131">Vous pouvez supprimer l’appareil des stratégies actives et, par conséquent, l’accès conditionnel ne sera pas appliqué à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="33aae-131">You can remove the device from the active policies and consequently, Conditional Access will not be applied on the device.</span></span> 

<span data-ttu-id="33aae-132">La correction manuelle nécessite qu’un administrateur secops examine une alerte et adresse le risque visible sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="33aae-132">Manual remediation requires a secops admin to investigate an alert and address the risk seen on the device.</span></span> <span data-ttu-id="33aae-133">La correction automatisée est configurée par le biais des paramètres de configuration fournis dans la section suivante, [Configurer l’accès conditionnel](configure-conditional-access.md).</span><span class="sxs-lookup"><span data-stu-id="33aae-133">The automated remediation is configured through configuration settings provided in the following section, [Configure Conditional Access](configure-conditional-access.md).</span></span>

<span data-ttu-id="33aae-134">Lorsque le risque est supprimé par le biais d’une correction manuelle ou automatisée, l’appareil revient à un état conforme et l’accès aux applications est accordé.</span><span class="sxs-lookup"><span data-stu-id="33aae-134">When the risk is removed either through manual or automated remediation, the device returns to a compliant state and access to applications is granted.</span></span>

<span data-ttu-id="33aae-135">L’exemple de séquence d’événements suivant explique l’accès conditionnel en action :</span><span class="sxs-lookup"><span data-stu-id="33aae-135">The following example sequence of events explains Conditional Access in action:</span></span>

1. <span data-ttu-id="33aae-136">Un utilisateur ouvre un fichier malveillant et Defender for Endpoint signale l’appareil comme étant à risque élevé.</span><span class="sxs-lookup"><span data-stu-id="33aae-136">A user opens a malicious file and Defender for Endpoint flags the device as high risk.</span></span>
2. <span data-ttu-id="33aae-137">L’évaluation à risque élevé est transmise à Intune.</span><span class="sxs-lookup"><span data-stu-id="33aae-137">The high risk assessment is passed along to Intune.</span></span> <span data-ttu-id="33aae-138">En parallèle, une enquête automatisée est lancée pour corriger la menace identifiée.</span><span class="sxs-lookup"><span data-stu-id="33aae-138">In parallel, an automated investigation is initiated to remediate the identified threat.</span></span> <span data-ttu-id="33aae-139">Une correction manuelle peut également être effectuée pour corriger la menace identifiée.</span><span class="sxs-lookup"><span data-stu-id="33aae-139">A manual remediation can also be done to remediate the identified threat.</span></span>
3. <span data-ttu-id="33aae-140">En fonction de la stratégie créée dans Intune, l’appareil est marqué comme non conforme.</span><span class="sxs-lookup"><span data-stu-id="33aae-140">Based on the policy created in Intune, the device is marked as not compliant.</span></span> <span data-ttu-id="33aae-141">L’évaluation est ensuite communiquée à Azure AD par la stratégie d’accès conditionnel Intune.</span><span class="sxs-lookup"><span data-stu-id="33aae-141">The assessment is then communicated to Azure AD by the Intune Conditional Access policy.</span></span> <span data-ttu-id="33aae-142">Dans Azure AD, la stratégie correspondante est appliquée pour bloquer l’accès aux applications.</span><span class="sxs-lookup"><span data-stu-id="33aae-142">In Azure AD, the corresponding policy is applied to block access to applications.</span></span>
4. <span data-ttu-id="33aae-143">L’examen et la correction manuels ou automatisés sont terminés et la menace est supprimée.</span><span class="sxs-lookup"><span data-stu-id="33aae-143">The manual or automated investigation and remediation is completed and the threat is removed.</span></span> <span data-ttu-id="33aae-144">Defender pour le point de terminaison constate qu’il n’y a aucun risque sur l’appareil et Intune évalue que l’appareil est dans un état conforme.</span><span class="sxs-lookup"><span data-stu-id="33aae-144">Defender for Endpoint sees that there is no risk on the device and Intune assesses the device to be in a compliant state.</span></span> <span data-ttu-id="33aae-145">Azure AD applique la stratégie qui autorise l’accès aux applications.</span><span class="sxs-lookup"><span data-stu-id="33aae-145">Azure AD applies the policy which allows access to applications.</span></span>
5. <span data-ttu-id="33aae-146">Les utilisateurs peuvent désormais accéder aux applications.</span><span class="sxs-lookup"><span data-stu-id="33aae-146">Users can now access applications.</span></span>

 
## <a name="related-topic"></a><span data-ttu-id="33aae-147">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="33aae-147">Related topic</span></span>
- [<span data-ttu-id="33aae-148">Configurer l’accès conditionnel dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="33aae-148">Configure Conditional Access in Microsoft Defender for Endpoint</span></span>](configure-conditional-access.md)
