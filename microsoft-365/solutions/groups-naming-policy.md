---
title: Stratégie de noms de groupes Microsoft 365
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
description: Découvrez comment créer une stratégie d’attribution de noms pour les groupes Microsoft 365.
ms.openlocfilehash: 55faf5c61d577b35b34923efc7b65457fe46de29
ms.sourcegitcommit: 9841058fcc95f7c2fed6af92bc3c3686944829b6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/07/2020
ms.locfileid: "48377604"
---
# <a name="microsoft-365-groups-naming-policy"></a><span data-ttu-id="7f106-103">Stratégie de noms de groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7f106-103">Microsoft 365 groups naming policy</span></span>

<span data-ttu-id="7f106-104">Vous pouvez utiliser une stratégie de noms de groupes pour appliquer une stratégie d’attribution de noms cohérente pour les groupes créés par les utilisateurs au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7f106-104">You can use a group naming policy to enforce a consistent naming strategy for groups created by users in your organization.</span></span> <span data-ttu-id="7f106-105">Une stratégie de noms peut vous aider, ainsi que vos utilisateurs, à identifier la fonction du groupe, de l’appartenance, de la région géographique ou de la personne qui a créé le groupe.</span><span class="sxs-lookup"><span data-stu-id="7f106-105">A naming policy can help you and your users identify the function of the group, membership, geographic region, or who created the group.</span></span> <span data-ttu-id="7f106-106">La stratégie d’attribution de noms peut également aider à catégoriser les groupes dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="7f106-106">The naming policy can also help categorize groups in the address book.</span></span> <span data-ttu-id="7f106-107">Vous pouvez utiliser la stratégie pour empêcher l’utilisation de mots spécifiques dans les alias et les noms de groupes.</span><span class="sxs-lookup"><span data-stu-id="7f106-107">You can use the policy to block specific words from being used in group names and aliases.</span></span>

<span data-ttu-id="7f106-108">La stratégie de noms est appliquée aux groupes qui sont créés dans toutes les charges de travail de groupe (comme Outlook, Microsoft Teams, SharePoint, Planner, Yammer, etc.).</span><span class="sxs-lookup"><span data-stu-id="7f106-108">The naming policy is applied to groups that are created across all groups workloads (like Outlook, Microsoft Teams, SharePoint, Planner, Yammer, etc.).</span></span> <span data-ttu-id="7f106-109">Elle est appliquée à la fois au nom de groupe et à l’alias de groupe.</span><span class="sxs-lookup"><span data-stu-id="7f106-109">It gets applied to both the group name and group alias.</span></span> <span data-ttu-id="7f106-110">Elle est appliquée lorsqu’un utilisateur crée un groupe et lorsque le nom ou l’alias du groupe est modifié pour un groupe existant.</span><span class="sxs-lookup"><span data-stu-id="7f106-110">It gets applied when a user creates a group and when group name or alias is edited for an existing group.</span></span>

> [!TIP]
> <span data-ttu-id="7f106-111">Une stratégie de noms de groupes Microsoft 365 s’applique uniquement aux groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7f106-111">A Microsoft 365 group naming policy only applies to Microsoft 365 groups.</span></span> <span data-ttu-id="7f106-112">Elle ne s’applique pas aux groupes de distribution créés dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="7f106-112">It doesn't apply to distribution groups created in Exchange Online.</span></span> <span data-ttu-id="7f106-113">Pour créer une stratégie de noms pour les groupes de distribution, consultez [la rubrique Create a distribution Group Naming Policy](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-distribution-groups/create-group-naming-policy).</span><span class="sxs-lookup"><span data-stu-id="7f106-113">To create a naming policy for distribution groups, see [Create a distribution group naming policy](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-distribution-groups/create-group-naming-policy).</span></span>

<span data-ttu-id="7f106-114">La stratégie de noms de groupes se compose des fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="7f106-114">The group naming policy consists of the following features:</span></span>

