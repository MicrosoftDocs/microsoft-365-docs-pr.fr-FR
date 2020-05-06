---
title: Configuration d’EOP pour le courrier indésirable dans les environnements hybrides
f1.keywords:
- NOCSH
ms.author: chrisda
author: MSFTTracyP
manager: chrisda
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à acheminer le courrier indésirable vers les dossiers de courrier indésirable de l’utilisateur dans un environnement hybride Exchange Online Protection.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 14193fecf90a6f2ddde05fbfdaded0ff2bcb5875
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44036571"
---
# <a name="configure-standalone-eop-to-deliver-spam-to-the-junk-email-folder-in-hybrid-environments"></a><span data-ttu-id="54cd0-103">Configurer EOP autonome pour envoyer du courrier indésirable dans le dossier courrier indésirable dans des environnements hybrides</span><span class="sxs-lookup"><span data-stu-id="54cd0-103">Configure standalone EOP to deliver spam to the Junk Email folder in hybrid environments</span></span>

> [!IMPORTANT]
> <span data-ttu-id="54cd0-104">Cette rubrique s’utilise uniquement pour les clients EOP autonomes dans les environnements hybrides.</span><span class="sxs-lookup"><span data-stu-id="54cd0-104">This topic is only for standalone EOP customers in hybrid environments.</span></span> <span data-ttu-id="54cd0-105">Cette rubrique ne s’applique pas aux clients Microsoft 365 avec des boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="54cd0-105">This topic does not apply to Microsoft 365 customers with Exchange Online mailboxes.</span></span>

<span data-ttu-id="54cd0-106">Si vous êtes un client Exchange Online Protection (EOP) autonome dans un environnement hybride, vous devez configurer votre organisation Exchange locale pour qu’elle reconnaisse et traduise les verdicts de filtrage du courrier indésirable d’EOP, de sorte que la règle de courrier indésirable dans la boîte aux lettres locale puisse déplacer des messages vers le dossier courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="54cd0-106">If you're a standalone Exchange Online Protection (EOP) customer in a hybrid environment, you need to configure your on-premises Exchange organization to recognize and translate the spam filtering verdicts of EOP, so the junk email rule in the on-premises mailbox can move messages to the Junk Email folder.</span></span>

<span data-ttu-id="54cd0-107">Plus précisément, vous devez créer des règles de flux de messagerie (également appelées règles de transport) dans votre organisation Exchange locale avec des conditions qui recherchent les messages avec l’un des en-têtes et valeurs de blocage du courrier indésirable EOP suivants, ainsi que les actions qui définissent le seuil de probabilité de courrier indésirable (SCL) de ces messages à 6 :</span><span class="sxs-lookup"><span data-stu-id="54cd0-107">Specifically, you need to create mail flow rules (also known as transport rules) in your on-premises Exchange organization with conditions that find messages with any of the following EOP anti-spam headers and values, and actions that set the spam confidence level (SCL) of those messages to 6:</span></span>

- <span data-ttu-id="54cd0-108">`X-Forefront-Antispam-Report: SFV:SPM`(message marqué comme courrier indésirable par le filtrage du courrier indésirable)</span><span class="sxs-lookup"><span data-stu-id="54cd0-108">`X-Forefront-Antispam-Report: SFV:SPM` (message marked as spam by spam filtering)</span></span>

- <span data-ttu-id="54cd0-109">`X-Forefront-Antispam-Report: SFV:SKS`(message marqué comme courrier indésirable par les règles de flux de messagerie dans EOP avant le filtrage du courrier indésirable)</span><span class="sxs-lookup"><span data-stu-id="54cd0-109">`X-Forefront-Antispam-Report: SFV:SKS` (message marked as spam by mail flow rules in EOP before spam filtering)</span></span>

