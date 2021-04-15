---
title: Spécifier le niveau de protection cloud pour l'Antivirus Microsoft Defender
description: Définissez votre niveau de protection cloud pour l'Antivirus Microsoft Defender.
keywords: Antivirus Microsoft Defender, logiciel anti-programme malveillant, sécurité, defender, cloud, aggressiveness, niveau de protection
search.product: eADQiWindows 10XVcnh
ms.pagetype: security
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: normal
author: denisebmsft
ms.author: deniseb
ms.date: 10/26/2020
ms.reviewer: ''
manager: dansimp
ms.custom: nextgen
ms.technology: mde
ms.openlocfilehash: a0c73c8dd341c4940e3eddd4ede75240e57502d6
ms.sourcegitcommit: 7a339c9f7039825d131b39481ddf54c57b021b11
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51764120"
---
# <a name="specify-the-cloud-delivered-protection-level"></a><span data-ttu-id="dbccc-104">Spécifier le niveau de protection remis par le cloud</span><span class="sxs-lookup"><span data-stu-id="dbccc-104">Specify the cloud-delivered protection level</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="dbccc-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="dbccc-105">**Applies to:**</span></span>

- [<span data-ttu-id="dbccc-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="dbccc-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="dbccc-107">Vous pouvez spécifier votre niveau de protection cloud offerte par l'Antivirus Microsoft Defender à l'aide de Microsoft Endpoint Manager (recommandé) ou d'une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="dbccc-107">You can specify your level of cloud-delivered protection offered by Microsoft Defender Antivirus by using Microsoft Endpoint Manager (recommended) or Group Policy.</span></span>

> [!TIP]
> <span data-ttu-id="dbccc-108">La protection cloud n'est pas simplement une protection pour les fichiers stockés dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="dbccc-108">Cloud protection is not simply protection for files that are stored in the cloud.</span></span> <span data-ttu-id="dbccc-109">Le service cloud de l'Antivirus Microsoft Defender est un mécanisme permettant de fournir une protection mise à jour à votre réseau et à vos appareils (également appelés points de terminaison).</span><span class="sxs-lookup"><span data-stu-id="dbccc-109">The Microsoft Defender Antivirus cloud service is a mechanism for delivering updated protection to your network and devices (also called endpoints).</span></span> <span data-ttu-id="dbccc-110">La protection cloud avec l'Antivirus Microsoft Defender utilise des ressources distribuées et l'apprentissage automatique pour fournir une protection à vos points de terminaison à un taux beaucoup plus rapide que les mises à jour d'informations de sécurité traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="dbccc-110">Cloud protection with Microsoft Defender Antivirus uses distributed resources and machine learning to deliver protection to your endpoints at a rate that is far faster than traditional security intelligence updates.</span></span> <span data-ttu-id="dbccc-111">Microsoft Intune et Microsoft Endpoint Manager font désormais partie de [Microsoft Endpoint Manager.](/mem/endpoint-manager-overview)</span><span class="sxs-lookup"><span data-stu-id="dbccc-111">Microsoft Intune and Microsoft Endpoint Manager are now part of [Microsoft Endpoint Manager](/mem/endpoint-manager-overview).</span></span> 


## <a name="use-microsoft-endpoint-manager-to-specify-the-level-of-cloud-delivered-protection"></a><span data-ttu-id="dbccc-112">Utiliser Microsoft Endpoint Manager pour spécifier le niveau de protection cloud</span><span class="sxs-lookup"><span data-stu-id="dbccc-112">Use Microsoft Endpoint Manager to specify the level of cloud-delivered protection</span></span>

1. <span data-ttu-id="dbccc-113">Go to the Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="dbccc-113">Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and sign in.</span></span>

2. <span data-ttu-id="dbccc-114">Choisissez **l'Antivirus de sécurité des points de**  >  **terminaison.**</span><span class="sxs-lookup"><span data-stu-id="dbccc-114">Choose **Endpoint security** > **Antivirus**.</span></span>

3. <span data-ttu-id="dbccc-115">Sélectionnez un profil antivirus.</span><span class="sxs-lookup"><span data-stu-id="dbccc-115">Select an antivirus profile.</span></span> <span data-ttu-id="dbccc-116">(Si vous n'en avez pas encore, ou si vous souhaitez créer un profil, voir Configurer les paramètres de [restriction d'appareil dans Microsoft Intune](/intune/device-restrictions-configure).</span><span class="sxs-lookup"><span data-stu-id="dbccc-116">(If you don't have one yet, or if you want to create a new profile, see [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure).</span></span>

4. <span data-ttu-id="dbccc-117">Sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="dbccc-117">Select **Properties**.</span></span> <span data-ttu-id="dbccc-118">Ensuite, en de côté **des paramètres de configuration,** choisissez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="dbccc-118">Then, next to **Configuration settings**, choose **Edit**.</span></span>

5. <span data-ttu-id="dbccc-119">Développez **La protection** cloud, puis dans la liste des niveaux de **protection** cloud, sélectionnez l'une des listes suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbccc-119">Expand **Cloud protection**, and then in the **Cloud-delivered protection level** list, select one of the following:</span></span>

    1. <span data-ttu-id="dbccc-120">**Élevé**: applique un niveau de détection élevé.</span><span class="sxs-lookup"><span data-stu-id="dbccc-120">**High**: Applies a strong level of detection.</span></span>
    2. <span data-ttu-id="dbccc-121">**Plus élevé**: utilise le **niveau élevé** et applique des mesures de protection supplémentaires (peut avoir un impact sur les performances du client).</span><span class="sxs-lookup"><span data-stu-id="dbccc-121">**High plus**: Uses the **High** level and applies additional protection measures (may impact client performance).</span></span>
    3. <span data-ttu-id="dbccc-122">**Tolérance zéro :** bloque tous les exécutables inconnus.</span><span class="sxs-lookup"><span data-stu-id="dbccc-122">**Zero tolerance**: Blocks all unknown executables.</span></span>

6. <span data-ttu-id="dbccc-123">Choose **Review + save,** and then choose **Save**.</span><span class="sxs-lookup"><span data-stu-id="dbccc-123">Choose **Review + save**, and then choose **Save**.</span></span> 

> [!TIP]
> <span data-ttu-id="dbccc-124">Vous avez besoin d'aide ?</span><span class="sxs-lookup"><span data-stu-id="dbccc-124">Need some help?</span></span> <span data-ttu-id="dbccc-125">Consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbccc-125">See the following resources:</span></span>
> - [<span data-ttu-id="dbccc-126">Configurer Endpoint Protection</span><span class="sxs-lookup"><span data-stu-id="dbccc-126">Configure Endpoint Protection</span></span>](/mem/configmgr/protect/deploy-use/endpoint-protection-configure)
> - [<span data-ttu-id="dbccc-127">Ajouter des paramètres de protection des points de terminaison dans Intune</span><span class="sxs-lookup"><span data-stu-id="dbccc-127">Add endpoint protection settings in Intune</span></span>](/mem/intune/protect/endpoint-protection-configure)
  

## <a name="use-group-policy-to-specify-the-level-of-cloud-delivered-protection"></a><span data-ttu-id="dbccc-128">Utiliser une stratégie de groupe pour spécifier le niveau de protection cloud</span><span class="sxs-lookup"><span data-stu-id="dbccc-128">Use Group Policy to specify the level of cloud-delivered protection</span></span>

1.  <span data-ttu-id="dbccc-129">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console de gestion des stratégies de groupe.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="dbccc-129">On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)).</span></span>

