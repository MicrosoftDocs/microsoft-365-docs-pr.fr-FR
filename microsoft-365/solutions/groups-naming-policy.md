---
title: Microsoft 365 de noms de groupes
ms.reviewer: arvaradh
f1.keywords: NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- m365solution-collabgovernance
search.appverid:
- MET150
ms.assetid: 6ceca4d3-cad1-4532-9f0f-d469dfbbb552
recommendations: false
description: Découvrez comment créer une stratégie d’attribution de noms pour Microsoft 365 groupes.
ms.openlocfilehash: 5ab5f252e2b81470413b4efea17b131613aabc18
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52538170"
---
# <a name="microsoft-365-groups-naming-policy"></a><span data-ttu-id="c981d-103">Microsoft 365 de noms de groupes</span><span class="sxs-lookup"><span data-stu-id="c981d-103">Microsoft 365 groups naming policy</span></span>

<span data-ttu-id="c981d-104">Vous pouvez utiliser une stratégie de noms de groupes pour appliquer une stratégie d’attribution de noms cohérente pour les groupes créés par les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c981d-104">You can use a group naming policy to enforce a consistent naming strategy for groups created by users in your organization.</span></span> <span data-ttu-id="c981d-105">Une stratégie d’attribution de noms peut vous aider, ainsi que vos utilisateurs, à identifier la fonction du groupe, l’appartenance, la région géographique ou la personne qui a créé le groupe.</span><span class="sxs-lookup"><span data-stu-id="c981d-105">A naming policy can help you and your users identify the function of the group, membership, geographic region, or who created the group.</span></span> <span data-ttu-id="c981d-106">La stratégie d’attribution de noms peut également aider à classer les groupes dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="c981d-106">The naming policy can also help categorize groups in the address book.</span></span> <span data-ttu-id="c981d-107">Vous pouvez utiliser la stratégie pour empêcher l’utilisation de mots spécifiques dans les noms de groupe et les alias.</span><span class="sxs-lookup"><span data-stu-id="c981d-107">You can use the policy to block specific words from being used in group names and aliases.</span></span>

<span data-ttu-id="c981d-108">La stratégie d’attribution de noms s’applique aux groupes créés dans toutes les charges de travail de groupes (par exemple, Outlook, Microsoft Teams, SharePoint, Planificateur, Yammer, etc.).</span><span class="sxs-lookup"><span data-stu-id="c981d-108">The naming policy is applied to groups that are created across all groups workloads (like Outlook, Microsoft Teams, SharePoint, Planner, Yammer, etc.).</span></span> <span data-ttu-id="c981d-109">Elle est appliquée à la fois au nom de groupe et à l’alias de groupe.</span><span class="sxs-lookup"><span data-stu-id="c981d-109">It gets applied to both the group name and group alias.</span></span> <span data-ttu-id="c981d-110">Elle est également appliquée lorsqu’un utilisateur crée un groupe et lorsque le nom du groupe, l’alias, la description ou l’avatar est modifié pour un groupe existant.</span><span class="sxs-lookup"><span data-stu-id="c981d-110">It also gets applied when a user creates a group and when the group name, alias, description, or avatar is edited for an existing group.</span></span>

> [!TIP]
> <span data-ttu-id="c981d-111">Une stratégie Microsoft 365 noms de groupes s’applique uniquement Microsoft 365 groupes.</span><span class="sxs-lookup"><span data-stu-id="c981d-111">A Microsoft 365 group naming policy only applies to Microsoft 365 groups.</span></span> <span data-ttu-id="c981d-112">Elle ne s’applique pas aux groupes de distribution créés dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c981d-112">It doesn't apply to distribution groups created in Exchange Online.</span></span> <span data-ttu-id="c981d-113">Pour créer une stratégie d’attribution de noms pour les groupes de distribution, voir Créer une stratégie de noms de groupes [de distribution.](/exchange/recipients-in-exchange-online/manage-distribution-groups/create-group-naming-policy)</span><span class="sxs-lookup"><span data-stu-id="c981d-113">To create a naming policy for distribution groups, see [Create a distribution group naming policy](/exchange/recipients-in-exchange-online/manage-distribution-groups/create-group-naming-policy).</span></span>

<span data-ttu-id="c981d-114">La stratégie de noms de groupes comprend les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="c981d-114">The group naming policy consists of the following features:</span></span>

