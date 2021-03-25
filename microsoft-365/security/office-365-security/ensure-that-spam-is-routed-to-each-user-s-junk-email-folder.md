---
title: Configurer EOP pour le courrier indésirable dans les environnements hybrides
f1.keywords:
- NOCSH
ms.author: chrisda
author: MSFTTracyP
manager: chrisda
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à router le courrier indésirable vers les dossiers courrier indésirable de l’utilisateur dans un environnement hybride Exchange Online Protection.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: ae6ee551d04b242891c9638d6d99d79240480d27
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204259"
---
# <a name="configure-standalone-eop-to-deliver-spam-to-the-junk-email-folder-in-hybrid-environments"></a><span data-ttu-id="c092a-103">Configurer EOP autonome pour remettre le courrier indésirable dans le dossier Courrier indésirable dans les environnements hybrides</span><span class="sxs-lookup"><span data-stu-id="c092a-103">Configure standalone EOP to deliver spam to the Junk Email folder in hybrid environments</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="c092a-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c092a-104">**Applies to**</span></span>
-  [<span data-ttu-id="c092a-105">Exchange Online Protection autonome</span><span class="sxs-lookup"><span data-stu-id="c092a-105">Exchange Online Protection standalone</span></span>](exchange-online-protection-overview.md)

> [!IMPORTANT]
> <span data-ttu-id="c092a-106">Cette rubrique s’adresse uniquement aux clients EOP autonomes dans les environnements hybrides.</span><span class="sxs-lookup"><span data-stu-id="c092a-106">This topic is only for standalone EOP customers in hybrid environments.</span></span> <span data-ttu-id="c092a-107">Cette rubrique ne s’applique pas aux clients Microsoft 365 ayant des boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c092a-107">This topic does not apply to Microsoft 365 customers with Exchange Online mailboxes.</span></span>

<span data-ttu-id="c092a-108">Si vous êtes un client Exchange Online Protection (EOP) autonome dans un environnement hybride, vous devez configurer votre organisation Exchange sur site pour reconnaître et traduire les verdicts de filtrage du courrier indésirable d’EOP, afin que la règle de courrier indésirable dans la boîte aux lettres sur site puisse déplacer les messages vers le dossier Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c092a-108">If you're a standalone Exchange Online Protection (EOP) customer in a hybrid environment, you need to configure your on-premises Exchange organization to recognize and translate the spam filtering verdicts of EOP, so the junk email rule in the on-premises mailbox can move messages to the Junk Email folder.</span></span>

<span data-ttu-id="c092a-109">Plus précisément, vous devez créer des règles de flux de messagerie (également appelées règles de transport) dans votre organisation Exchange sur site avec des conditions qui recherchent des messages avec l’un des en-têtes et valeurs EOP anti-courrier indésirable suivants, ainsi que des actions qui définissent le niveau de confiance du courrier indésirable (SCL) de ces messages sur 6 :</span><span class="sxs-lookup"><span data-stu-id="c092a-109">Specifically, you need to create mail flow rules (also known as transport rules) in your on-premises Exchange organization with conditions that find messages with any of the following EOP anti-spam headers and values, and actions that set the spam confidence level (SCL) of those messages to 6:</span></span>

- <span data-ttu-id="c092a-110">`X-Forefront-Antispam-Report: SFV:SPM` (message marqué comme courrier indésirable par filtrage du courrier indésirable)</span><span class="sxs-lookup"><span data-stu-id="c092a-110">`X-Forefront-Antispam-Report: SFV:SPM` (message marked as spam by spam filtering)</span></span>

- <span data-ttu-id="c092a-111">`X-Forefront-Antispam-Report: SFV:SKS` (message marqué comme courrier indésirable par des règles de flux de messagerie dans EOP avant le filtrage du courrier indésirable)</span><span class="sxs-lookup"><span data-stu-id="c092a-111">`X-Forefront-Antispam-Report: SFV:SKS` (message marked as spam by mail flow rules in EOP before spam filtering)</span></span>

