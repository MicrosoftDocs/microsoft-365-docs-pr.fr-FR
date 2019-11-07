---
title: Ajustement de l’accès conditionnel
description: Procédure d’exclusion de certains comptes Microsoft
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 1b91186837ad558965d675f82d013a7081c7c7ec
ms.sourcegitcommit: 3d37043c0447359c952dc99026c219dd69f6fb8d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "38012461"
---
# <a name="adjust-conditional-access"></a><span data-ttu-id="be740-104">Ajustement de l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="be740-104">Adjust conditional access</span></span>

<span data-ttu-id="be740-105">Si vous utilisez des stratégies d' [accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) dans votre organisation, vous devez les définir pour exclure certains comptes afin que le bureau géré Microsoft puisse fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="be740-105">If you use [conditional access](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) policies in your organization, you'll have to set them to exclude certain accounts so that Microsoft Managed Desktop can work properly.</span></span>

<span data-ttu-id="be740-106">Pour cela, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="be740-106">To do this, follow these steps:</span></span>

1. <span data-ttu-id="be740-107">Reportez-vous à la section « étapes de restauration » de la rubrique [How to : plan Your ConditionalAttribute Access Deployment in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access#rollback-steps).</span><span class="sxs-lookup"><span data-stu-id="be740-107">Refer to the "Rollback steps" section of [How To: Plan your Conditional Access deployment in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access#rollback-steps).</span></span>
2. <span data-ttu-id="be740-108">Suivez les étapes ci-dessous pour exclure le groupe de *comptes de service d’espace de travail moderne* pour toutes les stratégies.</span><span class="sxs-lookup"><span data-stu-id="be740-108">Follow the steps there to exclude the *Modern Workplace Service Accounts* group for all policies.</span></span>


<span data-ttu-id="be740-109">Si vous rencontrez des difficultés avec l’accès conditionnel, contactez le [support](../working-with-managed-desktop/admin-support.md)d’administration.</span><span class="sxs-lookup"><span data-stu-id="be740-109">If you have any difficulty with conditional access, contact admin [support](../working-with-managed-desktop/admin-support.md).</span></span>

## <a name="steps-to-get-started-with-microsoft-managed-desktop"></a><span data-ttu-id="be740-110">Étapes de prise en main de Microsoft Managed Desktop</span><span class="sxs-lookup"><span data-stu-id="be740-110">Steps to get started with Microsoft Managed Desktop</span></span>

1. [<span data-ttu-id="be740-111">Ajouter et vérifier des contacts d’administration dans le portail d’administration</span><span class="sxs-lookup"><span data-stu-id="be740-111">Add and verify admin contacts in the Admin portal</span></span>](add-admin-contacts.md)
2. <span data-ttu-id="be740-112">Ajuster l’accès conditionnel (cette rubrique)</span><span class="sxs-lookup"><span data-stu-id="be740-112">Adjust conditional access (this topic)</span></span>
3. [<span data-ttu-id="be740-113">Attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="be740-113">Assign licenses</span></span>](assign-licenses.md)
4. [<span data-ttu-id="be740-114">Déployer le portail d’entreprise Intune</span><span class="sxs-lookup"><span data-stu-id="be740-114">Deploy Intune Company Portal</span></span>](company-portal.md)
5. [<span data-ttu-id="be740-115">Activer l’itinérance de l’état d’entreprise</span><span class="sxs-lookup"><span data-stu-id="be740-115">Enable Enterprise State Roaming</span></span>](enterprise-state-roaming.md)
6. [<span data-ttu-id="be740-116">Configurer les appareils</span><span class="sxs-lookup"><span data-stu-id="be740-116">Set up devices</span></span>](set-up-devices.md)
7. [<span data-ttu-id="be740-117">Préparer vos utilisateurs à l’utilisation des appareils</span><span class="sxs-lookup"><span data-stu-id="be740-117">Get your users ready to use devices</span></span>](get-started-devices.md)
8. [<span data-ttu-id="be740-118">Déployer des applications</span><span class="sxs-lookup"><span data-stu-id="be740-118">Deploy apps</span></span>](deploy-apps.md)