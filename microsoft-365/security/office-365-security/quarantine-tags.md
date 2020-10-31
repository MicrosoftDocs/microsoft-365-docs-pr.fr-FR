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
ms.openlocfilehash: 557a6832807c1768f482e76c76c0e92b027e49a7
ms.sourcegitcommit: 2810d1347e5016412074b2dd18e654aee7e593de
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2020
ms.locfileid: "48819174"
---
# <a name="quarantine-tags"></a><span data-ttu-id="90095-103">Balises de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="90095-103">Quarantine tags</span></span>

> [!NOTE]
> <span data-ttu-id="90095-104">Les fonctionnalités décrites dans cet article sont actuellement en version préliminaire, ne sont pas disponibles pour tous les utilisateurs et peuvent faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="90095-104">The features that are described in this article are currently in Preview, aren't available to everyone, and are subject to change.</span></span>

<span data-ttu-id="90095-105">Les balises de mise en quarantaine dans Exchange Online Protection (EOP) permettent aux administrateurs de contrôler ce que les utilisateurs peuvent faire de leurs messages mis en quarantaine en fonction de la mise en quarantaine du message.</span><span class="sxs-lookup"><span data-stu-id="90095-105">Quarantine tags in Exchange Online Protection (EOP) allow admins to control what users are able to do to their quarantined messages based on how the message arrived in quarantine.</span></span>