- <span data-ttu-id="c981d-115">Stratégie de noms de **préfixe-suffixe**: vous pouvez utiliser des préfixes ou des suffixes pour définir la convention d’attribution de noms des groupes (par exemple : « US \_ My Group \_ Engineering »).</span><span class="sxs-lookup"><span data-stu-id="c981d-115">**Prefix-Suffix naming policy**: You can use prefixes or suffixes to define the naming convention of groups (for example: "US\_My Group\_Engineering").</span></span> <span data-ttu-id="c981d-116">Les préfixes/suffixes peuvent être des chaînes fixes ou des attributs utilisateur tels que [Service] qui seront remplacés en fonction de l’utilisateur qui crée le groupe.</span><span class="sxs-lookup"><span data-stu-id="c981d-116">The prefixes/suffixes can either be fixed strings or user attributes like [Department] that will get substituted based on the user who is creating the group.</span></span>

- <span data-ttu-id="c981d-117">**Mots bloqués personnalisés**: vous pouvez télécharger un ensemble de mots bloqués spécifiques à votre organisation qui seraient bloqués dans les groupes créés par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c981d-117">**Custom Blocked Words**: You can upload a set of blocked words specific to your organization that would be blocked in groups created by users.</span></span> <span data-ttu-id="c981d-118">(Par exemple : « PDG, Paie, RH »).</span><span class="sxs-lookup"><span data-stu-id="c981d-118">(For example: "CEO, Payroll, HR").</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="c981d-119">Conditions d'octroi de licence</span><span class="sxs-lookup"><span data-stu-id="c981d-119">Licensing requirements</span></span>

<span data-ttu-id="c981d-120">L’utilisation d’une stratégie de noms Azure AD pour les groupes Microsoft 365 nécessite que vous possédiez, mais pas nécessairement attribuer une licence Azure Active Directory Premium P1 ou azure AD Basic EDU pour chaque utilisateur unique (y compris les invités) membre d’un ou de plusieurs groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c981d-120">Using Azure AD naming policy for Microsoft 365 Groups requires that you possess but not necessarily assign an Azure Active Directory Premium P1 license or Azure AD Basic EDU license for each unique user (including guests) that is a member of one or more Microsoft 365 groups.</span></span>

<span data-ttu-id="c981d-121">Cela est également requis pour l’administrateur qui crée la stratégie de noms de groupes.</span><span class="sxs-lookup"><span data-stu-id="c981d-121">This is also required for the administrator that creates the groups naming policy.</span></span>

## <a name="prefix-suffix-naming-policy"></a><span data-ttu-id="c981d-122">Prefix-Suffix d’attribution de noms</span><span class="sxs-lookup"><span data-stu-id="c981d-122">Prefix-Suffix naming policy</span></span>

<span data-ttu-id="c981d-123">Les préfixes et les suffixes peuvent être des chaînes fixes ou des attributs utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c981d-123">Prefixes and suffixes can either be fixed strings or user attributes.</span></span>

### <a name="fixed-strings"></a><span data-ttu-id="c981d-124">Chaînes fixes</span><span class="sxs-lookup"><span data-stu-id="c981d-124">Fixed strings</span></span>

<span data-ttu-id="c981d-125">Vous pouvez utiliser des chaînes courtes qui peuvent vous aider à différencier les groupes dans la liste d’erreurs d’erreur et la navigation gauche des charges de travail de groupe.</span><span class="sxs-lookup"><span data-stu-id="c981d-125">You can use short strings that can help you differentiate groups in the GAL and left navigation of the group workloads.</span></span> <span data-ttu-id="c981d-126">Certains des suffixes de préfixe courants sont des mots clés tels que « Grp Name » (nom grp), « Name » \_ (nom), « Name » \# \_ (nom)</span><span class="sxs-lookup"><span data-stu-id="c981d-126">Some of the common prefixes suffixes are keywords like 'Grp\_Name' , '\#Name', '\_Name'</span></span>

### <a name="attributes"></a><span data-ttu-id="c981d-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="c981d-127">Attributes</span></span>

<span data-ttu-id="c981d-128">Vous pouvez utiliser des attributs qui peuvent aider à identifier qui a créé le groupe comme [Service] et où il a été créé à partir de [Pays].</span><span class="sxs-lookup"><span data-stu-id="c981d-128">You can use attributes that can help identify who created the group like [Department] and where it was created from like [Country].</span></span>

