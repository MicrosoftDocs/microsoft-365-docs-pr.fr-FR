---
title: Envoi manuel de messages à Microsoft pour analyse
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: dad30e2f-93fe-4d21-9a36-21c87ced85c1
ms.collection:
- M365-security-compliance
description: 'Vous et vos utilisateurs pouvez soumettre des messages indésirables faux positifs et faux positifs à Microsoft pour analyse. '
ms.openlocfilehash: f6dbd808fac54ae273c21773bf8caeabce09b7fb
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43631240"
---
# <a name="manually-submit-messages-to-microsoft-for-analysis"></a><span data-ttu-id="e6adf-103">Envoi manuel de messages à Microsoft pour analyse</span><span class="sxs-lookup"><span data-stu-id="e6adf-103">Manually submit messages to Microsoft for analysis</span></span>

> [!NOTE]
> <span data-ttu-id="e6adf-104">Si vous êtes administrateur d’une organisation Microsoft 365 avec des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail d’envoi du centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="e6adf-104">If you're an admin in an Microsoft 365 organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="e6adf-105">Pour plus d’informations, consultez la rubrique [utiliser la soumission de l’administrateur pour envoyer des courriers indésirables, des hameçons, des URL et des fichiers à Microsoft](admin-submission.md).</span><span class="sxs-lookup"><span data-stu-id="e6adf-105">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

<span data-ttu-id="e6adf-106">Il peut être frustrant lorsque les utilisateurs de votre organisation reçoivent des courriers indésirables (spam) ou des messages de hameçonnage dans leur boîte de réception, ou s’ils ne reçoivent pas de message électronique légitime, car il est marqué comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="e6adf-106">It can be frustrating when users in your organization receive junk messages (spam) or phishing messages in their Inbox, or if they don't receive a legitimate email message because it's marked as junk.</span></span> <span data-ttu-id="e6adf-107">Nous ajustons constamment les filtres de courrier indésirable pour qu’ils soient plus précis.</span><span class="sxs-lookup"><span data-stu-id="e6adf-107">We're constantly fine-tuning our spam filters to be more accurate.</span></span>

<span data-ttu-id="e6adf-108">Vous et vos utilisateurs pouvez aider ce processus en soumettant des faux positifs (courrier électronique marqué comme incorrect), des faux négatifs (courrier incorrect) et des messages de hameçonnage à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="e6adf-108">You and your users can help this process by submitting false positives (good email marked as bad), false negatives (bad mail allowed) and phishing messages to Microsoft for analysis.</span></span>

> [!NOTE]
> <span data-ttu-id="e6adf-109">En raison du volume élevé des envois que nous recevons, il se peut que nous ne parvenons pas à répondre à toutes les demandes d’analyse.</span><span class="sxs-lookup"><span data-stu-id="e6adf-109">Because of the high volume of submissions that we receive, we may not be able to answer all requests for analysis.</span></span>

## <a name="submit-false-negatives-to-microsoft"></a><span data-ttu-id="e6adf-110">Soumettre des faux négatifs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="e6adf-110">Submit false negatives to Microsoft</span></span>