- <span data-ttu-id="c092a-112">`X-Forefront-Antispam-Report: SFV:SKB` (message marqué comme courrier indésirable par filtrage du courrier indésirable en raison de l’adresse de messagerie ou du domaine de messagerie de l’expéditeur se trouver dans la liste des expéditeurs bloqués ou la liste des domaines bloqués dans EOP)</span><span class="sxs-lookup"><span data-stu-id="c092a-112">`X-Forefront-Antispam-Report: SFV:SKB` (message marked as spam by spam filtering due to the sender's email address or email domain being in the blocked sender list or the blocked domain list in EOP)</span></span>

<span data-ttu-id="c092a-113">Pour plus d’informations sur ces valeurs d’en-tête, consultez les [en-têtes de message anti-courrier indésirable.](anti-spam-message-headers.md)</span><span class="sxs-lookup"><span data-stu-id="c092a-113">For more information about these header values, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span>

<span data-ttu-id="c092a-114">Cette rubrique décrit comment créer ces règles de flux de messagerie dans le Centre d’administration Exchange (EAC) et dans l’Environnement de ligne de bord Exchange Management Shell (Exchange PowerShell) dans l’organisation Exchange sur site.</span><span class="sxs-lookup"><span data-stu-id="c092a-114">This topic describes how to create these mail flow rules the Exchange admin center (EAC) and in the Exchange Management Shell (Exchange PowerShell) in the on-premises Exchange organization.</span></span>

> [!TIP]
> <span data-ttu-id="c092a-115">Au lieu de remettre les messages dans le dossier Courrier indésirable de l’utilisateur local, vous pouvez configurer des stratégies anti-courrier indésirable dans EOP pour mettre en quarantaine les messages indésirables dans EOP.</span><span class="sxs-lookup"><span data-stu-id="c092a-115">Instead of delivering the messages to the on-premises user's Junk Email folder, you can configure anti-spam policies in EOP to quarantine spam messages in EOP.</span></span> <span data-ttu-id="c092a-116">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c092a-116">For more information, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="c092a-117">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="c092a-117">What do you need to know before you begin?</span></span>

- <span data-ttu-id="c092a-118">Des autorisations doivent vous être attribuées dans l’environnement Exchange local avant de pouvoir suivre ces procédures.</span><span class="sxs-lookup"><span data-stu-id="c092a-118">You need to be assigned permissions in the on-premises Exchange environment before you can do these procedures.</span></span> <span data-ttu-id="c092a-119">Plus précisément, vous devez avoir le rôle Règles de **transport,** qui est  attribué aux rôles Gestion de l’organisation, Gestion de la conformité et Gestion des enregistrements par défaut. </span><span class="sxs-lookup"><span data-stu-id="c092a-119">Specifically, you need to be assigned the **Transport Rules** role, which is assigned to the **Organization Management**, **Compliance Management**, and **Records Management** roles by default.</span></span> <span data-ttu-id="c092a-120">Pour plus d’informations, voir [Ajouter des membres à un groupe de rôles.](/Exchange/permissions/role-group-members#add-members-to-a-role-group)</span><span class="sxs-lookup"><span data-stu-id="c092a-120">For more information, see [Add members to a role group](/Exchange/permissions/role-group-members#add-members-to-a-role-group).</span></span>

- <span data-ttu-id="c092a-121">Si et quand un message est remis au dossier Courrier indésirable dans une organisation Exchange sur site est contrôlé par une combinaison des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="c092a-121">If and when a message is delivered to the Junk Email folder in an on-premises Exchange organization is controlled by a combination of the following settings:</span></span>

  - <span data-ttu-id="c092a-122">Valeur _du paramètre SCLJunkThreshold_ sur la cmdlet [Set-OrganizationConfig](/powershell/module/exchange/set-organizationconfig) dans l’Environnement de travail Exchange Management Shell.</span><span class="sxs-lookup"><span data-stu-id="c092a-122">The _SCLJunkThreshold_ parameter value on the [Set-OrganizationConfig](/powershell/module/exchange/set-organizationconfig) cmdlet in the Exchange Management Shell.</span></span> <span data-ttu-id="c092a-123">La valeur par défaut est 4, ce qui signifie qu’un SCL de 5 ou plus doit remettre le message dans le dossier Courrier indésirable de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c092a-123">The default value is 4, which means an SCL of 5 or higher should deliver the message to the user's Junk email folder.</span></span>

  - <span data-ttu-id="c092a-124">Valeur _du paramètre SCLJunkThreshold_ sur la cmdlet [Set-Mailbox](/powershell/module/exchange/set-mailbox) dans l’Environnement de travail Exchange Management Shell.</span><span class="sxs-lookup"><span data-stu-id="c092a-124">The _SCLJunkThreshold_ parameter value on the [Set-Mailbox](/powershell/module/exchange/set-mailbox) cmdlet in the Exchange Management Shell.</span></span> <span data-ttu-id="c092a-125">La valeur par défaut est vide ($null), ce qui signifie que le paramètre de l’organisation est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c092a-125">The default value is blank ($null), which means the organization setting is used.</span></span>

  <span data-ttu-id="c092a-126">Pour plus d’informations, consultez les seuils de seuil de confiance du courrier indésirable [Exchange (SCL).](/Exchange/antispam-and-antimalware/antispam-protection/scl)</span><span class="sxs-lookup"><span data-stu-id="c092a-126">For details, see [Exchange spam confidence level (SCL) thresholds](/Exchange/antispam-and-antimalware/antispam-protection/scl).</span></span>

  - <span data-ttu-id="c092a-127">Si la règle de courrier indésirable est activée sur la boîte aux lettres (la valeur du paramètre _Enabled_ est $true sur la cmdlet [Set-MailboxJunkEmailConfiguration](/powershell/module/exchange/set-mailboxjunkemailconfiguration) dans l’Environnement de messagerie Exchange Management Shell).</span><span class="sxs-lookup"><span data-stu-id="c092a-127">Whether the junk email rule is enabled on the mailbox (the _Enabled_ parameter value is $true on the [Set-MailboxJunkEmailConfiguration](/powershell/module/exchange/set-mailboxjunkemailconfiguration) cmdlet in the Exchange Management Shell).</span></span> <span data-ttu-id="c092a-128">C’est la règle de courrier indésirable qui déplace réellement le message vers le dossier Courrier indésirable après la remise.</span><span class="sxs-lookup"><span data-stu-id="c092a-128">It's the junk email rule that actually moves the message to the Junk Email folder after delivery.</span></span> <span data-ttu-id="c092a-129">Par défaut, la règle de courrier indésirable est activée sur les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c092a-129">By default, the junk email rule is enabled on mailboxes.</span></span> <span data-ttu-id="c092a-130">Pour plus d’informations, consultez la rubrique [Configure Exchange antispam settings on mailboxes](/Exchange/antispam-and-antimalware/antispam-protection/configure-antispam-settings).</span><span class="sxs-lookup"><span data-stu-id="c092a-130">For more information, see [Configure Exchange antispam settings on mailboxes](/Exchange/antispam-and-antimalware/antispam-protection/configure-antispam-settings).</span></span>

- <span data-ttu-id="c092a-131">Pour ouvrir le CENTRE d’administration Exchange sur une Exchange Server, consultez le [Centre d’administration Exchange dans Exchange Server](/Exchange/architecture/client-access/exchange-admin-center).</span><span class="sxs-lookup"><span data-stu-id="c092a-131">To open the EAC on an Exchange Server, see [Exchange admin center in Exchange Server](/Exchange/architecture/client-access/exchange-admin-center).</span></span> <span data-ttu-id="c092a-132">Pour ouvrir l’environnement de ligne de commande Exchange Management Shell, consultez [Ouvrir l’environnement de ligne de commande Exchange Management Shell](/powershell/exchange/open-the-exchange-management-shell).</span><span class="sxs-lookup"><span data-stu-id="c092a-132">To open the Exchange Management Shell, see [Open the Exchange Management Shell](/powershell/exchange/open-the-exchange-management-shell).</span></span>

- <span data-ttu-id="c092a-133">Pour plus d’informations sur les règles de flux de messagerie dans Exchange local, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c092a-133">For more information about mail flow rules in on-premises Exchange, see the following topics:</span></span>

  - [<span data-ttu-id="c092a-134">Règles de flux de messagerie dans Exchange Server</span><span class="sxs-lookup"><span data-stu-id="c092a-134">Mail flow rules in Exchange Server</span></span>](/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rules)

  - [<span data-ttu-id="c092a-135">Conditions et exceptions de règle de flux de messagerie (prédicats) dans Exchange Server</span><span class="sxs-lookup"><span data-stu-id="c092a-135">Mail flow rule conditions and exceptions (predicates) in Exchange Server</span></span>](/Exchange/policy-and-compliance/mail-flow-rules/conditions-and-exceptions)

  - [<span data-ttu-id="c092a-136">Actions de règle de flux de messagerie dans Exchange Server</span><span class="sxs-lookup"><span data-stu-id="c092a-136">Mail flow rule actions in Exchange Server</span></span>](/Exchange/policy-and-compliance/mail-flow-rules/actions)

## <a name="use-the-eac-to-create-mail-flow-rules-that-set-the-scl-of-eop-spam-messages"></a><span data-ttu-id="c092a-137">Utiliser le CAE pour créer des règles de flux de messagerie qui définissent le SCL des messages indésirables EOP</span><span class="sxs-lookup"><span data-stu-id="c092a-137">Use the EAC to create mail flow rules that set the SCL of EOP spam messages</span></span>

1. <span data-ttu-id="c092a-138">Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="c092a-138">In the EAC, go to **Mail flow** \> **Rules**.</span></span>

2. <span data-ttu-id="c092a-139">Cliquez **sur** Ajouter une icône, puis sélectionnez Créer une règle ![ dans la ](../../media/ITPro-EAC-AddIcon.png) drop-down qui s’affiche. </span><span class="sxs-lookup"><span data-stu-id="c092a-139">Click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png) and select **Create a new rule** in the drop-down that appears.</span></span>

3. <span data-ttu-id="c092a-140">Dans la page **Nouvelle règle** qui s'ouvre, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="c092a-140">In the **New rule** page that opens, configure the following settings:</span></span>

   - <span data-ttu-id="c092a-141">**Nom**: entrez un nom unique et descriptif pour la règle.</span><span class="sxs-lookup"><span data-stu-id="c092a-141">**Name**: Enter a unique, descriptive name for the rule.</span></span> <span data-ttu-id="c092a-142">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c092a-142">For example:</span></span>

     - <span data-ttu-id="c092a-143">EOP SFV:SPM vers SCL 6</span><span class="sxs-lookup"><span data-stu-id="c092a-143">EOP SFV:SPM to SCL 6</span></span>

     - <span data-ttu-id="c092a-144">EOP SFV:SKS vers SCL 6</span><span class="sxs-lookup"><span data-stu-id="c092a-144">EOP SFV:SKS to SCL 6</span></span>

     - <span data-ttu-id="c092a-145">EOP SFV:SKB vers SCL 6</span><span class="sxs-lookup"><span data-stu-id="c092a-145">EOP SFV:SKB to SCL 6</span></span>

   - <span data-ttu-id="c092a-146">Cliquez sur **Autres options**.</span><span class="sxs-lookup"><span data-stu-id="c092a-146">Click **More Options**.</span></span>

   - <span data-ttu-id="c092a-147">**Appliquez cette règle si**: **Sélectionnez un en-tête de message** \> **inclut l’un de ces mots.**</span><span class="sxs-lookup"><span data-stu-id="c092a-147">**Apply this rule if**: Select **A message header** \> **includes any of these words**.</span></span>

     <span data-ttu-id="c092a-148">Dans **l’en-tête** Entrée de texte inclut la phrase Entrée de mots qui s’affiche, faites les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c092a-148">In the **Enter text header includes Enter words** sentence that appears, do the following steps:</span></span>

     - <span data-ttu-id="c092a-149">Cliquez **sur Entrée de texte**.</span><span class="sxs-lookup"><span data-stu-id="c092a-149">Click **Enter text**.</span></span> <span data-ttu-id="c092a-150">Dans la **boîte de dialogue** Spécifier le nom d’en-tête qui s’affiche, entrez **X-Forefront-Antispam-Report,** puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c092a-150">In the **Specify header name** dialog that appears, enter **X-Forefront-Antispam-Report** and then click **OK**.</span></span>

     - <span data-ttu-id="c092a-151">Cliquez **sur Entrer des mots.**</span><span class="sxs-lookup"><span data-stu-id="c092a-151">Click  **Enter words**.</span></span> <span data-ttu-id="c092a-152">Dans la boîte de dialogue Spécifier des mots ou des expressions qui s’affiche, entrez l’une des **valeurs** d’en-tête de courrier indésirable EOP (**SFV:SPM**, **SFV:SKS** ou **SFV:SKB**), cliquez sur Ajouter une  ![ icône, puis cliquez sur ](../../media/ITPro-EAC-AddIcon.png) **OK**.</span><span class="sxs-lookup"><span data-stu-id="c092a-152">In the **Specify words or phrases** dialog that appears, enter one of the EOP spam header values (**SFV:SPM**, **SFV:SKS**, or **SFV:SKB**), click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png), and then click **OK**.</span></span>

   - <span data-ttu-id="c092a-153">**Pour ce faire,** **sélectionnez Modifier les propriétés du message** Définir le niveau de \> **confiance du courrier indésirable (SCL).**</span><span class="sxs-lookup"><span data-stu-id="c092a-153">**Do the following**: Select **Modify the message properties** \> **Set the spam confidence level (SCL)**.</span></span>

     <span data-ttu-id="c092a-154">Dans la **boîte de dialogue Spécifier le SCL** qui s’affiche, **sélectionnez 6** (la valeur par défaut est **5**).</span><span class="sxs-lookup"><span data-stu-id="c092a-154">In the **Specify SCL** dialog that appears, select **6** (the default value is **5**).</span></span>

   <span data-ttu-id="c092a-155">Lorsque vous avez terminé, cliquez sur **Enregistrer**</span><span class="sxs-lookup"><span data-stu-id="c092a-155">When you're finished, click **Save**</span></span>