2. <span data-ttu-id="dbccc-130">Cliquez avec le bouton droit sur l'objet de stratégie de groupe que vous souhaitez configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="dbccc-130">Right-click the Group Policy Object you want to configure, and then click **Edit**.</span></span>

3.  <span data-ttu-id="dbccc-131">Dans **l'Éditeur de gestion des stratégies de** groupe, allez **aux**  >  **modèles d'administration de configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="dbccc-131">In the **Group Policy Management Editor** go to **Computer Configuration** > **Administrative templates**.</span></span>

4.  <span data-ttu-id="dbccc-132">Développez l'arborescence **composants Windows**  >  **De l'Antivirus Microsoft Defender**  >  **MpEngine**.</span><span class="sxs-lookup"><span data-stu-id="dbccc-132">Expand the tree to **Windows Components** > **Microsoft Defender Antivirus** > **MpEngine**.</span></span>

5.  <span data-ttu-id="dbccc-133">Double-cliquez sur le paramètre Sélectionner le **niveau de protection cloud** et définissez-le sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="dbccc-133">Double-click the **Select cloud protection level** setting and set it to **Enabled**.</span></span> <span data-ttu-id="dbccc-134">Sélectionnez le niveau de protection :</span><span class="sxs-lookup"><span data-stu-id="dbccc-134">Select the level of protection:</span></span>
    - <span data-ttu-id="dbccc-135">**Le niveau de blocage par défaut** offre une détection forte sans augmenter le risque de détection de fichiers légitimes.</span><span class="sxs-lookup"><span data-stu-id="dbccc-135">**Default blocking level** provides strong detection without increasing the risk of detecting legitimate files.</span></span>
    - <span data-ttu-id="dbccc-136">**Un niveau de blocage modéré** fournit un niveau modéré uniquement pour les détections à niveau de confiance élevé</span><span class="sxs-lookup"><span data-stu-id="dbccc-136">**Moderate blocking level** provides moderate only for high confidence detections</span></span>
    - <span data-ttu-id="dbccc-137">**Un niveau de blocage élevé** applique un niveau élevé de détection tout en optimisant les performances du client (mais peut également vous donner plus de chances de faux positifs).</span><span class="sxs-lookup"><span data-stu-id="dbccc-137">**High blocking level** applies a strong level of detection while optimizing client performance (but can also give you a greater chance of false positives).</span></span>
    - <span data-ttu-id="dbccc-138">**Un niveau élevé + de blocage applique** des mesures de protection supplémentaires (peut avoir un impact sur les performances du client et augmenter votre risque de faux positifs).</span><span class="sxs-lookup"><span data-stu-id="dbccc-138">**High + blocking level** applies additional protection measures (might impact client performance and increase your chance of false positives).</span></span>
    - <span data-ttu-id="dbccc-139">**Le niveau de blocage de tolérance zéro** bloque tous les exécutables inconnus.</span><span class="sxs-lookup"><span data-stu-id="dbccc-139">**Zero tolerance blocking level** blocks all unknown executables.</span></span>
    
    > [!WARNING]
    > <span data-ttu-id="dbccc-140">Bien qu'il soit peu probable, la définition de ce commutateur sur **Élevé** ou Élevé **+** peut entraîner la détection de certains fichiers légitimes (bien que vous aurez la possibilité de débloquer ou de disputer cette détection).</span><span class="sxs-lookup"><span data-stu-id="dbccc-140">While unlikely, setting this switch to **High** or **High +** may cause some legitimate files to be detected (although you will have the option to unblock or dispute that detection).</span></span>

