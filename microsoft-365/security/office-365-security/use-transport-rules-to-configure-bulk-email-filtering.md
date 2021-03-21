---
title: Utiliser des règles de flux de messagerie pour filtrer les messages électroniques en masse
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à utiliser des règles de flux de messagerie (règles de transport) pour identifier et filtrer le courrier en nombre (courrier gris) dans Exchange Online Protection (EOP).
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 8632a0b583ec0457ea1146f0e197321890414ce3
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50926677"
---
# <a name="use-mail-flow-rules-to-filter-bulk-email-in-eop"></a><span data-ttu-id="7046d-103">Utiliser des règles de flux de courriers pour filtrer les e-mails en bloc dans EOP</span><span class="sxs-lookup"><span data-stu-id="7046d-103">Use mail flow rules to filter bulk email in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="7046d-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="7046d-104">**Applies to**</span></span>
- [<span data-ttu-id="7046d-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="7046d-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="7046d-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="7046d-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="7046d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7046d-107">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="7046d-108">Dans les organisations Microsoft 365 ayant des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, EOP utilise des stratégies anti-courrier indésirable (également appelées stratégies de filtrage du courrier indésirable ou stratégies de filtrage de contenu) pour analyser les messages entrants à la recherche de courrier indésirable et de courrier en masse (également appelé courrier gris).</span><span class="sxs-lookup"><span data-stu-id="7046d-108">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, EOP uses anti-spam policies (also known as spam filter policies or content filter policies) to scan inbound messages for spam and bulk mail (also known as gray mail).</span></span> <span data-ttu-id="7046d-109">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="7046d-109">For more information, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

<span data-ttu-id="7046d-110">Si vous souhaitez plus d’options pour filtrer le courrier en nombre, vous pouvez créer des règles de flux de messagerie (également appelées règles de transport) pour rechercher des modèles de texte ou des expressions fréquemment trouvés dans les messages en nombre, et marquer ces messages comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="7046d-110">If you want more options to filter bulk mail, you can create mail flow rules (also known as transport rules) to search for text patterns or phrases that are frequently found in bulk mail, and mark those messages as spam.</span></span> <span data-ttu-id="7046d-111">Pour plus [d’informations](what-s-the-difference-between-junk-email-and-bulk-email.md) sur le courrier en nombre, voir Quelle est la différence entre le courrier indésirable et le courrier en masse ? et le niveau de réclamation en bloc [(BCL) dans EOP](bulk-complaint-level-values.md).</span><span class="sxs-lookup"><span data-stu-id="7046d-111">For more information about bulk mail, see [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md) and [Bulk complaint level (BCL) in EOP](bulk-complaint-level-values.md).</span></span>

<span data-ttu-id="7046d-112">Cette rubrique explique comment créer ces règles de flux de messagerie dans le Centre d’administration Exchange (CAE) et PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec boîtes aux lettres dans Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="7046d-112">This topic explains how create these mail flow rules in the Exchange admin center (EAC) and PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="7046d-113">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="7046d-113">What do you need to know before you begin?</span></span>

- <span data-ttu-id="7046d-114">Des autorisations doivent vous être attribuées dans Exchange Online ou Exchange Online Protection avant de pouvoir suivre les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="7046d-114">You need to be assigned permissions in Exchange Online or Exchange Online Protection before you can do the procedures in this article.</span></span> <span data-ttu-id="7046d-115">Plus précisément, vous avez besoin du rôle Règles de **transport,** qui est  attribué par défaut aux groupes de rôles Gestion de l’organisation, Gestion de la conformité **(administrateurs** globaux) et Gestion des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="7046d-115">Specifically, you need the **Transport Rules** role, which is assigned to the **Organization Management**, **Compliance Management** (global admins), and **Records Management** role groups by default.</span></span>

  <span data-ttu-id="7046d-116">Pour plus d’informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="7046d-116">For more information, see the following topics:</span></span>

  - [<span data-ttu-id="7046d-117">Autorisations dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="7046d-117">Permissions in Exchange Online</span></span>](/exchange/permissions-exo/permissions-exo)
  - [<span data-ttu-id="7046d-118">Autorisations dans EOP autonome</span><span class="sxs-lookup"><span data-stu-id="7046d-118">Permissions in standalone EOP</span></span>](feature-permissions-in-eop.md)
  - [<span data-ttu-id="7046d-119">Utiliser le EAC pour modifier la liste des membres dans les groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="7046d-119">Use the EAC modify the list of members in role groups</span></span>](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups)

- <span data-ttu-id="7046d-120">Pour ouvrir le CENTRE d’administration Exchange dans Exchange Online, consultez le [Centre d’administration Exchange dans Exchange Online.](/Exchange/exchange-admin-center)</span><span class="sxs-lookup"><span data-stu-id="7046d-120">To open the EAC in Exchange Online, see [Exchange admin center in Exchange Online](/Exchange/exchange-admin-center).</span></span> <span data-ttu-id="7046d-121">Pour ouvrir le CAE dans EOP autonome, consultez le Centre d’administration [Exchange dans EOP autonome.](exchange-admin-center-in-exchange-online-protection-eop.md)</span><span class="sxs-lookup"><span data-stu-id="7046d-121">To open the EAC in standalone EOP, see [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="7046d-122">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="7046d-122">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="7046d-123">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="7046d-123">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="7046d-124">Pour plus d’informations sur les règles de flux de messagerie dans Exchange Online et EOP autonome, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="7046d-124">For more information about mail flow rules in Exchange Online and standalone EOP, see the following topics:</span></span>

  - [<span data-ttu-id="7046d-125">Règles de flux de messagerie (règles de transport) dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="7046d-125">Mail flow rules (transport rules) in Exchange Online</span></span>](/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)

  - [<span data-ttu-id="7046d-126">Conditions de règle de flux de messagerie et exceptions (prédicats) dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="7046d-126">Mail flow rule conditions and exceptions (predicates) in Exchange Online</span></span>](/Exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions)

  - [<span data-ttu-id="7046d-127">Actions de règle de flux de courrier dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="7046d-127">Mail flow rule actions in Exchange Online</span></span>](/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions)

- <span data-ttu-id="7046d-128">La liste des mots et des modèles de texte utilisés pour identifier les messages en nombre dans les exemples n’est pas exhaustive . vous pouvez ajouter et supprimer des entrées si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7046d-128">The list of words and text patterns that are used to identify bulk mail in the examples aren't exhaustive; you can add and remove entries as necessary.</span></span> <span data-ttu-id="7046d-129">Toutefois, ils sont un bon point de départ.</span><span class="sxs-lookup"><span data-stu-id="7046d-129">However, they are a good starting point.</span></span>

- <span data-ttu-id="7046d-p107">La recherche de mots clés ou de modèles de texte dans l’objet ou dans d’autres champs d’en-tête du message est effectuée *après* que le codage utilisé avec la méthode MIME pour transmettre le message binaire entre les serveurs SMTP a été décodé en texte ASCII. Vous ne pouvez pas utiliser de conditions ou d’exceptions pour rechercher les valeurs codées brutes (en règle générale, en base 64) dans l’objet ou d’autres champs d’en-tête des messages.</span><span class="sxs-lookup"><span data-stu-id="7046d-p107">The search for words or text patterns in the subject or other header fields in the message occurs *after* the message has been decoded from the MIME content transfer encoding method that was used to transmit the binary message between SMTP servers in ASCII text. You can't use conditions or exceptions to search for the raw (typically, Base64) encoded values of the subject or other header fields in messages.</span></span>

- <span data-ttu-id="7046d-132">Les procédures suivantes marquent un message en masse comme courrier indésirable pour l’ensemble de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7046d-132">The following procedures mark a bulk message as spam for your entire organization.</span></span> <span data-ttu-id="7046d-133">Toutefois, vous pouvez ajouter une autre condition pour appliquer ces règles uniquement à des destinataires spécifiques, afin que vous pouvez utiliser un filtrage agressif sur quelques utilisateurs hautement ciblés, tandis que le reste de vos utilisateurs (qui obtiennent principalement le courrier en nombre pour qui ils se sont inscrits) ne sont pas touchés.</span><span class="sxs-lookup"><span data-stu-id="7046d-133">However, you can add another condition to apply these rules only to specific recipients, so you can use aggressive filtering on a few, highly targeted users, while the rest of your users (who mostly get the bulk email they signed up for) aren't impacted.</span></span>

## <a name="use-the-eac-to-create-mail-flow-rules-that-filter-bulk-email"></a><span data-ttu-id="7046d-134">Utiliser le EAC pour créer des règles de flux de messagerie qui filtrent les messages électroniques en masse</span><span class="sxs-lookup"><span data-stu-id="7046d-134">Use the EAC to create mail flow rules that filter bulk email</span></span>

1. <span data-ttu-id="7046d-135">Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="7046d-135">In the EAC, go to **Mail flow** \> **Rules**.</span></span>

2. <span data-ttu-id="7046d-136">Cliquez **sur Ajouter** une icône ![ ](../../media/ITPro-EAC-AddIcon.png) Ajouter, puis **sélectionnez Créer une règle.**</span><span class="sxs-lookup"><span data-stu-id="7046d-136">Click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png) and then select **Create a new rule**.</span></span>

3. <span data-ttu-id="7046d-137">Dans la page **Nouvelle règle** qui s'ouvre, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7046d-137">In the **New rule** page that opens, configure the following settings:</span></span>

   - <span data-ttu-id="7046d-138">**Nom**: entrez un nom unique et descriptif pour la règle.</span><span class="sxs-lookup"><span data-stu-id="7046d-138">**Name**: Enter a unique, descriptive name for the rule.</span></span>

   - <span data-ttu-id="7046d-139">Cliquez sur **Autres options**.</span><span class="sxs-lookup"><span data-stu-id="7046d-139">Click **More Options**.</span></span>

   - <span data-ttu-id="7046d-140">**Appliquez cette règle si**: Configurez l’un des paramètres suivants pour rechercher du contenu dans les messages à l’aide d’expressions régulières (RegEx), de mots ou d’expressions :</span><span class="sxs-lookup"><span data-stu-id="7046d-140">**Apply this rule if**: Configure one of the following settings to look for content in messages using regular expressions (RegEx) or words or phrases:</span></span>

     - <span data-ttu-id="7046d-141">**Objet ou corps** \> l’objet ou le corps correspond à ces **modèles** de texte : dans la  boîte de dialogue Spécifier des mots ou des expressions qui s’affiche, entrez l’une des **valeurs** suivantes, cliquez sur Ajouter une icône, puis répétez ![ jusqu’à ce que vous avez entré toutes les ](../../media/ITPro-EAC-AddIcon.png) valeurs.</span><span class="sxs-lookup"><span data-stu-id="7046d-141">**The subject or body** \> **subject or body matches these text patterns**: In the **Specify words or phrases** dialog that appears, enter one of the following values, click **Add** ![Add Icon](../../media/ITPro-EAC-AddIcon.png), and repeat until you've entered all the values.</span></span>

       - `If you are unable to view the content of this email\, please`
       - `\>(safe )?unsubscribe( here)?\</a\>`
       - `If you do not wish to receive further communications like this\, please`
       - `<img height="?1"? width="?1"? src=.?http\://`
       - `To stop receiving these+emails\:http\://`
       - `To unsubscribe from \w+ (e\-?letter|e?-?mail|newsletter)`
       - `no longer (wish )?(to )?(be sent|receive) w+ email`
       - `If you are unable to view the content of this email\, please click here`
       - `To ensure you receive (your daily deals|our e-?mails)\, add`
       - `If you no longer wish to receive these emails`
       - `to change your (subscription preferences|preferences or unsubscribe)`
       - `click (here to|the) unsubscribe`

      <span data-ttu-id="7046d-142">Pour modifier une entrée, sélectionnez-la et cliquez sur **Modifier** ![ ](../../media/ITPro-EAC-EditIcon.png) l’icône Modifier.</span><span class="sxs-lookup"><span data-stu-id="7046d-142">To edit an entry, select it and click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png).</span></span> <span data-ttu-id="7046d-143">Pour supprimer une entrée, sélectionnez-la et cliquez **sur Supprimer** ![ l’icône ](../../media/ITPro-EAC-DeleteIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="7046d-143">To remove an entry, select it and click **Remove** ![Remove icon](../../media/ITPro-EAC-DeleteIcon.png).</span></span>

       <span data-ttu-id="7046d-144">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7046d-144">When you're finished, click **OK**.</span></span>

     - <span data-ttu-id="7046d-145">**Objet ou corps** \> **l’objet** ou le corps inclut l’un de ces mots : dans la  boîte de dialogue Spécifier des mots ou des expressions qui s’affiche, entrez l’une des **valeurs suivantes,** cliquez sur Ajouter une icône, puis répétez ![ jusqu’à ce que vous avez entré toutes les ](../../media/ITPro-EAC-AddIcon.png) valeurs.</span><span class="sxs-lookup"><span data-stu-id="7046d-145">**The subject or body** \> **subject or body includes any of these words**: In the **Specify words or phrases** dialog that appears, enter one of the following values, click **Add** ![Add Icon](../../media/ITPro-EAC-AddIcon.png), and repeat until you've entered all the values.</span></span>

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

      <span data-ttu-id="7046d-146">Pour modifier une entrée, sélectionnez-la et cliquez sur **Modifier** ![ ](../../media/ITPro-EAC-EditIcon.png) l’icône Modifier.</span><span class="sxs-lookup"><span data-stu-id="7046d-146">To edit an entry, select it and click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png).</span></span> <span data-ttu-id="7046d-147">Pour supprimer une entrée, sélectionnez-la et cliquez **sur Supprimer** ![ l’icône ](../../media/ITPro-EAC-DeleteIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="7046d-147">To remove an entry, select it and click **Remove** ![Remove icon](../../media/ITPro-EAC-DeleteIcon.png).</span></span>

       <span data-ttu-id="7046d-148">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7046d-148">When you're finished, click **OK**.</span></span>

   - <span data-ttu-id="7046d-149">**Pour ce faire,** **sélectionnez Modifier les propriétés du message** pour définir le niveau de \> **confiance du courrier indésirable (SCL).**</span><span class="sxs-lookup"><span data-stu-id="7046d-149">**Do the following**: Select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span> <span data-ttu-id="7046d-150">Dans la **boîte de dialogue Spécifier le SCL** qui s’affiche, configurez l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7046d-150">In the **Specify SCL** dialog that appears, configure one of the following settings:</span></span>

     - <span data-ttu-id="7046d-151">Pour marquer les messages comme **courrier indésirable,** **sélectionnez 6**.</span><span class="sxs-lookup"><span data-stu-id="7046d-151">To mark messages as **Spam**, select **6**.</span></span> <span data-ttu-id="7046d-152">L’action que vous avez  configurée pour les verdicts de filtrage du courrier indésirable dans vos stratégies anti-courrier indésirable est appliquée aux messages (la valeur par défaut est Déplacer le message vers le dossier Courrier **indésirable).**</span><span class="sxs-lookup"><span data-stu-id="7046d-152">The action that you've configured for **Spam** filtering verdicts in your anti-spam policies is applied to the messages (the default value is **Move message to Junk Email folder**).</span></span>

     - <span data-ttu-id="7046d-153">Pour marquer les messages comme courrier **indésirable à niveau de confiance élevé,** **sélectionnez 9**.</span><span class="sxs-lookup"><span data-stu-id="7046d-153">To mark messages as **High confidence spam** select **9**.</span></span> <span data-ttu-id="7046d-154">L’action que vous avez  configurée pour les verdicts de filtrage du courrier indésirable à niveau de confiance élevé dans vos stratégies anti-courrier indésirable est appliquée aux messages (la valeur par défaut est Déplacer le message vers le dossier Courrier **indésirable).**</span><span class="sxs-lookup"><span data-stu-id="7046d-154">The action that you've configured for **High confidence spam** filtering verdicts in your anti-spam policies is applied to the messages (the default value is **Move message to Junk Email folder**).</span></span>

    <span data-ttu-id="7046d-155">Pour plus d’informations sur les valeurs SCL, voir Le niveau de confiance du courrier indésirable [(SCL) dans EOP.](spam-confidence-levels.md)</span><span class="sxs-lookup"><span data-stu-id="7046d-155">For more information about SCL values, see [Spam confidence level (SCL) in EOP](spam-confidence-levels.md).</span></span>

   <span data-ttu-id="7046d-156">Lorsque vous avez terminé, cliquez sur **Enregistrer**</span><span class="sxs-lookup"><span data-stu-id="7046d-156">When you're finished, click **Save**</span></span>

## <a name="use-powershell-to-create-mail-flow-rules-that-filter-bulk-email"></a><span data-ttu-id="7046d-157">Utiliser PowerShell pour créer des règles de flux de messagerie qui filtrent les messages électroniques en masse</span><span class="sxs-lookup"><span data-stu-id="7046d-157">Use PowerShell to create mail flow rules that filter bulk email</span></span>

<span data-ttu-id="7046d-158">Utilisez la syntaxe suivante pour créer une ou les deux règles de flux de messagerie (expressions régulières et mots) :</span><span class="sxs-lookup"><span data-stu-id="7046d-158">Use the following syntax to create one or both of the mail flow rules (regular expressions vs. words):</span></span>

```powershell
New-TransportRule -Name "<UniqueName>" [-SubjectOrBodyMatchesPatterns "<RegEx1>","<RegEx2>"...] [-SubjectOrBodyContainsWords "<WordOrPhrase1>","<WordOrPhrase2>"...] -SetSCL <6 | 9>
```

<span data-ttu-id="7046d-159">Cet exemple crée une règle nommée « Bulk email filtering - RegEx » qui utilise la même liste d’expressions régulières plus tôt dans la rubrique pour définir les messages comme courrier **indésirable**.</span><span class="sxs-lookup"><span data-stu-id="7046d-159">This example creates a new rule named "Bulk email filtering - RegEx" that uses the same list of regular expressions from earlier in the topic to set messages as **Spam**.</span></span>

```powershell
New-TransportRule -Name "Bulk email filtering - RegEx" -SubjectOrBodyMatchesPatterns "If you are unable to view the content of this email\, please","\>(safe )?unsubscribe( here)?\</a\>","If you do not wish to receive further communications like this\, please","\<img height\="?1"? width\="?1"? src=.?http\://","To stop receiving these+emails\:http\://","To unsubscribe from \w+ (e\-?letter|e?-?mail|newsletter)","no longer (wish )?(to )?(be sent|receive) w+ email","If you are unable to view the content of this email\, please click here","To ensure you receive (your daily deals|our e-?mails)\, add","If you no longer wish to receive these emails","to change your (subscription preferences|preferences or unsubscribe)","click (here to|the) unsubscribe"... -SetSCL 6
```

<span data-ttu-id="7046d-160">Cet exemple crée une règle nommée « Filtrage des messages électroniques en bloc - Mots » qui utilise la même liste de mots que celle de la rubrique précédente pour définir les messages comme courrier indésirable à niveau de confiance **élevé.**</span><span class="sxs-lookup"><span data-stu-id="7046d-160">This example creates a new rule named "Bulk email filtering - Words" that uses the same list of words from earlier in the topic to set messages as **High confidence spam**.</span></span>

```powershell
New-TransportRule -Name "Bulk email filtering - Words" -SubjectOrBodyContainsWords "to change your preferences or unsubscribe","Modify email preferences or unsubscribe","This is a promotional email","You are receiving this email because you requested a subscription","click here to unsubscribe","You have received this email because you are subscribed","If you no longer wish to receive our email newsletter","to unsubscribe from this newsletter","If you have trouble viewing this email","This is an advertisement","you would like to unsubscribe or change your","view this email as a webpage","You are receiving this email because you are subscribed" -SetSCL 9
```

<span data-ttu-id="7046d-161">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TransportRule](/powershell/module/exchange/new-transportrule).</span><span class="sxs-lookup"><span data-stu-id="7046d-161">For detailed syntax and parameter information, see [New-TransportRule](/powershell/module/exchange/new-transportrule).</span></span>

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="7046d-162">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="7046d-162">How do you know this worked?</span></span>