- <span data-ttu-id="7f106-115">**Préfixe-suffixe stratégie de noms**: vous pouvez utiliser des préfixes ou des suffixes pour définir la Convention d’affectation de noms des groupes (par exemple : « US \_ My Group \_ Engineering »).</span><span class="sxs-lookup"><span data-stu-id="7f106-115">**Prefix-Suffix naming policy**: You can use prefixes or suffixes to define the naming convention of groups (for example: "US\_My Group\_Engineering").</span></span> <span data-ttu-id="7f106-116">Les préfixes/suffixes peuvent être des chaînes fixes ou des attributs utilisateur comme [service] qui sont remplacés en fonction de l’utilisateur qui crée le groupe.</span><span class="sxs-lookup"><span data-stu-id="7f106-116">The prefixes/suffixes can either be fixed strings or user attributes like [Department] that will get substituted based on the user who is creating the group.</span></span>

- <span data-ttu-id="7f106-117">**Mots bloqués personnalisés**: vous pouvez télécharger un ensemble de mots bloqués spécifiques à votre organisation qui seraient bloqués dans les groupes créés par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7f106-117">**Custom Blocked Words**: You can upload a set of blocked words specific to your organization that would be blocked in groups created by users.</span></span> <span data-ttu-id="7f106-118">(Par exemple : « PDG, paie, RH »).</span><span class="sxs-lookup"><span data-stu-id="7f106-118">(For example: "CEO, Payroll, HR").</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="7f106-119">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="7f106-119">Licensing requirements</span></span>

<span data-ttu-id="7f106-120">L’utilisation de la stratégie d’attribution de noms Azure AD pour les groupes Microsoft 365 nécessite que vous disposiez, mais pas nécessairement d’une licence Azure Active Directory Premium P1 ou d’Azure AD basique EDU pour chaque utilisateur (y compris les invités) qui est membre d’un ou de plusieurs groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7f106-120">Using Azure AD naming policy for Microsoft 365 Groups requires that you possess but not necessarily assign an Azure Active Directory Premium P1 license or Azure AD Basic EDU license for each unique user (including guests) that is a member of one or more Microsoft 365 groups.</span></span>

<span data-ttu-id="7f106-121">Cela est également requis pour l’administrateur qui crée la stratégie de noms de groupes.</span><span class="sxs-lookup"><span data-stu-id="7f106-121">This is also required for the administrator that creates the groups naming policy.</span></span>

## <a name="prefix-suffix-naming-policy"></a><span data-ttu-id="7f106-122">Préfixe-suffixe de nom de suffixe</span><span class="sxs-lookup"><span data-stu-id="7f106-122">Prefix-Suffix naming policy</span></span>

<span data-ttu-id="7f106-123">Les préfixes et suffixes peuvent être des chaînes fixes ou des attributs d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f106-123">Prefixes and suffixes can either be fixed strings or user attributes.</span></span>

### <a name="fixed-strings"></a><span data-ttu-id="7f106-124">Chaînes fixes</span><span class="sxs-lookup"><span data-stu-id="7f106-124">Fixed strings</span></span>

<span data-ttu-id="7f106-125">Vous pouvez utiliser des chaînes courtes qui peuvent vous aider à différencier les groupes dans la liste d’adresses globale et la navigation de gauche des charges de travail de groupe.</span><span class="sxs-lookup"><span data-stu-id="7f106-125">You can use short strings that can help you differentiate groups in the GAL and left navigation of the group workloads.</span></span> <span data-ttu-id="7f106-126">Certains suffixes de préfixe courants sont des mots clés tels que « GRP \_ Name », « \# Name », « \_ Name »</span><span class="sxs-lookup"><span data-stu-id="7f106-126">Some of the common prefixes suffixes are keywords like 'Grp\_Name' , '\#Name', '\_Name'</span></span>

### <a name="attributes"></a><span data-ttu-id="7f106-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="7f106-127">Attributes</span></span>

<span data-ttu-id="7f106-128">Vous pouvez utiliser des attributs qui peuvent aider à identifier qui a créé le groupe, comme [service] et où il a été créé à partir de comme [pays].</span><span class="sxs-lookup"><span data-stu-id="7f106-128">You can use attributes that can help identify who created the group like [Department] and where it was created from like [Country].</span></span>

<span data-ttu-id="7f106-129">Exemples :</span><span class="sxs-lookup"><span data-stu-id="7f106-129">Examples:</span></span>

