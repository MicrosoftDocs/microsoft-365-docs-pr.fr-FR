---
title: 'Étape 4 : Planifier des modifications d’adresse URL et d’adresse IP'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/05/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: ''
ms.openlocfilehash: 44990dcfd09e5cc2a44666da43fdeeaffd59da7d
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26866829"
---
# <a name="step-4-plan-for-url-and-ip-address-changes"></a><span data-ttu-id="a8765-102">Étape 4 : Planifier des modifications d’adresse URL et d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="a8765-102">Step 4: Plan for URL and IP address changes</span></span>

<span data-ttu-id="a8765-103">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="a8765-103">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/networking_icon-small.png)

>[!Note]
><span data-ttu-id="a8765-p101">Cette étape requiert l’[Étape 3](networking-configure-proxies-firewalls.md). Si vous n’avez pas suivi l’Étape 3, vous pouvez passer à l’[Étape 5](networking-optimize-tcp-performance.md).</span><span class="sxs-lookup"><span data-stu-id="a8765-p101">This step requires [Step 3](networking-configure-proxies-firewalls.md). If you have not done Step 3, you can skip to [Step 5](networking-optimize-tcp-performance.md).</span></span>
>

<span data-ttu-id="a8765-p102">Les URL et adresses IP utilisées par le réseau Microsoft 365 général changent au fil du temps, donc il est important de planifier des mises à jour de ces points de terminaison. Par exemple, vous devrez peut-être reconfigurer vos appareils de périmètre de sécurité avec les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a8765-p102">The URLs and IP addresses used by the global Microsoft 365 network change over time, so it’s important to plan for updates to these endpoints. For example, you may need to reconfigure your security perimeter devices with:</span></span>

- <span data-ttu-id="a8765-108">de nouvelles URL pour les nouveaux services qui nécessiteront un traitement facile ;</span><span class="sxs-lookup"><span data-stu-id="a8765-108">New URLs for new services that will need unhindered processing</span></span>
- <span data-ttu-id="a8765-109">des URL supprimées pour les services qui ne sont plus disponibles ;</span><span class="sxs-lookup"><span data-stu-id="a8765-109">Removed URLs for discontinued services</span></span>
- <span data-ttu-id="a8765-110">de nouvelles plages d’adresses IP pour les nouveaux emplacements réseau Microsoft et serveurs sur Internet ;</span><span class="sxs-lookup"><span data-stu-id="a8765-110">New IP address ranges for new Microsoft network locations and servers on the Internet</span></span> 
- <span data-ttu-id="a8765-111">des modifications des plages d’adresses IP pour les différents services.</span><span class="sxs-lookup"><span data-stu-id="a8765-111">Changes in IP address ranges for the different services</span></span>

<span data-ttu-id="a8765-112">Pour plus d’informations sur l’établissement d’un plan d’implémentation pour les modifications des points de terminaison, qui inclut les notifications de ces modifications, reportez-vous aux rubriques [Gestion des points de terminaison Office 365 - Intégration](https://support.office.com/article/Managing-Office-365-endpoints-99cab9d4-ef59-4207-9f2b-3728eb46bf9a?ui=en-US#ID0EABAAA=2._Proxies&ID0EAEAAA=3._Integration) et [Gestion des points de terminaison Office 365 - Proxys](https://support.office.com/article/Managing-Office-365-endpoints-99cab9d4-ef59-4207-9f2b-3728eb46bf9a#ID0EABAAA=2._Proxies&ID0EAEAAA=2._Proxies).</span><span class="sxs-lookup"><span data-stu-id="a8765-112">For more information about establishing an implementation plan for changes in endpoints, which includes being notified of changes, see [Managing Office 365 endpoints-Integration](https://support.office.com/article/Managing-Office-365-endpoints-99cab9d4-ef59-4207-9f2b-3728eb46bf9a?ui=en-US#ID0EABAAA=2._Proxies&ID0EAEAAA=3._Integration) and [Managing Office 365 endpoints-Proxies](https://support.office.com/article/Managing-Office-365-endpoints-99cab9d4-ef59-4207-9f2b-3728eb46bf9a#ID0EABAAA=2._Proxies&ID0EAEAAA=2._Proxies).</span></span>

<span data-ttu-id="a8765-113">Comme point de vérification intermédiaire, vous pouvez consultez les [critères de sortie](networking-exit-criteria.md#crit-networking-step4) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="a8765-113">As an interim checkpoint, you can see the [exit criteria](networking-exit-criteria.md#crit-networking-step4) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="a8765-114">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="a8765-114">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step5.png)|[<span data-ttu-id="a8765-115">Optimiser les performances du service Office 365 et du client</span><span class="sxs-lookup"><span data-stu-id="a8765-115">Optimize client and Office 365 service performance</span></span>](networking-optimize-tcp-performance.md)|
