---
title: Spécifier une boîte aux lettres pour les soumissions d’utilisateurs de messages de courrier indésirable et de hameçonnage
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à configurer une boîte aux lettres pour collecter le courrier indésirable et le courrier indésirable transmis par les utilisateurs.
ms.openlocfilehash: 458938105d03cb82dfa4e9a7824f8b026fddec5d
ms.sourcegitcommit: 89b2ad0793c68415f178b8792a9757b9448345a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2020
ms.locfileid: "47294752"
---
# <a name="specify-a-mailbox-for-user-submissions-of-spam-and-phishing-messages-in-exchange-online"></a><span data-ttu-id="21c17-103">Spécifier une boîte aux lettres pour les soumissions d’utilisateurs de messages de courrier indésirable et de hameçonnage dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="21c17-103">Specify a mailbox for user submissions of spam and phishing messages in Exchange Online</span></span>

<span data-ttu-id="21c17-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres Exchange Online, vous pouvez spécifier une boîte aux lettres pour recevoir les messages signalés comme malveillants ou non malveillants par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="21c17-104">In Microsoft 365 organizations with Exchange Online mailboxes, you can specify a mailbox to receive messages that users report as malicious or not malicious.</span></span> <span data-ttu-id="21c17-105">Lorsque les utilisateurs envoient des messages à l’aide des différentes options de création de rapports, vous pouvez utiliser cette boîte aux lettres pour intercepter des messages (Envoyer à la boîte aux lettres personnalisée uniquement) ou recevoir des copies de messages (Envoyer à la boîte aux lettres personnalisée et à Microsoft).</span><span class="sxs-lookup"><span data-stu-id="21c17-105">When users submit messages using the various reporting options, you can use this mailbox to intercept messages (send to the custom mailbox only) or receive copies of messages (send to the custom mailbox and Microsoft).</span></span> <span data-ttu-id="21c17-106">Cette fonctionnalité fonctionne avec les options de signalement de message suivantes :</span><span class="sxs-lookup"><span data-stu-id="21c17-106">This feature works with the following message reporting options:</span></span>

- [<span data-ttu-id="21c17-107">Complément de message de rapport</span><span class="sxs-lookup"><span data-stu-id="21c17-107">The Report Message add-in</span></span>](enable-the-report-message-add-in.md)

- <span data-ttu-id="21c17-108">[Création de rapports intégrée dans Outlook sur le Web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md) (anciennement appelé Outlook Web App)</span><span class="sxs-lookup"><span data-stu-id="21c17-108">[Built-in reporting in Outlook on the web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md) (formerly known as Outlook Web App)</span></span>