<span data-ttu-id="c092a-156">Répétez ces étapes pour les autres valeurs de verdict de courrier indésirable EOP (**SFV:SPM,** **SFV:SKS** ou **SFV:SKB**).</span><span class="sxs-lookup"><span data-stu-id="c092a-156">Repeat these steps for the remaining EOP spam verdict values (**SFV:SPM**, **SFV:SKS**, or **SFV:SKB**).</span></span>

## <a name="use-the-exchange-management-shell-to-create-mail-flow-rules-that-set-the-scl-of-eop-spam-messages"></a><span data-ttu-id="c092a-157">Utiliser l’Environnement de travail Exchange Management Shell pour créer des règles de flux de messagerie qui définissent le SCL des messages indésirables EOP</span><span class="sxs-lookup"><span data-stu-id="c092a-157">Use the Exchange Management Shell to create mail flow rules that set the SCL of EOP spam messages</span></span>

<span data-ttu-id="c092a-158">Utilisez la syntaxe suivante pour créer les trois règles de flux de messagerie :</span><span class="sxs-lookup"><span data-stu-id="c092a-158">Use the following syntax to create the three mail flow rules:</span></span>

```Powershell
New-TransportRule -Name "<RuleName>" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "<EOPSpamFilteringVerdict>" -SetSCL 6
```

