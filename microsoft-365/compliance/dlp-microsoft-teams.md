---
title: Prévention des pertes de données et Microsoft Teams
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
description: Microsoft Teams conversations et canaux prend en charge les stratégies de protection contre la perte de données (DLP).
ms.openlocfilehash: 6467ae7fdfc9c8636bd306efde5cb89c100e5e6c
ms.sourcegitcommit: 3b9fab82d63aea41d5f544938868c5d2cbf52d7a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "52782560"
---
# <a name="data-loss-prevention-and-microsoft-teams"></a><span data-ttu-id="21d52-103">Prévention des pertes de données et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="21d52-103">Data loss prevention and Microsoft Teams</span></span>

<span data-ttu-id="21d52-104">Si votre organisation dispose d’une protection contre la perte de données (DLP), vous pouvez définir des stratégies qui empêchent les utilisateurs de partager des informations sensibles dans un canal Microsoft Teams ou une session de conversation.</span><span class="sxs-lookup"><span data-stu-id="21d52-104">If your organization has data loss prevention (DLP), you can define policies that prevent people from sharing sensitive information in a Microsoft Teams channel or chat session.</span></span> <span data-ttu-id="21d52-105">Voici quelques exemples de fonctionnement de cette protection :</span><span class="sxs-lookup"><span data-stu-id="21d52-105">Here are some examples of how this protection works:</span></span>

