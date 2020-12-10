---
title: Balises de mise en quarantaine
ms.author: chrisda
author: chrisda
manager: dansimp
ms.reviewer: ''
ms.date: ''
audience: ITPro
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
ROBOTS: NOINDEX
description: Les administrateurs peuvent apprendre à utiliser les balises de mise en quarantaine pour contrôler ce que les utilisateurs peuvent faire à leurs messages mis en quarantaine.
ms.openlocfilehash: 498a5f45fa62481f7f4f8dfe5ece8a51a038f99a
ms.sourcegitcommit: ee39faf3507d0edc9497117b3b2854955c959c6c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "49616007"
---
# <a name="quarantine-tags"></a><span data-ttu-id="c46df-103">Balises de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="c46df-103">Quarantine tags</span></span>

> [!NOTE]
> <span data-ttu-id="c46df-104">Les fonctionnalités décrites dans cet article sont actuellement en version préliminaire, ne sont pas disponibles pour tous les utilisateurs et peuvent faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="c46df-104">The features that are described in this article are currently in Preview, aren't available to everyone, and are subject to change.</span></span>

<span data-ttu-id="c46df-105">Les balises de mise en quarantaine dans Exchange Online Protection (EOP) permettent aux administrateurs de contrôler ce que les utilisateurs peuvent faire de leurs messages mis en quarantaine en fonction de la mise en quarantaine du message.</span><span class="sxs-lookup"><span data-stu-id="c46df-105">Quarantine tags in Exchange Online Protection (EOP) allow admins to control what users are able to do to their quarantined messages based on how the message arrived in quarantine.</span></span>