<span data-ttu-id="c092a-159">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c092a-159">For example:</span></span>

```Powershell
New-TransportRule -Name "EOP SFV:SPM to SCL 6" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
```

```Powershell
New-TransportRule -Name "EOP SFV:SKS to SCL 6" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
```

```Powershell
New-TransportRule -Name "EOP SFV:SKB to SCL 6" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
```

<span data-ttu-id="c092a-160">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TransportRule](/powershell/module/exchange/new-transportrule).</span><span class="sxs-lookup"><span data-stu-id="c092a-160">For detailed syntax and parameter information, see [New-TransportRule](/powershell/module/exchange/new-transportrule).</span></span>

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="c092a-161">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="c092a-161">How do you know this worked?</span></span>

<span data-ttu-id="c092a-162">Pour vérifier que vous avez correctement configuré EOP autonome pour remettre le courrier indésirable dans le dossier Courrier indésirable dans un environnement hybride, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c092a-162">To verify that you've successfully configured standalone EOP to deliver spam to the Junk Email folder in hybrid environment, do any of the following steps:</span></span>

- <span data-ttu-id="c092a-163">Dans le EAC, sélectionnez règles de **flux** de messagerie, sélectionnez la règle, puis cliquez sur Modifier l’icône \> Modifier pour vérifier les  ![ ](../../media/ITPro-EAC-EditIcon.png) paramètres.</span><span class="sxs-lookup"><span data-stu-id="c092a-163">In the EAC, go to **Mail flow** \> **Rules**, select the rule, and then click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png) to verify the settings.</span></span>

