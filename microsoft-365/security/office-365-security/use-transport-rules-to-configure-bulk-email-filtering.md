---
title: Utiliser des règles de flux de messagerie pour filtrer les messages électroniques en masse
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à utiliser des règles de flux de messagerie (règles de transport) pour identifier et filtrer les messages en masse (courrier gris) dans Exchange Online Protection (EOP).
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: dfe841d3e80efc50d6ffbc702faefa1c9a971b13
ms.sourcegitcommit: e12fa502bc216f6083ef5666f693a04bb727d4df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "46826752"
---
# <a name="use-mail-flow-rules-to-filter-bulk-email-in-eop"></a><span data-ttu-id="dbe70-103">Utiliser des règles de flux de courrier pour filtrer les messages électroniques en bloc dans EOP</span><span class="sxs-lookup"><span data-stu-id="dbe70-103">Use mail flow rules to filter bulk email in EOP</span></span>

<span data-ttu-id="dbe70-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîte aux lettres Exchange Online, EOP utilise des stratégies de blocage du courrier indésirable (également appelées stratégies de filtrage du courrier indésirable) pour analyser les messages entrants pour le courrier indésirable et le courrier en nombre (également appelé courrier gris).</span><span class="sxs-lookup"><span data-stu-id="dbe70-104">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, EOP uses anti-spam policies (also known as spam filter policies or content filter policies) to scan inbound messages for spam and bulk mail (also known as gray mail).</span></span> <span data-ttu-id="dbe70-105">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="dbe70-105">For more information, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

<span data-ttu-id="dbe70-106">Si vous souhaitez utiliser davantage d’options pour filtrer les messages en masse, vous pouvez créer des règles de flux de messagerie (également appelées règles de transport) pour rechercher des modèles de texte ou des expressions fréquemment trouvées dans le courrier en nombre et marquer ces messages comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="dbe70-106">If you want more options to filter bulk mail, you can create mail flow rules (also known as transport rules) to search for text patterns or phrases that are frequently found in bulk mail, and mark those messages as spam.</span></span> <span data-ttu-id="dbe70-107">Pour plus d’informations sur le courrier en nombre, consultez [la rubrique quelle est la différence entre courrier indésirable et courrier électronique en masse ?](what-s-the-difference-between-junk-email-and-bulk-email.md) et [BCL (Bulk Complaint Level) dans EOP](bulk-complaint-level-values.md).</span><span class="sxs-lookup"><span data-stu-id="dbe70-107">For more information about bulk mail, see [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md) and [Bulk complaint level (BCL) in EOP](bulk-complaint-level-values.md).</span></span>

<span data-ttu-id="dbe70-108">Cette rubrique explique comment créer ces règles de flux de messagerie dans le centre d’administration Exchange et PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ; environnement de ligne de commande Exchange.</span><span class="sxs-lookup"><span data-stu-id="dbe70-108">This topic explains how create these mail flow rules in the Exchange admin center (EAC) and PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="dbe70-109">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="dbe70-109">What do you need to know before you begin?</span></span>

