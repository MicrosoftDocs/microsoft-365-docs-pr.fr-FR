---
title: 'Étape 4 : Configurer la protection des informations Windows'
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/19/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et déployez la protection des informations Windows dans Microsoft 365.
ms.openlocfilehash: c7b76ef28d41810d6e9e45e98adb7a94cf8ae2f4
ms.sourcegitcommit: 634abe8a237e27dfe82376e6ef32280aab5d4a27
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2020
ms.locfileid: "45005721"
---
# <a name="step-4-configure-windows-information-protection"></a><span data-ttu-id="d31f8-103">Étape 4 : Configurer la protection des informations Windows</span><span class="sxs-lookup"><span data-stu-id="d31f8-103">Step 4: Configure Windows Information Protection</span></span>

<span data-ttu-id="d31f8-104">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="d31f8-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![Phase 6 : Protection des informations](../media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="d31f8-106">L’augmentation du nombre d’appareils personnels utilisés au travail entraîne un risque accru de fuite de données.</span><span class="sxs-lookup"><span data-stu-id="d31f8-106">With more personal devices being used for work, there’s increased risk for apps and devices to leak private organization data.</span></span> <span data-ttu-id="d31f8-107">Par exemple, un employé risque de diffuser par inadvertance l’image d’un plan marketing de futur produit sur un site de réseau social ou d’enregistrer un fichier contenant des informations hautement confidentielles sur son stockage cloud public.</span><span class="sxs-lookup"><span data-stu-id="d31f8-107">For example, an employee inadvertently sends a picture of a marketing plan for a future product to a social media site or saves a file containing highly confidential information to their public cloud storage.</span></span> 

<span data-ttu-id="d31f8-108">La Protection des informations Windows contribue à protéger contre ces types de fuites de données sur des appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d31f8-108">Windows Information Protection (WIP) helps protect against these types of data leakage on Windows 10 devices.</span></span> <span data-ttu-id="d31f8-109">Pour plus d’informations, voir [Protéger vos données d’entreprise à l’aide de Protection des informations Windows](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span><span class="sxs-lookup"><span data-stu-id="d31f8-109">For more information, see [Protect your enterprise data using WIP](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="d31f8-110">Dans Microsoft 365 Entreprise, la Protection des informations Windows est une combinaison de Windows 10 Entreprise et de Microsoft Intune, fournie avec votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="d31f8-110">In Microsoft 365 Enterprise, WIP is a combination of Windows 10 Enterprise and Microsoft Intune, which is included with your subscription.</span></span> 

<span data-ttu-id="d31f8-111">Pour déployer la Protection des informations Windows dans votre organisation avec Microsoft 365 Entreprise :</span><span class="sxs-lookup"><span data-stu-id="d31f8-111">To deploy WIP in your organization with Microsoft 365 Enterprise:</span></span>

1. <span data-ttu-id="d31f8-112">Inscrivez vos appareils Windows dans Intune.</span><span class="sxs-lookup"><span data-stu-id="d31f8-112">Enroll your Windows devices in Intune.</span></span> <span data-ttu-id="d31f8-113">Vous devez avoir effectué cette opération à l’[Étape 5 : Gestion des appareils mobiles](mobility-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="d31f8-113">You should have done this in [Phase 5: Mobile Device Management](mobility-infrastructure.md).</span></span>

2. <span data-ttu-id="d31f8-114">Créez une [stratégie Intune pour la Protection des informations Windows](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/create-wip-policy-using-intune-azure).</span><span class="sxs-lookup"><span data-stu-id="d31f8-114">Create an [Intune policy for WIP](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/create-wip-policy-using-intune-azure).</span></span>

   -    <span data-ttu-id="d31f8-115">Vérifiez que vous avez rempli votre liste d’applications protégées.</span><span class="sxs-lookup"><span data-stu-id="d31f8-115">Ensure that you have filled out your Protected apps list.</span></span>
  
   - <span data-ttu-id="d31f8-116">Choisissez votre niveau de Protection des informations Windows.</span><span class="sxs-lookup"><span data-stu-id="d31f8-116">Choose your WIP protection level.</span></span>

<span data-ttu-id="d31f8-117">Vous pouvez aussi utiliser Travaux en cours avec [Microsoft Endpoint Configuration Manager](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/create-wip-policy-using-configmgr).</span><span class="sxs-lookup"><span data-stu-id="d31f8-117">You can also use WIP with [Microsoft Endpoint Configuration Manager](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/create-wip-policy-using-configmgr).</span></span> 

<span data-ttu-id="d31f8-118">Pour plus d’informations, voir [Meilleures pratiques de Protection des informations Windows]( https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/guidance-and-best-practices-wip).</span><span class="sxs-lookup"><span data-stu-id="d31f8-118">See [WIP best practices]( https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/guidance-and-best-practices-wip) for more information.</span></span>

<span data-ttu-id="d31f8-119">Comme point de contrôle intermédiaire, consultez les [critères de sortie](infoprotect-exit-criteria.md#crit-infoprotect-step4) correspondant à cette étape.</span><span class="sxs-lookup"><span data-stu-id="d31f8-119">As an interim checkpoint, see the [exit criteria](infoprotect-exit-criteria.md#crit-infoprotect-step4) corresponding to this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="d31f8-120">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="d31f8-120">Next step</span></span>

|||
|:-------|:-----|
|![Étape 5](../media/stepnumbers/Step5.png)|[<span data-ttu-id="d31f8-122">Configurer la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="d31f8-122">Configure Data Loss Prevention</span></span>](infoprotect-data-loss-prevention.md)|