- <span data-ttu-id="c092a-164">Dans l’Environnement de commande Exchange Management Shell, remplacez-le par le nom de la règle de flux de messagerie, puis rulez la commande suivante pour \<RuleName\> vérifier les paramètres :</span><span class="sxs-lookup"><span data-stu-id="c092a-164">In the Exchange Management Shell, replace \<RuleName\> with the name of the mail flow rule, and rul the following command to verify the settings:</span></span>

  ```powershell
  Get-TransportRule -Identity "<RuleName>" | Format-List
  ```

- <span data-ttu-id="c092a-165">Dans un système de courrier externe qui **n’analyse** pas les messages sortants à la recherche de courrier indésirable, envoyez un test générique pour le message GTUBE (Unsolicited Bulk Email) à un destinataire affecté et confirmez qu’il est remis à son dossier Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c092a-165">In an external email system **that doesn't scan outbound messages for spam**, send a Generic Test for Unsolicited Bulk Email (GTUBE) message to an affected recipient, and confirm that it's delivered to their Junk Email folder.</span></span> <span data-ttu-id="c092a-166">Un message GTUBE est semblable au fichier texte EICAR (European Institute for Computer Virus Research) pour tester les paramètres des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="c092a-166">A GTUBE message is similar to the European Institute for Computer Antivirus Research (EICAR) text file for testing malware settings.</span></span>

  <span data-ttu-id="c092a-167">Pour envoyer un message GTUBE, incluez le texte suivant dans le corps d’un message électronique sur une seule ligne, sans espace ni coupure de ligne :</span><span class="sxs-lookup"><span data-stu-id="c092a-167">To send a GTUBE message, include the following text in the body of an email message on a single line, without any spaces or line breaks:</span></span>

  ```text
  XJS*C4JDBQADN1.NSBN3*2IDNEN*GTUBE-STANDARD-ANTI-UBE-TEST-EMAIL*C.34X
  ```