- <span data-ttu-id="dbe70-110">Pour pouvoir effectuer ces procédures, vous devez disposer des autorisations suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbe70-110">You need to be assigned permissions before you can do these procedures:</span></span>

  - <span data-ttu-id="dbe70-111">Dans Exchange Online, consultez l’entrée « flux de messagerie » dans [autorisations des fonctionnalités dans Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/feature-permissions).</span><span class="sxs-lookup"><span data-stu-id="dbe70-111">In Exchange Online, see the "Mail flow" entry in [Feature Permissions in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/feature-permissions).</span></span>
  
  - <span data-ttu-id="dbe70-112">Dans EOP autonome, vous avez besoin du rôle de règles de transport, qui est affecté par défaut aux rôles OrganizationManagement, ComplianceManagement et RecordsManagement.</span><span class="sxs-lookup"><span data-stu-id="dbe70-112">In standalone EOP, you need the Transport Rules role, which is assigned to the OrganizationManagement, ComplianceManagement, and RecordsManagement roles by default.</span></span> <span data-ttu-id="dbe70-113">Pour plus d’informations, consultez la rubrique [autorisations dans EOP autonome](feature-permissions-in-eop.md) et utiliser le centre d’administration Exchange pour [modifier la liste des membres dans les groupes de rôles](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span><span class="sxs-lookup"><span data-stu-id="dbe70-113">For more information, see [Permissions in standalone EOP](feature-permissions-in-eop.md) and [Use the EAC modify the list of members in role groups](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span></span>

- <span data-ttu-id="dbe70-114">Pour ouvrir le centre d’administration Exchange dans Exchange Online, consultez la rubrique [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center).</span><span class="sxs-lookup"><span data-stu-id="dbe70-114">To open the EAC in Exchange Online, see [Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center).</span></span> <span data-ttu-id="dbe70-115">Pour ouvrir le centre d’administration Exchange en mode autonome EOP, consultez la rubrique [Exchange Admin Center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="dbe70-115">To open the EAC in standalone EOP, see [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="dbe70-116">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="dbe70-116">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="dbe70-117">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="dbe70-117">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="dbe70-118">Pour plus d’informations sur les règles de flux de messagerie dans Exchange Online et dans la version autonome d’EOP, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbe70-118">For more information about mail flow rules in Exchange Online and standalone EOP, see the following topics:</span></span>

  - [<span data-ttu-id="dbe70-119">Règles de flux de messagerie (règles de transport) dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="dbe70-119">Mail flow rules (transport rules) in Exchange Online</span></span>](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)

  - [<span data-ttu-id="dbe70-120">Conditions de règle de flux de messagerie et exceptions (prédicats) dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="dbe70-120">Mail flow rule conditions and exceptions (predicates) in Exchange Online</span></span>](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions)

  - [<span data-ttu-id="dbe70-121">Actions de règle de flux de courrier dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="dbe70-121">Mail flow rule actions in Exchange Online</span></span>](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions)

- <span data-ttu-id="dbe70-122">La liste des mots et des modèles de texte utilisés pour identifier le courrier en nombre dans les exemples n’est pas exhaustive ; vous pouvez ajouter et supprimer des entrées si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="dbe70-122">The list of words and text patterns that are used to identify bulk mail in the examples aren't exhaustive; you can add and remove entries as necessary.</span></span> <span data-ttu-id="dbe70-123">Toutefois, ils constituent un point de départ approprié.</span><span class="sxs-lookup"><span data-stu-id="dbe70-123">However, they are a good starting point.</span></span>

- <span data-ttu-id="dbe70-p107">La recherche de mots clés ou de modèles de texte dans l’objet ou dans d’autres champs d’en-tête du message est effectuée *après* que le codage utilisé avec la méthode MIME pour transmettre le message binaire entre les serveurs SMTP a été décodé en texte ASCII. Vous ne pouvez pas utiliser de conditions ou d’exceptions pour rechercher les valeurs codées brutes (en règle générale, en base 64) dans l’objet ou d’autres champs d’en-tête des messages.</span><span class="sxs-lookup"><span data-stu-id="dbe70-p107">The search for words or text patterns in the subject or other header fields in the message occurs *after* the message has been decoded from the MIME content transfer encoding method that was used to transmit the binary message between SMTP servers in ASCII text. You can't use conditions or exceptions to search for the raw (typically, Base64) encoded values of the subject or other header fields in messages.</span></span>

- <span data-ttu-id="dbe70-126">Les procédures suivantes marquent un message en bloc comme courrier indésirable pour l’ensemble de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="dbe70-126">The following procedures mark a bulk message as spam for your entire organization.</span></span> <span data-ttu-id="dbe70-127">Toutefois, vous pouvez ajouter une autre condition pour appliquer ces règles à des destinataires spécifiques, de sorte que vous pouvez utiliser un filtrage agressif sur quelques utilisateurs hautement ciblés, tandis que les autres utilisateurs (qui obtiennent principalement le courrier en nombre auquel ils étaient inscrits) ne sont pas concernés.</span><span class="sxs-lookup"><span data-stu-id="dbe70-127">However, you can add another condition to apply these rules only to specific recipients, so you can use aggressive filtering on a few, highly targeted users, while the rest of your users (who mostly get the bulk email they signed up for) aren't impacted.</span></span>

## <a name="use-the-eac-to-create-mail-flow-rules-that-filter-bulk-email"></a><span data-ttu-id="dbe70-128">Utiliser le centre d’administration Exchange pour créer des règles de flux de messagerie qui filtrent les messages électroniques en masse</span><span class="sxs-lookup"><span data-stu-id="dbe70-128">Use the EAC to create mail flow rules that filter bulk email</span></span>

1. <span data-ttu-id="dbe70-129">Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="dbe70-129">In the EAC, go to **Mail flow** \> **Rules**.</span></span>

2. <span data-ttu-id="dbe70-130">Cliquez sur **Ajouter** ![ une icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) , puis sélectionnez **créer une nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="dbe70-130">Click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png) and then select **Create a new rule**.</span></span>

3. <span data-ttu-id="dbe70-131">Dans la page **Nouvelle règle** qui s'ouvre, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="dbe70-131">In the **New rule** page that opens, configure the following settings:</span></span>

   - <span data-ttu-id="dbe70-132">**Nom**: entrez un nom unique et descriptif pour la règle.</span><span class="sxs-lookup"><span data-stu-id="dbe70-132">**Name**: Enter a unique, descriptive name for the rule.</span></span>

   - <span data-ttu-id="dbe70-133">Cliquez sur **Autres options**.</span><span class="sxs-lookup"><span data-stu-id="dbe70-133">Click **More Options**.</span></span>

   - <span data-ttu-id="dbe70-134">**Appliquer cette règle si**: configurez l’un des paramètres suivants pour rechercher du contenu dans les messages à l’aide d’expressions régulières (Regex) ou de mots ou d’expressions :</span><span class="sxs-lookup"><span data-stu-id="dbe70-134">**Apply this rule if**: Configure one of the following settings to look for content in messages using regular expressions (RegEx) or words or phrases:</span></span>

     - <span data-ttu-id="dbe70-135">**L’objet ou le corps** \> l' **objet ou le corps correspond à ces modèles de texte**: dans la boîte de dialogue **spécifier des mots ou des expressions** qui s’affiche, entrez l’une des valeurs suivantes, puis cliquez sur **Ajouter** une ![ icône ](../../media/ITPro-EAC-AddIcon.png) et répétez l’opération jusqu’à ce que vous entriez toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="dbe70-135">**The subject or body** \> **subject or body matches these text patterns**: In the **Specify words or phrases** dialog that appears, enter one of the following values, click **Add** ![Add Icon](../../media/ITPro-EAC-AddIcon.png), and repeat until you've entered all the values.</span></span>

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

      <span data-ttu-id="dbe70-136">Pour modifier une entrée, sélectionnez-la et cliquez sur **modifier** l' ![ icône modifier ](../../media/ITPro-EAC-EditIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="dbe70-136">To edit an entry, select it and click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png).</span></span> <span data-ttu-id="dbe70-137">Pour supprimer une entrée, sélectionnez-la et cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-DeleteIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="dbe70-137">To remove an entry, select it and click **Remove** ![Remove icon](../../media/ITPro-EAC-DeleteIcon.png).</span></span>

       <span data-ttu-id="dbe70-138">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbe70-138">When you're finished, click **OK**.</span></span>

     - <span data-ttu-id="dbe70-139">**L’objet ou le corps** \> **Subject ou Body comprend l’un des mots**suivants : dans la boîte de dialogue **spécifier des mots ou des expressions** qui s’affiche, entrez l’une des valeurs suivantes, puis cliquez sur **Ajouter** une ![ icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) et répétez l’opération jusqu’à ce que vous ayez entré toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="dbe70-139">**The subject or body** \> **subject or body includes any of these words**: In the **Specify words or phrases** dialog that appears, enter one of the following values, click **Add** ![Add Icon](../../media/ITPro-EAC-AddIcon.png), and repeat until you've entered all the values.</span></span>

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

      <span data-ttu-id="dbe70-140">Pour modifier une entrée, sélectionnez-la et cliquez sur **modifier** l' ![ icône modifier ](../../media/ITPro-EAC-EditIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="dbe70-140">To edit an entry, select it and click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png).</span></span> <span data-ttu-id="dbe70-141">Pour supprimer une entrée, sélectionnez-la et cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-DeleteIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="dbe70-141">To remove an entry, select it and click **Remove** ![Remove icon](../../media/ITPro-EAC-DeleteIcon.png).</span></span>

       <span data-ttu-id="dbe70-142">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbe70-142">When you're finished, click **OK**.</span></span>

   - <span data-ttu-id="dbe70-143">**Procédez comme suit**: sélectionnez **modifier les propriétés du message** \> **définir le seuil de probabilité de courrier indésirable (SCL)**.</span><span class="sxs-lookup"><span data-stu-id="dbe70-143">**Do the following**: Select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span> <span data-ttu-id="dbe70-144">Dans la boîte de dialogue spécifier la valeur **SCL** qui s’affiche, configurez l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="dbe70-144">In the **Specify SCL** dialog that appears, configure one of the following settings:</span></span>

     - <span data-ttu-id="dbe70-145">Pour marquer les messages comme **courrier indésirable**, sélectionnez **6**.</span><span class="sxs-lookup"><span data-stu-id="dbe70-145">To mark messages as **Spam**, select **6**.</span></span> <span data-ttu-id="dbe70-146">L’action que vous avez configurée pour le filtrage du **courrier indésirable** dans vos stratégies de blocage du courrier indésirable est appliquée aux messages (la valeur par défaut est **déplacer le message vers le dossier courrier indésirable**).</span><span class="sxs-lookup"><span data-stu-id="dbe70-146">The action that you've configured for **Spam** filtering verdicts in your anti-spam policies is applied to the messages (the default value is **Move message to Junk Email folder**).</span></span>

     - <span data-ttu-id="dbe70-147">Pour marquer les messages comme **courriers indésirables à niveau de confiance élevé** , sélectionnez **9**.</span><span class="sxs-lookup"><span data-stu-id="dbe70-147">To mark messages as **High confidence spam** select **9**.</span></span> <span data-ttu-id="dbe70-148">L’action que vous avez configurée pour le filtrage du **courrier indésirable à niveau de confiance élevé** est appliquée aux messages dans vos stratégies de blocage du courrier indésirable (la valeur par défaut est **déplacer le message vers le dossier courrier indésirable**).</span><span class="sxs-lookup"><span data-stu-id="dbe70-148">The action that you've configured for **High confidence spam** filtering verdicts in your anti-spam policies is applied to the messages (the default value is **Move message to Junk Email folder**).</span></span>

    <span data-ttu-id="dbe70-149">Pour plus d’informations sur les valeurs SCL, voir [taux de probabilité de courrier indésirable (SCL) dans EOP](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="dbe70-149">For more information about SCL values, see [Spam confidence level (SCL) in EOP](spam-confidence-levels.md).</span></span>

   <span data-ttu-id="dbe70-150">Lorsque vous avez terminé, cliquez sur **Enregistrer** .</span><span class="sxs-lookup"><span data-stu-id="dbe70-150">When you're finished, click **Save**</span></span>

## <a name="use-powershell-to-create-mail-flow-rules-that-filter-bulk-email"></a><span data-ttu-id="dbe70-151">Utiliser PowerShell pour créer des règles de flux de messagerie qui filtrent les messages électroniques en masse</span><span class="sxs-lookup"><span data-stu-id="dbe70-151">Use PowerShell to create mail flow rules that filter bulk email</span></span>

<span data-ttu-id="dbe70-152">Utilisez la syntaxe suivante pour créer une des règles de flux de messagerie ou les deux (expressions régulières et mots) :</span><span class="sxs-lookup"><span data-stu-id="dbe70-152">Use the following syntax to create one or both of the mail flow rules (regular expressions vs. words):</span></span>

```powershell
New-TransportRule -Name "<UniqueName>" [-SubjectOrBodyMatchesPatterns "<RegEx1>","<RegEx2>"...] [-SubjectOrBodyContainsWords "<WordOrPhrase1>","<WordOrPhrase2>"...] -SetSCL <6 | 9>
```

<span data-ttu-id="dbe70-153">Cet exemple crée une nouvelle règle nommée « Bulk Email Filtering-RegEx » qui utilise la même liste d’expressions régulières que celle décrite plus haut dans la rubrique pour définir les messages comme **courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="dbe70-153">This example creates a new rule named "Bulk email filtering - RegEx" that uses the same list of regular expressions from earlier in the topic to set messages as **Spam**.</span></span>

```powershell
New-TransportRule -Name "Bulk email filtering - RegEx" -SubjectOrBodyMatchesPatterns "If you are unable to view the content of this email\, please","\>(safe )?unsubscribe( here)?\</a\>","If you do not wish to receive further communications like this\, please","\<img height\="?1"? width\="?1"? sr\c=.?http\://","To stop receiving these+emails\:http\://","To unsubscribe from \w+ (e\-?letter|e?-?mail|newsletter)","no longer (wish )?(to )?(be sent|receive) w+ email","If you are unable to view the content of this email\, please click here","To ensure you receive (your daily deals|our e-?mails)\, add","If you no longer wish to receive these emails","to change your (subscription preferences|preferences or unsubscribe)","click (here to|the) unsubscribe"... -SetSCL 6
```

<span data-ttu-id="dbe70-154">Cet exemple crée une règle nommée « filtrage des courriers électroniques en bloc » qui utilise la même liste de mots que précédemment dans la rubrique pour définir les messages comme **courrier indésirable à niveau de confiance élevé**.</span><span class="sxs-lookup"><span data-stu-id="dbe70-154">This example creates a new rule named "Bulk email filtering - Words" that uses the same list of words from earlier in the topic to set messages as **High confidence spam**.</span></span>

```powershell
New-TransportRule -Name "Bulk email filtering - Words" -SubjectOrBodyContainsWords "to change your preferences or unsubscribe","Modify email preferences or unsubscribe","This is a promotional email","You are receiving this email because you requested a subscription","click here to unsubscribe","You have received this email because you are subscribed","If you no longer wish to receive our email newsletter","to unsubscribe from this newsletter","If you have trouble viewing this email","This is an advertisement","you would like to unsubscribe or change your","view this email as a webpage","You are receiving this email because you are subscribed" -SetSCL 9
```

<span data-ttu-id="dbe70-155">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/new-transportrule).</span><span class="sxs-lookup"><span data-stu-id="dbe70-155">For detailed syntax and parameter information, see [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/new-transportrule).</span></span>

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="dbe70-156">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="dbe70-156">How do you know this worked?</span></span>

<span data-ttu-id="dbe70-157">Pour vérifier que vous avez configuré les règles de flux de messagerie pour filtrer les messages électroniques en masse, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbe70-157">To verify that you've configured mail flow rules to filter bulk email, do any of the following steps:</span></span>

- <span data-ttu-id="dbe70-158">Dans le centre d’administration Exchange, accédez à règles de **flux de messagerie** \> **Rules** \> Sélectionnez la règle \> , cliquez sur **modifier** ![ l’icône d’édition ](../../media/ITPro-EAC-EditIcon.png) et vérifiez les paramètres.</span><span class="sxs-lookup"><span data-stu-id="dbe70-158">In the EAC, go to **Mail flow** \> **Rules** \> select the rule \> click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png), and verify the settings.</span></span>

- <span data-ttu-id="dbe70-159">Dans PowerShell, remplacez \<Rule Name\> par le nom de la règle, puis exécutez la commande suivante pour vérifier les paramètres :</span><span class="sxs-lookup"><span data-stu-id="dbe70-159">In PowerShell, replace \<Rule Name\> with the name of the rule, and run the following command to verify the settings:</span></span>

  ```powershell
  Get-TransportRule -Identity "<Rule Name>" | Format-List
  ```

- <span data-ttu-id="dbe70-160">À partir d’un compte externe, envoyez un message de test à un destinataire affecté qui contient l’une des expressions ou des modèles de texte, puis vérifiez les résultats.</span><span class="sxs-lookup"><span data-stu-id="dbe70-160">From an external account, send a test messages to an affected recipient that contains one of the phrases or text patterns, and verify the results.</span></span>