> [!TIP]
> <span data-ttu-id="e6adf-111">Au lieu d’utiliser les procédures suivantes pour signaler les faux négatifs, les utilisateurs dans Outlook et Outlook sur le Web (anciennement appelé Outlook Web App) peuvent utiliser le complément de message de rapport pour Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="e6adf-111">Instead of using the following procedures to report false negatives, users in Outlook and Outlook on the web (formerly known as Outlook Web App) can use the Report Message Add-in for Microsoft Outlook.</span></span> <span data-ttu-id="e6adf-112">Pour plus d’informations sur l’installation et l’utilisation de cet outil, voir [activer le complément de message de rapport](enable-the-report-message-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="e6adf-112">For information about how to install and use this tool, see [Enable the Report Message add-in](enable-the-report-message-add-in.md).</span></span>

<span data-ttu-id="e6adf-113">Si vous recevez un message transmis par le biais du filtrage du courrier indésirable qui aurait dû être identifié comme courrier indésirable ou hameçonnage, vous pouvez envoyer le message aux équipes analyse du courrier indésirable et Microsoft Phishing Analysis, selon le cas.</span><span class="sxs-lookup"><span data-stu-id="e6adf-113">If you receive a message that passed through spam filtering that should have been identified as spam or phishing, you can submit the message to the Microsoft Spam Analysis and Microsoft Phishing Analysis teams as appropriate.</span></span> <span data-ttu-id="e6adf-114">Les analystes examineront le message et l’ajouteront aux filtres à l’échelle du service s’il répond aux critères de classification.</span><span class="sxs-lookup"><span data-stu-id="e6adf-114">The analysts will review the message and add it to the service-wide filters if it meets the classification criteria.</span></span>

1. <span data-ttu-id="e6adf-115">Créez un message électronique vide avec l’un des destinataires suivants :</span><span class="sxs-lookup"><span data-stu-id="e6adf-115">Create a new, blank email message with the one of the following recipients:</span></span>

   - <span data-ttu-id="e6adf-116">**Courrier indésirable**:`junk@office365.microsoft.com`</span><span class="sxs-lookup"><span data-stu-id="e6adf-116">**Junk**: `junk@office365.microsoft.com`</span></span>

   - <span data-ttu-id="e6adf-117">**Hameçonnage**:`phish@office365.microsoft.com`</span><span class="sxs-lookup"><span data-stu-id="e6adf-117">**Phishing**: `phish@office365.microsoft.com`</span></span>

2. <span data-ttu-id="e6adf-118">Faites glisser et déposez le message de courrier indésirable dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="e6adf-118">Drag and drop the junk or phishing message into the new message.</span></span> <span data-ttu-id="e6adf-119">Cette opération permet d’enregistrer le message de courrier indésirable ou de hameçonnage en tant que pièce jointe dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="e6adf-119">This will save the junk or phishing message as an attachment in the new message.</span></span> <span data-ttu-id="e6adf-120">Ne copiez pas et ne collez pas le contenu du message ou transférez le message (nous avons besoin du message d’origine pour pouvoir inspecter les en-têtes des messages).</span><span class="sxs-lookup"><span data-stu-id="e6adf-120">Don't copy and paste the content of the message or forward the message (we need the original message so we can inspect the message headers).</span></span>

   > [!NOTE]
   > <ul><li><span data-ttu-id="e6adf-121">Vous pouvez joindre plusieurs messages dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="e6adf-121">You can attach multiple messages in the new message.</span></span> <span data-ttu-id="e6adf-122">Assurez-vous que tous les messages sont du même type : les messages de hameçonnage ou les messages électroniques de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="e6adf-122">Make sure that all the messages are the same type: either phishing scam messages or junk email messages.</span></span></li><li><span data-ttu-id="e6adf-123">Laissez le corps du message vide.</span><span class="sxs-lookup"><span data-stu-id="e6adf-123">Leave the body of the new message empty.</span></span></li><li><span data-ttu-id="e6adf-124">Utilisez les formats. MSG (format Outlook par défaut) ou. eml (Outlook sur le format Web par défaut) pour les messages joints.</span><span class="sxs-lookup"><span data-stu-id="e6adf-124">Use either .msg (default Outlook format) or .eml (default Outlook on the Web format) formats for the attached messages.</span></span></li></ul>

3. <span data-ttu-id="e6adf-125">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="e6adf-125">When you're finished, click **Send**.</span></span>

> [!TIP]
> <span data-ttu-id="e6adf-126">Les administrateurs disposent de différentes manières de bloquer des messages spécifiques identifiés comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="e6adf-126">Admins have several different ways to block specific messages that are being misidentified as spam.</span></span> <span data-ttu-id="e6adf-127">Pour plus d’informations, consultez la rubrique [créer des listes d’expéditeurs bloqués dans Office 365](create-block-sender-lists-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="e6adf-127">For details, see [Create blocked sender lists in Office 365](create-block-sender-lists-in-office-365.md).</span></span>

## <a name="submit-false-positives-to-microsoft"></a><span data-ttu-id="e6adf-128">Soumettre des faux positifs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="e6adf-128">Submit false positives to Microsoft</span></span>

> [!TIP]
> <span data-ttu-id="e6adf-129">Au lieu d’utiliser les procédures suivantes pour signaler les faux positifs, les utilisateurs dans Outlook et Outlook sur le Web peuvent utiliser le complément de message de rapport pour Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="e6adf-129">Instead of using the following procedures to report false positives, users in Outlook and Outlook on the web can use the Report Message Add-in for Microsoft Outlook.</span></span> <span data-ttu-id="e6adf-130">Pour plus d’informations sur l’installation et l’utilisation de cet outil, voir [activer le complément de message de rapport](enable-the-report-message-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="e6adf-130">For information about how to install and use this tool, see [Enable the Report Message add-in](enable-the-report-message-add-in.md).</span></span>

<span data-ttu-id="e6adf-131">Si un message a été identifié de manière incorrecte comme courrier indésirable, vous pouvez envoyer le message à l’équipe d’analyse du courrier indésirable de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e6adf-131">If a message was incorrectly identified as spam, you can submit the message to the Microsoft Spam Analysis Team.</span></span> <span data-ttu-id="e6adf-132">Les analystes évaluent le message et (en fonction des résultats de l’analyse) les filtres à l’échelle du service peuvent être ajustés pour autoriser le message.</span><span class="sxs-lookup"><span data-stu-id="e6adf-132">The analysts will evaluate the message, and (depending on the results of the analysis) the service-wide filters can be adjusted to allow the message through.</span></span>

1. <span data-ttu-id="e6adf-133">Créez un message électronique vide avec `not_junk@office365.microsoft.com` comme destinataire :</span><span class="sxs-lookup"><span data-stu-id="e6adf-133">Create a new, blank email message with `not_junk@office365.microsoft.com` as the recipient:</span></span>

2. <span data-ttu-id="e6adf-134">Faites glisser et déposez le message qui a été identifié dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="e6adf-134">Drag and drop the misidentified message into the new message.</span></span> <span data-ttu-id="e6adf-135">Cette opération permet d’enregistrer le message identifié de manière indéterminée en tant que pièce jointe dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="e6adf-135">This will save the misidentified message as an attachment in the new message.</span></span> <span data-ttu-id="e6adf-136">Ne copiez pas et ne collez pas le contenu du message ou transférez le message (nous avons besoin du message d’origine pour pouvoir inspecter les en-têtes des messages).</span><span class="sxs-lookup"><span data-stu-id="e6adf-136">Don't copy and paste the content of the message or forward the message (we need the original message so we can inspect the message headers).</span></span>

   > [!NOTE]
   > <ul><li><span data-ttu-id="e6adf-137">Vous pouvez joindre plusieurs messages dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="e6adf-137">You can attach multiple messages in the new message.</span></span> <span data-ttu-id="e6adf-138">Assurez-vous que tous les messages sont du même type : les messages de hameçonnage ou les messages électroniques de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="e6adf-138">Make sure that all the messages are the same type: either phishing messages or junk email messages.</span></span></li><li><span data-ttu-id="e6adf-139">Laissez le corps du message vide.</span><span class="sxs-lookup"><span data-stu-id="e6adf-139">Leave the body of the new message empty.</span></span></li><li><span data-ttu-id="e6adf-140">Utilisez les formats. MSG (format Outlook par défaut) ou. eml (Outlook sur le format Web par défaut) pour les messages joints.</span><span class="sxs-lookup"><span data-stu-id="e6adf-140">Use either .msg (default Outlook format) or .eml (default Outlook on the Web format) formats for the attached messages.</span></span></li></ul>

3. <span data-ttu-id="e6adf-141">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="e6adf-141">When you're finished, click **Send**.</span></span>

> [!TIP]
> <span data-ttu-id="e6adf-142">Les administrateurs disposent de différentes manières d’autoriser des messages spécifiques à ignorer le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="e6adf-142">Admins have several different ways to allow specific messages to skip spam filtering.</span></span> <span data-ttu-id="e6adf-143">Pour plus d’informations, consultez la rubrique [créer des listes d’expéditeurs approuvés dans Office 365](create-safe-sender-lists-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="e6adf-143">For details, see [Create safe sender lists in Office 365](create-safe-sender-lists-in-office-365.md).</span></span>

## <a name="create-a-mail-flow-rule-to-receive-copies-of-messages-that-are-reported-to-microsoft"></a><span data-ttu-id="e6adf-144">Créer une règle de flux de messagerie pour recevoir des copies des messages signalés à Microsoft</span><span class="sxs-lookup"><span data-stu-id="e6adf-144">Create a mail flow rule to receive copies of messages that are reported to Microsoft</span></span>

<span data-ttu-id="e6adf-145">Vous pouvez créer une règle de flux de messagerie (également appelée règle de transport) qui recherche les messages électroniques envoyés à Microsoft à l’aide des méthodes décrites dans cette rubrique, et vous pouvez configurer les destinataires CCI de sorte qu’ils reçoivent des copies de ces messages signalés.</span><span class="sxs-lookup"><span data-stu-id="e6adf-145">You can create a mail flow rule (also known as a transport rule) that looks for email messages that are reported to Microsoft by using the methods described in this topic, and you can configure Bcc recipients to receive copies of these reported messages.</span></span>

<span data-ttu-id="e6adf-146">Vous pouvez créer la règle de flux de messagerie dans le centre d’administration Exchange et PowerShell (Exchange Online PowerShell pour les clients Microsoft 365 ; Exchange Online Protection PowerShell pour les clients EOP autonomes).</span><span class="sxs-lookup"><span data-stu-id="e6adf-146">You can create the mail flow rule in the Exchange admin center (EAC) and PowerShell (Exchange Online PowerShell for Microsoft 365 customers; Exchange Online Protection PowerShell for standalone EOP customers).</span></span>

### <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="e6adf-147">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="e6adf-147">What do you need to know before you begin?</span></span>

- <span data-ttu-id="e6adf-148">Pour pouvoir effectuer ces procédures, vous devez disposer d’autorisations dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="e6adf-148">You need to be assigned permissions in Exchange Online before you can do these procedures.</span></span> <span data-ttu-id="e6adf-149">Plus précisément, vous devez disposer du rôle **de règles de transport** , qui est affecté aux rôles de gestion de l' **organisation**, de gestion de **la conformité**et de **gestion des enregistrements** par défaut.</span><span class="sxs-lookup"><span data-stu-id="e6adf-149">Specifically, you need to be assigned the **Transport Rules** role, which is assigned to the **Organization Management**, **Compliance Management**, and **Records Management** roles by default.</span></span> <span data-ttu-id="e6adf-150">Pour plus d’informations, voir [Gérer les groupes de rôles dans Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span><span class="sxs-lookup"><span data-stu-id="e6adf-150">For more information, see [Manage role groups in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span></span>

- <span data-ttu-id="e6adf-151">Pour ouvrir le centre d’administration Exchange dans Exchange Online, consultez la rubrique [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center).</span><span class="sxs-lookup"><span data-stu-id="e6adf-151">To open the EAC in Exchange Online, see [Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center).</span></span>

- <span data-ttu-id="e6adf-152">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="e6adf-152">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="e6adf-153">Pour vous connecter à un service Exchange Online Protection autonome, voir [Se connecter à PowerShell d’Exchange Online Protection](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="e6adf-153">To connect to standalone Exchange Online Protection PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="e6adf-154">Pour plus d’informations sur les règles de flux de messagerie dans Exchange Online et dans la version autonome d’EOP, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6adf-154">For more information about mail flow rules in Exchange Online and standalone EOP, see the following topics:</span></span>

  - [<span data-ttu-id="e6adf-155">Règles de flux de messagerie (règles de transport) dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="e6adf-155">Mail flow rules (transport rules) in Exchange Online</span></span>](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)

  - [<span data-ttu-id="e6adf-156">Conditions de règle de flux de messagerie et exceptions (prédicats) dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="e6adf-156">Mail flow rule conditions and exceptions (predicates) in Exchange Online</span></span>](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions)

  - [<span data-ttu-id="e6adf-157">Actions de règle de flux de messagerie dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="e6adf-157">Mail flow rule actions in Exchange Online</span></span>](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions)

### <a name="use-the-eac-to-create-a-mail-flow-rule-to-receive-copies-of-reported-messages"></a><span data-ttu-id="e6adf-158">Utiliser le centre d’administration Exchange pour créer une règle de flux de messagerie pour recevoir des copies des messages signalés</span><span class="sxs-lookup"><span data-stu-id="e6adf-158">Use the EAC to create a mail flow rule to receive copies of reported messages</span></span>

1. <span data-ttu-id="e6adf-159">Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="e6adf-159">In the EAC, go to **Mail flow** \> **Rules**.</span></span>

2. <span data-ttu-id="e6adf-160">Cliquez sur **Ajouter** ![une](../../media/ITPro-EAC-AddIcon.png) icône Ajouter, puis sélectionnez **créer une nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="e6adf-160">Click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png) and then select **Create a new rule**.</span></span>

3. <span data-ttu-id="e6adf-161">Dans la page **Nouvelle règle** qui s'ouvre, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e6adf-161">In the **New rule** page that opens, configure the following settings:</span></span>

   - <span data-ttu-id="e6adf-162">**Nom**: entrez un nom unique et descriptif pour la règle.</span><span class="sxs-lookup"><span data-stu-id="e6adf-162">**Name**: Enter a unique, descriptive name for the rule.</span></span> <span data-ttu-id="e6adf-163">Par exemple, les messages CCI signalés à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e6adf-163">For example, Bcc Messages Reported to Microsoft.</span></span>

   - <span data-ttu-id="e6adf-164">Cliquez sur **Autres options**.</span><span class="sxs-lookup"><span data-stu-id="e6adf-164">Click **More Options**.</span></span>

   - <span data-ttu-id="e6adf-165">**Appliquer cette règle si**: sélectionnez **l’adresse du destinataire** \> **contient l’un des mots**suivants : dans la boîte de dialogue **spécifier des mots ou des expressions** qui s’affiche, entrez l’une des valeurs suivantes, puis cliquez sur **Ajouter** ![une icône](../../media/ITPro-EAC-AddIcon.png)et répétez l’opération jusqu’à ce que vous ayez entré toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="e6adf-165">**Apply this rule if**: Select **The recipient** \> **address includes any of these words**: In the **Specify words or phrases** dialog that appears, enter one of the following values, click **Add** ![Add Icon](../../media/ITPro-EAC-AddIcon.png), and repeat until you've entered all the values.</span></span>

     - `junk@office365.microsoft.com`
     - `abuse@messaging.microsoft.com`
     - `phish@office365.microsoft.com`
     - `false_positive@messaging.microsoft.com`

     <span data-ttu-id="e6adf-166">Pour modifier une entrée, sélectionnez-la et **Edit** ![cliquez sur modifier](../../media/ITPro-EAC-EditIcon.png)l’icône modifier.</span><span class="sxs-lookup"><span data-stu-id="e6adf-166">To edit an entry, select it and click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png).</span></span> <span data-ttu-id="e6adf-167">Pour supprimer une entrée, sélectionnez-la et **Remove** ![cliquez sur supprimer](../../media/ITPro-EAC-DeleteIcon.png)l’icône Supprimer.</span><span class="sxs-lookup"><span data-stu-id="e6adf-167">To remove an entry, select it and click **Remove** ![Remove icon](../../media/ITPro-EAC-DeleteIcon.png).</span></span>

     <span data-ttu-id="e6adf-168">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6adf-168">When you're finished, click **OK**.</span></span>

   - <span data-ttu-id="e6adf-169">**Procédez comme suit**: sélectionnez **Ajouter des destinataires** \> **dans le champ CCI**.</span><span class="sxs-lookup"><span data-stu-id="e6adf-169">**Do the following**: Select **Add recipients** \> **to the Bcc box**.</span></span> <span data-ttu-id="e6adf-170">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez les destinataires que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="e6adf-170">In the dialog that appears, find and select the recipients that you want to add.</span></span> <span data-ttu-id="e6adf-171">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6adf-171">When you're finished, click **OK**.</span></span>

4. <span data-ttu-id="e6adf-172">Vous pouvez effectuer des sélections supplémentaires pour auditer la règle, tester la règle, activer la règle pendant une période spécifique, ainsi que d’autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="e6adf-172">You can make additional selections to audit the rule, test the rule, activate the rule during a specific time period, and other settings.</span></span> <span data-ttu-id="e6adf-173">Nous vous recommandons de tester la règle avant de l’appliquer.</span><span class="sxs-lookup"><span data-stu-id="e6adf-173">We recommend testing the rule before you enforce it.</span></span>

5. <span data-ttu-id="e6adf-174">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e6adf-174">When you're finished, click **Save**.</span></span>

### <a name="use-powershell-to-create-a-mail-flow-rule-to-receive-copies-of-reported-messages"></a><span data-ttu-id="e6adf-175">Utiliser PowerShell pour créer une règle de flux de messagerie pour recevoir des copies des messages signalés</span><span class="sxs-lookup"><span data-stu-id="e6adf-175">Use PowerShell to create a mail flow rule to receive copies of reported messages</span></span>

<span data-ttu-id="e6adf-176">Cet exemple crée une règle de flux de messagerie nommée CCI messages signalés à Microsoft qui recherche les messages électroniques signalés à Microsoft à l’aide des méthodes décrites dans cette rubrique, et ajoute les utilisateurs laura@contoso.com et julia@contoso.com en tant que destinataires CCI.</span><span class="sxs-lookup"><span data-stu-id="e6adf-176">This example creates a new mail flow rule named Bcc Messages Reported to Microsoft that looks for email messages that are reported to Microsoft by using the methods described in this topic, and adds the users laura@contoso.com and julia@contoso.com as Bcc recipients.</span></span>

```powershell
New-TransportRule -Name "Bcc Messages Reported to Microsoft" -RecipientAddressContainsWords "junk@office365.microsoft.com","abuse@messaging.microsoft.com","phish@office365.microsoft.com","false_positive@messaging.microsoft.com" -BlindCopyTo "laura@contoso.com","julia@contoso.com".
```

<span data-ttu-id="e6adf-177">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-transportrule).</span><span class="sxs-lookup"><span data-stu-id="e6adf-177">For detailed syntax and parameter information, see [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-transportrule).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="e6adf-178">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="e6adf-178">How do you know this worked?</span></span>

<span data-ttu-id="e6adf-179">Pour vérifier que vous avez configuré des règles de flux de messagerie pour recevoir des copies de messages signalés, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6adf-179">To verify that you've configured a mail flow rules to receive copies of reported messages, do any of the following steps:</span></span>

- <span data-ttu-id="e6adf-180">Dans le centre d’administration Exchange, accédez à **règles** \> de **flux** \> de **Edit** ![messagerie sélectionnez la](../../media/ITPro-EAC-EditIcon.png)règle \> , cliquez sur modifier l’icône d’édition et vérifiez les paramètres.</span><span class="sxs-lookup"><span data-stu-id="e6adf-180">In the EAC, go to **Mail flow** \> **Rules** \> select the rule \> click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png), and verify the settings.</span></span>

- <span data-ttu-id="e6adf-181">Dans PowerShell, exécutez la commande suivante pour vérifier les paramètres :</span><span class="sxs-lookup"><span data-stu-id="e6adf-181">In PowerShell, run the following command to verify the settings:</span></span>

  ```powershell
  Get-TransportRule -Identity "Bcc Messages Reported to Microsoft" | Format-List
  ```

- <span data-ttu-id="e6adf-182">Envoyez un message de test à l’une des adresses de messagerie de création de rapports et vérifiez les résultats.</span><span class="sxs-lookup"><span data-stu-id="e6adf-182">Send a test messages to one of the reporting email addresses and verify the results.</span></span>
