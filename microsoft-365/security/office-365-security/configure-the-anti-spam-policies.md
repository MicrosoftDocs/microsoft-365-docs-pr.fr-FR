---
title: Configuration de stratégies de blocage du courrier indésirable
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 6/9/2015
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 31279431-828d-48bd-b979-20b6de15fa4a
ms.collection:
- M365-security-compliance
description: Le filtrage du courrier indésirable est automatiquement activé à l'échelle de l'entreprise selon les stratégies anti-spam par défaut (filtre de connexion, filtre du courrier indésirable et courrier indésirable sortant). En qualité d'administrateur, vous pouvez afficher et modifier, mais pas supprimer, les stratégies anti-spam par défaut pour les adapter parfaitement aux besoins de votre organisation. Pour une précision accrue, vous pouvez également créer des stratégies de filtrage de contenu personnalisées et les appliquer à des utilisateurs, à des groupes ou à des domaines spécifiés dans votre organisation. Par défaut, les stratégies personnalisées priment sur la stratégie par défaut. Vous pouvez cependant modifier la priorité de vos stratégies.
ms.openlocfilehash: 2ee5833bf476123a84411a7ad645b9f8c5d0b2b8
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41599581"
---
# <a name="configure-the-anti-spam-policies"></a><span data-ttu-id="0919d-106">Configuration de stratégies de blocage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="0919d-106">Configure the anti-spam policies</span></span>

<span data-ttu-id="0919d-p102">Le filtrage du courrier indésirable est automatiquement activé à l'échelle de l'entreprise selon les stratégies anti-spam par défaut (filtre de connexion, filtre du courrier indésirable et courrier indésirable sortant). En qualité d'administrateur, vous pouvez afficher et modifier, mais pas supprimer, les stratégies anti-spam par défaut pour les adapter parfaitement aux besoins de votre organisation. Pour une précision accrue, vous pouvez également créer des stratégies de filtrage de contenu personnalisées et les appliquer à des utilisateurs, à des groupes ou à des domaines spécifiés dans votre organisation. Par défaut, les stratégies personnalisées priment sur la stratégie par défaut. Vous pouvez cependant modifier la priorité de vos stratégies.</span><span class="sxs-lookup"><span data-stu-id="0919d-p102">Spam filtering is automatically enabled company-wide through the default anti-spam policies (connection filter, spam filter, and outbound spam). As an administrator, you can view and edit, but not delete, the default anti-spam policies so that they are tailored to best meet the needs of your organization. For greater granularity, you can also create custom policies and apply them to specified users, groups, or domains in your organization. By default, custom policies take precedence over the default policy, but you can change the priority of your policies.</span></span> 
  
<span data-ttu-id="0919d-111">Pour plus d'informations sur la configuration de vos stratégies anti-spam, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="0919d-111">For more about configuring your anti-spam policies, see the following topics:</span></span>
  
[<span data-ttu-id="0919d-112">Configuration de la stratégie de filtrage des connexions</span><span class="sxs-lookup"><span data-stu-id="0919d-112">Configure the connection filter policy</span></span>](configure-the-connection-filter-policy.md)
  
[<span data-ttu-id="0919d-113">Configuration de vos stratégies de filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="0919d-113">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
> [!IMPORTANT]
> <span data-ttu-id="0919d-114">Pour les clients autonomes EOP : par défaut, les filtres de contenu Exchange Online Protection envoient les messages indésirables détectés dans le dossier Courrier indésirable respectif de chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="0919d-114">For EOP standalone customers: By default, the EOP content filters send spam-detected messages to each recipients' Junk Email folder.</span></span> <span data-ttu-id="0919d-115">Toutefois, pour vous assurer que l’action **déplacer le message vers le dossier courrier indésirable** fonctionnera avec des boîtes aux lettres locales, vous devez configurer deux règles de flux de messagerie Exchange (également appelées règles de transport) sur vos serveurs locaux pour détecter les en-têtes de courrier indésirable ajoutés par EOP.</span><span class="sxs-lookup"><span data-stu-id="0919d-115">However, in order to ensure that the **Move message to Junk Email folder** action will work with on-premises mailboxes, you must configure two Exchange mail flow rules (also known as transport rules) on your on-premises servers to detect spam headers added by EOP.</span></span> <span data-ttu-id="0919d-116">Pour plus d'informations, voir [Vérification de l'acheminement du courrier indésirable vers le dossier Courrier indésirable de chaque utilisateur](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span><span class="sxs-lookup"><span data-stu-id="0919d-116">For details, see [Ensure that spam is routed to each user's Junk Email folder](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span></span> 
  
[<span data-ttu-id="0919d-117">Configurer la stratégie anti-courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="0919d-117">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  

