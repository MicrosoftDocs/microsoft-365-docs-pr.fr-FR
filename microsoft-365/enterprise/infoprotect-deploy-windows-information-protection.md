---
title: 'Étape 4 : Configurer la protection des informations Windows'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/25/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et déployez la protection des informations Windows dans Microsoft 365.
ms.openlocfilehash: ca706d49053bbc100a633afb74c7c978de2e4c5c
ms.sourcegitcommit: 3b2d3e2b38c4860db977e73dda119a465c669fa4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2019
ms.locfileid: "33353099"
---
# <a name="step-4-configure-windows-information-protection"></a><span data-ttu-id="02f89-103">Étape 4 : Configurer la protection des informations Windows</span><span class="sxs-lookup"><span data-stu-id="02f89-103">Step 4: Configure Windows Information Protection</span></span>

<span data-ttu-id="02f89-104">*Cette étape facultative s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="02f89-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="02f89-105">L’augmentation du nombre d’appareils personnels utilisés au travail entraîne un risque accru de fuite de données.</span><span class="sxs-lookup"><span data-stu-id="02f89-105">With more personal devices being used for work, there’s increased risk for apps and devices to leak private organization data.</span></span> <span data-ttu-id="02f89-106">Par exemple, un employé risque de diffuser par inadvertance l’image d’un plan marketing de futur produit sur un site de réseau social ou d’enregistrer un fichier contenant des informations hautement confidentielles sur son stockage cloud public.</span><span class="sxs-lookup"><span data-stu-id="02f89-106">For example, an employee inadvertently sends a picture of a marketing plan for a future product to a social media site or saves a file containing highly confidential information to their public cloud storage.</span></span> 

<span data-ttu-id="02f89-107">La Protection des informations Windows contribue à protéger contre ces types de fuites de données sur des appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="02f89-107">Windows Information Protection (WIP) helps protect against these types of data leakage on Windows 10 devices.</span></span> <span data-ttu-id="02f89-108">Pour plus d’informations, voir [Protéger vos données d’entreprise à l’aide de Protection des informations Windows](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span><span class="sxs-lookup"><span data-stu-id="02f89-108">For more information, see [Protect your enterprise data using WIP](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="02f89-109">Dans Microsoft 365 Entreprise, la Protection des informations Windows est une combinaison de Windows 10 Entreprise et de Microsoft Intune, fournie avec Enterprise Mobility + Security dans le cadre de votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="02f89-109">In Microsoft 365 Enterprise, WIP is a combination of Windows 10 Enterprise and Microsoft Intune, which is included with Enterprise Mobility + Security (EMS) in your subscription.</span></span> 

<span data-ttu-id="02f89-110">Pour déployer la Protection des informations Windows dans votre organisation avec Microsoft 365 Entreprise :</span><span class="sxs-lookup"><span data-stu-id="02f89-110">To deploy WIP in your organization with Microsoft 365 Enterprise:</span></span>

1. <span data-ttu-id="02f89-111">Inscrivez vos appareils Windows dans Intune.</span><span class="sxs-lookup"><span data-stu-id="02f89-111">Enroll your Windows devices in Intune.</span></span> <span data-ttu-id="02f89-112">Vous devez avoir effectué cette opération à l’[Étape 5 : Gestion des appareils mobiles](mobility-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="02f89-112">You should have done this in [Phase 5: Mobile Device Management](mobility-infrastructure.md).</span></span>
2. <span data-ttu-id="02f89-113">Créez une [stratégie Intune pour la Protection des informations Windows](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/create-wip-policy-using-intune-azure).</span><span class="sxs-lookup"><span data-stu-id="02f89-113">Create an [Intune policy for WIP](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/create-wip-policy-using-intune-azure).</span></span>
  - <span data-ttu-id="02f89-114">Vérifiez que vous avez rempli votre liste d’applications protégées.</span><span class="sxs-lookup"><span data-stu-id="02f89-114">Ensure that you have filled out your Protected apps list.</span></span>
  - <span data-ttu-id="02f89-115">Choisissez votre niveau de Protection des informations Windows.</span><span class="sxs-lookup"><span data-stu-id="02f89-115">Choose your WIP protection level.</span></span>

<span data-ttu-id="02f89-116">Vous pouvez également utiliser la Protection des informations Windows avec [System Center Configuration Manager](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/overview-create-wip-policy-sccm).</span><span class="sxs-lookup"><span data-stu-id="02f89-116">You can also use WIP with [System Center Configuration Manager](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/overview-create-wip-policy-sccm).</span></span> 

<span data-ttu-id="02f89-117">Pour plus d’informations, voir [Meilleures pratiques de Protection des informations Windows]( https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/guidance-and-best-practices-wip).</span><span class="sxs-lookup"><span data-stu-id="02f89-117">See [WIP best practices]( https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/guidance-and-best-practices-wip) for more information.</span></span>

<span data-ttu-id="02f89-118">Comme point de contrôle intermédiaire, consultez les [critères de sortie](infoprotect-exit-criteria.md#crit-infoprotect-step4) correspondant à cette étape.</span><span class="sxs-lookup"><span data-stu-id="02f89-118">As an interim checkpoint, see the [exit criteria](infoprotect-exit-criteria.md#crit-infoprotect-step4) corresponding to this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="02f89-119">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="02f89-119">Next step</span></span>


|||
|:-------|:-----|
|![](./media/stepnumbers/Step5.png)|[<span data-ttu-id="02f89-120">Configurer la protection contre la perte de données d’Office 365</span><span class="sxs-lookup"><span data-stu-id="02f89-120">Office 365 Data Loss Prevention (DLP)</span></span>](infoprotect-data-loss-prevention.md)|


