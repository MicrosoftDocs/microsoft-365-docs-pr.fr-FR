---
title: Balises de mise en quarantaine
ms.author: chrisda
author: chrisda
manager: dansimp
ms.reviewer: ''
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
ROBOTS: NOINDEX
description: Les administrateurs peuvent apprendre à utiliser des balises de mise en quarantaine pour contrôler ce que les utilisateurs peuvent faire pour leurs messages mis en quarantaine.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 207f22c9acaa183e195f5a2ee33be65cdf4991dd
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50289412"
---
# <a name="quarantine-tags"></a><span data-ttu-id="551b5-103">Balises de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="551b5-103">Quarantine tags</span></span>

> [!NOTE]
> <span data-ttu-id="551b5-104">Les fonctionnalités décrites dans cet article sont actuellement en prévisualisation, ne sont pas disponibles pour tout le monde et peuvent faire l’objet de changements.</span><span class="sxs-lookup"><span data-stu-id="551b5-104">The features that are described in this article are currently in Preview, aren't available to everyone, and are subject to change.</span></span>

<span data-ttu-id="551b5-105">Les balises de mise en quarantaine dans Exchange Online Protection (EOP) permettent aux administrateurs de contrôler ce que les utilisateurs peuvent faire pour leurs messages mis en quarantaine en fonction de la façon dont le message est arrivé en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="551b5-105">Quarantine tags in Exchange Online Protection (EOP) allow admins to control what users are able to do to their quarantined messages based on how the message arrived in quarantine.</span></span>