<span data-ttu-id="90095-106">EOP a traditionnellement autorisé ou empêché certains niveaux d’interactivité pour les messages en [quarantaine](find-and-release-quarantined-messages-as-a-user.md) et dans les [notifications de courrier indésirable pour l’utilisateur final](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span><span class="sxs-lookup"><span data-stu-id="90095-106">EOP has traditionally allowed or prevented certain levels of interactivity for messages in [quarantine](find-and-release-quarantined-messages-as-a-user.md) and in [end-user spam notifications](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span> <span data-ttu-id="90095-107">Par exemple, les utilisateurs finaux peuvent afficher et libérer les messages qui ont été mis en quarantaine par le filtrage du courrier indésirable en tant que courrier indésirable ou en bloc, mais ils ne peuvent pas afficher ou libérer les messages mis en quarantaine en tant que phishing à haut niveau de fiabilité.</span><span class="sxs-lookup"><span data-stu-id="90095-107">For example, end-users can view and release messages that were quarantined by anti-spam filtering as spam or bulk, but they can't view or release messages that were quarantined as high confidence phishing.</span></span>

<span data-ttu-id="90095-108">Pour les [fonctionnalités de protection prises en charge](#step-2-assign-a-quarantine-tag-to-supported-features), les balises de mise en quarantaine spécifient ce que les utilisateurs sont autorisés à faire dans les messages de notification de courrier indésirable de l’utilisateur final et dans les messages mis en quarantaine (messages dans lesquels l’utilisateur est un destinataire).</span><span class="sxs-lookup"><span data-stu-id="90095-108">For [supported protection features](#step-2-assign-a-quarantine-tag-to-supported-features), quarantine tags specify what users are allowed to do in end-user spam notification messages and in their quarantined messages in quarantine (messages where the user is a recipient).</span></span> <span data-ttu-id="90095-109">Les balises de mise en quarantaine par défaut sont automatiquement attribuées pour appliquer les fonctionnalités d’historique pour les utilisateurs finaux sur les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="90095-109">Default quarantine tags are automatically assigned to enforce the historical capabilities for end-users on quarantined messages.</span></span> <span data-ttu-id="90095-110">Vous pouvez créer et affecter des balises de mise en quarantaine personnalisées pour autoriser ou empêcher les utilisateurs finals d’effectuer des actions spécifiques sur les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="90095-110">Or, you can create and assign custom quarantine tags to allow or prevent end-users from performing specific actions on quarantined messages.</span></span>

<span data-ttu-id="90095-111">Les autorisations individuelles sont combinées dans les groupes d’autorisations prédéfinis suivants :</span><span class="sxs-lookup"><span data-stu-id="90095-111">The individual permissions are combined into the following preset permission groups:</span></span>

- <span data-ttu-id="90095-112">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="90095-112">No access</span></span>
- <span data-ttu-id="90095-113">Accès limité</span><span class="sxs-lookup"><span data-stu-id="90095-113">Limited access</span></span>
- <span data-ttu-id="90095-114">Accès total</span><span class="sxs-lookup"><span data-stu-id="90095-114">Full access</span></span>

<span data-ttu-id="90095-115">Les autorisations individuelles disponibles et ce qui est inclus ou non dans les groupes d’autorisations prédéfinis sont décrits dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="90095-115">The available individual permissions and what's included or not included in the preset permission groups are described in the following table:</span></span>

|<span data-ttu-id="90095-116">Autorisation</span><span class="sxs-lookup"><span data-stu-id="90095-116">Permission</span></span>|<span data-ttu-id="90095-117">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="90095-117">No access</span></span>|<span data-ttu-id="90095-118">Accès limité</span><span class="sxs-lookup"><span data-stu-id="90095-118">Limited access</span></span>|<span data-ttu-id="90095-119">Accès total</span><span class="sxs-lookup"><span data-stu-id="90095-119">Full access</span></span>|
|---|:---:|:---:|:---:|
|<span data-ttu-id="90095-120">**Autoriser l’expéditeur** ( _PermissionToAllowSender_ )</span><span class="sxs-lookup"><span data-stu-id="90095-120">**Allow sender** ( _PermissionToAllowSender_ )</span></span>|||![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="90095-122">**Bloquer l’expéditeur** ( _PermissionToBlockSender_ )</span><span class="sxs-lookup"><span data-stu-id="90095-122">**Block sender** ( _PermissionToBlockSender_ )</span></span>||![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="90095-125">**Supprimer** ( _PermissionToDelete_ )</span><span class="sxs-lookup"><span data-stu-id="90095-125">**Delete** ( _PermissionToDelete_ )</span></span>||![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="90095-128">**Aperçu** ( _PermissionToPreview_ )</span><span class="sxs-lookup"><span data-stu-id="90095-128">**Preview** ( _PermissionToPreview_ )</span></span>||![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="90095-131">**Autoriser les destinataires à libérer un message en quarantaine** ( _PermissionToRelease_ )</span><span class="sxs-lookup"><span data-stu-id="90095-131">**Allow recipients to release a message from quarantine** ( _PermissionToRelease_ )</span></span>|||![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="90095-133">**Autoriser les destinataires à demander la libération d’un message en quarantaine** ( _PermissionToRequestRelease_ )</span><span class="sxs-lookup"><span data-stu-id="90095-133">**Allow recipients to request a message to be released from quarantine** ( _PermissionToRequestRelease_ )</span></span>||![Coche](../../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
|

<span data-ttu-id="90095-135">Si vous n’aimez pas les autorisations par défaut dans les groupes d’autorisations prédéfinis, vous pouvez utiliser des autorisations personnalisées lors de la création ou de la modification de balises de mise en quarantaine personnalisées.</span><span class="sxs-lookup"><span data-stu-id="90095-135">If you don't like the default permissions in the preset permission groups, you can use custom permissions when you create or modify custom quarantine tags.</span></span> <span data-ttu-id="90095-136">Pour plus d’informations sur ce que fait chaque autorisation, voir la section Détails de l' [autorisation de mise en quarantaine](#quarantine-tag-permission-details) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="90095-136">For more information about what each permission does, see the [Quarantine tag permission details](#quarantine-tag-permission-details) section later in this article.</span></span>

<span data-ttu-id="90095-137">Vous créez et attribuez des balises de mise en quarantaine dans le centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres Exchange Online ; environnement EOP autonome dans les organisations EOP sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="90095-137">You create and assign quarantine tags in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with Exchange Online Mailboxes; standalone EOP PowerShell in EOP organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="90095-138">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="90095-138">What do you need to know before you begin?</span></span>

- <span data-ttu-id="90095-139">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="90095-139">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="90095-140">Pour accéder directement à la page **balises de quarantaine** , ouvrez <https://protection.office.com/quarantineTags> .</span><span class="sxs-lookup"><span data-stu-id="90095-140">To go directly to the **Quarantine tags** page, open <https://protection.office.com/quarantineTags>.</span></span>

- <span data-ttu-id="90095-141">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="90095-141">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="90095-142">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="90095-142">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="90095-143">Pour afficher, créer, modifier ou supprimer des balises de mise en quarantaine, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="90095-143">To view, create, modify, or remove quarantine tags, you need to be a member of one of the following role groups:</span></span>
  - <span data-ttu-id="90095-144">**Gestion de l’organisation** ou **Administrateur de sécurité** dans le [Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="90095-144">**Organization Management** or **Security Administrator** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  - <span data-ttu-id="90095-145">**Gestion de l’organisation** ou **Gestion de l’hygiène** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="90095-145">**Organization Management** or **Hygiene Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

## <a name="step-1-create-quarantine-tags-in-the-security--compliance-center"></a><span data-ttu-id="90095-146">Étape 1 : créer des balises de mise en quarantaine dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="90095-146">Step 1: Create quarantine tags in the Security & Compliance Center</span></span>

1. <span data-ttu-id="90095-147">Dans le centre de sécurité & conformité, accédez à stratégie de **gestion des menaces** , \> **Policy** puis sélectionnez **balises de mise en quarantaine** .</span><span class="sxs-lookup"><span data-stu-id="90095-147">In the Security & Compliance Center, go to **Threat management** \> **Policy** and then select **Quarantine tags** .</span></span>

2. <span data-ttu-id="90095-148">Sur la page **balises de quarantaine** , sélectionnez **Ajouter une balise personnalisée** .</span><span class="sxs-lookup"><span data-stu-id="90095-148">On the **Quarantine tags** page, select **Add custom tag** .</span></span>

3. <span data-ttu-id="90095-149">L’Assistant **nouvelle balise** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="90095-149">The **New tag** wizard opens.</span></span> <span data-ttu-id="90095-150">Dans la page nom de la **balise** , entrez un bref nom unique dans le champ nom de la **balise** .</span><span class="sxs-lookup"><span data-stu-id="90095-150">On the **Tag name** page, enter a brief but unique name in the **Tag name** field.</span></span> <span data-ttu-id="90095-151">Vous devrez identifier et sélectionner la balise par nom dans les étapes à venir.</span><span class="sxs-lookup"><span data-stu-id="90095-151">You'll need to identify and select the tag by name in upcoming steps.</span></span> <span data-ttu-id="90095-152">Lorsque vous avez terminé, cliquez sur **Suivant** .</span><span class="sxs-lookup"><span data-stu-id="90095-152">When you're finished, click **Next** .</span></span>

4. <span data-ttu-id="90095-153">Sur la page **accès aux messages des destinataires** , sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="90095-153">On the **Recipient message access** page, select one of the following values:</span></span>
   - <span data-ttu-id="90095-154">**Aucun accès**</span><span class="sxs-lookup"><span data-stu-id="90095-154">**No access**</span></span>
   - <span data-ttu-id="90095-155">**Accès limité**</span><span class="sxs-lookup"><span data-stu-id="90095-155">**Limited access**</span></span>
   - <span data-ttu-id="90095-156">**Accès total**</span><span class="sxs-lookup"><span data-stu-id="90095-156">**Full access**</span></span>

   <span data-ttu-id="90095-157">Les autorisations individuelles qui sont incluses dans ces groupes d’autorisations sont décrites plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="90095-157">The individual permissions that are included in these permission groups are described earlier in this article.</span></span>

   <span data-ttu-id="90095-158">Pour spécifier des autorisations personnalisées, sélectionnez **définir un accès spécifique (avancé)** et configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="90095-158">To specify custom permissions, select **Set specific access (Advanced)** and configure the following settings:</span></span>

     - <span data-ttu-id="90095-159">**Sélectionnez la préférence** de l’action de publication : sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="90095-159">**Select release action preference** : Select one of the following values:</span></span>
       - <span data-ttu-id="90095-160">**Aucune action de libération** : il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="90095-160">**No release action** : This is the default value.</span></span>
       - <span data-ttu-id="90095-161">**Autoriser les destinataires à diffuser un message en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="90095-161">**Allow recipients to release a message from quarantine**</span></span>
       - <span data-ttu-id="90095-162">**Autoriser les destinataires à demander la libération d’un message en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="90095-162">**Allow recipients to request a message to be released from quarantine**</span></span>

     - <span data-ttu-id="90095-163">**Sélectionnez les actions supplémentaires que les destinataires peuvent effectuer sur les messages mis en quarantaine** : sélectionnez certaines, toutes ou aucune des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="90095-163">**Select additional actions recipients can take on quarantined messages** : Select some, all, or none of the following values:</span></span>
       - <span data-ttu-id="90095-164">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="90095-164">**Delete**</span></span>
       - <span data-ttu-id="90095-165">**Aperçu**</span><span class="sxs-lookup"><span data-stu-id="90095-165">**Preview**</span></span>
       - <span data-ttu-id="90095-166">**Autoriser l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="90095-166">**Allow sender**</span></span>
       - <span data-ttu-id="90095-167">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="90095-167">**Block sender**</span></span>

   <span data-ttu-id="90095-168">Ces autorisations et leur effet sur les messages mis en quarantaine et les notifications de courrier indésirable de l’utilisateur final sont décrits dans la section Détails des autorisations de la [balise de mise en quarantaine](#quarantine-tag-permission-details) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="90095-168">These permissions and their effect on quarantined messages and in end-user spam notifications are described in the [Quarantine tag permission details](#quarantine-tag-permission-details) section later in this article.</span></span>

   <span data-ttu-id="90095-169">Lorsque vous avez terminé, cliquez sur **Suivant** .</span><span class="sxs-lookup"><span data-stu-id="90095-169">When you're finished, click **Next** .</span></span>

5. <span data-ttu-id="90095-170">Sur la page **récapitulative** qui s’affiche, vérifiez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="90095-170">On the **Summary** page that appears, review your settings.</span></span> <span data-ttu-id="90095-171">Vous pouvez cliquer sur **modifier** sur chaque paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="90095-171">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="90095-172">Lorsque vous avez terminé, cliquez sur **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="90095-172">When you're finished, click **Submit** .</span></span>

6. <span data-ttu-id="90095-173">Cliquez sur **OK** dans la page de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="90095-173">Click **Done** on the confirmation page that appears.</span></span>

<span data-ttu-id="90095-174">Vous êtes maintenant prêt à affecter la balise de mise en quarantaine à une fonctionnalité de mise en quarantaine, comme décrit dans la section [étape 2](#step-2-assign-a-quarantine-tag-to-supported-features) .</span><span class="sxs-lookup"><span data-stu-id="90095-174">Now you are ready to assign the quarantine tag to a quarantine feature as described in the [Step 2](#step-2-assign-a-quarantine-tag-to-supported-features) section.</span></span>

### <a name="create-quarantine-tags-in-powershell"></a><span data-ttu-id="90095-175">Créer des balises de mise en quarantaine dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="90095-175">Create quarantine tags in PowerShell</span></span>

<span data-ttu-id="90095-176">Si vous préférez utiliser PowerShell pour créer des balises de mise en quarantaine, connectez-vous à Exchange Online PowerShell ou à Exchange Online Protection PowerShell et utilisez la cmdlet **New-QuarantineTag** .</span><span class="sxs-lookup"><span data-stu-id="90095-176">If you'd rather use PowerShell to create quarantine tags, connect to Exchange Online PowerShell or Exchange Online Protection PowerShell and use the **New-QuarantineTag** cmdlet.</span></span> <span data-ttu-id="90095-177">Vous avez le choix entre deux méthodes :</span><span class="sxs-lookup"><span data-stu-id="90095-177">You have two different methods to choose from:</span></span>

- <span data-ttu-id="90095-178">Utilisez le paramètre _EndUserQuarantinePermissionsValue_ .</span><span class="sxs-lookup"><span data-stu-id="90095-178">Use the _EndUserQuarantinePermissionsValue_ parameter.</span></span>
- <span data-ttu-id="90095-179">Utilisez le paramètre _EndUserQuarantinePermissions_ .</span><span class="sxs-lookup"><span data-stu-id="90095-179">Use the _EndUserQuarantinePermissions_ parameter.</span></span>

<span data-ttu-id="90095-180">Ces méthodes sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="90095-180">These methods are described in the following sections.</span></span>

#### <a name="use-the-enduserquarantinepermissionsvalue-parameter"></a><span data-ttu-id="90095-181">Utiliser le paramètre EndUserQuarantinePermissionsValue</span><span class="sxs-lookup"><span data-stu-id="90095-181">Use the EndUserQuarantinePermissionsValue parameter</span></span>

<span data-ttu-id="90095-182">Pour créer une balise de mise en quarantaine à l’aide du paramètre _EndUserQuarantinePermissionsValue_ , utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="90095-182">To create a quarantine tag using the _EndUserQuarantinePermissionsValue_ parameter, use the following syntax:</span></span>

```powershell
New-QuarantineTag -Name "<UniqueName>" -EndUserQuarantinePermissionsValue <0 to 236>
```

<span data-ttu-id="90095-183">Le paramètre _EndUserQuarantinePermissionsValue_ utilise une valeur décimale qui est convertie à partir d’une valeur binaire.</span><span class="sxs-lookup"><span data-stu-id="90095-183">The _EndUserQuarantinePermissionsValue_ parameter uses a decimal value that's converted from a binary value.</span></span> <span data-ttu-id="90095-184">La valeur binaire correspond aux autorisations de mise en quarantaine de l’utilisateur final disponibles dans un ordre spécifique.</span><span class="sxs-lookup"><span data-stu-id="90095-184">The binary value corresponds to the available end-user quarantine permissions in a specific order.</span></span> <span data-ttu-id="90095-185">Pour chaque autorisation, la valeur 1 est égale à true et la valeur 0 équivaut à false.</span><span class="sxs-lookup"><span data-stu-id="90095-185">For each permission, the value 1 equals True and the value 0 equals False.</span></span>

<span data-ttu-id="90095-186">L’ordre et les valeurs requis pour chaque autorisation individuelle dans des groupes d’autorisations prédéfinis sont décrits dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="90095-186">The required order and values for each individual permission in preset permission groups are described in the following table:</span></span>

****

|<span data-ttu-id="90095-187">Autorisation</span><span class="sxs-lookup"><span data-stu-id="90095-187">Permission</span></span>|<span data-ttu-id="90095-188">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="90095-188">No access</span></span>|<span data-ttu-id="90095-189">Accès limité</span><span class="sxs-lookup"><span data-stu-id="90095-189">Limited access</span></span>|<span data-ttu-id="90095-190">Accès total</span><span class="sxs-lookup"><span data-stu-id="90095-190">Full access</span></span>|
|---|:---:|:---:|:---:|
|<span data-ttu-id="90095-191">PermissionToAllowSender</span><span class="sxs-lookup"><span data-stu-id="90095-191">PermissionToAllowSender</span></span>|<span data-ttu-id="90095-192">0</span><span class="sxs-lookup"><span data-stu-id="90095-192">0</span></span>|<span data-ttu-id="90095-193">0</span><span class="sxs-lookup"><span data-stu-id="90095-193">0</span></span>|<span data-ttu-id="90095-194">0,1</span><span class="sxs-lookup"><span data-stu-id="90095-194">1</span></span>|
|<span data-ttu-id="90095-195">PermissionToBlockSender</span><span class="sxs-lookup"><span data-stu-id="90095-195">PermissionToBlockSender</span></span>|<span data-ttu-id="90095-196">0</span><span class="sxs-lookup"><span data-stu-id="90095-196">0</span></span>|<span data-ttu-id="90095-197">0,1</span><span class="sxs-lookup"><span data-stu-id="90095-197">1</span></span>|<span data-ttu-id="90095-198">0,1</span><span class="sxs-lookup"><span data-stu-id="90095-198">1</span></span>|
|<span data-ttu-id="90095-199">PermissionToDelete</span><span class="sxs-lookup"><span data-stu-id="90095-199">PermissionToDelete</span></span>|<span data-ttu-id="90095-200">0</span><span class="sxs-lookup"><span data-stu-id="90095-200">0</span></span>|<span data-ttu-id="90095-201">0,1</span><span class="sxs-lookup"><span data-stu-id="90095-201">1</span></span>|<span data-ttu-id="90095-202">0,1</span><span class="sxs-lookup"><span data-stu-id="90095-202">1</span></span>|
|<span data-ttu-id="90095-203">PermissionToDownload<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90095-203">PermissionToDownload<sup>\*</sup></span></span>|<span data-ttu-id="90095-204">0</span><span class="sxs-lookup"><span data-stu-id="90095-204">0</span></span>|<span data-ttu-id="90095-205">0</span><span class="sxs-lookup"><span data-stu-id="90095-205">0</span></span>|<span data-ttu-id="90095-206">0</span><span class="sxs-lookup"><span data-stu-id="90095-206">0</span></span>|
|<span data-ttu-id="90095-207">PermissionToPreview</span><span class="sxs-lookup"><span data-stu-id="90095-207">PermissionToPreview</span></span>|<span data-ttu-id="90095-208">0</span><span class="sxs-lookup"><span data-stu-id="90095-208">0</span></span>|<span data-ttu-id="90095-209">0,1</span><span class="sxs-lookup"><span data-stu-id="90095-209">1</span></span>|<span data-ttu-id="90095-210">0,1</span><span class="sxs-lookup"><span data-stu-id="90095-210">1</span></span>|
|<span data-ttu-id="90095-211">PermissionToRelease<sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="90095-211">PermissionToRelease<sup>\*\*</sup></span></span>|<span data-ttu-id="90095-212">0</span><span class="sxs-lookup"><span data-stu-id="90095-212">0</span></span>|<span data-ttu-id="90095-213">0</span><span class="sxs-lookup"><span data-stu-id="90095-213">0</span></span>|<span data-ttu-id="90095-214">0,1</span><span class="sxs-lookup"><span data-stu-id="90095-214">1</span></span>|
|<span data-ttu-id="90095-215">PermissionToRequestRelease<sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="90095-215">PermissionToRequestRelease<sup>\*\*</sup></span></span>|<span data-ttu-id="90095-216">0</span><span class="sxs-lookup"><span data-stu-id="90095-216">0</span></span>|<span data-ttu-id="90095-217">0,1</span><span class="sxs-lookup"><span data-stu-id="90095-217">1</span></span>|<span data-ttu-id="90095-218">0</span><span class="sxs-lookup"><span data-stu-id="90095-218">0</span></span>|
|<span data-ttu-id="90095-219">PermissionToViewHeader<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90095-219">PermissionToViewHeader<sup>\*</sup></span></span>|<span data-ttu-id="90095-220">0</span><span class="sxs-lookup"><span data-stu-id="90095-220">0</span></span>|<span data-ttu-id="90095-221">0</span><span class="sxs-lookup"><span data-stu-id="90095-221">0</span></span>|<span data-ttu-id="90095-222">0</span><span class="sxs-lookup"><span data-stu-id="90095-222">0</span></span>|
|<span data-ttu-id="90095-223">Valeur binaire</span><span class="sxs-lookup"><span data-stu-id="90095-223">Binary value</span></span>|<span data-ttu-id="90095-224">00000000</span><span class="sxs-lookup"><span data-stu-id="90095-224">00000000</span></span>|<span data-ttu-id="90095-225">01101010</span><span class="sxs-lookup"><span data-stu-id="90095-225">01101010</span></span>|<span data-ttu-id="90095-226">11101100</span><span class="sxs-lookup"><span data-stu-id="90095-226">11101100</span></span>|
|<span data-ttu-id="90095-227">Valeur décimale à utiliser</span><span class="sxs-lookup"><span data-stu-id="90095-227">Decimal value to use</span></span>|<span data-ttu-id="90095-228">0</span><span class="sxs-lookup"><span data-stu-id="90095-228">0</span></span>|<span data-ttu-id="90095-229">106</span><span class="sxs-lookup"><span data-stu-id="90095-229">106</span></span>|<span data-ttu-id="90095-230">236</span><span class="sxs-lookup"><span data-stu-id="90095-230">236</span></span>|

<span data-ttu-id="90095-231"><sup>\*</sup> Actuellement, cette valeur est toujours 0.</span><span class="sxs-lookup"><span data-stu-id="90095-231"><sup>\*</sup> Currently, this value is always 0.</span></span> <span data-ttu-id="90095-232">Pour PermissionToViewHeader, la valeur 0 ne masque pas le bouton d' **en-tête afficher le message** dans les détails du message en quarantaine (le bouton est toujours disponible).</span><span class="sxs-lookup"><span data-stu-id="90095-232">For PermissionToViewHeader, the value 0 doesn't hide the **View message header** button in the details of the quarantined message (the button is always available).</span></span>

<span data-ttu-id="90095-233"><sup>\*\*</sup> Ne définissez pas ces deux valeurs sur 1.</span><span class="sxs-lookup"><span data-stu-id="90095-233"><sup>\*\*</sup> Don't set both of these values to 1.</span></span> <span data-ttu-id="90095-234">Définissez un sur 1 et l’autre sur 0, ou définissez-les deux sur 0.</span><span class="sxs-lookup"><span data-stu-id="90095-234">Set one to 1 and the other to 0, or set both to 0.</span></span>

<span data-ttu-id="90095-235">Cet exemple montre comment créer un nom de balise de mise en quarantaine NoAccess qui affecte les autorisations sans accès comme décrit dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="90095-235">This example creates a new quarantine tag name NoAccess that assigns the No access permissions as described in the previous table.</span></span>

```powershell
New-QuarantineTag -Name NoAccess -EndUserQuarantinePermissionsValue 0
```

<span data-ttu-id="90095-236">Pour les autorisations d’accès limité, utilisez la valeur 106.</span><span class="sxs-lookup"><span data-stu-id="90095-236">For Limited access permissions, use the value 106.</span></span> <span data-ttu-id="90095-237">Pour les autorisations d’accès total, utilisez la valeur 236.</span><span class="sxs-lookup"><span data-stu-id="90095-237">For Full access permissions, use the value 236.</span></span>

<span data-ttu-id="90095-238">Pour les autorisations personnalisées, utilisez le tableau précédent pour obtenir la valeur binaire correspondant aux autorisations de votre choix.</span><span class="sxs-lookup"><span data-stu-id="90095-238">For custom permissions, use the previous table to get the binary value that corresponds to the permissions you want.</span></span> <span data-ttu-id="90095-239">Convertissez la valeur binaire en une valeur décimale et utilisez la valeur décimale pour le paramètre _EndUserQuarantinePermissionsValue_ .</span><span class="sxs-lookup"><span data-stu-id="90095-239">Convert the binary value to a decimal value and use the decimal value for the _EndUserQuarantinePermissionsValue_ parameter.</span></span>

<span data-ttu-id="90095-240">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/new-quarantinetag).</span><span class="sxs-lookup"><span data-stu-id="90095-240">For detailed syntax and parameter information, see [New-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/new-quarantinetag).</span></span>

#### <a name="use-the-enduserquarantinepermissions-parameter"></a><span data-ttu-id="90095-241">Utiliser le paramètre EndUserQuarantinePermissions</span><span class="sxs-lookup"><span data-stu-id="90095-241">Use the EndUserQuarantinePermissions parameter</span></span>

<span data-ttu-id="90095-242">Pour créer une balise de mise en quarantaine à l’aide du paramètre _EndUserQuarantinePermissionsValue_ , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="90095-242">To create a quarantine tag using the _EndUserQuarantinePermissionsValue_ parameter, do the following steps:</span></span>

<span data-ttu-id="90095-243">A.</span><span class="sxs-lookup"><span data-stu-id="90095-243">A.</span></span> <span data-ttu-id="90095-244">Stockez un objet d’autorisations de mise en quarantaine dans une variable à l’aide de la cmdlet **New-QuarantinePermissions** .</span><span class="sxs-lookup"><span data-stu-id="90095-244">Store a quarantine permissions object in a variable using the **New-QuarantinePermissions** cmdlet.</span></span>
<br/>
<span data-ttu-id="90095-245">B.</span><span class="sxs-lookup"><span data-stu-id="90095-245">B.</span></span> <span data-ttu-id="90095-246">Utilisez la variable comme valeur _EndUserQuarantinePermissions_ dans la commande **New-QuarantineTag** .</span><span class="sxs-lookup"><span data-stu-id="90095-246">Use the variable as the _EndUserQuarantinePermissions_ value in the **New-QuarantineTag** command.</span></span>

##### <a name="step-a-store-a-quarantine-permissions-object-in-a-variable"></a><span data-ttu-id="90095-247">Étape A : stocker un objet d’autorisations de mise en quarantaine dans une variable</span><span class="sxs-lookup"><span data-stu-id="90095-247">Step A: Store a quarantine permissions object in a variable</span></span>

<span data-ttu-id="90095-248">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="90095-248">Use the following syntax:</span></span>

```powershell
$<VariableName> = New-QuarantinePermissions [-PermissionToAllowSender <$true | $False>] [-PermissionToBlockSender <$true | $False>] [-PermissionToDelete <$true | $False>] [-PermissionToPreview <$true | $False>] [-PermissionToRelease <$true | $False>] [-PermissionToRequestRelease <$true | $False>]
```

<span data-ttu-id="90095-249">La valeur par défaut des paramètres inutilisés est `$false` , de sorte que vous devez uniquement utiliser les paramètres pour lesquels vous souhaitez définir la valeur `$true` .</span><span class="sxs-lookup"><span data-stu-id="90095-249">The default value for any unused parameters is `$false`, so you only need to use the parameters where you want to set value to `$true`.</span></span>

<span data-ttu-id="90095-250">Les exemples suivants montrent comment créer des objets permission qui correspondent aux groupes d’autorisations prédéfinis :</span><span class="sxs-lookup"><span data-stu-id="90095-250">The following examples show how to create permission objects that correspond to the preset permissions groups:</span></span>

- <span data-ttu-id="90095-251">**Aucun accès** :</span><span class="sxs-lookup"><span data-stu-id="90095-251">**No access** :</span></span>

  ```powershell
  $NoAccess = New-QuarantinePermissions
  ```

- <span data-ttu-id="90095-252">**Accès limité** :</span><span class="sxs-lookup"><span data-stu-id="90095-252">**Limited access** :</span></span>

  ```powershell
  $LimitedAccess = New-QuarantinePermissions -PermissionToBlockSender $true -PermissionToDelete $true -PermissionToPreview $true -PermissionToRequestRelease $true
  ```

- <span data-ttu-id="90095-253">**Accès total** :</span><span class="sxs-lookup"><span data-stu-id="90095-253">**Full access** :</span></span>

  ```powershell
  $FullAccess = New-QuarantinePermissions -PermissionToAllowSender $true -PermissionToBlockSender $true -PermissionToDelete $true -PermissionToPreview $true -PermissionToRelease $true
  ```

<span data-ttu-id="90095-254">Pour afficher les valeurs que vous avez définies, exécutez le nom de la variable en tant que commande (par exemple, exécutez la commande `$NoAccess` ).</span><span class="sxs-lookup"><span data-stu-id="90095-254">To see the values that you've set, run the variable name as a command (for example, run the command `$NoAccess`).</span></span>

<span data-ttu-id="90095-255">Pour les autorisations personnalisées, ne définissez pas les paramètres _PermissionToRelease_ et _PermissionToRequestRelease_ sur `$true` .</span><span class="sxs-lookup"><span data-stu-id="90095-255">For custom permissions, don't set both the _PermissionToRelease_ and _PermissionToRequestRelease_ parameters to `$true`.</span></span> <span data-ttu-id="90095-256">Définissez un comme `$true` et laissez le reste `$false` , ou laissez les deux en tant que `$false` .</span><span class="sxs-lookup"><span data-stu-id="90095-256">Set one to `$true` and leave the other as `$false`, or leave both as `$false`.</span></span>

<span data-ttu-id="90095-257">Vous pouvez également modifier une variable d’objet d’autorisations existante après avoir créé mais avant de l’utiliser à l’aide de la cmdlet **Set-QuarantinePermissions** .</span><span class="sxs-lookup"><span data-stu-id="90095-257">You can also modify an existing permissions object variable after you create but before you use it by using the **Set-QuarantinePermissions** cmdlet.</span></span>

<span data-ttu-id="90095-258">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-QuarantinePermissions](https://docs.microsoft.com/powershell/module/exchange/new-quarantinepermissions) et [Set-QuarantinePermissions](https://docs.microsoft.com/powershell/module/exchange/set-quarantinepermissions).</span><span class="sxs-lookup"><span data-stu-id="90095-258">For detailed syntax and parameter information, see [New-QuarantinePermissions](https://docs.microsoft.com/powershell/module/exchange/new-quarantinepermissions) and [Set-QuarantinePermissions](https://docs.microsoft.com/powershell/module/exchange/set-quarantinepermissions).</span></span>

##### <a name="step-b-use-the-variable-in-the-new-quarantinetag-command"></a><span data-ttu-id="90095-259">Étape B : utiliser la variable dans la commande New-QuarantineTag</span><span class="sxs-lookup"><span data-stu-id="90095-259">Step B: Use the variable in the New-QuarantineTag command</span></span>

<span data-ttu-id="90095-260">Une fois que vous avez créé et stocké l’objet permissions dans une variable, utilisez la variable pour la valeur du paramètre _EndUserQuarantinePermission_ dans la commande **New-QuarantineTag** suivante :</span><span class="sxs-lookup"><span data-stu-id="90095-260">After you've created and stored the permissions object in a variable, use the variable for the _EndUserQuarantinePermission_ parameter value in the following **New-QuarantineTag** command:</span></span>

```powershell
New-QuarantineTag -Name "<UniqueName>" -EndUserQuarantinePermissions $<VariableName>
```

<span data-ttu-id="90095-261">Cet exemple crée une nouvelle balise de mise en quarantaine nommée LimitedAccess à l’aide de l' `$LimitedAccess` objet permissions qui a été décrit et créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="90095-261">This example creates a new quarantine tag named LimitedAccess using the `$LimitedAccess` permissions object that was described and created in the previous step.</span></span>

```powershell
New-QuarantineTag -Name LimitedAccess -EndUserQuarantinePermissions $LimitedAccess
```

<span data-ttu-id="90095-262">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/new-quarantinetag).</span><span class="sxs-lookup"><span data-stu-id="90095-262">For detailed syntax and parameter information, see [New-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/new-quarantinetag).</span></span>

## <a name="step-2-assign-a-quarantine-tag-to-supported-features"></a><span data-ttu-id="90095-263">Étape 2 : affecter une balise de mise en quarantaine aux fonctionnalités prises en charge</span><span class="sxs-lookup"><span data-stu-id="90095-263">Step 2: Assign a quarantine tag to supported features</span></span>

<span data-ttu-id="90095-264">Dans les fonctionnalités de protection _prises en charge_ qui met en quarantaine les messages ou les fichiers (automatiquement ou en tant qu’une action configurable), vous pouvez affecter une balise de mise en quarantaine aux actions de mise en quarantaine disponibles.</span><span class="sxs-lookup"><span data-stu-id="90095-264">In _supported_ protection features that quarantine messages or files (automatically or as a configurable action), you can assign a quarantine tag to the available quarantine actions.</span></span> <span data-ttu-id="90095-265">Les fonctionnalités de mise en quarantaine des messages et la disponibilité des balises de mise en quarantaine sont décrites dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="90095-265">Features that quarantine messages and the availability of quarantine tags are described in the following table:</span></span>

****

|<span data-ttu-id="90095-266">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="90095-266">Feature</span></span>|<span data-ttu-id="90095-267">Balises de mise en quarantaine prises en charge ?</span><span class="sxs-lookup"><span data-stu-id="90095-267">Quarantine tags supported?</span></span>|<span data-ttu-id="90095-268">Balises de mise en quarantaine par défaut utilisées</span><span class="sxs-lookup"><span data-stu-id="90095-268">Default quarantine tags used</span></span>|
|---|:---:|---|
|<span data-ttu-id="90095-269">[Stratégies de blocage du courrier indésirable](configure-your-spam-filter-policies.md):</span><span class="sxs-lookup"><span data-stu-id="90095-269">[Anti-spam policies](configure-your-spam-filter-policies.md):</span></span> <ul><li><span data-ttu-id="90095-270">**Courrier indésirable** ( _SpamAction_ )</span><span class="sxs-lookup"><span data-stu-id="90095-270">**Spam** ( _SpamAction_ )</span></span></li><li><span data-ttu-id="90095-271">**Courrier indésirable à niveau de confiance élevé** ( _HighConfidenceSpamAction_ )</span><span class="sxs-lookup"><span data-stu-id="90095-271">**High confidence spam** ( _HighConfidenceSpamAction_ )</span></span></li><li><span data-ttu-id="90095-272">**Courrier électronique de hameçonnage** ( _PhishSpamAction_ )</span><span class="sxs-lookup"><span data-stu-id="90095-272">**Phishing email** ( _PhishSpamAction_ )</span></span></li><li><span data-ttu-id="90095-273">**Courrier électronique de hameçonnage à haute fiabilité** ( _HighConfidencePhishAction_ )</span><span class="sxs-lookup"><span data-stu-id="90095-273">**High confidence phishing email** ( _HighConfidencePhishAction_ )</span></span></li><li><span data-ttu-id="90095-274">**Courrier en masse** ( _BulkSpamAction_ )</span><span class="sxs-lookup"><span data-stu-id="90095-274">**Bulk email** ( _BulkSpamAction_ )</span></span></li></ul>|<span data-ttu-id="90095-275">Oui</span><span class="sxs-lookup"><span data-stu-id="90095-275">Yes</span></span>|<ul><li><span data-ttu-id="90095-276">DefaultSpamTag (accès total)</span><span class="sxs-lookup"><span data-stu-id="90095-276">DefaultSpamTag (Full access)</span></span></li><li><span data-ttu-id="90095-277">DefaultHighConfSpamTag (accès total)</span><span class="sxs-lookup"><span data-stu-id="90095-277">DefaultHighConfSpamTag (Full access)</span></span></li><li><span data-ttu-id="90095-278">DefaultPhishTag (accès total)</span><span class="sxs-lookup"><span data-stu-id="90095-278">DefaultPhishTag (Full access)</span></span></li><li><span data-ttu-id="90095-279">DefaultHighConfPhishTag (pas d’accès)</span><span class="sxs-lookup"><span data-stu-id="90095-279">DefaultHighConfPhishTag (No access)</span></span></li><li><span data-ttu-id="90095-280">DefaultBulkTag (accès total)</span><span class="sxs-lookup"><span data-stu-id="90095-280">DefaultBulkTag (Full access)</span></span></li></ul>
|<span data-ttu-id="90095-281">Stratégies anti-hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="90095-281">Anti-phishing policies:</span></span> <ul><li><span data-ttu-id="90095-282">[Protection contre l’usurpation d’identité](set-up-anti-phishing-policies.md#spoof-settings) ( _AuthenticationFailAction_ )</span><span class="sxs-lookup"><span data-stu-id="90095-282">[Spoof intelligence protection](set-up-anti-phishing-policies.md#spoof-settings) ( _AuthenticationFailAction_ )</span></span></li><li><span data-ttu-id="90095-283">[Protection contre l’usurpation d’identité](set-up-anti-phishing-policies.md#impersonation-settings-in-atp-anti-phishing-policies):<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90095-283">[Impersonation protection](set-up-anti-phishing-policies.md#impersonation-settings-in-atp-anti-phishing-policies):<sup>\*</sup></span></span> <ul><li><span data-ttu-id="90095-284">**Si le courrier électronique est envoyé par un utilisateur emprunté** ( _TargetedUserProtectionAction_ )</span><span class="sxs-lookup"><span data-stu-id="90095-284">**If email is sent by an impersonated user** ( _TargetedUserProtectionAction_ )</span></span></li><li><span data-ttu-id="90095-285">**Si le courrier électronique est envoyé par un domaine emprunté** ( _TargetedDomainProtectionAction_ )</span><span class="sxs-lookup"><span data-stu-id="90095-285">**If email is sent by an impersonated domain** ( _TargetedDomainProtectionAction_ )</span></span></li><li><span data-ttu-id="90095-286">Intelligence des boîtes **aux lettres** \> **Si le courrier électronique est envoyé par un utilisateur emprunté** ( _MailboxIntelligenceProtectionAction_ )</span><span class="sxs-lookup"><span data-stu-id="90095-286">**Mailbox intelligence** \> **If email is sent by an impersonated user** ( _MailboxIntelligenceProtectionAction_ )</span></span></li></ul></li></ul></ul>|<span data-ttu-id="90095-287">Non</span><span class="sxs-lookup"><span data-stu-id="90095-287">No</span></span>|<span data-ttu-id="90095-288">s/o</span><span class="sxs-lookup"><span data-stu-id="90095-288">n/a</span></span>|
|<span data-ttu-id="90095-289">[Stratégies de protection contre les programmes malveillants](configure-anti-malware-policies.md): tous les messages détectés sont toujours mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="90095-289">[Anti-malware policies](configure-anti-malware-policies.md): All detected messages are always quarantined.</span></span>|<span data-ttu-id="90095-290">Non</span><span class="sxs-lookup"><span data-stu-id="90095-290">No</span></span>|<span data-ttu-id="90095-291">s/o</span><span class="sxs-lookup"><span data-stu-id="90095-291">n/a</span></span>|
|[<span data-ttu-id="90095-292">ATP pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="90095-292">ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](atp-for-spo-odb-and-teams.md)|<span data-ttu-id="90095-293">Non</span><span class="sxs-lookup"><span data-stu-id="90095-293">No</span></span>|<span data-ttu-id="90095-294">s/o</span><span class="sxs-lookup"><span data-stu-id="90095-294">n/a</span></span>|
|<span data-ttu-id="90095-295">Les [règles de flux de messagerie](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (également appelées règles de transport) avec l’action : **remet le message à la quarantaine hébergée** ( _mise en quarantaine_ ).</span><span class="sxs-lookup"><span data-stu-id="90095-295">[Mail flow rules](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (also known as transport rules) with the action: **Deliver the message to the hosted quarantine** ( _Quarantine_ ).</span></span>|<span data-ttu-id="90095-296">Non</span><span class="sxs-lookup"><span data-stu-id="90095-296">No</span></span>|<span data-ttu-id="90095-297">s/o</span><span class="sxs-lookup"><span data-stu-id="90095-297">n/a</span></span>|
|

<span data-ttu-id="90095-298"><sup>\*</sup> Les paramètres de protection contre l’emprunt d’identité sont disponibles uniquement dans les stratégies anti-hameçonnage de Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="90095-298"><sup>\*</sup> Impersonation protection settings are available only in anti-phishing policies in Microsoft Defender for Office 365.</span></span>

<span data-ttu-id="90095-299">Si vous êtes satisfait des autorisations de l’utilisateur final fournies par les balises de mise en quarantaine par défaut, aucune action n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="90095-299">If you're happy with the end-user permissions that are provided by the default quarantine tags, you don't need to do anything.</span></span> <span data-ttu-id="90095-300">Si vous souhaitez personnaliser les fonctionnalités de l’utilisateur final (boutons disponibles) dans les notifications de courrier indésirable de l’utilisateur final ou les détails du message en quarantaine, vous pouvez affecter une balise de mise en quarantaine personnalisée.</span><span class="sxs-lookup"><span data-stu-id="90095-300">If you want to customize the end-user capabilities (available buttons) in end-user spam notifications or in quarantined message details, you can assign a custom quarantine tag.</span></span>

### <a name="assign-quarantine-tags-in-anti-spam-policies-in-the-security--compliance-center"></a><span data-ttu-id="90095-301">Attribuer des balises de mise en quarantaine dans les stratégies de blocage du courrier indésirable dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="90095-301">Assign quarantine tags in anti-spam policies in the Security & Compliance Center</span></span>

<span data-ttu-id="90095-302">Pour plus d’informations sur la création et la modification de stratégies de blocage du courrier indésirable, voir [configurer les stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="90095-302">Full instructions for creating and modifying anti-spam policies are described in [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

1. <span data-ttu-id="90095-303">Dans le centre de sécurité & conformité, accédez à stratégie de **gestion des menaces** , \> **Policy** \> puis sélectionnez **blocage du courrier indésirable** .</span><span class="sxs-lookup"><span data-stu-id="90095-303">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> and then select **Anti-spam** .</span></span> <span data-ttu-id="90095-304">Ou ouvrez <https://protection.office.com/antispam> .</span><span class="sxs-lookup"><span data-stu-id="90095-304">Or, open <https://protection.office.com/antispam>.</span></span>

2. <span data-ttu-id="90095-305">Recherchez et sélectionnez une stratégie de blocage du courrier indésirable existante à modifier, ou créez une nouvelle stratégie de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="90095-305">Find and select an existing anti-spam policy to edit, or create a new anti-spam policy.</span></span>

3. <span data-ttu-id="90095-306">Dans la fenêtre mobile détails de la stratégie, développez la section **actions de courrier indésirable et en bloc** .</span><span class="sxs-lookup"><span data-stu-id="90095-306">In the policy details flyout, expand the **Spam and bulk actions** section.</span></span>
  
4. <span data-ttu-id="90095-307">Si vous avez sélectionné **message mis en quarantaine** pour l’action d’une option de filtrage du courrier indésirable disponible, la zone **appliquer la balise de stratégie de mise en quarantaine** est disponible pour vous permettant de sélectionner la balise de mise en quarantaine pour ce verdict.</span><span class="sxs-lookup"><span data-stu-id="90095-307">If you've selected **Quarantine message** for the action of an available spam filtering verdict, the **Apply quarantine policy tag** box is available for you to select the quarantine tag for that verdict.</span></span>

   <span data-ttu-id="90095-308">**Remarque** : lorsque vous créez une stratégie, une valeur de balise de mise en quarantaine vide pour un filtrage du courrier indésirable en verdict indique que la balise de mise en quarantaine par défaut pour ce verdict est utilisée.</span><span class="sxs-lookup"><span data-stu-id="90095-308">**Note** : When you create a new policy, a blank quarantine tag value for a spam filtering verdict indicates the default quarantine tag for that verdict is used.</span></span> <span data-ttu-id="90095-309">Lorsque vous modifiez ultérieurement la stratégie, les valeurs non renseignées sont remplacées par les noms de balise de mise en quarantaine par défaut réels, comme décrit dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="90095-309">When you later edit the policy, the blank values are replaced by the actual default quarantine tag names as described in the previous table.</span></span>
  
   ![Sélections de la balise de quarantaine dans une stratégie de blocage du courrier indésirable](../../media/quarantine-tags-in-anti-spam-policies.png)

5. <span data-ttu-id="90095-311">Lorsque vous avez terminé, cliquez sur **Enregistrer** .</span><span class="sxs-lookup"><span data-stu-id="90095-311">When you're finished, click **Save** .</span></span>

#### <a name="assign-quarantine-tags-in-anti-spam-policies-in-powershell"></a><span data-ttu-id="90095-312">Attribuer des balises de mise en quarantaine dans les stratégies de blocage du courrier indésirable dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="90095-312">Assign quarantine tags in anti-spam policies in PowerShell</span></span>

<span data-ttu-id="90095-313">Si vous préférez utiliser PowerShell pour attribuer des balises de mise en quarantaine dans des stratégies de blocage du courrier indésirable, connectez-vous à Exchange Online PowerShell ou à Exchange Online Protection PowerShell, puis utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="90095-313">If you'd rather use PowerShell to assign quarantine tags in anti-spam policies, connect to Exchange Online PowerShell or Exchange Online Protection PowerShell and use the following syntax:</span></span>

```powershell
<New-HostedContentFilterPolicy -Name "<Unique name>" | Set-HostedContentFilterPolicy -Identity "<Policy name>">  [-SpamAction Quarantine] [-SpamQuarantineTag <QuarantineTagName>] [-HighConfidenceSpamAction Quarantine] [-HighConfidenceSpamQuarantineTag <QuarantineTagName>] [-PhishSpamAction Quarantine] [-PhishQuarantineTag <QuarantineTagName>] [-HighConfidencePhishQuarantineTag <QuarantineTagName>] [-BulkSpamAction Quarantine] [-BulkQuarantineTag <QuarantineTagName>] ...
```

<span data-ttu-id="90095-314">**Remarques**  :</span><span class="sxs-lookup"><span data-stu-id="90095-314">**Notes** :</span></span>

- <span data-ttu-id="90095-315">La valeur par défaut du paramètre _HighConfidencePhishAction_ est mise en quarantaine, vous n’avez donc pas besoin de définir l’action de mise en quarantaine pour les détections de hameçonnage à haute fiabilité dans les nouvelles stratégies de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="90095-315">The default value for the _HighConfidencePhishAction_ parameter is Quarantine, so you don't need to set the Quarantine action for high confidence phishing detections in new anti-spam policies.</span></span> <span data-ttu-id="90095-316">Pour tous les autres filtrages de courrier indésirable en fonction des stratégies anti-courrier indésirable nouvelles ou existantes, la balise de mise en quarantaine n’est effective que si la valeur de l’action est mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="90095-316">For all other spam filtering verdicts in new or existing anti-spam policies, the quarantine tag is only effective if the action value is Quarantine.</span></span> <span data-ttu-id="90095-317">Pour afficher les valeurs d’action dans les stratégies anti-courrier indésirable existantes, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="90095-317">To see the action values in existing anti-spam policies, run the following command:</span></span>

  ```powershell
  Get-HostedContentFilterPolicy | Format-Table Name,*SpamAction,HighConfidencePhishAction
  ```

  <span data-ttu-id="90095-318">Pour plus d’informations sur les valeurs d’action par défaut et sur les valeurs d’action recommandées pour standard et strict, voir [EOP anti-spam Policy Settings](recommended-settings-for-eop-and-office365-atp.md#eop-anti-spam-policy-settings).</span><span class="sxs-lookup"><span data-stu-id="90095-318">For information about the default action values and the recommended action values for Standard and Strict, see [EOP anti-spam policy settings](recommended-settings-for-eop-and-office365-atp.md#eop-anti-spam-policy-settings).</span></span>

- <span data-ttu-id="90095-319">Le filtrage du courrier indésirable correspondant à un paramètre de balise de mise en quarantaine correspondant signifie que la [balise de mise en quarantaine par défaut](#step-2-assign-a-quarantine-tag-to-supported-features) pour ce verdict est utilisée.</span><span class="sxs-lookup"><span data-stu-id="90095-319">A spam filtering verdict without a corresponding quarantine tag parameter means the [default quarantine tag](#step-2-assign-a-quarantine-tag-to-supported-features) for that verdict is used.</span></span>

  <span data-ttu-id="90095-320">Vous ne devez remplacer une balise de mise en quarantaine par défaut par une balise de mise en quarantaine personnalisée que si vous souhaitez modifier les fonctionnalités de l’utilisateur final par défaut sur les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="90095-320">You only need to replace a default quarantine tag with a custom quarantine tag if you want to change the default end-user capabilities on quarantined messages.</span></span>

- <span data-ttu-id="90095-321">Une nouvelle stratégie de blocage du courrier indésirable dans PowerShell nécessite une stratégie de filtrage du courrier indésirable (paramètres) à l’aide de la cmdlet **New-HostedContentFilterPolicy** et une nouvelle règle de filtrage du courrier indésirable (filtres de destinataires) à l’aide de la cmdlet **New-hostedcontentfilterrule permet** .</span><span class="sxs-lookup"><span data-stu-id="90095-321">A new anti-spam policy in PowerShell requires a spam filter policy (settings) using the **New-HostedContentFilterPolicy** cmdlet and a new spam filter rule (recipient filters) using the **New-HostedContentFilterRule** cmdlet.</span></span> <span data-ttu-id="90095-322">Pour obtenir des instructions, consultez la rubrique [Utiliser PowerShell pour créer des stratégies de blocage du courrier indésirable](configure-your-spam-filter-policies.md#use-powershell-to-create-anti-spam-policies).</span><span class="sxs-lookup"><span data-stu-id="90095-322">For instructions, see [Use PowerShell to create anti-spam policies](configure-your-spam-filter-policies.md#use-powershell-to-create-anti-spam-policies).</span></span>

<span data-ttu-id="90095-323">Cet exemple crée une nouvelle stratégie de filtrage du courrier indésirable nommée Research Department avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="90095-323">This example creates a new spam filter policy named Research Department with the following settings:</span></span>

- <span data-ttu-id="90095-324">L’action pour l’ensemble du filtrage du courrier indésirable est définie sur quarantaine.</span><span class="sxs-lookup"><span data-stu-id="90095-324">The action for all spam filtering verdicts is set to Quarantine.</span></span>
- <span data-ttu-id="90095-325">La balise de mise en quarantaine personnalisée nommée NoAccess qui n’affecte pas d’autorisations d' **accès** remplace les balises de mise en quarantaine par défaut qui n’assignent pas encore d’autorisations d' **accès** par défaut.</span><span class="sxs-lookup"><span data-stu-id="90095-325">The custom quarantine tag named NoAccess that assigns **No access** permissions replaces any default quarantine tags that don't already assign **No access** permissions by default.</span></span>

```powershell
New-HostedContentFilterPolicy -Name Research Department -SpamAction Quarantine -SpamQuarantineTag NoAccess -HighConfidenceSpamAction Quarantine -HighConfidenceSpamQuarantineTag NoAction -PhishSpamAction Quarantine -PhishQuarantineTag NoAction -BulkSpamAction Quarantine -BulkQuarantineTag NoAccess
```

<span data-ttu-id="90095-326">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/new-hostedcontentfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="90095-326">For detailed syntax and parameter information, see [New-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/new-hostedcontentfilterpolicy).</span></span>

<span data-ttu-id="90095-327">Cet exemple modifie la stratégie de filtrage du courrier indésirable nommée Human Resources.</span><span class="sxs-lookup"><span data-stu-id="90095-327">This example modifies the existing spam filter policy named Human Resources.</span></span> <span data-ttu-id="90095-328">L’action pour le verdict de mise en quarantaine du courrier indésirable est définie sur quarantaine et la balise de mise en quarantaine personnalisée nommée NoAccess est attribuée.</span><span class="sxs-lookup"><span data-stu-id="90095-328">The action for the spam quarantine verdict is set to Quarantine, and the custom quarantine tag named NoAccess is assigned.</span></span>

```powershell
Set-HostedContentFilterPolicy -Identity "Human Resources" -SpamAction Quarantine -SpamQuarantineTag NoAccess
```

<span data-ttu-id="90095-329">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-hostedcontentfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="90095-329">For detailed syntax and parameter information, see [Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-hostedcontentfilterpolicy).</span></span>

## <a name="configure-global-quarantine-notification-settings-in-the-security--compliance-center"></a><span data-ttu-id="90095-330">Configurer les paramètres de notification de mise en quarantaine globale dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="90095-330">Configure global quarantine notification settings in the Security & Compliance Center</span></span>

<span data-ttu-id="90095-331">Les paramètres globaux pour les balises de mise en quarantaine vous permettent de personnaliser les notifications de courrier indésirable de l’utilisateur final qui sont envoyées aux destinataires des messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="90095-331">The global settings for quarantine tags allow you to customize the end-user spam notifications that are sent to recipients of messages that were quarantined.</span></span> <span data-ttu-id="90095-332">Pour plus d’informations sur ces notifications, consultez la rubrique [notifications de courrier indésirable de l’utilisateur final](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span><span class="sxs-lookup"><span data-stu-id="90095-332">For more information about these notifications, see [End-user spam notifications](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span>

1. <span data-ttu-id="90095-333">Dans le centre de sécurité & conformité, accédez à stratégie de **gestion des menaces** , \> **Policy** puis sélectionnez **balises de mise en quarantaine** .</span><span class="sxs-lookup"><span data-stu-id="90095-333">In the Security & Compliance Center, go to **Threat management** \> **Policy** and then select **Quarantine tags** .</span></span>

2. <span data-ttu-id="90095-334">Sur la page **balises de quarantaine** , sélectionnez **paramètres globaux** .</span><span class="sxs-lookup"><span data-stu-id="90095-334">On the **Quarantine tags** page, select **Global settings** .</span></span>

3. <span data-ttu-id="90095-335">Dans la fenêtre mobile **paramètres de notification de mise en quarantaine** qui s’ouvre, configurez une partie ou l’ensemble des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="90095-335">In the **Quarantine notification settings** flyout that opens, configure some or all of the following settings:</span></span>

   - <span data-ttu-id="90095-336">**Utiliser mon logo de société** : sélectionnez cette option pour remplacer le logo Microsoft par défaut qui est utilisé en haut des notifications de courrier indésirable de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="90095-336">**Use my company logo** : Select this option to replace the default Microsoft logo that's use at the top of end-user spam notifications.</span></span> <span data-ttu-id="90095-337">Avant cela, vous devez suivre les instructions de la procédure [personnaliser le thème Microsoft 365 de votre organisation](https://docs.microsoft.com/microsoft-365/admin/setup/customize-your-organization-theme) pour télécharger votre logo personnalisé.</span><span class="sxs-lookup"><span data-stu-id="90095-337">Before you do this, you need to follow the instructions in [Customize the Microsoft 365 theme for your organization](https://docs.microsoft.com/microsoft-365/admin/setup/customize-your-organization-theme) to upload your custom logo.</span></span>

     <span data-ttu-id="90095-338">La capture d’écran suivante montre un logo personnalisé dans une notification de courrier indésirable pour l’utilisateur final :</span><span class="sxs-lookup"><span data-stu-id="90095-338">The following screenshot shows a custom logo in an end-user spam notification:</span></span>

     ![Un logo personnalisé dans une notification de courrier indésirable pour l’utilisateur final](../../media/quarantine-tags-esn-customization-logo.png)

   - <span data-ttu-id="90095-340">**Choisir la langue** : les notifications de courrier indésirable de l’utilisateur final sont déjà localisées en fonction des paramètres de langue du destinataire.</span><span class="sxs-lookup"><span data-stu-id="90095-340">**Choose language** : End-user spam notifications are already localized based on the recipient's language settings.</span></span> <span data-ttu-id="90095-341">Vous pouvez spécifier un texte personnalisé dans différentes langues pour le **nom d’affichage** et les valeurs de clause d’exclusion de **responsabilité** .</span><span class="sxs-lookup"><span data-stu-id="90095-341">You can specify customized text in different languages for the **Display name** and **Disclaimer** values.</span></span>

     <span data-ttu-id="90095-342">Sélectionnez au moins une langue dans la première langue, puis cliquez sur **Ajouter** .</span><span class="sxs-lookup"><span data-stu-id="90095-342">Select at least one language from the first language box and then click **Add** .</span></span> <span data-ttu-id="90095-343">Vous pouvez sélectionner plusieurs langues en cliquant sur **Ajouter** après chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="90095-343">You can select multiple languages by clicking **Add** after each one.</span></span> <span data-ttu-id="90095-344">Une case langue de section affiche toutes les langues que vous avez sélectionnées :</span><span class="sxs-lookup"><span data-stu-id="90095-344">A section language box shows all of the languages that you've selected:</span></span>

     ![Langues sélectionnées dans la deuxième langue de la zone dans les paramètres de notification de mise en quarantaine globale des balises de mise en quarantaine](../../media/quarantine-tags-esn-customization-selected-languages.png)

   - <span data-ttu-id="90095-346">**Nom d’affichage** : Personnalisez le nom d’affichage de l’expéditeur utilisé dans les notifications de courrier indésirable de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="90095-346">**Display name** : Customize the sender's display name that's used in end-user spam notifications.</span></span>

     <span data-ttu-id="90095-347">Pour chaque langue que vous avez ajoutée, sélectionnez la langue dans la seconde langue (ne cliquez pas sur le X) et entrez la valeur de texte souhaitée dans la zone **nom complet** .</span><span class="sxs-lookup"><span data-stu-id="90095-347">For each language that you've added, select the language in the second language box (don't click on the X) and enter the text value you want in the **Display name** box.</span></span>

     <span data-ttu-id="90095-348">La capture d’écran suivante montre le nom d’affichage personnalisé dans une notification de courrier indésirable de l’utilisateur final :</span><span class="sxs-lookup"><span data-stu-id="90095-348">The following screenshot shows the customized display name in an end-user spam notification:</span></span>

     ![Nom d’affichage personnalisé de l’expéditeur dans une notification de courrier indésirable pour l’utilisateur final](../../media/quarantine-tags-esn-customization-display-name.png)

   - <span data-ttu-id="90095-350">**Clause d’exclusion** de responsabilité : ajoutez une clause d’exclusion de responsabilité personnalisée au bas des notifications de courrier indésirable de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="90095-350">**Disclaimer** : Add a custom disclaimer to the bottom of end-user spam notifications.</span></span> <span data-ttu-id="90095-351">Le texte localisé, **une clause d’exclusion de responsabilité de votre organisation :** est toujours inclus en premier, suivi du texte que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="90095-351">The localized text, **A disclaimer from your organization:** is always included first, followed by the text you specify.</span></span>

     <span data-ttu-id="90095-352">Pour chaque langue que vous avez ajoutée, sélectionnez la langue dans la deuxième langue (ne cliquez pas sur X) et entrez la valeur de texte souhaitée dans la zone **exclusion de responsabilité** .</span><span class="sxs-lookup"><span data-stu-id="90095-352">For each language that you've added, select the language in the second language box  (don't click the X) and enter the text value you want in the **Disclaimer** box.</span></span>

     <span data-ttu-id="90095-353">La capture d’écran suivante montre la clause d’exclusion de responsabilité personnalisée dans une notification de courrier indésirable de l’utilisateur final :</span><span class="sxs-lookup"><span data-stu-id="90095-353">The following screenshot shows the customized disclaimer in an end-user spam notification:</span></span>

     ![Une clause d’exclusion de responsabilité personnalisée au bas d’une notification de courrier indésirable de l’utilisateur final](../../media/quarantine-tags-esn-customization-disclaimer.png)

## <a name="view-quarantine-tags-in-the-security--compliance-center"></a><span data-ttu-id="90095-355">Afficher les balises de mise en quarantaine dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="90095-355">View quarantine tags in the Security & Compliance Center</span></span>

1. <span data-ttu-id="90095-356">Dans le centre de sécurité & conformité, accédez à stratégie de **gestion des menaces** , \> **Policy** puis sélectionnez **balises de mise en quarantaine** .</span><span class="sxs-lookup"><span data-stu-id="90095-356">In the Security & Compliance Center, go to **Threat management** \> **Policy** and then select **Quarantine tags** .</span></span>

- <span data-ttu-id="90095-357">Pour afficher les paramètres des balises de mise en quarantaine prédéfinies ou personnalisées, sélectionnez la balise de mise en quarantaine dans la liste (n’activez pas la case à cocher).</span><span class="sxs-lookup"><span data-stu-id="90095-357">To view the settings of built-in or custom quarantine tags, select the quarantine tag from the list (don't select the check box).</span></span>

- <span data-ttu-id="90095-358">Pour afficher les paramètres globaux, sélectionnez **paramètres globaux** .</span><span class="sxs-lookup"><span data-stu-id="90095-358">To view the global settings, select **Global settings**</span></span>

### <a name="view-quarantine-tags-in-powershell"></a><span data-ttu-id="90095-359">Afficher les balises de mise en quarantaine dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="90095-359">View quarantine tags in PowerShell</span></span>

<span data-ttu-id="90095-360">Si vous préférez utiliser PowerShell pour afficher les balises de mise en quarantaine, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="90095-360">If you'd rather use PowerShell to view quarantine tags, do any of the following steps:</span></span>

- <span data-ttu-id="90095-361">Pour afficher la liste récapitulative de toutes les balises prédéfinies ou personnalisées, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="90095-361">To view a summary list of all built-in or custom tags, run the following command:</span></span>

  ```powershell
  Get-QuarantineTag | Format-Table Name
  ```

- <span data-ttu-id="90095-362">Pour afficher les paramètres des balises de mise en quarantaine prédéfinies ou personnalisées, remplacez \<TagName\> par le nom de la balise de mise en quarantaine, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="90095-362">To view the settings of built-in or custom quarantine tags, replace \<TagName\> with the name of the quarantine tag, and run the following command:</span></span>

  ```powershell
  Get-QuarantineTag -Identity "<TagName>"
  ```

- <span data-ttu-id="90095-363">Pour afficher les paramètres globaux, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="90095-363">To view the global settings, run the following command:</span></span>

  ```powershell
  Get-QuarantineTag -QuarantineTagType GlobalQuarantineTag
  ```

<span data-ttu-id="90095-364">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/get-hostedcontentfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="90095-364">For detailed syntax and parameter information, see [Get-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/get-hostedcontentfilterpolicy).</span></span>

## <a name="remove-quarantine-tags-in-the-security--compliance-center"></a><span data-ttu-id="90095-365">Supprimer les balises de mise en quarantaine dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="90095-365">Remove quarantine tags in the Security & Compliance Center</span></span>

<span data-ttu-id="90095-366">**Remarques**  :</span><span class="sxs-lookup"><span data-stu-id="90095-366">**Notes** :</span></span>

- <span data-ttu-id="90095-367">Vous ne pouvez pas supprimer les balises de quarantaine prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="90095-367">You can't remove built-in quarantine tags.</span></span>

- <span data-ttu-id="90095-368">Avant de supprimer une balise de mise en quarantaine personnalisée, vérifiez qu’elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="90095-368">Before you remove a custom quarantine tag, verify that it's not being used.</span></span> <span data-ttu-id="90095-369">Par exemple, exécutez la commande suivante dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="90095-369">For example, run the following command in PowerShell:</span></span>

  ```powershell
  Get-HostedContentFilterPolicy | Format-List Name,*QuarantineTag
  ```

  <span data-ttu-id="90095-370">Si la balise de mise en quarantaine est utilisée, [Remplacez la balise de mise en quarantaine affectée avant de la](#step-2-assign-a-quarantine-tag-to-supported-features) supprimer.</span><span class="sxs-lookup"><span data-stu-id="90095-370">If the quarantine tag is being used, [replace the assigned quarantine tag](#step-2-assign-a-quarantine-tag-to-supported-features) before you remove it.</span></span>

1. <span data-ttu-id="90095-371">Dans le centre de sécurité & conformité, accédez à stratégie de **gestion des menaces** , \> **Policy** puis sélectionnez **balises de mise en quarantaine** .</span><span class="sxs-lookup"><span data-stu-id="90095-371">In the Security & Compliance Center, go to **Threat management** \> **Policy** and then select **Quarantine tags** .</span></span>

2. <span data-ttu-id="90095-372">Sur la page **balises de quarantaine** , sélectionnez la balise de mise en quarantaine personnalisée que vous souhaitez supprimer, puis cliquez sur **Supprimer la balise** .</span><span class="sxs-lookup"><span data-stu-id="90095-372">On the **Quarantine tags** page, select the custom quarantine tag that you want to remove, and the click **Delete tag** .</span></span>

3. <span data-ttu-id="90095-373">Cliquez sur **Supprimer la balise** dans la boîte de dialogue de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="90095-373">Click **Remove tag** in the confirmation dialog that appears.</span></span>

### <a name="remove-quarantine-tags-in-powershell"></a><span data-ttu-id="90095-374">Supprimer les balises de mise en quarantaine dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="90095-374">Remove quarantine tags in PowerShell</span></span>

<span data-ttu-id="90095-375">Si vous préférez utiliser PowerShell pour supprimer une balise de mise en quarantaine personnalisée, remplacez \<TagName\> par le nom de la balise de mise en quarantaine, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="90095-375">If you'd rather use PowerShell to remove a custom quarantine tag, replace \<TagName\> with the name of the quarantine tag, and run the following command:</span></span>

```powershell
Remove-QuarantineTag -Identity "<TagName>"
```

<span data-ttu-id="90095-376">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/remove-quarantinetag).</span><span class="sxs-lookup"><span data-stu-id="90095-376">For detailed syntax and parameter information, see [Remove-QuarantineTag](https://docs.microsoft.com/powershell/module/exchange/remove-quarantinetag).</span></span>

## <a name="quarantine-tag-permission-details"></a><span data-ttu-id="90095-377">Détails des autorisations de la balise de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="90095-377">Quarantine tag permission details</span></span>

<span data-ttu-id="90095-378">Les sections suivantes décrivent les effets des groupes d’autorisations prédéfinis et des autorisations individuelles dans les détails des messages mis en quarantaine et dans les notifications de courrier indésirable de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="90095-378">The following sections describe the effects of preset permission groups and individual permissions in the details of quarantined messages and in end-user spam notifications.</span></span>

### <a name="preset-permissions-groups"></a><span data-ttu-id="90095-379">Groupes d’autorisations prédéfinis</span><span class="sxs-lookup"><span data-stu-id="90095-379">Preset permissions groups</span></span>

<span data-ttu-id="90095-380">Les autorisations individuelles qui sont incluses dans des groupes d’autorisations prédéfinis sont répertoriées dans le tableau au début de cet article.</span><span class="sxs-lookup"><span data-stu-id="90095-380">The individual permissions that are included in preset permission groups are listed in the table at the beginning of this article.</span></span>

#### <a name="no-access"></a><span data-ttu-id="90095-381">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="90095-381">No access</span></span>

<span data-ttu-id="90095-382">Si la balise de mise en quarantaine affecte les autorisations **aucune** autorisation (aucune autorisation), les utilisateurs reçoivent toujours des fonctionnalités de ligne de base :</span><span class="sxs-lookup"><span data-stu-id="90095-382">If the quarantine tag assigns the **No access** permissions (no permissions), users still get some baseline capabilities:</span></span>

- <span data-ttu-id="90095-383">**Détails du message en quarantaine** : le bouton d' **en-tête afficher le message** est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-383">**Quarantined message details** : The **View message header** button is always available.</span></span>

  ![Boutons disponibles dans les détails du message en quarantaine si la balise de mise en quarantaine donne à l’utilisateur aucune autorisation d’accès](../../media/quarantine-tags-quarantined-message-details-no-access.png)

- <span data-ttu-id="90095-385">**Notifications de courrier indésirable de l’utilisateur final** : le bouton **Review** qui dirige l’utilisateur vers le message en quarantaine est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-385">**End-user spam notifications** : The **Review** button that takes the user to the message in quarantine is always available.</span></span>

  ![Boutons disponibles dans la notification de courrier indésirable de l’utilisateur final si la balise de mise en quarantaine donne à l’utilisateur aucune autorisation d’accès](../../media/quarantine-tags-esn-no-access.png)

#### <a name="limited-access"></a><span data-ttu-id="90095-387">Accès limité</span><span class="sxs-lookup"><span data-stu-id="90095-387">Limited access</span></span>

<span data-ttu-id="90095-388">Si la balise de mise en quarantaine affecte les autorisations d' **accès limitées** , les utilisateurs obtiennent les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="90095-388">If the quarantine tag assigns the **Limited access** permissions, users get the following capabilities:</span></span>

- <span data-ttu-id="90095-389">**Détails du message en quarantaine** : les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="90095-389">**Quarantined message details** : The following buttons are available:</span></span>
  - <span data-ttu-id="90095-390">**Version de la demande**</span><span class="sxs-lookup"><span data-stu-id="90095-390">**Request release**</span></span>
  - <span data-ttu-id="90095-391">**Afficher l’en-tête du message**</span><span class="sxs-lookup"><span data-stu-id="90095-391">**View message header**</span></span>
  - <span data-ttu-id="90095-392">**Aperçu du message**</span><span class="sxs-lookup"><span data-stu-id="90095-392">**Preview message**</span></span>
  - <span data-ttu-id="90095-393">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="90095-393">**Block sender**</span></span>
  - <span data-ttu-id="90095-394">**Supprimer de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="90095-394">**Remove from quarantine**</span></span>

  ![Boutons disponibles dans les détails du message en quarantaine si la balise de mise en quarantaine accorde aux utilisateurs des autorisations d’accès limitées](../../media/quarantine-tags-quarantined-message-details-limited-access.png)

- <span data-ttu-id="90095-396">**Notifications de courrier indésirable de l’utilisateur final** : les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="90095-396">**End-user spam notifications** : The following buttons are available:</span></span>
  - <span data-ttu-id="90095-397">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="90095-397">**Block sender**</span></span>
  - <span data-ttu-id="90095-398">**Révision**</span><span class="sxs-lookup"><span data-stu-id="90095-398">**Review**</span></span>

  ![Boutons disponibles dans la notification de courrier indésirable de l’utilisateur final si la balise de mise en quarantaine accorde aux utilisateurs des autorisations d’accès limitées](../../media/quarantine-tags-esn-limited-access.png)

#### <a name="full-access"></a><span data-ttu-id="90095-400">Accès total</span><span class="sxs-lookup"><span data-stu-id="90095-400">Full access</span></span>

<span data-ttu-id="90095-401">Si la balise de mise en quarantaine affecte les autorisations d' **accès total** (toutes les autorisations disponibles), les utilisateurs bénéficient des fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="90095-401">If the quarantine tag assigns the **Full access** permissions (all available permissions), users get the following capabilities:</span></span>

- <span data-ttu-id="90095-402">**Détails du message en quarantaine** : les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="90095-402">**Quarantined message details** : The following buttons are available:</span></span>
  - <span data-ttu-id="90095-403">**Message de publication**</span><span class="sxs-lookup"><span data-stu-id="90095-403">**Release message**</span></span>
  - <span data-ttu-id="90095-404">**Afficher l’en-tête du message**</span><span class="sxs-lookup"><span data-stu-id="90095-404">**View message header**</span></span>
  - <span data-ttu-id="90095-405">**Aperçu du message**</span><span class="sxs-lookup"><span data-stu-id="90095-405">**Preview message**</span></span>
  - <span data-ttu-id="90095-406">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="90095-406">**Block sender**</span></span>
  - <span data-ttu-id="90095-407">**Autoriser l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="90095-407">**Allow sender**</span></span>
  - <span data-ttu-id="90095-408">**Supprimer de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="90095-408">**Remove from quarantine**</span></span>

  ![Boutons disponibles dans les détails du message en quarantaine si la balise de mise en quarantaine accorde à l’utilisateur les autorisations d’accès total](../../media/quarantine-tags-quarantined-message-details-full-access.png)

- <span data-ttu-id="90095-410">**Notifications de courrier indésirable de l’utilisateur final** : les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="90095-410">**End-user spam notifications** : The following buttons are available:</span></span>
  - <span data-ttu-id="90095-411">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="90095-411">**Block sender**</span></span>
  - <span data-ttu-id="90095-412">**Version**</span><span class="sxs-lookup"><span data-stu-id="90095-412">**Release**</span></span>
  - <span data-ttu-id="90095-413">**Révision**</span><span class="sxs-lookup"><span data-stu-id="90095-413">**Review**</span></span>

  ![Boutons disponibles dans la notification de courrier indésirable de l’utilisateur final si la balise de mise en quarantaine accorde à l’utilisateur les autorisations d’accès total](../../media/quarantine-tags-esn-full-access.png)

### <a name="individual-permissions"></a><span data-ttu-id="90095-415">Autorisations individuelles</span><span class="sxs-lookup"><span data-stu-id="90095-415">Individual permissions</span></span>

> [!NOTE]
> <span data-ttu-id="90095-416">N’oubliez pas que les utilisateurs reçoivent toujours les boutons décrits dans la section [pas d’accès](#no-access) .</span><span class="sxs-lookup"><span data-stu-id="90095-416">Remember, users always get the buttons described in the [No access](#no-access) section.</span></span> <span data-ttu-id="90095-417">Ces boutons ne sont pas inclus dans les descriptions d’autorisation individuelles.</span><span class="sxs-lookup"><span data-stu-id="90095-417">These buttons are not included in the individual permission descriptions.</span></span>

#### <a name="allow-sender-permission"></a><span data-ttu-id="90095-418">Autorisation de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="90095-418">Allow sender permission</span></span>

<span data-ttu-id="90095-419">L’autorisation **autoriser l’expéditeur** ( _PermissionToAllowSender_ ) contrôle l’accès au bouton qui permet aux utilisateurs d’ajouter facilement l’expéditeur du message en quarantaine à leur liste des expéditeurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="90095-419">The **Allow sender** permission ( _PermissionToAllowSender_ ) controls access to the button that allows users to conveniently add the quarantined message sender to their Safe Senders list.</span></span>

- <span data-ttu-id="90095-420">**Détails du message en quarantaine** :</span><span class="sxs-lookup"><span data-stu-id="90095-420">**Quarantined message details** :</span></span>
  - <span data-ttu-id="90095-421">**Autoriser** l’autorisation de l’expéditeur activé : le bouton **autoriser l’expéditeur** est disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-421">**Allow sender** permission enabled: The **Allow sender** button is available.</span></span>
  - <span data-ttu-id="90095-422">**Autoriser l’expéditeur** désactivé : le bouton **autoriser l’expéditeur** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-422">**Allow sender** permission disabled: The **Allow sender** button is not available.</span></span>

- <span data-ttu-id="90095-423">**Notifications de courrier indésirable de l’utilisateur final** : aucun effet.</span><span class="sxs-lookup"><span data-stu-id="90095-423">**End-user spam notifications** : No effect.</span></span>

<span data-ttu-id="90095-424">Pour plus d’informations sur la liste des expéditeurs approuvés, voir [empêcher le blocage des expéditeurs approuvés](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379666) et [utiliser Exchange Online PowerShell pour configurer la collection de listes fiables sur une boîte aux lettres](https://docs.microsoft.com/microsoft-365/security/office-365-security/configure-junk-email-settings-on-exo-mailboxes#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox).</span><span class="sxs-lookup"><span data-stu-id="90095-424">For more information about the Safe Senders list, see [Prevent trusted senders from being blocked](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379666) and [Use Exchange Online PowerShell to configure the safelist collection on a mailbox](https://docs.microsoft.com/microsoft-365/security/office-365-security/configure-junk-email-settings-on-exo-mailboxes#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox).</span></span>

### <a name="block-sender-permission"></a><span data-ttu-id="90095-425">Autorisation bloquer l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="90095-425">Block sender permission</span></span>

<span data-ttu-id="90095-426">L’autorisation **proscrire l’expéditeur** ( _PermissionToBlockSender_ ) contrôle l’accès au bouton qui permet aux utilisateurs d’ajouter facilement l’expéditeur du message en quarantaine à la liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="90095-426">The **Block sender** permission ( _PermissionToBlockSender_ ) controls access to the button that allows users to conveniently add the quarantined message sender to their Blocked Senders list.</span></span>

- <span data-ttu-id="90095-427">**Détails du message en quarantaine** :</span><span class="sxs-lookup"><span data-stu-id="90095-427">**Quarantined message details** :</span></span>
  - <span data-ttu-id="90095-428">Autorisation de blocage de l' **expéditeur** activée : le bouton **bloquer l’expéditeur** est disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-428">**Block sender** permission enabled: The **Block sender** button is available.</span></span>
  - <span data-ttu-id="90095-429">Autorisation de blocage de l' **expéditeur** désactivée : le bouton **bloquer l’expéditeur** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-429">**Block sender** permission disabled: The **Block sender** button is not available.</span></span>

- <span data-ttu-id="90095-430">**Notifications de courrier indésirable de l’utilisateur final** :</span><span class="sxs-lookup"><span data-stu-id="90095-430">**End-user spam notifications** :</span></span>
  - <span data-ttu-id="90095-431">Autorisation de blocage de l' **expéditeur** désactivée : le bouton **bloquer l’expéditeur** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-431">**Block sender** permission disabled: The **Block sender** button is not available.</span></span>
  - <span data-ttu-id="90095-432">Autorisation de blocage de l' **expéditeur** activée : le bouton **bloquer l’expéditeur** est disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-432">**Block sender** permission enabled: The **Block sender** button is available.</span></span>

<span data-ttu-id="90095-433">Pour plus d’informations sur la liste des expéditeurs bloqués, voir [bloquer les messages de quelqu’un](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379667) et [utiliser Exchange Online PowerShell pour configurer la collection de listes fiables sur une boîte aux lettres](https://docs.microsoft.com/microsoft-365/security/office-365-security/configure-junk-email-settings-on-exo-mailboxes#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox).</span><span class="sxs-lookup"><span data-stu-id="90095-433">For more information about the Blocked Senders list, see [Block messages from someone](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379667) and [Use Exchange Online PowerShell to configure the safelist collection on a mailbox](https://docs.microsoft.com/microsoft-365/security/office-365-security/configure-junk-email-settings-on-exo-mailboxes#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox).</span></span>

### <a name="delete-permission"></a><span data-ttu-id="90095-434">Autorisations de suppression</span><span class="sxs-lookup"><span data-stu-id="90095-434">Delete permission</span></span>

<span data-ttu-id="90095-435">L’autorisation de **suppression** ( _PermissionToDelete_ ) contrôle la possibilité pour les utilisateurs de supprimer leurs messages (messages dans lesquels l’utilisateur est un destinataire) de la mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="90095-435">The **Delete** permission ( _PermissionToDelete_ ) controls the ability to of users to delete their messages (messages where the user is a recipient) from quarantine.</span></span>

- <span data-ttu-id="90095-436">**Détails du message en quarantaine** :</span><span class="sxs-lookup"><span data-stu-id="90095-436">**Quarantined message details** :</span></span>
  - <span data-ttu-id="90095-437">Autorisation de **suppression** activée : le bouton **supprimer de la quarantaine** est disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-437">**Delete** permission enabled: The **Remove from quarantine** button is available.</span></span>
  - <span data-ttu-id="90095-438">Autorisation de **suppression** désactivée : le bouton **supprimer du contrôle** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-438">**Delete** permission disabled: The **Remove from quarantine** button is not available.</span></span>

- <span data-ttu-id="90095-439">**Notifications de courrier indésirable de l’utilisateur final** : aucun effet.</span><span class="sxs-lookup"><span data-stu-id="90095-439">**End-user spam notifications** : No effect.</span></span>

### <a name="preview-permission"></a><span data-ttu-id="90095-440">Autorisation d’aperçu</span><span class="sxs-lookup"><span data-stu-id="90095-440">Preview permission</span></span>

<span data-ttu-id="90095-441">L’autorisation **preview** ( _PermissionToPreview_ ) contrôle la possibilité pour les utilisateurs de prévisualiser leurs messages en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="90095-441">The **Preview** permission ( _PermissionToPreview_ ) controls the ability to of users to preview their messages in quarantine.</span></span>

- <span data-ttu-id="90095-442">**Détails du message en quarantaine** :</span><span class="sxs-lookup"><span data-stu-id="90095-442">**Quarantined message details** :</span></span>
  - <span data-ttu-id="90095-443">Autorisation d' **Aperçu** activée : le bouton **Aperçu du message** est disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-443">**Preview** permission enabled: The **Preview message** button is available.</span></span>
  - <span data-ttu-id="90095-444">Autorisation d' **Aperçu** désactivée : le bouton **Aperçu du message** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-444">**Preview** permission disabled: The **Preview message** button is not available.</span></span>

- <span data-ttu-id="90095-445">**Notifications de courrier indésirable de l’utilisateur final** : aucun effet.</span><span class="sxs-lookup"><span data-stu-id="90095-445">**End-user spam notifications** : No effect.</span></span>

#### <a name="allow-recipients-to-release-a-message-from-quarantine-permission"></a><span data-ttu-id="90095-446">Autoriser les destinataires à libérer un message à partir de l’autorisation de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="90095-446">Allow recipients to release a message from quarantine permission</span></span>

<span data-ttu-id="90095-447">L’autorisation **autoriser les destinataires à libérer un message à partir de la quarantaine** ( _PermissionToRelease_ ) contrôle la capacité des utilisateurs à libérer leurs messages mis en quarantaine directement et sans l’approbation d’un administrateur.</span><span class="sxs-lookup"><span data-stu-id="90095-447">The **Allow recipients to release a message from quarantine** permission ( _PermissionToRelease_ ) controls the ability of users to release their quarantined messages directly and without the approval of an admin.</span></span>

- <span data-ttu-id="90095-448">**Détails du message en quarantaine** :</span><span class="sxs-lookup"><span data-stu-id="90095-448">**Quarantined message details** :</span></span>
  - <span data-ttu-id="90095-449">Autorisation activée : le bouton **diffuser le message** est disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-449">Permission enabled: The **Release message** button is available.</span></span>
  - <span data-ttu-id="90095-450">Autorisation désactivée : le bouton **diffuser le message** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-450">Permission disabled: The **Release message** button is not available.</span></span>
  
- <span data-ttu-id="90095-451">**Notifications de courrier indésirable de l’utilisateur final** :</span><span class="sxs-lookup"><span data-stu-id="90095-451">**End-user spam notifications** :</span></span>
  - <span data-ttu-id="90095-452">Autorisation activée : le bouton de **publication** est disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-452">Permission enabled: The **Release** button is available.</span></span>
  - <span data-ttu-id="90095-453">Autorisation désactivée : le bouton de **publication** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-453">Permission disabled: The **Release** button is not available.</span></span>

#### <a name="allow-recipients-to-request-a-message-to-be-released-from-quarantine-permission"></a><span data-ttu-id="90095-454">Autoriser les destinataires à demander la libération d’un message à partir de l’autorisation de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="90095-454">Allow recipients to request a message to be released from quarantine permission</span></span>

<span data-ttu-id="90095-455">L’option **autoriser les destinataires à demander la libération d’un message à partir de l’autorisation de mise en quarantaine** ( _PermissionToRequestRelease_ ) contrôle la capacité des utilisateurs à _demander_ la libération de leurs messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="90095-455">The **Allow recipients to request a message to be released from quarantine** permission ( _PermissionToRequestRelease_ ) controls the ability of users to _request_ the release of their quarantined messages.</span></span> <span data-ttu-id="90095-456">Le message n’est publié qu’après qu’un administrateur a approuvé la demande.</span><span class="sxs-lookup"><span data-stu-id="90095-456">The message is only released after an admin approves the request.</span></span>

- <span data-ttu-id="90095-457">**Détails du message en quarantaine** :</span><span class="sxs-lookup"><span data-stu-id="90095-457">**Quarantined message details** :</span></span>
  - <span data-ttu-id="90095-458">Autorisation activée : le bouton de lancement de la **demande** est disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-458">Permission enabled: The **Request release** button is available.</span></span>
  - <span data-ttu-id="90095-459">Autorisation désactivée : le bouton de libération de la **demande** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-459">Permission disabled: The **Request release** button is not available.</span></span>

- <span data-ttu-id="90095-460">**Notifications de courrier indésirable de l’utilisateur final** : le bouton de **publication** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="90095-460">**End-user spam notifications** : The **Release** button is not available.</span></span>
