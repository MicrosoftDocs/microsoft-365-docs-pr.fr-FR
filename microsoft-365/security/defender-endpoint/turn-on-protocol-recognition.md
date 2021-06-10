---
title: Activer la reconnaissance de protocole pour Antivirus Microsoft Defender
description: Activer la reconnaissance de protocole pour Antivirus Microsoft Defender.
keywords: Antivirus Microsoft Defender, anti-programme malveillant, sécurité, defender, reconnaissance de protocole
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
ms.openlocfilehash: 890303a15618a0318db0421c9c80f270583e19bf
ms.sourcegitcommit: de5fce90de22ba588e75e1a1d2e87e03b9e25ec7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52296476"
---
# <a name="turn-on-protocol-recognition"></a><span data-ttu-id="ffd67-104">Activer la reconnaissance de protocole</span><span class="sxs-lookup"><span data-stu-id="ffd67-104">Turn on protocol recognition</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="ffd67-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ffd67-105">**Applies to:**</span></span>

- [<span data-ttu-id="ffd67-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ffd67-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="ffd67-107">Ce paramètre de stratégie vous permet de configurer la reconnaissance de protocole pour la protection du réseau contre les attaques de vulnérabilités connues.</span><span class="sxs-lookup"><span data-stu-id="ffd67-107">This policy setting allows you to configure protocol recognition for network protection against exploits of known vulnerabilities.</span></span> <span data-ttu-id="ffd67-108">Si vous activez ou ne configurez pas ce paramètre, la reconnaissance de protocole est activée.</span><span class="sxs-lookup"><span data-stu-id="ffd67-108">If you enable or do not configure this setting, protocol recognition will be enabled.</span></span> <span data-ttu-id="ffd67-109">Si vous désactivez ce paramètre, la reconnaissance de protocole sera désactivée.</span><span class="sxs-lookup"><span data-stu-id="ffd67-109">If you disable this setting, protocol recognition will be disabled.</span></span>

## <a name="use-group-policy-to-configure-protocol-recognition"></a><span data-ttu-id="ffd67-110">Utiliser une stratégie de groupe pour configurer la reconnaissance de protocole</span><span class="sxs-lookup"><span data-stu-id="ffd67-110">Use Group Policy to configure protocol recognition</span></span>

1. <span data-ttu-id="ffd67-111">Sur votre point de terminaison de gestion des stratégies de groupe, ouvrez la [Console de gestion des stratégies de groupe.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="ffd67-111">On your Group Policy management endpoint, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)).</span></span>

2. <span data-ttu-id="ffd67-112">Go to **Computer Configuration**  >  **Administrative Templates** Windows  >  **Components**  >  **Antivirus Microsoft Defender** Network  >  **Inspection System**.</span><span class="sxs-lookup"><span data-stu-id="ffd67-112">Go to **Computer Configuration** > **Administrative Templates** > **Windows Components** > **Microsoft Defender Antivirus** > **Network Inspection System**.</span></span> 

3. <span data-ttu-id="ffd67-113">Sélectionnez **la reconnaissance de protocole.**</span><span class="sxs-lookup"><span data-stu-id="ffd67-113">Select **protocol recognition**.</span></span> <span data-ttu-id="ffd67-114">Par défaut, cette stratégie est activée.</span><span class="sxs-lookup"><span data-stu-id="ffd67-114">By default, this policy is enabled.</span></span> <span data-ttu-id="ffd67-115">Si la configuration **n’est pas configurée,** le retrait de définition est activé.</span><span class="sxs-lookup"><span data-stu-id="ffd67-115">If set **Not configured**, definition retirement is enabled.</span></span> 

4. <span data-ttu-id="ffd67-116">Pour modifier la stratégie, sélectionnez le lien **modifier le paramètre de stratégie.**</span><span class="sxs-lookup"><span data-stu-id="ffd67-116">To edit the policy, select the **edit policy setting** link.</span></span>

5. <span data-ttu-id="ffd67-117">Sélectionnez **Activé,** puis **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffd67-117">Select **Enabled**, and then select **OK**.</span></span>

6. <span data-ttu-id="ffd67-118">Déployez votre objet de stratégie de groupe mis à jour.</span><span class="sxs-lookup"><span data-stu-id="ffd67-118">Deploy your updated Group Policy Object.</span></span> <span data-ttu-id="ffd67-119">Voir [La Console de gestion des stratégies de groupe.](/windows/win32/srvnodes/group-policy)</span><span class="sxs-lookup"><span data-stu-id="ffd67-119">See [Group Policy Management Console](/windows/win32/srvnodes/group-policy).</span></span>

> [!TIP]
> <span data-ttu-id="ffd67-120">Utilisez-vous des objets de stratégie de groupe en local ?</span><span class="sxs-lookup"><span data-stu-id="ffd67-120">Are you using Group Policy Objects on premises?</span></span> <span data-ttu-id="ffd67-121">Découvrez comment ils traduisent dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="ffd67-121">See how they translate in the cloud.</span></span> <span data-ttu-id="ffd67-122">[Analysez vos objets de stratégie](/mem/intune/configuration/group-policy-analytics)de groupe en local à l’aide de l’analyse de stratégie de groupe dans Microsoft Endpoint Manager - Aperçu .</span><span class="sxs-lookup"><span data-stu-id="ffd67-122">[Analyze your on-premises group policy objects using Group Policy analytics in Microsoft Endpoint Manager - Preview](/mem/intune/configuration/group-policy-analytics).</span></span> 
  
## <a name="related-articles"></a><span data-ttu-id="ffd67-123">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="ffd67-123">Related articles</span></span>

- [<span data-ttu-id="ffd67-124">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="ffd67-124">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
 
- [<span data-ttu-id="ffd67-125">Protection fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="ffd67-125">Enable cloud-delivered protection</span></span>](enable-cloud-protection-microsoft-defender-antivirus.md)

- [<span data-ttu-id="ffd67-126">Comment créer et déployer des stratégies de logiciel anti-programme malveillant : service de protection cloud</span><span class="sxs-lookup"><span data-stu-id="ffd67-126">How to create and deploy antimalware policies: Cloud-protection service</span></span>](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service)