---
title: Conditions préalables pour les comptes invité
description: Instructions de configuration pour les comptes invités et comment les ajuster
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
audience: Admin
ms.openlocfilehash: bbf679a01716fc48d37b241d69740f50a985f048
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51574606"
---
# <a name="prerequisites-for-guest-accounts"></a><span data-ttu-id="7d6db-104">Conditions préalables pour les comptes invité</span><span class="sxs-lookup"><span data-stu-id="7d6db-104">Prerequisites for guest accounts</span></span>

<span data-ttu-id="7d6db-105">Bureau géré Microsoft requiert les paramètres suivants dans votre organisation Azure AD pour l’accès au compte invité.</span><span class="sxs-lookup"><span data-stu-id="7d6db-105">Microsoft Managed Desktop requires the following settings in your Azure AD organization for guest account access.</span></span> <span data-ttu-id="7d6db-106">Vous pouvez ajuster ces paramètres sur le portail [Azure](https://portal.azure.com) sous **Identités externes /Collaboration externe**:</span><span class="sxs-lookup"><span data-stu-id="7d6db-106">You can adjust these settings at the [Azure portal](https://portal.azure.com) under **External Identities / External collaboration**:</span></span>

-   <span data-ttu-id="7d6db-107">**Les administrateurs et les utilisateurs du rôle d’invite d’invités** peuvent inviter des personnes définies sur **Oui**</span><span class="sxs-lookup"><span data-stu-id="7d6db-107">**Admins and users in the guest inviter role can invite** set to **Yes**</span></span>
-   <span data-ttu-id="7d6db-108">Pour **les restrictions de collaboration,** choisissez l’une des options ci-après :</span><span class="sxs-lookup"><span data-stu-id="7d6db-108">For **Collaboration restrictions**, choose any of these options:</span></span>
    -   <span data-ttu-id="7d6db-109">Si vous **sélectionnez Autoriser l’envoi d’invitations** à un domaine (le plus inclus), aucune autre configuration n’est requise.</span><span class="sxs-lookup"><span data-stu-id="7d6db-109">If you select **Allow invitations to be sent to any domain (most inclusive)**, no other configuration required.</span></span>
    -   <span data-ttu-id="7d6db-110">Si vous sélectionnez Refuser les invitations aux domaines **spécifiés,** assurez-vous Microsoft.com n’est pas répertorié dans les domaines cibles.</span><span class="sxs-lookup"><span data-stu-id="7d6db-110">If you select **Deny invitations to the specified domains**, make sure that Microsoft.com isn’t listed in the target domains.</span></span>
    -   <span data-ttu-id="7d6db-111">Si vous sélectionnez Autoriser les invitations uniquement aux domaines **spécifiés (les plus restrictifs),** assurez-vous que Microsoft.com est répertorié dans les domaines cibles. </span><span class="sxs-lookup"><span data-stu-id="7d6db-111">If you select **Allow invitations only to the specified domains (most restrictive)**, make sure that Microsoft.com *is* listed in the target domains.</span></span>

<span data-ttu-id="7d6db-112">Si vous définissez des restrictions qui interagissent avec ces paramètres, veillez à exclure les comptes azure Active Directory **Modern Workplace Service**.</span><span class="sxs-lookup"><span data-stu-id="7d6db-112">If you set restrictions that interact with these settings, make sure to exclude the Azure Active Directory **Modern Workplace Service Accounts**.</span></span> <span data-ttu-id="7d6db-113">Par exemple, si vous avez une stratégie d’accès conditionnel qui empêche les comptes invités d’accéder au portail Intune, excluez le groupe Comptes de **service** Workplace modernes de cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="7d6db-113">For example, if you have a conditional access policy that prevents guest accounts from accessing the Intune portal, exclude the **Modern Workplace Service Accounts** group from this policy.</span></span>

## <a name="steps-to-get-ready"></a><span data-ttu-id="7d6db-114">Étapes pour vous préparer</span><span class="sxs-lookup"><span data-stu-id="7d6db-114">Steps to get ready</span></span>

1. <span data-ttu-id="7d6db-115">Passer en [revue les conditions préalables pour le Bureau géré Microsoft.](prerequisites.md)</span><span class="sxs-lookup"><span data-stu-id="7d6db-115">Review [prerequisites for Microsoft Managed Desktop](prerequisites.md).</span></span>
2. <span data-ttu-id="7d6db-116">Utiliser les [outils d’évaluation de la préparation.](readiness-assessment-tool.md)</span><span class="sxs-lookup"><span data-stu-id="7d6db-116">Use [readiness assessment tools](readiness-assessment-tool.md).</span></span>
3. <span data-ttu-id="7d6db-117">[Conditions préalables pour les comptes invités](guest-accounts.md) (cet article)</span><span class="sxs-lookup"><span data-stu-id="7d6db-117">[Prerequisites for guest accounts](guest-accounts.md) (This article)</span></span>
4. [<span data-ttu-id="7d6db-118">Configuration du réseau pour Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="7d6db-118">Network configuration for Microsoft Managed Desktop</span></span>](network.md)
5. [<span data-ttu-id="7d6db-119">Préparer les certificats et les profils réseau pour le Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="7d6db-119">Prepare certificates and network profiles for Microsoft Managed Desktop</span></span>](certs-wifi-lan.md)
6. [<span data-ttu-id="7d6db-120">Préparer l’accès aux ressources locales pour le Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="7d6db-120">Prepare on-premises resources access for Microsoft Managed Desktop</span></span>](authentication.md)
7. [<span data-ttu-id="7d6db-121">Applications dans le Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="7d6db-121">Apps in Microsoft Managed Desktop</span></span>](apps.md)
8. [<span data-ttu-id="7d6db-122">Préparer les lecteurs mappés pour le Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="7d6db-122">Prepare mapped drives for Microsoft Managed Desktop</span></span>](mapped-drives.md)
9. [<span data-ttu-id="7d6db-123">Préparer des ressources d’impression pour le Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="7d6db-123">Prepare printing resources for Microsoft Managed Desktop</span></span>](printing.md)