- <span data-ttu-id="7f106-130">Policy = "GRP [nom_groupe] [service]"</span><span class="sxs-lookup"><span data-stu-id="7f106-130">Policy = "GRP [GroupName] [Department]"</span></span>
- <span data-ttu-id="7f106-131">Service de l’utilisateur = ingénierie</span><span class="sxs-lookup"><span data-stu-id="7f106-131">User's department = Engineering</span></span>
- <span data-ttu-id="7f106-132">Créé le nom du groupe = « GRP My Group Engineering »</span><span class="sxs-lookup"><span data-stu-id="7f106-132">Created group name = "GRP My Group Engineering"</span></span>

<span data-ttu-id="7f106-133">Les attributs Azure Active Directory (Azure AD) pris en charge sont [service], [Company], [Office], [StateOrProvince], [CountryOrRegion] et [title].</span><span class="sxs-lookup"><span data-stu-id="7f106-133">Supported Azure Active Directory (Azure AD) attributes are [Department], [Company], [Office], [StateOrProvince], [CountryOrRegion], and [Title].</span></span>

- <span data-ttu-id="7f106-134">Les attributs utilisateur non pris en charge sont considérés comme des chaînes fixes, par exemple, [CodePostal].</span><span class="sxs-lookup"><span data-stu-id="7f106-134">Unsupported user attributes are considered as fixed strings, for example [postalCode].</span></span>

- <span data-ttu-id="7f106-135">Les attributs d’extension et les attributs personnalisés ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7f106-135">Extension attributes and custom attributes aren't supported.</span></span>

<span data-ttu-id="7f106-136">Il est recommandé d’utiliser des attributs dont les valeurs sont renseignées pour tous les utilisateurs de votre organisation et n’utilisent pas les attributs dont les valeurs sont plus longues.</span><span class="sxs-lookup"><span data-stu-id="7f106-136">It's recommended that you use attributes that have values filled in for all users in your organization and don't use attributes that have longer values.</span></span>

### <a name="things-to-look-out-for"></a><span data-ttu-id="7f106-137">Éléments à rechercher</span><span class="sxs-lookup"><span data-stu-id="7f106-137">Things to look out for</span></span>

- <span data-ttu-id="7f106-138">Pendant la création de la stratégie, la longueur de la chaîne des préfixes et des suffixes est limitée à 53 caractères.</span><span class="sxs-lookup"><span data-stu-id="7f106-138">During policy creation, the total prefixes and suffixes string length is restricted to 53 characters.</span></span>

- <span data-ttu-id="7f106-139">Les préfixes et les suffixes peuvent contenir des caractères spéciaux pris en charge dans le nom du groupe et l’alias de groupe.</span><span class="sxs-lookup"><span data-stu-id="7f106-139">Prefixes and suffixes can contain special characters supported in group name and group alias.</span></span> <span data-ttu-id="7f106-140">Lorsque les préfixes et les suffixes contiennent des caractères spéciaux qui ne sont pas autorisés dans l’alias de groupe, ils ne sont appliqués qu’au nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="7f106-140">When the prefixes and suffixes contain special characters that are not allowed in the group alias, they are only applied to the group name.</span></span> <span data-ttu-id="7f106-141">Dans ce cas, les préfixes et les suffixes appliqués au nom de groupe diffèrent de ceux appliqués à l’alias de groupe.</span><span class="sxs-lookup"><span data-stu-id="7f106-141">So in this case, the prefixes and suffixes applied to group name would be different from the ones applied to the group alias.</span></span>

  > [!NOTE]
  > <span data-ttu-id="7f106-142">Un point (.) ou un tiret (-) est autorisé n’importe où dans le nom du groupe, sauf au début ou à la fin du nom.</span><span class="sxs-lookup"><span data-stu-id="7f106-142">A period (.) or a hyphen (-) is permitted anywhere in the group name, except at the beginning or end of the name.</span></span> <span data-ttu-id="7f106-143">Un trait de soulignement (_) est autorisé n’importe où dans le nom du groupe, y compris au début ou à la fin du nom.</span><span class="sxs-lookup"><span data-stu-id="7f106-143">An underscore (_) is permitted anywhere in the group name, including at the beginning or end of the name.</span></span>

