---
title: Ajuster l’accès conditionnel
description: Procédure d’exclusion de certains comptes Microsoft
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 1bc5d937616cba60c5af43fe22a7c4dccf89a55e
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42085804"
---
# <a name="adjust-conditional-access"></a><span data-ttu-id="47dd9-104">Ajuster l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="47dd9-104">Adjust conditional access</span></span>

<span data-ttu-id="47dd9-105">Si vous utilisez des stratégies d' [accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) dans votre organisation, vous devez les définir pour exclure certains comptes afin que le bureau géré Microsoft puisse fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="47dd9-105">If you use [conditional access](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) policies in your organization, you'll have to set them to exclude certain accounts so that Microsoft Managed Desktop can work properly.</span></span>

<span data-ttu-id="47dd9-106">Pour cela, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="47dd9-106">To do this, follow these steps:</span></span>

1. <span data-ttu-id="47dd9-107">Reportez-vous à la section « étapes de restauration » de la rubrique [How to : plan Your ConditionalAttribute Access Deployment in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access#rollback-steps).</span><span class="sxs-lookup"><span data-stu-id="47dd9-107">Refer to the "Rollback steps" section of [How To: Plan your Conditional Access deployment in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access#rollback-steps).</span></span>
2. <span data-ttu-id="47dd9-108">Suivez les étapes ci-dessous pour exclure le groupe de *comptes de service d’espace de travail moderne* pour toutes les stratégies.</span><span class="sxs-lookup"><span data-stu-id="47dd9-108">Follow the steps there to exclude the *Modern Workplace Service Accounts* group for all policies.</span></span>


<span data-ttu-id="47dd9-109">Si vous rencontrez des difficultés avec l’accès conditionnel, contactez le [support](../working-with-managed-desktop/admin-support.md)d’administration.</span><span class="sxs-lookup"><span data-stu-id="47dd9-109">If you have any difficulty with conditional access, contact admin [support](../working-with-managed-desktop/admin-support.md).</span></span>

## <a name="steps-to-get-started-with-microsoft-managed-desktop"></a><span data-ttu-id="47dd9-110">Étapes de prise en main de Microsoft Managed Desktop</span><span class="sxs-lookup"><span data-stu-id="47dd9-110">Steps to get started with Microsoft Managed Desktop</span></span>

1. [<span data-ttu-id="47dd9-111">Ajouter et vérifier des contacts d’administrateur dans le portail d’administration</span><span class="sxs-lookup"><span data-stu-id="47dd9-111">Add and verify admin contacts in the Admin portal</span></span>](add-admin-contacts.md)
2. <span data-ttu-id="47dd9-112">Ajuster l’accès conditionnel (cette rubrique)</span><span class="sxs-lookup"><span data-stu-id="47dd9-112">Adjust conditional access (this topic)</span></span>
3. [<span data-ttu-id="47dd9-113">Affecter des licences</span><span class="sxs-lookup"><span data-stu-id="47dd9-113">Assign licenses</span></span>](assign-licenses.md)
4. [<span data-ttu-id="47dd9-114">Déployer le portail d’entreprise Intune</span><span class="sxs-lookup"><span data-stu-id="47dd9-114">Deploy Intune Company Portal</span></span>](company-portal.md)
5. [<span data-ttu-id="47dd9-115">Activer Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="47dd9-115">Enable Enterprise State Roaming</span></span>](enterprise-state-roaming.md)
6. [<span data-ttu-id="47dd9-116">Configurer les appareils</span><span class="sxs-lookup"><span data-stu-id="47dd9-116">Set up devices</span></span>](set-up-devices.md)
7. [<span data-ttu-id="47dd9-117">Préparer vos utilisateurs à l’utilisation des appareils</span><span class="sxs-lookup"><span data-stu-id="47dd9-117">Get your users ready to use devices</span></span>](get-started-devices.md)
8. [<span data-ttu-id="47dd9-118">Déployer des applications</span><span class="sxs-lookup"><span data-stu-id="47dd9-118">Deploy apps</span></span>](deploy-apps.md)
