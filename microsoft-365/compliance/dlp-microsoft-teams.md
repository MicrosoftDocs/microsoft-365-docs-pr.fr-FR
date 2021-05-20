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
description: Vous pouvez désormais appliquer des stratégies DLP à Microsoft Teams conversations et canaux. Lisez cet article pour en savoir plus sur son fonctionnement.
ms.openlocfilehash: 9fdce86473dcfbb7ec75b9d371b8782d4141ef57
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52572464"
---
# <a name="data-loss-prevention-and-microsoft-teams"></a><span data-ttu-id="7f54a-104">Prévention des pertes de données et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7f54a-104">Data loss prevention and Microsoft Teams</span></span>

> [!NOTE]
> <span data-ttu-id="7f54a-105">Des fonctionnalités de protection contre la perte de données ont été récemment ajoutées aux messages de conversation et de canal Microsoft Teams pour les utilisateurs titulaires d’une licence Office 365 E5/A5, Microsoft 365 E5/A5, Microsoft 365 Information Protection and Governance ou Conformité avancée Office 365.</span><span class="sxs-lookup"><span data-stu-id="7f54a-105">Data loss prevention capabilities were recently added to Microsoft Teams chat and channel messages for users licensed for Office 365 E5/A5, Microsoft 365 E5/A5, Microsoft 365 Information Protection and Governance or Office 365 Advanced Compliance.</span></span> <span data-ttu-id="7f54a-106">Office 365 et Microsoft 365 E3 incluent la protection DLP pour SharePoint Online, OneDrive et Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="7f54a-106">Office 365 and Microsoft 365 E3 include DLP protection for SharePoint Online, OneDrive, and Exchange Online.</span></span> <span data-ttu-id="7f54a-107">Cela inclut également les fichiers partagés via Teams, car Teams utilise SharePoint Online et OneDrive pour partager des fichiers.</span><span class="sxs-lookup"><span data-stu-id="7f54a-107">This also includes files that are shared through Teams because Teams uses SharePoint Online and OneDrive to share files.</span></span>
<span data-ttu-id="7f54a-108">La prise en charge de la protection DLP dans Teams chat nécessite E5.</span><span class="sxs-lookup"><span data-stu-id="7f54a-108">Support for DLP protection in Teams Chat requires E5.</span></span>
<span data-ttu-id="7f54a-109">Pour en savoir plus sur les conditions d’octroi de licences, consultez [Conseils sur la gestion des licences des services de niveau client de Microsoft 365](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance).</span><span class="sxs-lookup"><span data-stu-id="7f54a-109">To learn more about licensing requirements, see [Microsoft 365 Tenant-Level Services Licensing Guidance](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance).</span></span>

## <a name="overview-of-dlp-for-microsoft-teams"></a><span data-ttu-id="7f54a-110">Aperçu du DLP pour Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7f54a-110">Overview of DLP for Microsoft Teams</span></span>

<span data-ttu-id="7f54a-111">Récemment, [les fonctionnalités de protection](dlp-learn-about-dlp.md) contre la perte de données ont été étendues pour inclure Microsoft Teams messages de conversation et de canal, y compris les messages de canal **privé.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-111">Recently, [data loss prevention](dlp-learn-about-dlp.md) capabilities were extended to include Microsoft Teams chat and channel messages, **including private channel messages**.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="7f54a-112">La DLP s’applique actuellement uniquement aux messages réels dans le thread de conversation ou de canal.</span><span class="sxs-lookup"><span data-stu-id="7f54a-112">DLP currently applies only to the actual messages in the chat or channel thread.</span></span> <span data-ttu-id="7f54a-113">Les notifications d’activité, qui incluent un aperçu de message court et  s’affichent en fonction des paramètres de notification d’un utilisateur, ne sont pas incluses dans Teams DLP pour le moment.</span><span class="sxs-lookup"><span data-stu-id="7f54a-113">Activity notifications -- which include a short message preview and appear based on a user's notification settings -- are **not** included in Teams DLP at this time.</span></span> <span data-ttu-id="7f54a-114">Toutes les informations sensibles présentes dans la partie du message qui s’affiche dans l’aperçu resteront visibles dans la notification même après l’application de la stratégie DLP et la suppression des informations sensibles du message lui-même.</span><span class="sxs-lookup"><span data-stu-id="7f54a-114">Any sensitive information present in the part of the message that appears in the preview will remain visible in the notification even after the DLP policy has been applied and removed sensitive information the message itself.</span></span>