<span data-ttu-id="551b5-106">EOP a traditionnellement autorisé ou empêché certains niveaux d’interactivité pour les messages en quarantaine et dans les notifications de courrier indésirable de [l’utilisateur final.](use-spam-notifications-to-release-and-report-quarantined-messages.md) [](find-and-release-quarantined-messages-as-a-user.md)</span><span class="sxs-lookup"><span data-stu-id="551b5-106">EOP has traditionally allowed or prevented certain levels of interactivity for messages in [quarantine](find-and-release-quarantined-messages-as-a-user.md) and in [end-user spam notifications](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span> <span data-ttu-id="551b5-107">Par exemple, les utilisateurs finaux peuvent afficher et libérer les messages mis en quarantaine par le filtrage anti-courrier indésirable en tant que courrier indésirable ou en bloc, mais ils ne peuvent pas afficher ou libérer les messages mis en quarantaine comme hameçonnage à haut niveau de confiance.</span><span class="sxs-lookup"><span data-stu-id="551b5-107">For example, end-users can view and release messages that were quarantined by anti-spam filtering as spam or bulk, but they can't view or release messages that were quarantined as high confidence phishing.</span></span>

<span data-ttu-id="551b5-108">Pour les fonctionnalités de [protection](#step-2-assign-a-quarantine-tag-to-supported-features)prise en charge, les balises de mise en quarantaine spécifient ce que les utilisateurs sont autorisés à faire dans les messages de notification de courrier indésirable de l’utilisateur final et dans leurs messages mis en quarantaine en quarantaine (messages dont l’utilisateur est un destinataire).</span><span class="sxs-lookup"><span data-stu-id="551b5-108">For [supported protection features](#step-2-assign-a-quarantine-tag-to-supported-features), quarantine tags specify what users are allowed to do in end-user spam notification messages and in their quarantined messages in quarantine (messages where the user is a recipient).</span></span> <span data-ttu-id="551b5-109">Les balises de mise en quarantaine par défaut sont automatiquement attribuées pour appliquer les fonctionnalités historiques pour les utilisateurs finaux sur les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="551b5-109">Default quarantine tags are automatically assigned to enforce the historical capabilities for end-users on quarantined messages.</span></span> <span data-ttu-id="551b5-110">Vous pouvez également créer et affecter des balises de mise en quarantaine personnalisées pour autoriser ou empêcher les utilisateurs finaux d’effectuer des actions spécifiques sur les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="551b5-110">Or, you can create and assign custom quarantine tags to allow or prevent end-users from performing specific actions on quarantined messages.</span></span>

<span data-ttu-id="551b5-111">Les autorisations individuelles sont combinées dans les groupes d’autorisations prédéfiny suivants :</span><span class="sxs-lookup"><span data-stu-id="551b5-111">The individual permissions are combined into the following preset permission groups:</span></span>

- <span data-ttu-id="551b5-112">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="551b5-112">No access</span></span>
- <span data-ttu-id="551b5-113">Accès limité</span><span class="sxs-lookup"><span data-stu-id="551b5-113">Limited access</span></span>
- <span data-ttu-id="551b5-114">Accès total</span><span class="sxs-lookup"><span data-stu-id="551b5-114">Full access</span></span>

<span data-ttu-id="551b5-115">Les autorisations individuelles disponibles et les autorisations incluses ou non dans les groupes d’autorisations prédéfinits sont décrites dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="551b5-115">The available individual permissions and what's included or not included in the preset permission groups are described in the following table:</span></span>

|<span data-ttu-id="551b5-116">Autorisation</span><span class="sxs-lookup"><span data-stu-id="551b5-116">Permission</span></span>|<span data-ttu-id="551b5-117">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="551b5-117">No access</span></span>|<span data-ttu-id="551b5-118">Accès limité</span><span class="sxs-lookup"><span data-stu-id="551b5-118">Limited access</span></span>|<span data-ttu-id="551b5-119">Accès total</span><span class="sxs-lookup"><span data-stu-id="551b5-119">Full access</span></span>|
|---|:---:|:---:|:---:|
|<span data-ttu-id="551b5-120">**Autoriser l’expéditeur** (_PermissionToAllowSender_)</span><span class="sxs-lookup"><span data-stu-id="551b5-120">**Allow sender** (_PermissionToAllowSender_)</span></span>|||![Coche](../../media/checkmark.png)|
|<span data-ttu-id="551b5-122">**Bloquer l’expéditeur** (_PermissionToBlockSender_)</span><span class="sxs-lookup"><span data-stu-id="551b5-122">**Block sender** (_PermissionToBlockSender_)</span></span>||![Coche](../../media/checkmark.png)|![Coche](../../media/checkmark.png)|
|<span data-ttu-id="551b5-125">**Delete** (_PermissionToDelete_)</span><span class="sxs-lookup"><span data-stu-id="551b5-125">**Delete** (_PermissionToDelete_)</span></span>||![Coche](../../media/checkmark.png)|![Coche](../../media/checkmark.png)|
|<span data-ttu-id="551b5-128">**Preview** (_PermissionToPreview_)</span><span class="sxs-lookup"><span data-stu-id="551b5-128">**Preview** (_PermissionToPreview_)</span></span>||![Coche](../../media/checkmark.png)|![Coche](../../media/checkmark.png)|
|<span data-ttu-id="551b5-131">**Autoriser les destinataires à libérer un message de la quarantaine** (_PermissionToRelease_)</span><span class="sxs-lookup"><span data-stu-id="551b5-131">**Allow recipients to release a message from quarantine** (_PermissionToRelease_)</span></span>|||![Coche](../../media/checkmark.png)|
|<span data-ttu-id="551b5-133">**Autoriser les destinataires à demander qu’un message** soit libéré de la quarantaine (_PermissionToRequestRelease_)</span><span class="sxs-lookup"><span data-stu-id="551b5-133">**Allow recipients to request a message to be released from quarantine** (_PermissionToRequestRelease_)</span></span>||![Coche](../../media/checkmark.png)||
|

<span data-ttu-id="551b5-135">Si vous n’aimez pas les autorisations par défaut dans les groupes d’autorisations prédéfin produits, vous pouvez utiliser des autorisations personnalisées lorsque vous créez ou modifiez des balises de mise en quarantaine personnalisées.</span><span class="sxs-lookup"><span data-stu-id="551b5-135">If you don't like the default permissions in the preset permission groups, you can use custom permissions when you create or modify custom quarantine tags.</span></span> <span data-ttu-id="551b5-136">Pour plus d’informations sur l’objet de chaque autorisation, consultez la section [Détails](#quarantine-tag-permission-details) de l’autorisation de balise de mise en quarantaine plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="551b5-136">For more information about what each permission does, see the [Quarantine tag permission details](#quarantine-tag-permission-details) section later in this article.</span></span>

<span data-ttu-id="551b5-137">Vous créez et affectez des balises de mise en quarantaine dans le Centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec boîtes aux lettres Exchange Online ; EOP PowerShell autonome dans les organisations EOP sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="551b5-137">You create and assign quarantine tags in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with Exchange Online Mailboxes; standalone EOP PowerShell in EOP organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="551b5-138">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="551b5-138">What do you need to know before you begin?</span></span>

- <span data-ttu-id="551b5-139">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="551b5-139">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="551b5-140">Pour aller directement à la page des **balises de mise** en quarantaine, ouvrez <https://protection.office.com/quarantineTags> .</span><span class="sxs-lookup"><span data-stu-id="551b5-140">To go directly to the **Quarantine tags** page, open <https://protection.office.com/quarantineTags>.</span></span>

- <span data-ttu-id="551b5-141">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="551b5-141">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="551b5-142">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="551b5-142">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="551b5-143">Pour afficher, créer, modifier ou supprimer des balises de  mise  en quarantaine, vous devez être membre des rôles Gestion de l’organisation ou Administrateur de la sécurité dans le Centre de sécurité [& conformité.](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="551b5-143">To view, create, modify, or remove quarantine tags, you need to be a member of the **Organization Management** or **Security Administrator** roles in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="step-1-create-quarantine-tags-in-the-security--compliance-center"></a><span data-ttu-id="551b5-144">Étape 1 : Créer des balises de mise en quarantaine dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="551b5-144">Step 1: Create quarantine tags in the Security & Compliance Center</span></span>

1. <span data-ttu-id="551b5-145">Dans le Centre de sécurité &  conformité, sélectionnez Stratégie de gestion des menaces, puis sélectionnez Les balises \>  de mise **en quarantaine.**</span><span class="sxs-lookup"><span data-stu-id="551b5-145">In the Security & Compliance Center, go to **Threat management** \> **Policy** and then select **Quarantine tags**.</span></span>

2. <span data-ttu-id="551b5-146">Dans la page Mettre en quarantaine **les balises,** **sélectionnez Ajouter une balise personnalisée.**</span><span class="sxs-lookup"><span data-stu-id="551b5-146">On the **Quarantine tags** page, select **Add custom tag**.</span></span>

3. <span data-ttu-id="551b5-147">**L’Assistant Nouvelle balise** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="551b5-147">The **New tag** wizard opens.</span></span> <span data-ttu-id="551b5-148">Dans la page **Nom de la** balise, entrez un nom court mais unique dans le champ Nom de **balise.**</span><span class="sxs-lookup"><span data-stu-id="551b5-148">On the **Tag name** page, enter a brief but unique name in the **Tag name** field.</span></span> <span data-ttu-id="551b5-149">Vous devrez identifier et sélectionner la balise par son nom dans les étapes à venir.</span><span class="sxs-lookup"><span data-stu-id="551b5-149">You'll need to identify and select the tag by name in upcoming steps.</span></span> <span data-ttu-id="551b5-150">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="551b5-150">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="551b5-151">Dans la page **d’accès au message du** destinataire, sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="551b5-151">On the **Recipient message access** page, select one of the following values:</span></span>
   - <span data-ttu-id="551b5-152">**Aucun accès**</span><span class="sxs-lookup"><span data-stu-id="551b5-152">**No access**</span></span>
   - <span data-ttu-id="551b5-153">**Accès limité**</span><span class="sxs-lookup"><span data-stu-id="551b5-153">**Limited access**</span></span>
   - <span data-ttu-id="551b5-154">**Accès total**</span><span class="sxs-lookup"><span data-stu-id="551b5-154">**Full access**</span></span>

   <span data-ttu-id="551b5-155">Les autorisations individuelles incluses dans ces groupes d’autorisations sont décrites plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="551b5-155">The individual permissions that are included in these permission groups are described earlier in this article.</span></span>

   <span data-ttu-id="551b5-156">Pour spécifier des autorisations personnalisées, sélectionnez Définir un accès **spécifique (Avancé)** et configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="551b5-156">To specify custom permissions, select **Set specific access (Advanced)** and configure the following settings:</span></span>

     - <span data-ttu-id="551b5-157">**Sélectionnez la préférence d’action de** publication : sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="551b5-157">**Select release action preference**: Select one of the following values:</span></span>
       - <span data-ttu-id="551b5-158">**Aucune action de publication**: il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="551b5-158">**No release action**: This is the default value.</span></span>
       - <span data-ttu-id="551b5-159">**Autoriser les destinataires à libérer un message de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="551b5-159">**Allow recipients to release a message from quarantine**</span></span>
       - <span data-ttu-id="551b5-160">**Autoriser les destinataires à demander qu’un message soit libéré de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="551b5-160">**Allow recipients to request a message to be released from quarantine**</span></span>

     - <span data-ttu-id="551b5-161">**Sélectionnez des actions supplémentaires que les destinataires peuvent prendre** sur les messages mis en quarantaine : sélectionnez une partie, l’ensemble ou aucune des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="551b5-161">**Select additional actions recipients can take on quarantined messages**: Select some, all, or none of the following values:</span></span>
       - <span data-ttu-id="551b5-162">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="551b5-162">**Delete**</span></span>
       - <span data-ttu-id="551b5-163">**Aperçu**</span><span class="sxs-lookup"><span data-stu-id="551b5-163">**Preview**</span></span>
       - <span data-ttu-id="551b5-164">**Autoriser l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="551b5-164">**Allow sender**</span></span>
       - <span data-ttu-id="551b5-165">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="551b5-165">**Block sender**</span></span>

   <span data-ttu-id="551b5-166">Ces autorisations et leur effet sur les messages mis en quarantaine et les notifications de courrier indésirable à l’utilisateur final sont décrits dans la section Détails des [autorisations](#quarantine-tag-permission-details) de balise de mise en quarantaine plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="551b5-166">These permissions and their effect on quarantined messages and in end-user spam notifications are described in the [Quarantine tag permission details](#quarantine-tag-permission-details) section later in this article.</span></span>

   <span data-ttu-id="551b5-167">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="551b5-167">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="551b5-168">Dans la page **Résumé** qui s’affiche, examinez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="551b5-168">On the **Summary** page that appears, review your settings.</span></span> <span data-ttu-id="551b5-169">Vous pouvez cliquer **sur Modifier** sur chaque paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="551b5-169">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="551b5-170">Lorsque vous avez terminé, cliquez sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="551b5-170">When you're finished, click **Submit**.</span></span>

6. <span data-ttu-id="551b5-171">Cliquez **sur Terminé** sur la page de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="551b5-171">Click **Done** on the confirmation page that appears.</span></span>

<span data-ttu-id="551b5-172">Vous êtes maintenant prêt à affecter la balise de mise en quarantaine à une fonctionnalité de mise en quarantaine, comme décrit dans la section [Étape 2.](#step-2-assign-a-quarantine-tag-to-supported-features)</span><span class="sxs-lookup"><span data-stu-id="551b5-172">Now you are ready to assign the quarantine tag to a quarantine feature as described in the [Step 2](#step-2-assign-a-quarantine-tag-to-supported-features) section.</span></span>

### <a name="create-quarantine-tags-in-powershell"></a><span data-ttu-id="551b5-173">Créer des balises de mise en quarantaine dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="551b5-173">Create quarantine tags in PowerShell</span></span>

<span data-ttu-id="551b5-174">Si vous préférez utiliser PowerShell pour créer des balises de mise en quarantaine, connectez-vous à Exchange Online PowerShell ou Exchange Online Protection PowerShell et utilisez la cmdlet **New-QuarantineTag.**</span><span class="sxs-lookup"><span data-stu-id="551b5-174">If you'd rather use PowerShell to create quarantine tags, connect to Exchange Online PowerShell or Exchange Online Protection PowerShell and use the **New-QuarantineTag** cmdlet.</span></span> <span data-ttu-id="551b5-175">Vous avez le choix entre deux méthodes différentes :</span><span class="sxs-lookup"><span data-stu-id="551b5-175">You have two different methods to choose from:</span></span>

- <span data-ttu-id="551b5-176">Utilisez le _paramètre EndUserQuarantinePermissionsValue._</span><span class="sxs-lookup"><span data-stu-id="551b5-176">Use the _EndUserQuarantinePermissionsValue_ parameter.</span></span>
- <span data-ttu-id="551b5-177">Utilisez le _paramètre EndUserQuarantinePermissions._</span><span class="sxs-lookup"><span data-stu-id="551b5-177">Use the _EndUserQuarantinePermissions_ parameter.</span></span>

<span data-ttu-id="551b5-178">Ces méthodes sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="551b5-178">These methods are described in the following sections.</span></span>

#### <a name="use-the-enduserquarantinepermissionsvalue-parameter"></a><span data-ttu-id="551b5-179">Utiliser le paramètre EndUserQuarantinePermissionsValue</span><span class="sxs-lookup"><span data-stu-id="551b5-179">Use the EndUserQuarantinePermissionsValue parameter</span></span>

<span data-ttu-id="551b5-180">Pour créer une balise de mise en quarantaine à l’aide du paramètre _EndUserQuarantinePermissionsValue,_ utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="551b5-180">To create a quarantine tag using the _EndUserQuarantinePermissionsValue_ parameter, use the following syntax:</span></span>

```powershell
New-QuarantineTag -Name "<UniqueName>" -EndUserQuarantinePermissionsValue <0 to 236>
```

<span data-ttu-id="551b5-181">Le _paramètre EndUserQuarantinePermissionsValue_ utilise une valeur décimale convertie à partir d’une valeur binaire.</span><span class="sxs-lookup"><span data-stu-id="551b5-181">The _EndUserQuarantinePermissionsValue_ parameter uses a decimal value that's converted from a binary value.</span></span> <span data-ttu-id="551b5-182">La valeur binaire correspond aux autorisations de mise en quarantaine de l’utilisateur final disponibles dans un ordre spécifique.</span><span class="sxs-lookup"><span data-stu-id="551b5-182">The binary value corresponds to the available end-user quarantine permissions in a specific order.</span></span> <span data-ttu-id="551b5-183">Pour chaque autorisation, la valeur 1 est égale à True et la valeur 0 à False.</span><span class="sxs-lookup"><span data-stu-id="551b5-183">For each permission, the value 1 equals True and the value 0 equals False.</span></span>

<span data-ttu-id="551b5-184">L’ordre et les valeurs requis pour chaque autorisation individuelle dans les groupes d’autorisations prédéfinits sont décrits dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="551b5-184">The required order and values for each individual permission in preset permission groups are described in the following table:</span></span>

****

|<span data-ttu-id="551b5-185">Autorisation</span><span class="sxs-lookup"><span data-stu-id="551b5-185">Permission</span></span>|<span data-ttu-id="551b5-186">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="551b5-186">No access</span></span>|<span data-ttu-id="551b5-187">Accès limité</span><span class="sxs-lookup"><span data-stu-id="551b5-187">Limited access</span></span>|<span data-ttu-id="551b5-188">Accès total</span><span class="sxs-lookup"><span data-stu-id="551b5-188">Full access</span></span>|
|---|:---:|:---:|:---:|
|<span data-ttu-id="551b5-189">PermissionToAllowSender</span><span class="sxs-lookup"><span data-stu-id="551b5-189">PermissionToAllowSender</span></span>|<span data-ttu-id="551b5-190">0</span><span class="sxs-lookup"><span data-stu-id="551b5-190">0</span></span>|<span data-ttu-id="551b5-191">0</span><span class="sxs-lookup"><span data-stu-id="551b5-191">0</span></span>|<span data-ttu-id="551b5-192">1 </span><span class="sxs-lookup"><span data-stu-id="551b5-192">1</span></span>|
|<span data-ttu-id="551b5-193">PermissionToBlockSender</span><span class="sxs-lookup"><span data-stu-id="551b5-193">PermissionToBlockSender</span></span>|<span data-ttu-id="551b5-194">0</span><span class="sxs-lookup"><span data-stu-id="551b5-194">0</span></span>|<span data-ttu-id="551b5-195">1 </span><span class="sxs-lookup"><span data-stu-id="551b5-195">1</span></span>|<span data-ttu-id="551b5-196">1 </span><span class="sxs-lookup"><span data-stu-id="551b5-196">1</span></span>|
|<span data-ttu-id="551b5-197">PermissionToDelete</span><span class="sxs-lookup"><span data-stu-id="551b5-197">PermissionToDelete</span></span>|<span data-ttu-id="551b5-198">0</span><span class="sxs-lookup"><span data-stu-id="551b5-198">0</span></span>|<span data-ttu-id="551b5-199">1 </span><span class="sxs-lookup"><span data-stu-id="551b5-199">1</span></span>|<span data-ttu-id="551b5-200">1 </span><span class="sxs-lookup"><span data-stu-id="551b5-200">1</span></span>|
|<span data-ttu-id="551b5-201">PermissionToDownload<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="551b5-201">PermissionToDownload<sup>\*</sup></span></span>|<span data-ttu-id="551b5-202">0</span><span class="sxs-lookup"><span data-stu-id="551b5-202">0</span></span>|<span data-ttu-id="551b5-203">0</span><span class="sxs-lookup"><span data-stu-id="551b5-203">0</span></span>|<span data-ttu-id="551b5-204">0</span><span class="sxs-lookup"><span data-stu-id="551b5-204">0</span></span>|
|<span data-ttu-id="551b5-205">PermissionToPreview</span><span class="sxs-lookup"><span data-stu-id="551b5-205">PermissionToPreview</span></span>|<span data-ttu-id="551b5-206">0</span><span class="sxs-lookup"><span data-stu-id="551b5-206">0</span></span>|<span data-ttu-id="551b5-207">1 </span><span class="sxs-lookup"><span data-stu-id="551b5-207">1</span></span>|<span data-ttu-id="551b5-208">1 </span><span class="sxs-lookup"><span data-stu-id="551b5-208">1</span></span>|
|<span data-ttu-id="551b5-209">PermissionToRelease<sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="551b5-209">PermissionToRelease<sup>\*\*</sup></span></span>|<span data-ttu-id="551b5-210">0</span><span class="sxs-lookup"><span data-stu-id="551b5-210">0</span></span>|<span data-ttu-id="551b5-211">0</span><span class="sxs-lookup"><span data-stu-id="551b5-211">0</span></span>|<span data-ttu-id="551b5-212">1 </span><span class="sxs-lookup"><span data-stu-id="551b5-212">1</span></span>|
|<span data-ttu-id="551b5-213">PermissionToRequestRelease<sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="551b5-213">PermissionToRequestRelease<sup>\*\*</sup></span></span>|<span data-ttu-id="551b5-214">0</span><span class="sxs-lookup"><span data-stu-id="551b5-214">0</span></span>|<span data-ttu-id="551b5-215">1 </span><span class="sxs-lookup"><span data-stu-id="551b5-215">1</span></span>|<span data-ttu-id="551b5-216">0</span><span class="sxs-lookup"><span data-stu-id="551b5-216">0</span></span>|
|<span data-ttu-id="551b5-217">PermissionToViewHeader<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="551b5-217">PermissionToViewHeader<sup>\*</sup></span></span>|<span data-ttu-id="551b5-218">0</span><span class="sxs-lookup"><span data-stu-id="551b5-218">0</span></span>|<span data-ttu-id="551b5-219">0</span><span class="sxs-lookup"><span data-stu-id="551b5-219">0</span></span>|<span data-ttu-id="551b5-220">0</span><span class="sxs-lookup"><span data-stu-id="551b5-220">0</span></span>|
|<span data-ttu-id="551b5-221">Valeur binaire</span><span class="sxs-lookup"><span data-stu-id="551b5-221">Binary value</span></span>|<span data-ttu-id="551b5-222">00000000</span><span class="sxs-lookup"><span data-stu-id="551b5-222">00000000</span></span>|<span data-ttu-id="551b5-223">01101010</span><span class="sxs-lookup"><span data-stu-id="551b5-223">01101010</span></span>|<span data-ttu-id="551b5-224">11101100</span><span class="sxs-lookup"><span data-stu-id="551b5-224">11101100</span></span>|
|<span data-ttu-id="551b5-225">Valeur décimale à utiliser</span><span class="sxs-lookup"><span data-stu-id="551b5-225">Decimal value to use</span></span>|<span data-ttu-id="551b5-226">0</span><span class="sxs-lookup"><span data-stu-id="551b5-226">0</span></span>|<span data-ttu-id="551b5-227">106</span><span class="sxs-lookup"><span data-stu-id="551b5-227">106</span></span>|<span data-ttu-id="551b5-228">236</span><span class="sxs-lookup"><span data-stu-id="551b5-228">236</span></span>|

<span data-ttu-id="551b5-229"><sup>\*</sup> Actuellement, cette valeur est toujours 0.</span><span class="sxs-lookup"><span data-stu-id="551b5-229"><sup>\*</sup> Currently, this value is always 0.</span></span> <span data-ttu-id="551b5-230">Pour PermissionToViewHeader, la valeur 0 ne masque pas le bouton Afficher l’en-tête du **message** dans les détails du message mis en quarantaine (le bouton est toujours disponible).</span><span class="sxs-lookup"><span data-stu-id="551b5-230">For PermissionToViewHeader, the value 0 doesn't hide the **View message header** button in the details of the quarantined message (the button is always available).</span></span>

<span data-ttu-id="551b5-231"><sup>\*\*</sup> Ne définissez pas ces deux valeurs sur 1.</span><span class="sxs-lookup"><span data-stu-id="551b5-231"><sup>\*\*</sup> Don't set both of these values to 1.</span></span> <span data-ttu-id="551b5-232">Définissez l’un sur 1 et l’autre sur 0, ou définissez les deux sur 0.</span><span class="sxs-lookup"><span data-stu-id="551b5-232">Set one to 1 and the other to 0, or set both to 0.</span></span>

<span data-ttu-id="551b5-233">Cet exemple crée un nouveau nom de balise de mise en quarantaine NoAccess qui attribue les autorisations d’accès Non, comme décrit dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="551b5-233">This example creates a new quarantine tag name NoAccess that assigns the No access permissions as described in the previous table.</span></span>

```powershell
New-QuarantineTag -Name NoAccess -EndUserQuarantinePermissionsValue 0
```

<span data-ttu-id="551b5-234">Pour les autorisations d’accès limité, utilisez la valeur 106.</span><span class="sxs-lookup"><span data-stu-id="551b5-234">For Limited access permissions, use the value 106.</span></span> <span data-ttu-id="551b5-235">Pour les autorisations d’accès total, utilisez la valeur 236.</span><span class="sxs-lookup"><span data-stu-id="551b5-235">For Full access permissions, use the value 236.</span></span>

<span data-ttu-id="551b5-236">Pour les autorisations personnalisées, utilisez le tableau précédent pour obtenir la valeur binaire qui correspond aux autorisations de votre choix.</span><span class="sxs-lookup"><span data-stu-id="551b5-236">For custom permissions, use the previous table to get the binary value that corresponds to the permissions you want.</span></span> <span data-ttu-id="551b5-237">Convertissez la valeur binaire en valeur décimale et utilisez la valeur décimale pour le paramètre _EndUserQuarantinePermissionsValue._</span><span class="sxs-lookup"><span data-stu-id="551b5-237">Convert the binary value to a decimal value and use the decimal value for the _EndUserQuarantinePermissionsValue_ parameter.</span></span>

<span data-ttu-id="551b5-238">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/new-quarantinetag).</span><span class="sxs-lookup"><span data-stu-id="551b5-238">For detailed syntax and parameter information, see [New-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/new-quarantinetag).</span></span>

#### <a name="use-the-enduserquarantinepermissions-parameter"></a><span data-ttu-id="551b5-239">Utiliser le paramètre EndUserQuarantinePermissions</span><span class="sxs-lookup"><span data-stu-id="551b5-239">Use the EndUserQuarantinePermissions parameter</span></span>

<span data-ttu-id="551b5-240">Pour créer une balise de mise en quarantaine à l’aide du paramètre _EndUserQuarantinePermissionsValue,_ utilisez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="551b5-240">To create a quarantine tag using the _EndUserQuarantinePermissionsValue_ parameter, do the following steps:</span></span>

<span data-ttu-id="551b5-241">A.</span><span class="sxs-lookup"><span data-stu-id="551b5-241">A.</span></span> <span data-ttu-id="551b5-242">Stockez un objet d’autorisations de mise en quarantaine dans une variable à l’aide de la cmdlet **New-QuarantinePermissions.**</span><span class="sxs-lookup"><span data-stu-id="551b5-242">Store a quarantine permissions object in a variable using the **New-QuarantinePermissions** cmdlet.</span></span>

<p>

<span data-ttu-id="551b5-243">B.</span><span class="sxs-lookup"><span data-stu-id="551b5-243">B.</span></span> <span data-ttu-id="551b5-244">Utilisez la variable comme valeur _EndUserQuarantinePermissions_ dans la **commande New-QuarantineTag.**</span><span class="sxs-lookup"><span data-stu-id="551b5-244">Use the variable as the _EndUserQuarantinePermissions_ value in the **New-QuarantineTag** command.</span></span>

##### <a name="step-a-store-a-quarantine-permissions-object-in-a-variable"></a><span data-ttu-id="551b5-245">Étape A : Stocker un objet d’autorisations de mise en quarantaine dans une variable</span><span class="sxs-lookup"><span data-stu-id="551b5-245">Step A: Store a quarantine permissions object in a variable</span></span>

<span data-ttu-id="551b5-246">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="551b5-246">Use the following syntax:</span></span>

```powershell
$<VariableName> = New-QuarantinePermissions [-PermissionToAllowSender <$true | $False>] [-PermissionToBlockSender <$true | $False>] [-PermissionToDelete <$true | $False>] [-PermissionToPreview <$true | $False>] [-PermissionToRelease <$true | $False>] [-PermissionToRequestRelease <$true | $False>]
```

<span data-ttu-id="551b5-247">La valeur par défaut pour tous les paramètres inutilisés est , vous devez donc utiliser uniquement les paramètres où vous souhaitez définir `$false` la valeur sur `$true` .</span><span class="sxs-lookup"><span data-stu-id="551b5-247">The default value for any unused parameters is `$false`, so you only need to use the parameters where you want to set value to `$true`.</span></span>

<span data-ttu-id="551b5-248">Les exemples suivants montrent comment créer des objets d’autorisation qui correspondent aux groupes d’autorisations prédéfinës :</span><span class="sxs-lookup"><span data-stu-id="551b5-248">The following examples show how to create permission objects that correspond to the preset permissions groups:</span></span>

- <span data-ttu-id="551b5-249">**Aucun accès**:</span><span class="sxs-lookup"><span data-stu-id="551b5-249">**No access**:</span></span>

  ```powershell
  $NoAccess = New-QuarantinePermissions
  ```

- <span data-ttu-id="551b5-250">**Accès limité**:</span><span class="sxs-lookup"><span data-stu-id="551b5-250">**Limited access**:</span></span>

  ```powershell
  $LimitedAccess = New-QuarantinePermissions -PermissionToBlockSender $true -PermissionToDelete $true -PermissionToPreview $true -PermissionToRequestRelease $true
  ```

- <span data-ttu-id="551b5-251">**Accès total**:</span><span class="sxs-lookup"><span data-stu-id="551b5-251">**Full access**:</span></span>

  ```powershell
  $FullAccess = New-QuarantinePermissions -PermissionToAllowSender $true -PermissionToBlockSender $true -PermissionToDelete $true -PermissionToPreview $true -PermissionToRelease $true
  ```

<span data-ttu-id="551b5-252">Pour voir les valeurs que vous avez définies, exécutez le nom de la variable en tant que commande (par exemple, exécutez la `$NoAccess` commande).</span><span class="sxs-lookup"><span data-stu-id="551b5-252">To see the values that you've set, run the variable name as a command (for example, run the command `$NoAccess`).</span></span>

<span data-ttu-id="551b5-253">Pour les autorisations personnalisées, ne définissez pas les paramètres _PermissionToRelease_ et _PermissionToRequestRelease_ sur `$true` .</span><span class="sxs-lookup"><span data-stu-id="551b5-253">For custom permissions, don't set both the _PermissionToRelease_ and _PermissionToRequestRelease_ parameters to `$true`.</span></span> <span data-ttu-id="551b5-254">Définissez `$true` l’un sur et laissez l’autre en tant `$false` que , ou laissez les deux comme `$false` .</span><span class="sxs-lookup"><span data-stu-id="551b5-254">Set one to `$true` and leave the other as `$false`, or leave both as `$false`.</span></span>

<span data-ttu-id="551b5-255">Vous pouvez également modifier une variable objet d’autorisations existante après la création mais avant de l’utiliser à l’aide de la cmdlet **Set-QuarantinePermissions.**</span><span class="sxs-lookup"><span data-stu-id="551b5-255">You can also modify an existing permissions object variable after you create but before you use it by using the **Set-QuarantinePermissions** cmdlet.</span></span>

<span data-ttu-id="551b5-256">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-QuarantinePermissions](https://docs.microsoft.com/powershell/module/exchange/new-quarantinepermissions) et [Set-QuarantinePermissions.](https://docs.microsoft.com/powershell/module/exchange/set-quarantinepermissions)</span><span class="sxs-lookup"><span data-stu-id="551b5-256">For detailed syntax and parameter information, see [New-QuarantinePermissions](https://docs.microsoft.com/powershell/module/exchange/new-quarantinepermissions) and [Set-QuarantinePermissions](https://docs.microsoft.com/powershell/module/exchange/set-quarantinepermissions).</span></span>

##### <a name="step-b-use-the-variable-in-the-new-quarantinetag-command"></a><span data-ttu-id="551b5-257">Étape B : Utiliser la variable dans la commande New-QuarantineTag commande</span><span class="sxs-lookup"><span data-stu-id="551b5-257">Step B: Use the variable in the New-QuarantineTag command</span></span>

<span data-ttu-id="551b5-258">Après avoir créé et stocké l’objet Permissions dans une variable, utilisez la variable pour la valeur du paramètre _EndUserQuarantinePermission_ dans la commande **New-QuarantineTag** suivante :</span><span class="sxs-lookup"><span data-stu-id="551b5-258">After you've created and stored the permissions object in a variable, use the variable for the _EndUserQuarantinePermission_ parameter value in the following **New-QuarantineTag** command:</span></span>

```powershell
New-QuarantineTag -Name "<UniqueName>" -EndUserQuarantinePermissions $<VariableName>
```

<span data-ttu-id="551b5-259">Cet exemple crée une balise de mise en quarantaine nommée LimitedAccess à l’aide de l’objet permissions qui a été décrit et créé `$LimitedAccess` à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="551b5-259">This example creates a new quarantine tag named LimitedAccess using the `$LimitedAccess` permissions object that was described and created in the previous step.</span></span>

```powershell
New-QuarantineTag -Name LimitedAccess -EndUserQuarantinePermissions $LimitedAccess
```

<span data-ttu-id="551b5-260">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/new-quarantinetag).</span><span class="sxs-lookup"><span data-stu-id="551b5-260">For detailed syntax and parameter information, see [New-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/new-quarantinetag).</span></span>

## <a name="step-2-assign-a-quarantine-tag-to-supported-features"></a><span data-ttu-id="551b5-261">Étape 2 : Affecter une balise de mise en quarantaine aux fonctionnalités prise en charge</span><span class="sxs-lookup"><span data-stu-id="551b5-261">Step 2: Assign a quarantine tag to supported features</span></span>

<span data-ttu-id="551b5-262">Dans _les fonctionnalités_ de protection prises en charge qui met en quarantaine des messages ou des fichiers (automatiquement ou en tant qu’action configurable), vous pouvez affecter une balise de mise en quarantaine aux actions de mise en quarantaine disponibles.</span><span class="sxs-lookup"><span data-stu-id="551b5-262">In _supported_ protection features that quarantine messages or files (automatically or as a configurable action), you can assign a quarantine tag to the available quarantine actions.</span></span> <span data-ttu-id="551b5-263">Les fonctionnalités qui met en quarantaine les messages et la disponibilité des balises de mise en quarantaine sont décrites dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="551b5-263">Features that quarantine messages and the availability of quarantine tags are described in the following table:</span></span>

****

|<span data-ttu-id="551b5-264">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="551b5-264">Feature</span></span>|<span data-ttu-id="551b5-265">Balises de mise en quarantaine pris en charge ?</span><span class="sxs-lookup"><span data-stu-id="551b5-265">Quarantine tags supported?</span></span>|<span data-ttu-id="551b5-266">Balises de mise en quarantaine par défaut utilisées</span><span class="sxs-lookup"><span data-stu-id="551b5-266">Default quarantine tags used</span></span>|
|---|:---:|---|
|<span data-ttu-id="551b5-267">[Stratégies anti-courrier indésirable](configure-your-spam-filter-policies.md):</span><span class="sxs-lookup"><span data-stu-id="551b5-267">[Anti-spam policies](configure-your-spam-filter-policies.md):</span></span> <ul><li><span data-ttu-id="551b5-268">**Courrier** indésirable (_SpamAction_)</span><span class="sxs-lookup"><span data-stu-id="551b5-268">**Spam** (_SpamAction_)</span></span></li><li><span data-ttu-id="551b5-269">**Courrier indésirable à niveau** de confiance élevé (_HighConfidenceSpamAction_)</span><span class="sxs-lookup"><span data-stu-id="551b5-269">**High confidence spam** (_HighConfidenceSpamAction_)</span></span></li><li><span data-ttu-id="551b5-270">**E-mail de hameçonnage** (_PhishSpamAction_)</span><span class="sxs-lookup"><span data-stu-id="551b5-270">**Phishing email** (_PhishSpamAction_)</span></span></li><li><span data-ttu-id="551b5-271">**E-mail de hameçonnage à haut niveau** de confiance (_HighConfidencePhishAction_)</span><span class="sxs-lookup"><span data-stu-id="551b5-271">**High confidence phishing email** (_HighConfidencePhishAction_)</span></span></li><li><span data-ttu-id="551b5-272">**Courrier électronique en** bloc (_BulkSpamAction_)</span><span class="sxs-lookup"><span data-stu-id="551b5-272">**Bulk email** (_BulkSpamAction_)</span></span></li></ul>|<span data-ttu-id="551b5-273">Oui</span><span class="sxs-lookup"><span data-stu-id="551b5-273">Yes</span></span>|<ul><li><span data-ttu-id="551b5-274">DefaultSpamTag (accès complet)</span><span class="sxs-lookup"><span data-stu-id="551b5-274">DefaultSpamTag (Full access)</span></span></li><li><span data-ttu-id="551b5-275">DefaultHighConfSpamTag (accès complet)</span><span class="sxs-lookup"><span data-stu-id="551b5-275">DefaultHighConfSpamTag (Full access)</span></span></li><li><span data-ttu-id="551b5-276">DefaultPhishTag (accès complet)</span><span class="sxs-lookup"><span data-stu-id="551b5-276">DefaultPhishTag (Full access)</span></span></li><li><span data-ttu-id="551b5-277">DefaultHighConfPhishTag (aucun accès)</span><span class="sxs-lookup"><span data-stu-id="551b5-277">DefaultHighConfPhishTag (No access)</span></span></li><li><span data-ttu-id="551b5-278">DefaultBulkTag (accès complet)</span><span class="sxs-lookup"><span data-stu-id="551b5-278">DefaultBulkTag (Full access)</span></span></li></ul>
|<span data-ttu-id="551b5-279">Stratégies anti-hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="551b5-279">Anti-phishing policies:</span></span> <ul><li><span data-ttu-id="551b5-280">[Protection contre l’usurpation d’identité](set-up-anti-phishing-policies.md#spoof-settings) (_AuthenticationFailAction_)</span><span class="sxs-lookup"><span data-stu-id="551b5-280">[Spoof intelligence protection](set-up-anti-phishing-policies.md#spoof-settings) (_AuthenticationFailAction_)</span></span></li><li><span data-ttu-id="551b5-281">[Protection contre l’emprunt d’identité](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365):<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="551b5-281">[Impersonation protection](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365):<sup>\*</sup></span></span> <ul><li><span data-ttu-id="551b5-282">**Si le courrier électronique est envoyé par un utilisateur dont l’identité** est usurpée (_TargetedUserProtectionAction_)</span><span class="sxs-lookup"><span data-stu-id="551b5-282">**If email is sent by an impersonated user** (_TargetedUserProtectionAction_)</span></span></li><li><span data-ttu-id="551b5-283">**Si le courrier électronique est envoyé par un domaine dont l’identité** est usurpée (_TargetedDomainProtectionAction_)</span><span class="sxs-lookup"><span data-stu-id="551b5-283">**If email is sent by an impersonated domain** (_TargetedDomainProtectionAction_)</span></span></li><li><span data-ttu-id="551b5-284">**Veille sur les boîtes aux lettres** \> **Si le courrier électronique est envoyé par un utilisateur dont l’identité** est usurpée (_MailboxIntelligenceProtectionAction_)</span><span class="sxs-lookup"><span data-stu-id="551b5-284">**Mailbox intelligence** \> **If email is sent by an impersonated user** (_MailboxIntelligenceProtectionAction_)</span></span></li></ul></li></ul></ul>|<span data-ttu-id="551b5-285">Non</span><span class="sxs-lookup"><span data-stu-id="551b5-285">No</span></span>|<span data-ttu-id="551b5-286">s/o</span><span class="sxs-lookup"><span data-stu-id="551b5-286">n/a</span></span>|
|<span data-ttu-id="551b5-287">[Stratégies anti-programme](configure-anti-malware-policies.md)malveillant : tous les messages détectés sont toujours mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="551b5-287">[Anti-malware policies](configure-anti-malware-policies.md): All detected messages are always quarantined.</span></span>|<span data-ttu-id="551b5-288">Non</span><span class="sxs-lookup"><span data-stu-id="551b5-288">No</span></span>|<span data-ttu-id="551b5-289">s/o</span><span class="sxs-lookup"><span data-stu-id="551b5-289">n/a</span></span>|
|[<span data-ttu-id="551b5-290">Pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="551b5-290">Safe Attachments for SharePoint, OneDrive, and Microsoft Teams</span></span>](atp-for-spo-odb-and-teams.md)|<span data-ttu-id="551b5-291">Non</span><span class="sxs-lookup"><span data-stu-id="551b5-291">No</span></span>|<span data-ttu-id="551b5-292">s/o</span><span class="sxs-lookup"><span data-stu-id="551b5-292">n/a</span></span>|
|<span data-ttu-id="551b5-293">[Règles de flux de messagerie](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (également appelées règles de transport) avec l’action : Remettre le **message** en quarantaine hébergé (mise en _quarantaine)._</span><span class="sxs-lookup"><span data-stu-id="551b5-293">[Mail flow rules](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (also known as transport rules) with the action: **Deliver the message to the hosted quarantine** (_Quarantine_).</span></span>|<span data-ttu-id="551b5-294">Non</span><span class="sxs-lookup"><span data-stu-id="551b5-294">No</span></span>|<span data-ttu-id="551b5-295">s/o</span><span class="sxs-lookup"><span data-stu-id="551b5-295">n/a</span></span>|
|

<span data-ttu-id="551b5-296"><sup>\*</sup> Les paramètres de protection contre l’emprunt d’identité sont disponibles uniquement dans les stratégies anti-hameçonnage dans Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="551b5-296"><sup>\*</sup> Impersonation protection settings are available only in anti-phishing policies in Microsoft Defender for Office 365.</span></span>

<span data-ttu-id="551b5-297">Si vous êtes satisfait des autorisations de l’utilisateur final fournies par les balises de mise en quarantaine par défaut, vous n’avez rien à faire.</span><span class="sxs-lookup"><span data-stu-id="551b5-297">If you're happy with the end-user permissions that are provided by the default quarantine tags, you don't need to do anything.</span></span> <span data-ttu-id="551b5-298">Si vous souhaitez personnaliser les fonctionnalités de l’utilisateur final (boutons disponibles) dans les notifications de courrier indésirable de l’utilisateur final ou dans les détails des messages mis en quarantaine, vous pouvez affecter une balise de mise en quarantaine personnalisée.</span><span class="sxs-lookup"><span data-stu-id="551b5-298">If you want to customize the end-user capabilities (available buttons) in end-user spam notifications or in quarantined message details, you can assign a custom quarantine tag.</span></span>

### <a name="assign-quarantine-tags-in-anti-spam-policies-in-the-security--compliance-center"></a><span data-ttu-id="551b5-299">Attribuer des balises de mise en quarantaine dans les stratégies anti-courrier indésirable dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="551b5-299">Assign quarantine tags in anti-spam policies in the Security & Compliance Center</span></span>

<span data-ttu-id="551b5-300">Des instructions complètes pour la création et la modification des stratégies anti-courrier indésirable sont décrites dans Configurer des stratégies [anti-courrier indésirable dans EOP.](configure-your-spam-filter-policies.md)</span><span class="sxs-lookup"><span data-stu-id="551b5-300">Full instructions for creating and modifying anti-spam policies are described in [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

1. <span data-ttu-id="551b5-301">Dans le Centre de sécurité &  conformité, sélectionnez Stratégie de gestion des menaces, puis \>  \> **sélectionnez Anti-courrier indésirable.**</span><span class="sxs-lookup"><span data-stu-id="551b5-301">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> and then select **Anti-spam**.</span></span> <span data-ttu-id="551b5-302">Ou, ouvrez <https://protection.office.com/antispam> .</span><span class="sxs-lookup"><span data-stu-id="551b5-302">Or, open <https://protection.office.com/antispam>.</span></span>

2. <span data-ttu-id="551b5-303">Recherchez et sélectionnez une stratégie anti-courrier indésirable existante à modifier, ou créez une stratégie anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="551b5-303">Find and select an existing anti-spam policy to edit, or create a new anti-spam policy.</span></span>

3. <span data-ttu-id="551b5-304">Dans le volet des détails de la stratégie, développez la section **Courrier indésirable et actions en bloc.**</span><span class="sxs-lookup"><span data-stu-id="551b5-304">In the policy details flyout, expand the **Spam and bulk actions** section.</span></span>

4. <span data-ttu-id="551b5-305">Si vous avez sélectionné le **message** de mise en quarantaine  pour l’action d’un verdict de filtrage du courrier indésirable disponible, la zone de balise Appliquer la stratégie de mise en quarantaine est disponible pour que vous sélectionniez la balise de mise en quarantaine pour ce verdict.</span><span class="sxs-lookup"><span data-stu-id="551b5-305">If you've selected **Quarantine message** for the action of an available spam filtering verdict, the **Apply quarantine policy tag** box is available for you to select the quarantine tag for that verdict.</span></span>

   <span data-ttu-id="551b5-306">**Remarque**: lorsque vous créez une stratégie, une valeur de balise de mise en quarantaine vide pour un verdict de filtrage du courrier indésirable indique que la balise de mise en quarantaine par défaut pour ce verdict est utilisée.</span><span class="sxs-lookup"><span data-stu-id="551b5-306">**Note**: When you create a new policy, a blank quarantine tag value for a spam filtering verdict indicates the default quarantine tag for that verdict is used.</span></span> <span data-ttu-id="551b5-307">Lorsque vous modifiez ultérieurement la stratégie, les valeurs vides sont remplacées par les noms de balise de mise en quarantaine par défaut réels, comme décrit dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="551b5-307">When you later edit the policy, the blank values are replaced by the actual default quarantine tag names as described in the previous table.</span></span>

   ![Sélections de balises de mise en quarantaine dans une stratégie anti-courrier indésirable](../../media/quarantine-tags-in-anti-spam-policies.png)

5. <span data-ttu-id="551b5-309">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="551b5-309">When you're finished, click **Save**.</span></span>

#### <a name="assign-quarantine-tags-in-anti-spam-policies-in-powershell"></a><span data-ttu-id="551b5-310">Attribuer des balises de mise en quarantaine dans les stratégies anti-courrier indésirable dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="551b5-310">Assign quarantine tags in anti-spam policies in PowerShell</span></span>

<span data-ttu-id="551b5-311">Si vous préférez utiliser PowerShell pour affecter des balises de mise en quarantaine dans les stratégies anti-courrier indésirable, connectez-vous à Exchange Online PowerShell ou Exchange Online Protection PowerShell et utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="551b5-311">If you'd rather use PowerShell to assign quarantine tags in anti-spam policies, connect to Exchange Online PowerShell or Exchange Online Protection PowerShell and use the following syntax:</span></span>

```powershell
<New-HostedContentFilterPolicy -Name "<Unique name>" | Set-HostedContentFilterPolicy -Identity "<Policy name>">  [-SpamAction Quarantine] [-SpamQuarantineTag <QuarantineTagName>] [-HighConfidenceSpamAction Quarantine] [-HighConfidenceSpamQuarantineTag <QuarantineTagName>] [-PhishSpamAction Quarantine] [-PhishQuarantineTag <QuarantineTagName>] [-HighConfidencePhishQuarantineTag <QuarantineTagName>] [-BulkSpamAction Quarantine] [-BulkQuarantineTag <QuarantineTagName>] ...
```

<span data-ttu-id="551b5-312">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="551b5-312">**Notes**:</span></span>

- <span data-ttu-id="551b5-313">La valeur par défaut du paramètre _HighConfidencePhishAction_ est Mise en quarantaine. Vous n’avez donc pas besoin de définir l’action de mise en quarantaine pour les détections de hameçonnage à haut niveau de confiance dans les nouvelles stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="551b5-313">The default value for the _HighConfidencePhishAction_ parameter is Quarantine, so you don't need to set the Quarantine action for high confidence phishing detections in new anti-spam policies.</span></span> <span data-ttu-id="551b5-314">Pour tous les autres verdicts de filtrage du courrier indésirable dans les stratégies anti-courrier indésirable nouvelles ou existantes, la balise de mise en quarantaine n’est effective que si la valeur de l’action est Mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="551b5-314">For all other spam filtering verdicts in new or existing anti-spam policies, the quarantine tag is only effective if the action value is Quarantine.</span></span> <span data-ttu-id="551b5-315">Pour voir les valeurs d’action dans les stratégies anti-courrier indésirable existantes, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="551b5-315">To see the action values in existing anti-spam policies, run the following command:</span></span>

  ```powershell
  Get-HostedContentFilterPolicy | Format-Table Name,*SpamAction,HighConfidencePhishAction
  ```

  <span data-ttu-id="551b5-316">Pour plus d’informations sur les valeurs d’action par défaut et les valeurs d’action recommandées pour Standard et Strict, voir paramètres de stratégie [anti-courrier indésirable EOP.](recommended-settings-for-eop-and-office365-atp.md#eop-anti-spam-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="551b5-316">For information about the default action values and the recommended action values for Standard and Strict, see [EOP anti-spam policy settings](recommended-settings-for-eop-and-office365-atp.md#eop-anti-spam-policy-settings).</span></span>

- <span data-ttu-id="551b5-317">Un verdict de filtrage du courrier indésirable sans paramètre de balise de mise en quarantaine correspondant signifie que la balise de mise en quarantaine [par](#step-2-assign-a-quarantine-tag-to-supported-features) défaut pour ce verdict est utilisée.</span><span class="sxs-lookup"><span data-stu-id="551b5-317">A spam filtering verdict without a corresponding quarantine tag parameter means the [default quarantine tag](#step-2-assign-a-quarantine-tag-to-supported-features) for that verdict is used.</span></span>

  <span data-ttu-id="551b5-318">Vous devez uniquement remplacer une balise de mise en quarantaine par défaut par une balise de mise en quarantaine personnalisée si vous souhaitez modifier les fonctionnalités par défaut de l’utilisateur final sur les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="551b5-318">You only need to replace a default quarantine tag with a custom quarantine tag if you want to change the default end-user capabilities on quarantined messages.</span></span>

- <span data-ttu-id="551b5-319">Une nouvelle stratégie anti-courrier indésirable dans PowerShell nécessite une stratégie de filtrage du courrier indésirable (paramètres) à l’aide de la cmdlet **New-HostedContentFilterPolicy** et une nouvelle règle de filtrage du courrier indésirable (filtres de destinataires) à l’aide de la cmdlet **New-HostedContentFilterRule.**</span><span class="sxs-lookup"><span data-stu-id="551b5-319">A new anti-spam policy in PowerShell requires a spam filter policy (settings) using the **New-HostedContentFilterPolicy** cmdlet and a new spam filter rule (recipient filters) using the **New-HostedContentFilterRule** cmdlet.</span></span> <span data-ttu-id="551b5-320">Pour obtenir des instructions, [voir Utiliser PowerShell pour créer des stratégies anti-courrier indésirable.](configure-your-spam-filter-policies.md#use-powershell-to-create-anti-spam-policies)</span><span class="sxs-lookup"><span data-stu-id="551b5-320">For instructions, see [Use PowerShell to create anti-spam policies](configure-your-spam-filter-policies.md#use-powershell-to-create-anti-spam-policies).</span></span>

<span data-ttu-id="551b5-321">Cet exemple crée une stratégie de filtrage du courrier indésirable nommée Research Department avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="551b5-321">This example creates a new spam filter policy named Research Department with the following settings:</span></span>

- <span data-ttu-id="551b5-322">L’action pour tous les verdicts de filtrage du courrier indésirable est définie sur Quarantaine.</span><span class="sxs-lookup"><span data-stu-id="551b5-322">The action for all spam filtering verdicts is set to Quarantine.</span></span>
- <span data-ttu-id="551b5-323">La balise de mise en quarantaine  personnalisée nommée NoAccess qui attribue aucune autorisation  d’accès remplace toutes les balises de mise en quarantaine par défaut qui n’attribuent pas déjà aucune autorisation d’accès par défaut.</span><span class="sxs-lookup"><span data-stu-id="551b5-323">The custom quarantine tag named NoAccess that assigns **No access** permissions replaces any default quarantine tags that don't already assign **No access** permissions by default.</span></span>

```powershell
New-HostedContentFilterPolicy -Name Research Department -SpamAction Quarantine -SpamQuarantineTag NoAccess -HighConfidenceSpamAction Quarantine -HighConfidenceSpamQuarantineTag NoAction -PhishSpamAction Quarantine -PhishQuarantineTag NoAction -BulkSpamAction Quarantine -BulkQuarantineTag NoAccess
```

<span data-ttu-id="551b5-324">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/new-hostedcontentfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="551b5-324">For detailed syntax and parameter information, see [New-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/new-hostedcontentfilterpolicy).</span></span>

<span data-ttu-id="551b5-325">Cet exemple modifie la stratégie de filtrage du courrier indésirable existante nommée Human Resources.</span><span class="sxs-lookup"><span data-stu-id="551b5-325">This example modifies the existing spam filter policy named Human Resources.</span></span> <span data-ttu-id="551b5-326">L’action pour le verdict de mise en quarantaine du courrier indésirable est définie sur Mise en quarantaine et la balise de mise en quarantaine personnalisée nommée NoAccess est affectée.</span><span class="sxs-lookup"><span data-stu-id="551b5-326">The action for the spam quarantine verdict is set to Quarantine, and the custom quarantine tag named NoAccess is assigned.</span></span>

```powershell
Set-HostedContentFilterPolicy -Identity "Human Resources" -SpamAction Quarantine -SpamQuarantineTag NoAccess
```

<span data-ttu-id="551b5-327">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-hostedcontentfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="551b5-327">For detailed syntax and parameter information, see [Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-hostedcontentfilterpolicy).</span></span>

## <a name="configure-global-quarantine-notification-settings-in-the-security--compliance-center"></a><span data-ttu-id="551b5-328">Configurer les paramètres globaux de notification de mise en quarantaine dans le Centre de conformité & sécurité</span><span class="sxs-lookup"><span data-stu-id="551b5-328">Configure global quarantine notification settings in the Security & Compliance Center</span></span>

<span data-ttu-id="551b5-329">Les paramètres globaux des balises de mise en quarantaine vous permettent de personnaliser les notifications de courrier indésirable de l’utilisateur final qui sont envoyées aux destinataires des messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="551b5-329">The global settings for quarantine tags allow you to customize the end-user spam notifications that are sent to recipients of messages that were quarantined.</span></span> <span data-ttu-id="551b5-330">Pour plus d’informations sur ces notifications, voir notifications de courrier indésirable pour [l’utilisateur final.](use-spam-notifications-to-release-and-report-quarantined-messages.md)</span><span class="sxs-lookup"><span data-stu-id="551b5-330">For more information about these notifications, see [End-user spam notifications](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span>

1. <span data-ttu-id="551b5-331">Dans le Centre de sécurité &  conformité, sélectionnez Stratégie de gestion des menaces, puis sélectionnez Les balises \>  de mise **en quarantaine.**</span><span class="sxs-lookup"><span data-stu-id="551b5-331">In the Security & Compliance Center, go to **Threat management** \> **Policy** and then select **Quarantine tags**.</span></span>

2. <span data-ttu-id="551b5-332">Dans la page **Des balises de** mise en quarantaine, sélectionnez **Paramètres globaux.**</span><span class="sxs-lookup"><span data-stu-id="551b5-332">On the **Quarantine tags** page, select **Global settings**.</span></span>

3. <span data-ttu-id="551b5-333">Dans le volant **des paramètres de notification de** mise en quarantaine qui s’ouvre, configurez tout ou partie des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="551b5-333">In the **Quarantine notification settings** flyout that opens, configure some or all of the following settings:</span></span>

   - <span data-ttu-id="551b5-334">**Utilisez le logo de mon** entreprise : sélectionnez cette option pour remplacer le logo Microsoft par défaut qui est utilisé en haut des notifications de courrier indésirable à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="551b5-334">**Use my company logo**: Select this option to replace the default Microsoft logo that's use at the top of end-user spam notifications.</span></span> <span data-ttu-id="551b5-335">Avant de faire cela, vous devez suivre les instructions dans Personnaliser le thème [Microsoft 365](../../admin/setup/customize-your-organization-theme.md) pour que votre organisation télécharge votre logo personnalisé.</span><span class="sxs-lookup"><span data-stu-id="551b5-335">Before you do this, you need to follow the instructions in [Customize the Microsoft 365 theme for your organization](../../admin/setup/customize-your-organization-theme.md) to upload your custom logo.</span></span>

     <span data-ttu-id="551b5-336">La capture d’écran suivante montre un logo personnalisé dans une notification de courrier indésirable à l’utilisateur final :</span><span class="sxs-lookup"><span data-stu-id="551b5-336">The following screenshot shows a custom logo in an end-user spam notification:</span></span>

     ![Logo personnalisé dans une notification de courrier indésirable à l’utilisateur final](../../media/quarantine-tags-esn-customization-logo.png)

   - <span data-ttu-id="551b5-338">**Choisir la langue**: les notifications de courrier indésirable de l’utilisateur final sont déjà localisées en fonction des paramètres de langue du destinataire.</span><span class="sxs-lookup"><span data-stu-id="551b5-338">**Choose language**: End-user spam notifications are already localized based on the recipient's language settings.</span></span> <span data-ttu-id="551b5-339">Vous pouvez spécifier du texte personnalisé dans différentes langues pour le nom **d’affichage** et les valeurs **d’exclusion** de responsabilité.</span><span class="sxs-lookup"><span data-stu-id="551b5-339">You can specify customized text in different languages for the **Display name** and **Disclaimer** values.</span></span>

     <span data-ttu-id="551b5-340">Sélectionnez au moins une langue dans la première langue, puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="551b5-340">Select at least one language from the first language box and then click **Add**.</span></span> <span data-ttu-id="551b5-341">Vous pouvez sélectionner plusieurs langues en cliquant sur **Ajouter** après chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="551b5-341">You can select multiple languages by clicking **Add** after each one.</span></span> <span data-ttu-id="551b5-342">Une zone de langue de section affiche toutes les langues que vous avez sélectionnées :</span><span class="sxs-lookup"><span data-stu-id="551b5-342">A section language box shows all of the languages that you've selected:</span></span>

     ![Langues sélectionnées dans la deuxième langue dans les paramètres globaux de notification de mise en quarantaine des balises de mise en quarantaine](../../media/quarantine-tags-esn-customization-selected-languages.png)

   - <span data-ttu-id="551b5-344">**Nom complet**: personnalisez le nom complet de l’expéditeur utilisé dans les notifications de courrier indésirable à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="551b5-344">**Display name**: Customize the sender's display name that's used in end-user spam notifications.</span></span>

     <span data-ttu-id="551b5-345">Pour chaque langue que vous avez ajoutée, sélectionnez la langue dans la deuxième langue (ne cliquez pas  sur le X) et entrez la valeur de texte de votre choix dans la zone Nom complet.</span><span class="sxs-lookup"><span data-stu-id="551b5-345">For each language that you've added, select the language in the second language box (don't click on the X) and enter the text value you want in the **Display name** box.</span></span>

     <span data-ttu-id="551b5-346">La capture d’écran suivante montre le nom complet personnalisé dans une notification de courrier indésirable à l’utilisateur final :</span><span class="sxs-lookup"><span data-stu-id="551b5-346">The following screenshot shows the customized display name in an end-user spam notification:</span></span>

     ![Nom d’affichage de l’expéditeur personnalisé dans une notification de courrier indésirable à l’utilisateur final](../../media/quarantine-tags-esn-customization-display-name.png)

   - <span data-ttu-id="551b5-348">**Clause d’exclusion de** responsabilité : ajoutez une clause d’exclusion de responsabilité personnalisée au bas des notifications de courrier indésirable à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="551b5-348">**Disclaimer**: Add a custom disclaimer to the bottom of end-user spam notifications.</span></span> <span data-ttu-id="551b5-349">Le texte localisé, **une clause d’exclusion** de responsabilité de votre organisation, est toujours inclus en premier, suivi du texte que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="551b5-349">The localized text, **A disclaimer from your organization:** is always included first, followed by the text you specify.</span></span>

     <span data-ttu-id="551b5-350">Pour chaque langue que vous avez ajoutée, sélectionnez la langue dans la deuxième langue (ne cliquez pas sur le X) et entrez la valeur de texte de votre choix dans la zone Exclusion de **responsabilité.**</span><span class="sxs-lookup"><span data-stu-id="551b5-350">For each language that you've added, select the language in the second language box  (don't click the X) and enter the text value you want in the **Disclaimer** box.</span></span>

     <span data-ttu-id="551b5-351">La capture d’écran suivante montre la clause d’exclusion de responsabilité personnalisée dans une notification de courrier indésirable à l’utilisateur final :</span><span class="sxs-lookup"><span data-stu-id="551b5-351">The following screenshot shows the customized disclaimer in an end-user spam notification:</span></span>

     ![Une clause d’exclusion de responsabilité personnalisée au bas d’une notification de courrier indésirable à l’utilisateur final](../../media/quarantine-tags-esn-customization-disclaimer.png)

## <a name="view-quarantine-tags-in-the-security--compliance-center"></a><span data-ttu-id="551b5-353">Afficher les balises de mise en quarantaine dans le Centre de conformité & sécurité</span><span class="sxs-lookup"><span data-stu-id="551b5-353">View quarantine tags in the Security & Compliance Center</span></span>

1. <span data-ttu-id="551b5-354">Dans le Centre de sécurité &  conformité, sélectionnez Stratégie de gestion des menaces, puis sélectionnez Les balises \>  de mise **en quarantaine.**</span><span class="sxs-lookup"><span data-stu-id="551b5-354">In the Security & Compliance Center, go to **Threat management** \> **Policy** and then select **Quarantine tags**.</span></span>

- <span data-ttu-id="551b5-355">Pour afficher les paramètres des balises de mise en quarantaine intégrées ou personnalisées, sélectionnez la balise de mise en quarantaine dans la liste (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="551b5-355">To view the settings of built-in or custom quarantine tags, select the quarantine tag from the list (don't select the check box).</span></span>

- <span data-ttu-id="551b5-356">Pour afficher les paramètres globaux, sélectionnez **Paramètres globaux**</span><span class="sxs-lookup"><span data-stu-id="551b5-356">To view the global settings, select **Global settings**</span></span>

### <a name="view-quarantine-tags-in-powershell"></a><span data-ttu-id="551b5-357">Afficher les balises de mise en quarantaine dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="551b5-357">View quarantine tags in PowerShell</span></span>

<span data-ttu-id="551b5-358">Si vous préférez utiliser PowerShell pour afficher les balises de mise en quarantaine, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="551b5-358">If you'd rather use PowerShell to view quarantine tags, do any of the following steps:</span></span>

- <span data-ttu-id="551b5-359">Pour afficher une liste récapitulatif de toutes les balises intégrées ou personnalisées, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="551b5-359">To view a summary list of all built-in or custom tags, run the following command:</span></span>

  ```powershell
  Get-QuarantineTag | Format-Table Name
  ```

- <span data-ttu-id="551b5-360">Pour afficher les paramètres des balises de mise en quarantaine intégrées ou personnalisées, remplacez-les par le nom de la balise de mise en quarantaine \<TagName\> et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="551b5-360">To view the settings of built-in or custom quarantine tags, replace \<TagName\> with the name of the quarantine tag, and run the following command:</span></span>

  ```powershell
  Get-QuarantineTag -Identity "<TagName>"
  ```

- <span data-ttu-id="551b5-361">Pour afficher les paramètres globaux, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="551b5-361">To view the global settings, run the following command:</span></span>

  ```powershell
  Get-QuarantineTag -QuarantineTagType GlobalQuarantineTag
  ```

<span data-ttu-id="551b5-362">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/get-hostedcontentfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="551b5-362">For detailed syntax and parameter information, see [Get-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/get-hostedcontentfilterpolicy).</span></span>

## <a name="remove-quarantine-tags-in-the-security--compliance-center"></a><span data-ttu-id="551b5-363">Supprimer les balises de mise en quarantaine dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="551b5-363">Remove quarantine tags in the Security & Compliance Center</span></span>

<span data-ttu-id="551b5-364">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="551b5-364">**Notes**:</span></span>

- <span data-ttu-id="551b5-365">Vous ne pouvez pas supprimer les balises de mise en quarantaine intégrées.</span><span class="sxs-lookup"><span data-stu-id="551b5-365">You can't remove built-in quarantine tags.</span></span>

- <span data-ttu-id="551b5-366">Avant de supprimer une balise de mise en quarantaine personnalisée, vérifiez qu’elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="551b5-366">Before you remove a custom quarantine tag, verify that it's not being used.</span></span> <span data-ttu-id="551b5-367">Par exemple, exécutez la commande suivante dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="551b5-367">For example, run the following command in PowerShell:</span></span>

  ```powershell
  Get-HostedContentFilterPolicy | Format-List Name,*QuarantineTag
  ```

  <span data-ttu-id="551b5-368">Si la balise de mise en quarantaine est utilisée, [remplacez la balise de](#step-2-assign-a-quarantine-tag-to-supported-features) mise en quarantaine affectée avant de la supprimer.</span><span class="sxs-lookup"><span data-stu-id="551b5-368">If the quarantine tag is being used, [replace the assigned quarantine tag](#step-2-assign-a-quarantine-tag-to-supported-features) before you remove it.</span></span>

1. <span data-ttu-id="551b5-369">Dans le Centre de sécurité &  conformité, sélectionnez Stratégie de gestion des menaces, puis sélectionnez Les balises \>  de mise **en quarantaine.**</span><span class="sxs-lookup"><span data-stu-id="551b5-369">In the Security & Compliance Center, go to **Threat management** \> **Policy** and then select **Quarantine tags**.</span></span>

2. <span data-ttu-id="551b5-370">Dans la page **Des balises de** mise en quarantaine, sélectionnez la balise de mise en quarantaine personnalisée à supprimer, puis cliquez sur **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="551b5-370">On the **Quarantine tags** page, select the custom quarantine tag that you want to remove, and the click **Delete tag**.</span></span>

3. <span data-ttu-id="551b5-371">Cliquez **sur Supprimer la balise** dans la boîte de dialogue de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="551b5-371">Click **Remove tag** in the confirmation dialog that appears.</span></span>

### <a name="remove-quarantine-tags-in-powershell"></a><span data-ttu-id="551b5-372">Supprimer les balises de mise en quarantaine dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="551b5-372">Remove quarantine tags in PowerShell</span></span>

<span data-ttu-id="551b5-373">Si vous préférez utiliser PowerShell pour supprimer une balise de mise en quarantaine personnalisée, remplacez-la par le nom de la balise de mise en quarantaine \<TagName\> et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="551b5-373">If you'd rather use PowerShell to remove a custom quarantine tag, replace \<TagName\> with the name of the quarantine tag, and run the following command:</span></span>

```powershell
Remove-QuarantineTag -Identity "<TagName>"
```

<span data-ttu-id="551b5-374">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/remove-quarantinetag).</span><span class="sxs-lookup"><span data-stu-id="551b5-374">For detailed syntax and parameter information, see [Remove-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/remove-quarantinetag).</span></span>

## <a name="quarantine-tag-permission-details"></a><span data-ttu-id="551b5-375">Détails de l’autorisation de balise de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="551b5-375">Quarantine tag permission details</span></span>

<span data-ttu-id="551b5-376">Les sections suivantes décrivent les effets des groupes d’autorisations prédéfinés et des autorisations individuelles dans les détails des messages mis en quarantaine et dans les notifications de courrier indésirable à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="551b5-376">The following sections describe the effects of preset permission groups and individual permissions in the details of quarantined messages and in end-user spam notifications.</span></span>

### <a name="preset-permissions-groups"></a><span data-ttu-id="551b5-377">Groupes d’autorisations prédéfins</span><span class="sxs-lookup"><span data-stu-id="551b5-377">Preset permissions groups</span></span>

<span data-ttu-id="551b5-378">Les autorisations individuelles incluses dans les groupes d’autorisations prédéfinés sont répertoriées dans le tableau au début de cet article.</span><span class="sxs-lookup"><span data-stu-id="551b5-378">The individual permissions that are included in preset permission groups are listed in the table at the beginning of this article.</span></span>

#### <a name="no-access"></a><span data-ttu-id="551b5-379">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="551b5-379">No access</span></span>

<span data-ttu-id="551b5-380">Si la balise de mise en quarantaine attribue les **autorisations** Aucun accès (aucune autorisation), les utilisateurs obtiennent toujours certaines fonctionnalités de référence :</span><span class="sxs-lookup"><span data-stu-id="551b5-380">If the quarantine tag assigns the **No access** permissions (no permissions), users still get some baseline capabilities:</span></span>

- <span data-ttu-id="551b5-381">**Détails du message mis en quarantaine**: le bouton Afficher **l’en-tête du message** est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-381">**Quarantined message details**: The **View message header** button is always available.</span></span>

  ![Boutons disponibles dans les détails du message mis en quarantaine si la balise de mise en quarantaine accorde à l’utilisateur des autorisations d’accès illimités](../../media/quarantine-tags-quarantined-message-details-no-access.png)

- <span data-ttu-id="551b5-383">**Notifications de courrier** indésirable  à l’utilisateur final : le bouton Révision qui met l’utilisateur en quarantaine est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-383">**End-user spam notifications**: The **Review** button that takes the user to the message in quarantine is always available.</span></span>

  ![Boutons disponibles dans la notification de courrier indésirable de l’utilisateur final si la balise de mise en quarantaine donne à l’utilisateur des autorisations d’accès sans accès](../../media/quarantine-tags-esn-no-access.png)

#### <a name="limited-access"></a><span data-ttu-id="551b5-385">Accès limité</span><span class="sxs-lookup"><span data-stu-id="551b5-385">Limited access</span></span>

<span data-ttu-id="551b5-386">Si la balise de mise en quarantaine attribue les **autorisations** d’accès limité, les utilisateurs obtiennent les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="551b5-386">If the quarantine tag assigns the **Limited access** permissions, users get the following capabilities:</span></span>

- <span data-ttu-id="551b5-387">**Détails du message mis en quarantaine**: les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="551b5-387">**Quarantined message details**: The following buttons are available:</span></span>
  - <span data-ttu-id="551b5-388">**Publication de la demande**</span><span class="sxs-lookup"><span data-stu-id="551b5-388">**Request release**</span></span>
  - <span data-ttu-id="551b5-389">**Afficher l’en-tête du message**</span><span class="sxs-lookup"><span data-stu-id="551b5-389">**View message header**</span></span>
  - <span data-ttu-id="551b5-390">**Aperçu du message**</span><span class="sxs-lookup"><span data-stu-id="551b5-390">**Preview message**</span></span>
  - <span data-ttu-id="551b5-391">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="551b5-391">**Block sender**</span></span>
  - <span data-ttu-id="551b5-392">**Supprimer de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="551b5-392">**Remove from quarantine**</span></span>

  ![Boutons disponibles dans les détails du message mis en quarantaine si la balise de mise en quarantaine accorde à l’utilisateur des autorisations d’accès limité](../../media/quarantine-tags-quarantined-message-details-limited-access.png)

- <span data-ttu-id="551b5-394">**Notifications de courrier indésirable pour l’utilisateur final**: les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="551b5-394">**End-user spam notifications**: The following buttons are available:</span></span>
  - <span data-ttu-id="551b5-395">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="551b5-395">**Block sender**</span></span>
  - <span data-ttu-id="551b5-396">**Révision**</span><span class="sxs-lookup"><span data-stu-id="551b5-396">**Review**</span></span>

  ![Boutons disponibles dans la notification de courrier indésirable de l’utilisateur final si la balise de mise en quarantaine accorde à l’utilisateur des autorisations d’accès limité](../../media/quarantine-tags-esn-limited-access.png)

#### <a name="full-access"></a><span data-ttu-id="551b5-398">Accès total</span><span class="sxs-lookup"><span data-stu-id="551b5-398">Full access</span></span>

<span data-ttu-id="551b5-399">Si la balise de mise en quarantaine attribue les **autorisations** d’accès total (toutes les autorisations disponibles), les utilisateurs disposent des fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="551b5-399">If the quarantine tag assigns the **Full access** permissions (all available permissions), users get the following capabilities:</span></span>

- <span data-ttu-id="551b5-400">**Détails du message mis en quarantaine**: les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="551b5-400">**Quarantined message details**: The following buttons are available:</span></span>
  - <span data-ttu-id="551b5-401">**Message de libération**</span><span class="sxs-lookup"><span data-stu-id="551b5-401">**Release message**</span></span>
  - <span data-ttu-id="551b5-402">**Afficher l’en-tête du message**</span><span class="sxs-lookup"><span data-stu-id="551b5-402">**View message header**</span></span>
  - <span data-ttu-id="551b5-403">**Aperçu du message**</span><span class="sxs-lookup"><span data-stu-id="551b5-403">**Preview message**</span></span>
  - <span data-ttu-id="551b5-404">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="551b5-404">**Block sender**</span></span>
  - <span data-ttu-id="551b5-405">**Autoriser l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="551b5-405">**Allow sender**</span></span>
  - <span data-ttu-id="551b5-406">**Supprimer de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="551b5-406">**Remove from quarantine**</span></span>

  ![Boutons disponibles dans les détails du message mis en quarantaine si la balise de mise en quarantaine accorde à l’utilisateur des autorisations d’accès total](../../media/quarantine-tags-quarantined-message-details-full-access.png)

- <span data-ttu-id="551b5-408">**Notifications de courrier indésirable pour l’utilisateur final**: les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="551b5-408">**End-user spam notifications**: The following buttons are available:</span></span>
  - <span data-ttu-id="551b5-409">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="551b5-409">**Block sender**</span></span>
  - <span data-ttu-id="551b5-410">**Version**</span><span class="sxs-lookup"><span data-stu-id="551b5-410">**Release**</span></span>
  - <span data-ttu-id="551b5-411">**Révision**</span><span class="sxs-lookup"><span data-stu-id="551b5-411">**Review**</span></span>

  ![Boutons disponibles dans la notification de courrier indésirable de l’utilisateur final si la balise de mise en quarantaine donne à l’utilisateur des autorisations d’accès total](../../media/quarantine-tags-esn-full-access.png)

### <a name="individual-permissions"></a><span data-ttu-id="551b5-413">Autorisations individuelles</span><span class="sxs-lookup"><span data-stu-id="551b5-413">Individual permissions</span></span>

> [!NOTE]
> <span data-ttu-id="551b5-414">N’oubliez pas que les utilisateurs obtiennent toujours les boutons décrits dans la section [Aucun](#no-access) accès.</span><span class="sxs-lookup"><span data-stu-id="551b5-414">Remember, users always get the buttons described in the [No access](#no-access) section.</span></span> <span data-ttu-id="551b5-415">Ces boutons ne sont pas inclus dans les descriptions des autorisations individuelles.</span><span class="sxs-lookup"><span data-stu-id="551b5-415">These buttons are not included in the individual permission descriptions.</span></span>

#### <a name="allow-sender-permission"></a><span data-ttu-id="551b5-416">Autoriser l’autorisation de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="551b5-416">Allow sender permission</span></span>

<span data-ttu-id="551b5-417">**L’autorisation** Autoriser l’expéditeur (_PermissionToAllowSender_) contrôle l’accès au bouton qui permet aux utilisateurs d’ajouter facilement l’expéditeur du message mis en quarantaine à leur liste des expéditeurs autorisés.</span><span class="sxs-lookup"><span data-stu-id="551b5-417">The **Allow sender** permission (_PermissionToAllowSender_) controls access to the button that allows users to conveniently add the quarantined message sender to their Safe Senders list.</span></span>

- <span data-ttu-id="551b5-418">**Détails du message mis en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="551b5-418">**Quarantined message details**:</span></span>
  - <span data-ttu-id="551b5-419">**Autoriser l’autorisation** de l’expéditeur activée : le bouton Autoriser **l’expéditeur** est disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-419">**Allow sender** permission enabled: The **Allow sender** button is available.</span></span>
  - <span data-ttu-id="551b5-420">**Autoriser l’autorisation** de l’expéditeur désactivée : le bouton Autoriser **l’expéditeur** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-420">**Allow sender** permission disabled: The **Allow sender** button is not available.</span></span>

- <span data-ttu-id="551b5-421">**Notifications de courrier indésirable pour l’utilisateur final**: aucun effet.</span><span class="sxs-lookup"><span data-stu-id="551b5-421">**End-user spam notifications**: No effect.</span></span>

<span data-ttu-id="551b5-422">Pour plus d’informations sur la [](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379666) liste des expéditeurs fiables, voir Empêcher le blocage des expéditeurs fiables et Utiliser [Exchange Online PowerShell](configure-junk-email-settings-on-exo-mailboxes.md#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox)pour configurer la collection de listes fiables sur une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="551b5-422">For more information about the Safe Senders list, see [Prevent trusted senders from being blocked](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379666) and [Use Exchange Online PowerShell to configure the safelist collection on a mailbox](configure-junk-email-settings-on-exo-mailboxes.md#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox).</span></span>

#### <a name="block-sender-permission"></a><span data-ttu-id="551b5-423">Bloquer l’autorisation de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="551b5-423">Block sender permission</span></span>

<span data-ttu-id="551b5-424">**L’autorisation** Bloquer l’expéditeur (_PermissionToBlockSender_) contrôle l’accès au bouton qui permet aux utilisateurs d’ajouter facilement l’expéditeur du message mis en quarantaine à leur liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="551b5-424">The **Block sender** permission (_PermissionToBlockSender_) controls access to the button that allows users to conveniently add the quarantined message sender to their Blocked Senders list.</span></span>

- <span data-ttu-id="551b5-425">**Détails du message mis en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="551b5-425">**Quarantined message details**:</span></span>
  - <span data-ttu-id="551b5-426">**Autorisation bloquer l’expéditeur** activée : le **bouton Bloquer l’expéditeur** est disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-426">**Block sender** permission enabled: The **Block sender** button is available.</span></span>
  - <span data-ttu-id="551b5-427">**Bloquer l’autorisation** de l’expéditeur désactivée : le bouton **Bloquer l’expéditeur** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-427">**Block sender** permission disabled: The **Block sender** button is not available.</span></span>

- <span data-ttu-id="551b5-428">**Notifications de courrier indésirable pour l’utilisateur final**:</span><span class="sxs-lookup"><span data-stu-id="551b5-428">**End-user spam notifications**:</span></span>
  - <span data-ttu-id="551b5-429">**Bloquer l’autorisation** de l’expéditeur désactivée : le bouton **Bloquer l’expéditeur** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-429">**Block sender** permission disabled: The **Block sender** button is not available.</span></span>
  - <span data-ttu-id="551b5-430">**Autorisation bloquer l’expéditeur** activée : le **bouton Bloquer l’expéditeur** est disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-430">**Block sender** permission enabled: The **Block sender** button is available.</span></span>

<span data-ttu-id="551b5-431">Pour plus d’informations sur la liste des expéditeurs bloqués, voir Bloquer les [messages](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379667) d’une personne et utiliser Exchange Online PowerShell pour configurer la collection de listes sécurisées sur [une boîte aux lettres.](configure-junk-email-settings-on-exo-mailboxes.md#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox)</span><span class="sxs-lookup"><span data-stu-id="551b5-431">For more information about the Blocked Senders list, see [Block messages from someone](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379667) and [Use Exchange Online PowerShell to configure the safelist collection on a mailbox](configure-junk-email-settings-on-exo-mailboxes.md#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox).</span></span>

#### <a name="delete-permission"></a><span data-ttu-id="551b5-432">Autorisations de suppression</span><span class="sxs-lookup"><span data-stu-id="551b5-432">Delete permission</span></span>

<span data-ttu-id="551b5-433">**L’autorisation** Supprimer (_PermissionToDelete_) contrôle la possibilité pour les utilisateurs de supprimer leurs messages (messages dont l’utilisateur est un destinataire) de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="551b5-433">The **Delete** permission (_PermissionToDelete_) controls the ability to of users to delete their messages (messages where the user is a recipient) from quarantine.</span></span>

- <span data-ttu-id="551b5-434">**Détails du message mis en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="551b5-434">**Quarantined message details**:</span></span>
  - <span data-ttu-id="551b5-435">**Autorisation de** suppression activée : le bouton **Supprimer de** la quarantaine est disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-435">**Delete** permission enabled: The **Remove from quarantine** button is available.</span></span>
  - <span data-ttu-id="551b5-436">**Autorisation de** suppression désactivée : le bouton **Supprimer de la quarantaine** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-436">**Delete** permission disabled: The **Remove from quarantine** button is not available.</span></span>

- <span data-ttu-id="551b5-437">**Notifications de courrier indésirable pour l’utilisateur final**: aucun effet.</span><span class="sxs-lookup"><span data-stu-id="551b5-437">**End-user spam notifications**: No effect.</span></span>

#### <a name="preview-permission"></a><span data-ttu-id="551b5-438">Autorisation d’aperçu</span><span class="sxs-lookup"><span data-stu-id="551b5-438">Preview permission</span></span>

<span data-ttu-id="551b5-439">**L’autorisation** Aperçu (_PermissionToPreview_) contrôle la possibilité pour les utilisateurs d’afficher un aperçu de leurs messages en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="551b5-439">The **Preview** permission (_PermissionToPreview_) controls the ability to of users to preview their messages in quarantine.</span></span>

- <span data-ttu-id="551b5-440">**Détails du message mis en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="551b5-440">**Quarantined message details**:</span></span>
  - <span data-ttu-id="551b5-441">**Autorisation d’aperçu** activée : le bouton **Aperçu du message** est disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-441">**Preview** permission enabled: The **Preview message** button is available.</span></span>
  - <span data-ttu-id="551b5-442">**Autorisation d’aperçu** désactivée : le bouton **Aperçu du message** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-442">**Preview** permission disabled: The **Preview message** button is not available.</span></span>

- <span data-ttu-id="551b5-443">**Notifications de courrier indésirable pour l’utilisateur final**: aucun effet.</span><span class="sxs-lookup"><span data-stu-id="551b5-443">**End-user spam notifications**: No effect.</span></span>

#### <a name="allow-recipients-to-release-a-message-from-quarantine-permission"></a><span data-ttu-id="551b5-444">Autoriser les destinataires à libérer un message de l’autorisation de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="551b5-444">Allow recipients to release a message from quarantine permission</span></span>

<span data-ttu-id="551b5-445">L’autorisation autoriser les destinataires à libérer un message de l’autorisation de mise en quarantaine (_PermissionToRelease_) contrôle la capacité des **utilisateurs** à libérer leurs messages mis en quarantaine directement et sans l’approbation d’un administrateur.</span><span class="sxs-lookup"><span data-stu-id="551b5-445">The **Allow recipients to release a message from quarantine** permission (_PermissionToRelease_) controls the ability of users to release their quarantined messages directly and without the approval of an admin.</span></span>

- <span data-ttu-id="551b5-446">**Détails du message mis en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="551b5-446">**Quarantined message details**:</span></span>
  - <span data-ttu-id="551b5-447">Autorisation activée : le bouton **Libérer le message** est disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-447">Permission enabled: The **Release message** button is available.</span></span>
  - <span data-ttu-id="551b5-448">Autorisation désactivée : le bouton **Libérer le message** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-448">Permission disabled: The **Release message** button is not available.</span></span>

- <span data-ttu-id="551b5-449">**Notifications de courrier indésirable pour l’utilisateur final**:</span><span class="sxs-lookup"><span data-stu-id="551b5-449">**End-user spam notifications**:</span></span>
  - <span data-ttu-id="551b5-450">Autorisation activée : le bouton **Libérer** est disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-450">Permission enabled: The **Release** button is available.</span></span>
  - <span data-ttu-id="551b5-451">Autorisation désactivée : **le** bouton Libérer n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-451">Permission disabled: The **Release** button is not available.</span></span>

#### <a name="allow-recipients-to-request-a-message-to-be-released-from-quarantine-permission"></a><span data-ttu-id="551b5-452">Autoriser les destinataires à demander la libération d’un message de l’autorisation de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="551b5-452">Allow recipients to request a message to be released from quarantine permission</span></span>

<span data-ttu-id="551b5-453">L’autorisation autoriser les destinataires à demander la libération d’un message de l’autorisation  de mise en quarantaine (_PermissionToRequestRelease_) contrôle la capacité des **utilisateurs** à demander la libération de leurs messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="551b5-453">The **Allow recipients to request a message to be released from quarantine** permission (_PermissionToRequestRelease_) controls the ability of users to _request_ the release of their quarantined messages.</span></span> <span data-ttu-id="551b5-454">Le message n’est publié qu’une fois qu’un administrateur a approuvé la demande.</span><span class="sxs-lookup"><span data-stu-id="551b5-454">The message is only released after an admin approves the request.</span></span>

- <span data-ttu-id="551b5-455">**Détails du message mis en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="551b5-455">**Quarantined message details**:</span></span>
  - <span data-ttu-id="551b5-456">Autorisation activée : le bouton **De publication** de la demande est disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-456">Permission enabled: The **Request release** button is available.</span></span>
  - <span data-ttu-id="551b5-457">Autorisation désactivée : le bouton **De publication** de la demande n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-457">Permission disabled: The **Request release** button is not available.</span></span>

- <span data-ttu-id="551b5-458">**Notifications de courrier indésirable pour l’utilisateur final**: **le** bouton Release n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="551b5-458">**End-user spam notifications**: The **Release** button is not available.</span></span>
