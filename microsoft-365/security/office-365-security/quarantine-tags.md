---
title: Stratégies de mise en quarantaine
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
description: Les administrateurs peuvent apprendre à utiliser des stratégies de mise en quarantaine pour contrôler ce que les utilisateurs peuvent faire pour leurs messages mis en quarantaine.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 96dc1e2158787457884ca6a3c6f27bf76e83a369
ms.sourcegitcommit: fa9efab24a84f71fec7d001f2ad8949125fa8eee
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2021
ms.locfileid: "53055217"
---
# <a name="quarantine-policies"></a><span data-ttu-id="00b91-103">Stratégies de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="00b91-103">Quarantine policies</span></span>

> [!NOTE]
> <span data-ttu-id="00b91-104">Les fonctionnalités décrites dans cet article sont actuellement en prévisualisation, ne sont pas disponibles pour tout le monde et peuvent faire l’objet de changements.</span><span class="sxs-lookup"><span data-stu-id="00b91-104">The features that are described in this article are currently in Preview, aren't available to everyone, and are subject to change.</span></span>

<span data-ttu-id="00b91-105">Les stratégies de mise en quarantaine (auparavant appelées balises de mise en quarantaine) dans Exchange Online Protection (EOP) permettent aux administrateurs de contrôler ce que les utilisateurs sont en mesure de faire pour leurs messages mis en quarantaine en fonction de la façon dont le message est arrivé en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="00b91-105">Quarantine policies (formerly known as quarantine tags) in Exchange Online Protection (EOP) allow admins to control what users are able to do to their quarantined messages based on how the message arrived in quarantine.</span></span>