<span data-ttu-id="7f54a-115">Si votre organisation dispose d’une DLP, vous pouvez désormais définir des stratégies qui empêchent les personnes de partager des informations sensibles dans un canal Microsoft Teams ou une session de conversation.</span><span class="sxs-lookup"><span data-stu-id="7f54a-115">If your organization has DLP, you can now define policies that prevent people from sharing sensitive information in a Microsoft Teams channel or chat session.</span></span> <span data-ttu-id="7f54a-116">Voici quelques exemples de fonctionnement de cette protection :</span><span class="sxs-lookup"><span data-stu-id="7f54a-116">Here are some examples of how this protection works:</span></span>

- <span data-ttu-id="7f54a-117">**Exemple 1 : protection des informations sensibles dans les messages**.</span><span class="sxs-lookup"><span data-stu-id="7f54a-117">**Example 1: Protecting sensitive information in messages**.</span></span> <span data-ttu-id="7f54a-118">Supposons qu’une personne tente de partager des informations sensibles dans une conversation Teams ou un canal avec des invités (utilisateurs externes).</span><span class="sxs-lookup"><span data-stu-id="7f54a-118">Suppose that someone attempts to share sensitive information in a Teams chat or channel with guests (external users).</span></span> <span data-ttu-id="7f54a-119">Si vous avez défini une stratégie DLP pour éviter cela, les messages avec des informations sensibles envoyés à des utilisateurs externes sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="7f54a-119">If you have a DLP policy defined to prevent this, messages with sensitive information that are sent to external users are deleted.</span></span> <span data-ttu-id="7f54a-120">Cela se produit automatiquement et en quelques secondes, en fonction de la configuration de votre stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="7f54a-120">This happens automatically, and within seconds, according to how your DLP policy is configured.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7f54a-121">La DLP pour Microsoft Teams bloque le contenu sensible lorsqu’il est partagé avec Microsoft Teams utilisateurs qui ont :</span><span class="sxs-lookup"><span data-stu-id="7f54a-121">DLP for Microsoft Teams blocks sensitive content when shared with Microsoft Teams users who have:</span></span><br/><span data-ttu-id="7f54a-122">- [accès invité dans](/MicrosoftTeams/guest-access) les équipes et les canaux ; ou</span><span class="sxs-lookup"><span data-stu-id="7f54a-122">- [guest access](/MicrosoftTeams/guest-access) in teams and channels; or</span></span><br/><span data-ttu-id="7f54a-123">- [accès externe](/MicrosoftTeams/manage-external-access) dans les réunions et les sessions de conversation.</span><span class="sxs-lookup"><span data-stu-id="7f54a-123">- [external access](/MicrosoftTeams/manage-external-access) in meetings and chat sessions.</span></span> <p><span data-ttu-id="7f54a-124">La DLP pour les sessions de conversation externe ne fonctionne que si l’expéditeur et le destinataire sont en mode Teams uniquement et utilisent la fédération Microsoft Teams [native.](/microsoftteams/manage-external-access)</span><span class="sxs-lookup"><span data-stu-id="7f54a-124">DLP for external chat sessions will only work if both the sender and the receiver are in Teams Only mode and using [Microsoft Teams native federation](/microsoftteams/manage-external-access).</span></span> <span data-ttu-id="7f54a-125">La prévention contre la Teams ne bloque pas les messages en cas [d’Skype Entreprise](/microsoftteams/teams-and-skypeforbusiness-coexistence-and-interoperability#interoperability-of-teams-and-skype-for-business) sessions de conversation fédérée non natives ou non natives.</span><span class="sxs-lookup"><span data-stu-id="7f54a-125">DLP for Teams does not block messages in [interop](/microsoftteams/teams-and-skypeforbusiness-coexistence-and-interoperability#interoperability-of-teams-and-skype-for-business) with Skype for Business or non-native federated chat sessions.</span></span>