- <span data-ttu-id="54cd0-110">`X-Forefront-Antispam-Report: SFV:SKB`(message marqué comme courrier indésirable par filtrage du courrier indésirable, car l’adresse de messagerie ou le domaine de messagerie de l’expéditeur se trouve dans la liste des expéditeurs bloqués ou dans la liste des domaines bloqués dans EOP)</span><span class="sxs-lookup"><span data-stu-id="54cd0-110">`X-Forefront-Antispam-Report: SFV:SKB` (message marked as spam by spam filtering due to the sender's email address or email domain being in the blocked sender list or the blocked domain list in EOP)</span></span>

<span data-ttu-id="54cd0-111">Pour plus d’informations sur ces valeurs d’en-tête, consultez la rubrique [anti-spam message headers](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="54cd0-111">For more information about these header values, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span>

<span data-ttu-id="54cd0-112">Cette rubrique décrit comment créer ces règles de flux de messagerie le centre d’administration Exchange et l’environnement de commande Exchange Management Shell (Exchange PowerShell) dans l’organisation Exchange locale.</span><span class="sxs-lookup"><span data-stu-id="54cd0-112">This topic describes how to create these mail flow rules the Exchange admin center (EAC) and in the Exchange Management Shell (Exchange PowerShell) in the on-premises Exchange organization.</span></span>

> [!TIP]
> <span data-ttu-id="54cd0-113">Au lieu de transmettre les messages au dossier de courrier indésirable de l’utilisateur local, vous pouvez configurer des stratégies de blocage du courrier indésirable dans EOP pour mettre en quarantaine les messages de courrier indésirable dans EOP.</span><span class="sxs-lookup"><span data-stu-id="54cd0-113">Instead of delivering the messages to the on-premises user's Junk Email folder, you can configure anti-spam policies in EOP to quarantine spam messages in EOP.</span></span> <span data-ttu-id="54cd0-114">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans Office 365](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="54cd0-114">For more information, see [Configure anti-spam policies in Office 365](configure-your-spam-filter-policies.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="54cd0-115">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="54cd0-115">What do you need to know before you begin?</span></span>

- <span data-ttu-id="54cd0-116">Vous devez disposer d’autorisations dans l’environnement Exchange local avant de pouvoir effectuer ces procédures.</span><span class="sxs-lookup"><span data-stu-id="54cd0-116">You need to be assigned permissions in the on-premises Exchange environment before you can do these procedures.</span></span> <span data-ttu-id="54cd0-117">Plus précisément, vous devez disposer du rôle **de règles de transport** , qui est affecté aux rôles de gestion de l' **organisation**, de gestion de **la conformité**et de **gestion des enregistrements** par défaut.</span><span class="sxs-lookup"><span data-stu-id="54cd0-117">Specifically, you need to be assigned the **Transport Rules** role, which is assigned to the **Organization Management**, **Compliance Management**, and **Records Management** roles by default.</span></span> <span data-ttu-id="54cd0-118">Pour plus d’informations, consultez [la rubrique ajouter des membres à un groupe de rôles](https://docs.microsoft.com/Exchange/permissions/role-group-members?view=exchserver-2019#add-members-to-a-role-group).</span><span class="sxs-lookup"><span data-stu-id="54cd0-118">For more information, see [Add members to a role group](https://docs.microsoft.com/Exchange/permissions/role-group-members?view=exchserver-2019#add-members-to-a-role-group).</span></span>

- <span data-ttu-id="54cd0-119">Si et quand un message est remis dans le dossier courrier indésirable d’une organisation Exchange locale est contrôlé par une combinaison des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="54cd0-119">If and when a message is delivered to the Junk Email folder in an on-premises Exchange organization is controlled by a combination of the following settings:</span></span>

  - <span data-ttu-id="54cd0-120">Valeur du paramètre _SCLJunkThreshold_ sur la cmdlet [Set-OrganizationConfig](https://docs.microsoft.com/powershell/module/exchange/organization/set-organizationconfig) dans l’environnement de commande Exchange Management Shell.</span><span class="sxs-lookup"><span data-stu-id="54cd0-120">The _SCLJunkThreshold_ parameter value on the [Set-OrganizationConfig](https://docs.microsoft.com/powershell/module/exchange/organization/set-organizationconfig) cmdlet in the Exchange Management Shell.</span></span> <span data-ttu-id="54cd0-121">La valeur par défaut est 4, ce qui signifie qu’une valeur SCL supérieure ou égale à 5 doit transmettre le message au dossier de courrier indésirable de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="54cd0-121">The default value is 4, which means an SCL of 5 or higher should deliver the message to the user's Junk email folder.</span></span>

  - <span data-ttu-id="54cd0-122">Valeur du paramètre _SCLJunkThreshold_ sur la cmdlet [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox) dans l’environnement de commande Exchange Management Shell.</span><span class="sxs-lookup"><span data-stu-id="54cd0-122">The _SCLJunkThreshold_ parameter value on the [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox) cmdlet in the Exchange Management Shell.</span></span> <span data-ttu-id="54cd0-123">La valeur par défaut est vide ($null), ce qui signifie que le paramètre de l’organisation est utilisé.</span><span class="sxs-lookup"><span data-stu-id="54cd0-123">The default value is blank ($null), which means the organization setting is used.</span></span>

  <span data-ttu-id="54cd0-124">Pour plus d’informations, consultez la rubrique [seuils de probabilité de courrier indésirable Exchange](https://docs.microsoft.com/Exchange/antispam-and-antimalware/antispam-protection/scl).</span><span class="sxs-lookup"><span data-stu-id="54cd0-124">For details, see [Exchange spam confidence level (SCL) thresholds](https://docs.microsoft.com/Exchange/antispam-and-antimalware/antispam-protection/scl).</span></span>

  - <span data-ttu-id="54cd0-125">Si la règle de courrier indésirable est activée sur la boîte aux lettres (la valeur du paramètre _Enabled_ est $true sur la cmdlet [Set-MailboxJunkEmailConfiguration](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-mailboxjunkemailconfiguration) dans l’environnement de commande Exchange Management Shell).</span><span class="sxs-lookup"><span data-stu-id="54cd0-125">Whether the junk email rule is enabled on the mailbox (the _Enabled_ parameter value is $true on the [Set-MailboxJunkEmailConfiguration](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-mailboxjunkemailconfiguration) cmdlet in the Exchange Management Shell).</span></span> <span data-ttu-id="54cd0-126">Il s’agit de la règle de courrier indésirable qui déplace le message vers le dossier courrier indésirable après la remise.</span><span class="sxs-lookup"><span data-stu-id="54cd0-126">It's the junk email rule that actually moves the message to the Junk Email folder after delivery.</span></span> <span data-ttu-id="54cd0-127">Par défaut, la règle de courrier indésirable est activée sur les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="54cd0-127">By default, the junk email rule is enabled on mailboxes.</span></span> <span data-ttu-id="54cd0-128">Pour plus d’informations, consultez la rubrique [Configure Exchange antispam settings on mailboxes](https://docs.microsoft.com/Exchange/antispam-and-antimalware/antispam-protection/configure-antispam-settings).</span><span class="sxs-lookup"><span data-stu-id="54cd0-128">For more information, see [Configure Exchange antispam settings on mailboxes](https://docs.microsoft.com/Exchange/antispam-and-antimalware/antispam-protection/configure-antispam-settings).</span></span>
  
- <span data-ttu-id="54cd0-129">Pour ouvrir le centre d’administration Exchange sur un serveur Exchange, consultez la rubrique [Exchange Admin Center in Exchange Server](https://docs.microsoft.com/Exchange/architecture/client-access/exchange-admin-center).</span><span class="sxs-lookup"><span data-stu-id="54cd0-129">To open the EAC on an Exchange Server, see [Exchange admin center in Exchange Server](https://docs.microsoft.com/Exchange/architecture/client-access/exchange-admin-center).</span></span> <span data-ttu-id="54cd0-130">Pour ouvrir l’environnement de commande Exchange Management [https://docs.microsoft.com/powershell/exchange/exchange-server/open-the-exchange-management-shell](https://docs.microsoft.com/powershell/exchange/exchange-server/open-the-exchange-management-shell)Shell, reportez-vous à.</span><span class="sxs-lookup"><span data-stu-id="54cd0-130">To open the Exchange Management Shell, see [https://docs.microsoft.com/powershell/exchange/exchange-server/open-the-exchange-management-shell](https://docs.microsoft.com/powershell/exchange/exchange-server/open-the-exchange-management-shell).</span></span>

- <span data-ttu-id="54cd0-131">Pour plus d’informations sur les règles de flux de messagerie dans Exchange sur site, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="54cd0-131">For more information about mail flow rules in on-premises Exchange, see the following topics:</span></span>

  - [<span data-ttu-id="54cd0-132">Règles de flux de messagerie dans Exchange Server</span><span class="sxs-lookup"><span data-stu-id="54cd0-132">Mail flow rules in Exchange Server</span></span>](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rules)

  - [<span data-ttu-id="54cd0-133">Conditions de règle de flux de messagerie et exceptions (prédicats) dans Exchange Server</span><span class="sxs-lookup"><span data-stu-id="54cd0-133">Mail flow rule conditions and exceptions (predicates) in Exchange Server</span></span>](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/conditions-and-exceptions)

  - [<span data-ttu-id="54cd0-134">Actions de règle de flux de messagerie dans Exchange Server</span><span class="sxs-lookup"><span data-stu-id="54cd0-134">Mail flow rule actions in Exchange Server</span></span>](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/actions)

## <a name="use-the-eac-to-create-mail-flow-rules-that-set-the-scl-of-eop-spam-messages"></a><span data-ttu-id="54cd0-135">Utiliser le centre d’administration Exchange pour créer des règles de flux de messagerie qui définissent la valeur SCL des messages de courrier indésirable EOP</span><span class="sxs-lookup"><span data-stu-id="54cd0-135">Use the EAC to create mail flow rules that set the SCL of EOP spam messages</span></span>

1. <span data-ttu-id="54cd0-136">Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="54cd0-136">In the EAC, go to **Mail flow** \> **Rules**.</span></span>

2. <span data-ttu-id="54cd0-137">Cliquez sur **Ajouter** ![une](../../media/ITPro-EAC-AddIcon.png) icône et sélectionnez **créer une nouvelle règle** dans la liste déroulante qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="54cd0-137">Click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png) and select **Create a new rule** in the drop-down that appears.</span></span>

3. <span data-ttu-id="54cd0-138">Dans la page **Nouvelle règle** qui s'ouvre, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="54cd0-138">In the **New rule** page that opens, configure the following settings:</span></span>

   - <span data-ttu-id="54cd0-139">**Nom**: entrez un nom unique et descriptif pour la règle.</span><span class="sxs-lookup"><span data-stu-id="54cd0-139">**Name**: Enter a unique, descriptive name for the rule.</span></span> <span data-ttu-id="54cd0-140">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="54cd0-140">For example:</span></span>

     - <span data-ttu-id="54cd0-141">EOP SFV : SPM vers SCL 6</span><span class="sxs-lookup"><span data-stu-id="54cd0-141">EOP SFV:SPM to SCL 6</span></span>

     - <span data-ttu-id="54cd0-142">EOP SFV : SKS vers le niveau SCL 6</span><span class="sxs-lookup"><span data-stu-id="54cd0-142">EOP SFV:SKS to SCL 6</span></span>

     - <span data-ttu-id="54cd0-143">EOP SFV : SKB vers le niveau SCL 6</span><span class="sxs-lookup"><span data-stu-id="54cd0-143">EOP SFV:SKB to SCL 6</span></span>

   - <span data-ttu-id="54cd0-144">Cliquez sur **Autres options**.</span><span class="sxs-lookup"><span data-stu-id="54cd0-144">Click **More Options**.</span></span>

   - <span data-ttu-id="54cd0-145">**Appliquer cette règle si**: sélectionnez **un en-tête** \> **de message contient l’un de ces mots**.</span><span class="sxs-lookup"><span data-stu-id="54cd0-145">**Apply this rule if**: Select **A message header** \> **includes any of these words**.</span></span>

     <span data-ttu-id="54cd0-146">Dans la phrase entrez le texte de l' **en-tête saisissez les mots** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="54cd0-146">In the **Enter text header includes Enter words** sentence that appears, do the following steps:</span></span>

     - <span data-ttu-id="54cd0-147">Cliquez sur **entrer du texte**.</span><span class="sxs-lookup"><span data-stu-id="54cd0-147">Click **Enter text**.</span></span> <span data-ttu-id="54cd0-148">Dans la boîte de dialogue spécifier le nom de l' **en-tête** qui s’affiche, entrez **X-Forefront-antispam-Report** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="54cd0-148">In the **Specify header name** dialog that appears, enter **X-Forefront-Antispam-Report** and then click **OK**.</span></span>

     - <span data-ttu-id="54cd0-149">Cliquez sur **Entrez les mots**.</span><span class="sxs-lookup"><span data-stu-id="54cd0-149">Click  **Enter words**.</span></span> <span data-ttu-id="54cd0-150">Dans la boîte de dialogue **spécifier des mots ou des expressions** qui s’affiche, entrez l’une des valeurs d’en-tête de courrier indésirable EOP (**SFV : SPM**, **SFV : SKS**ou **SFV : SKB**), cliquez sur **Ajouter** ![une icône](../../media/ITPro-EAC-AddIcon.png)d’ajout, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="54cd0-150">In the **Specify words or phrases** dialog that appears, enter one of the EOP spam header values (**SFV:SPM**, **SFV:SKS**, or **SFV:SKB**), click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png), and then click **OK**.</span></span>

   - <span data-ttu-id="54cd0-151">**Procédez comme suit**: sélectionnez **modifier les propriétés** \> du message **définir le seuil de probabilité de courrier indésirable (SCL)**.</span><span class="sxs-lookup"><span data-stu-id="54cd0-151">**Do the following**: Select **Modify the message properties** \> **Set the spam confidence level (SCL)**.</span></span>

     <span data-ttu-id="54cd0-152">Dans la boîte de dialogue spécifier la valeur **SCL** qui s’affiche, sélectionnez **6** (la valeur par défaut est **5**).</span><span class="sxs-lookup"><span data-stu-id="54cd0-152">In the **Specify SCL** dialog that appears, select **6** (the default value is **5**).</span></span>

   <span data-ttu-id="54cd0-153">Lorsque vous avez terminé, cliquez sur **Enregistrer** .</span><span class="sxs-lookup"><span data-stu-id="54cd0-153">When you're finished, click **Save**</span></span>

<span data-ttu-id="54cd0-154">Répétez ces étapes pour les autres valeurs de verdict de courrier indésirable EOP (**SFV : SPM**, **SFV : SKS**ou **SFV : SKB**).</span><span class="sxs-lookup"><span data-stu-id="54cd0-154">Repeat these steps for the remaining EOP spam verdict values (**SFV:SPM**, **SFV:SKS**, or **SFV:SKB**).</span></span>

## <a name="use-the-exchange-management-shell-to-create-mail-flow-rules-that-set-the-scl-of-eop-spam-messages"></a><span data-ttu-id="54cd0-155">Utiliser l’environnement de commande Exchange Management Shell pour créer des règles de flux de messagerie qui définissent la valeur SCL des messages de courrier indésirable EOP</span><span class="sxs-lookup"><span data-stu-id="54cd0-155">Use the Exchange Management Shell to create mail flow rules that set the SCL of EOP spam messages</span></span>

<span data-ttu-id="54cd0-156">Utilisez la syntaxe suivante pour créer les trois règles de flux de messagerie :</span><span class="sxs-lookup"><span data-stu-id="54cd0-156">Use the following syntax to create the three mail flow rules:</span></span>

```Powershell
New-TransportRule -Name "<RuleName>" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "<EOPSpamFilteringVerdict>" -SetSCL 6
```

<span data-ttu-id="54cd0-157">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="54cd0-157">For example:</span></span>

```Powershell
New-TransportRule -Name "EOP SFV:SPM to SCL 6" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
```

```Powershell
New-TransportRule -Name "EOP SFV:SKS to SCL 6" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
```

```Powershell
New-TransportRule -Name "EOP SFV:SKB to SCL 6" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
```

<span data-ttu-id="54cd0-158">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-transportrule).</span><span class="sxs-lookup"><span data-stu-id="54cd0-158">For detailed syntax and parameter information, see [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-transportrule).</span></span>

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="54cd0-159">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="54cd0-159">How do you know this worked?</span></span>

<span data-ttu-id="54cd0-160">Pour vérifier que vous avez bien configuré EOP autonome pour envoyer du courrier indésirable dans le dossier courrier indésirable dans un environnement hybride, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="54cd0-160">To verify that you've successfully configured standalone EOP to deliver spam to the Junk Email folder in hybrid environment, do any of the following steps:</span></span>

- <span data-ttu-id="54cd0-161">Dans le centre d’administration Exchange, accédez à **règles**de **flux** \> de messagerie, sélectionnez la règle, puis](../../media/ITPro-EAC-EditIcon.png) cliquez sur **modifier** ![l’icône modifier pour vérifier les paramètres.</span><span class="sxs-lookup"><span data-stu-id="54cd0-161">In the EAC, go to **Mail flow** \> **Rules**, select the rule, and then click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png) to verify the settings.</span></span>

- <span data-ttu-id="54cd0-162">Dans l’environnement de commande Exchange Management \<Shell\> , remplacez RuleName par le nom de la règle de flux de messagerie et RUL la commande suivante pour vérifier les paramètres :</span><span class="sxs-lookup"><span data-stu-id="54cd0-162">In the Exchange Management Shell, replace \<RuleName\> with the name of the mail flow rule, and rul the following command to verify the settings:</span></span>

  ```powershell
  Get-TransportRule -Identity "<RuleName>" | Format-List
  ```

- <span data-ttu-id="54cd0-163">Dans un système de messagerie externe **qui n’analyse pas les messages sortants pour le courrier indésirable**, envoie un test générique pour le message de courrier en masse non sollicité (GTUBE) à un destinataire affecté et confirme qu’il est remis dans son dossier de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="54cd0-163">In an external email system **that doesn't scan outbound messages for spam**, send a Generic Test for Unsolicited Bulk Email (GTUBE) message to an affected recipient, and confirm that it's delivered to their Junk Email folder.</span></span> <span data-ttu-id="54cd0-164">Un message GTUBE est semblable au fichier texte EICAR (European Institute for Computer Virus Research) pour tester les paramètres des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="54cd0-164">A GTUBE message is similar to the European Institute for Computer Antivirus Research (EICAR) text file for testing malware settings.</span></span>

  <span data-ttu-id="54cd0-165">Pour envoyer un message GTUBE, incluez le texte suivant dans le corps d’un message électronique sur une seule ligne, sans espaces ni sauts de ligne :</span><span class="sxs-lookup"><span data-stu-id="54cd0-165">To send a GTUBE message, include the following text in the body of an email message on a single line, without any spaces or line breaks:</span></span>

  ```text
  XJS*C4JDBQADN1.NSBN3*2IDNEN*GTUBE-STANDARD-ANTI-UBE-TEST-EMAIL*C.34X
  ```