<span data-ttu-id="00b91-106">EOP a traditionnellement autorisé ou empêché certains niveaux d’interactivité pour les messages en quarantaine et dans les notifications de courrier indésirable de [l’utilisateur final.](use-spam-notifications-to-release-and-report-quarantined-messages.md) [](find-and-release-quarantined-messages-as-a-user.md)</span><span class="sxs-lookup"><span data-stu-id="00b91-106">EOP has traditionally allowed or prevented certain levels of interactivity for messages in [quarantine](find-and-release-quarantined-messages-as-a-user.md) and in [end-user spam notifications](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span> <span data-ttu-id="00b91-107">Par exemple, les utilisateurs peuvent afficher et libérer les messages mis en quarantaine par le filtrage anti-courrier indésirable en tant que courrier indésirable ou en bloc, mais ils ne peuvent pas afficher ou libérer les messages mis en quarantaine comme hameçonnage à haut niveau de confiance (seuls les administrateurs peuvent le faire).</span><span class="sxs-lookup"><span data-stu-id="00b91-107">For example, users can view and release messages that were quarantined by anti-spam filtering as spam or bulk, but they can't view or release messages that were quarantined as high confidence phishing (only admins can do that).</span></span>

<span data-ttu-id="00b91-108">Pour les fonctionnalités de [protection](#step-2-assign-a-quarantine-policy-to-supported-features)prise en charge, les stratégies de mise en quarantaine spécifient ce que les utilisateurs sont autorisés à faire dans les messages de notification de courrier indésirable de l’utilisateur final et dans leurs messages mis en quarantaine en quarantaine (messages dont l’utilisateur est un destinataire).</span><span class="sxs-lookup"><span data-stu-id="00b91-108">For [supported protection features](#step-2-assign-a-quarantine-policy-to-supported-features), quarantine policies specify what users are allowed to do in end-user spam notification messages and in their quarantined messages in quarantine (messages where the user is a recipient).</span></span> <span data-ttu-id="00b91-109">Les stratégies de mise en quarantaine par défaut sont automatiquement affectées pour appliquer les fonctionnalités historiques pour les utilisateurs sur les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="00b91-109">Default quarantine policies are automatically assigned to enforce the historical capabilities for users on quarantined messages.</span></span> <span data-ttu-id="00b91-110">Vous pouvez également créer et affecter des stratégies de mise en quarantaine personnalisées pour autoriser ou empêcher les utilisateurs finaux d’effectuer des actions spécifiques sur les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="00b91-110">Or, you can create and assign custom quarantine policies to allow or prevent end users from performing specific actions on quarantined messages.</span></span>

<span data-ttu-id="00b91-111">Les autorisations individuelles sont combinées dans les groupes d’autorisations prédéfiny suivants :</span><span class="sxs-lookup"><span data-stu-id="00b91-111">The individual permissions are combined into the following preset permission groups:</span></span>

- <span data-ttu-id="00b91-112">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="00b91-112">No access</span></span>
- <span data-ttu-id="00b91-113">Accès limité</span><span class="sxs-lookup"><span data-stu-id="00b91-113">Limited access</span></span>
- <span data-ttu-id="00b91-114">Accès total</span><span class="sxs-lookup"><span data-stu-id="00b91-114">Full access</span></span>

<span data-ttu-id="00b91-115">Les autorisations individuelles disponibles et les autorisations incluses ou non dans les groupes d’autorisations prédéfinits sont décrites dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="00b91-115">The available individual permissions and what's included or not included in the preset permission groups are described in the following table:</span></span>

<br>

****

|<span data-ttu-id="00b91-116">Autorisation</span><span class="sxs-lookup"><span data-stu-id="00b91-116">Permission</span></span>|<span data-ttu-id="00b91-117">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="00b91-117">No access</span></span>|<span data-ttu-id="00b91-118">Accès limité</span><span class="sxs-lookup"><span data-stu-id="00b91-118">Limited access</span></span>|<span data-ttu-id="00b91-119">Accès total</span><span class="sxs-lookup"><span data-stu-id="00b91-119">Full access</span></span>|
|---|:---:|:---:|:---:|
|<span data-ttu-id="00b91-120">**Autoriser l’expéditeur** (_PermissionToAllowSender_)</span><span class="sxs-lookup"><span data-stu-id="00b91-120">**Allow sender** (_PermissionToAllowSender_)</span></span>|||![Coche](../../media/checkmark.png)|
|<span data-ttu-id="00b91-122">**Bloquer l’expéditeur** (_PermissionToBlockSender_)</span><span class="sxs-lookup"><span data-stu-id="00b91-122">**Block sender** (_PermissionToBlockSender_)</span></span>||![Coche](../../media/checkmark.png)|![Coche](../../media/checkmark.png)|
|<span data-ttu-id="00b91-125">**Delete** (_PermissionToDelete_)</span><span class="sxs-lookup"><span data-stu-id="00b91-125">**Delete** (_PermissionToDelete_)</span></span>||![Coche](../../media/checkmark.png)|![Coche](../../media/checkmark.png)|
|<span data-ttu-id="00b91-128">**Preview** (_PermissionToPreview_)</span><span class="sxs-lookup"><span data-stu-id="00b91-128">**Preview** (_PermissionToPreview_)</span></span>||![Coche](../../media/checkmark.png)|![Coche](../../media/checkmark.png)|
|<span data-ttu-id="00b91-131">**Autoriser les destinataires à libérer un message de la quarantaine** (_PermissionToRelease_)</span><span class="sxs-lookup"><span data-stu-id="00b91-131">**Allow recipients to release a message from quarantine** (_PermissionToRelease_)</span></span>|||![Coche](../../media/checkmark.png)|
|<span data-ttu-id="00b91-133">**Autoriser les destinataires à demander qu’un message** soit libéré de la quarantaine (_PermissionToRequestRelease_)</span><span class="sxs-lookup"><span data-stu-id="00b91-133">**Allow recipients to request a message to be released from quarantine** (_PermissionToRequestRelease_)</span></span>||![Coche](../../media/checkmark.png)||
|

<span data-ttu-id="00b91-135">Si vous n’aimez pas les autorisations par défaut dans les groupes d’autorisations prédéfin produits, vous pouvez utiliser des autorisations personnalisées lorsque vous créez ou modifiez des stratégies de mise en quarantaine personnalisées.</span><span class="sxs-lookup"><span data-stu-id="00b91-135">If you don't like the default permissions in the preset permission groups, you can use custom permissions when you create or modify custom quarantine policies.</span></span> <span data-ttu-id="00b91-136">Pour plus d’informations sur l’objet de chaque autorisation, consultez la section Détails des [autorisations](#quarantine-policy-permission-details) de stratégie de mise en quarantaine plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="00b91-136">For more information about what each permission does, see the [Quarantine policy permission details](#quarantine-policy-permission-details) section later in this article.</span></span>

<span data-ttu-id="00b91-137">Vous créez et affectez des stratégies de mise en quarantaine dans le portail Microsoft 365 Defender ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres Exchange Online ; EOP PowerShell autonome dans les organisations EOP sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="00b91-137">You create and assign quarantine policies in the Microsoft 365 Defender portal or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with Exchange Online Mailboxes; standalone EOP PowerShell in EOP organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="00b91-138">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="00b91-138">What do you need to know before you begin?</span></span>

- <span data-ttu-id="00b91-139">Vous ouvrez le Portail Microsoft 365 Defender sur <https://security.microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="00b91-139">You open the Microsoft 365 Defender portal at <https://security.microsoft.com>.</span></span> <span data-ttu-id="00b91-140">Ou pour aller directement à la page Des stratégies **de** mise en quarantaine, ouvrez <https://security.microsoft.com/quarantineTags> .</span><span class="sxs-lookup"><span data-stu-id="00b91-140">Or to go directly to the **Quarantine policies** page, open <https://security.microsoft.com/quarantineTags>.</span></span>

- <span data-ttu-id="00b91-141">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="00b91-141">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="00b91-142">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="00b91-142">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="00b91-143">Pour afficher, créer, modifier ou supprimer des stratégies de  mise  en quarantaine, vous devez être membre des rôles Gestion de l’organisation ou Administrateur de la sécurité dans le portail Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="00b91-143">To view, create, modify, or remove quarantine policies, you need to be a member of the **Organization Management** or **Security Administrator** roles in the Microsoft 365 Defender portal.</span></span> <span data-ttu-id="00b91-144">Pour plus d’informations, consultez [Autorisations dans le portail Microsoft 365 Defender](permissions-microsoft-365-security-center.md).</span><span class="sxs-lookup"><span data-stu-id="00b91-144">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-microsoft-365-security-center.md).</span></span>

## <a name="step-1-create-quarantine-policies-in-the-microsoft-365-defender-portal"></a><span data-ttu-id="00b91-145">Étape 1 : Créer des stratégies de mise en quarantaine dans le portail Microsoft 365 Defender de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="00b91-145">Step 1: Create quarantine policies in the Microsoft 365 Defender portal</span></span>

1. <span data-ttu-id="00b91-146">Dans le portail Microsoft 365 Defender, sélectionnez Stratégies de mise en quarantaine & stratégies de **collaboration** sur les menaces, puis \>  \>  \>  sélectionnez **Stratégies de mise en quarantaine.**</span><span class="sxs-lookup"><span data-stu-id="00b91-146">In the Microsoft 365 Defender portal, go to **Email & collaboration** \>**Threat policies** \> **Rules** section \> **Quarantine policies** and then select **Quarantine policies**.</span></span>

2. <span data-ttu-id="00b91-147">Dans la page **Stratégie de** mise en quarantaine, cliquez sur Ajouter une icône de stratégie personnalisée Ajouter une ![ stratégie ](../../media/m365-cc-sc-create-icon.png) **personnalisée.**</span><span class="sxs-lookup"><span data-stu-id="00b91-147">On the **Quarantine policy** page, click ![Add custom policy icon](../../media/m365-cc-sc-create-icon.png) **Add custom policy**.</span></span>

3. <span data-ttu-id="00b91-148">**L’Assistant Nouvelle stratégie** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="00b91-148">The **New policy** wizard opens.</span></span> <span data-ttu-id="00b91-149">Dans la page **Nom de la** stratégie, entrez un nom court mais unique dans la zone Nom de **la** stratégie.</span><span class="sxs-lookup"><span data-stu-id="00b91-149">On the **Policy name** page, enter a brief but unique name in the **Policy name** box.</span></span> <span data-ttu-id="00b91-150">Vous devez identifier et sélectionner la stratégie de mise en quarantaine par nom dans les étapes à venir.</span><span class="sxs-lookup"><span data-stu-id="00b91-150">You'll need to identify and select the quarantine policy by name in upcoming steps.</span></span> <span data-ttu-id="00b91-151">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="00b91-151">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="00b91-152">Dans la page **d’accès aux messages du** destinataire, sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="00b91-152">On the **Recipient message access** page, select one of the following values:</span></span>
   - <span data-ttu-id="00b91-153">**Aucun accès**</span><span class="sxs-lookup"><span data-stu-id="00b91-153">**No access**</span></span>
   - <span data-ttu-id="00b91-154">**Accès limité**</span><span class="sxs-lookup"><span data-stu-id="00b91-154">**Limited access**</span></span>
   - <span data-ttu-id="00b91-155">**Accès total**</span><span class="sxs-lookup"><span data-stu-id="00b91-155">**Full access**</span></span>

   <span data-ttu-id="00b91-156">Les autorisations individuelles incluses dans ces groupes d’autorisations sont décrites plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="00b91-156">The individual permissions that are included in these permission groups are described earlier in this article.</span></span>

   <span data-ttu-id="00b91-157">Pour spécifier des autorisations personnalisées, sélectionnez Définir un accès spécifique **(Avancé)** et configurez les paramètres suivants qui s’affichent :</span><span class="sxs-lookup"><span data-stu-id="00b91-157">To specify custom permissions, select **Set specific access (Advanced)** and the configure the following settings that appear:</span></span>

     - <span data-ttu-id="00b91-158">**Sélectionnez la préférence d’action de** publication : sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="00b91-158">**Select release action preference**: Select one of the following values:</span></span>
       - <span data-ttu-id="00b91-159">**Aucune action de publication**: il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="00b91-159">**No release action**: This is the default value.</span></span>
       - <span data-ttu-id="00b91-160">**Autoriser les destinataires à libérer un message de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="00b91-160">**Allow recipients to release a message from quarantine**</span></span>
       - <span data-ttu-id="00b91-161">**Autoriser les destinataires à demander qu’un message soit libéré de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="00b91-161">**Allow recipients to request a message to be released from quarantine**</span></span>
     - <span data-ttu-id="00b91-162">**Sélectionnez des actions supplémentaires que les destinataires peuvent prendre** sur les messages mis en quarantaine : sélectionnez une partie, l’ensemble ou aucune des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="00b91-162">**Select additional actions recipients can take on quarantined messages**: Select some, all, or none of the following values:</span></span>
       - <span data-ttu-id="00b91-163">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="00b91-163">**Delete**</span></span>
       - <span data-ttu-id="00b91-164">**Aperçu**</span><span class="sxs-lookup"><span data-stu-id="00b91-164">**Preview**</span></span>
       - <span data-ttu-id="00b91-165">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="00b91-165">**Block sender**</span></span>

   <span data-ttu-id="00b91-166">Ces autorisations et leur effet sur les messages mis en quarantaine et dans les notifications de courrier indésirable de l’utilisateur final sont décrits dans la section détails des [autorisations](#quarantine-policy-permission-details) de stratégie de mise en quarantaine plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="00b91-166">These permissions and their effect on quarantined messages and in end-user spam notifications are described in the [Quarantine policy permission details](#quarantine-policy-permission-details) section later in this article.</span></span>

   <span data-ttu-id="00b91-167">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="00b91-167">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="00b91-168">Dans la page **Examiner la stratégie** qui s’affiche, examinez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="00b91-168">On the **Review policy** page that appears, review your settings.</span></span> <span data-ttu-id="00b91-169">Vous pouvez sélectionner **Modifier** dans chaque section pour modifier les paramètres de la section.</span><span class="sxs-lookup"><span data-stu-id="00b91-169">You can select **Edit** in each section to modify the settings within the section.</span></span> <span data-ttu-id="00b91-170">Vous pouvez également cliquer sur **Précédent** ou sélectionner la page spécifique dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="00b91-170">Or you can click **Back** or select the specific page in the wizard.</span></span>

   <span data-ttu-id="00b91-171">Lorsque vous avez terminé, cliquez sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="00b91-171">When you're finished, click **Submit**.</span></span>

6. <span data-ttu-id="00b91-172">Dans la page de confirmation qui s’affiche, cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="00b91-172">On the confirmation page that appears, click **Done**.</span></span>

<span data-ttu-id="00b91-173">Vous êtes maintenant prêt à affecter la stratégie de mise en quarantaine à une fonctionnalité de mise en quarantaine, comme décrit dans la section [Étape 2.](#step-2-assign-a-quarantine-policy-to-supported-features)</span><span class="sxs-lookup"><span data-stu-id="00b91-173">Now you're ready to assign the quarantine policy to a quarantine feature as described in the [Step 2](#step-2-assign-a-quarantine-policy-to-supported-features) section.</span></span>

### <a name="create-quarantine-policies-in-powershell"></a><span data-ttu-id="00b91-174">Créer des stratégies de mise en quarantaine dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="00b91-174">Create quarantine policies in PowerShell</span></span>

<span data-ttu-id="00b91-175">Si vous préférez utiliser PowerShell pour créer des stratégies de mise en quarantaine, connectez-vous à Exchange Online PowerShell ou Exchange Online Protection PowerShell et utilisez la cmdlet **New-QuarantineTag.**</span><span class="sxs-lookup"><span data-stu-id="00b91-175">If you'd rather use PowerShell to create quarantine policies, connect to Exchange Online PowerShell or Exchange Online Protection PowerShell and use the **New-QuarantineTag** cmdlet.</span></span> <span data-ttu-id="00b91-176">Vous avez le choix entre deux méthodes différentes :</span><span class="sxs-lookup"><span data-stu-id="00b91-176">You have two different methods to choose from:</span></span>

- <span data-ttu-id="00b91-177">Utilisez le _paramètre EndUserQuarantinePermissionsValue._</span><span class="sxs-lookup"><span data-stu-id="00b91-177">Use the _EndUserQuarantinePermissionsValue_ parameter.</span></span>
- <span data-ttu-id="00b91-178">Utilisez le _paramètre EndUserQuarantinePermissions._</span><span class="sxs-lookup"><span data-stu-id="00b91-178">Use the _EndUserQuarantinePermissions_ parameter.</span></span>

<span data-ttu-id="00b91-179">Ces méthodes sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="00b91-179">These methods are described in the following sections.</span></span>

#### <a name="use-the-enduserquarantinepermissionsvalue-parameter"></a><span data-ttu-id="00b91-180">Utiliser le paramètre EndUserQuarantinePermissionsValue</span><span class="sxs-lookup"><span data-stu-id="00b91-180">Use the EndUserQuarantinePermissionsValue parameter</span></span>

<span data-ttu-id="00b91-181">Pour créer une stratégie de mise en quarantaine à l’aide du paramètre _EndUserQuarantinePermissionsValue,_ utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="00b91-181">To create a quarantine policy using the _EndUserQuarantinePermissionsValue_ parameter, use the following syntax:</span></span>

```powershell
New-QuarantineTag -Name "<UniqueName>" -EndUserQuarantinePermissionsValue <0 to 236>
```

<span data-ttu-id="00b91-182">Le _paramètre EndUserQuarantinePermissionsValue_ utilise une valeur décimale convertie à partir d’une valeur binaire.</span><span class="sxs-lookup"><span data-stu-id="00b91-182">The _EndUserQuarantinePermissionsValue_ parameter uses a decimal value that's converted from a binary value.</span></span> <span data-ttu-id="00b91-183">La valeur binaire correspond aux autorisations de mise en quarantaine de l’utilisateur final disponibles dans un ordre spécifique.</span><span class="sxs-lookup"><span data-stu-id="00b91-183">The binary value corresponds to the available end-user quarantine permissions in a specific order.</span></span> <span data-ttu-id="00b91-184">Pour chaque autorisation, la valeur 1 est égale à True et la valeur 0 à False.</span><span class="sxs-lookup"><span data-stu-id="00b91-184">For each permission, the value 1 equals True and the value 0 equals False.</span></span>

<span data-ttu-id="00b91-185">L’ordre et les valeurs requis pour chaque autorisation individuelle dans les groupes d’autorisations prédéfinits sont décrits dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="00b91-185">The required order and values for each individual permission in preset permission groups are described in the following table:</span></span>

<br>

****

|<span data-ttu-id="00b91-186">Autorisation</span><span class="sxs-lookup"><span data-stu-id="00b91-186">Permission</span></span>|<span data-ttu-id="00b91-187">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="00b91-187">No access</span></span>|<span data-ttu-id="00b91-188">Accès limité</span><span class="sxs-lookup"><span data-stu-id="00b91-188">Limited access</span></span>|<span data-ttu-id="00b91-189">Accès total</span><span class="sxs-lookup"><span data-stu-id="00b91-189">Full access</span></span>|
|---|:---:|:---:|:---:|
|<span data-ttu-id="00b91-190">PermissionToAllowSender</span><span class="sxs-lookup"><span data-stu-id="00b91-190">PermissionToAllowSender</span></span>|<span data-ttu-id="00b91-191">0</span><span class="sxs-lookup"><span data-stu-id="00b91-191">0</span></span>|<span data-ttu-id="00b91-192">0</span><span class="sxs-lookup"><span data-stu-id="00b91-192">0</span></span>|<span data-ttu-id="00b91-193">1</span><span class="sxs-lookup"><span data-stu-id="00b91-193">1</span></span>|
|<span data-ttu-id="00b91-194">PermissionToBlockSender</span><span class="sxs-lookup"><span data-stu-id="00b91-194">PermissionToBlockSender</span></span>|<span data-ttu-id="00b91-195">0</span><span class="sxs-lookup"><span data-stu-id="00b91-195">0</span></span>|<span data-ttu-id="00b91-196">1</span><span class="sxs-lookup"><span data-stu-id="00b91-196">1</span></span>|<span data-ttu-id="00b91-197">1</span><span class="sxs-lookup"><span data-stu-id="00b91-197">1</span></span>|
|<span data-ttu-id="00b91-198">PermissionToDelete</span><span class="sxs-lookup"><span data-stu-id="00b91-198">PermissionToDelete</span></span>|<span data-ttu-id="00b91-199">0</span><span class="sxs-lookup"><span data-stu-id="00b91-199">0</span></span>|<span data-ttu-id="00b91-200">1</span><span class="sxs-lookup"><span data-stu-id="00b91-200">1</span></span>|<span data-ttu-id="00b91-201">1</span><span class="sxs-lookup"><span data-stu-id="00b91-201">1</span></span>|
|<span data-ttu-id="00b91-202">PermissionToDownload<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="00b91-202">PermissionToDownload<sup>\*</sup></span></span>|<span data-ttu-id="00b91-203">0</span><span class="sxs-lookup"><span data-stu-id="00b91-203">0</span></span>|<span data-ttu-id="00b91-204">0</span><span class="sxs-lookup"><span data-stu-id="00b91-204">0</span></span>|<span data-ttu-id="00b91-205">0</span><span class="sxs-lookup"><span data-stu-id="00b91-205">0</span></span>|
|<span data-ttu-id="00b91-206">PermissionToPreview</span><span class="sxs-lookup"><span data-stu-id="00b91-206">PermissionToPreview</span></span>|<span data-ttu-id="00b91-207">0</span><span class="sxs-lookup"><span data-stu-id="00b91-207">0</span></span>|<span data-ttu-id="00b91-208">1</span><span class="sxs-lookup"><span data-stu-id="00b91-208">1</span></span>|<span data-ttu-id="00b91-209">1</span><span class="sxs-lookup"><span data-stu-id="00b91-209">1</span></span>|
|<span data-ttu-id="00b91-210">PermissionToRelease<sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="00b91-210">PermissionToRelease<sup>\*\*</sup></span></span>|<span data-ttu-id="00b91-211">0</span><span class="sxs-lookup"><span data-stu-id="00b91-211">0</span></span>|<span data-ttu-id="00b91-212">0</span><span class="sxs-lookup"><span data-stu-id="00b91-212">0</span></span>|<span data-ttu-id="00b91-213">1</span><span class="sxs-lookup"><span data-stu-id="00b91-213">1</span></span>|
|<span data-ttu-id="00b91-214">PermissionToRequestRelease<sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="00b91-214">PermissionToRequestRelease<sup>\*\*</sup></span></span>|<span data-ttu-id="00b91-215">0</span><span class="sxs-lookup"><span data-stu-id="00b91-215">0</span></span>|<span data-ttu-id="00b91-216">1</span><span class="sxs-lookup"><span data-stu-id="00b91-216">1</span></span>|<span data-ttu-id="00b91-217">0</span><span class="sxs-lookup"><span data-stu-id="00b91-217">0</span></span>|
|<span data-ttu-id="00b91-218">PermissionToViewHeader<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="00b91-218">PermissionToViewHeader<sup>\*</sup></span></span>|<span data-ttu-id="00b91-219">0</span><span class="sxs-lookup"><span data-stu-id="00b91-219">0</span></span>|<span data-ttu-id="00b91-220">0</span><span class="sxs-lookup"><span data-stu-id="00b91-220">0</span></span>|<span data-ttu-id="00b91-221">0</span><span class="sxs-lookup"><span data-stu-id="00b91-221">0</span></span>|
|<span data-ttu-id="00b91-222">Valeur binaire</span><span class="sxs-lookup"><span data-stu-id="00b91-222">Binary value</span></span>|<span data-ttu-id="00b91-223">00000000</span><span class="sxs-lookup"><span data-stu-id="00b91-223">00000000</span></span>|<span data-ttu-id="00b91-224">01101010</span><span class="sxs-lookup"><span data-stu-id="00b91-224">01101010</span></span>|<span data-ttu-id="00b91-225">11101100</span><span class="sxs-lookup"><span data-stu-id="00b91-225">11101100</span></span>|
|<span data-ttu-id="00b91-226">Valeur décimale à utiliser</span><span class="sxs-lookup"><span data-stu-id="00b91-226">Decimal value to use</span></span>|<span data-ttu-id="00b91-227">0</span><span class="sxs-lookup"><span data-stu-id="00b91-227">0</span></span>|<span data-ttu-id="00b91-228">106</span><span class="sxs-lookup"><span data-stu-id="00b91-228">106</span></span>|<span data-ttu-id="00b91-229">236</span><span class="sxs-lookup"><span data-stu-id="00b91-229">236</span></span>|
|

<span data-ttu-id="00b91-230"><sup>\*</sup> Actuellement, cette valeur est toujours 0.</span><span class="sxs-lookup"><span data-stu-id="00b91-230"><sup>\*</sup> Currently, this value is always 0.</span></span> <span data-ttu-id="00b91-231">Pour PermissionToViewHeader, la valeur 0 ne masque pas le bouton Afficher l’en-tête du **message** dans les détails du message mis en quarantaine (le bouton est toujours disponible).</span><span class="sxs-lookup"><span data-stu-id="00b91-231">For PermissionToViewHeader, the value 0 doesn't hide the **View message header** button in the details of the quarantined message (the button is always available).</span></span>

<span data-ttu-id="00b91-232"><sup>\*\*</sup> Ne définissez pas ces deux valeurs sur 1.</span><span class="sxs-lookup"><span data-stu-id="00b91-232"><sup>\*\*</sup> Don't set both of these values to 1.</span></span> <span data-ttu-id="00b91-233">Définissez l’un sur 1 et l’autre sur 0, ou définissez les deux sur 0.</span><span class="sxs-lookup"><span data-stu-id="00b91-233">Set one to 1 and the other to 0, or set both to 0.</span></span>

<span data-ttu-id="00b91-234">Cet exemple crée un nouveau nom de stratégie de mise en quarantaine NoAccess qui attribue les autorisations d’accès Non, comme décrit dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="00b91-234">This example creates a new quarantine policy name NoAccess that assigns the No access permissions as described in the previous table.</span></span>

```powershell
New-QuarantineTag -Name NoAccess -EndUserQuarantinePermissionsValue 0
```

<span data-ttu-id="00b91-235">Pour les autorisations d’accès limité, utilisez la valeur 106.</span><span class="sxs-lookup"><span data-stu-id="00b91-235">For Limited access permissions, use the value 106.</span></span> <span data-ttu-id="00b91-236">Pour les autorisations d’accès total, utilisez la valeur 236.</span><span class="sxs-lookup"><span data-stu-id="00b91-236">For Full access permissions, use the value 236.</span></span>

<span data-ttu-id="00b91-237">Pour les autorisations personnalisées, utilisez le tableau précédent pour obtenir la valeur binaire qui correspond aux autorisations de votre choix.</span><span class="sxs-lookup"><span data-stu-id="00b91-237">For custom permissions, use the previous table to get the binary value that corresponds to the permissions you want.</span></span> <span data-ttu-id="00b91-238">Convertissez la valeur binaire en valeur décimale et utilisez la valeur décimale pour le paramètre _EndUserQuarantinePermissionsValue._</span><span class="sxs-lookup"><span data-stu-id="00b91-238">Convert the binary value to a decimal value and use the decimal value for the _EndUserQuarantinePermissionsValue_ parameter.</span></span>

<span data-ttu-id="00b91-239">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-QuarantineTag](/powershell/module/exchange/new-quarantinetag).</span><span class="sxs-lookup"><span data-stu-id="00b91-239">For detailed syntax and parameter information, see [New-QuarantineTag](/powershell/module/exchange/new-quarantinetag).</span></span>

#### <a name="use-the-enduserquarantinepermissions-parameter"></a><span data-ttu-id="00b91-240">Utiliser le paramètre EndUserQuarantinePermissions</span><span class="sxs-lookup"><span data-stu-id="00b91-240">Use the EndUserQuarantinePermissions parameter</span></span>

<span data-ttu-id="00b91-241">Pour créer une stratégie de mise en quarantaine à l’aide du paramètre _EndUserQuarantinePermissionsValue,_ utilisez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="00b91-241">To create a quarantine policy using the _EndUserQuarantinePermissionsValue_ parameter, do the following steps:</span></span>

<span data-ttu-id="00b91-242">A.</span><span class="sxs-lookup"><span data-stu-id="00b91-242">A.</span></span> <span data-ttu-id="00b91-243">Stockez un objet d’autorisations de mise en quarantaine dans une variable à l’aide de la cmdlet **New-QuarantinePermissions.**</span><span class="sxs-lookup"><span data-stu-id="00b91-243">Store a quarantine permissions object in a variable using the **New-QuarantinePermissions** cmdlet.</span></span>

<p>

<span data-ttu-id="00b91-244">B.</span><span class="sxs-lookup"><span data-stu-id="00b91-244">B.</span></span> <span data-ttu-id="00b91-245">Utilisez la variable comme valeur _EndUserQuarantinePermissions_ dans la **commande New-QuarantineTag.**</span><span class="sxs-lookup"><span data-stu-id="00b91-245">Use the variable as the _EndUserQuarantinePermissions_ value in the **New-QuarantineTag** command.</span></span>

##### <a name="step-a-store-a-quarantine-permissions-object-in-a-variable"></a><span data-ttu-id="00b91-246">Étape A : Stocker un objet d’autorisations de mise en quarantaine dans une variable</span><span class="sxs-lookup"><span data-stu-id="00b91-246">Step A: Store a quarantine permissions object in a variable</span></span>

<span data-ttu-id="00b91-247">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="00b91-247">Use the following syntax:</span></span>

```powershell
$<VariableName> = New-QuarantinePermissions [-PermissionToAllowSender <$true | $False>] [-PermissionToBlockSender <$true | $False>] [-PermissionToDelete <$true | $False>] [-PermissionToPreview <$true | $False>] [-PermissionToRelease <$true | $False>] [-PermissionToRequestRelease <$true | $False>]
```

<span data-ttu-id="00b91-248">La valeur par défaut pour tous les paramètres inutilisés est , vous devez donc utiliser uniquement les paramètres où vous souhaitez définir `$false` la valeur sur `$true` .</span><span class="sxs-lookup"><span data-stu-id="00b91-248">The default value for any unused parameters is `$false`, so you only need to use the parameters where you want to set value to `$true`.</span></span>

<span data-ttu-id="00b91-249">Les exemples suivants montrent comment créer des objets d’autorisation qui correspondent aux groupes d’autorisations prédéfins :</span><span class="sxs-lookup"><span data-stu-id="00b91-249">The following examples show how to create permission objects that correspond to the preset permissions groups:</span></span>

- <span data-ttu-id="00b91-250">**Aucun accès**:</span><span class="sxs-lookup"><span data-stu-id="00b91-250">**No access**:</span></span>

  ```powershell
  $NoAccess = New-QuarantinePermissions
  ```

- <span data-ttu-id="00b91-251">**Accès limité**:</span><span class="sxs-lookup"><span data-stu-id="00b91-251">**Limited access**:</span></span>

  ```powershell
  $LimitedAccess = New-QuarantinePermissions -PermissionToBlockSender $true -PermissionToDelete $true -PermissionToPreview $true -PermissionToRequestRelease $true
  ```

- <span data-ttu-id="00b91-252">**Accès total**:</span><span class="sxs-lookup"><span data-stu-id="00b91-252">**Full access**:</span></span>

  ```powershell
  $FullAccess = New-QuarantinePermissions -PermissionToAllowSender $true -PermissionToBlockSender $true -PermissionToDelete $true -PermissionToPreview $true -PermissionToRelease $true
  ```

<span data-ttu-id="00b91-253">Pour voir les valeurs que vous avez définies, exécutez le nom de la variable en tant que commande (par exemple, exécutez la `$NoAccess` commande).</span><span class="sxs-lookup"><span data-stu-id="00b91-253">To see the values that you've set, run the variable name as a command (for example, run the command `$NoAccess`).</span></span>

<span data-ttu-id="00b91-254">Pour les autorisations personnalisées, ne définissez pas les paramètres _PermissionToRelease_ et _PermissionToRequestRelease_ sur `$true` .</span><span class="sxs-lookup"><span data-stu-id="00b91-254">For custom permissions, don't set both the _PermissionToRelease_ and _PermissionToRequestRelease_ parameters to `$true`.</span></span> <span data-ttu-id="00b91-255">Définissez `$true` l’un sur et laissez l’autre en tant `$false` que , ou laissez les deux comme `$false` .</span><span class="sxs-lookup"><span data-stu-id="00b91-255">Set one to `$true` and leave the other as `$false`, or leave both as `$false`.</span></span>

<span data-ttu-id="00b91-256">Vous pouvez également modifier une variable objet d’autorisations existante après la création, mais avant de l’utiliser à l’aide de la cmdlet **Set-QuarantinePermissions.**</span><span class="sxs-lookup"><span data-stu-id="00b91-256">You can also modify an existing permissions object variable after you create but before you use it by using the **Set-QuarantinePermissions** cmdlet.</span></span>

<span data-ttu-id="00b91-257">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-QuarantinePermissions](/powershell/module/exchange/new-quarantinepermissions) et [Set-QuarantinePermissions.](/powershell/module/exchange/set-quarantinepermissions)</span><span class="sxs-lookup"><span data-stu-id="00b91-257">For detailed syntax and parameter information, see [New-QuarantinePermissions](/powershell/module/exchange/new-quarantinepermissions) and [Set-QuarantinePermissions](/powershell/module/exchange/set-quarantinepermissions).</span></span>

##### <a name="step-b-use-the-variable-in-the-new-quarantinetag-command"></a><span data-ttu-id="00b91-258">Étape B : Utiliser la variable dans la commande New-QuarantineTag commande</span><span class="sxs-lookup"><span data-stu-id="00b91-258">Step B: Use the variable in the New-QuarantineTag command</span></span>

<span data-ttu-id="00b91-259">Après avoir créé et stocké l’objet Permissions dans une variable, utilisez la variable pour la valeur du paramètre _EndUserQuarantinePermission_ dans la commande **New-QuarantineTag** suivante :</span><span class="sxs-lookup"><span data-stu-id="00b91-259">After you've created and stored the permissions object in a variable, use the variable for the _EndUserQuarantinePermission_ parameter value in the following **New-QuarantineTag** command:</span></span>

```powershell
New-QuarantineTag -Name "<UniqueName>" -EndUserQuarantinePermissions $<VariableName>
```

<span data-ttu-id="00b91-260">Cet exemple crée une stratégie de mise en quarantaine nommée LimitedAccess à l’aide de l’objet permissions qui a été décrit et créé `$LimitedAccess` à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="00b91-260">This example creates a new quarantine policy named LimitedAccess using the `$LimitedAccess` permissions object that was described and created in the previous step.</span></span>

```powershell
New-QuarantineTag -Name LimitedAccess -EndUserQuarantinePermissions $LimitedAccess
```

<span data-ttu-id="00b91-261">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-QuarantineTag](/powershell/module/exchange/new-quarantinetag).</span><span class="sxs-lookup"><span data-stu-id="00b91-261">For detailed syntax and parameter information, see [New-QuarantineTag](/powershell/module/exchange/new-quarantinetag).</span></span>