- <span data-ttu-id="7f54a-126">**Exemple 2 : protection des informations sensibles dans les documents**.</span><span class="sxs-lookup"><span data-stu-id="7f54a-126">**Example 2: Protecting sensitive information in documents**.</span></span> <span data-ttu-id="7f54a-127">Supposons qu’une personne tente de partager un document avec des invités dans un canal Microsoft Teams ou une conversation instantanée, et que le document contient des informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="7f54a-127">Suppose that someone attempts to share a document with guests in a Microsoft Teams channel or chat, and the document contains sensitive information.</span></span> <span data-ttu-id="7f54a-128">Si vous avez défini une stratégie DLP pour éviter cela, le document ne s’ouvre pas pour ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7f54a-128">If you have a DLP policy defined to prevent this, the document won't open for those users.</span></span> <span data-ttu-id="7f54a-129">Notez que dans ce cas, votre stratégie DLP doit inclure des SharePoint et OneDrive pour que la protection soit en place.</span><span class="sxs-lookup"><span data-stu-id="7f54a-129">Note that in this case, your DLP policy must include SharePoint and OneDrive in order for protection to be in place.</span></span> <span data-ttu-id="7f54a-130">(Il s’agit d’un exemple de DLP pour SharePoint qui s’affiche dans Microsoft Teams et qui nécessite donc que les utilisateurs soient titulaires d’une licence pour Office 365 DLP (inclus dans Office 365 E3), mais ne nécessite pas que les utilisateurs soient titulaires d’une licence pour Conformité avancée Office 365.)</span><span class="sxs-lookup"><span data-stu-id="7f54a-130">(This is an example of DLP for SharePoint that shows up in Microsoft Teams, and therefore requires that users are licensed for Office 365 DLP (included in Office 365 E3), but does not require users to be licensed for Office 365 Advanced Compliance.)</span></span>

## <a name="policy-tips-help-educate-users"></a><span data-ttu-id="7f54a-131">Les conseils de stratégie aident à former les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7f54a-131">Policy tips help educate users</span></span>

