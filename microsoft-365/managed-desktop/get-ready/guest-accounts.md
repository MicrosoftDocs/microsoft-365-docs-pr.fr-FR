---
title: Conditions préalables pour les comptes invités
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
# <a name="prerequisites-for-guest-accounts"></a><span data-ttu-id="377dc-104">Conditions préalables pour les comptes invités</span><span class="sxs-lookup"><span data-stu-id="377dc-104">Prerequisites for guest accounts</span></span>

<span data-ttu-id="377dc-105">Microsoft Managed Desktop requiert les paramètres suivants dans votre organisation Azure AD pour l’accès au compte invité.</span><span class="sxs-lookup"><span data-stu-id="377dc-105">Microsoft Managed Desktop requires the following settings in your Azure AD organization for guest account access.</span></span> <span data-ttu-id="377dc-106">Vous pouvez ajuster ces paramètres sur le [portail Azure](https://portal.azure.com) sous **identités externes/collaboration externe** :</span><span class="sxs-lookup"><span data-stu-id="377dc-106">You can adjust these settings at the [Azure portal](https://portal.azure.com) under **External Identities / External collaboration** :</span></span>

-   <span data-ttu-id="377dc-107">Les **administrateurs et les utilisateurs du rôle invités invité peuvent inviter la** valeur **Oui**</span><span class="sxs-lookup"><span data-stu-id="377dc-107">**Admins and users in the guest inviter role can invite** set to **Yes**</span></span>
-   <span data-ttu-id="377dc-108">Pour les **restrictions de collaboration** , choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="377dc-108">For **Collaboration restrictions** , choose any of these options:</span></span>
    -   <span data-ttu-id="377dc-109">Si vous sélectionnez **autoriser l’envoi d’invitations à n’importe quel domaine (la plus incluse)** , aucune autre configuration n’est requise.</span><span class="sxs-lookup"><span data-stu-id="377dc-109">If you select **Allow invitations to be sent to any domain (most inclusive)** , no other configuration required.</span></span>
    -   <span data-ttu-id="377dc-110">Si vous sélectionnez **refuser les invitations aux domaines spécifiés** , vérifiez que Microsoft.com n’est pas indiqué dans les domaines cibles.</span><span class="sxs-lookup"><span data-stu-id="377dc-110">If you select **Deny invitations to the specified domains** , make sure that Microsoft.com isn’t listed in the target domains.</span></span>
    -   <span data-ttu-id="377dc-111">Si vous sélectionnez **autoriser uniquement les invitations aux domaines spécifiés (le plus restrictif)** , assurez-vous que Microsoft.com *est* indiqué dans les domaines cibles.</span><span class="sxs-lookup"><span data-stu-id="377dc-111">If you select **Allow invitations only to the specified domains (most restrictive)** , make sure that Microsoft.com *is* listed in the target domains.</span></span>

<span data-ttu-id="377dc-112">Si vous définissez des restrictions qui interagissent avec ces paramètres, veillez à exclure les **comptes de service espace de travail moderne** Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="377dc-112">If you set restrictions that interact with these settings, make sure to exclude the Azure Active Directory **Modern Workplace Service Accounts**.</span></span> <span data-ttu-id="377dc-113">Par exemple, si vous avez une stratégie d’accès conditionnel qui empêche les comptes invités d’accéder au portail Intune, excluez le groupe de comptes de service de l' **espace de travail moderne** de cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="377dc-113">For example, if you have a conditional access policy that prevents guest accounts from accessing the Intune portal, exclude the **Modern Workplace Service Accounts** group from this policy.</span></span>