- <span data-ttu-id="7f106-144">Si vous utilisez des groupes liés à Yammer Office 365, évitez d’utiliser les caractères suivants dans votre stratégie de noms : @, \# , \[ , \] , \<, and \> .</span><span class="sxs-lookup"><span data-stu-id="7f106-144">If you are using Yammer Office 365 connected groups, avoid using the following characters in your naming policy: @, \#, \[, \], \<, and \>.</span></span> <span data-ttu-id="7f106-145">Si ces caractères sont dans la stratégie de noms, les utilisateurs de Yammer ordinaires ne pourront pas créer de groupes.</span><span class="sxs-lookup"><span data-stu-id="7f106-145">If these characters are in the naming policy, regular Yammer users will not be able to create groups.</span></span>

> [!Tip]
> - <span data-ttu-id="7f106-146">Utiliser des chaînes courtes comme suffixe.</span><span class="sxs-lookup"><span data-stu-id="7f106-146">Use short strings as suffix.</span></span>
> - <span data-ttu-id="7f106-147">Utilisez des attributs avec des valeurs.</span><span class="sxs-lookup"><span data-stu-id="7f106-147">Use attributes with values.</span></span>
> - <span data-ttu-id="7f106-148">Ne soyez pas trop créatif, la longueur totale du nom est de 264 caractères au maximum.</span><span class="sxs-lookup"><span data-stu-id="7f106-148">Don't be too creative, total name length has a maximum of 264 characters.</span></span>
> - <span data-ttu-id="7f106-149">Charger les mots bloqués spécifiques de votre organisation pour restreindre l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="7f106-149">Upload your organization specific blocked words to restrict usage.</span></span>

## <a name="custom-blocked-words"></a><span data-ttu-id="7f106-150">Mots bloqués personnalisés</span><span class="sxs-lookup"><span data-stu-id="7f106-150">Custom blocked words</span></span>

<span data-ttu-id="7f106-151">Vous pouvez entrer une liste de mots bloqués séparés par des virgules qui seront bloqués dans les noms de groupe et les alias.</span><span class="sxs-lookup"><span data-stu-id="7f106-151">You can enter a comma separated list of blocked words that will be blocked in group names and aliases.</span></span>

<span data-ttu-id="7f106-152">Aucune recherche de sous-chaîne n’est effectuée ; plus précisément, une correspondance exacte entre le nom entré par l’utilisateur et les mots bloqués personnalisés est requise pour déclencher un échec.</span><span class="sxs-lookup"><span data-stu-id="7f106-152">No sub-string searches are carried out; specifically, an exact match between the user entered name and the custom blocked words is required to trigger a failure.</span></span>

<span data-ttu-id="7f106-153">**Éléments à rechercher**:</span><span class="sxs-lookup"><span data-stu-id="7f106-153">**Things to look out for**:</span></span>

- <span data-ttu-id="7f106-154">Les mots bloqués ne sont pas sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="7f106-154">The blocked words are case-insensitive.</span></span>

- <span data-ttu-id="7f106-155">Lorsqu’un utilisateur entre un mot bloqué, le client de groupe affiche un message d’erreur avec le mot bloqué.</span><span class="sxs-lookup"><span data-stu-id="7f106-155">When a user enters a blocked word, the group client will show an error message with the blocked word.</span></span>

- <span data-ttu-id="7f106-156">Il n’existe pas de restrictions de caractères dans les mots bloqués utilisés.</span><span class="sxs-lookup"><span data-stu-id="7f106-156">There are no character restrictions in the blocked words used.</span></span>

- <span data-ttu-id="7f106-157">Il existe une limite de 5000 mots pouvant être définis en tant que mots bloqués.</span><span class="sxs-lookup"><span data-stu-id="7f106-157">There is a limit of 5000 words that can be set as blocked words.</span></span>

## <a name="admin-override"></a><span data-ttu-id="7f106-158">Remplacement par l’administrateur</span><span class="sxs-lookup"><span data-stu-id="7f106-158">Admin override</span></span>