- <span data-ttu-id="21d52-106">**Exemple 1 : protection des informations sensibles dans les messages**.</span><span class="sxs-lookup"><span data-stu-id="21d52-106">**Example 1: Protecting sensitive information in messages**.</span></span> <span data-ttu-id="21d52-107">Supposons qu’une personne tente de partager des informations sensibles dans une conversation Teams ou un canal avec des invités (utilisateurs externes).</span><span class="sxs-lookup"><span data-stu-id="21d52-107">Suppose that someone attempts to share sensitive information in a Teams chat or channel with guests (external users).</span></span> <span data-ttu-id="21d52-108">Si vous avez défini une stratégie DLP pour éviter cela, les messages avec des informations sensibles envoyés à des utilisateurs externes sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="21d52-108">If you have a DLP policy defined to prevent this, messages with sensitive information that are sent to external users are deleted.</span></span> <span data-ttu-id="21d52-109">Cela se produit automatiquement et en quelques secondes, en fonction de la configuration de votre stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="21d52-109">This happens automatically, and within seconds, according to how your DLP policy is configured.</span></span>

    > [!NOTE]
    > <span data-ttu-id="21d52-110">La DLP pour Microsoft Teams bloque le contenu sensible lorsqu’il est partagé avec Microsoft Teams utilisateurs qui ont :</span><span class="sxs-lookup"><span data-stu-id="21d52-110">DLP for Microsoft Teams blocks sensitive content when shared with Microsoft Teams users who have:</span></span><br/><span data-ttu-id="21d52-111">- [accès invité dans](/MicrosoftTeams/guest-access) les équipes et les canaux ; ou</span><span class="sxs-lookup"><span data-stu-id="21d52-111">- [guest access](/MicrosoftTeams/guest-access) in teams and channels; or</span></span><br/><span data-ttu-id="21d52-112">- [accès externe](/MicrosoftTeams/manage-external-access) dans les réunions et les sessions de conversation.</span><span class="sxs-lookup"><span data-stu-id="21d52-112">- [external access](/MicrosoftTeams/manage-external-access) in meetings and chat sessions.</span></span> <p><span data-ttu-id="21d52-113">La DLP pour les sessions de conversation externe ne fonctionne que si l’expéditeur et le destinataire sont en mode Teams uniquement et utilisent la fédération Microsoft Teams [native.](/microsoftteams/manage-external-access)</span><span class="sxs-lookup"><span data-stu-id="21d52-113">DLP for external chat sessions will only work if both the sender and the receiver are in Teams Only mode and using [Microsoft Teams native federation](/microsoftteams/manage-external-access).</span></span> <span data-ttu-id="21d52-114">La prévention contre la Teams ne bloque pas les messages en cas [d’Skype Entreprise](/microsoftteams/teams-and-skypeforbusiness-coexistence-and-interoperability#interoperability-of-teams-and-skype-for-business) sessions de conversation fédérée non natives ou non natives.</span><span class="sxs-lookup"><span data-stu-id="21d52-114">DLP for Teams does not block messages in [interop](/microsoftteams/teams-and-skypeforbusiness-coexistence-and-interoperability#interoperability-of-teams-and-skype-for-business) with Skype for Business or non-native federated chat sessions.</span></span>

- <span data-ttu-id="21d52-115">**Exemple 2 : protection des informations sensibles dans les documents**.</span><span class="sxs-lookup"><span data-stu-id="21d52-115">**Example 2: Protecting sensitive information in documents**.</span></span> <span data-ttu-id="21d52-116">Supposons qu’une personne tente de partager un document avec des invités dans un canal Microsoft Teams ou une conversation, et que le document contient des informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="21d52-116">Suppose that someone attempts to share a document with guests in a Microsoft Teams channel or chat, and the document contains sensitive information.</span></span> <span data-ttu-id="21d52-117">Si vous avez défini une stratégie DLP pour éviter cela, le document ne s’ouvre pas pour ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="21d52-117">If you have a DLP policy defined to prevent this, the document won't open for those users.</span></span> <span data-ttu-id="21d52-118">Votre stratégie DLP doit inclure SharePoint et OneDrive pour que la protection soit en place.</span><span class="sxs-lookup"><span data-stu-id="21d52-118">Your DLP policy must include SharePoint and OneDrive in order for protection to be in place.</span></span> <span data-ttu-id="21d52-119">Il s’agit d’un exemple de DLP pour les SharePoint qui s’affiche dans Microsoft Teams et qui nécessite donc que les utilisateurs soient titulaires d’une licence pour Office 365 DLP (inclus dans Office 365 E3), mais ne nécessite pas que les utilisateurs soient titulaires d’une licence pour Conformité avancée Office 365.)</span><span class="sxs-lookup"><span data-stu-id="21d52-119">This is an example of DLP for SharePoint that shows up in Microsoft Teams, and therefore requires that users are licensed for Office 365 DLP (included in Office 365 E3), but does not require users to be licensed for Office 365 Advanced Compliance.)</span></span>

## <a name="dlp-licensing-for-microsoft-teams"></a><span data-ttu-id="21d52-120">Gestion des licences DLP pour Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="21d52-120">DLP Licensing for Microsoft Teams</span></span>

<span data-ttu-id="21d52-121">[Les fonctionnalités de protection](dlp-learn-about-dlp.md) contre la perte de données ont été étendues pour inclure Microsoft Teams messages de conversation et de canal, y compris les **messages de canal privé** pour :</span><span class="sxs-lookup"><span data-stu-id="21d52-121">[Data loss prevention](dlp-learn-about-dlp.md) capabilities were extended to include Microsoft Teams chat and channel messages, **including private channel messages** for:</span></span>

- <span data-ttu-id="21d52-122">Office 365 E5/A5</span><span class="sxs-lookup"><span data-stu-id="21d52-122">Office 365 E5/A5</span></span>
- <span data-ttu-id="21d52-123">Microsoft 365 E5/A5</span><span class="sxs-lookup"><span data-stu-id="21d52-123">Microsoft 365 E5/A5</span></span>
- <span data-ttu-id="21d52-124">Protection des informations et gouvernance Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="21d52-124">Microsoft 365 Information Protection and Governance</span></span>
- <span data-ttu-id="21d52-125">Conformité avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="21d52-125">Office 365 Advanced Compliance</span></span>

<span data-ttu-id="21d52-126">Office 365 et Microsoft 365 E3 incluent la protection DLP pour SharePoint Online, OneDrive et Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="21d52-126">Office 365 and Microsoft 365 E3 include DLP protection for SharePoint Online, OneDrive, and Exchange Online.</span></span> <span data-ttu-id="21d52-127">Cela inclut également les fichiers partagés via Teams, car Teams utilise SharePoint Online et OneDrive pour partager des fichiers.</span><span class="sxs-lookup"><span data-stu-id="21d52-127">This also includes files that are shared through Teams because Teams uses SharePoint Online and OneDrive to share files.</span></span>

<span data-ttu-id="21d52-128">La prise en charge de la protection DLP dans Teams chat nécessite E5.</span><span class="sxs-lookup"><span data-stu-id="21d52-128">Support for DLP protection in Teams Chat requires E5.</span></span>

<span data-ttu-id="21d52-129">Pour en savoir plus sur les conditions d’octroi de licences, consultez [Conseils sur la gestion des licences des services de niveau client de Microsoft 365](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).</span><span class="sxs-lookup"><span data-stu-id="21d52-129">To learn more about licensing requirements, see [Microsoft 365 Tenant-Level Services Licensing Guidance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21d52-130">DLP s’applique uniquement aux messages réels dans le thread de conversation ou de canal.</span><span class="sxs-lookup"><span data-stu-id="21d52-130">DLP applies only to the actual messages in the chat or channel thread.</span></span> <span data-ttu-id="21d52-131">Les notifications d’activité, qui incluent un aperçu de message court et  s’affichent en fonction des paramètres de notification d’un utilisateur, ne sont pas incluses dans Teams DLP.</span><span class="sxs-lookup"><span data-stu-id="21d52-131">Activity notifications -- which include a short message preview and appear based on a user's notification settings -- are **not** included in Teams DLP.</span></span> <span data-ttu-id="21d52-132">Toutes les informations sensibles présentes dans la partie du message qui s’affiche dans l’aperçu resteront visibles dans la notification même après l’application de la stratégie DLP et la suppression des informations sensibles du message lui-même.</span><span class="sxs-lookup"><span data-stu-id="21d52-132">Any sensitive information present in the part of the message that appears in the preview will remain visible in the notification even after the DLP policy has been applied and removed sensitive information the message itself.</span></span>

## <a name="scope-of-dlp-protection"></a><span data-ttu-id="21d52-133">Étendue de la protection DLP</span><span class="sxs-lookup"><span data-stu-id="21d52-133">Scope of DLP protection</span></span>

<span data-ttu-id="21d52-134">La protection DLP est appliquée différemment Teams entités.</span><span class="sxs-lookup"><span data-stu-id="21d52-134">DLP protection are applied differently to Teams entities.</span></span>

|<span data-ttu-id="21d52-135">Comptes d’utilisateur/groupes/liste</span><span class="sxs-lookup"><span data-stu-id="21d52-135">User Accounts/Groups/List</span></span>  |<span data-ttu-id="21d52-136">Teams Entité</span><span class="sxs-lookup"><span data-stu-id="21d52-136">Teams Entity</span></span> |<span data-ttu-id="21d52-137">Protection DLP disponible</span><span class="sxs-lookup"><span data-stu-id="21d52-137">DLP protection available</span></span>|
|---------|---------|---------|
|<span data-ttu-id="21d52-138">comptes d’utilisateur individuels</span><span class="sxs-lookup"><span data-stu-id="21d52-138">individual user accounts</span></span>     |<span data-ttu-id="21d52-139">Conversations 1:1/n</span><span class="sxs-lookup"><span data-stu-id="21d52-139">1:1/n chats</span></span>         |<span data-ttu-id="21d52-140">oui</span><span class="sxs-lookup"><span data-stu-id="21d52-140">yes</span></span>         |
|     |<span data-ttu-id="21d52-141">conversations générales</span><span class="sxs-lookup"><span data-stu-id="21d52-141">general chats</span></span>         |<span data-ttu-id="21d52-142">non</span><span class="sxs-lookup"><span data-stu-id="21d52-142">no</span></span>         |
|     |<span data-ttu-id="21d52-143">canaux privés</span><span class="sxs-lookup"><span data-stu-id="21d52-143">private channels</span></span>         |<span data-ttu-id="21d52-144">oui</span><span class="sxs-lookup"><span data-stu-id="21d52-144">yes</span></span>         |
|<span data-ttu-id="21d52-145">groupes de sécurité/listes de distribution</span><span class="sxs-lookup"><span data-stu-id="21d52-145">security groups/distribution lists</span></span>  | <span data-ttu-id="21d52-146">Conversations 1:1/n</span><span class="sxs-lookup"><span data-stu-id="21d52-146">1:1/n chats</span></span>         |<span data-ttu-id="21d52-147">oui</span><span class="sxs-lookup"><span data-stu-id="21d52-147">yes</span></span>         |
|     |<span data-ttu-id="21d52-148">conversations générales</span><span class="sxs-lookup"><span data-stu-id="21d52-148">general chats</span></span>         |<span data-ttu-id="21d52-149">non</span><span class="sxs-lookup"><span data-stu-id="21d52-149">no</span></span>         |
|     |<span data-ttu-id="21d52-150">canaux privés</span><span class="sxs-lookup"><span data-stu-id="21d52-150">private channels</span></span>         |<span data-ttu-id="21d52-151">oui</span><span class="sxs-lookup"><span data-stu-id="21d52-151">yes</span></span>        |
|<span data-ttu-id="21d52-152">Microsoft 365 groupe</span><span class="sxs-lookup"><span data-stu-id="21d52-152">Microsoft 365 group</span></span>    |<span data-ttu-id="21d52-153">Conversations 1:1/n</span><span class="sxs-lookup"><span data-stu-id="21d52-153">1:1/n chats</span></span>          |<span data-ttu-id="21d52-154">non</span><span class="sxs-lookup"><span data-stu-id="21d52-154">no</span></span>         |
|     |<span data-ttu-id="21d52-155">conversations générales</span><span class="sxs-lookup"><span data-stu-id="21d52-155">general chats</span></span>          |<span data-ttu-id="21d52-156">oui</span><span class="sxs-lookup"><span data-stu-id="21d52-156">yes</span></span>        |
|     |<span data-ttu-id="21d52-157">canaux privés</span><span class="sxs-lookup"><span data-stu-id="21d52-157">private channels</span></span>|<span data-ttu-id="21d52-158">non</span><span class="sxs-lookup"><span data-stu-id="21d52-158">no</span></span>| 


## <a name="policy-tips-help-educate-users"></a><span data-ttu-id="21d52-159">Les conseils de stratégie aident à former les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="21d52-159">Policy tips help educate users</span></span>

<span data-ttu-id="21d52-160">De la même manière que dans [Exchange, Outlook, Outlook](data-loss-prevention-policies.md#policy-evaluation-in-exchange-online-outlook-and-outlook-on-the-web)sur le web, [SharePoint Online, les sites OneDrive Entreprise](data-loss-prevention-policies.md#policy-evaluation-in-onedrive-for-business-and-sharepoint-online-sites)et les clients de bureau [Office,](data-loss-prevention-policies.md#policy-evaluation-in-the-office-desktop-programs)des conseils de stratégie s’affichent lorsqu’une action se déclenche avec une stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="21d52-160">Similar to how DLP works in [Exchange, Outlook, Outlook on the web](data-loss-prevention-policies.md#policy-evaluation-in-exchange-online-outlook-and-outlook-on-the-web), [SharePoint Online, OneDrive for Business sites](data-loss-prevention-policies.md#policy-evaluation-in-onedrive-for-business-and-sharepoint-online-sites), and [Office desktop clients](data-loss-prevention-policies.md#policy-evaluation-in-the-office-desktop-programs), policy tips appear when an action triggers with a DLP policy.</span></span> <span data-ttu-id="21d52-161">Voici un exemple de conseil de stratégie :</span><span class="sxs-lookup"><span data-stu-id="21d52-161">Here's an example of a policy tip:</span></span>

![Notification de message bloqué dans Teams](../media/dlp-teams-blockedmessage-notification.png)

<span data-ttu-id="21d52-163">Ici, l’expéditeur a tenté de partager un numéro de sécurité sociale dans un canal Microsoft Teams réseau.</span><span class="sxs-lookup"><span data-stu-id="21d52-163">Here, the sender attempted to share a social security number in a Microsoft Teams channel.</span></span> <span data-ttu-id="21d52-164">Le **lien Que puis-je faire ?** ouvre une boîte de dialogue qui fournit des options à l’expéditeur pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="21d52-164">The **What can I do?** link opens a dialog box that provides options for the sender to resolve the issue.</span></span> <span data-ttu-id="21d52-165">Notez que l’expéditeur peut choisir de remplacer la stratégie ou d’avertir un administrateur de la réviser et de la résoudre.</span><span class="sxs-lookup"><span data-stu-id="21d52-165">Notice that, the sender can opt to override the policy, or notify an admin to review and resolve it.</span></span>

![Options pour résoudre le message bloqué](../media/dlp-teams-blockedmessage-possibleactions.png)

<span data-ttu-id="21d52-167">Dans votre organisation, vous pouvez choisir d’autoriser les utilisateurs à remplacer une stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="21d52-167">In your organization, you can choose to allow users to override a DLP policy.</span></span> <span data-ttu-id="21d52-168">Lorsque vous configurez vos stratégies DLP, vous pouvez utiliser les conseils de stratégie par défaut ou personnaliser les conseils [de](#to-customize-policy-tips) stratégie pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="21d52-168">When you configure your DLP policies, you can use the default policy tips, or [customize policy tips](#to-customize-policy-tips) for your organization.</span></span>

<span data-ttu-id="21d52-169">Pour revenir à notre exemple, où un expéditeur a partagé un numéro de sécurité sociale dans un canal Teams, voici ce que le destinataire a vu :</span><span class="sxs-lookup"><span data-stu-id="21d52-169">Returning to our example, where a sender shared a social security number in a Teams channel, here's what the recipient saw:</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="21d52-170">![Message bloqué](../media/dlp-teams-blockedmessage-notification-to-user.png)</span><span class="sxs-lookup"><span data-stu-id="21d52-170">![Message blocked](../media/dlp-teams-blockedmessage-notification-to-user.png)</span></span>

### <a name="to-customize-policy-tips"></a><span data-ttu-id="21d52-171">Pour personnaliser les conseils de stratégie</span><span class="sxs-lookup"><span data-stu-id="21d52-171">To customize policy tips</span></span>

<span data-ttu-id="21d52-172">Pour effectuer cette tâche, vous devez avoir un rôle qui dispose des autorisations pour modifier les stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="21d52-172">To perform this task, you must be assigned a role that has permissions to edit DLP policies.</span></span> <span data-ttu-id="21d52-173">Pour en savoir plus, voir [Autorisations](data-loss-prevention-policies.md#permissions).</span><span class="sxs-lookup"><span data-stu-id="21d52-173">To learn more, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

1. <span data-ttu-id="21d52-174">Go to the Compliance Center ( [https://compliance.microsoft.com](https://compliance.microsoft.com) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="21d52-174">Go to the Compliance Center ([https://compliance.microsoft.com](https://compliance.microsoft.com)) and sign in.</span></span>

2. <span data-ttu-id="21d52-175">Choisissez **la stratégie de protection contre la perte de**  >  **données.**</span><span class="sxs-lookup"><span data-stu-id="21d52-175">Choose **Data loss prevention** > **Policy**.</span></span>

3. <span data-ttu-id="21d52-176">Select a policy, and next to **Policy settings**, choose **Edit**.</span><span class="sxs-lookup"><span data-stu-id="21d52-176">Select a policy, and next to **Policy settings**, choose **Edit**.</span></span>

4. <span data-ttu-id="21d52-177">Créez une règle ou modifiez une règle existante pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="21d52-177">Either create a new rule, or edit an existing rule for the policy.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="21d52-178">![Modification d’une règle pour une stratégie](../media/dlp-teams-editrule.png)</span><span class="sxs-lookup"><span data-stu-id="21d52-178">![Editing a rule for a policy](../media/dlp-teams-editrule.png)</span></span>

5. <span data-ttu-id="21d52-179">Sous **l’onglet Notifications de** l’utilisateur, sélectionnez Personnaliser le texte de l’e-mail et/ou personnaliser les options de texte du **conseil de** stratégie. </span><span class="sxs-lookup"><span data-stu-id="21d52-179">On the **User notifications** tab, select **Customize the email text** and/or **Customize the policy tip text** options.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="21d52-180">![Personnaliser les notifications utilisateur et les conseils de stratégie](../media/dlp-teams-editrule-usernotifications.png)</span><span class="sxs-lookup"><span data-stu-id="21d52-180">![Customize user notifications and policy tips](../media/dlp-teams-editrule-usernotifications.png)</span></span><br/>  

6. <span data-ttu-id="21d52-181">Spécifiez le texte que vous souhaitez utiliser pour les notifications par courrier électronique et/ou les conseils de stratégie, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="21d52-181">Specify the text you want to use for email notifications and/or policy tips, and then choose **Save**.</span></span>

7. <span data-ttu-id="21d52-182">Sous **l’onglet Paramètres de stratégie,** sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="21d52-182">On the **Policy settings** tab, choose **Save**.</span></span>

<span data-ttu-id="21d52-183">Laissez environ une heure pour que vos modifications fonctionnent dans votre centre de données et se synchronisent avec les comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="21d52-183">Allow approximately one hour for your changes to work their way through your data center and sync to user accounts.</span></span>
 <!-- why are these syncing to user accounts? -->

## <a name="add-microsoft-teams-as-a-location-to-existing-dlp-policies"></a><span data-ttu-id="21d52-184">Ajouter Microsoft Teams comme emplacement aux stratégies DLP existantes</span><span class="sxs-lookup"><span data-stu-id="21d52-184">Add Microsoft Teams as a location to existing DLP policies</span></span>

<span data-ttu-id="21d52-185">Pour effectuer cette tâche, vous devez avoir un rôle qui dispose des autorisations pour modifier les stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="21d52-185">To perform this task, you must be assigned a role that has permissions to edit DLP policies.</span></span> <span data-ttu-id="21d52-186">Pour en savoir plus, voir [Autorisations](data-loss-prevention-policies.md#permissions).</span><span class="sxs-lookup"><span data-stu-id="21d52-186">To learn more, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

1. <span data-ttu-id="21d52-187">Go to the Compliance Center ( [https://compliance.microsoft.com](https://compliance.microsoft.com) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="21d52-187">Go to the Compliance Center ([https://compliance.microsoft.com](https://compliance.microsoft.com)) and sign in.</span></span>

2. <span data-ttu-id="21d52-188">Choisissez **la stratégie de protection contre la perte de**  >  **données.**</span><span class="sxs-lookup"><span data-stu-id="21d52-188">Choose **Data loss prevention** > **Policy**.</span></span>

3. <span data-ttu-id="21d52-189">Sélectionnez une stratégie et regardez les valeurs sous **Emplacements.**</span><span class="sxs-lookup"><span data-stu-id="21d52-189">Select a policy, and look at the values under **Locations**.</span></span> <span data-ttu-id="21d52-190">Si vous voyez des **Teams de conversation et de canal,** vous êtes tous ensemble.</span><span class="sxs-lookup"><span data-stu-id="21d52-190">If you see **Teams chat and channel messages**, you're all set.</span></span> <span data-ttu-id="21d52-191">Si ce n’est pas le cas, cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="21d52-191">If you don't, click **Edit**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="21d52-192">![Emplacements pour la stratégie existante](../media/dlp-teams-editexistingpolicy.png)</span><span class="sxs-lookup"><span data-stu-id="21d52-192">![Locations for existing policy](../media/dlp-teams-editexistingpolicy.png)</span></span>

4. <span data-ttu-id="21d52-193">Dans la **colonne État,** activer la stratégie pour les messages **Teams de conversation et de canal.**</span><span class="sxs-lookup"><span data-stu-id="21d52-193">In the **Status** column, turn the policy on for **Teams chat and channel messages**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="21d52-194">![DLP pour les Teams et les canaux](../media/dlp-teams-addteamschatschannels.png)</span><span class="sxs-lookup"><span data-stu-id="21d52-194">![DLP for Teams chats and channels](../media/dlp-teams-addteamschatschannels.png)</span></span>

5. <span data-ttu-id="21d52-195">Sous **l’onglet** Choisir des emplacements, conservez le paramètre par défaut de tous les comptes, ou sélectionnez **Choisir des emplacements spécifiques.**</span><span class="sxs-lookup"><span data-stu-id="21d52-195">On the **Choose locations** tab, keep the default setting of all accounts, or select **Let me choose specific locations**.</span></span> <span data-ttu-id="21d52-196">Vous pouvez spécifier :</span><span class="sxs-lookup"><span data-stu-id="21d52-196">You can specify:</span></span>

    1. <span data-ttu-id="21d52-197">jusqu’à 1 000 comptes individuels à inclure ou à exclure</span><span class="sxs-lookup"><span data-stu-id="21d52-197">up to 1000 individual accounts to include or exclude</span></span>
    1. <span data-ttu-id="21d52-198">listes de distribution et groupes de sécurité à inclure ou à exclure;</span><span class="sxs-lookup"><span data-stu-id="21d52-198">distribution lists and security groups to include or exclude.</span></span> 
    <!-- 1. the shared mailbox of a shared channel. **This is a public preview feature.**--> 
    
6. <span data-ttu-id="21d52-199">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="21d52-199">Then choose **Next**.</span></span>

7. <span data-ttu-id="21d52-200">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="21d52-200">Click **Save**.</span></span>

<span data-ttu-id="21d52-201">Laissez environ une heure pour que vos modifications fonctionnent dans votre centre de données et se synchronisent avec les comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="21d52-201">Allow approximately one hour for your changes to work their way through your data center and sync to user accounts.</span></span>
<!-- again, why user accounts? -->

## <a name="define-a-new-dlp-policy-for-microsoft-teams"></a><span data-ttu-id="21d52-202">Définir une nouvelle stratégie DLP pour Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="21d52-202">Define a new DLP policy for Microsoft Teams</span></span>

<span data-ttu-id="21d52-203">Pour effectuer cette tâche, vous devez avoir un rôle qui dispose des autorisations pour modifier les stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="21d52-203">To perform this task, you must be assigned a role that has permissions to edit DLP policies.</span></span> <span data-ttu-id="21d52-204">Pour en savoir plus, voir [Autorisations](data-loss-prevention-policies.md#permissions).</span><span class="sxs-lookup"><span data-stu-id="21d52-204">To learn more, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

1. <span data-ttu-id="21d52-205">Go to the Compliance Center ( [https://compliance.microsoft.com](https://compliance.microsoft.com) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="21d52-205">Go to the Compliance Center ([https://compliance.microsoft.com](https://compliance.microsoft.com)) and sign in.</span></span>

2. <span data-ttu-id="21d52-206">Choisissez **stratégie de protection contre la perte**  >  **de**  >  **données + Créer une stratégie.**</span><span class="sxs-lookup"><span data-stu-id="21d52-206">Choose **Data loss prevention** > **Policy** > **+ Create a policy**.</span></span>

3. <span data-ttu-id="21d52-207">Choisissez un [modèle,](data-loss-prevention-policies.md#dlp-policy-templates)puis choisissez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="21d52-207">Choose a [template](data-loss-prevention-policies.md#dlp-policy-templates), and then choose **Next**.</span></span>

    <span data-ttu-id="21d52-208">Dans notre exemple, nous avons choisi le modèle de données d’informations d’identification personnelle des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="21d52-208">In our example, we chose the U.S. Personally Identifiable Information Data template.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="21d52-209">![Modèle de confidentialité pour la stratégie DLP](../media/dlp-teams-createnewpolicy-template.png)</span><span class="sxs-lookup"><span data-stu-id="21d52-209">![Privacy template for DLP policy](../media/dlp-teams-createnewpolicy-template.png)</span></span><br/>

4. <span data-ttu-id="21d52-210">Sous **l’onglet Nom de votre stratégie,** spécifiez un nom et une description pour la stratégie, puis choisissez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="21d52-210">On the **Name your policy** tab, specify a name and description for the policy, and then choose **Next**.</span></span>

5. <span data-ttu-id="21d52-211">Sous **l’onglet** Choisir des emplacements, conservez le paramètre par défaut de tous les comptes, ou sélectionnez **Choisir des emplacements spécifiques.**</span><span class="sxs-lookup"><span data-stu-id="21d52-211">On the **Choose locations** tab, keep the default setting of all accounts, or select **Let me choose specific locations**.</span></span> <span data-ttu-id="21d52-212">Vous pouvez spécifier :</span><span class="sxs-lookup"><span data-stu-id="21d52-212">You can specify:</span></span>

    1. <span data-ttu-id="21d52-213">jusqu’à 1 000 comptes individuels à inclure ou à exclure</span><span class="sxs-lookup"><span data-stu-id="21d52-213">up to 1000 individual accounts to include or exclude</span></span>
    1. <span data-ttu-id="21d52-214">listes de distribution et groupes de sécurité à inclure ou à exclure;</span><span class="sxs-lookup"><span data-stu-id="21d52-214">distribution lists and security groups to include or exclude.</span></span> <span data-ttu-id="21d52-215">**Il s’agit d’une fonctionnalité de prévisualisation publique.**</span><span class="sxs-lookup"><span data-stu-id="21d52-215">**This is a public preview feature.**</span></span>
    <!-- 1. the shared mailbox of a shared channel. **This is a public preview feature.**-->  

    ![Emplacements de stratégie DLP](../media/dlp-teams-selectlocationsnewpolicy.png)

    > [!NOTE]
    > <span data-ttu-id="21d52-217">Si vous souhaitez vous assurer que les documents qui contiennent des informations sensibles ne sont pas partagés de manière inappropriée dans Teams, assurez-vous que les **sites SharePoint** et les comptes OneDrive sont **allumés,** ainsi que les messages de conversation et de canal **Teams.**</span><span class="sxs-lookup"><span data-stu-id="21d52-217">If you want to make sure documents that contain sensitive information are not shared inappropriately in Teams, make sure **SharePoint sites** and **OneDrive accounts** are turned on, along with **Teams chat and channel messages**.</span></span>

6. <span data-ttu-id="21d52-218">Sous **l’onglet Paramètres** de stratégie, sous Personnaliser le **type** de contenu à protéger, conservez les paramètres simples par défaut, ou choisissez Utiliser les **paramètres** avancés, puis choisissez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="21d52-218">On the **Policy settings** tab, under **Customize the type of content you want to protect**, keep the default simple settings, or choose **Use advanced settings**, and then choose **Next**.</span></span> <span data-ttu-id="21d52-219">Si vous choisissez des paramètres avancés, vous pouvez créer ou modifier des règles pour votre stratégie.</span><span class="sxs-lookup"><span data-stu-id="21d52-219">If you choose advanced settings, you can create or edit rules for your policy.</span></span> <span data-ttu-id="21d52-220">Pour obtenir de l’aide, voir [Paramètres simples et paramètres avancés.](data-loss-prevention-policies.md#simple-settings-vs-advanced-settings)</span><span class="sxs-lookup"><span data-stu-id="21d52-220">To get help with this, see [Simple settings vs. advanced settings](data-loss-prevention-policies.md#simple-settings-vs-advanced-settings).</span></span>

7.  <span data-ttu-id="21d52-221">Sous **l’onglet Paramètres de stratégie,** sous Que voulez-vous faire si nous détectons des informations sensibles **?**, examinez les paramètres.</span><span class="sxs-lookup"><span data-stu-id="21d52-221">On the **Policy settings** tab, under **What do you want to do if we detect sensitive info?**, review the settings.</span></span> <span data-ttu-id="21d52-222">C’est ici que vous pouvez choisir de conserver les conseils de stratégie par défaut et les [notifications par courrier électronique,](use-notifications-and-policy-tips.md)ou de les personnaliser.</span><span class="sxs-lookup"><span data-stu-id="21d52-222">Here's where you can choose to keep default [policy tips and email notifications](use-notifications-and-policy-tips.md), or customize them.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="21d52-223">![Paramètres de stratégie DLP avec conseils et notifications](../media/dlp-teams-policysettings-tipsemails.png)</span><span class="sxs-lookup"><span data-stu-id="21d52-223">![DLP policy settings with tips and notifications](../media/dlp-teams-policysettings-tipsemails.png)</span></span>

    <span data-ttu-id="21d52-224">Lorsque vous avez terminé de passer en revue ou de modifier les paramètres, choisissez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="21d52-224">When you're finished reviewing or editing settings, choose **Next**.</span></span>

8. <span data-ttu-id="21d52-225">Sous l’onglet **Paramètres** de stratégie, sous Voulez-vous activer la stratégie ou d’abord tester les éléments **?**, choisissez d’activer la [stratégie,](dlp-overview-plan-for-dlp.md#policy-deployment)de la tester en premier ou de la maintenir désactivée pour l’instant, puis choisissez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="21d52-225">On the **Policy settings** tab, under **Do you want to turn on the policy or test things out first?**, choose whether to turn the policy on, [test it first](dlp-overview-plan-for-dlp.md#policy-deployment), or keep it turned off for now, and then choose **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="21d52-226">![Spécifier s’il faut activer la stratégie](../media/dlp-teams-policysettings-turnonnow.png)</span><span class="sxs-lookup"><span data-stu-id="21d52-226">![Specify whether to turn the policy on](../media/dlp-teams-policysettings-turnonnow.png)</span></span>

9. <span data-ttu-id="21d52-227">Sous **l’onglet Examiner vos paramètres,** examinez les paramètres de votre nouvelle stratégie.</span><span class="sxs-lookup"><span data-stu-id="21d52-227">On the **Review your settings** tab, review the settings for your new policy.</span></span> <span data-ttu-id="21d52-228">Sélectionnez **Modifier** pour apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="21d52-228">Choose **Edit** to make changes.</span></span> <span data-ttu-id="21d52-229">Lorsque vous avez terminé, choisissez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="21d52-229">When you're finished, choose **Create**.</span></span>

<span data-ttu-id="21d52-230">Laissez environ une heure à votre nouvelle stratégie pour passer par votre centre de données et se synchroniser avec les comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="21d52-230">Allow approximately one hour for your new policy to work its way through your data center and sync to user accounts.</span></span>

## <a name="prevent-external-access-to-sensitive-documents"></a><span data-ttu-id="21d52-231">Empêcher l'accès externe aux documents sensibles</span><span class="sxs-lookup"><span data-stu-id="21d52-231">Prevent external access to sensitive documents</span></span>

<span data-ttu-id="21d52-232">Pour vous assurer que SharePoint documents contenant des informations sensibles ne peuvent pas être accessibles par des invités externes à partir de SharePoint ou Teams par défaut, sélectionnez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="21d52-232">To ensure that SharePoint documents that contain sensitive information cannot be accessed by external guests either from SharePoint or Teams by default, select the following:</span></span>

- <span data-ttu-id="21d52-233">Vous pouvez vous assurer que les documents sont protégés jusqu’à ce que DLP analyse et les marque comme étant sûrs à partager en marquant les nouveaux fichiers comme sensibles [par défaut.](/sharepoint/sensitive-by-default)</span><span class="sxs-lookup"><span data-stu-id="21d52-233">You can ensure that documents are protected until DLP scans and marks them as safe to share by [marking new files as sensitive by default](/sharepoint/sensitive-by-default).</span></span>

- <span data-ttu-id="21d52-234">Structure de stratégie DLP recommandée</span><span class="sxs-lookup"><span data-stu-id="21d52-234">Recommended DLP policy structure</span></span>

    - <span data-ttu-id="21d52-235">**Conditions**</span><span class="sxs-lookup"><span data-stu-id="21d52-235">**Conditions**</span></span>
        - <span data-ttu-id="21d52-236">Le contenu contient l’un de ces types d’informations sensibles : [Sélectionner tout ce qui s’applique]</span><span class="sxs-lookup"><span data-stu-id="21d52-236">Content contains any of these sensitive information types: [Select all that apply]</span></span>
        
        - <span data-ttu-id="21d52-237">Le contenu est partagé à partir Microsoft 365 avec des personnes extérieures à mon organisation</span><span class="sxs-lookup"><span data-stu-id="21d52-237">Content is shared from Microsoft 365 with people outside my organization</span></span>
        
          > [!div class="mx-imgBorder"]
          > <span data-ttu-id="21d52-238">![Conditions DLP pour détecter le partage externe de contenu sensible](../media/dlp-teams-external-sharing/external-condition.png)</span><span class="sxs-lookup"><span data-stu-id="21d52-238">![DLP conditions to detect external sharing of sensitive content](../media/dlp-teams-external-sharing/external-condition.png)</span></span>

    - <span data-ttu-id="21d52-239">**Actions**</span><span class="sxs-lookup"><span data-stu-id="21d52-239">**Actions**</span></span>
        - <span data-ttu-id="21d52-240">Restreindre l’accès au contenu pour utilisateurs externe</span><span class="sxs-lookup"><span data-stu-id="21d52-240">Restrict access to the content for external users</span></span>
        
        - <span data-ttu-id="21d52-241">Informer les utilisateurs à l’aide de courriers électroniques et de conseils de stratégie</span><span class="sxs-lookup"><span data-stu-id="21d52-241">Notify users with email and policy tips</span></span>
        
        - <span data-ttu-id="21d52-242">Envoyer des rapports d’incident à l’administrateur</span><span class="sxs-lookup"><span data-stu-id="21d52-242">Send incident reports to the Administrator</span></span>
        
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="21d52-243">![Action DLP pour bloquer le partage externe de contenu sensible](../media/dlp-teams-external-sharing/external-action.png)</span><span class="sxs-lookup"><span data-stu-id="21d52-243">![DLP action to block external sharing of sensitive content](../media/dlp-teams-external-sharing/external-action.png)</span></span>

<span data-ttu-id="21d52-244">Stratégie DLP en action lors de la tentative de partage d’un document dans SharePoint contenant des informations sensibles avec un invité externe :</span><span class="sxs-lookup"><span data-stu-id="21d52-244">DLP policy in action when attempting to share a document in SharePoint that contains sensitive information with an external guest:</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="21d52-245">![Partage externe bloqué](../media/dlp-teams-external-sharing/external-sharing-blocked.png)</span><span class="sxs-lookup"><span data-stu-id="21d52-245">![External sharing blocked](../media/dlp-teams-external-sharing/external-sharing-blocked.png)</span></span>


<span data-ttu-id="21d52-246">Stratégie DLP en action lorsque l’invité tente d’ouvrir un document Teams avec un bloc externe :</span><span class="sxs-lookup"><span data-stu-id="21d52-246">DLP policy in action when guest attempts to open a document in Teams with block external:</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="21d52-247">![Accès externe bloqué](../media/dlp-teams-external-sharing/external-access-blocked.png)</span><span class="sxs-lookup"><span data-stu-id="21d52-247">![External access blocked](../media/dlp-teams-external-sharing/external-access-blocked.png)</span></span>

## <a name="related-articles"></a><span data-ttu-id="21d52-248">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="21d52-248">Related articles</span></span>

- [<span data-ttu-id="21d52-249">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="21d52-249">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="21d52-250">Envoi des notifications et affichage des conseils de stratégie pour les stratégies DLP</span><span class="sxs-lookup"><span data-stu-id="21d52-250">Send email notifications and show policy tips for DLP policies</span></span>](use-notifications-and-policy-tips.md)
