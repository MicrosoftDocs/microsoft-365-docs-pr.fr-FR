---
title: Utiliser des règles de flux de messagerie pour configurer le filtrage du courrier en nombre dans Exchange Online Protection
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à utiliser des règles de flux de messagerie dans Exchange Online Protection pour le filtrage de courrier en nombre.
ms.openlocfilehash: 557a12455284519cc224cbee5e40a564aa3d4f14
ms.sourcegitcommit: cbf117a4cd92a907115c9f10752f3c557361e586
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/10/2019
ms.locfileid: "37441145"
---
# <a name="use-mail-flow-rules-to-configure-bulk-email-filtering-in-exchange-online-protection"></a><span data-ttu-id="c66a6-103">Utiliser des règles de flux de messagerie pour configurer le filtrage du courrier en nombre dans Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="c66a6-103">Use mail flow rules to configure bulk email filtering in Exchange Online Protection</span></span>

<span data-ttu-id="c66a6-p101">Vous pouvez définir des filtres de contenu à l'échelle de l'entreprise pour le courrier indésirable et le courrier en masse à l'aide des stratégies de filtrage de contenu du courrier indésirable par défaut. Consultez la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md) et [Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/Set-HostedContentFilterPolicy?view=exchange-ps) sur la façon de définir les stratégies de filtrage de contenu.</span><span class="sxs-lookup"><span data-stu-id="c66a6-p101">You can set company-wide content filters for spam and bulk email using the default spam content-filter policies. Check out [Configure your spam filter policies](configure-your-spam-filter-policies.md) and [Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/Set-HostedContentFilterPolicy?view=exchange-ps) on how to set the content filter policies.</span></span>

<span data-ttu-id="c66a6-106">Si vous souhaitez utiliser davantage d’options pour filtrer les messages en masse, vous pouvez créer des règles de flux de messagerie (également appelées règles de transport) pour rechercher des modèles de texte ou des expressions fréquemment trouvées dans les messages électroniques en masse.</span><span class="sxs-lookup"><span data-stu-id="c66a6-106">If you want to more options to filter bulk messages, you can create mail flow rules (also known as transport rules) to search for text patterns or phrases frequently found in bulk emails.</span></span> <span data-ttu-id="c66a6-107">Tout message contenant ces caractéristiques sera marqué comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c66a6-107">Any message containing these characteristics will be marked as spam.</span></span> <span data-ttu-id="c66a6-108">L'utilisation de ces règles peut aider à réduire la quantité de messages électroniques indésirables que reçoit votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c66a6-108">Using these rules can help reduce the amount of unwanted bulk email your organization receives.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c66a6-109">Avant de créer les règles de flux de messagerie décrites dans cette rubrique, nous vous recommandons de lire [d’abord la différence entre le courrier indésirable et le courrier électronique en](what-s-the-difference-between-junk-email-and-bulk-email.md) masse, ainsi que les [valeurs de niveau de réclamation en bloc](bulk-complaint-level-values.md).</span><span class="sxs-lookup"><span data-stu-id="c66a6-109">Before creating the mail flow rules documented this topic, we recommend that you first read [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md) and [Bulk Complaint Level values](bulk-complaint-level-values.md).</span></span><br><span data-ttu-id="c66a6-p103">Les procédures suivantes permettent de marquer un message comme indésirable à l'échelle de votre organisation toute entière. Toutefois, vous pouvez ajouter une condition afin de n'appliquer ces règles qu'à des destinataires spécifiques de votre organisation. De cette façon, les paramètres de filtrage restrictif des messages électroniques ne s'appliqueront qu'à quelques utilisateurs particulièrement ciblés et le reste de vos utilisateurs (qui reçoivent en général les messages électroniques en masse auxquels ils se sont inscrits) ne seront pas concernés.</span><span class="sxs-lookup"><span data-stu-id="c66a6-p103"> The following procedures mark a message as spam for your entire organization. However, you can add another condition to apply these rules only to specific recipients in your organization. This way, the aggressive bulk email filtering settings can apply to a few users who are highly targeted, while the rest of your users (who mostly get the bulk email they signed up for) aren't impacted.</span></span>

