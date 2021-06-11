---
title: Activer le retrait de définition pour Antivirus Microsoft Defender
description: Activez le retrait de définition pour Antivirus Microsoft Defender.
keywords: Antivirus Microsoft Defender logiciel anti-programme malveillant, sécurité, defender, retrait de définition
search.product: eADQiWindows 10XVcnh
ms.pagetype: security
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.date: 06/10/2021
ms.reviewer: ''
manager: dansimp
ms.custom: nextgen
ms.technology: mde
ms.topic: article
ms.openlocfilehash: 505270d319a78de20bf6fed01b7ca79c9fc2b400
ms.sourcegitcommit: 33d19853a38dfa4e6ed21b313976643670a14581
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "52903803"
---
# <a name="turn-on-definition-retirement"></a><span data-ttu-id="49b6b-104">Activer le retrait des définitions</span><span class="sxs-lookup"><span data-stu-id="49b6b-104">Turn on definition retirement</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="49b6b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="49b6b-105">**Applies to:**</span></span>

- [<span data-ttu-id="49b6b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="49b6b-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="49b6b-107">Vous pouvez configurer le retrait des définitions à l’aide de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="49b6b-107">You can configure definition retirement using Group Policy.</span></span> <span data-ttu-id="49b6b-108">La définition du retrait vérifie si un ordinateur dispose des mises à jour de sécurité requises pour le protéger contre une vulnérabilité particulière.</span><span class="sxs-lookup"><span data-stu-id="49b6b-108">Definition retirement checks to see if a computer has the required security updates necessary to protect it against a particular vulnerability.</span></span> <span data-ttu-id="49b6b-109">Si le système n’est pas vulnérable à l’exploit détecté par une définition, cette définition est « retirée ».</span><span class="sxs-lookup"><span data-stu-id="49b6b-109">If the system is not vulnerable to the exploit detected by a definition, then that definition is "retired".</span></span> <span data-ttu-id="49b6b-110">Si toutes les informations de sécurité pour un protocole donné sont retirées, ce protocole n’est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="49b6b-110">If all security intelligence for a given protocol are retired then that protocol is no longer parsed.</span></span> <span data-ttu-id="49b6b-111">L’activation de cette fonctionnalité permet d’améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="49b6b-111">Enabling this feature helps to improve performance.</span></span> <span data-ttu-id="49b6b-112">Sur un ordinateur à jour avec toutes les dernières mises à jour de sécurité, la protection du réseau n’aura aucun impact sur les performances du réseau.</span><span class="sxs-lookup"><span data-stu-id="49b6b-112">On a computer that is up-to-date with all the latest security updates, network protection will have no impact on network performance.</span></span>

## <a name="use-group-policy-to-configure-definition-retirement"></a><span data-ttu-id="49b6b-113">Utiliser la stratégie de groupe pour configurer le retrait des définitions</span><span class="sxs-lookup"><span data-stu-id="49b6b-113">Use Group Policy to configure definition retirement</span></span>

1. <span data-ttu-id="49b6b-114">Sur votre point de terminaison de gestion des stratégies de groupe, ouvrez la [console de gestion des stratégies de groupe.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="49b6b-114">On your Group Policy management endpoint, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)).</span></span>

2. <span data-ttu-id="49b6b-115">Go to **Computer Configuration**  >  **Administrative Templates** Windows  >  **Components**  >  **Antivirus Microsoft Defender** Network  >  **Inspection System**.</span><span class="sxs-lookup"><span data-stu-id="49b6b-115">Go to **Computer Configuration** > **Administrative Templates** > **Windows Components** > **Microsoft Defender Antivirus** > **Network Inspection System**.</span></span> 

3. <span data-ttu-id="49b6b-116">Sélectionnez **Activer le retrait de définition.**</span><span class="sxs-lookup"><span data-stu-id="49b6b-116">Select **Turn on definition retirement**.</span></span> <span data-ttu-id="49b6b-117">Par défaut, cette stratégie est activée.</span><span class="sxs-lookup"><span data-stu-id="49b6b-117">By default, this policy is enabled.</span></span> <span data-ttu-id="49b6b-118">Si la définition **n’est pas configurée,** le retrait de définition est activé.</span><span class="sxs-lookup"><span data-stu-id="49b6b-118">If set **Not configured**, definition retirement is enabled.</span></span> 

4. <span data-ttu-id="49b6b-119">Pour modifier la stratégie, sélectionnez le lien **modifier le paramètre de stratégie.**</span><span class="sxs-lookup"><span data-stu-id="49b6b-119">To edit the policy, select the **edit policy setting** link.</span></span>

5. <span data-ttu-id="49b6b-120">Sélectionnez **Activé,** puis **OK**.</span><span class="sxs-lookup"><span data-stu-id="49b6b-120">Select **Enabled**, and then select **OK**.</span></span>

6. <span data-ttu-id="49b6b-121">Déployez votre objet de stratégie de groupe mis à jour.</span><span class="sxs-lookup"><span data-stu-id="49b6b-121">Deploy your updated Group Policy Object.</span></span> <span data-ttu-id="49b6b-122">Voir [La Console de gestion des stratégies de groupe.](/windows/win32/srvnodes/group-policy)</span><span class="sxs-lookup"><span data-stu-id="49b6b-122">See [Group Policy Management Console](/windows/win32/srvnodes/group-policy).</span></span>

> [!TIP]
> <span data-ttu-id="49b6b-123">Utilisez-vous des objets de stratégie de groupe en local ?</span><span class="sxs-lookup"><span data-stu-id="49b6b-123">Are you using Group Policy Objects on premises?</span></span> <span data-ttu-id="49b6b-124">Découvrez comment ils traduisent dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="49b6b-124">See how they translate in the cloud.</span></span> <span data-ttu-id="49b6b-125">[Analysez vos objets de stratégie](/mem/intune/configuration/group-policy-analytics)de groupe en local à l’aide de l’analyse de stratégie de groupe dans Microsoft Endpoint Manager - Aperçu .</span><span class="sxs-lookup"><span data-stu-id="49b6b-125">[Analyze your on-premises group policy objects using Group Policy analytics in Microsoft Endpoint Manager - Preview](/mem/intune/configuration/group-policy-analytics).</span></span> 
  