<span data-ttu-id="c981d-129">Exemples :</span><span class="sxs-lookup"><span data-stu-id="c981d-129">Examples:</span></span>

- <span data-ttu-id="c981d-130">Stratégie = « GRP [GroupName] [Department] »</span><span class="sxs-lookup"><span data-stu-id="c981d-130">Policy = "GRP [GroupName] [Department]"</span></span>
- <span data-ttu-id="c981d-131">Service de l’utilisateur = Ingénierie</span><span class="sxs-lookup"><span data-stu-id="c981d-131">User's department = Engineering</span></span>
- <span data-ttu-id="c981d-132">Nom du groupe créé = « GRP My Group Engineering »</span><span class="sxs-lookup"><span data-stu-id="c981d-132">Created group name = "GRP My Group Engineering"</span></span>

<span data-ttu-id="c981d-133">Les attributs Azure Active Directory (Azure AD) pris en charge sont [Department], [Company], [Office], [StateOrProvince], [CountryOrRegion] et [Title].</span><span class="sxs-lookup"><span data-stu-id="c981d-133">Supported Azure Active Directory (Azure AD) attributes are [Department], [Company], [Office], [StateOrProvince], [CountryOrRegion], and [Title].</span></span>

- <span data-ttu-id="c981d-134">Les attributs utilisateur non pris en compte sont considérés comme des chaînes fixes, par exemple [postalCode].</span><span class="sxs-lookup"><span data-stu-id="c981d-134">Unsupported user attributes are considered as fixed strings, for example [postalCode].</span></span>

- <span data-ttu-id="c981d-135">Les attributs d’extension et les attributs personnalisés ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c981d-135">Extension attributes and custom attributes aren't supported.</span></span>

<span data-ttu-id="c981d-136">Il est recommandé d’utiliser des attributs dont les valeurs sont remplies pour tous les utilisateurs de votre organisation et qui n’utilisent pas d’attributs dont les valeurs sont plus longues.</span><span class="sxs-lookup"><span data-stu-id="c981d-136">It's recommended that you use attributes that have values filled in for all users in your organization and don't use attributes that have longer values.</span></span>

### <a name="things-to-look-out-for"></a><span data-ttu-id="c981d-137">Éléments à rechercher</span><span class="sxs-lookup"><span data-stu-id="c981d-137">Things to look out for</span></span>

- <span data-ttu-id="c981d-138">Lors de la création de la stratégie, le nombre total de préfixes et de suffixes est limité à 53 caractères.</span><span class="sxs-lookup"><span data-stu-id="c981d-138">During policy creation, the total prefixes and suffixes string length is restricted to 53 characters.</span></span>

- <span data-ttu-id="c981d-139">Les préfixes et suffixes peuvent contenir des caractères spéciaux pris en charge dans le nom de groupe et l’alias de groupe.</span><span class="sxs-lookup"><span data-stu-id="c981d-139">Prefixes and suffixes can contain special characters supported in group name and group alias.</span></span> <span data-ttu-id="c981d-140">Lorsque les préfixes et suffixes contiennent des caractères spéciaux qui ne sont pas autorisés dans l’alias de groupe, ils sont appliqués uniquement au nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="c981d-140">When the prefixes and suffixes contain special characters that are not allowed in the group alias, they are only applied to the group name.</span></span> <span data-ttu-id="c981d-141">Ainsi, dans ce cas, les préfixes et suffixes appliqués au nom de groupe sont différents de ceux appliqués à l’alias de groupe.</span><span class="sxs-lookup"><span data-stu-id="c981d-141">So in this case, the prefixes and suffixes applied to group name would be different from the ones applied to the group alias.</span></span>

  > [!NOTE]
  > <span data-ttu-id="c981d-142">Un point (.) ou un trait d’union (-) est autorisé n’importe où dans le nom du groupe, sauf au début ou à la fin du nom.</span><span class="sxs-lookup"><span data-stu-id="c981d-142">A period (.) or a hyphen (-) is permitted anywhere in the group name, except at the beginning or end of the name.</span></span> <span data-ttu-id="c981d-143">Un trait de soulignement (_) est autorisé n’importe où dans le nom du groupe, y compris au début ou à la fin du nom.</span><span class="sxs-lookup"><span data-stu-id="c981d-143">An underscore (_) is permitted anywhere in the group name, including at the beginning or end of the name.</span></span>

