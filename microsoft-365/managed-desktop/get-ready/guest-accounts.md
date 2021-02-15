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
ms.openlocfilehash: d8953e9f451daa02671a1e1544f2dfe6649ab1b3
ms.sourcegitcommit: fcc1b40732f28f075d95faffc1655473e262dd95
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2020
ms.locfileid: "49073202"
---
# <a name="prerequisites-for-guest-accounts"></a><span data-ttu-id="d2d9b-104">Conditions préalables pour les comptes invité</span><span class="sxs-lookup"><span data-stu-id="d2d9b-104">Prerequisites for guest accounts</span></span>

<span data-ttu-id="d2d9b-105">Bureau géré Microsoft requiert les paramètres suivants dans votre organisation Azure AD pour l’accès au compte invité.</span><span class="sxs-lookup"><span data-stu-id="d2d9b-105">Microsoft Managed Desktop requires the following settings in your Azure AD organization for guest account access.</span></span> <span data-ttu-id="d2d9b-106">Vous pouvez ajuster ces paramètres sur le portail [Azure](https://portal.azure.com) sous **Identités externes /Collaboration externe**:</span><span class="sxs-lookup"><span data-stu-id="d2d9b-106">You can adjust these settings at the [Azure portal](https://portal.azure.com) under **External Identities / External collaboration**:</span></span>

-   <span data-ttu-id="d2d9b-107">**Les administrateurs et les utilisateurs du rôle d’invite d’invités** peuvent inviter des personnes définies sur **Oui**</span><span class="sxs-lookup"><span data-stu-id="d2d9b-107">**Admins and users in the guest inviter role can invite** set to **Yes**</span></span>
-   <span data-ttu-id="d2d9b-108">Pour **les restrictions de collaboration,** choisissez l’une des options ci-après :</span><span class="sxs-lookup"><span data-stu-id="d2d9b-108">For **Collaboration restrictions**, choose any of these options:</span></span>
    -   <span data-ttu-id="d2d9b-109">Si vous **sélectionnez Autoriser l’envoi d’invitations** à un domaine (le plus inclus), aucune autre configuration n’est requise.</span><span class="sxs-lookup"><span data-stu-id="d2d9b-109">If you select **Allow invitations to be sent to any domain (most inclusive)**, no other configuration required.</span></span>
    -   <span data-ttu-id="d2d9b-110">Si vous sélectionnez Refuser les invitations aux domaines **spécifiés,** assurez-vous Microsoft.com n’est pas répertorié dans les domaines cibles.</span><span class="sxs-lookup"><span data-stu-id="d2d9b-110">If you select **Deny invitations to the specified domains**, make sure that Microsoft.com isn’t listed in the target domains.</span></span>
    -   <span data-ttu-id="d2d9b-111">Si vous sélectionnez Autoriser les invitations uniquement aux domaines **spécifiés (les plus restrictifs),** assurez-vous que Microsoft.com est répertorié dans les domaines cibles. </span><span class="sxs-lookup"><span data-stu-id="d2d9b-111">If you select **Allow invitations only to the specified domains (most restrictive)**, make sure that Microsoft.com *is* listed in the target domains.</span></span>

<span data-ttu-id="d2d9b-112">Si vous définissez des restrictions qui interagissent avec ces paramètres, veillez à exclure les comptes azure Active Directory **Modern Workplace Service**.</span><span class="sxs-lookup"><span data-stu-id="d2d9b-112">If you set restrictions that interact with these settings, make sure to exclude the Azure Active Directory **Modern Workplace Service Accounts**.</span></span> <span data-ttu-id="d2d9b-113">Par exemple, si vous avez une stratégie d’accès conditionnel qui empêche les comptes invités d’accéder au portail Intune, excluez le groupe Comptes de **service** Workplace modernes de cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="d2d9b-113">For example, if you have a conditional access policy that prevents guest accounts from accessing the Intune portal, exclude the **Modern Workplace Service Accounts** group from this policy.</span></span>