- [<span data-ttu-id="21c17-109">Création de rapports intégrés dans Outlook pour iOS et Android</span><span class="sxs-lookup"><span data-stu-id="21c17-109">Built-in reporting in Outlook for iOS and Android</span></span>](report-junk-email-and-phishing-scams-in-outlook-for-iOS-and-Android.md)

  > [!NOTE]
  > <span data-ttu-id="21c17-110">Si la création de rapports a été [désactivée dans Outlook sur le Web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md#disable-or-enable-junk-email-reporting-in-outlook-on-the-web), l’activation des soumissions d’utilisateurs ici remplacera ce paramètre et permettra aux utilisateurs de signaler à nouveau les messages dans Outlook sur le Web.</span><span class="sxs-lookup"><span data-stu-id="21c17-110">If reporting has been [disabled in Outlook on the web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md#disable-or-enable-junk-email-reporting-in-outlook-on-the-web), enabling user submissions here will override that setting and enable users to report messages in Outlook on the web again.</span></span>

<span data-ttu-id="21c17-111">Vous pouvez également configurer des outils de création de rapports de messages tiers pour transférer des messages vers la boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="21c17-111">You can also configure third-party message reporting tools to forward messages to the mailbox that you specify.</span></span>

<span data-ttu-id="21c17-112">La remise des messages signalés par l’utilisateur à une boîte aux lettres personnalisée au lieu de Microsoft permet à vos administrateurs de signaler des messages de façon sélective et manuelle à Microsoft à l’aide de la soumission de l' [administrateur](admin-submission.md).</span><span class="sxs-lookup"><span data-stu-id="21c17-112">Delivering user reported messages to a custom mailbox instead of directly to Microsoft allows your admins to selectively and manually report messages to Microsoft using [Admin submission](admin-submission.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="21c17-113">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="21c17-113">What do you need to know before you begin?</span></span>

- <span data-ttu-id="21c17-114">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="21c17-114">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="21c17-115">Pour accéder directement à la page **soumissions** de l’utilisateur, utilisez <https://protection.office.com/userSubmissionsReportMessage> .</span><span class="sxs-lookup"><span data-stu-id="21c17-115">To go directly to the **User submissions** page, use <https://protection.office.com/userSubmissionsReportMessage>.</span></span>

- <span data-ttu-id="21c17-116">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures. décrites dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="21c17-116">You need to be assigned permissions before you can do the procedures in this topic:</span></span>

  - <span data-ttu-id="21c17-117">Pour modifier la configuration des envois utilisateur, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="21c17-117">To modify the configuration for User submissions, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="21c17-118">**[Administrateur Exchange](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#exchange-administrator)** dans Azure ad, **gestion** de l’organisation ou **administrateur de sécurité** , et dans le [Centre de sécurité & conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="21c17-118">**[Exchange Administrator](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#exchange-administrator)** in Azure AD and **Organization Management** or **Security Administrator** and in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="21c17-119">**Gestion de l’organisation** ou **Gestion de l’hygiène** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="21c17-119">**Organization Management** or **Hygiene Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

  - <span data-ttu-id="21c17-120">Pour un accès en lecture seule aux soumissions des utilisateurs, vous devez être membre des deux groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="21c17-120">For read-only access to User submissions, you need to be a member of both of the following role groups:</span></span>

    - <span data-ttu-id="21c17-121">**Lecteur de sécurité** dans le [Centre de conformité et sécurité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="21c17-121">**Security Reader** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="21c17-122">**Gestion de l’organisation en affichage seul** dans[Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="21c17-122">**View-Only Organization Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

## <a name="use-the-security--compliance-center-to-configure-the-user-submissions-mailbox"></a><span data-ttu-id="21c17-123">Utiliser le centre de sécurité & conformité pour configurer la boîte aux lettres d’envoi des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="21c17-123">Use the Security & Compliance Center to configure the user submissions mailbox</span></span>

1. <span data-ttu-id="21c17-124">Dans le centre de sécurité & conformité, accédez à l’utilisateur de la stratégie de **gestion des menaces** \> **Policy** \> **User submissions**.</span><span class="sxs-lookup"><span data-stu-id="21c17-124">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **User submissions**.</span></span>

2. <span data-ttu-id="21c17-125">Dans la page **soumissions** de l’utilisateur qui s’affiche, sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="21c17-125">In the **User submissions** page that appears, select one of the following options:</span></span>

   <span data-ttu-id="21c17-126">a.</span><span class="sxs-lookup"><span data-stu-id="21c17-126">a.</span></span> <span data-ttu-id="21c17-127">**Activer la fonctionnalité de rapport de message pour Outlook (recommandé)**: sélectionnez cette option si vous utilisez le complément de rapport de message ou le complément de création de rapports dans Outlook sur le Web, puis configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="21c17-127">**Enable the Report Message feature for Outlook (Recommended)**: Select this option if you use the Report Message add-in or the built-in reporting in Outlook on the web, and then configure the following settings:</span></span>

      - <span data-ttu-id="21c17-128">**Personnaliser le message de confirmation de l’utilisateur final**: cliquez sur ce lien.</span><span class="sxs-lookup"><span data-stu-id="21c17-128">**Customize the end-user confirmation message**: Click this link.</span></span> <span data-ttu-id="21c17-129">Dans la fenêtre mobile **personnaliser le message de confirmation** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="21c17-129">In the **Customize confirmation message** flyout that appears, configure the following settings:</span></span>

      - <span data-ttu-id="21c17-130">**Avant l’envoi**: dans les zones de message de **titre** et de **confirmation** , entrez le texte descriptif que les utilisateurs voient avant de signaler un message à l’aide du complément de message de rapport.</span><span class="sxs-lookup"><span data-stu-id="21c17-130">**Before submission**: In the **Title** and **Confirmation message** boxes, enter the descriptive text that users see before they report a message using the Report Message add-in.</span></span> <span data-ttu-id="21c17-131">Vous pouvez utiliser la variable% type% pour inclure le type d’envoi (courrier indésirable, pas courrier indésirable, hameçonnage, etc.).</span><span class="sxs-lookup"><span data-stu-id="21c17-131">You can use the variable %type% to include the submission type (junk, not junk, phish, etc.).</span></span>

        <span data-ttu-id="21c17-132">Comme indiqué, si vous sélectionnez une option qui envoie les messages signalés à Microsoft, le texte suivant est également ajouté à la notification :</span><span class="sxs-lookup"><span data-stu-id="21c17-132">As noted, if you select an option that sends the reported messages to Microsoft, the following text is also added to the notification:</span></span>

        > <span data-ttu-id="21c17-133">Votre courrier électronique sera envoyé tel quel à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="21c17-133">Your email will be submitted as-is to Microsoft for analysis.</span></span> <span data-ttu-id="21c17-134">Certains courriers électroniques peuvent contenir des informations personnelles ou sensibles.</span><span class="sxs-lookup"><span data-stu-id="21c17-134">Some emails might contain personal or sensitive information.</span></span>

      - <span data-ttu-id="21c17-135">**Après l’envoi**: cliquez sur ![ développer ](../../media/scc-expand-icon.png) .</span><span class="sxs-lookup"><span data-stu-id="21c17-135">**After submission**: Click ![Expand icon](../../media/scc-expand-icon.png).</span></span> <span data-ttu-id="21c17-136">Dans les zones de **message** de **titre** et de confirmation, entrez le texte descriptif que les utilisateurs voient lorsqu’ils signalent un message à l’aide du complément de message de rapport.</span><span class="sxs-lookup"><span data-stu-id="21c17-136">In the **Title** and **Confirmation message** boxes, enter the descriptive text that users see after they report a message using the Report Message add-in.</span></span> <span data-ttu-id="21c17-137">Vous pouvez utiliser la variable% type% pour inclure le type d’envoi.</span><span class="sxs-lookup"><span data-stu-id="21c17-137">You can use the variable %type% to include the submission type.</span></span>

      <span data-ttu-id="21c17-138">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="21c17-138">When you're finished, click **Save**.</span></span> <span data-ttu-id="21c17-139">Pour effacer ces valeurs, cliquez sur **restaurer** sur la page **soumissions** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="21c17-139">To clear these values, click **Restore** back on the **User submissions** page.</span></span>

      - <span data-ttu-id="21c17-140">**Envoyer les messages signalés à**: effectuez l’une des sélections suivantes :</span><span class="sxs-lookup"><span data-stu-id="21c17-140">**Send the reported messages to**: Make one of the following selections:</span></span>

        - <span data-ttu-id="21c17-141">**Microsoft (recommandé)**: la boîte aux lettres d’envoi n’est pas utilisée (tous les messages signalés sont transmis à Microsoft).</span><span class="sxs-lookup"><span data-stu-id="21c17-141">**Microsoft (Recommended)**: The user submissions mailbox isn't used (all reported messages go to Microsoft).</span></span>

        - <span data-ttu-id="21c17-142">**Microsoft et une boîte aux lettres personnalisée**: dans la zone qui s’affiche, entrez l’adresse de messagerie d’une boîte aux lettres Exchange Online existante.</span><span class="sxs-lookup"><span data-stu-id="21c17-142">**Microsoft and a custom mailbox**: In the box that appears, enter the email address of an existing Exchange Online mailbox.</span></span> <span data-ttu-id="21c17-143">Les groupes de distribution ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="21c17-143">Distribution groups are not allowed.</span></span> <span data-ttu-id="21c17-144">Les soumissions des utilisateurs seront dirigées vers Microsoft pour analyse et vers la boîte aux lettres personnalisée que votre administrateur ou votre équipe chargée des opérations de sécurité doit analyser.</span><span class="sxs-lookup"><span data-stu-id="21c17-144">User submissions will go to both Microsoft for analysis and to the custom mailbox for your admin or security operations team to analyze.</span></span>

        - <span data-ttu-id="21c17-145">**Boîte aux lettres personnalisée**: dans la zone qui s’affiche, entrez l’adresse de messagerie d’une boîte aux lettres Exchange Online existante.</span><span class="sxs-lookup"><span data-stu-id="21c17-145">**Custom mailbox**: In the box that appears, enter the email address of an existing Exchange Online mailbox.</span></span> <span data-ttu-id="21c17-146">Les groupes de distribution ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="21c17-146">Distribution groups are not allowed.</span></span> <span data-ttu-id="21c17-147">Utilisez cette option si vous souhaitez que le message soit uniquement destiné aux administrateurs ou à l’équipe des opérations de sécurité pour analyse.</span><span class="sxs-lookup"><span data-stu-id="21c17-147">Use this option if you want the message to only go to an admin or the security operations team for analysis first.</span></span> <span data-ttu-id="21c17-148">Les messages ne sont pas envoyés à Microsoft à moins que l’administrateur ne le transfère eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="21c17-148">Messages will not go to Microsoft unless the admin forwards it themselves.</span></span>

        > [!NOTE]
        > <span data-ttu-id="21c17-149">Les organisations gouvernementales américaines (GCC, GCC-H et DoD) ne peuvent configurer que la **boîte aux lettres personnalisée**.</span><span class="sxs-lookup"><span data-stu-id="21c17-149">U.S. Government organizations (GCC, GCC-H, and DoD) can only configure **Custom mailbox**.</span></span> <span data-ttu-id="21c17-150">Les deux autres options sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="21c17-150">The other two options are disabled.</span></span> 

      <span data-ttu-id="21c17-151">Lorsque vous avez terminé, cliquez sur **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="21c17-151">When you're finished, click **Confirm**.</span></span>

      > [!CAUTION]
      > <span data-ttu-id="21c17-152">Si vous avez [désactivé la création de rapports de courrier indésirable dans Outlook sur le Web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md#disable-or-enable-junk-email-reporting-in-outlook-on-the-web) à l’aide des stratégies de boîte aux lettres Outlook sur le Web, mais que vous configurez l’un des paramètres précédents pour signaler les messages à Microsoft, les utilisateurs pourront signaler les messages à Microsoft dans Outlook sur le Web à l’aide du complément Report message.</span><span class="sxs-lookup"><span data-stu-id="21c17-152">If you have [disabled junk email reporting in Outlook on the web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md#disable-or-enable-junk-email-reporting-in-outlook-on-the-web) using Outlook on the web mailbox policies, but you configure either of the previous settings to report messages to Microsoft, users will be able to report messages to Microsoft in Outlook on the web using the Report Message add-in.</span></span>

   - <span data-ttu-id="21c17-153">**Désactiver la fonctionnalité de rapport de message pour Outlook**: sélectionnez cette option si vous utilisez des outils de création de rapports tiers à la place du complément de rapport de message ou de la création de rapports intégrée dans Outlook sur le Web, puis configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="21c17-153">**Disable the Report Message feature for Outlook**: Select this option if you use third-party reporting tools instead of the Report Message add-in or the built-in reporting in Outlook on the web, and then configure the following settings:</span></span>

      <span data-ttu-id="21c17-154">Sélectionnez **utiliser cette boîte aux lettres personnalisée pour recevoir des envois signalés par l’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="21c17-154">Select **Use this custom mailbox to receive user reported submissions**.</span></span> <span data-ttu-id="21c17-155">Dans la zone qui s’affiche, entrez l’adresse de messagerie d’une boîte aux lettres existante qui se trouve déjà dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="21c17-155">In the box that appears, enter the email address of an existing mailbox that is already in Office 365.</span></span> <span data-ttu-id="21c17-156">Il doit s’agir d’une boîte aux lettres existante dans Exchange Online qui peut recevoir des courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="21c17-156">This has to be an existing mailbox in Exchange Online that can receive email.</span></span>

      <span data-ttu-id="21c17-157">Lorsque vous avez terminé, cliquez sur **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="21c17-157">When you're finished, click **Confirm**.</span></span>

## <a name="message-submission-format"></a><span data-ttu-id="21c17-158">Format de dépôt des messages</span><span class="sxs-lookup"><span data-stu-id="21c17-158">Message submission format</span></span>

<span data-ttu-id="21c17-159">Les messages envoyés à des boîtes aux lettres personnalisées doivent suivre un format de message d’envoi spécifique.</span><span class="sxs-lookup"><span data-stu-id="21c17-159">Messages sent to custom mailboxes need to follow a specific submission mail format.</span></span> <span data-ttu-id="21c17-160">L’objet (titre de l’enveloppe) de l’envoi doit être au format suivant :</span><span class="sxs-lookup"><span data-stu-id="21c17-160">The Subject (Envelope Title) of the submission should be in this format:</span></span>

`SafetyAPIAction|NetworkMessageId|SenderIp|FromAddress|(Message Subject)`

<span data-ttu-id="21c17-161">SafetyAPIAction est l’une des valeurs entières suivantes :</span><span class="sxs-lookup"><span data-stu-id="21c17-161">were SafetyAPIAction is one of the following integer values:</span></span>

- <span data-ttu-id="21c17-162">1 : courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="21c17-162">1: Junk</span></span>
- <span data-ttu-id="21c17-163">2 : NotJunk</span><span class="sxs-lookup"><span data-stu-id="21c17-163">2: NotJunk</span></span>
- <span data-ttu-id="21c17-164">3 : hameçonnage</span><span class="sxs-lookup"><span data-stu-id="21c17-164">3: Phish</span></span>

<span data-ttu-id="21c17-165">Dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="21c17-165">In the following example:</span></span>

- <span data-ttu-id="21c17-166">Le message est signalé comme hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="21c17-166">The message is being reported as Phish.</span></span>
- <span data-ttu-id="21c17-167">L’ID de message réseau est 49871234-6dc6-43e8-ABCD-08d797f20abe.</span><span class="sxs-lookup"><span data-stu-id="21c17-167">The Network Message ID is 49871234-6dc6-43e8-abcd-08d797f20abe.</span></span>
- <span data-ttu-id="21c17-168">L’adresse IP de l’expéditeur est 167.220.232.101.</span><span class="sxs-lookup"><span data-stu-id="21c17-168">The Sender IP is 167.220.232.101.</span></span>
- <span data-ttu-id="21c17-169">L’adresse de l’adresse est test@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="21c17-169">The From address is test@contoso.com.</span></span>
- <span data-ttu-id="21c17-170">La ligne d’objet du message est « tester la soumission de hameçonnage »</span><span class="sxs-lookup"><span data-stu-id="21c17-170">The message's subject line is "test phish submission"</span></span>

`3|49871234-6dc6-43e8-abcd-08d797f20abe|167.220.232.101|test@contoso.com|(test phish submission)`

<span data-ttu-id="21c17-171">Les messages qui ne suivent pas ce format ne s’afficheront pas correctement dans le portail des dépôts.</span><span class="sxs-lookup"><span data-stu-id="21c17-171">Messages that do not follow this format will not display properly in the Submissions portal.</span></span>