- <span data-ttu-id="c981d-144">Si vous utilisez des Yammer Office 365 connectés, évitez d’utiliser les caractères suivants dans votre stratégie d’attribution de noms : @, \# , \[ , , \] \<, and \> .</span><span class="sxs-lookup"><span data-stu-id="c981d-144">If you are using Yammer Office 365 connected groups, avoid using the following characters in your naming policy: @, \#, \[, \], \<, and \>.</span></span> <span data-ttu-id="c981d-145">Si ces caractères sont dans la stratégie d’attribution de noms, les Yammer utilisateurs ne pourront pas créer de groupes.</span><span class="sxs-lookup"><span data-stu-id="c981d-145">If these characters are in the naming policy, regular Yammer users will not be able to create groups.</span></span>

> [!Tip]
> - <span data-ttu-id="c981d-146">Utilisez des chaînes courtes comme suffixe.</span><span class="sxs-lookup"><span data-stu-id="c981d-146">Use short strings as suffix.</span></span>
> - <span data-ttu-id="c981d-147">Utilisez des attributs avec des valeurs.</span><span class="sxs-lookup"><span data-stu-id="c981d-147">Use attributes with values.</span></span>
> - <span data-ttu-id="c981d-148">Ne soyez pas trop créatif, la longueur totale du nom est de 264 caractères au maximum.</span><span class="sxs-lookup"><span data-stu-id="c981d-148">Don't be too creative, total name length has a maximum of 264 characters.</span></span>
> - <span data-ttu-id="c981d-149">Télécharger mots bloqués spécifiques à votre organisation pour restreindre l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c981d-149">Upload your organization specific blocked words to restrict usage.</span></span>

## <a name="custom-blocked-words"></a><span data-ttu-id="c981d-150">Mots bloqués personnalisés</span><span class="sxs-lookup"><span data-stu-id="c981d-150">Custom blocked words</span></span>

<span data-ttu-id="c981d-151">Vous pouvez entrer une liste séparée par des virgules de mots bloqués qui seront bloqués dans les noms de groupe et les alias.</span><span class="sxs-lookup"><span data-stu-id="c981d-151">You can enter a comma separated list of blocked words that will be blocked in group names and aliases.</span></span>

<span data-ttu-id="c981d-152">Aucune recherche de sous-chaîne n’est effectuée ; plus précisément, une correspondance exacte entre le nom entré par l’utilisateur et les mots bloqués personnalisés est nécessaire pour déclencher un échec.</span><span class="sxs-lookup"><span data-stu-id="c981d-152">No sub-string searches are carried out; specifically, an exact match between the user entered name and the custom blocked words is required to trigger a failure.</span></span>

<span data-ttu-id="c981d-153">**Éléments à rechercher**:</span><span class="sxs-lookup"><span data-stu-id="c981d-153">**Things to look out for**:</span></span>

- <span data-ttu-id="c981d-154">Les mots bloqués ne sont pas sensibles à la cas.</span><span class="sxs-lookup"><span data-stu-id="c981d-154">The blocked words are case-insensitive.</span></span>

- <span data-ttu-id="c981d-155">Lorsqu’un utilisateur entre un mot bloqué, le client de groupe affiche un message d’erreur avec le mot bloqué.</span><span class="sxs-lookup"><span data-stu-id="c981d-155">When a user enters a blocked word, the group client will show an error message with the blocked word.</span></span>

- <span data-ttu-id="c981d-156">Il n’existe aucune restriction de caractère dans les mots bloqués utilisés.</span><span class="sxs-lookup"><span data-stu-id="c981d-156">There are no character restrictions in the blocked words used.</span></span>

- <span data-ttu-id="c981d-157">Il existe une limite de 5 000 mots qui peuvent être définies comme mots bloqués.</span><span class="sxs-lookup"><span data-stu-id="c981d-157">There is a limit of 5000 words that can be set as blocked words.</span></span>

## <a name="admin-override"></a><span data-ttu-id="c981d-158">Remplacement par l’administrateur</span><span class="sxs-lookup"><span data-stu-id="c981d-158">Admin override</span></span>