<span data-ttu-id="7f54a-132">Comme dans [Exchange, Outlook, Outlook](data-loss-prevention-policies.md#policy-evaluation-in-exchange-online-outlook-and-outlook-on-the-web)sur le web, [SharePoint Online, les sites OneDrive Entreprise](data-loss-prevention-policies.md#policy-evaluation-in-onedrive-for-business-and-sharepoint-online-sites)et les clients de bureau [Office,](data-loss-prevention-policies.md#policy-evaluation-in-the-office-desktop-programs)des conseils de stratégie s’affichent lorsqu’une action entre en conflit avec une stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="7f54a-132">Similar to how DLP works in [Exchange, Outlook, Outlook on the web](data-loss-prevention-policies.md#policy-evaluation-in-exchange-online-outlook-and-outlook-on-the-web), [SharePoint Online, OneDrive for Business sites](data-loss-prevention-policies.md#policy-evaluation-in-onedrive-for-business-and-sharepoint-online-sites), and [Office desktop clients](data-loss-prevention-policies.md#policy-evaluation-in-the-office-desktop-programs), policy tips appear when an action conflicts with a DLP policy.</span></span> <span data-ttu-id="7f54a-133">Voici un exemple de conseil de stratégie :</span><span class="sxs-lookup"><span data-stu-id="7f54a-133">Here's an example of a policy tip:</span></span>

![Notification de message bloqué dans Teams](../media/dlp-teams-blockedmessage-notification.png)

<span data-ttu-id="7f54a-135">Dans ce cas, l’expéditeur a tenté de partager un numéro de sécurité sociale dans Microsoft Teams canal.</span><span class="sxs-lookup"><span data-stu-id="7f54a-135">In this case, the sender attempted to share a social security number in a Microsoft Teams channel.</span></span> <span data-ttu-id="7f54a-136">Le **lien Que puis-je faire ?** ouvre une boîte de dialogue qui fournit des options à l’expéditeur pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="7f54a-136">The **What can I do?** link opens a dialog box that provides options for the sender to resolve the issue.</span></span> <span data-ttu-id="7f54a-137">Notez que dans ce cas, l’expéditeur peut choisir de remplacer la stratégie ou d’avertir un administrateur de la réviser et de la résoudre.</span><span class="sxs-lookup"><span data-stu-id="7f54a-137">Notice that in this case, the sender can opt to override the policy, or notify an admin to review and resolve it.</span></span>

![Options pour résoudre le message bloqué](../media/dlp-teams-blockedmessage-possibleactions.png)

<span data-ttu-id="7f54a-139">Dans votre organisation, vous pouvez choisir d’autoriser les utilisateurs à remplacer une stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="7f54a-139">In your organization, you can choose to allow users to override a DLP policy.</span></span> <span data-ttu-id="7f54a-140">De plus, lorsque vous configurez vos stratégies DLP, vous pouvez utiliser les conseils de stratégie par défaut ou personnaliser les conseils de stratégie [pour](#to-customize-policy-tips) votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7f54a-140">And, when you configure your DLP policies, you can use the default policy tips, or [customize policy tips](#to-customize-policy-tips) for your organization.</span></span>

<span data-ttu-id="7f54a-141">Pour revenir à notre exemple, où un expéditeur a partagé un numéro de sécurité sociale dans un canal Teams, voici ce que le destinataire a vu :</span><span class="sxs-lookup"><span data-stu-id="7f54a-141">Returning to our example, where a sender shared a social security number in a Teams channel, here's what the recipient saw:</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="7f54a-142">![Message bloqué](../media/dlp-teams-blockedmessage-notification-to-user.png)</span><span class="sxs-lookup"><span data-stu-id="7f54a-142">![Message blocked](../media/dlp-teams-blockedmessage-notification-to-user.png)</span></span>

### <a name="to-customize-policy-tips"></a><span data-ttu-id="7f54a-143">Pour personnaliser les conseils de stratégie</span><span class="sxs-lookup"><span data-stu-id="7f54a-143">To customize policy tips</span></span>

<span data-ttu-id="7f54a-144">Pour effectuer cette tâche, vous devez avoir un rôle qui dispose des autorisations pour modifier les stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="7f54a-144">To perform this task, you must be assigned a role that has permissions to edit DLP policies.</span></span> <span data-ttu-id="7f54a-145">Pour en savoir plus, voir [Autorisations](data-loss-prevention-policies.md#permissions).</span><span class="sxs-lookup"><span data-stu-id="7f54a-145">To learn more, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

1. <span data-ttu-id="7f54a-146">Go to the Security & Compliance Center ( [https://protection.office.com](https://protection.office.com) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="7f54a-146">Go to the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)) and sign in.</span></span>

2. <span data-ttu-id="7f54a-147">Choisissez **la stratégie de protection contre la perte de**  >  **données.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-147">Choose **Data loss prevention** > **Policy**.</span></span>

3. <span data-ttu-id="7f54a-148">Select a policy, and next to **Policy settings**, choose **Edit**.</span><span class="sxs-lookup"><span data-stu-id="7f54a-148">Select a policy, and next to **Policy settings**, choose **Edit**.</span></span>

4. <span data-ttu-id="7f54a-149">Créez une règle ou modifiez une règle existante pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="7f54a-149">Either create a new rule, or edit an existing rule for the policy.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="7f54a-150">![Modification d’une règle pour une stratégie](../media/dlp-teams-editrule.png)</span><span class="sxs-lookup"><span data-stu-id="7f54a-150">![Editing a rule for a policy](../media/dlp-teams-editrule.png)</span></span>

5. <span data-ttu-id="7f54a-151">Sous **l’onglet Notifications de** l’utilisateur, **sélectionnez Personnaliser** le texte du message électronique et/ou personnaliser les options de texte du **conseil de stratégie.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-151">On the **User notifications** tab, select **Customize the email text** and/or **Customize the policy tip text** options.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="7f54a-152">![Personnaliser les notifications utilisateur et les conseils de stratégie](../media/dlp-teams-editrule-usernotifications.png)</span><span class="sxs-lookup"><span data-stu-id="7f54a-152">![Customize user notifications and policy tips](../media/dlp-teams-editrule-usernotifications.png)</span></span><br/>  

6. <span data-ttu-id="7f54a-153">Spécifiez le texte que vous souhaitez utiliser pour les notifications par courrier électronique et/ou les conseils de stratégie, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7f54a-153">Specify the text you want to use for email notifications and/or policy tips, and then choose **Save**.</span></span>

7. <span data-ttu-id="7f54a-154">Sous **l’onglet Paramètres de stratégie,** sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-154">On the **Policy settings** tab, choose **Save**.</span></span>

<span data-ttu-id="7f54a-155">Laissez environ une heure pour que vos modifications fonctionnent dans votre centre de données et se synchronisent avec les comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7f54a-155">Allow approximately one hour for your changes to work their way through your data center and sync to user accounts.</span></span>
 <!-- why are these syncing to user accounts? -->

## <a name="add-microsoft-teams-as-a-location-to-existing-dlp-policies"></a><span data-ttu-id="7f54a-156">Ajouter Microsoft Teams comme emplacement aux stratégies DLP existantes</span><span class="sxs-lookup"><span data-stu-id="7f54a-156">Add Microsoft Teams as a location to existing DLP policies</span></span>

<span data-ttu-id="7f54a-157">Pour effectuer cette tâche, vous devez avoir un rôle qui dispose des autorisations pour modifier les stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="7f54a-157">To perform this task, you must be assigned a role that has permissions to edit DLP policies.</span></span> <span data-ttu-id="7f54a-158">Pour en savoir plus, voir [Autorisations](data-loss-prevention-policies.md#permissions).</span><span class="sxs-lookup"><span data-stu-id="7f54a-158">To learn more, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

1. <span data-ttu-id="7f54a-159">Go to the Security & Compliance Center ( [https://protection.office.com](https://protection.office.com) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="7f54a-159">Go to the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)) and sign in.</span></span>

2. <span data-ttu-id="7f54a-160">Choisissez **la stratégie de protection contre la perte de**  >  **données.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-160">Choose **Data loss prevention** > **Policy**.</span></span>

3. <span data-ttu-id="7f54a-161">Sélectionnez une stratégie et regardez les valeurs sous **Emplacements.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-161">Select a policy, and look at the values under **Locations**.</span></span> <span data-ttu-id="7f54a-162">Si vous voyez des **Teams de conversation et de canal,** vous êtes tous ensemble.</span><span class="sxs-lookup"><span data-stu-id="7f54a-162">If you see **Teams chat and channel messages**, you're all set.</span></span> <span data-ttu-id="7f54a-163">Si ce n’est pas le cas, cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-163">If you don't, click **Edit**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="7f54a-164">![Emplacements pour la stratégie existante](../media/dlp-teams-editexistingpolicy.png)</span><span class="sxs-lookup"><span data-stu-id="7f54a-164">![Locations for existing policy](../media/dlp-teams-editexistingpolicy.png)</span></span>

4. <span data-ttu-id="7f54a-165">Dans la **colonne État,** activer la stratégie pour les messages **Teams de conversation et de canal.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-165">In the **Status** column, turn the policy on for **Teams chat and channel messages**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="7f54a-166">![DLP pour les Teams et les canaux](../media/dlp-teams-addteamschatschannels.png)</span><span class="sxs-lookup"><span data-stu-id="7f54a-166">![DLP for Teams chats and channels](../media/dlp-teams-addteamschatschannels.png)</span></span>

5. <span data-ttu-id="7f54a-167">Sous **l’onglet** Choisir des emplacements, conservez le paramètre par défaut de tous les comptes, ou sélectionnez **Choisir des emplacements spécifiques.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-167">On the **Choose locations** tab, keep the default setting of all accounts, or select **Let me choose specific locations**.</span></span> <span data-ttu-id="7f54a-168">Vous pouvez spécifier :</span><span class="sxs-lookup"><span data-stu-id="7f54a-168">You can specify:</span></span>

    1. <span data-ttu-id="7f54a-169">jusqu’à 1 000 comptes individuels à inclure ou à exclure</span><span class="sxs-lookup"><span data-stu-id="7f54a-169">up to 1000 individual accounts to include or exclude</span></span>
    1. <span data-ttu-id="7f54a-170">listes de distribution et groupes de sécurité à inclure ou à exclure;</span><span class="sxs-lookup"><span data-stu-id="7f54a-170">distribution lists and security groups to include or exclude.</span></span> 
    <!-- 1. the shared mailbox of a shared channel. **This is a public preview feature.**--> 
    
6. <span data-ttu-id="7f54a-171">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="7f54a-171">Then choose **Next**.</span></span>

7. <span data-ttu-id="7f54a-172">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7f54a-172">Click **Save**.</span></span>

<span data-ttu-id="7f54a-173">Laissez environ une heure pour que vos modifications fonctionnent dans votre centre de données et se synchronisent avec les comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7f54a-173">Allow approximately one hour for your changes to work their way through your data center and sync to user accounts.</span></span>
<!-- again, why user accounts? -->

## <a name="define-a-new-dlp-policy-for-microsoft-teams"></a><span data-ttu-id="7f54a-174">Définir une nouvelle stratégie DLP pour Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7f54a-174">Define a new DLP policy for Microsoft Teams</span></span>

<span data-ttu-id="7f54a-175">Pour effectuer cette tâche, vous devez avoir un rôle qui dispose des autorisations pour modifier les stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="7f54a-175">To perform this task, you must be assigned a role that has permissions to edit DLP policies.</span></span> <span data-ttu-id="7f54a-176">Pour en savoir plus, voir [Autorisations](data-loss-prevention-policies.md#permissions).</span><span class="sxs-lookup"><span data-stu-id="7f54a-176">To learn more, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

1. <span data-ttu-id="7f54a-177">Go to the Security & Compliance Center ( [https://protection.office.com](https://protection.office.com) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="7f54a-177">Go to the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)) and sign in.</span></span>

2. <span data-ttu-id="7f54a-178">Choisissez **stratégie de protection contre la perte**  >  **de**  >  **données + Créer une stratégie.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-178">Choose **Data loss prevention** > **Policy** > **+ Create a policy**.</span></span>

3. <span data-ttu-id="7f54a-179">Choisissez un [modèle,](data-loss-prevention-policies.md#dlp-policy-templates)puis choisissez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-179">Choose a [template](data-loss-prevention-policies.md#dlp-policy-templates), and then choose **Next**.</span></span>

    <span data-ttu-id="7f54a-180">Dans notre exemple, nous avons choisi le modèle de données d’informations d’identification personnelle des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="7f54a-180">In our example, we chose the U.S. Personally Identifiable Information Data template.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="7f54a-181">![Modèle de confidentialité pour la stratégie DLP](../media/dlp-teams-createnewpolicy-template.png)</span><span class="sxs-lookup"><span data-stu-id="7f54a-181">![Privacy template for DLP policy](../media/dlp-teams-createnewpolicy-template.png)</span></span><br/>

4. <span data-ttu-id="7f54a-182">Sous **l’onglet Nom de votre stratégie,** spécifiez un nom et une description pour la stratégie, puis choisissez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="7f54a-182">On the **Name your policy** tab, specify a name and description for the policy, and then choose **Next**.</span></span>

5. <span data-ttu-id="7f54a-183">Sous **l’onglet** Choisir des emplacements, conservez le paramètre par défaut de tous les comptes, ou sélectionnez **Choisir des emplacements spécifiques.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-183">On the **Choose locations** tab, keep the default setting of all accounts, or select **Let me choose specific locations**.</span></span> <span data-ttu-id="7f54a-184">Vous pouvez spécifier :</span><span class="sxs-lookup"><span data-stu-id="7f54a-184">You can specify:</span></span>

    1. <span data-ttu-id="7f54a-185">jusqu’à 1 000 comptes individuels à inclure ou à exclure</span><span class="sxs-lookup"><span data-stu-id="7f54a-185">up to 1000 individual accounts to include or exclude</span></span>
    1. <span data-ttu-id="7f54a-186">listes de distribution et groupes de sécurité à inclure ou à exclure;</span><span class="sxs-lookup"><span data-stu-id="7f54a-186">distribution lists and security groups to include or exclude.</span></span> <span data-ttu-id="7f54a-187">**Il s’agit d’une fonctionnalité de prévisualisation publique.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-187">**This is a public preview feature.**</span></span>
    <!-- 1. the shared mailbox of a shared channel. **This is a public preview feature.**-->  

    ![Emplacements de stratégie DLP](../media/dlp-teams-selectlocationsnewpolicy.png)

    > [!NOTE]
    > <span data-ttu-id="7f54a-189">Si vous souhaitez vous assurer que les documents qui contiennent des informations sensibles ne sont pas partagés de manière inappropriée dans Teams, assurez-vous que les **sites SharePoint** et les comptes OneDrive sont **allumés,** ainsi que les messages de conversation et de canal **Teams.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-189">If you want to make sure documents that contain sensitive information are not shared inappropriately in Teams, make sure **SharePoint sites** and **OneDrive accounts** are turned on, along with **Teams chat and channel messages**.</span></span>

6. <span data-ttu-id="7f54a-190">Sous **l’onglet Paramètres** de stratégie, sous Personnaliser le **type** de contenu que vous souhaitez protéger, conservez les paramètres simples par défaut, ou choisissez Utiliser les **paramètres** avancés, puis choisissez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="7f54a-190">On the **Policy settings** tab, under **Customize the type of content you want to protect**, keep the default simple settings, or choose **Use advanced settings**, and then choose **Next**.</span></span> <span data-ttu-id="7f54a-191">Si vous choisissez des paramètres avancés, vous pouvez créer ou modifier des règles pour votre stratégie.</span><span class="sxs-lookup"><span data-stu-id="7f54a-191">If you choose advanced settings, you can create or edit rules for your policy.</span></span> <span data-ttu-id="7f54a-192">(Pour obtenir de l’aide, voir [Paramètres simples et paramètres avancés.)](data-loss-prevention-policies.md#simple-settings-vs-advanced-settings)</span><span class="sxs-lookup"><span data-stu-id="7f54a-192">(To get help with this, see [Simple settings vs. advanced settings](data-loss-prevention-policies.md#simple-settings-vs-advanced-settings).)</span></span>

7.  <span data-ttu-id="7f54a-193">Sous **l’onglet Paramètres de stratégie,** sous Que voulez-vous faire si nous détectons des informations sensibles **?**, examinez les paramètres.</span><span class="sxs-lookup"><span data-stu-id="7f54a-193">On the **Policy settings** tab, under **What do you want to do if we detect sensitive info?**, review the settings.</span></span> <span data-ttu-id="7f54a-194">(C’est ici que vous pouvez choisir de conserver les conseils de stratégie par défaut et les [notifications par](use-notifications-and-policy-tips.md)courrier électronique, ou de les personnaliser.)</span><span class="sxs-lookup"><span data-stu-id="7f54a-194">(Here's where you can choose to keep default [policy tips and email notifications](use-notifications-and-policy-tips.md), or customize them.)</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="7f54a-195">![Paramètres de stratégie DLP avec conseils et notifications](../media/dlp-teams-policysettings-tipsemails.png)</span><span class="sxs-lookup"><span data-stu-id="7f54a-195">![DLP policy settings with tips and notifications](../media/dlp-teams-policysettings-tipsemails.png)</span></span>

    <span data-ttu-id="7f54a-196">Lorsque vous avez terminé de passer en revue ou de modifier les paramètres, choisissez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="7f54a-196">When you're finished reviewing or editing settings, choose **Next**.</span></span>

8. <span data-ttu-id="7f54a-197">Sous l’onglet **Paramètres** de stratégie, sous Voulez-vous activer la stratégie ou d’abord tester les éléments **?**, choisissez d’activer la [stratégie,](dlp-overview-plan-for-dlp.md#policy-deployment)de la tester en premier ou de la maintenir désactivée pour l’instant, puis choisissez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-197">On the **Policy settings** tab, under **Do you want to turn on the policy or test things out first?**, choose whether to turn the policy on, [test it first](dlp-overview-plan-for-dlp.md#policy-deployment), or keep it turned off for now, and then choose **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="7f54a-198">![Spécifier s’il faut activer la stratégie](../media/dlp-teams-policysettings-turnonnow.png)</span><span class="sxs-lookup"><span data-stu-id="7f54a-198">![Specify whether to turn the policy on](../media/dlp-teams-policysettings-turnonnow.png)</span></span>

9. <span data-ttu-id="7f54a-199">Sous **l’onglet Examiner vos paramètres,** examinez les paramètres de votre nouvelle stratégie.</span><span class="sxs-lookup"><span data-stu-id="7f54a-199">On the **Review your settings** tab, review the settings for your new policy.</span></span> <span data-ttu-id="7f54a-200">Sélectionnez **Modifier** pour apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="7f54a-200">Choose **Edit** to make changes.</span></span> <span data-ttu-id="7f54a-201">Lorsque vous avez terminé, choisissez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-201">When you're finished, choose **Create**.</span></span>

<span data-ttu-id="7f54a-202">Laissez environ une heure à votre nouvelle stratégie pour passer par votre centre de données et se synchroniser avec les comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7f54a-202">Allow approximately one hour for your new policy to work its way through your data center and sync to user accounts.</span></span>

## <a name="prevent-external-access-to-sensitive-documents"></a><span data-ttu-id="7f54a-203">Empêcher l'accès externe aux documents sensibles</span><span class="sxs-lookup"><span data-stu-id="7f54a-203">Prevent external access to sensitive documents</span></span>

<span data-ttu-id="7f54a-204">Pour vous assurer que SharePoint documents contenant des informations sensibles ne peuvent pas être accessibles par des invités externes à partir de SharePoint ou Teams par défaut, sélectionnez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7f54a-204">To ensure that SharePoint documents that contain sensitive information cannot be accessed by external guests either from SharePoint or Teams by default, select the following:</span></span>

- <span data-ttu-id="7f54a-205">Vous pouvez vous assurer que les documents sont protégés jusqu’à ce que DLP analyse et les marque comme étant sûrs à partager en marquant les nouveaux fichiers comme sensibles [par défaut.](/sharepoint/sensitive-by-default)</span><span class="sxs-lookup"><span data-stu-id="7f54a-205">You can ensure that documents are protected until DLP scans and marks them as safe to share by [marking new files as sensitive by default](/sharepoint/sensitive-by-default).</span></span>

- <span data-ttu-id="7f54a-206">Structure de stratégie DLP recommandée</span><span class="sxs-lookup"><span data-stu-id="7f54a-206">Recommended DLP policy structure</span></span>

    - <span data-ttu-id="7f54a-207">**Conditions**</span><span class="sxs-lookup"><span data-stu-id="7f54a-207">**Conditions**</span></span>
        - <span data-ttu-id="7f54a-208">Le contenu contient l’un de ces types d’informations sensibles : [Sélectionner tout ce qui s’applique]</span><span class="sxs-lookup"><span data-stu-id="7f54a-208">Content contains any of these sensitive information types: [Select all that applies]</span></span>
        
        - <span data-ttu-id="7f54a-209">Le contenu est partagé à partir Microsoft 365 avec des personnes extérieures à mon organisation</span><span class="sxs-lookup"><span data-stu-id="7f54a-209">Content is shared from Microsoft 365 with people outside my organization</span></span>
        
          > [!div class="mx-imgBorder"]
          > <span data-ttu-id="7f54a-210">![Conditions DLP pour détecter le partage externe de contenu sensible](../media/dlp-teams-external-sharing/external-condition.png)</span><span class="sxs-lookup"><span data-stu-id="7f54a-210">![DLP conditions to detect external sharing of sensitive content](../media/dlp-teams-external-sharing/external-condition.png)</span></span>

    - <span data-ttu-id="7f54a-211">**Actions**</span><span class="sxs-lookup"><span data-stu-id="7f54a-211">**Actions**</span></span>
        - <span data-ttu-id="7f54a-212">Restreindre l’accès au contenu pour utilisateurs externe</span><span class="sxs-lookup"><span data-stu-id="7f54a-212">Restrict access to the content for external users</span></span>
        
        - <span data-ttu-id="7f54a-213">Informer les utilisateurs à l’aide de courriers électroniques et de conseils de stratégie</span><span class="sxs-lookup"><span data-stu-id="7f54a-213">Notify users with email and policy tips</span></span>
        
        - <span data-ttu-id="7f54a-214">Envoyer des rapports d’incident à l’administrateur</span><span class="sxs-lookup"><span data-stu-id="7f54a-214">Send incident reports to the Administrator</span></span>
        
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="7f54a-215">![Action DLP pour bloquer le partage externe de contenu sensible](../media/dlp-teams-external-sharing/external-action.png)</span><span class="sxs-lookup"><span data-stu-id="7f54a-215">![DLP action to block external sharing of sensitive content](../media/dlp-teams-external-sharing/external-action.png)</span></span>

<span data-ttu-id="7f54a-216">Stratégie DLP en action lors de la tentative de partage d’un document dans SharePoint contenant des informations sensibles avec un invité externe :</span><span class="sxs-lookup"><span data-stu-id="7f54a-216">DLP policy in action when attempting to share a document in SharePoint that contains sensitive information with an external guest:</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="7f54a-217">![Partage externe bloqué](../media/dlp-teams-external-sharing/external-sharing-blocked.png)</span><span class="sxs-lookup"><span data-stu-id="7f54a-217">![External sharing blocked](../media/dlp-teams-external-sharing/external-sharing-blocked.png)</span></span>


<span data-ttu-id="7f54a-218">Stratégie DLP en action lorsque l’invité tente d’ouvrir un document Teams avec un bloc externe :</span><span class="sxs-lookup"><span data-stu-id="7f54a-218">DLP policy in action when guest attempts to open a document in Teams with block external:</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="7f54a-219">![Accès externe bloqué](../media/dlp-teams-external-sharing/external-access-blocked.png)</span><span class="sxs-lookup"><span data-stu-id="7f54a-219">![External access blocked](../media/dlp-teams-external-sharing/external-access-blocked.png)</span></span>

## <a name="related-articles"></a><span data-ttu-id="7f54a-220">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="7f54a-220">Related articles</span></span>

[<span data-ttu-id="7f54a-221">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="7f54a-221">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)

[<span data-ttu-id="7f54a-222">Envoi des notifications et affichage des conseils de stratégie pour les stratégies DLP</span><span class="sxs-lookup"><span data-stu-id="7f54a-222">Send email notifications and show policy tips for DLP policies</span></span>](use-notifications-and-policy-tips.md)