<span data-ttu-id="7046d-163">Pour vérifier que vous avez configuré des règles de flux de messagerie pour filtrer les messages électroniques en nombre, appliquez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="7046d-163">To verify that you've configured mail flow rules to filter bulk email, do any of the following steps:</span></span>

- <span data-ttu-id="7046d-164">Dans le EAC, sélectionnez Règles de **flux** de messagerie et sélectionnez l’icône Modifier, puis \>  \> \> vérifiez les  ![ ](../../media/ITPro-EAC-EditIcon.png) paramètres.</span><span class="sxs-lookup"><span data-stu-id="7046d-164">In the EAC, go to **Mail flow** \> **Rules** \> select the rule \> click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png), and verify the settings.</span></span>

- <span data-ttu-id="7046d-165">Dans PowerShell, remplacez-la par le nom de la règle et exécutez la commande suivante \<Rule Name\> pour vérifier les paramètres :</span><span class="sxs-lookup"><span data-stu-id="7046d-165">In PowerShell, replace \<Rule Name\> with the name of the rule, and run the following command to verify the settings:</span></span>

  ```powershell
  Get-TransportRule -Identity "<Rule Name>" | Format-List
  ```

- <span data-ttu-id="7046d-166">À partir d’un compte externe, envoyez un message de test à un destinataire affecté qui contient l’une des expressions ou des modèles de texte, puis vérifiez les résultats.</span><span class="sxs-lookup"><span data-stu-id="7046d-166">From an external account, send a test messages to an affected recipient that contains one of the phrases or text patterns, and verify the results.</span></span>