<span data-ttu-id="c981d-159">Certains administrateurs sont exemptés de ces stratégies, sur toutes les charges de travail de groupe et points de terminaison, afin qu’ils peuvent créer des groupes avec ces mots bloqués et avec leurs conventions d’attribution de noms souhaitées.</span><span class="sxs-lookup"><span data-stu-id="c981d-159">Some administrators are exempted from these policies, across all group workloads and endpoints, so that they can create groups with these blocked words and with their desired naming conventions.</span></span> <span data-ttu-id="c981d-160">Voici la liste des rôles d’administrateur exemptés de la stratégie de noms de groupes.</span><span class="sxs-lookup"><span data-stu-id="c981d-160">The following are the list of administrator roles exempted from the group naming policy.</span></span>

- <span data-ttu-id="c981d-161">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="c981d-161">Global admin</span></span>

- <span data-ttu-id="c981d-162">Support partenaire de niveau 1</span><span class="sxs-lookup"><span data-stu-id="c981d-162">Partner Tier 1 Support</span></span>

- <span data-ttu-id="c981d-163">Support partenaire de niveau 2</span><span class="sxs-lookup"><span data-stu-id="c981d-163">Partner Tier 2 Support</span></span>

- <span data-ttu-id="c981d-164">Administrateur de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="c981d-164">User account admin</span></span>

## <a name="how-to-set-up-the-naming-policy"></a><span data-ttu-id="c981d-165">Comment configurer la stratégie d’attribution de noms</span><span class="sxs-lookup"><span data-stu-id="c981d-165">How to set up the naming policy</span></span>

<span data-ttu-id="c981d-166">Pour configurer une stratégie d’attribution de noms :</span><span class="sxs-lookup"><span data-stu-id="c981d-166">To set up a naming policy:</span></span>

1. <span data-ttu-id="c981d-167">Dans [Azure Active Directory](https://aad.portal.azure.com), sous **Gérer,** cliquez sur **Groupes.**</span><span class="sxs-lookup"><span data-stu-id="c981d-167">In [Azure Active Directory](https://aad.portal.azure.com), under **Manage**, click **Groups**.</span></span>
2. <span data-ttu-id="c981d-168">Sous **Paramètres**, cliquez sur **Stratégie d’attribution de noms.**</span><span class="sxs-lookup"><span data-stu-id="c981d-168">Under **Settings**, click **Naming policy**.</span></span>
3. <span data-ttu-id="c981d-169">Sélectionnez **l’onglet Stratégie de noms de** groupes.</span><span class="sxs-lookup"><span data-stu-id="c981d-169">Choose the **Group naming policy** tab.</span></span>
4. <span data-ttu-id="c981d-170">Sous **Stratégie actuelle,** choisissez si vous souhaitez exiger un préfixe ou un suffixe ou les deux, puis cochez les cases appropriées.</span><span class="sxs-lookup"><span data-stu-id="c981d-170">Under **Current policy**, choose if you want to require a prefix or suffix or both, and select the appropriate check boxes.</span></span>
5. <span data-ttu-id="c981d-171">Choisissez entre **Attribut et** **Chaîne** pour chaque ligne, puis spécifiez l’attribut ou la chaîne.</span><span class="sxs-lookup"><span data-stu-id="c981d-171">Choose between **Attribute** and **String** for each line and then specify the attribute or string.</span></span>
6. <span data-ttu-id="c981d-172">Lorsque vous avez ajouté les préfixes et les suffixes dont vous avez besoin, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c981d-172">When you have added the prefixes and suffixes that you need, click **Save**.</span></span>

![Capture d’écran des paramètres de stratégie d’attribution de noms de groupes Azure Active Directory](../media/groups-naming-policy-azure.png)

## <a name="related-topics"></a><span data-ttu-id="c981d-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c981d-174">Related topics</span></span>

[<span data-ttu-id="c981d-175">Planification pas à pas de la gouvernance de la collaboration</span><span class="sxs-lookup"><span data-stu-id="c981d-175">Collaboration governance planning step-by-step</span></span>](collaboration-governance-overview.md#collaboration-governance-planning-step-by-step)

[<span data-ttu-id="c981d-176">Créer votre plan de gouvernance de collaboration</span><span class="sxs-lookup"><span data-stu-id="c981d-176">Create your collaboration governance plan</span></span>](collaboration-governance-first.md)

[<span data-ttu-id="c981d-177">Cmdlets Azure Active Directory pour la configuration de paramètres de groupe</span><span class="sxs-lookup"><span data-stu-id="c981d-177">Azure Active Directory cmdlets for configuring group settings</span></span>](/azure/active-directory/enterprise-users/groups-settings-cmdlets)