## <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a><span data-ttu-id="c66a6-113">Créer une règle de flux de messagerie pour filtrer les messages électroniques en masse en fonction des modèles de texte</span><span class="sxs-lookup"><span data-stu-id="c66a6-113">Create a mail flow rule to filter bulk email messages based on text patterns</span></span>

1. <span data-ttu-id="c66a6-114">Dans le Centre d’administration Exchange, accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="c66a6-114">In the Exchange admin center (EAC), go to **Mail flow** \> **Rules**.</span></span>

2. <span data-ttu-id="c66a6-115">Cliquez sur **Ajouter** ![une](../media/ITPro-EAC-AddIcon.gif) icône Ajouter, puis sélectionnez **créer une nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="c66a6-115">Click **Add** ![Add Icon](../media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>

3. <span data-ttu-id="c66a6-116">Indiquez le nom de la règle.</span><span class="sxs-lookup"><span data-stu-id="c66a6-116">Specify a name for the rule.</span></span>

4. <span data-ttu-id="c66a6-117">Cliquez sur **plus** ![d’options.](../media/ITPro-EAC-MoreOptionsIcon.png)icône autres options.</span><span class="sxs-lookup"><span data-stu-id="c66a6-117">Click **More options** ![More options icon](../media/ITPro-EAC-MoreOptionsIcon.png).</span></span> <span data-ttu-id="c66a6-118">Sous **Appliquer cette règle si**, sélectionnez **L'objet ou le corps** \> **l'objet ou le corps correspond à ces modèles de texte**.</span><span class="sxs-lookup"><span data-stu-id="c66a6-118">Under **Apply this rule if**, select **The subject or body** \> **subject or body matches these text patterns**.</span></span>

5. <span data-ttu-id="c66a6-119">Dans la boîte de dialogue **spécifier des mots ou des expressions** , ajoutez une par une les expressions régulières suivantes généralement présentes dans les messages électroniques en masse, puis cliquez sur **OK** lorsque vous avez fini :</span><span class="sxs-lookup"><span data-stu-id="c66a6-119">In the **specify words or phrases** dialog box, add the following regular expressions commonly found in bulk emails, one at a time, and click **OK** when you're done:</span></span>

   - `If you are unable to view the content of this email\, please`

   - `\>(safe )?unsubscribe( here)?\</a\>`

   - `If you do not wish to receive further communications like this\, please`

   - `\<img height\="?1"? width\="?1"? sr\c=.?http\://`

   - `To stop receiving these+emails\:http\://`

   - `To unsubscribe from \w+ (e\-?letter|e?-?mail|newsletter)`

   - `no longer (wish )?(to )?(be sent|receive) w+ email`

   - `If you are unable to view the content of this email\, please click here`

   - `To ensure you receive (your daily deals|our e-?mails)\, add`

   - `If you no longer wish to receive these emails`

   - `to change your (subscription preferences|preferences or unsubscribe)`

   - `click (here to|the) unsubscribe`

   <span data-ttu-id="c66a6-120">La liste ci-dessus n’est pas un ensemble exhaustif d’expressions régulières trouvées dans les messages électroniques en masse ; vous pouvez en ajouter ou en supprimer autant que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c66a6-120">The above list isn't an exhaustive set of regular expressions found in bulk emails; more can be added or removed as needed.</span></span> <span data-ttu-id="c66a6-121">Toutefois, ils constituent un bon point de départ.</span><span class="sxs-lookup"><span data-stu-id="c66a6-121">However, it's a good starting point.</span></span>

   <span data-ttu-id="c66a6-p106">La recherche de mots clés ou de modèles de texte dans l’objet ou dans d’autres champs d’en-tête du message est effectuée *après* que le codage utilisé avec la méthode MIME pour transmettre le message binaire entre les serveurs SMTP a été décodé en texte ASCII. Vous ne pouvez pas utiliser de conditions ou d’exceptions pour rechercher les valeurs codées brutes (en règle générale, en base 64) dans l’objet ou d’autres champs d’en-tête des messages.</span><span class="sxs-lookup"><span data-stu-id="c66a6-p106">The search for words or text patterns in the subject or other header fields in the message occurs *after* the message has been decoded from the MIME content transfer encoding method that was used to transmit the binary message between SMTP servers in ASCII text. You can't use conditions or exceptions to search for the raw (typically, Base64) encoded values of the subject or other header fields in messages.</span></span>

6. <span data-ttu-id="c66a6-124">Sous **Effectuer les opérations suivantes**, sélectionnez **Modifier les propriétés des messages** \> **Définir le seuil de probabilité de courrier indésirable (SCL)**.</span><span class="sxs-lookup"><span data-stu-id="c66a6-124">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>

7. <span data-ttu-id="c66a6-125">Dans la boîte de dialogue **spécifier la valeur SCL**, définissez la valeur SCL sur **5**, **6** ou **9**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c66a6-125">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>

   <span data-ttu-id="c66a6-p107">La définition du SCL sur 5 ou 6 déclenche l'action **Courrier indésirable**, tandis qu'une définition sur 9 déclenche l'action **Courrier indésirable à niveau de confiance élevé**, comme configuré dans la stratégie de filtrage du contenu. Le service effectue l'action définie dans la stratégie de filtrage de contenu. L'action par défaut consiste à placer le message dans le dossier Courrier indésirable des destinataires, mais différentes actions peuvent être configurées, comme décrit dans [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c66a6-p107">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>

   <span data-ttu-id="c66a6-129">Si votre action configurée consiste à mettre le message en quarantaine au lieu de l’envoyer au dossier de courrier indésirable des destinataires, le message est envoyé à la mise en quarantaine de l’administrateur en tant que correspondance de règle de flux de messagerie et n’est pas disponible dans le cadre de la mise en quarantaine du courrier indésirable de l’utilisateur final ou via l’utilisateur final notifications de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c66a6-129">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span>

   <span data-ttu-id="c66a6-130">Pour plus d'informations sur les valeurs SCL, voir [Seuils de probabilité de courrier indésirable](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="c66a6-130">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>

8. <span data-ttu-id="c66a6-131">Enregistrez la règle.</span><span class="sxs-lookup"><span data-stu-id="c66a6-131">Save the rule.</span></span>

## <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-phrases"></a><span data-ttu-id="c66a6-132">Créer une règle de flux de messagerie pour filtrer les messages électroniques en masse en fonction des expressions</span><span class="sxs-lookup"><span data-stu-id="c66a6-132">Create a mail flow rule to filter bulk email messages based on phrases</span></span>

1. <span data-ttu-id="c66a6-133">Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="c66a6-133">In the EAC, go to **Mail flow** \> **Rules**.</span></span>

2. <span data-ttu-id="c66a6-134">Cliquez sur **Ajouter** ![une](../media/ITPro-EAC-AddIcon.gif) icône Ajouter, puis sélectionnez **créer une nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="c66a6-134">Click **Add** ![Add Icon](../media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>

3. <span data-ttu-id="c66a6-135">Indiquez le nom de la règle.</span><span class="sxs-lookup"><span data-stu-id="c66a6-135">Specify a name for the rule.</span></span>

4. <span data-ttu-id="c66a6-p108">Cliquez sur **Plus d'options**. Sous **Appliquer cette règle si**, sélectionnez **L'objet ou le corps** \> **l'objet ou le corps inclut l'un de ces mots**.</span><span class="sxs-lookup"><span data-stu-id="c66a6-p108">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body includes any of these words**.</span></span>

5. <span data-ttu-id="c66a6-138">Dans la boîte de dialogue **spécifier des mots ou des expressions**, ajoutez une par une les expressions suivantes, qui figurent généralement dans les messages électroniques en masse, et cliquez sur **OK** lorsque vous avez terminé :</span><span class="sxs-lookup"><span data-stu-id="c66a6-138">In the **specify words or phrases** dialog box, add the following phrases commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span>

   - `to change your preferences or unsubscribe`

   - `Modify email preferences or unsubscribe`

   - `This is a promotional email`

   - `You are receiving this email because you requested a subscription`

   - `click here to unsubscribe`

   - `You have received this email because you are subscribed`

   - `If you no longer wish to receive our email newsletter`

   - `to unsubscribe from this newsletter`

   - `If you have trouble viewing this email`

   - `This is an advertisement`

   - `you would like to unsubscribe or change your`

   - `view this email as a webpage`

   - `You are receiving this email because you are subscribed`

   <span data-ttu-id="c66a6-139">Cette liste n’est pas un ensemble exhaustif d’expressions trouvées dans les messages électroniques en masse ; vous pouvez en ajouter ou en supprimer autant que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c66a6-139">This list isn't an exhaustive set of phrases found in bulk emails; more can be added or removed as needed.</span></span> <span data-ttu-id="c66a6-140">Toutefois, ils constituent un bon point de départ.</span><span class="sxs-lookup"><span data-stu-id="c66a6-140">However, it's a good starting point.</span></span>

6. <span data-ttu-id="c66a6-141">Sous **Effectuer les opérations suivantes**, sélectionnez **Modifier les propriétés des messages** \> **Définir le seuil de probabilité de courrier indésirable (SCL)**.</span><span class="sxs-lookup"><span data-stu-id="c66a6-141">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>

7. <span data-ttu-id="c66a6-142">Dans la boîte de dialogue **spécifier la valeur SCL**, définissez la valeur SCL sur **5**, **6** ou **9**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c66a6-142">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>

   <span data-ttu-id="c66a6-p110">La définition du SCL sur 5 ou 6 déclenche l'action **Courrier indésirable**, tandis qu'une définition sur 9 déclenche l'action **Courrier indésirable à niveau de confiance élevé**, comme configuré dans la stratégie de filtrage du contenu. Le service effectue l'action définie dans la stratégie de filtrage de contenu. L'action par défaut consiste à placer le message dans le dossier Courrier indésirable des destinataires, mais différentes actions peuvent être configurées, comme décrit dans [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c66a6-p110">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>

   <span data-ttu-id="c66a6-146">Si votre action configurée consiste à mettre le message en quarantaine au lieu de l’envoyer au dossier de courrier indésirable des destinataires, le message est envoyé à la mise en quarantaine de l’administrateur en tant que correspondance de règle de flux de messagerie et n’est pas disponible dans le cadre de la mise en quarantaine du courrier indésirable de l’utilisateur final ou via l’utilisateur final notifications de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c66a6-146">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span>

   <span data-ttu-id="c66a6-147">Pour plus d'informations sur les valeurs SCL, voir [Seuils de probabilité de courrier indésirable](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="c66a6-147">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>

8. <span data-ttu-id="c66a6-148">Enregistrez la règle.</span><span class="sxs-lookup"><span data-stu-id="c66a6-148">Save the rule.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="c66a6-149">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="c66a6-149">For more information</span></span>

[<span data-ttu-id="c66a6-150">Quelle est la différence entre courrier indésirable et message électronique en masse ?</span><span class="sxs-lookup"><span data-stu-id="c66a6-150">What's the difference between junk email and bulk email?</span></span>](what-s-the-difference-between-junk-email-and-bulk-email.md)

[<span data-ttu-id="c66a6-151">Valeurs BCL</span><span class="sxs-lookup"><span data-stu-id="c66a6-151">Bulk Complaint Level values</span></span>](bulk-complaint-level-values.md)

[<span data-ttu-id="c66a6-152">Configuration de vos stratégies de filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="c66a6-152">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)

[<span data-ttu-id="c66a6-153">Options de filtrage avancé du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="c66a6-153">Advanced spam filtering  options</span></span>](advanced-spam-filtering-asf-options.md)
