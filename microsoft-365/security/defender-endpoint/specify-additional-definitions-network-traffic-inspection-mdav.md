---
title: Spécifier des ensembles de définitions supplémentaires pour l’inspection du trafic réseau Antivirus Microsoft Defender
description: Spécifiez des ensembles de définitions supplémentaires pour l’inspection du trafic Antivirus Microsoft Defender.
keywords: Antivirus Microsoft Defender, anti-programme malveillant, sécurité, defender, inspection du trafic réseau
search.product: eADQiWindows 10XVcnh
ms.pagetype: security
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.date: 05/07/2021
ms.reviewer: ''
manager: dansimp
ms.custom: nextgen
ms.technology: mde
ms.topic: article
ms.openlocfilehash: 82568df0a6ad2225fd31b4c0fa4a654710f1e98b
ms.sourcegitcommit: de5fce90de22ba588e75e1a1d2e87e03b9e25ec7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52300194"
---
# <a name="specify-additional-definition-sets-for-network-traffic-inspection"></a><span data-ttu-id="7eeb4-104">Spécifier des ensembles de définitions supplémentaires pour l’inspection du trafic réseau</span><span class="sxs-lookup"><span data-stu-id="7eeb4-104">Specify additional definition sets for network traffic inspection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="7eeb4-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7eeb4-105">**Applies to:**</span></span>

- [<span data-ttu-id="7eeb4-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7eeb4-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="7eeb4-107">Vous pouvez spécifier des ensembles de définitions supplémentaires pour l’inspection du trafic réseau à l’aide de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="7eeb4-107">You can specify additional definition sets for network traffic inspection using Group Policy.</span></span>

## <a name="use-group-policy-to-specify-additional-definition-sets-for-network-traffic-inspection"></a><span data-ttu-id="7eeb4-108">Utiliser une stratégie de groupe pour spécifier des ensembles de définitions supplémentaires pour l’inspection du trafic réseau</span><span class="sxs-lookup"><span data-stu-id="7eeb4-108">Use Group Policy to specify additional definition sets for network traffic inspection</span></span>

1. <span data-ttu-id="7eeb4-109">Sur votre point de terminaison de gestion des stratégies de groupe, ouvrez la [Console de gestion des stratégies de groupe.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="7eeb4-109">On your Group Policy management endpoint, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)).</span></span>

2. <span data-ttu-id="7eeb4-110">Go to **Windows Components**  >  **Antivirus Microsoft Defender**  >  **Network Inspection System**.</span><span class="sxs-lookup"><span data-stu-id="7eeb4-110">Go to **Windows Components** > **Microsoft Defender Antivirus** > **Network Inspection System**.</span></span> 

3. <span data-ttu-id="7eeb4-111">Sélectionnez **Spécifier des jeux de définitions supplémentaires pour l’inspection du trafic réseau.**</span><span class="sxs-lookup"><span data-stu-id="7eeb4-111">Select **Specify additional definition sets for network traffic inspection**.</span></span> <span data-ttu-id="7eeb4-112">Par défaut, cette stratégie est définie sur **Non configuré.**</span><span class="sxs-lookup"><span data-stu-id="7eeb4-112">By default, this policy is set to **Not configured**.</span></span> 

4. <span data-ttu-id="7eeb4-113">Pour modifier la stratégie, sélectionnez le lien **modifier le paramètre de stratégie.**</span><span class="sxs-lookup"><span data-stu-id="7eeb4-113">To edit the policy, select the **edit policy setting** link.</span></span>

5. <span data-ttu-id="7eeb4-114">Sélectionnez **Activé,** puis, dans la section **Options,** **sélectionnez Afficher...**.</span><span class="sxs-lookup"><span data-stu-id="7eeb4-114">Select **Enabled**, and then in the **Options** section, select **Show...**.</span></span>

6. <span data-ttu-id="7eeb4-115">Ajoutez des entrées à la liste, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="7eeb4-115">Add entries to the list, and then select **OK**.</span></span> 

   <span data-ttu-id="7eeb4-116">Chaque entrée doit être répertoriée en tant que paire nom-valeur, où le nom est une représentation sous la chaîne d’un GUID de jeu de définitions.</span><span class="sxs-lookup"><span data-stu-id="7eeb4-116">Each entry must be listed as a name-value pair, where the name is a string representation of a definition set GUID.</span></span> <span data-ttu-id="7eeb4-117">Par exemple, le GUID de définition défini pour activer l’intelligence de sécurité de test est défini comme : `{b54b6ac9-a737-498e-9120-6616ad3bf590}` .</span><span class="sxs-lookup"><span data-stu-id="7eeb4-117">As an example, the definition set GUID to enable test security intelligence is defined as: `{b54b6ac9-a737-498e-9120-6616ad3bf590}`.</span></span> <span data-ttu-id="7eeb4-118">La valeur n’est pas utilisée, donc nous vous recommandons de la définir sur `0` .</span><span class="sxs-lookup"><span data-stu-id="7eeb4-118">The value is not used, so we recommend setting it to `0`.</span></span> 

7. <span data-ttu-id="7eeb4-119">Sélectionnez **OK,** puis déployez votre objet de stratégie de groupe mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7eeb4-119">Select **OK**, and then deploy your updated Group Policy Object.</span></span> <span data-ttu-id="7eeb4-120">Voir [La Console de gestion des stratégies de groupe.](/windows/win32/srvnodes/group-policy)</span><span class="sxs-lookup"><span data-stu-id="7eeb4-120">See [Group Policy Management Console](/windows/win32/srvnodes/group-policy).</span></span>

> [!TIP]
> <span data-ttu-id="7eeb4-121">Utilisez-vous des objets de stratégie de groupe en local ?</span><span class="sxs-lookup"><span data-stu-id="7eeb4-121">Are you using Group Policy Objects on premises?</span></span> <span data-ttu-id="7eeb4-122">Découvrez comment ils traduisent dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="7eeb4-122">See how they translate in the cloud.</span></span> <span data-ttu-id="7eeb4-123">[Analysez vos objets de stratégie](/mem/intune/configuration/group-policy-analytics)de groupe en local à l’aide de l’analyse de stratégie de groupe dans Microsoft Endpoint Manager - Aperçu .</span><span class="sxs-lookup"><span data-stu-id="7eeb4-123">[Analyze your on-premises group policy objects using Group Policy analytics in Microsoft Endpoint Manager - Preview](/mem/intune/configuration/group-policy-analytics).</span></span> 
  
## <a name="related-articles"></a><span data-ttu-id="7eeb4-124">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="7eeb4-124">Related articles</span></span>

- [<span data-ttu-id="7eeb4-125">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="7eeb4-125">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
 
- [<span data-ttu-id="7eeb4-126">Protection fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="7eeb4-126">Enable cloud-delivered protection</span></span>](enable-cloud-protection-microsoft-defender-antivirus.md)

- [<span data-ttu-id="7eeb4-127">Comment créer et déployer des stratégies de logiciel anti-programme malveillant : service de protection cloud</span><span class="sxs-lookup"><span data-stu-id="7eeb4-127">How to create and deploy antimalware policies: Cloud-protection service</span></span>](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service)