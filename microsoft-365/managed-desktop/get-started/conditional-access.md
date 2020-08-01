---
title: Ajuster l’accès conditionnel
description: Procédure d’exclusion de certains comptes Microsoft
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: 8844c50f5faba609b3f5f53adc5ab45ba1dbaa74
ms.sourcegitcommit: 126d22d8abd190beb7101f14bd357005e4c729f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/30/2020
ms.locfileid: "46529682"
---
# <a name="adjust-conditional-access"></a><span data-ttu-id="ddb7c-104">Ajuster l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="ddb7c-104">Adjust conditional access</span></span>

<span data-ttu-id="ddb7c-105">Si vous utilisez des stratégies d' [accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) dans votre organisation, vous devez les définir pour exclure certains comptes afin que le bureau géré Microsoft puisse fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="ddb7c-105">If you use [conditional access](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) policies in your organization, you'll have to set them to exclude certain accounts so that Microsoft Managed Desktop can work properly.</span></span>

<span data-ttu-id="ddb7c-106">Pour cela, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ddb7c-106">To do this, follow these steps:</span></span>

1. <span data-ttu-id="ddb7c-107">Reportez-vous à la section « étapes de restauration » de la rubrique [How to : plan Your ConditionalAttribute Access Deployment in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access#rollback-steps).</span><span class="sxs-lookup"><span data-stu-id="ddb7c-107">Refer to the "Rollback steps" section of [How To: Plan your Conditional Access deployment in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access#rollback-steps).</span></span>
2. <span data-ttu-id="ddb7c-108">Suivez les étapes ci-dessous pour exclure le groupe de *comptes de service d’espace de travail moderne* pour toutes les stratégies.</span><span class="sxs-lookup"><span data-stu-id="ddb7c-108">Follow the steps there to exclude the *Modern Workplace Service Accounts* group for all policies.</span></span>


<span data-ttu-id="ddb7c-109">Si vous rencontrez des difficultés avec l’accès conditionnel, contactez le [support](../working-with-managed-desktop/admin-support.md)d’administration.</span><span class="sxs-lookup"><span data-stu-id="ddb7c-109">If you have any difficulty with conditional access, contact admin [support](../working-with-managed-desktop/admin-support.md).</span></span>

## <a name="steps-to-get-started-with-microsoft-managed-desktop"></a><span data-ttu-id="ddb7c-110">Étapes de prise en main de Microsoft Managed Desktop</span><span class="sxs-lookup"><span data-stu-id="ddb7c-110">Steps to get started with Microsoft Managed Desktop</span></span>

1. [<span data-ttu-id="ddb7c-111">Ajouter et vérifier des contacts d’administrateur dans le portail d’administration</span><span class="sxs-lookup"><span data-stu-id="ddb7c-111">Add and verify admin contacts in the Admin portal</span></span>](add-admin-contacts.md)
2. <span data-ttu-id="ddb7c-112">Ajuster l’accès conditionnel (cette rubrique)</span><span class="sxs-lookup"><span data-stu-id="ddb7c-112">Adjust conditional access (this topic)</span></span>
3. [<span data-ttu-id="ddb7c-113">Affecter des licences</span><span class="sxs-lookup"><span data-stu-id="ddb7c-113">Assign licenses</span></span>](assign-licenses.md)
4. [<span data-ttu-id="ddb7c-114">Déployer le portail d’entreprise Intune</span><span class="sxs-lookup"><span data-stu-id="ddb7c-114">Deploy Intune Company Portal</span></span>](company-portal.md)
5. [<span data-ttu-id="ddb7c-115">Activer Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="ddb7c-115">Enable Enterprise State Roaming</span></span>](enterprise-state-roaming.md)
6. [<span data-ttu-id="ddb7c-116">Configurer les appareils</span><span class="sxs-lookup"><span data-stu-id="ddb7c-116">Set up devices</span></span>](set-up-devices.md)
7. [<span data-ttu-id="ddb7c-117">Préparer vos utilisateurs à l’utilisation les appareils</span><span class="sxs-lookup"><span data-stu-id="ddb7c-117">Get your users ready to use devices</span></span>](get-started-devices.md)
8. [<span data-ttu-id="ddb7c-118">Déployer des applications</span><span class="sxs-lookup"><span data-stu-id="ddb7c-118">Deploy apps</span></span>](deploy-apps.md)