## <a name="step-2-assign-a-quarantine-policy-to-supported-features"></a><span data-ttu-id="00b91-262">Étape 2 : Attribuer une stratégie de mise en quarantaine aux fonctionnalités prise en charge</span><span class="sxs-lookup"><span data-stu-id="00b91-262">Step 2: Assign a quarantine policy to supported features</span></span>

<span data-ttu-id="00b91-263">Dans _les fonctionnalités_ de protection prises en charge qui met en quarantaine les messages ou les fichiers (automatiquement ou en tant qu’action configurable), vous pouvez affecter une stratégie de mise en quarantaine aux actions de mise en quarantaine disponibles.</span><span class="sxs-lookup"><span data-stu-id="00b91-263">In _supported_ protection features that quarantine messages or files (automatically or as a configurable action), you can assign a quarantine policy to the available quarantine actions.</span></span> <span data-ttu-id="00b91-264">Les fonctionnalités de mise en quarantaine des messages et la disponibilité des stratégies de mise en quarantaine sont décrites dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="00b91-264">Features that quarantine messages and the availability of quarantine policies are described in the following table:</span></span>

<br>

****

|<span data-ttu-id="00b91-265">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="00b91-265">Feature</span></span>|<span data-ttu-id="00b91-266">Stratégies de mise en quarantaine pris en charge ?</span><span class="sxs-lookup"><span data-stu-id="00b91-266">Quarantine policies supported?</span></span>|<span data-ttu-id="00b91-267">Stratégies de mise en quarantaine par défaut utilisées</span><span class="sxs-lookup"><span data-stu-id="00b91-267">Default quarantine policies used</span></span>|
|---|:---:|---|
|<span data-ttu-id="00b91-268">[Stratégies anti-courrier indésirable](configure-your-spam-filter-policies.md):</span><span class="sxs-lookup"><span data-stu-id="00b91-268">[Anti-spam policies](configure-your-spam-filter-policies.md):</span></span> <ul><li><span data-ttu-id="00b91-269">**Courrier** indésirable (_SpamAction_)</span><span class="sxs-lookup"><span data-stu-id="00b91-269">**Spam** (_SpamAction_)</span></span></li><li><span data-ttu-id="00b91-270">**Courrier indésirable à niveau** de confiance élevé (_HighConfidenceSpamAction_)</span><span class="sxs-lookup"><span data-stu-id="00b91-270">**High confidence spam** (_HighConfidenceSpamAction_)</span></span></li><li><span data-ttu-id="00b91-271">**Hameçonnage** (_PhishSpamAction_)</span><span class="sxs-lookup"><span data-stu-id="00b91-271">**Phishing** (_PhishSpamAction_)</span></span></li><li><span data-ttu-id="00b91-272">**Hameçonnage à haut niveau de** confiance (_HighConfidencePhishAction_)</span><span class="sxs-lookup"><span data-stu-id="00b91-272">**High confidence phishing** (_HighConfidencePhishAction_)</span></span></li><li><span data-ttu-id="00b91-273">**Bulk** (_BulkSpamAction_)</span><span class="sxs-lookup"><span data-stu-id="00b91-273">**Bulk** (_BulkSpamAction_)</span></span></li></ul>|<span data-ttu-id="00b91-274">Oui</span><span class="sxs-lookup"><span data-stu-id="00b91-274">Yes</span></span>|<ul><li><span data-ttu-id="00b91-275">DefaultSpamTag (accès complet)</span><span class="sxs-lookup"><span data-stu-id="00b91-275">DefaultSpamTag (Full access)</span></span></li><li><span data-ttu-id="00b91-276">DefaultHighConfSpamTag (accès complet)</span><span class="sxs-lookup"><span data-stu-id="00b91-276">DefaultHighConfSpamTag (Full access)</span></span></li><li><span data-ttu-id="00b91-277">DefaultPhishTag (accès complet)</span><span class="sxs-lookup"><span data-stu-id="00b91-277">DefaultPhishTag (Full access)</span></span></li><li><span data-ttu-id="00b91-278">DefaultHighConfPhishTag (aucun accès)</span><span class="sxs-lookup"><span data-stu-id="00b91-278">DefaultHighConfPhishTag (No access)</span></span></li><li><span data-ttu-id="00b91-279">DefaultBulkTag (accès complet)</span><span class="sxs-lookup"><span data-stu-id="00b91-279">DefaultBulkTag (Full access)</span></span></li></ul>
|<span data-ttu-id="00b91-280">Stratégies anti-hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="00b91-280">Anti-phishing policies:</span></span> <ul><li><span data-ttu-id="00b91-281">[Protection contre l’usurpation d’identité](set-up-anti-phishing-policies.md#spoof-settings) (_AuthenticationFailAction_)</span><span class="sxs-lookup"><span data-stu-id="00b91-281">[Spoof intelligence protection](set-up-anti-phishing-policies.md#spoof-settings) (_AuthenticationFailAction_)</span></span></li><li><span data-ttu-id="00b91-282">[Protection contre l’emprunt d’identité](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365):<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="00b91-282">[Impersonation protection](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365):<sup>\*</sup></span></span> <ul><li><span data-ttu-id="00b91-283">**Si le message est détecté comme un utilisateur dont** l’identité est usurpée (_TargetedUserProtectionAction_)</span><span class="sxs-lookup"><span data-stu-id="00b91-283">**If message is detected as an impersonated user** (_TargetedUserProtectionAction_)</span></span></li><li><span data-ttu-id="00b91-284">**Si le message est détecté comme un** domaine dont l’identité est usurpée (_TargetedDomainProtectionAction_)</span><span class="sxs-lookup"><span data-stu-id="00b91-284">**If message is detected as an impersonated domain** (_TargetedDomainProtectionAction_)</span></span></li><li><span data-ttu-id="00b91-285">**Si l’intelligence de boîte aux lettres détecte et usurpe l’identité** de l’utilisateur (_MailboxIntelligenceProtectionAction_)</span><span class="sxs-lookup"><span data-stu-id="00b91-285">**If mailbox intelligence detects and impersonated user** (_MailboxIntelligenceProtectionAction_)</span></span></li></ul></li></ul></ul>|<span data-ttu-id="00b91-286">Non</span><span class="sxs-lookup"><span data-stu-id="00b91-286">No</span></span>|<span data-ttu-id="00b91-287">s/o</span><span class="sxs-lookup"><span data-stu-id="00b91-287">n/a</span></span>|
|<span data-ttu-id="00b91-288">[Stratégies anti-programme](configure-anti-malware-policies.md)malveillant : tous les messages détectés sont toujours mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="00b91-288">[Anti-malware policies](configure-anti-malware-policies.md): All detected messages are always quarantined.</span></span>|<span data-ttu-id="00b91-289">Non</span><span class="sxs-lookup"><span data-stu-id="00b91-289">No</span></span>|<span data-ttu-id="00b91-290">s/o</span><span class="sxs-lookup"><span data-stu-id="00b91-290">n/a</span></span>|
|[<span data-ttu-id="00b91-291">Pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="00b91-291">Safe Attachments for SharePoint, OneDrive, and Microsoft Teams</span></span>](mdo-for-spo-odb-and-teams.md)|<span data-ttu-id="00b91-292">Non</span><span class="sxs-lookup"><span data-stu-id="00b91-292">No</span></span>|<span data-ttu-id="00b91-293">s/o</span><span class="sxs-lookup"><span data-stu-id="00b91-293">n/a</span></span>|
|<span data-ttu-id="00b91-294">[Règles de flux de messagerie](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (également appelées règles de transport) avec l’action : Remettre le **message** en quarantaine hébergé (mise en _quarantaine)._</span><span class="sxs-lookup"><span data-stu-id="00b91-294">[Mail flow rules](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (also known as transport rules) with the action: **Deliver the message to the hosted quarantine** (_Quarantine_).</span></span>|<span data-ttu-id="00b91-295">Non</span><span class="sxs-lookup"><span data-stu-id="00b91-295">No</span></span>|<span data-ttu-id="00b91-296">s/o</span><span class="sxs-lookup"><span data-stu-id="00b91-296">n/a</span></span>|
|

<span data-ttu-id="00b91-297"><sup>\*</sup>Les paramètres de protection contre l’emprunt d’identité sont disponibles uniquement dans les stratégies anti-hameçonnage de Microsoft Defender Office 365.</span><span class="sxs-lookup"><span data-stu-id="00b91-297"><sup>\*</sup> Impersonation protection settings are available only in anti-phishing policies in Microsoft Defender for Office 365.</span></span>

<span data-ttu-id="00b91-298">Si vous êtes satisfait des autorisations de l’utilisateur final fournies par les stratégies de mise en quarantaine par défaut, vous n’avez rien à faire.</span><span class="sxs-lookup"><span data-stu-id="00b91-298">If you're happy with the end-user permissions that are provided by the default quarantine policies, you don't need to do anything.</span></span> <span data-ttu-id="00b91-299">Si vous souhaitez personnaliser les fonctionnalités de l’utilisateur final (boutons disponibles) dans les notifications de courrier indésirable de l’utilisateur final ou dans les détails des messages mis en quarantaine, vous pouvez affecter une stratégie de mise en quarantaine personnalisée.</span><span class="sxs-lookup"><span data-stu-id="00b91-299">If you want to customize the end-user capabilities (available buttons) in end-user spam notifications or in quarantined message details, you can assign a custom quarantine policy.</span></span>

### <a name="assign-quarantine-policies-in-anti-spam-policies-in-the-microsoft-365-defender-portal"></a><span data-ttu-id="00b91-300">Affecter des stratégies de mise en quarantaine dans les stratégies anti-courrier indésirable dans le portail Microsoft 365 Defender de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="00b91-300">Assign quarantine policies in anti-spam policies in the Microsoft 365 Defender portal</span></span>

<span data-ttu-id="00b91-301">Des instructions complètes pour la création et la modification des stratégies anti-courrier indésirable sont décrites dans Configurer des stratégies [anti-courrier indésirable dans EOP.](configure-your-spam-filter-policies.md)</span><span class="sxs-lookup"><span data-stu-id="00b91-301">Full instructions for creating and modifying anti-spam policies are described in [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

1. <span data-ttu-id="00b91-302">Dans le portail Microsoft 365 Defender, go to **Email & collaboration** Policies & \> **rules** \> **Policies** section \> **Anti-spam**.</span><span class="sxs-lookup"><span data-stu-id="00b91-302">In the Microsoft 365 Defender portal, go to **Email & collaboration** \> **Policies & rules** \> **Policies** section \> **Anti-spam**.</span></span> <span data-ttu-id="00b91-303">Ou, ouvrez <https://security.microsoft.com/antispam> .</span><span class="sxs-lookup"><span data-stu-id="00b91-303">Or, open <https://security.microsoft.com/antispam>.</span></span>

2. <span data-ttu-id="00b91-304">Dans la page **Stratégies anti-courrier** indésirable, faites l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="00b91-304">On the **Anti-spam policies** page, do one of the following steps:</span></span>
   - <span data-ttu-id="00b91-305">Recherchez et sélectionnez **une** stratégie de courrier indésirable entrant existante.</span><span class="sxs-lookup"><span data-stu-id="00b91-305">Find and select an existing **inbound** anti-spam policy.</span></span>
   - <span data-ttu-id="00b91-306">Créez une stratégie **de** courrier indésirable entrant.</span><span class="sxs-lookup"><span data-stu-id="00b91-306">Create a new **inbound** anti-spam policy.</span></span>

3. <span data-ttu-id="00b91-307">Effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="00b91-307">Do one of the following steps:</span></span>
   - <span data-ttu-id="00b91-308">**Modifier la stratégie anti-courrier** indésirable existante : dans le volet détails de la stratégie, allez dans la section **Actions,** puis cliquez sur **Modifier les actions.**</span><span class="sxs-lookup"><span data-stu-id="00b91-308">**Edit existing anti-spam policy**: In the policy details flyout, go to the **Actions** section and then click **Edit actions**.</span></span>
   - <span data-ttu-id="00b91-309">**Créer une stratégie anti-courrier indésirable**: dans l’Assistant Nouvelle stratégie, allez sur la page **Actions.**</span><span class="sxs-lookup"><span data-stu-id="00b91-309">**Create new anti-spam policy**: In the new policy wizard, go to the **Actions** page.</span></span>

4. <span data-ttu-id="00b91-310">Dans la page **Actions.**</span><span class="sxs-lookup"><span data-stu-id="00b91-310">On the **Actions** page.</span></span> <span data-ttu-id="00b91-311">Chaque verdict qui a l’action  de **message** de mise en quarantaine aura également la zone Sélectionner la stratégie de mise en quarantaine pour vous aider à sélectionner une stratégie de mise en quarantaine correspondante.</span><span class="sxs-lookup"><span data-stu-id="00b91-311">every verdict that has the **Quarantine message** action will also have the **Select quarantine policy** box for you to select a corresponding quarantine policy.</span></span>

   <span data-ttu-id="00b91-312">**Remarque**: lorsque vous créez  une stratégie, une valeur de stratégie de mise en quarantaine Select vide indique que la stratégie de mise en quarantaine par défaut pour ce verdict est utilisée.</span><span class="sxs-lookup"><span data-stu-id="00b91-312">**Note**: When you create a new policy, a blank **Select quarantine policy** value indicates the default quarantine policy for that verdict is used.</span></span> <span data-ttu-id="00b91-313">Lorsque vous modifiez ultérieurement la stratégie, les valeurs vides sont remplacées par les noms de stratégie de mise en quarantaine par défaut réels, comme décrit dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="00b91-313">When you later edit the policy, the blank values are replaced by the actual default quarantine policy names as described in the previous table.</span></span>

   ![Sélections de stratégie de mise en quarantaine dans une stratégie anti-courrier indésirable](../../media/quarantine-tags-in-anti-spam-policies.png)

5. <span data-ttu-id="00b91-315">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="00b91-315">When you're finished, click **Save**.</span></span>

#### <a name="assign-quarantine-policies-in-anti-spam-policies-in-powershell"></a><span data-ttu-id="00b91-316">Attribuer des stratégies de mise en quarantaine dans les stratégies anti-courrier indésirable dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="00b91-316">Assign quarantine policies in anti-spam policies in PowerShell</span></span>

<span data-ttu-id="00b91-317">Si vous préférez utiliser PowerShell pour affecter des stratégies de mise en quarantaine dans les stratégies anti-courrier indésirable, connectez-vous à Exchange Online PowerShell ou Exchange Online Protection PowerShell et utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="00b91-317">If you'd rather use PowerShell to assign quarantine policies in anti-spam policies, connect to Exchange Online PowerShell or Exchange Online Protection PowerShell and use the following syntax:</span></span>

```powershell
<New-HostedContentFilterPolicy -Name "<Unique name>" | Set-HostedContentFilterPolicy -Identity "<Policy name>">  [-SpamAction Quarantine] [-SpamQuarantineTag <QuarantineTagName>] [-HighConfidenceSpamAction Quarantine] [-HighConfidenceSpamQuarantineTag <QuarantineTagName>] [-PhishSpamAction Quarantine] [-PhishQuarantineTag <QuarantineTagName>] [-HighConfidencePhishQuarantineTag <QuarantineTagName>] [-BulkSpamAction Quarantine] [-BulkQuarantineTag <QuarantineTagName>] ...
```

<span data-ttu-id="00b91-318">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="00b91-318">**Notes**:</span></span>

- <span data-ttu-id="00b91-319">La valeur par défaut du paramètre _HighConfidencePhishAction_ est Mise en quarantaine. Vous n’avez donc pas besoin de définir l’action de mise en quarantaine pour les détections de hameçonnage à haut niveau de confiance dans les nouvelles stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="00b91-319">The default value for the _HighConfidencePhishAction_ parameter is Quarantine, so you don't need to set the Quarantine action for high confidence phishing detections in new anti-spam policies.</span></span> <span data-ttu-id="00b91-320">Pour tous les autres verdicts de filtrage du courrier indésirable dans les stratégies anti-courrier indésirable nouvelles ou existantes, la stratégie de mise en quarantaine n’est effective que si la valeur de l’action est Mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="00b91-320">For all other spam filtering verdicts in new or existing anti-spam policies, the quarantine policy is only effective if the action value is Quarantine.</span></span> <span data-ttu-id="00b91-321">Pour voir les valeurs d’action dans les stratégies anti-courrier indésirable existantes, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="00b91-321">To see the action values in existing anti-spam policies, run the following command:</span></span>

  ```powershell
  Get-HostedContentFilterPolicy | Format-Table Name,*SpamAction,HighConfidencePhishAction
  ```

  <span data-ttu-id="00b91-322">Pour plus d’informations sur les valeurs d’action par défaut et les valeurs d’action recommandées pour Standard et Strict, voir paramètres de stratégie [anti-courrier indésirable EOP.](recommended-settings-for-eop-and-office365.md#eop-anti-spam-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="00b91-322">For information about the default action values and the recommended action values for Standard and Strict, see [EOP anti-spam policy settings](recommended-settings-for-eop-and-office365.md#eop-anti-spam-policy-settings).</span></span>

- <span data-ttu-id="00b91-323">Un verdict de filtrage du courrier indésirable sans paramètre de stratégie de mise en quarantaine correspondant signifie que la stratégie de mise en quarantaine [par](#step-2-assign-a-quarantine-policy-to-supported-features) défaut pour ce verdict est utilisée.</span><span class="sxs-lookup"><span data-stu-id="00b91-323">A spam filtering verdict without a corresponding quarantine policy parameter means the [default quarantine policy](#step-2-assign-a-quarantine-policy-to-supported-features) for that verdict is used.</span></span>

  <span data-ttu-id="00b91-324">Vous devez uniquement remplacer une stratégie de mise en quarantaine par défaut par une stratégie de mise en quarantaine personnalisée si vous souhaitez modifier les fonctionnalités par défaut de l’utilisateur final sur les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="00b91-324">You only need to replace a default quarantine policy with a custom quarantine policy if you want to change the default end-user capabilities on quarantined messages.</span></span>

- <span data-ttu-id="00b91-325">Une nouvelle stratégie anti-courrier indésirable dans PowerShell nécessite une stratégie de filtrage du courrier indésirable (paramètres) à l’aide de la cmdlet **New-HostedContentFilterPolicy** et une nouvelle règle de filtrage du courrier indésirable (filtres de destinataires) à l’aide de la cmdlet **New-HostedContentFilterRule.**</span><span class="sxs-lookup"><span data-stu-id="00b91-325">A new anti-spam policy in PowerShell requires a spam filter policy (settings) using the **New-HostedContentFilterPolicy** cmdlet and a new spam filter rule (recipient filters) using the **New-HostedContentFilterRule** cmdlet.</span></span> <span data-ttu-id="00b91-326">Pour obtenir des instructions, [voir Utiliser PowerShell pour créer des stratégies anti-courrier indésirable.](configure-your-spam-filter-policies.md#use-powershell-to-create-anti-spam-policies)</span><span class="sxs-lookup"><span data-stu-id="00b91-326">For instructions, see [Use PowerShell to create anti-spam policies](configure-your-spam-filter-policies.md#use-powershell-to-create-anti-spam-policies).</span></span>

<span data-ttu-id="00b91-327">Cet exemple crée une stratégie de filtrage du courrier indésirable nommée Research Department avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="00b91-327">This example creates a new spam filter policy named Research Department with the following settings:</span></span>

- <span data-ttu-id="00b91-328">L’action de tous les verdicts de filtrage du courrier indésirable est définie sur Quarantaine.</span><span class="sxs-lookup"><span data-stu-id="00b91-328">The action for all spam filtering verdicts is set to Quarantine.</span></span>
- <span data-ttu-id="00b91-329">La stratégie de mise en quarantaine  personnalisée nommée NoAccess qui attribue aucune autorisation  d’accès remplace toutes les stratégies de mise en quarantaine par défaut qui n’attribuent pas déjà aucune autorisation d’accès par défaut.</span><span class="sxs-lookup"><span data-stu-id="00b91-329">The custom quarantine policy named NoAccess that assigns **No access** permissions replaces any default quarantine policies that don't already assign **No access** permissions by default.</span></span>

```powershell
New-HostedContentFilterPolicy -Name Research Department -SpamAction Quarantine -SpamQuarantineTag NoAccess -HighConfidenceSpamAction Quarantine -HighConfidenceSpamQuarantineTag NoAction -PhishSpamAction Quarantine -PhishQuarantineTag NoAction -BulkSpamAction Quarantine -BulkQuarantineTag NoAccess
```

<span data-ttu-id="00b91-330">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-HostedContentFilterPolicy](/powershell/module/exchange/new-hostedcontentfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="00b91-330">For detailed syntax and parameter information, see [New-HostedContentFilterPolicy](/powershell/module/exchange/new-hostedcontentfilterpolicy).</span></span>

<span data-ttu-id="00b91-331">Cet exemple modifie la stratégie de filtrage du courrier indésirable existante nommée Human Resources.</span><span class="sxs-lookup"><span data-stu-id="00b91-331">This example modifies the existing spam filter policy named Human Resources.</span></span> <span data-ttu-id="00b91-332">L’action pour le verdict de mise en quarantaine du courrier indésirable est définie sur Quarantaine et la stratégie de mise en quarantaine personnalisée nommée NoAccess est affectée.</span><span class="sxs-lookup"><span data-stu-id="00b91-332">The action for the spam quarantine verdict is set to Quarantine, and the custom quarantine policy named NoAccess is assigned.</span></span>

```powershell
Set-HostedContentFilterPolicy -Identity "Human Resources" -SpamAction Quarantine -SpamQuarantineTag NoAccess
```

<span data-ttu-id="00b91-333">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-HostedContentFilterPolicy](/powershell/module/exchange/set-hostedcontentfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="00b91-333">For detailed syntax and parameter information, see [Set-HostedContentFilterPolicy](/powershell/module/exchange/set-hostedcontentfilterpolicy).</span></span>

## <a name="configure-global-quarantine-notification-settings-in-the-microsoft-365-defender-portal"></a><span data-ttu-id="00b91-334">Configurer les paramètres globaux de notification de mise en quarantaine dans le portail Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="00b91-334">Configure global quarantine notification settings in the Microsoft 365 Defender portal</span></span>

<span data-ttu-id="00b91-335">Les paramètres globaux des stratégies de mise en quarantaine vous permettent de personnaliser les notifications de courrier indésirable à l’utilisateur final qui sont envoyées aux destinataires des messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="00b91-335">The global settings for quarantine policies allow you to customize the end-user spam notifications that are sent to recipients of messages that were quarantined.</span></span> <span data-ttu-id="00b91-336">Pour plus d’informations sur ces notifications, voir notifications de courrier indésirable pour [l’utilisateur final.](use-spam-notifications-to-release-and-report-quarantined-messages.md)</span><span class="sxs-lookup"><span data-stu-id="00b91-336">For more information about these notifications, see [End-user spam notifications](use-spam-notifications-to-release-and-report-quarantined-messages.md).</span></span>

1. <span data-ttu-id="00b91-337">Dans le portail Microsoft 365 Defender, sélectionnez Stratégies de mise en quarantaine & stratégies de **collaboration** sur les menaces, puis \>  \>  \>  sélectionnez **Stratégies de mise en quarantaine.**</span><span class="sxs-lookup"><span data-stu-id="00b91-337">In the Microsoft 365 Defender portal, go to **Email & collaboration** \>**Threat policies** \> **Rules** section \> **Quarantine policies** and then select **Quarantine policies**.</span></span>

2. <span data-ttu-id="00b91-338">Dans la page **Stratégie de** mise en quarantaine, sélectionnez **Paramètres globaux.**</span><span class="sxs-lookup"><span data-stu-id="00b91-338">On the **Quarantine policy** page, select **Global settings**.</span></span>

3. <span data-ttu-id="00b91-339">Dans le volant **des paramètres de notification de** mise en quarantaine qui s’ouvre, configurez tout ou partie des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="00b91-339">In the **Quarantine notification settings** flyout that opens, configure some or all of the following settings:</span></span>

   - <span data-ttu-id="00b91-340">**Nom complet**: personnalisez le nom complet de l’expéditeur utilisé dans les notifications de courrier indésirable à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="00b91-340">**Display name**: Customize the sender's display name that's used in end-user spam notifications.</span></span>

     <span data-ttu-id="00b91-341">Pour chaque langue que vous avez ajoutée, sélectionnez la langue dans la deuxième langue (ne cliquez pas  sur le X) et entrez la valeur de texte de votre choix dans la zone Nom complet.</span><span class="sxs-lookup"><span data-stu-id="00b91-341">For each language that you've added, select the language in the second language box (don't click on the X) and enter the text value you want in the **Display name** box.</span></span>

     <span data-ttu-id="00b91-342">La capture d’écran suivante montre le nom complet personnalisé dans une notification de courrier indésirable à l’utilisateur final :</span><span class="sxs-lookup"><span data-stu-id="00b91-342">The following screenshot shows the customized display name in an end-user spam notification:</span></span>

     ![Nom d’affichage de l’expéditeur personnalisé dans une notification de courrier indésirable à l’utilisateur final](../../media/quarantine-tags-esn-customization-display-name.png)

   - <span data-ttu-id="00b91-344">**Clause d’exclusion de** responsabilité : ajoutez une clause d’exclusion de responsabilité personnalisée au bas des notifications de courrier indésirable à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="00b91-344">**Disclaimer**: Add a custom disclaimer to the bottom of end-user spam notifications.</span></span> <span data-ttu-id="00b91-345">Le texte localisé, **une clause d’exclusion** de responsabilité de votre organisation, est toujours inclus en premier, suivi du texte que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="00b91-345">The localized text, **A disclaimer from your organization:** is always included first, followed by the text you specify.</span></span>

     <span data-ttu-id="00b91-346">Pour chaque langue que vous avez ajoutée, sélectionnez la langue dans la deuxième langue (ne cliquez pas sur le X) et entrez la valeur de texte de votre choix dans la zone Exclusion de **responsabilité.**</span><span class="sxs-lookup"><span data-stu-id="00b91-346">For each language that you've added, select the language in the second language box  (don't click the X) and enter the text value you want in the **Disclaimer** box.</span></span>

     <span data-ttu-id="00b91-347">La capture d’écran suivante montre la clause d’exclusion de responsabilité personnalisée dans une notification de courrier indésirable à l’utilisateur final :</span><span class="sxs-lookup"><span data-stu-id="00b91-347">The following screenshot shows the customized disclaimer in an end-user spam notification:</span></span>

     ![Une clause d’exclusion de responsabilité personnalisée au bas d’une notification de courrier indésirable à l’utilisateur final](../../media/quarantine-tags-esn-customization-disclaimer.png)

   - <span data-ttu-id="00b91-349">**Choisir la langue**: les notifications de courrier indésirable de l’utilisateur final sont déjà localisées en fonction des paramètres de langue du destinataire.</span><span class="sxs-lookup"><span data-stu-id="00b91-349">**Choose language**: End-user spam notifications are already localized based on the recipient's language settings.</span></span> <span data-ttu-id="00b91-350">Vous pouvez spécifier du texte personnalisé dans différentes langues pour les valeurs **Nom d’affichage** et Exclusion **de** responsabilité.</span><span class="sxs-lookup"><span data-stu-id="00b91-350">You can specify customized text in different languages for the **Display name** and **Disclaimer** values.</span></span>

     <span data-ttu-id="00b91-351">Sélectionnez au moins une langue dans la première langue, puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="00b91-351">Select at least one language from the first language box and then click **Add**.</span></span> <span data-ttu-id="00b91-352">Vous pouvez sélectionner plusieurs langues en cliquant sur **Ajouter** après chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="00b91-352">You can select multiple languages by clicking **Add** after each one.</span></span> <span data-ttu-id="00b91-353">Une zone de langue de section affiche toutes les langues que vous avez sélectionnées :</span><span class="sxs-lookup"><span data-stu-id="00b91-353">A section language box shows all of the languages that you've selected:</span></span>

     ![Langues sélectionnées dans la deuxième langue dans les paramètres globaux de notification de mise en quarantaine des stratégies de mise en quarantaine](../../media/quarantine-tags-esn-customization-selected-languages.png)

   - <span data-ttu-id="00b91-355">**Utilisez le logo de mon** entreprise : sélectionnez cette option pour remplacer le logo Microsoft par défaut qui est utilisé en haut des notifications de courrier indésirable à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="00b91-355">**Use my company logo**: Select this option to replace the default Microsoft logo that's use at the top of end-user spam notifications.</span></span> <span data-ttu-id="00b91-356">Avant de faire cela, vous devez suivre les instructions dans Personnaliser le thème [Microsoft 365](../../admin/setup/customize-your-organization-theme.md) pour que votre organisation télécharge votre logo personnalisé.</span><span class="sxs-lookup"><span data-stu-id="00b91-356">Before you do this, you need to follow the instructions in [Customize the Microsoft 365 theme for your organization](../../admin/setup/customize-your-organization-theme.md) to upload your custom logo.</span></span>

     <span data-ttu-id="00b91-357">La capture d’écran suivante montre un logo personnalisé dans une notification de courrier indésirable à l’utilisateur final :</span><span class="sxs-lookup"><span data-stu-id="00b91-357">The following screenshot shows a custom logo in an end-user spam notification:</span></span>

     ![Logo personnalisé dans une notification de courrier indésirable à l’utilisateur final](../../media/quarantine-tags-esn-customization-logo.png)

## <a name="view-quarantine-policies-in-the-microsoft-365-defender-portal"></a><span data-ttu-id="00b91-359">Afficher les stratégies de mise en quarantaine dans le portail Microsoft 365 Defender de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="00b91-359">View quarantine policies in the Microsoft 365 Defender portal</span></span>

1. <span data-ttu-id="00b91-360">Dans le portail Microsoft 365 Defender, sélectionnez Stratégies de mise en quarantaine & stratégies de **collaboration** sur les menaces, puis \>  \>  \>  sélectionnez **Stratégies de mise en quarantaine.**</span><span class="sxs-lookup"><span data-stu-id="00b91-360">In the Microsoft 365 Defender portal, go to **Email & collaboration** \>**Threat policies** \> **Rules** section \> **Quarantine policies** and then select **Quarantine policies**.</span></span>

2. <span data-ttu-id="00b91-361">La **page Stratégie de** mise en quarantaine affiche la liste des stratégies par **nom** et date de dernière mise **à** jour.</span><span class="sxs-lookup"><span data-stu-id="00b91-361">The **Quarantine policy** page shows the list of policies by **Name** and **Last updated** date.</span></span>

3. <span data-ttu-id="00b91-362">Pour afficher les paramètres des stratégies de mise en quarantaine intégrées ou personnalisées, sélectionnez la stratégie de mise en quarantaine dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="00b91-362">To view the settings of built-in or custom quarantine policies, select the quarantine policy from the list by clicking on the name.</span></span>

4. <span data-ttu-id="00b91-363">Pour afficher les paramètres globaux, cliquez **sur Paramètres globaux**</span><span class="sxs-lookup"><span data-stu-id="00b91-363">To view the global settings, click **Global settings**</span></span>

### <a name="view-quarantine-policies-in-powershell"></a><span data-ttu-id="00b91-364">Afficher les stratégies de mise en quarantaine dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="00b91-364">View quarantine policies in PowerShell</span></span>

<span data-ttu-id="00b91-365">Si vous préférez utiliser PowerShell pour afficher les stratégies de mise en quarantaine, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="00b91-365">If you'd rather use PowerShell to view quarantine policies, do any of the following steps:</span></span>

- <span data-ttu-id="00b91-366">Pour afficher une liste récapitulatif de toutes les stratégies intégrées ou personnalisées, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="00b91-366">To view a summary list of all built-in or custom policies, run the following command:</span></span>

  ```powershell
  Get-QuarantineTag | Format-Table Name
  ```

- <span data-ttu-id="00b91-367">Pour afficher les paramètres des stratégies de mise en quarantaine intégrées ou personnalisées, remplacez-les par le nom de la stratégie de mise en quarantaine et exécutez \<QuarantinePolicyName\> la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="00b91-367">To view the settings of built-in or custom quarantine policies, replace \<QuarantinePolicyName\> with the name of the quarantine policy, and run the following command:</span></span>

  ```powershell
  Get-QuarantineTag -Identity "<QuarantinePolicyName>"
  ```

- <span data-ttu-id="00b91-368">Pour afficher les paramètres globaux, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="00b91-368">To view the global settings, run the following command:</span></span>

  ```powershell
  Get-QuarantineTag -QuarantineTagType GlobalQuarantineTag
  ```

<span data-ttu-id="00b91-369">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-HostedContentFilterPolicy](/powershell/module/exchange/get-hostedcontentfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="00b91-369">For detailed syntax and parameter information, see [Get-HostedContentFilterPolicy](/powershell/module/exchange/get-hostedcontentfilterpolicy).</span></span>

## <a name="modify-quarantine-policies-in-the-microsoft-365-defender-portal"></a><span data-ttu-id="00b91-370">Modifier les stratégies de mise en quarantaine dans le portail Microsoft 365 Defender de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="00b91-370">Modify quarantine policies in the Microsoft 365 Defender portal</span></span>

1. <span data-ttu-id="00b91-371">Dans le portail Microsoft 365 Defender, sélectionnez Stratégies de mise en quarantaine & stratégies de **collaboration** sur les menaces, puis \>  \>  \>  sélectionnez **Stratégies de mise en quarantaine.**</span><span class="sxs-lookup"><span data-stu-id="00b91-371">In the Microsoft 365 Defender portal, go to **Email & collaboration** \>**Threat policies** \> **Rules** section \> **Quarantine policies** and then select **Quarantine policies**.</span></span>

2. <span data-ttu-id="00b91-372">Dans la page **Stratégies de** mise en quarantaine, sélectionnez la stratégie en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="00b91-372">On the **Quarantine policies** page, select the policy by clicking on the name.</span></span>

3. <span data-ttu-id="00b91-373">Après avoir sélectionné la stratégie, cliquez sur l’icône Modifier la stratégie ![ ](../../media/m365-cc-sc-edit-icon.png) **icône Modifier** la stratégie qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="00b91-373">After you select the policy, click the ![Edit policy icon](../../media/m365-cc-sc-edit-icon.png) **Edit policy** icon that appears.</span></span>

4. <span data-ttu-id="00b91-374">**L’Assistant** Modifier la stratégie qui s’ouvre est pratiquement identique à l’Assistant Nouvelle stratégie, comme décrit dans la section Créer des stratégies de mise en quarantaine dans la section du portail [Microsoft 365 Defender](#step-1-create-quarantine-policies-in-the-microsoft-365-defender-portal) plus tôt dans cet article. </span><span class="sxs-lookup"><span data-stu-id="00b91-374">The **Edit policy** wizard that opens is virtually identical to the **New policy** wizard as described in the [Create quarantine policies in the Microsoft 365 Defender portal](#step-1-create-quarantine-policies-in-the-microsoft-365-defender-portal) section earlier in this article.</span></span>

   <span data-ttu-id="00b91-375">La principale différence est que vous ne pouvez pas renommer une stratégie existante.</span><span class="sxs-lookup"><span data-stu-id="00b91-375">The main difference is: you can't rename an existing policy.</span></span>

5. <span data-ttu-id="00b91-376">Lorsque vous avez terminé de modifier la stratégie, allez sur la **page** Résumé et cliquez sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="00b91-376">When you're finished modifying the policy, go to the **Summary** page and click **Submit**.</span></span>

### <a name="modify-quarantine-policies-in-powershell"></a><span data-ttu-id="00b91-377">Modifier les stratégies de mise en quarantaine dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="00b91-377">Modify quarantine policies in PowerShell</span></span>

<span data-ttu-id="00b91-378">Si vous préférez utiliser PowerShell pour modifier une stratégie de mise en quarantaine personnalisée, remplacez-la par le nom de la stratégie de mise en quarantaine et utilisez \<QuarantinePolicyName\> la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="00b91-378">If you'd rather use PowerShell to modify a custom quarantine policy, replace \<QuarantinePolicyName\> with the name of the quarantine policy, and use the following syntax:</span></span>

```powershell
Set-QuarantineTag -Identity "<QuarantinePolicyName>" [Settings]
```

<span data-ttu-id="00b91-379">Les paramètres disponibles sont les mêmes que ceux décrits pour la création de stratégies de mise en quarantaine plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="00b91-379">The available settings are the same as described for creating quarantine policies earlier in this article.</span></span>

<span data-ttu-id="00b91-380">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-QuarantineTag](/powershell/module/exchange/set-quarantinetag).</span><span class="sxs-lookup"><span data-stu-id="00b91-380">For detailed syntax and parameter information, see [Set-QuarantineTag](/powershell/module/exchange/set-quarantinetag).</span></span>

## <a name="remove-quarantine-policies-in-the-microsoft-365-defender-portal"></a><span data-ttu-id="00b91-381">Supprimer les stratégies de mise en quarantaine dans le portail Microsoft 365 Defender de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="00b91-381">Remove quarantine policies in the Microsoft 365 Defender portal</span></span>

<span data-ttu-id="00b91-382">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="00b91-382">**Notes**:</span></span>

- <span data-ttu-id="00b91-383">Vous ne pouvez pas supprimer les stratégies de mise en quarantaine intégrées.</span><span class="sxs-lookup"><span data-stu-id="00b91-383">You can't remove built-in quarantine policies.</span></span>
- <span data-ttu-id="00b91-384">Avant de supprimer une stratégie de mise en quarantaine personnalisée, vérifiez qu’elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="00b91-384">Before you remove a custom quarantine policy, verify that it's not being used.</span></span> <span data-ttu-id="00b91-385">Par exemple, exécutez la commande suivante dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="00b91-385">For example, run the following command in PowerShell:</span></span>

  ```powershell
  Get-HostedContentFilterPolicy | Format-List Name,*QuarantineTag
  ```

  <span data-ttu-id="00b91-386">Si la stratégie de mise en quarantaine est utilisée, [remplacez la stratégie](#step-2-assign-a-quarantine-policy-to-supported-features) de mise en quarantaine attribuée avant de la supprimer.</span><span class="sxs-lookup"><span data-stu-id="00b91-386">If the quarantine policy is being used, [replace the assigned quarantine policy](#step-2-assign-a-quarantine-policy-to-supported-features) before you remove it.</span></span>

1. <span data-ttu-id="00b91-387">Dans le portail Microsoft 365 Defender, sélectionnez Stratégies de mise en quarantaine & stratégies de **collaboration** sur les menaces, puis \>  \>  \>  sélectionnez **Stratégies de mise en quarantaine.**</span><span class="sxs-lookup"><span data-stu-id="00b91-387">In the Microsoft 365 Defender portal, go to **Email & collaboration** \>**Threat policies** \> **Rules** section \> **Quarantine policies** and then select **Quarantine policies**.</span></span>

2. <span data-ttu-id="00b91-388">Dans la page **Stratégie de** mise en quarantaine, sélectionnez la stratégie de mise en quarantaine personnalisée à supprimer en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="00b91-388">On the **Quarantine policy** page, select the custom quarantine policy that you want to remove by clicking on the name.</span></span>

3. <span data-ttu-id="00b91-389">Après avoir sélectionné la stratégie, cliquez sur l’icône Supprimer la stratégie Icône Supprimer la stratégie ![ ](../../media/m365-cc-sc-delete-icon.png)  qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="00b91-389">After you select the policy, click the ![Delete policy icon](../../media/m365-cc-sc-delete-icon.png) **Delete policy** icon that appears.</span></span>

4. <span data-ttu-id="00b91-390">Cliquez **sur Supprimer la stratégie** dans la boîte de dialogue de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="00b91-390">Click **Remove policy** in the confirmation dialog that appears.</span></span>

### <a name="remove-quarantine-policies-in-powershell"></a><span data-ttu-id="00b91-391">Supprimer les stratégies de mise en quarantaine dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="00b91-391">Remove quarantine policies in PowerShell</span></span>

<span data-ttu-id="00b91-392">Si vous préférez utiliser PowerShell pour supprimer une stratégie de mise en quarantaine personnalisée, remplacez-la par le nom de la stratégie de mise en quarantaine \<QuarantinePolicyName\> et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="00b91-392">If you'd rather use PowerShell to remove a custom quarantine policy, replace \<QuarantinePolicyName\> with the name of the quarantine policy, and run the following command:</span></span>

```powershell
Remove-QuarantineTag -Identity "<QuarantinePolicyName>"
```

<span data-ttu-id="00b91-393">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-QuarantineTag](/powershell/module/exchange/remove-quarantinetag).</span><span class="sxs-lookup"><span data-stu-id="00b91-393">For detailed syntax and parameter information, see [Remove-QuarantineTag](/powershell/module/exchange/remove-quarantinetag).</span></span>

## <a name="quarantine-policy-permission-details"></a><span data-ttu-id="00b91-394">Détails des autorisations de stratégie de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="00b91-394">Quarantine policy permission details</span></span>

<span data-ttu-id="00b91-395">Les sections suivantes décrivent les effets des groupes d’autorisations prédéfinés et des autorisations individuelles dans les détails des messages mis en quarantaine et dans les notifications de courrier indésirable à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="00b91-395">The following sections describe the effects of preset permission groups and individual permissions in the details of quarantined messages and in end-user spam notifications.</span></span>

### <a name="preset-permissions-groups"></a><span data-ttu-id="00b91-396">Groupes d’autorisations prédéfins</span><span class="sxs-lookup"><span data-stu-id="00b91-396">Preset permissions groups</span></span>

<span data-ttu-id="00b91-397">Les autorisations individuelles incluses dans les groupes d’autorisations prédéfinés sont répertoriées dans le tableau au début de cet article.</span><span class="sxs-lookup"><span data-stu-id="00b91-397">The individual permissions that are included in preset permission groups are listed in the table at the beginning of this article.</span></span>

#### <a name="no-access"></a><span data-ttu-id="00b91-398">Pas d’accès</span><span class="sxs-lookup"><span data-stu-id="00b91-398">No access</span></span>

<span data-ttu-id="00b91-399">Si la stratégie de  mise en quarantaine attribue les autorisations Aucun accès (aucune autorisation), les utilisateurs obtiennent toujours certaines fonctionnalités de référence :</span><span class="sxs-lookup"><span data-stu-id="00b91-399">If the quarantine policy assigns the **No access** permissions (no permissions), users still get some baseline capabilities:</span></span>

- <span data-ttu-id="00b91-400">**Détails du message mis en quarantaine**: le bouton Afficher **l’en-tête du message** est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-400">**Quarantined message details**: The **View message header** button is always available.</span></span>

  ![Boutons disponibles dans les détails du message mis en quarantaine si la stratégie de mise en quarantaine accorde à l’utilisateur des autorisations d’accès sans accès](../../media/quarantine-tags-quarantined-message-details-no-access.png)

- <span data-ttu-id="00b91-402">**Notifications de courrier** indésirable  à l’utilisateur final : le bouton Révision qui met l’utilisateur en quarantaine est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-402">**End-user spam notifications**: The **Review** button that takes the user to the message in quarantine is always available.</span></span>

  ![Boutons disponibles dans la notification de courrier indésirable de l’utilisateur final si la stratégie de mise en quarantaine accorde à l’utilisateur des autorisations d’accès sans accès](../../media/quarantine-tags-esn-no-access.png)

#### <a name="limited-access"></a><span data-ttu-id="00b91-404">Accès limité</span><span class="sxs-lookup"><span data-stu-id="00b91-404">Limited access</span></span>

<span data-ttu-id="00b91-405">Si la stratégie de mise en quarantaine attribue les **autorisations** d’accès limité, les utilisateurs obtiennent les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="00b91-405">If the quarantine policy assigns the **Limited access** permissions, users get the following capabilities:</span></span>

- <span data-ttu-id="00b91-406">**Détails du message mis en quarantaine**: les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="00b91-406">**Quarantined message details**: The following buttons are available:</span></span>
  - <span data-ttu-id="00b91-407">**Publication de la demande**</span><span class="sxs-lookup"><span data-stu-id="00b91-407">**Request release**</span></span>
  - <span data-ttu-id="00b91-408">**Afficher l’en-tête du message**</span><span class="sxs-lookup"><span data-stu-id="00b91-408">**View message header**</span></span>
  - <span data-ttu-id="00b91-409">**Aperçu du message**</span><span class="sxs-lookup"><span data-stu-id="00b91-409">**Preview message**</span></span>
  - <span data-ttu-id="00b91-410">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="00b91-410">**Block sender**</span></span>
  - <span data-ttu-id="00b91-411">**Supprimer de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="00b91-411">**Remove from quarantine**</span></span>

  ![Boutons disponibles dans les détails du message mis en quarantaine si la stratégie de mise en quarantaine accorde à l’utilisateur des autorisations d’accès limité](../../media/quarantine-tags-quarantined-message-details-limited-access.png)

- <span data-ttu-id="00b91-413">**Notifications de courrier indésirable pour l’utilisateur final**: les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="00b91-413">**End-user spam notifications**: The following buttons are available:</span></span>
  - <span data-ttu-id="00b91-414">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="00b91-414">**Block sender**</span></span>
  - <span data-ttu-id="00b91-415">**Révision**</span><span class="sxs-lookup"><span data-stu-id="00b91-415">**Review**</span></span>

  ![Boutons disponibles dans la notification de courrier indésirable de l’utilisateur final si la stratégie de mise en quarantaine accorde à l’utilisateur des autorisations d’accès limité](../../media/quarantine-tags-esn-limited-access.png)

#### <a name="full-access"></a><span data-ttu-id="00b91-417">Accès total</span><span class="sxs-lookup"><span data-stu-id="00b91-417">Full access</span></span>

<span data-ttu-id="00b91-418">Si la stratégie de mise en quarantaine attribue les **autorisations** d’accès total (toutes les autorisations disponibles), les utilisateurs disposent des fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="00b91-418">If the quarantine policy assigns the **Full access** permissions (all available permissions), users get the following capabilities:</span></span>

- <span data-ttu-id="00b91-419">**Détails du message mis en quarantaine**: les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="00b91-419">**Quarantined message details**: The following buttons are available:</span></span>
  - <span data-ttu-id="00b91-420">**Message de publication**</span><span class="sxs-lookup"><span data-stu-id="00b91-420">**Release message**</span></span>
  - <span data-ttu-id="00b91-421">**Afficher l’en-tête du message**</span><span class="sxs-lookup"><span data-stu-id="00b91-421">**View message header**</span></span>
  - <span data-ttu-id="00b91-422">**Aperçu du message**</span><span class="sxs-lookup"><span data-stu-id="00b91-422">**Preview message**</span></span>
  - <span data-ttu-id="00b91-423">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="00b91-423">**Block sender**</span></span>
  - <span data-ttu-id="00b91-424">**Autoriser l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="00b91-424">**Allow sender**</span></span>
  - <span data-ttu-id="00b91-425">**Supprimer de la quarantaine**</span><span class="sxs-lookup"><span data-stu-id="00b91-425">**Remove from quarantine**</span></span>

  ![Boutons disponibles dans les détails du message mis en quarantaine si la stratégie de mise en quarantaine accorde à l’utilisateur des autorisations d’accès total](../../media/quarantine-tags-quarantined-message-details-full-access.png)

- <span data-ttu-id="00b91-427">**Notifications de courrier indésirable pour l’utilisateur final**: les boutons suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="00b91-427">**End-user spam notifications**: The following buttons are available:</span></span>
  - <span data-ttu-id="00b91-428">**Bloquer l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="00b91-428">**Block sender**</span></span>
  - <span data-ttu-id="00b91-429">**Débloquer**</span><span class="sxs-lookup"><span data-stu-id="00b91-429">**Release**</span></span>
  - <span data-ttu-id="00b91-430">**Révision**</span><span class="sxs-lookup"><span data-stu-id="00b91-430">**Review**</span></span>

  ![Boutons disponibles dans la notification de courrier indésirable de l’utilisateur final si la stratégie de mise en quarantaine accorde à l’utilisateur des autorisations d’accès total](../../media/quarantine-tags-esn-full-access.png)

### <a name="individual-permissions"></a><span data-ttu-id="00b91-432">Autorisations individuelles</span><span class="sxs-lookup"><span data-stu-id="00b91-432">Individual permissions</span></span>

> [!NOTE]
> <span data-ttu-id="00b91-433">N’oubliez pas que les utilisateurs obtiennent toujours les boutons décrits dans la section [Aucun](#no-access) accès.</span><span class="sxs-lookup"><span data-stu-id="00b91-433">Remember, users always get the buttons described in the [No access](#no-access) section.</span></span> <span data-ttu-id="00b91-434">Ces boutons ne sont pas inclus dans les descriptions des autorisations individuelles.</span><span class="sxs-lookup"><span data-stu-id="00b91-434">These buttons are not included in the individual permission descriptions.</span></span>

#### <a name="allow-sender-permission"></a><span data-ttu-id="00b91-435">Autoriser l’autorisation de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="00b91-435">Allow sender permission</span></span>

<span data-ttu-id="00b91-436">L’autorisation Autoriser l’expéditeur (_PermissionToAllowSender_) contrôle l’accès au bouton qui permet aux utilisateurs d’ajouter facilement l’expéditeur du message mis en quarantaine à leur liste Coffre expéditeurs. </span><span class="sxs-lookup"><span data-stu-id="00b91-436">The **Allow sender** permission (_PermissionToAllowSender_) controls access to the button that allows users to conveniently add the quarantined message sender to their Safe Senders list.</span></span>

- <span data-ttu-id="00b91-437">**Détails du message mis en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="00b91-437">**Quarantined message details**:</span></span>
  - <span data-ttu-id="00b91-438">**Autoriser l’autorisation** de l’expéditeur activée : le bouton Autoriser **l’expéditeur** est disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-438">**Allow sender** permission enabled: The **Allow sender** button is available.</span></span>
  - <span data-ttu-id="00b91-439">**Autoriser l’autorisation** de l’expéditeur désactivée : le bouton Autoriser **l’expéditeur** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-439">**Allow sender** permission disabled: The **Allow sender** button is not available.</span></span>

- <span data-ttu-id="00b91-440">**Notifications de courrier indésirable pour l’utilisateur final**: aucun effet.</span><span class="sxs-lookup"><span data-stu-id="00b91-440">**End-user spam notifications**: No effect.</span></span>

<span data-ttu-id="00b91-441">Pour plus d’informations sur la liste [](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379666) des expéditeurs Coffre, voir Empêcher le blocage des expéditeurs de confiance et Utiliser [Exchange Online PowerShell](configure-junk-email-settings-on-exo-mailboxes.md#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox)pour configurer la collection de listes fiables sur une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="00b91-441">For more information about the Safe Senders list, see [Prevent trusted senders from being blocked](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379666) and [Use Exchange Online PowerShell to configure the safelist collection on a mailbox](configure-junk-email-settings-on-exo-mailboxes.md#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox).</span></span>

#### <a name="block-sender-permission"></a><span data-ttu-id="00b91-442">Bloquer l’autorisation de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="00b91-442">Block sender permission</span></span>

<span data-ttu-id="00b91-443">**L’autorisation** Bloquer l’expéditeur (_PermissionToBlockSender_) contrôle l’accès au bouton qui permet aux utilisateurs d’ajouter facilement l’expéditeur du message mis en quarantaine à leur liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="00b91-443">The **Block sender** permission (_PermissionToBlockSender_) controls access to the button that allows users to conveniently add the quarantined message sender to their Blocked Senders list.</span></span>

- <span data-ttu-id="00b91-444">**Détails du message mis en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="00b91-444">**Quarantined message details**:</span></span>
  - <span data-ttu-id="00b91-445">**Autorisation bloquer l’expéditeur** activée : le **bouton Bloquer l’expéditeur** est disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-445">**Block sender** permission enabled: The **Block sender** button is available.</span></span>
  - <span data-ttu-id="00b91-446">**Bloquer l’autorisation** de l’expéditeur désactivée : le bouton **Bloquer l’expéditeur** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-446">**Block sender** permission disabled: The **Block sender** button is not available.</span></span>

- <span data-ttu-id="00b91-447">**Notifications de courrier indésirable pour l’utilisateur final**:</span><span class="sxs-lookup"><span data-stu-id="00b91-447">**End-user spam notifications**:</span></span>
  - <span data-ttu-id="00b91-448">**Bloquer l’autorisation** de l’expéditeur désactivée : le bouton **Bloquer l’expéditeur** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-448">**Block sender** permission disabled: The **Block sender** button is not available.</span></span>
  - <span data-ttu-id="00b91-449">**Autorisation bloquer l’expéditeur** activée : le **bouton Bloquer l’expéditeur** est disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-449">**Block sender** permission enabled: The **Block sender** button is available.</span></span>

<span data-ttu-id="00b91-450">Pour plus d’informations sur la liste des expéditeurs bloqués, voir Bloquer les [messages](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379667) d’une personne et utiliser Exchange Online PowerShell pour configurer la collection de listes sécurisées sur [une boîte aux lettres.](configure-junk-email-settings-on-exo-mailboxes.md#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox)</span><span class="sxs-lookup"><span data-stu-id="00b91-450">For more information about the Blocked Senders list, see [Block messages from someone](https://support.microsoft.com/office/274ae301-5db2-4aad-be21-25413cede077#__toc304379667) and [Use Exchange Online PowerShell to configure the safelist collection on a mailbox](configure-junk-email-settings-on-exo-mailboxes.md#use-exchange-online-powershell-to-configure-the-safelist-collection-on-a-mailbox).</span></span>

#### <a name="delete-permission"></a><span data-ttu-id="00b91-451">Autorisations de suppression</span><span class="sxs-lookup"><span data-stu-id="00b91-451">Delete permission</span></span>

<span data-ttu-id="00b91-452">**L’autorisation** Supprimer (_PermissionToDelete_) contrôle la possibilité pour les utilisateurs de supprimer leurs messages (messages dont l’utilisateur est un destinataire) de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="00b91-452">The **Delete** permission (_PermissionToDelete_) controls the ability to of users to delete their messages (messages where the user is a recipient) from quarantine.</span></span>

- <span data-ttu-id="00b91-453">**Détails du message mis en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="00b91-453">**Quarantined message details**:</span></span>
  - <span data-ttu-id="00b91-454">**Autorisation de** suppression activée : le bouton **Supprimer de** la quarantaine est disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-454">**Delete** permission enabled: The **Remove from quarantine** button is available.</span></span>
  - <span data-ttu-id="00b91-455">**Autorisation de** suppression désactivée : le bouton **Supprimer de la quarantaine** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-455">**Delete** permission disabled: The **Remove from quarantine** button is not available.</span></span>

- <span data-ttu-id="00b91-456">**Notifications de courrier indésirable pour l’utilisateur final**: aucun effet.</span><span class="sxs-lookup"><span data-stu-id="00b91-456">**End-user spam notifications**: No effect.</span></span>

#### <a name="preview-permission"></a><span data-ttu-id="00b91-457">Autorisation d’aperçu</span><span class="sxs-lookup"><span data-stu-id="00b91-457">Preview permission</span></span>

<span data-ttu-id="00b91-458">**L’autorisation** Aperçu (_PermissionToPreview_) contrôle la possibilité pour les utilisateurs d’afficher un aperçu de leurs messages en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="00b91-458">The **Preview** permission (_PermissionToPreview_) controls the ability to of users to preview their messages in quarantine.</span></span>

- <span data-ttu-id="00b91-459">**Détails du message mis en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="00b91-459">**Quarantined message details**:</span></span>
  - <span data-ttu-id="00b91-460">**Autorisation d’aperçu** activée : le bouton **Aperçu du message** est disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-460">**Preview** permission enabled: The **Preview message** button is available.</span></span>
  - <span data-ttu-id="00b91-461">**Autorisation d’aperçu** désactivée : le bouton **Aperçu du message** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-461">**Preview** permission disabled: The **Preview message** button is not available.</span></span>

- <span data-ttu-id="00b91-462">**Notifications de courrier indésirable pour l’utilisateur final**: aucun effet.</span><span class="sxs-lookup"><span data-stu-id="00b91-462">**End-user spam notifications**: No effect.</span></span>

#### <a name="allow-recipients-to-release-a-message-from-quarantine-permission"></a><span data-ttu-id="00b91-463">Autoriser les destinataires à libérer un message de l’autorisation de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="00b91-463">Allow recipients to release a message from quarantine permission</span></span>

<span data-ttu-id="00b91-464">L’autorisation autoriser les destinataires à libérer un message de l’autorisation de mise en quarantaine (_PermissionToRelease_) contrôle la capacité des **utilisateurs** à libérer leurs messages mis en quarantaine directement et sans l’approbation d’un administrateur.</span><span class="sxs-lookup"><span data-stu-id="00b91-464">The **Allow recipients to release a message from quarantine** permission (_PermissionToRelease_) controls the ability of users to release their quarantined messages directly and without the approval of an admin.</span></span>

- <span data-ttu-id="00b91-465">**Détails du message mis en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="00b91-465">**Quarantined message details**:</span></span>
  - <span data-ttu-id="00b91-466">Autorisation activée : le bouton **Libérer le message** est disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-466">Permission enabled: The **Release message** button is available.</span></span>
  - <span data-ttu-id="00b91-467">Autorisation désactivée : le bouton **Libérer le message** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-467">Permission disabled: The **Release message** button is not available.</span></span>

- <span data-ttu-id="00b91-468">**Notifications de courrier indésirable pour l’utilisateur final**:</span><span class="sxs-lookup"><span data-stu-id="00b91-468">**End-user spam notifications**:</span></span>
  - <span data-ttu-id="00b91-469">Autorisation activée : **le** bouton Libérer est disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-469">Permission enabled: The **Release** button is available.</span></span>
  - <span data-ttu-id="00b91-470">Autorisation désactivée : **le** bouton Libérer n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-470">Permission disabled: The **Release** button is not available.</span></span>

#### <a name="allow-recipients-to-request-a-message-to-be-released-from-quarantine-permission"></a><span data-ttu-id="00b91-471">Autoriser les destinataires à demander la libération d’un message de l’autorisation de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="00b91-471">Allow recipients to request a message to be released from quarantine permission</span></span>

<span data-ttu-id="00b91-472">L’autorisation autoriser les destinataires à demander la libération d’un message à partir de  l’autorisation de mise en quarantaine (_PermissionToRequestRelease_) contrôle la capacité des **utilisateurs** à demander la libération de leurs messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="00b91-472">The **Allow recipients to request a message to be released from quarantine** permission (_PermissionToRequestRelease_) controls the ability of users to _request_ the release of their quarantined messages.</span></span> <span data-ttu-id="00b91-473">Le message est publié uniquement après qu’un administrateur a approuvé la demande.</span><span class="sxs-lookup"><span data-stu-id="00b91-473">The message is only released after an admin approves the request.</span></span>

- <span data-ttu-id="00b91-474">**Détails du message mis en quarantaine**:</span><span class="sxs-lookup"><span data-stu-id="00b91-474">**Quarantined message details**:</span></span>
  - <span data-ttu-id="00b91-475">Autorisation activée : le bouton **De publication** de la demande est disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-475">Permission enabled: The **Request release** button is available.</span></span>
  - <span data-ttu-id="00b91-476">Autorisation désactivée : le bouton **De publication** de la demande n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-476">Permission disabled: The **Request release** button is not available.</span></span>

- <span data-ttu-id="00b91-477">**Notifications de courrier indésirable pour l’utilisateur final**: **le** bouton Release n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="00b91-477">**End-user spam notifications**: The **Release** button is not available.</span></span>