<span data-ttu-id="7f106-159">Certains administrateurs sont exemptés de ces stratégies, pour toutes les charges de travail et les points de terminaison de groupe, afin qu’ils puissent créer des groupes avec ces mots bloqués et avec les conventions d’affectation de noms de votre choix.</span><span class="sxs-lookup"><span data-stu-id="7f106-159">Some administrators are exempted from these policies, across all group workloads and endpoints, so that they can create groups with these blocked words and with their desired naming conventions.</span></span> <span data-ttu-id="7f106-160">Voici la liste des rôles d’administrateur exemptés de la stratégie de noms de groupes.</span><span class="sxs-lookup"><span data-stu-id="7f106-160">The following are the list of administrator roles exempted from the group naming policy.</span></span>

- <span data-ttu-id="7f106-161">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="7f106-161">Global admin</span></span>

- <span data-ttu-id="7f106-162">Prise en charge du niveau 1 du partenaire</span><span class="sxs-lookup"><span data-stu-id="7f106-162">Partner Tier 1 Support</span></span>

- <span data-ttu-id="7f106-163">Prise en charge du niveau 2 du partenaire</span><span class="sxs-lookup"><span data-stu-id="7f106-163">Partner Tier 2 Support</span></span>

- <span data-ttu-id="7f106-164">Administrateur de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="7f106-164">User account admin</span></span>

- <span data-ttu-id="7f106-165">Writers d’annuaire</span><span class="sxs-lookup"><span data-stu-id="7f106-165">Directory writers</span></span>

## <a name="how-to-set-up-the-naming-policy"></a><span data-ttu-id="7f106-166">Procédure de configuration de la stratégie de noms</span><span class="sxs-lookup"><span data-stu-id="7f106-166">How to set up the naming policy</span></span>

<span data-ttu-id="7f106-167">Pour configurer une stratégie d’attribution de noms :</span><span class="sxs-lookup"><span data-stu-id="7f106-167">To set up a naming policy:</span></span>

1. <span data-ttu-id="7f106-168">Dans [Azure Active Directory](https://aad.portal.azure.com), sous **gestion**, cliquez sur **groupes**.</span><span class="sxs-lookup"><span data-stu-id="7f106-168">In [Azure Active Directory](https://aad.portal.azure.com), under **Manage**, click **Groups**.</span></span>
2. <span data-ttu-id="7f106-169">Sous **paramètres**, cliquez sur **stratégie de noms**.</span><span class="sxs-lookup"><span data-stu-id="7f106-169">Under **Settings**, click **Naming policy**.</span></span>
3. <span data-ttu-id="7f106-170">Choisissez l’onglet **stratégie d’attribution de noms de groupes** .</span><span class="sxs-lookup"><span data-stu-id="7f106-170">Choose the **Group naming policy** tab.</span></span>
4. <span data-ttu-id="7f106-171">Sous **stratégie actuelle**, choisissez si vous souhaitez exiger un préfixe ou un suffixe, ou les deux, et activez les cases à cocher appropriées.</span><span class="sxs-lookup"><span data-stu-id="7f106-171">Under **Current policy**, choose if you want to require a prefix or suffix or both, and select the appropriate check boxes.</span></span>
5. <span data-ttu-id="7f106-172">Choisissez entre **attribut** et **chaîne** pour chaque ligne, puis spécifiez l’attribut ou la chaîne.</span><span class="sxs-lookup"><span data-stu-id="7f106-172">Choose between **Attribute** and **String** for each line and then specify the attribute or string.</span></span>
6. <span data-ttu-id="7f106-173">Une fois que vous avez ajouté les préfixes et les suffixes dont vous avez besoin, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7f106-173">When you have added the prefixes and suffixes that you need, click **Save**.</span></span>

![Capture d’écran des paramètres de stratégie d’attribution de noms de groupes dans Azure Active Directory](../media/groups-naming-policy-azure.png)

## <a name="related-topics"></a><span data-ttu-id="7f106-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f106-175">Related topics</span></span>

[<span data-ttu-id="7f106-176">Cmdlets Azure Active Directory pour la configuration de paramètres de groupe</span><span class="sxs-lookup"><span data-stu-id="7f106-176">Azure Active Directory cmdlets for configuring group settings</span></span>](https://go.microsoft.com/fwlink/?linkid=868341)