<span data-ttu-id="c46df-106">EOP a traditionnellement autorisé ou empêché certains niveaux d’interactivité pour les messages en [quarantaine](find-and-release-quarantined-messages-as-a-user.md) et dans les [notifications de courrier indésirable pour l’utilisateur final](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span><span class="sxs-lookup"><span data-stu-id="c46df-106">EOP has traditionally allowed or prevented certain levels of interactivity for messages in [quarantine](find-and-release-quarantined-messages-as-a-user.md) and in [end-user spam notifications](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span> <span data-ttu-id="c46df-107">Par exemple, les utilisateurs finaux peuvent afficher et libérer les messages qui ont été mis en quarantaine par le filtrage du courrier indésirable en tant que courrier indésirable ou en bloc, mais ils ne peuvent pas afficher ou libérer les messages mis en quarantaine en tant que phishing à haut niveau de fiabilité.</span><span class="sxs-lookup"><span data-stu-id="c46df-107">For example, end-users can view and release messages that were quarantined by anti-spam filtering as spam or bulk, but they can't view or release messages that were quarantined as high confidence phishing.</span></span>

<span data-ttu-id="c46df-108">Pour les [fonctionnalités de protection prises en charge](#step-2-assign-a-quarantine-tag-to-supported-features), les balises de mise en quarantaine spécifient ce que les utilisateurs sont autorisés à faire dans les messages de notification de courrier indésirable de l’utilisateur final et dans les messages mis en quarantaine (messages dans lesquels l’utilisateur est un destinataire).</span><span class="sxs-lookup"><span data-stu-id="c46df-108">For [supported protection features](#step-2-assign-a-quarantine-tag-to-supported-features), quarantine tags specify what users are allowed to do in end-user spam notification messages and in their quarantined messages in quarantine (messages where the user is a recipient).</span></span> <span data-ttu-id="c46df-109">Les balises de mise en quarantaine par défaut sont automatiquement attribuées pour appliquer les fonctionnalités d’historique pour les utilisateurs finaux sur les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c46df-109">Default quarantine tags are automatically assigned to enforce the historical capabilities for end-users on quarantined messages.</span></span> <span data-ttu-id="c46df-110">Vous pouvez créer et affecter des balises de mise en quarantaine personnalisées pour autoriser ou empêcher les utilisateurs finals d’effectuer des actions spécifiques sur les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c46df-110">Or, you can create and assign custom quarantine tags to allow or prevent end-users from performing specific actions on quarantined messages.</span></span>

<span data-ttu-id="c46df-111">Les autorisations individuelles sont combinées dans les groupes d’autorisations prédéfinis suivants :</span><span class="sxs-lookup"><span data-stu-id="c46df-111">The individual permissions are combined into the following preset permission groups:</span></span>

- <span data-ttu-id="c46df-112">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="c46df-112">No access</span></span>
- <span data-ttu-id="c46df-113">Accès limité</span><span class="sxs-lookup"><span data-stu-id="c46df-113">Limited access</span></span>
- <span data-ttu-id="c46df-114">Accès total</span><span class="sxs-lookup"><span data-stu-id="c46df-114">Full access</span></span>

<span data-ttu-id="c46df-115">Les autorisations individuelles disponibles et ce qui est inclus ou non dans les groupes d’autorisations prédéfinis sont décrits dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="c46df-115">The available individual permissions and what's included or not included in the preset permission groups are described in the following table:</span></span>

|<span data-ttu-id="c46df-116">Autorisation</span><span class="sxs-lookup"><span data-stu-id="c46df-116">Permission</span></span>|<span data-ttu-id="c46df-117">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="c46df-117">No access</span></span>|<span data-ttu-id="c46df-118">Accès limité</span><span class="sxs-lookup"><span data-stu-id="c46df-118">Limited access</span></span>|<span data-ttu-id="c46df-119">Accès total</span><span class="sxs-lookup"><span data-stu-id="c46df-119">Full access</span></span>|
|---|:---:|:---:|:---:|
|<span data-ttu-id="c46df-120">**Autoriser l’expéditeur** (_PermissionToAllowSender_)</span><span class="sxs-lookup"><span data-stu-id="c46df-120">**Allow sender** (_PermissionToAllowSender_)</span></span>|||![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="c46df-122">**Bloquer l’expéditeur** (_PermissionToBlockSender_)</span><span class="sxs-lookup"><span data-stu-id="c46df-122">**Block sender** (_PermissionToBlockSender_)</span></span>||![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="c46df-125">**Supprimer** (_PermissionToDelete_)</span><span class="sxs-lookup"><span data-stu-id="c46df-125">**Delete** (_PermissionToDelete_)</span></span>||![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="c46df-128">**Aperçu** (_PermissionToPreview_)</span><span class="sxs-lookup"><span data-stu-id="c46df-128">**Preview** (_PermissionToPreview_)</span></span>||![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="c46df-131">**Autoriser les destinataires à libérer un message en quarantaine** (_PermissionToRelease_)</span><span class="sxs-lookup"><span data-stu-id="c46df-131">**Allow recipients to release a message from quarantine** (_PermissionToRelease_)</span></span>|||![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="c46df-133">**Autoriser les destinataires à demander la libération d’un message en quarantaine** (_PermissionToRequestRelease_)</span><span class="sxs-lookup"><span data-stu-id="c46df-133">**Allow recipients to request a message to be released from quarantine** (_PermissionToRequestRelease_)</span></span>||![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
|

<span data-ttu-id="c46df-135">Si vous n’aimez pas les autorisations par défaut dans les groupes d’autorisations prédéfinis, vous pouvez utiliser des autorisations personnalisées lors de la création ou de la modification de balises de mise en quarantaine personnalisées.</span><span class="sxs-lookup"><span data-stu-id="c46df-135">If you don't like the default permissions in the preset permission groups, you can use custom permissions when you create or modify custom quarantine tags.</span></span> <span data-ttu-id="c46df-136">Pour plus d’informations sur ce que fait chaque autorisation, voir la section Détails de l' [autorisation de mise en quarantaine](#quarantine-tag-permission-details) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="c46df-136">For more information about what each permission does, see the [Quarantine tag permission details](#quarantine-tag-permission-details) section later in this article.</span></span>

<span data-ttu-id="c46df-137">Vous créez et attribuez des balises de mise en quarantaine dans le centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres Exchange Online ; environnement EOP autonome dans les organisations EOP sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="c46df-137">You create and assign quarantine tags in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with Exchange Online Mailboxes; standalone EOP PowerShell in EOP organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="c46df-138">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="c46df-138">What do you need to know before you begin?</span></span>

- <span data-ttu-id="c46df-139">Vous ouvrez le Centre de sécurité et conformité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="c46df-139">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="c46df-140">Pour accéder directement à la page **balises de quarantaine** , ouvrez <https://protection.office.com/quarantineTags> .</span><span class="sxs-lookup"><span data-stu-id="c46df-140">To go directly to the **Quarantine tags** page, open <https://protection.office.com/quarantineTags>.</span></span>

- <span data-ttu-id="c46df-141">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="c46df-141">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="c46df-142">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="c46df-142">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="c46df-143">Pour afficher, créer, modifier ou supprimer des balises de mise en quarantaine, vous devez être membre des rôles de gestion de l' **organisation** ou d' **administrateur de sécurité** dans le centre de [sécurité & conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="c46df-143">To view, create, modify, or remove quarantine tags, you need to be a member of the **Organization Management** or **Security Administrator** roles in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="step-1-create-quarantine-tags-in-the-security--compliance-center"></a><span data-ttu-id="c46df-144">Étape 1 : créer des balises de mise en quarantaine dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="c46df-144">Step 1: Create quarantine tags in the Security & Compliance Center</span></span>

1. <span data-ttu-id="c46df-145">Dans le centre de sécurité & conformité, accédez à stratégie de **gestion des menaces** , \>  puis sélectionnez **balises de mise en quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="c46df-145">In the Security & Compliance Center, go to **Threat management** \> **Policy** and then select **Quarantine tags**.</span></span>

2. <span data-ttu-id="c46df-146">Sur la page **balises de quarantaine** , sélectionnez **Ajouter une balise personnalisée**.</span><span class="sxs-lookup"><span data-stu-id="c46df-146">On the **Quarantine tags** page, select **Add custom tag**.</span></span>

3. <span data-ttu-id="c46df-147">L’Assistant **nouvelle balise** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="c46df-147">The **New tag** wizard opens.</span></span> <span data-ttu-id="c46df-148">Dans la page nom de la **balise** , entrez un bref nom unique dans le champ nom de la **balise** .</span><span class="sxs-lookup"><span data-stu-id="c46df-148">On the **Tag name** page, enter a brief but unique name in the **Tag name** field.</span></span> <span data-ttu-id="c46df-149">Vous devrez identifier et sélectionner la balise par nom dans les étapes à venir.</span><span class="sxs-lookup"><span data-stu-id="c46df-149">You'll need to identify and select the tag by name in upcoming steps.</span></span> <span data-ttu-id="c46df-150">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c46df-150">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="c46df-151">Sur la page **accès aux messages des destinataires** , sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c46df-151">On the **Recipient message access** page, select one of the following values:</span></span>
   - <span data-ttu-id="c46df-152">**Aucun accès**</span><span class="sxs-lookup"><span data-stu-id="c46df-152">**No access**</span></span>
   - <span data-ttu-id="c46df-153">**Accès limité**</span><span class="sxs-lookup"><span data-stu-id="c46df-153">**Limited access**</span></span>
   - <span data-ttu-id="c46df-154">**Accès total**</span><span class="sxs-lookup"><span data-stu-id="c46df-154">**Full access**</span></span>

   <span data-ttu-id="c46df-155">Les autorisations individuelles qui sont incluses dans ces groupes d’autorisations sont décrites plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="c46df-155">The individual permissions that are included in these permission groups are described earlier in this article.</span></span>

   <span data-ttu-id="c46df-156">Pour spécifier des autorisations personnalisées, sélectionnez **définir un accès spécifique (avancé)** et configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="c46df-156">To specify custom permissions, select **Set specific access (Advanced)** and configure the following settings:</span></span>

     - <span data-ttu-id="c46df-157">**Sélectionnez la préférence** de l’action de publication : sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c46df-157">**Select release action preference**: Select one of the following values:</span></span>
       - <span data-ttu-id="c46df-158">**Aucune action de libération**: il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c46df-158">**No release action**: This is the default value.</span></span>
       - <span data-ttu-id="c46df-159">**Autoriser les destinataires à diffuser un message en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="c46df-159">**Allow recipients to release a message from quarantine**</span></span>
       - <span data-ttu-id="c46df-160">**Autoriser les destinataires à demander la libération d’un message en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="c46df-160">**Allow recipients to request a message to be released from quarantine**</span></span>

     - <span data-ttu-id="c46df-161">**Sélectionnez les actions supplémentaires que les destinataires peuvent effectuer sur les messages mis en quarantaine**: sélectionnez certaines, toutes ou aucune des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c46df-161">**Select additional actions recipients can take on quarantined messages**: Select some, all, or none of the following values:</span></span>
       - <span data-ttu-id="c46df-162">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="c46df-162">**Delete**</span></span>
       - <span data-ttu-id="c46df-163">**Aperçu**</span><span class="sxs-lookup"><span data-stu-id="c46df-163">**Preview**</span></span>
       - <span data-ttu-id="c46df-164">**Autoriser l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="c46df-164">**Allow sender**</span></span>
       - <span data-ttu-id="c46df-165">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="c46df-165">**Block sender**</span></span>

   <span data-ttu-id="c46df-166">Ces autorisations et leur effet sur les messages mis en quarantaine et les notifications de courrier indésirable de l’utilisateur final sont décrits dans la section Détails des autorisations de la [balise de mise en quarantaine](#quarantine-tag-permission-details) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="c46df-166">These permissions and their effect on quarantined messages and in end-user spam notifications are described in the [Quarantine tag permission details](#quarantine-tag-permission-details) section later in this article.</span></span>

   <span data-ttu-id="c46df-167">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c46df-167">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="c46df-168">Sur la page **récapitulative** qui s’affiche, vérifiez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="c46df-168">On the **Summary** page that appears, review your settings.</span></span> <span data-ttu-id="c46df-169">Vous pouvez cliquer sur **modifier** sur chaque paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="c46df-169">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="c46df-170">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="c46df-170">When you're finished, click **Submit**.</span></span>

6. <span data-ttu-id="c46df-171">Cliquez sur **OK** dans la page de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c46df-171">Click **Done** on the confirmation page that appears.</span></span>

<span data-ttu-id="c46df-172">Vous êtes maintenant prêt à affecter la balise de mise en quarantaine à une fonctionnalité de mise en quarantaine, comme décrit dans la section [étape 2](#step-2-assign-a-quarantine-tag-to-supported-features) .</span><span class="sxs-lookup"><span data-stu-id="c46df-172">Now you are ready to assign the quarantine tag to a quarantine feature as described in the [Step 2](#step-2-assign-a-quarantine-tag-to-supported-features) section.</span></span>

### <a name="create-quarantine-tags-in-powershell"></a><span data-ttu-id="c46df-173">Créer des balises de mise en quarantaine dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="c46df-173">Create quarantine tags in PowerShell</span></span>

<span data-ttu-id="c46df-174">Si vous préférez utiliser PowerShell pour créer des balises de mise en quarantaine, connectez-vous à Exchange Online PowerShell ou à Exchange Online Protection PowerShell et utilisez la cmdlet **New-QuarantineTag** .</span><span class="sxs-lookup"><span data-stu-id="c46df-174">If you'd rather use PowerShell to create quarantine tags, connect to Exchange Online PowerShell or Exchange Online Protection PowerShell and use the **New-QuarantineTag** cmdlet.</span></span> <span data-ttu-id="c46df-175">Vous avez le choix entre deux méthodes :</span><span class="sxs-lookup"><span data-stu-id="c46df-175">You have two different methods to choose from:</span></span>

- <span data-ttu-id="c46df-176">Utilisez le paramètre _EndUserQuarantinePermissionsValue_ .</span><span class="sxs-lookup"><span data-stu-id="c46df-176">Use the _EndUserQuarantinePermissionsValue_ parameter.</span></span>
- <span data-ttu-id="c46df-177">Utilisez le paramètre _EndUserQuarantinePermissions_ .</span><span class="sxs-lookup"><span data-stu-id="c46df-177">Use the _EndUserQuarantinePermissions_ parameter.</span></span>

<span data-ttu-id="c46df-178">Ces méthodes sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c46df-178">These methods are described in the following sections.</span></span>

#### <a name="use-the-enduserquarantinepermissionsvalue-parameter"></a><span data-ttu-id="c46df-179">Utiliser le paramètre EndUserQuarantinePermissionsValue</span><span class="sxs-lookup"><span data-stu-id="c46df-179">Use the EndUserQuarantinePermissionsValue parameter</span></span>

<span data-ttu-id="c46df-180">Pour créer une balise de mise en quarantaine à l’aide du paramètre _EndUserQuarantinePermissionsValue_ , utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="c46df-180">To create a quarantine tag using the _EndUserQuarantinePermissionsValue_ parameter, use the following syntax:</span></span>

```powershell
New-QuarantineTag -Name "<UniqueName>" -EndUserQuarantinePermissionsValue <0 to 236>
```

<span data-ttu-id="c46df-181">Le paramètre _EndUserQuarantinePermissionsValue_ utilise une valeur décimale qui est convertie à partir d’une valeur binaire.</span><span class="sxs-lookup"><span data-stu-id="c46df-181">The _EndUserQuarantinePermissionsValue_ parameter uses a decimal value that's converted from a binary value.</span></span> <span data-ttu-id="c46df-182">La valeur binaire correspond aux autorisations de mise en quarantaine de l’utilisateur final disponibles dans un ordre spécifique.</span><span class="sxs-lookup"><span data-stu-id="c46df-182">The binary value corresponds to the available end-user quarantine permissions in a specific order.</span></span> <span data-ttu-id="c46df-183">Pour chaque autorisation, la valeur 1 est égale à true et la valeur 0 équivaut à false.</span><span class="sxs-lookup"><span data-stu-id="c46df-183">For each permission, the value 1 equals True and the value 0 equals False.</span></span>

<span data-ttu-id="c46df-184">L’ordre et les valeurs requis pour chaque autorisation individuelle dans des groupes d’autorisations prédéfinis sont décrits dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="c46df-184">The required order and values for each individual permission in preset permission groups are described in the following table:</span></span>

****

|<span data-ttu-id="c46df-185">Autorisation</span><span class="sxs-lookup"><span data-stu-id="c46df-185">Permission</span></span>|<span data-ttu-id="c46df-186">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="c46df-186">No access</span></span>|<span data-ttu-id="c46df-187">Accès limité</span><span class="sxs-lookup"><span data-stu-id="c46df-187">Limited access</span></span>|<span data-ttu-id="c46df-188">Accès total</span><span class="sxs-lookup"><span data-stu-id="c46df-188">Full access</span></span>|
|---|:---:|:---:|:---:|
|<span data-ttu-id="c46df-189">PermissionToAllowSender</span><span class="sxs-lookup"><span data-stu-id="c46df-189">PermissionToAllowSender</span></span>|<span data-ttu-id="c46df-190">0</span><span class="sxs-lookup"><span data-stu-id="c46df-190">0</span></span>|<span data-ttu-id="c46df-191">0</span><span class="sxs-lookup"><span data-stu-id="c46df-191">0</span></span>|<span data-ttu-id="c46df-192">1 </span><span class="sxs-lookup"><span data-stu-id="c46df-192">1</span></span>|
|<span data-ttu-id="c46df-193">PermissionToBlockSender</span><span class="sxs-lookup"><span data-stu-id="c46df-193">PermissionToBlockSender</span></span>|<span data-ttu-id="c46df-194">0</span><span class="sxs-lookup"><span data-stu-id="c46df-194">0</span></span>|<span data-ttu-id="c46df-195">1 </span><span class="sxs-lookup"><span data-stu-id="c46df-195">1</span></span>|<span data-ttu-id="c46df-196">1 </span><span class="sxs-lookup"><span data-stu-id="c46df-196">1</span></span>|
|<span data-ttu-id="c46df-197">PermissionToDelete</span><span class="sxs-lookup"><span data-stu-id="c46df-197">PermissionToDelete</span></span>|<span data-ttu-id="c46df-198">0</span><span class="sxs-lookup"><span data-stu-id="c46df-198">0</span></span>|<span data-ttu-id="c46df-199">1 </span><span class="sxs-lookup"><span data-stu-id="c46df-199">1</span></span>|<span data-ttu-id="c46df-200">1 </span><span class="sxs-lookup"><span data-stu-id="c46df-200">1</span></span>|
|<span data-ttu-id="c46df-201">PermissionToDownload<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c46df-201">PermissionToDownload<sup>\*</sup></span></span>|<span data-ttu-id="c46df-202">0</span><span class="sxs-lookup"><span data-stu-id="c46df-202">0</span></span>|<span data-ttu-id="c46df-203">0</span><span class="sxs-lookup"><span data-stu-id="c46df-203">0</span></span>|<span data-ttu-id="c46df-204">0</span><span class="sxs-lookup"><span data-stu-id="c46df-204">0</span></span>|
|<span data-ttu-id="c46df-205">PermissionToPreview</span><span class="sxs-lookup"><span data-stu-id="c46df-205">PermissionToPreview</span></span>|<span data-ttu-id="c46df-206">0</span><span class="sxs-lookup"><span data-stu-id="c46df-206">0</span></span>|<span data-ttu-id="c46df-207">1 </span><span class="sxs-lookup"><span data-stu-id="c46df-207">1</span></span>|<span data-ttu-id="c46df-208">1 </span><span class="sxs-lookup"><span data-stu-id="c46df-208">1</span></span>|
|<span data-ttu-id="c46df-209">PermissionToRelease<sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="c46df-209">PermissionToRelease<sup>\*\*</sup></span></span>|<span data-ttu-id="c46df-210">0</span><span class="sxs-lookup"><span data-stu-id="c46df-210">0</span></span>|<span data-ttu-id="c46df-211">0</span><span class="sxs-lookup"><span data-stu-id="c46df-211">0</span></span>|<span data-ttu-id="c46df-212">1 </span><span class="sxs-lookup"><span data-stu-id="c46df-212">1</span></span>|
|<span data-ttu-id="c46df-213">PermissionToRequestRelease<sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="c46df-213">PermissionToRequestRelease<sup>\*\*</sup></span></span>|<span data-ttu-id="c46df-214">0</span><span class="sxs-lookup"><span data-stu-id="c46df-214">0</span></span>|<span data-ttu-id="c46df-215">1 </span><span class="sxs-lookup"><span data-stu-id="c46df-215">1</span></span>|<span data-ttu-id="c46df-216">0</span><span class="sxs-lookup"><span data-stu-id="c46df-216">0</span></span>|
|<span data-ttu-id="c46df-217">PermissionToViewHeader<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c46df-217">PermissionToViewHeader<sup>\*</sup></span></span>|<span data-ttu-id="c46df-218">0</span><span class="sxs-lookup"><span data-stu-id="c46df-218">0</span></span>|<span data-ttu-id="c46df-219">0</span><span class="sxs-lookup"><span data-stu-id="c46df-219">0</span></span>|<span data-ttu-id="c46df-220">0</span><span class="sxs-lookup"><span data-stu-id="c46df-220">0</span></span>|
|<span data-ttu-id="c46df-221">Valeur binaire</span><span class="sxs-lookup"><span data-stu-id="c46df-221">Binary value</span></span>|<span data-ttu-id="c46df-222">00000000</span><span class="sxs-lookup"><span data-stu-id="c46df-222">00000000</span></span>|<span data-ttu-id="c46df-223">01101010</span><span class="sxs-lookup"><span data-stu-id="c46df-223">01101010</span></span>|<span data-ttu-id="c46df-224">11101100</span><span class="sxs-lookup"><span data-stu-id="c46df-224">11101100</span></span>|
|<span data-ttu-id="c46df-225">Valeur décimale à utiliser</span><span class="sxs-lookup"><span data-stu-id="c46df-225">Decimal value to use</span></span>|<span data-ttu-id="c46df-226">0</span><span class="sxs-lookup"><span data-stu-id="c46df-226">0</span></span>|<span data-ttu-id="c46df-227">106</span><span class="sxs-lookup"><span data-stu-id="c46df-227">106</span></span>|<span data-ttu-id="c46df-228">236</span><span class="sxs-lookup"><span data-stu-id="c46df-228">236</span></span>|

<span data-ttu-id="c46df-229"><sup>\*</sup> Actuellement, cette valeur est toujours 0.</span><span class="sxs-lookup"><span data-stu-id="c46df-229"><sup>\*</sup> Currently, this value is always 0.</span></span> <span data-ttu-id="c46df-230">Pour PermissionToViewHeader, la valeur 0 ne masque pas le bouton d' **en-tête afficher le message** dans les détails du message en quarantaine (le bouton est toujours disponible).</span><span class="sxs-lookup"><span data-stu-id="c46df-230">For PermissionToViewHeader, the value 0 doesn't hide the **View message header** button in the details of the quarantined message (the button is always available).</span></span>

<span data-ttu-id="c46df-231"><sup>\*\*</sup> Ne définissez pas ces deux valeurs sur 1.</span><span class="sxs-lookup"><span data-stu-id="c46df-231"><sup>\*\*</sup> Don't set both of these values to 1.</span></span> <span data-ttu-id="c46df-232">Définissez un sur 1 et l’autre sur 0, ou définissez-les deux sur 0.</span><span class="sxs-lookup"><span data-stu-id="c46df-232">Set one to 1 and the other to 0, or set both to 0.</span></span>

<span data-ttu-id="c46df-233">Cet exemple montre comment créer un nom de balise de mise en quarantaine NoAccess qui affecte les autorisations sans accès comme décrit dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="c46df-233">This example creates a new quarantine tag name NoAccess that assigns the No access permissions as described in the previous table.</span></span>

```powershell
New-QuarantineTag -Name NoAccess -EndUserQuarantinePermissionsValue 0
```

<span data-ttu-id="c46df-234">Pour les autorisations d’accès limité, utilisez la valeur 106.</span><span class="sxs-lookup"><span data-stu-id="c46df-234">For Limited access permissions, use the value 106.</span></span> <span data-ttu-id="c46df-235">Pour les autorisations d’accès total, utilisez la valeur 236.</span><span class="sxs-lookup"><span data-stu-id="c46df-235">For Full access permissions, use the value 236.</span></span>

<span data-ttu-id="c46df-236">Pour les autorisations personnalisées, utilisez le tableau précédent pour obtenir la valeur binaire correspondant aux autorisations de votre choix.</span><span class="sxs-lookup"><span data-stu-id="c46df-236">For custom permissions, use the previous table to get the binary value that corresponds to the permissions you want.</span></span> <span data-ttu-id="c46df-237">Convertissez la valeur binaire en une valeur décimale et utilisez la valeur décimale pour le paramètre _EndUserQuarantinePermissionsValue_ .</span><span class="sxs-lookup"><span data-stu-id="c46df-237">Convert the binary value to a decimal value and use the decimal value for the _EndUserQuarantinePermissionsValue_ parameter.</span></span>

<span data-ttu-id="c46df-238">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/new-quarantinetag).</span><span class="sxs-lookup"><span data-stu-id="c46df-238">For detailed syntax and parameter information, see [New-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/new-quarantinetag).</span></span>

#### <a name="use-the-enduserquarantinepermissions-parameter"></a><span data-ttu-id="c46df-239">Utiliser le paramètre EndUserQuarantinePermissions</span><span class="sxs-lookup"><span data-stu-id="c46df-239">Use the EndUserQuarantinePermissions parameter</span></span>

<span data-ttu-id="c46df-240">Pour créer une balise de mise en quarantaine à l’aide du paramètre _EndUserQuarantinePermissionsValue_ , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c46df-240">To create a quarantine tag using the _EndUserQuarantinePermissionsValue_ parameter, do the following steps:</span></span>

<span data-ttu-id="c46df-241">A.</span><span class="sxs-lookup"><span data-stu-id="c46df-241">A.</span></span> <span data-ttu-id="c46df-242">Stockez un objet d’autorisations de mise en quarantaine dans une variable à l’aide de la cmdlet **New-QuarantinePermissions** .</span><span class="sxs-lookup"><span data-stu-id="c46df-242">Store a quarantine permissions object in a variable using the **New-QuarantinePermissions** cmdlet.</span></span>

<p>

<span data-ttu-id="c46df-243">B.</span><span class="sxs-lookup"><span data-stu-id="c46df-243">B.</span></span> <span data-ttu-id="c46df-244">Utilisez la variable comme valeur _EndUserQuarantinePermissions_ dans la commande **New-QuarantineTag** .</span><span class="sxs-lookup"><span data-stu-id="c46df-244">Use the variable as the _EndUserQuarantinePermissions_ value in the **New-QuarantineTag** command.</span></span>

##### <a name="step-a-store-a-quarantine-permissions-object-in-a-variable"></a><span data-ttu-id="c46df-245">Étape A : stocker un objet d’autorisations de mise en quarantaine dans une variable</span><span class="sxs-lookup"><span data-stu-id="c46df-245">Step A: Store a quarantine permissions object in a variable</span></span>

<span data-ttu-id="c46df-246">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="c46df-246">Use the following syntax:</span></span>

```powershell
$<VariableName> = New-QuarantinePermissions [-PermissionToAllowSender <$true | $False>] [-PermissionToBlockSender <$true | $False>] [-PermissionToDelete <$true | $False>] [-PermissionToPreview <$true | $False>] [-PermissionToRelease <$true | $False>] [-PermissionToRequestRelease <$true | $False>]
```

<span data-ttu-id="c46df-247">La valeur par défaut des paramètres inutilisés est `$false` , de sorte que vous devez uniquement utiliser les paramètres pour lesquels vous souhaitez définir la valeur `$true` .</span><span class="sxs-lookup"><span data-stu-id="c46df-247">The default value for any unused parameters is `$false`, so you only need to use the parameters where you want to set value to `$true`.</span></span>

<span data-ttu-id="c46df-248">Les exemples suivants montrent comment créer des objets permission qui correspondent aux groupes d’autorisations prédéfinis :</span><span class="sxs-lookup"><span data-stu-id="c46df-248">The following examples show how to create permission objects that correspond to the preset permissions groups:</span></span>

- <span data-ttu-id="c46df-249">**Aucun accès**:</span><span class="sxs-lookup"><span data-stu-id="c46df-249">**No access**:</span></span>

  ```powershell
  $NoAccess = New-QuarantinePermissions
  ```

- <span data-ttu-id="c46df-250">**Accès limité**:</span><span class="sxs-lookup"><span data-stu-id="c46df-250">**Limited access**:</span></span>

  ```powershell
  $LimitedAccess = New-QuarantinePermissions -PermissionToBlockSender $true -PermissionToDelete $true -PermissionToPreview $true -PermissionToRequestRelease $true
  ```

- <span data-ttu-id="c46df-251">**Accès total**:</span><span class="sxs-lookup"><span data-stu-id="c46df-251">**Full access**:</span></span>

  ```powershell
  $FullAccess = New-QuarantinePermissions -PermissionToAllowSender $true -PermissionToBlockSender $true -PermissionToDelete $true -PermissionToPreview $true -PermissionToRelease $true
  ```

<span data-ttu-id="c46df-252">Pour afficher les valeurs que vous avez définies, exécutez le nom de la variable en tant que commande (par exemple, exécutez la commande `$NoAccess` ).</span><span class="sxs-lookup"><span data-stu-id="c46df-252">To see the values that you've set, run the variable name as a command (for example, run the command `$NoAccess`).</span></span>

<span data-ttu-id="c46df-253">Pour les autorisations personnalisées, ne définissez pas les paramètres _PermissionToRelease_ et _PermissionToRequestRelease_ sur `$true` .</span><span class="sxs-lookup"><span data-stu-id="c46df-253">For custom permissions, don't set both the _PermissionToRelease_ and _PermissionToRequestRelease_ parameters to `$true`.</span></span> <span data-ttu-id="c46df-254">Définissez un comme `$true` et laissez le reste `$false` , ou laissez les deux en tant que `$false` .</span><span class="sxs-lookup"><span data-stu-id="c46df-254">Set one to `$true` and leave the other as `$false`, or leave both as `$false`.</span></span>

<span data-ttu-id="c46df-255">Vous pouvez également modifier une variable d’objet d’autorisations existante après avoir créé mais avant de l’utiliser à l’aide de la cmdlet **Set-QuarantinePermissions** .</span><span class="sxs-lookup"><span data-stu-id="c46df-255">You can also modify an existing permissions object variable after you create but before you use it by using the **Set-QuarantinePermissions** cmdlet.</span></span>

<span data-ttu-id="c46df-256">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-QuarantinePermissions](https://docs.microsoft.com/powershell/module/exchange/new-quarantinepermissions) et [Set-QuarantinePermissions](https://docs.microsoft.com/powershell/module/exchange/set-quarantinepermissions).</span><span class="sxs-lookup"><span data-stu-id="c46df-256">For detailed syntax and parameter information, see [New-QuarantinePermissions](https://docs.microsoft.com/powershell/module/exchange/new-quarantinepermissions) and [Set-QuarantinePermissions](https://docs.microsoft.com/powershell/module/exchange/set-quarantinepermissions).</span></span>

##### <a name="step-b-use-the-variable-in-the-new-quarantinetag-command"></a><span data-ttu-id="c46df-257">Étape B : utiliser la variable dans la commande New-QuarantineTag</span><span class="sxs-lookup"><span data-stu-id="c46df-257">Step B: Use the variable in the New-QuarantineTag command</span></span>

<span data-ttu-id="c46df-258">Une fois que vous avez créé et stocké l’objet permissions dans une variable, utilisez la variable pour la valeur du paramètre _EndUserQuarantinePermission_ dans la commande **New-QuarantineTag** suivante :</span><span class="sxs-lookup"><span data-stu-id="c46df-258">After you've created and stored the permissions object in a variable, use the variable for the _EndUserQuarantinePermission_ parameter value in the following **New-QuarantineTag** command:</span></span>

```powershell
New-QuarantineTag -Name "<UniqueName>" -EndUserQuarantinePermissions $<VariableName>
```

<span data-ttu-id="c46df-259">Cet exemple crée une nouvelle balise de mise en quarantaine nommée LimitedAccess à l’aide de l' `$LimitedAccess` objet permissions qui a été décrit et créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="c46df-259">This example creates a new quarantine tag named LimitedAccess using the `$LimitedAccess` permissions object that was described and created in the previous step.</span></span>

```powershell
New-QuarantineTag -Name LimitedAccess -EndUserQuarantinePermissions $LimitedAccess
```

<span data-ttu-id="c46df-260">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/new-quarantinetag).</span><span class="sxs-lookup"><span data-stu-id="c46df-260">For detailed syntax and parameter information, see [New-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/new-quarantinetag).</span></span>

## <a name="step-2-assign-a-quarantine-tag-to-supported-features"></a><span data-ttu-id="c46df-261">Étape 2 : affecter une balise de mise en quarantaine aux fonctionnalités prises en charge</span><span class="sxs-lookup"><span data-stu-id="c46df-261">Step 2: Assign a quarantine tag to supported features</span></span>

<span data-ttu-id="c46df-262">Dans les fonctionnalités de protection _prises en charge_ qui met en quarantaine les messages ou les fichiers (automatiquement ou en tant qu’une action configurable), vous pouvez affecter une balise de mise en quarantaine aux actions de mise en quarantaine disponibles.</span><span class="sxs-lookup"><span data-stu-id="c46df-262">In _supported_ protection features that quarantine messages or files (automatically or as a configurable action), you can assign a quarantine tag to the available quarantine actions.</span></span> <span data-ttu-id="c46df-263">Les fonctionnalités de mise en quarantaine des messages et la disponibilité des balises de mise en quarantaine sont décrites dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="c46df-263">Features that quarantine messages and the availability of quarantine tags are described in the following table:</span></span>

****

|<span data-ttu-id="c46df-264">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="c46df-264">Feature</span></span>|<span data-ttu-id="c46df-265">Balises de mise en quarantaine prises en charge ?</span><span class="sxs-lookup"><span data-stu-id="c46df-265">Quarantine tags supported?</span></span>|<span data-ttu-id="c46df-266">Balises de mise en quarantaine par défaut utilisées</span><span class="sxs-lookup"><span data-stu-id="c46df-266">Default quarantine tags used</span></span>|
|---|:---:|---|
|<span data-ttu-id="c46df-267">[Stratégies de blocage du courrier indésirable](configure-your-spam-filter-policies.md):</span><span class="sxs-lookup"><span data-stu-id="c46df-267">[Anti-spam policies](configure-your-spam-filter-policies.md):</span></span> <ul><li><span data-ttu-id="c46df-268">**Courrier indésirable** (_SpamAction_)</span><span class="sxs-lookup"><span data-stu-id="c46df-268">**Spam** (_SpamAction_)</span></span></li><li><span data-ttu-id="c46df-269">**Courrier indésirable à niveau de confiance élevé** (_HighConfidenceSpamAction_)</span><span class="sxs-lookup"><span data-stu-id="c46df-269">**High confidence spam** (_HighConfidenceSpamAction_)</span></span></li><li><span data-ttu-id="c46df-270">**Courrier électronique de hameçonnage** (_PhishSpamAction_)</span><span class="sxs-lookup"><span data-stu-id="c46df-270">**Phishing email** (_PhishSpamAction_)</span></span></li><li><span data-ttu-id="c46df-271">**Courrier électronique de hameçonnage à haute fiabilité** (_HighConfidencePhishAction_)</span><span class="sxs-lookup"><span data-stu-id="c46df-271">**High confidence phishing email** (_HighConfidencePhishAction_)</span></span></li><li><span data-ttu-id="c46df-272">**Courrier en masse** (_BulkSpamAction_)</span><span class="sxs-lookup"><span data-stu-id="c46df-272">**Bulk email** (_BulkSpamAction_)</span></span></li></ul>|<span data-ttu-id="c46df-273">Oui</span><span class="sxs-lookup"><span data-stu-id="c46df-273">Yes</span></span>|<ul><li><span data-ttu-id="c46df-274">DefaultSpamTag (accès total)</span><span class="sxs-lookup"><span data-stu-id="c46df-274">DefaultSpamTag (Full access)</span></span></li><li><span data-ttu-id="c46df-275">DefaultHighConfSpamTag (accès total)</span><span class="sxs-lookup"><span data-stu-id="c46df-275">DefaultHighConfSpamTag (Full access)</span></span></li><li><span data-ttu-id="c46df-276">DefaultPhishTag (accès total)</span><span class="sxs-lookup"><span data-stu-id="c46df-276">DefaultPhishTag (Full access)</span></span></li><li><span data-ttu-id="c46df-277">DefaultHighConfPhishTag (pas d’accès)</span><span class="sxs-lookup"><span data-stu-id="c46df-277">DefaultHighConfPhishTag (No access)</span></span></li><li><span data-ttu-id="c46df-278">DefaultBulkTag (accès total)</span><span class="sxs-lookup"><span data-stu-id="c46df-278">DefaultBulkTag (Full access)</span></span></li></ul>
|<span data-ttu-id="c46df-279">Stratégies anti-hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="c46df-279">Anti-phishing policies:</span></span> <ul><li><span data-ttu-id="c46df-280">[Protection contre l’usurpation d’identité](set-up-anti-phishing-policies.md#spoof-settings) (_AuthenticationFailAction_)</span><span class="sxs-lookup"><span data-stu-id="c46df-280">[Spoof intelligence protection](set-up-anti-phishing-policies.md#spoof-settings) (_AuthenticationFailAction_)</span></span></li><li><span data-ttu-id="c46df-281">[Protection contre l’usurpation d’identité](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365):<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c46df-281">[Impersonation protection](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365):<sup>\*</sup></span></span> <ul><li><span data-ttu-id="c46df-282">**Si le courrier électronique est envoyé par un utilisateur emprunté** (_TargetedUserProtectionAction_)</span><span class="sxs-lookup"><span data-stu-id="c46df-282">**If email is sent by an impersonated user** (_TargetedUserProtectionAction_)</span></span></li><li><span data-ttu-id="c46df-283">**Si le courrier électronique est envoyé par un domaine emprunté** (_TargetedDomainProtectionAction_)</span><span class="sxs-lookup"><span data-stu-id="c46df-283">**If email is sent by an impersonated domain** (_TargetedDomainProtectionAction_)</span></span></li><li><span data-ttu-id="c46df-284">Intelligence des boîtes **aux lettres** \> **Si le courrier électronique est envoyé par un utilisateur emprunté** (_MailboxIntelligenceProtectionAction_)</span><span class="sxs-lookup"><span data-stu-id="c46df-284">**Mailbox intelligence** \> **If email is sent by an impersonated user** (_MailboxIntelligenceProtectionAction_)</span></span></li></ul></li></ul></ul>|<span data-ttu-id="c46df-285">Non</span><span class="sxs-lookup"><span data-stu-id="c46df-285">No</span></span>|<span data-ttu-id="c46df-286">s/o</span><span class="sxs-lookup"><span data-stu-id="c46df-286">n/a</span></span>|
|<span data-ttu-id="c46df-287">[Stratégies de protection contre les programmes malveillants](configure-anti-malware-policies.md): tous les messages détectés sont toujours mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c46df-287">[Anti-malware policies](configure-anti-malware-policies.md): All detected messages are always quarantined.</span></span>|<span data-ttu-id="c46df-288">Non</span><span class="sxs-lookup"><span data-stu-id="c46df-288">No</span></span>|<span data-ttu-id="c46df-289">s/o</span><span class="sxs-lookup"><span data-stu-id="c46df-289">n/a</span></span>|
|[<span data-ttu-id="c46df-290">ATP pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c46df-290">ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](atp-for-spo-odb-and-teams.md)|<span data-ttu-id="c46df-291">Non</span><span class="sxs-lookup"><span data-stu-id="c46df-291">No</span></span>|<span data-ttu-id="c46df-292">s/o</span><span class="sxs-lookup"><span data-stu-id="c46df-292">n/a</span></span>|
|<span data-ttu-id="c46df-293">Les [règles de flux de messagerie](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (également appelées règles de transport) avec l’action : **remet le message à la quarantaine hébergée** (_mise en quarantaine_).</span><span class="sxs-lookup"><span data-stu-id="c46df-293">[Mail flow rules](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (also known as transport rules) with the action: **Deliver the message to the hosted quarantine** (_Quarantine_).</span></span>|<span data-ttu-id="c46df-294">Non</span><span class="sxs-lookup"><span data-stu-id="c46df-294">No</span></span>|<span data-ttu-id="c46df-295">s/o</span><span class="sxs-lookup"><span data-stu-id="c46df-295">n/a</span></span>|
|

<span data-ttu-id="c46df-296"><sup>\*</sup> Les paramètres de protection contre l’emprunt d’identité sont disponibles uniquement dans les stratégies anti-hameçonnage de Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="c46df-296"><sup>\*</sup> Impersonation protection settings are available only in anti-phishing policies in Microsoft Defender for Office 365.</span></span>

<span data-ttu-id="c46df-297">Si vous êtes satisfait des autorisations de l’utilisateur final fournies par les balises de mise en quarantaine par défaut, aucune action n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c46df-297">If you're happy with the end-user permissions that are provided by the default quarantine tags, you don't need to do anything.</span></span> <span data-ttu-id="c46df-298">Si vous souhaitez personnaliser les fonctionnalités de l’utilisateur final (boutons disponibles) dans les notifications de courrier indésirable de l’utilisateur final ou les détails du message en quarantaine, vous pouvez affecter une balise de mise en quarantaine personnalisée.</span><span class="sxs-lookup"><span data-stu-id="c46df-298">If you want to customize the end-user capabilities (available buttons) in end-user spam notifications or in quarantined message details, you can assign a custom quarantine tag.</span></span>

### <a name="assign-quarantine-tags-in-anti-spam-policies-in-the-security--compliance-center"></a><span data-ttu-id="c46df-299">Attribuer des balises de mise en quarantaine dans les stratégies de blocage du courrier indésirable dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="c46df-299">Assign quarantine tags in anti-spam policies in the Security & Compliance Center</span></span>

<span data-ttu-id="c46df-300">Pour plus d’informations sur la création et la modification de stratégies de blocage du courrier indésirable, voir [configurer les stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c46df-300">Full instructions for creating and modifying anti-spam policies are described in [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

1. <span data-ttu-id="c46df-301">Dans le centre de sécurité & conformité, accédez à stratégie de **gestion des menaces** , \>  \> puis sélectionnez **blocage du courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="c46df-301">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> and then select **Anti-spam**.</span></span> <span data-ttu-id="c46df-302">Ou ouvrez <https://protection.office.com/antispam> .</span><span class="sxs-lookup"><span data-stu-id="c46df-302">Or, open <https://protection.office.com/antispam>.</span></span>

2. <span data-ttu-id="c46df-303">Recherchez et sélectionnez une stratégie de blocage du courrier indésirable existante à modifier, ou créez une nouvelle stratégie de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c46df-303">Find and select an existing anti-spam policy to edit, or create a new anti-spam policy.</span></span>

3. <span data-ttu-id="c46df-304">Dans la fenêtre mobile détails de la stratégie, développez la section **actions de courrier indésirable et en bloc** .</span><span class="sxs-lookup"><span data-stu-id="c46df-304">In the policy details flyout, expand the **Spam and bulk actions** section.</span></span>

4. <span data-ttu-id="c46df-305">Si vous avez sélectionné **message mis en quarantaine** pour l’action d’une option de filtrage du courrier indésirable disponible, la zone **appliquer la balise de stratégie de mise en quarantaine** est disponible pour vous permettant de sélectionner la balise de mise en quarantaine pour ce verdict.</span><span class="sxs-lookup"><span data-stu-id="c46df-305">If you've selected **Quarantine message** for the action of an available spam filtering verdict, the **Apply quarantine policy tag** box is available for you to select the quarantine tag for that verdict.</span></span>

   <span data-ttu-id="c46df-306">**Remarque**: lorsque vous créez une stratégie, une valeur de balise de mise en quarantaine vide pour un filtrage du courrier indésirable en verdict indique que la balise de mise en quarantaine par défaut pour ce verdict est utilisée.</span><span class="sxs-lookup"><span data-stu-id="c46df-306">**Note**: When you create a new policy, a blank quarantine tag value for a spam filtering verdict indicates the default quarantine tag for that verdict is used.</span></span> <span data-ttu-id="c46df-307">Lorsque vous modifiez ultérieurement la stratégie, les valeurs non renseignées sont remplacées par les noms de balise de mise en quarantaine par défaut réels, comme décrit dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="c46df-307">When you later edit the policy, the blank values are replaced by the actual default quarantine tag names as described in the previous table.</span></span>

   ![Sélections de la balise de quarantaine dans une stratégie de blocage du courrier indésirable](../../media/quarantine-tags-in-anti-spam-policies.png)

5. <span data-ttu-id="c46df-309">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c46df-309">When you're finished, click **Save**.</span></span>

#### <a name="assign-quarantine-tags-in-anti-spam-policies-in-powershell"></a><span data-ttu-id="c46df-310">Attribuer des balises de mise en quarantaine dans les stratégies de blocage du courrier indésirable dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="c46df-310">Assign quarantine tags in anti-spam policies in PowerShell</span></span>

<span data-ttu-id="c46df-311">Si vous préférez utiliser PowerShell pour attribuer des balises de mise en quarantaine dans des stratégies de blocage du courrier indésirable, connectez-vous à Exchange Online PowerShell ou à Exchange Online Protection PowerShell, puis utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="c46df-311">If you'd rather use PowerShell to assign quarantine tags in anti-spam policies, connect to Exchange Online PowerShell or Exchange Online Protection PowerShell and use the following syntax:</span></span>

```powershell
<New-HostedContentFilterPolicy -Name "<Unique name>" | Set-HostedContentFilterPolicy -Identity "<Policy name>">  [-SpamAction Quarantine] [-SpamQuarantineTag <QuarantineTagName>] [-HighConfidenceSpamAction Quarantine] [-HighConfidenceSpamQuarantineTag <QuarantineTagName>] [-PhishSpamAction Quarantine] [-PhishQuarantineTag <QuarantineTagName>] [-HighConfidencePhishQuarantineTag <QuarantineTagName>] [-BulkSpamAction Quarantine] [-BulkQuarantineTag <QuarantineTagName>] ...
```

<span data-ttu-id="c46df-312">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="c46df-312">**Notes**:</span></span>

- <span data-ttu-id="c46df-313">La valeur par défaut du paramètre _HighConfidencePhishAction_ est mise en quarantaine, vous n’avez donc pas besoin de définir l’action de mise en quarantaine pour les détections de hameçonnage à haute fiabilité dans les nouvelles stratégies de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c46df-313">The default value for the _HighConfidencePhishAction_ parameter is Quarantine, so you don't need to set the Quarantine action for high confidence phishing detections in new anti-spam policies.</span></span> <span data-ttu-id="c46df-314">Pour tous les autres filtrages de courrier indésirable en fonction des stratégies anti-courrier indésirable nouvelles ou existantes, la balise de mise en quarantaine n’est effective que si la valeur de l’action est mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c46df-314">For all other spam filtering verdicts in new or existing anti-spam policies, the quarantine tag is only effective if the action value is Quarantine.</span></span> <span data-ttu-id="c46df-315">Pour afficher les valeurs d’action dans les stratégies anti-courrier indésirable existantes, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c46df-315">To see the action values in existing anti-spam policies, run the following command:</span></span>

  ```powershell
  Get-HostedContentFilterPolicy | Format-Table Name,*SpamAction,HighConfidencePhishAction
  ```

  <span data-ttu-id="c46df-316">Pour plus d’informations sur les valeurs d’action par défaut et sur les valeurs d’action recommandées pour standard et strict, voir [EOP anti-spam Policy Settings](recommended-settings-for-eop-and-office365-atp.md#eop-anti-spam-policy-settings).</span><span class="sxs-lookup"><span data-stu-id="c46df-316">For information about the default action values and the recommended action values for Standard and Strict, see [EOP anti-spam policy settings](recommended-settings-for-eop-and-office365-atp.md#eop-anti-spam-policy-settings).</span></span>

- <span data-ttu-id="c46df-317">Le filtrage du courrier indésirable correspondant à un paramètre de balise de mise en quarantaine correspondant signifie que la [balise de mise en quarantaine par défaut](#step-2-assign-a-quarantine-tag-to-supported-features) pour ce verdict est utilisée.</span><span class="sxs-lookup"><span data-stu-id="c46df-317">A spam filtering verdict without a corresponding quarantine tag parameter means the [default quarantine tag](#step-2-assign-a-quarantine-tag-to-supported-features) for that verdict is used.</span></span>

  <span data-ttu-id="c46df-318">Vous ne devez remplacer une balise de mise en quarantaine par défaut par une balise de mise en quarantaine personnalisée que si vous souhaitez modifier les fonctionnalités de l’utilisateur final par défaut sur les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c46df-318">You only need to replace a default quarantine tag with a custom quarantine tag if you want to change the default end-user capabilities on quarantined messages.</span></span>

- <span data-ttu-id="c46df-319">Une nouvelle stratégie de blocage du courrier indésirable dans PowerShell nécessite une stratégie de filtrage du courrier indésirable (paramètres) à l’aide de la cmdlet **New-HostedContentFilterPolicy** et une nouvelle règle de filtrage du courrier indésirable (filtres de destinataires) à l’aide de la cmdlet **New-hostedcontentfilterrule permet** .</span><span class="sxs-lookup"><span data-stu-id="c46df-319">A new anti-spam policy in PowerShell requires a spam filter policy (settings) using the **New-HostedContentFilterPolicy** cmdlet and a new spam filter rule (recipient filters) using the **New-HostedContentFilterRule** cmdlet.</span></span> <span data-ttu-id="c46df-320">Pour obtenir des instructions, consultez la rubrique [Utiliser PowerShell pour créer des stratégies de blocage du courrier indésirable](configure-your-spam-filter-policies.md#use-powershell-to-create-anti-spam-policies).</span><span class="sxs-lookup"><span data-stu-id="c46df-320">For instructions, see [Use PowerShell to create anti-spam policies](configure-your-spam-filter-policies.md#use-powershell-to-create-anti-spam-policies).</span></span>

<span data-ttu-id="c46df-321">Cet exemple crée une nouvelle stratégie de filtrage du courrier indésirable nommée Research Department avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="c46df-321">This example creates a new spam filter policy named Research Department with the following settings:</span></span>

- <span data-ttu-id="c46df-322">L’action pour l’ensemble du filtrage du courrier indésirable est définie sur quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c46df-322">The action for all spam filtering verdicts is set to Quarantine.</span></span>
- <span data-ttu-id="c46df-323">La balise de mise en quarantaine personnalisée nommée NoAccess qui n’affecte pas d’autorisations d' **accès** remplace les balises de mise en quarantaine par défaut qui n’assignent pas encore d’autorisations d' **accès** par défaut.</span><span class="sxs-lookup"><span data-stu-id="c46df-323">The custom quarantine tag named NoAccess that assigns **No access** permissions replaces any default quarantine tags that don't already assign **No access** permissions by default.</span></span>

```powershell
New-HostedContentFilterPolicy -Name Research Department -SpamAction Quarantine -SpamQuarantineTag NoAccess -HighConfidenceSpamAction Quarantine -HighConfidenceSpamQuarantineTag NoAction -PhishSpamAction Quarantine -PhishQuarantineTag NoAction -BulkSpamAction Quarantine -BulkQuarantineTag NoAccess
```

<span data-ttu-id="c46df-324">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/new-hostedcontentfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="c46df-324">For detailed syntax and parameter information, see [New-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/new-hostedcontentfilterpolicy).</span></span>

<span data-ttu-id="c46df-325">Cet exemple modifie la stratégie de filtrage du courrier indésirable nommée Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c46df-325">This example modifies the existing spam filter policy named Human Resources.</span></span> <span data-ttu-id="c46df-326">L’action pour le verdict de mise en quarantaine du courrier indésirable est définie sur quarantaine et la balise de mise en quarantaine personnalisée nommée NoAccess est attribuée.</span><span class="sxs-lookup"><span data-stu-id="c46df-326">The action for the spam quarantine verdict is set to Quarantine, and the custom quarantine tag named NoAccess is assigned.</span></span>

```powershell
Set-HostedContentFilterPolicy -Identity "Human Resources" -SpamAction Quarantine -SpamQuarantineTag NoAccess
```

<span data-ttu-id="c46df-327">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-hostedcontentfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="c46df-327">For detailed syntax and parameter information, see [Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-hostedcontentfilterpolicy).</span></span>

## <a name="configure-global-quarantine-notification-settings-in-the-security--compliance-center"></a><span data-ttu-id="c46df-328">Configurer les paramètres de notification de mise en quarantaine globale dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="c46df-328">Configure global quarantine notification settings in the Security & Compliance Center</span></span>

<span data-ttu-id="c46df-329">Les paramètres globaux pour les balises de mise en quarantaine vous permettent de personnaliser les notifications de courrier indésirable de l’utilisateur final qui sont envoyées aux destinataires des messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c46df-329">The global settings for quarantine tags allow you to customize the end-user spam notifications that are sent to recipients of messages that were quarantined.</span></span> <span data-ttu-id="c46df-330">Pour plus d’informations sur ces notifications, consultez la rubrique [notifications de courrier indésirable de l’utilisateur final](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span><span class="sxs-lookup"><span data-stu-id="c46df-330">For more information about these notifications, see [End-user spam notifications](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span>

1. <span data-ttu-id="c46df-331">Dans le centre de sécurité & conformité, accédez à stratégie de **gestion des menaces** , \>  puis sélectionnez **balises de mise en quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="c46df-331">In the Security & Compliance Center, go to **Threat management** \> **Policy** and then select **Quarantine tags**.</span></span>

2. <span data-ttu-id="c46df-332">Sur la page **balises de quarantaine** , sélectionnez **paramètres globaux**.</span><span class="sxs-lookup"><span data-stu-id="c46df-332">On the **Quarantine tags** page, select **Global settings**.</span></span>

3. <span data-ttu-id="c46df-333">Dans la fenêtre mobile **paramètres de notification de mise en quarantaine** qui s’ouvre, configurez une partie ou l’ensemble des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="c46df-333">In the **Quarantine notification settings** flyout that opens, configure some or all of the following settings:</span></span>

   - <span data-ttu-id="c46df-334">**Utiliser mon logo de société**: sélectionnez cette option pour remplacer le logo Microsoft par défaut qui est utilisé en haut des notifications de courrier indésirable de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="c46df-334">**Use my company logo**: Select this option to replace the default Microsoft logo that's use at the top of end-user spam notifications.</span></span> <span data-ttu-id="c46df-335">Avant cela, vous devez suivre les instructions de la procédure [personnaliser le thème Microsoft 365 de votre organisation](https://docs.microsoft.com/microsoft-365/admin/setup/customize-your-organization-theme) pour télécharger votre logo personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c46df-335">Before you do this, you need to follow the instructions in [Customize the Microsoft 365 theme for your organization](https://docs.microsoft.com/microsoft-365/admin/setup/customize-your-organization-theme) to upload your custom logo.</span></span>

     <span data-ttu-id="c46df-336">La capture d’écran suivante montre un logo personnalisé dans une notification de courrier indésirable pour l’utilisateur final :</span><span class="sxs-lookup"><span data-stu-id="c46df-336">The following screenshot shows a custom logo in an end-user spam notification:</span></span>

     ![Un logo personnalisé dans une notification de courrier indésirable pour l’utilisateur final](../../media/quarantine-tags-esn-customization-logo.png)

   - <span data-ttu-id="c46df-338">**Choisir la langue**: les notifications de courrier indésirable de l’utilisateur final sont déjà localisées en fonction des paramètres de langue du destinataire.</span><span class="sxs-lookup"><span data-stu-id="c46df-338">**Choose language**: End-user spam notifications are already localized based on the recipient's language settings.</span></span> <span data-ttu-id="c46df-339">Vous pouvez spécifier un texte personnalisé dans différentes langues pour le **nom d’affichage** et les valeurs de clause d’exclusion de **responsabilité** .</span><span class="sxs-lookup"><span data-stu-id="c46df-339">You can specify customized text in different languages for the **Display name** and **Disclaimer** values.</span></span>

     <span data-ttu-id="c46df-340">Sélectionnez au moins une langue dans la première langue, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="c46df-340">Select at least one language from the first language box and then click **Add**.</span></span> <span data-ttu-id="c46df-341">Vous pouvez sélectionner plusieurs langues en cliquant sur **Ajouter** après chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="c46df-341">You can select multiple languages by clicking **Add** after each one.</span></span> <span data-ttu-id="c46df-342">Une case langue de section affiche toutes les langues que vous avez sélectionnées :</span><span class="sxs-lookup"><span data-stu-id="c46df-342">A section language box shows all of the languages that you've selected:</span></span>

     ![Langues sélectionnées dans la deuxième langue de la zone dans les paramètres de notification de mise en quarantaine globale des balises de mise en quarantaine](../../media/quarantine-tags-esn-customization-selected-languages.png)

   - <span data-ttu-id="c46df-344">**Nom d’affichage**: Personnalisez le nom d’affichage de l’expéditeur utilisé dans les notifications de courrier indésirable de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="c46df-344">**Display name**: Customize the sender's display name that's used in end-user spam notifications.</span></span>

     <span data-ttu-id="c46df-345">Pour chaque langue que vous avez ajoutée, sélectionnez la langue dans la seconde langue (ne cliquez pas sur le X) et entrez la valeur de texte souhaitée dans la zone **nom complet** .</span><span class="sxs-lookup"><span data-stu-id="c46df-345">For each language that you've added, select the language in the second language box (don't click on the X) and enter the text value you want in the **Display name** box.</span></span>

     <span data-ttu-id="c46df-346">La capture d’écran suivante montre le nom d’affichage personnalisé dans une notification de courrier indésirable de l’utilisateur final :</span><span class="sxs-lookup"><span data-stu-id="c46df-346">The following screenshot shows the customized display name in an end-user spam notification:</span></span>

     ![Nom d’affichage personnalisé de l’expéditeur dans une notification de courrier indésirable pour l’utilisateur final](../../media/quarantine-tags-esn-customization-display-name.png)

   - <span data-ttu-id="c46df-348">**Clause d’exclusion** de responsabilité : ajoutez une clause d’exclusion de responsabilité personnalisée au bas des notifications de courrier indésirable de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="c46df-348">**Disclaimer**: Add a custom disclaimer to the bottom of end-user spam notifications.</span></span> <span data-ttu-id="c46df-349">Le texte localisé, **une clause d’exclusion de responsabilité de votre organisation :** est toujours inclus en premier, suivi du texte que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="c46df-349">The localized text, **A disclaimer from your organization:** is always included first, followed by the text you specify.</span></span>

     <span data-ttu-id="c46df-350">Pour chaque langue que vous avez ajoutée, sélectionnez la langue dans la deuxième langue (ne cliquez pas sur X) et entrez la valeur de texte souhaitée dans la zone **exclusion de responsabilité** .</span><span class="sxs-lookup"><span data-stu-id="c46df-350">For each language that you've added, select the language in the second language box  (don't click the X) and enter the text value you want in the **Disclaimer** box.</span></span>

     <span data-ttu-id="c46df-351">La capture d’écran suivante montre la clause d’exclusion de responsabilité personnalisée dans une notification de courrier indésirable de l’utilisateur final :</span><span class="sxs-lookup"><span data-stu-id="c46df-351">The following screenshot shows the customized disclaimer in an end-user spam notification:</span></span>

     ![Une clause d’exclusion de responsabilité personnalisée au bas d’une notification de courrier indésirable de l’utilisateur final](../../media/quarantine-tags-esn-customization-disclaimer.png)

## <a name="view-quarantine-tags-in-the-security--compliance-center"></a><span data-ttu-id="c46df-353">Afficher les balises de mise en quarantaine dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="c46df-353">View quarantine tags in the Security & Compliance Center</span></span>

1. <span data-ttu-id="c46df-354">Dans le centre de sécurité & conformité, accédez à stratégie de **gestion des menaces** , \>  puis sélectionnez **balises de mise en quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="c46df-354">In the Security & Compliance Center, go to **Threat management** \> **Policy** and then select **Quarantine tags**.</span></span>

- <span data-ttu-id="c46df-355">Pour afficher les paramètres des balises de mise en quarantaine prédéfinies ou personnalisées, sélectionnez la balise de mise en quarantaine dans la liste (n’activez pas la case à cocher).</span><span class="sxs-lookup"><span data-stu-id="c46df-355">To view the settings of built-in or custom quarantine tags, select the quarantine tag from the list (don't select the check box).</span></span>

- <span data-ttu-id="c46df-356">Pour afficher les paramètres globaux, sélectionnez **paramètres globaux** .</span><span class="sxs-lookup"><span data-stu-id="c46df-356">To view the global settings, select **Global settings**</span></span>

### <a name="view-quarantine-tags-in-powershell"></a><span data-ttu-id="c46df-357">Afficher les balises de mise en quarantaine dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="c46df-357">View quarantine tags in PowerShell</span></span>

<span data-ttu-id="c46df-358">Si vous préférez utiliser PowerShell pour afficher les balises de mise en quarantaine, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c46df-358">If you'd rather use PowerShell to view quarantine tags, do any of the following steps:</span></span>

- <span data-ttu-id="c46df-359">Pour afficher la liste récapitulative de toutes les balises prédéfinies ou personnalisées, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c46df-359">To view a summary list of all built-in or custom tags, run the following command:</span></span>

  ```powershell
  Get-QuarantineTag | Format-Table Name
  ```

- <span data-ttu-id="c46df-360">Pour afficher les paramètres des balises de mise en quarantaine prédéfinies ou personnalisées, remplacez \<TagName\> par le nom de la balise de mise en quarantaine, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c46df-360">To view the settings of built-in or custom quarantine tags, replace \<TagName\> with the name of the quarantine tag, and run the following command:</span></span>

  ```powershell
  Get-QuarantineTag -Identity "<TagName>"
  ```

- <span data-ttu-id="c46df-361">Pour afficher les paramètres globaux, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c46df-361">To view the global settings, run the following command:</span></span>

  ```powershell
  Get-QuarantineTag -QuarantineTagType GlobalQuarantineTag
  ```

<span data-ttu-id="c46df-362">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/get-hostedcontentfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="c46df-362">For detailed syntax and parameter information, see [Get-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/get-hostedcontentfilterpolicy).</span></span>

## <a name="remove-quarantine-tags-in-the-security--compliance-center"></a><span data-ttu-id="c46df-363">Supprimer les balises de mise en quarantaine dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="c46df-363">Remove quarantine tags in the Security & Compliance Center</span></span>

<span data-ttu-id="c46df-364">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="c46df-364">**Notes**:</span></span>

- <span data-ttu-id="c46df-365">Vous ne pouvez pas supprimer les balises de quarantaine prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="c46df-365">You can't remove built-in quarantine tags.</span></span>

- <span data-ttu-id="c46df-366">Avant de supprimer une balise de mise en quarantaine personnalisée, vérifiez qu’elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c46df-366">Before you remove a custom quarantine tag, verify that it's not being used.</span></span> <span data-ttu-id="c46df-367">Par exemple, exécutez la commande suivante dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="c46df-367">For example, run the following command in PowerShell:</span></span>

  ```powershell
  Get-HostedContentFilterPolicy | Format-List Name,*QuarantineTag
  ```

  <span data-ttu-id="c46df-368">Si la balise de mise en quarantaine est utilisée, [Remplacez la balise de mise en quarantaine affectée avant de la](#step-2-assign-a-quarantine-tag-to-supported-features) supprimer.</span><span class="sxs-lookup"><span data-stu-id="c46df-368">If the quarantine tag is being used, [replace the assigned quarantine tag](#step-2-assign-a-quarantine-tag-to-supported-features) before you remove it.</span></span>

1. <span data-ttu-id="c46df-369">Dans le centre de sécurité & conformité, accédez à stratégie de **gestion des menaces** , \>  puis sélectionnez **balises de mise en quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="c46df-369">In the Security & Compliance Center, go to **Threat management** \> **Policy** and then select **Quarantine tags**.</span></span>

2. <span data-ttu-id="c46df-370">Sur la page **balises de quarantaine** , sélectionnez la balise de mise en quarantaine personnalisée que vous souhaitez supprimer, puis cliquez sur **Supprimer la balise**.</span><span class="sxs-lookup"><span data-stu-id="c46df-370">On the **Quarantine tags** page, select the custom quarantine tag that you want to remove, and the click **Delete tag**.</span></span>

3. <span data-ttu-id="c46df-371">Cliquez sur **Supprimer la balise** dans la boîte de dialogue de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c46df-371">Click **Remove tag** in the confirmation dialog that appears.</span></span>

### <a name="remove-quarantine-tags-in-powershell"></a><span data-ttu-id="c46df-372">Supprimer les balises de mise en quarantaine dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="c46df-372">Remove quarantine tags in PowerShell</span></span>

<span data-ttu-id="c46df-373">Si vous préférez utiliser PowerShell pour supprimer une balise de mise en quarantaine personnalisée, remplacez \<TagName\> par le nom de la balise de mise en quarantaine, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c46df-373">If you'd rather use PowerShell to remove a custom quarantine tag, replace \<TagName\> with the name of the quarantine tag, and run the following command:</span></span>

```powershell
Remove-QuarantineTag -Identity "<TagName>"
```

<span data-ttu-id="c46df-374">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/remove-quarantinetag).</span><span class="sxs-lookup"><span data-stu-id="c46df-374">For detailed syntax and parameter information, see [Remove-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/remove-quarantinetag).</span></span>

## <a name="quarantine-tag-permission-details"></a><span data-ttu-id="c46df-375">Détails des autorisations de la balise de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="c46df-375">Quarantine tag permission details</span></span>

<span data-ttu-id="c46df-376">Les sections suivantes décrivent les effets des groupes d’autorisations prédéfinis et des autorisations individuelles dans les détails des messages mis en quarantaine et dans les notifications de courrier indésirable de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="c46df-376">The following sections describe the effects of preset permission groups and individual permissions in the details of quarantined messages and in end-user spam notifications.</span></span>

### <a name="preset-permissions-groups"></a><span data-ttu-id="c46df-377">Groupes d’autorisations prédéfinis</span><span class="sxs-lookup"><span data-stu-id="c46df-377">Preset permissions groups</span></span>

<span data-ttu-id="c46df-378">Les autorisations individuelles qui sont incluses dans des groupes d’autorisations prédéfinis sont répertoriées dans le tableau au début de cet article.</span><span class="sxs-lookup"><span data-stu-id="c46df-378">The individual permissions that are included in preset permission groups are listed in the table at the beginning of this article.</span></span>

#### <a name="no-access"></a><span data-ttu-id="c46df-379">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="c46df-379">No access</span></span>

<span data-ttu-id="c46df-380">Si la balise de mise en quarantaine affecte les autorisations **aucune** autorisation (aucune autorisation), les utilisateurs reçoivent toujours des fonctionnalités de ligne de base :</span><span class="sxs-lookup"><span data-stu-id="c46df-380">If the quarantine tag assigns the **No access** permissions (no permissions), users still get some baseline capabilities:</span></span>

- <span data-ttu-id="c46df-381">**Détails du message en quarantaine**: le bouton d' **en-tête afficher le message** est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-381">**Quarantined message details**: The **View message header** button is always available.</span></span>

  ![Boutons disponibles dans les détails du message en quarantaine si la balise de mise en quarantaine donne à l’utilisateur aucune autorisation d’accès](../../media/quarantine-tags-quarantined-message-details-no-access.png)

- <span data-ttu-id="c46df-383">**Notifications de courrier indésirable de l’utilisateur final**: le bouton **Review** qui dirige l’utilisateur vers le message en quarantaine est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-383">**End-user spam notifications**: The **Review** button that takes the user to the message in quarantine is always available.</span></span>

  ![Boutons disponibles dans la notification de courrier indésirable de l’utilisateur final si la balise de mise en quarantaine donne à l’utilisateur aucune autorisation d’accès](../../media/quarantine-tags-esn-no-access.png)

#### <a name="limited-access"></a><span data-ttu-id="c46df-385">Accès limité</span><span class="sxs-lookup"><span data-stu-id="c46df-385">Limited access</span></span>

<span data-ttu-id="c46df-386">Si la balise de mise en quarantaine affecte les autorisations d' **accès limitées** , les utilisateurs obtiennent les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="c46df-386">If the quarantine tag assigns the **Limited access** permissions, users get the following capabilities:</span></span>

- <span data-ttu-id="c46df-387">**Détails du message en quarantaine**: les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="c46df-387">**Quarantined message details**: The following buttons are available:</span></span>
  - <span data-ttu-id="c46df-388">**Version de la demande**</span><span class="sxs-lookup"><span data-stu-id="c46df-388">**Request release**</span></span>
  - <span data-ttu-id="c46df-389">**Afficher l’en-tête du message**</span><span class="sxs-lookup"><span data-stu-id="c46df-389">**View message header**</span></span>
  - <span data-ttu-id="c46df-390">**Aperçu du message**</span><span class="sxs-lookup"><span data-stu-id="c46df-390">**Preview message**</span></span>
  - <span data-ttu-id="c46df-391">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="c46df-391">**Block sender**</span></span>
  - <span data-ttu-id="c46df-392">**Supprimer de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="c46df-392">**Remove from quarantine**</span></span>

  ![Boutons disponibles dans les détails du message en quarantaine si la balise de mise en quarantaine accorde aux utilisateurs des autorisations d’accès limitées](../../media/quarantine-tags-quarantined-message-details-limited-access.png)

- <span data-ttu-id="c46df-394">**Notifications de courrier indésirable de l’utilisateur final**: les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="c46df-394">**End-user spam notifications**: The following buttons are available:</span></span>
  - <span data-ttu-id="c46df-395">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="c46df-395">**Block sender**</span></span>
  - <span data-ttu-id="c46df-396">**Révision**</span><span class="sxs-lookup"><span data-stu-id="c46df-396">**Review**</span></span>

  ![Boutons disponibles dans la notification de courrier indésirable de l’utilisateur final si la balise de mise en quarantaine accorde aux utilisateurs des autorisations d’accès limitées](../../media/quarantine-tags-esn-limited-access.png)

#### <a name="full-access"></a><span data-ttu-id="c46df-398">Accès total</span><span class="sxs-lookup"><span data-stu-id="c46df-398">Full access</span></span>

<span data-ttu-id="c46df-399">Si la balise de mise en quarantaine affecte les autorisations d' **accès total** (toutes les autorisations disponibles), les utilisateurs bénéficient des fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="c46df-399">If the quarantine tag assigns the **Full access** permissions (all available permissions), users get the following capabilities:</span></span>

- <span data-ttu-id="c46df-400">**Détails du message en quarantaine**: les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="c46df-400">**Quarantined message details**: The following buttons are available:</span></span>
  - <span data-ttu-id="c46df-401">**Message de publication**</span><span class="sxs-lookup"><span data-stu-id="c46df-401">**Release message**</span></span>
  - <span data-ttu-id="c46df-402">**Afficher l’en-tête du message**</span><span class="sxs-lookup"><span data-stu-id="c46df-402">**View message header**</span></span>
  - <span data-ttu-id="c46df-403">**Aperçu du message**</span><span class="sxs-lookup"><span data-stu-id="c46df-403">**Preview message**</span></span>
  - <span data-ttu-id="c46df-404">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="c46df-404">**Block sender**</span></span>
  - <span data-ttu-id="c46df-405">**Autoriser l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="c46df-405">**Allow sender**</span></span>
  - <span data-ttu-id="c46df-406">**Supprimer de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="c46df-406">**Remove from quarantine**</span></span>

  ![Boutons disponibles dans les détails du message en quarantaine si la balise de mise en quarantaine accorde à l’utilisateur les autorisations d’accès total](../../media/quarantine-tags-quarantined-message-details-full-access.png)

- <span data-ttu-id="c46df-408">**Notifications de courrier indésirable de l’utilisateur final**: les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="c46df-408">**End-user spam notifications**: The following buttons are available:</span></span>
  - <span data-ttu-id="c46df-409">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="c46df-409">**Block sender**</span></span>
  - <span data-ttu-id="c46df-410">**Version**</span><span class="sxs-lookup"><span data-stu-id="c46df-410">**Release**</span></span>
  - <span data-ttu-id="c46df-411">**Révision**</span><span class="sxs-lookup"><span data-stu-id="c46df-411">**Review**</span></span>

  ![Boutons disponibles dans la notification de courrier indésirable de l’utilisateur final si la balise de mise en quarantaine accorde à l’utilisateur les autorisations d’accès total](../../media/quarantine-tags-esn-full-access.png)

### <a name="individual-permissions"></a><span data-ttu-id="c46df-413">Autorisations individuelles</span><span class="sxs-lookup"><span data-stu-id="c46df-413">Individual permissions</span></span>

> [!NOTE]
> <span data-ttu-id="c46df-414">N’oubliez pas que les utilisateurs reçoivent toujours les boutons décrits dans la section [pas d’accès](#no-access) .</span><span class="sxs-lookup"><span data-stu-id="c46df-414">Remember, users always get the buttons described in the [No access](#no-access) section.</span></span> <span data-ttu-id="c46df-415">Ces boutons ne sont pas inclus dans les descriptions d’autorisation individuelles.</span><span class="sxs-lookup"><span data-stu-id="c46df-415">These buttons are not included in the individual permission descriptions.</span></span>

#### <a name="allow-sender-permission"></a><span data-ttu-id="c46df-416">Autorisation de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="c46df-416">Allow sender permission</span></span>

<span data-ttu-id="c46df-417">L’autorisation **autoriser l’expéditeur** (_PermissionToAllowSender_) contrôle l’accès au bouton qui permet aux utilisateurs d’ajouter facilement l’expéditeur du message en quarantaine à leur liste des expéditeurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="c46df-417">The **Allow sender** permission (_PermissionToAllowSender_) controls access to the button that allows users to conveniently add the quarantined message sender to their Safe Senders list.</span></span>

- <span data-ttu-id="c46df-418">**Détails du message en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="c46df-418">**Quarantined message details**:</span></span>
  - <span data-ttu-id="c46df-419">**Autoriser** l’autorisation de l’expéditeur activé : le bouton **autoriser l’expéditeur** est disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-419">**Allow sender** permission enabled: The **Allow sender** button is available.</span></span>
  - <span data-ttu-id="c46df-420">**Autoriser l’expéditeur** désactivé : le bouton **autoriser l’expéditeur** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-420">**Allow sender** permission disabled: The **Allow sender** button is not available.</span></span>

- <span data-ttu-id="c46df-421">**Notifications de courrier indésirable de l’utilisateur final**: aucun effet.</span><span class="sxs-lookup"><span data-stu-id="c46df-421">**End-user spam notifications**: No effect.</span></span>

<span data-ttu-id="c46df-422">Pour plus d’informations sur la liste des expéditeurs approuvés, voir [empêcher le blocage des expéditeurs approuvés](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379666) et [utiliser Exchange Online PowerShell pour configurer la collection de listes fiables sur une boîte aux lettres](configure-junk-email-settings-on-exo-mailboxes.md#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox).</span><span class="sxs-lookup"><span data-stu-id="c46df-422">For more information about the Safe Senders list, see [Prevent trusted senders from being blocked](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379666) and [Use Exchange Online PowerShell to configure the safelist collection on a mailbox](configure-junk-email-settings-on-exo-mailboxes.md#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox).</span></span>

#### <a name="block-sender-permission"></a><span data-ttu-id="c46df-423">Autorisation bloquer l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="c46df-423">Block sender permission</span></span>

<span data-ttu-id="c46df-424">L’autorisation **proscrire l’expéditeur** (_PermissionToBlockSender_) contrôle l’accès au bouton qui permet aux utilisateurs d’ajouter facilement l’expéditeur du message en quarantaine à la liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="c46df-424">The **Block sender** permission (_PermissionToBlockSender_) controls access to the button that allows users to conveniently add the quarantined message sender to their Blocked Senders list.</span></span>

- <span data-ttu-id="c46df-425">**Détails du message en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="c46df-425">**Quarantined message details**:</span></span>
  - <span data-ttu-id="c46df-426">Autorisation de blocage de l' **expéditeur** activée : le bouton **bloquer l’expéditeur** est disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-426">**Block sender** permission enabled: The **Block sender** button is available.</span></span>
  - <span data-ttu-id="c46df-427">Autorisation de blocage de l' **expéditeur** désactivée : le bouton **bloquer l’expéditeur** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-427">**Block sender** permission disabled: The **Block sender** button is not available.</span></span>

- <span data-ttu-id="c46df-428">**Notifications de courrier indésirable de l’utilisateur final**:</span><span class="sxs-lookup"><span data-stu-id="c46df-428">**End-user spam notifications**:</span></span>
  - <span data-ttu-id="c46df-429">Autorisation de blocage de l' **expéditeur** désactivée : le bouton **bloquer l’expéditeur** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-429">**Block sender** permission disabled: The **Block sender** button is not available.</span></span>
  - <span data-ttu-id="c46df-430">Autorisation de blocage de l' **expéditeur** activée : le bouton **bloquer l’expéditeur** est disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-430">**Block sender** permission enabled: The **Block sender** button is available.</span></span>

<span data-ttu-id="c46df-431">Pour plus d’informations sur la liste des expéditeurs bloqués, voir [bloquer les messages de quelqu’un](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379667) et [utiliser Exchange Online PowerShell pour configurer la collection de listes fiables sur une boîte aux lettres](configure-junk-email-settings-on-exo-mailboxes.md#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox).</span><span class="sxs-lookup"><span data-stu-id="c46df-431">For more information about the Blocked Senders list, see [Block messages from someone](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379667) and [Use Exchange Online PowerShell to configure the safelist collection on a mailbox](configure-junk-email-settings-on-exo-mailboxes.md#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox).</span></span>

#### <a name="delete-permission"></a><span data-ttu-id="c46df-432">Supprimer une autorisation</span><span class="sxs-lookup"><span data-stu-id="c46df-432">Delete permission</span></span>

<span data-ttu-id="c46df-433">L’autorisation de **suppression** (_PermissionToDelete_) contrôle la possibilité pour les utilisateurs de supprimer leurs messages (messages dans lesquels l’utilisateur est un destinataire) de la mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c46df-433">The **Delete** permission (_PermissionToDelete_) controls the ability to of users to delete their messages (messages where the user is a recipient) from quarantine.</span></span>

- <span data-ttu-id="c46df-434">**Détails du message en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="c46df-434">**Quarantined message details**:</span></span>
  - <span data-ttu-id="c46df-435">Autorisation de **suppression** activée : le bouton **supprimer de la quarantaine** est disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-435">**Delete** permission enabled: The **Remove from quarantine** button is available.</span></span>
  - <span data-ttu-id="c46df-436">Autorisation de **suppression** désactivée : le bouton **supprimer du contrôle** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-436">**Delete** permission disabled: The **Remove from quarantine** button is not available.</span></span>

- <span data-ttu-id="c46df-437">**Notifications de courrier indésirable de l’utilisateur final**: aucun effet.</span><span class="sxs-lookup"><span data-stu-id="c46df-437">**End-user spam notifications**: No effect.</span></span>

#### <a name="preview-permission"></a><span data-ttu-id="c46df-438">Autorisation d’aperçu</span><span class="sxs-lookup"><span data-stu-id="c46df-438">Preview permission</span></span>

<span data-ttu-id="c46df-439">L’autorisation **preview** (_PermissionToPreview_) contrôle la possibilité pour les utilisateurs de prévisualiser leurs messages en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c46df-439">The **Preview** permission (_PermissionToPreview_) controls the ability to of users to preview their messages in quarantine.</span></span>

- <span data-ttu-id="c46df-440">**Détails du message en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="c46df-440">**Quarantined message details**:</span></span>
  - <span data-ttu-id="c46df-441">Autorisation d' **Aperçu** activée : le bouton **Aperçu du message** est disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-441">**Preview** permission enabled: The **Preview message** button is available.</span></span>
  - <span data-ttu-id="c46df-442">Autorisation d' **Aperçu** désactivée : le bouton **Aperçu du message** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-442">**Preview** permission disabled: The **Preview message** button is not available.</span></span>

- <span data-ttu-id="c46df-443">**Notifications de courrier indésirable de l’utilisateur final**: aucun effet.</span><span class="sxs-lookup"><span data-stu-id="c46df-443">**End-user spam notifications**: No effect.</span></span>

#### <a name="allow-recipients-to-release-a-message-from-quarantine-permission"></a><span data-ttu-id="c46df-444">Autoriser les destinataires à libérer un message à partir de l’autorisation de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="c46df-444">Allow recipients to release a message from quarantine permission</span></span>

<span data-ttu-id="c46df-445">L’autorisation **autoriser les destinataires à libérer un message à partir de la quarantaine** (_PermissionToRelease_) contrôle la capacité des utilisateurs à libérer leurs messages mis en quarantaine directement et sans l’approbation d’un administrateur.</span><span class="sxs-lookup"><span data-stu-id="c46df-445">The **Allow recipients to release a message from quarantine** permission (_PermissionToRelease_) controls the ability of users to release their quarantined messages directly and without the approval of an admin.</span></span>

- <span data-ttu-id="c46df-446">**Détails du message en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="c46df-446">**Quarantined message details**:</span></span>
  - <span data-ttu-id="c46df-447">Autorisation activée : le bouton **diffuser le message** est disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-447">Permission enabled: The **Release message** button is available.</span></span>
  - <span data-ttu-id="c46df-448">Autorisation désactivée : le bouton **diffuser le message** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-448">Permission disabled: The **Release message** button is not available.</span></span>

- <span data-ttu-id="c46df-449">**Notifications de courrier indésirable de l’utilisateur final**:</span><span class="sxs-lookup"><span data-stu-id="c46df-449">**End-user spam notifications**:</span></span>
  - <span data-ttu-id="c46df-450">Autorisation activée : le bouton de **publication** est disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-450">Permission enabled: The **Release** button is available.</span></span>
  - <span data-ttu-id="c46df-451">Autorisation désactivée : le bouton de **publication** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-451">Permission disabled: The **Release** button is not available.</span></span>

#### <a name="allow-recipients-to-request-a-message-to-be-released-from-quarantine-permission"></a><span data-ttu-id="c46df-452">Autoriser les destinataires à demander la libération d’un message à partir de l’autorisation de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="c46df-452">Allow recipients to request a message to be released from quarantine permission</span></span>

<span data-ttu-id="c46df-453">L’option **autoriser les destinataires à demander la libération d’un message à partir de l’autorisation de mise en quarantaine** (_PermissionToRequestRelease_) contrôle la capacité des utilisateurs à _demander_ la libération de leurs messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c46df-453">The **Allow recipients to request a message to be released from quarantine** permission (_PermissionToRequestRelease_) controls the ability of users to _request_ the release of their quarantined messages.</span></span> <span data-ttu-id="c46df-454">Le message n’est publié qu’après qu’un administrateur a approuvé la demande.</span><span class="sxs-lookup"><span data-stu-id="c46df-454">The message is only released after an admin approves the request.</span></span>

- <span data-ttu-id="c46df-455">**Détails du message en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="c46df-455">**Quarantined message details**:</span></span>
  - <span data-ttu-id="c46df-456">Autorisation activée : le bouton de lancement de la **demande** est disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-456">Permission enabled: The **Request release** button is available.</span></span>
  - <span data-ttu-id="c46df-457">Autorisation désactivée : le bouton de libération de la **demande** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-457">Permission disabled: The **Request release** button is not available.</span></span>

- <span data-ttu-id="c46df-458">**Notifications de courrier indésirable de l’utilisateur final**: le bouton de **publication** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c46df-458">**End-user spam notifications**: The **Release** button is not available.</span></span>