6. <span data-ttu-id="dbccc-141">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbccc-141">Click **OK**.</span></span>

7. <span data-ttu-id="dbccc-142">Déployez votre objet de stratégie de groupe mis à jour.</span><span class="sxs-lookup"><span data-stu-id="dbccc-142">Deploy your updated Group Policy Object.</span></span> <span data-ttu-id="dbccc-143">Voir [La Console de gestion des stratégies de groupe](/windows/win32/srvnodes/group-policy)</span><span class="sxs-lookup"><span data-stu-id="dbccc-143">See [Group Policy Management Console](/windows/win32/srvnodes/group-policy)</span></span>

> [!TIP]
> <span data-ttu-id="dbccc-144">Utilisez-vous des objets de stratégie de groupe en local ?</span><span class="sxs-lookup"><span data-stu-id="dbccc-144">Are you using Group Policy Objects on premises?</span></span> <span data-ttu-id="dbccc-145">Découvrez comment ils traduisent dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="dbccc-145">See how they translate in the cloud.</span></span> <span data-ttu-id="dbccc-146">[Analysez vos objets de stratégie](/mem/intune/configuration/group-policy-analytics)de groupe sur site à l'aide de l'analyse de la stratégie de groupe dans Microsoft Endpoint Manager - Aperçu .</span><span class="sxs-lookup"><span data-stu-id="dbccc-146">[Analyze your on-premises group policy objects using Group Policy analytics in Microsoft Endpoint Manager - Preview](/mem/intune/configuration/group-policy-analytics).</span></span> 
  
## <a name="related-articles"></a><span data-ttu-id="dbccc-147">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="dbccc-147">Related articles</span></span>

- [<span data-ttu-id="dbccc-148">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="dbccc-148">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="dbccc-149">Activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="dbccc-149">Enable cloud-delivered protection</span></span>](enable-cloud-protection-microsoft-defender-antivirus.md)
- [<span data-ttu-id="dbccc-150">Comment créer et déployer des stratégies de logiciel anti-programme malveillant : service de protection cloud</span><span class="sxs-lookup"><span data-stu-id="dbccc-150">How to create and deploy antimalware policies: Cloud-protection service</span></span>](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service)