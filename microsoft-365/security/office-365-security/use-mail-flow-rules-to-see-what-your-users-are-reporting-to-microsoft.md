---
title: Utiliser des règles de transport pour bloquer le signalement des courriers indésirables à Microsoft
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
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à utiliser des règles de flux de messagerie (également appelées règles de transport) pour recevoir des copies de messages que les utilisateurs signalent à Microsoft.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 5e6428a228ae64562f0b529f6aa90ddc3be46fdc
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204454"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a><span data-ttu-id="08d4c-103">Utiliser des règles de flux de courriers pour afficher les comptes-rendus envoyés par les utilisateurs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="08d4c-103">Use mail flow rules to see what your users are reporting to Microsoft</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="08d4c-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="08d4c-104">**Applies to**</span></span>
- [<span data-ttu-id="08d4c-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="08d4c-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="08d4c-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="08d4c-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="08d4c-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="08d4c-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="08d4c-108">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou dans des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, il existe plusieurs façons pour les utilisateurs de signaler des messages à Microsoft pour analyse, comme décrit dans La description du rapport sur les messages et les fichiers à [Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="08d4c-108">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, there are multiple ways for users to report messages to Microsoft for analysis as described in [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

<span data-ttu-id="08d4c-109">Vous pouvez créer une règle de flux de messagerie (également appelée règle de transport) qui recherche les messages que les utilisateurs signalent à Microsoft, et vous pouvez configurer les destinataires Bcc pour recevoir des copies de ces messages signalés.</span><span class="sxs-lookup"><span data-stu-id="08d4c-109">You can create a mail flow rule (also known as a transport rule) that looks for messages that users report to Microsoft, and you can configure Bcc recipients to receive copies of these reported messages.</span></span>

<span data-ttu-id="08d4c-110">Vous pouvez créer la règle de flux de messagerie dans le Centre d’administration Exchange (CAE) et PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec boîtes aux lettres dans Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="08d4c-110">You can create the mail flow rule in the Exchange admin center (EAC) and PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="08d4c-111">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="08d4c-111">What do you need to know before you begin?</span></span>

- <span data-ttu-id="08d4c-112">Des autorisations doivent vous être attribuées dans Exchange Online ou Exchange Online Protection avant de pouvoir suivre les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="08d4c-112">You need to be assigned permissions in Exchange Online or Exchange Online Protection before you can do the procedures in this article.</span></span> <span data-ttu-id="08d4c-113">Plus précisément, vous avez besoin du rôle Règles de **transport,** qui est  attribué par défaut aux groupes de rôles Gestion de l’organisation, Gestion de la conformité **(administrateurs** globaux) et Gestion des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="08d4c-113">Specifically, you need the **Transport Rules** role, which is assigned to the **Organization Management**, **Compliance Management** (global admins), and **Records Management** role groups by default.</span></span>

  <span data-ttu-id="08d4c-114">Pour plus d’informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="08d4c-114">For more information, see the following topics:</span></span>

  - [<span data-ttu-id="08d4c-115">Autorisations dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="08d4c-115">Permissions in Exchange Online</span></span>](/exchange/permissions-exo/permissions-exo)
  - [<span data-ttu-id="08d4c-116">Autorisations dans EOP autonome</span><span class="sxs-lookup"><span data-stu-id="08d4c-116">Permissions in standalone EOP</span></span>](feature-permissions-in-eop.md)
  - [<span data-ttu-id="08d4c-117">Utiliser le EAC pour modifier la liste des membres dans les groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="08d4c-117">Use the EAC modify the list of members in role groups</span></span>](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups)

- <span data-ttu-id="08d4c-118">Pour ouvrir le CENTRE d’administration Exchange dans Exchange Online, consultez le [Centre d’administration Exchange dans Exchange Online.](/Exchange/exchange-admin-center)</span><span class="sxs-lookup"><span data-stu-id="08d4c-118">To open the EAC in Exchange Online, see [Exchange admin center in Exchange Online](/Exchange/exchange-admin-center).</span></span> <span data-ttu-id="08d4c-119">Pour ouvrir le CAE dans EOP autonome, consultez le Centre [d’administration Exchange dans EOP autonome.](exchange-admin-center-in-exchange-online-protection-eop.md)</span><span class="sxs-lookup"><span data-stu-id="08d4c-119">To open the EAC in standalone EOP, see [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="08d4c-120">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="08d4c-120">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="08d4c-121">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="08d4c-121">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="08d4c-122">Pour plus d’informations sur les règles de flux de messagerie dans Exchange Online et EOP autonome, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="08d4c-122">For more information about mail flow rules in Exchange Online and standalone EOP, see the following topics:</span></span>
  - [<span data-ttu-id="08d4c-123">Règles de flux de messagerie (règles de transport) dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="08d4c-123">Mail flow rules (transport rules) in Exchange Online</span></span>](/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)
  - [<span data-ttu-id="08d4c-124">Conditions de règle de flux de messagerie et exceptions (prédicats) dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="08d4c-124">Mail flow rule conditions and exceptions (predicates) in Exchange Online</span></span>](/Exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions)
  - [<span data-ttu-id="08d4c-125">Actions de règle de flux de courrier dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="08d4c-125">Mail flow rule actions in Exchange Online</span></span>](/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions)

## <a name="use-the-eac-to-create-a-mail-flow-rule-to-receive-copies-of-reported-messages"></a><span data-ttu-id="08d4c-126">Utiliser le EAC pour créer une règle de flux de messagerie afin de recevoir des copies des messages signalés</span><span class="sxs-lookup"><span data-stu-id="08d4c-126">Use the EAC to create a mail flow rule to receive copies of reported messages</span></span>

1. <span data-ttu-id="08d4c-127">Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="08d4c-127">In the EAC, go to **Mail flow** \> **Rules**.</span></span>

2. <span data-ttu-id="08d4c-128">Cliquez **sur Ajouter** une icône ![ ](../../media/ITPro-EAC-AddIcon.png) Ajouter, puis **sélectionnez Créer une règle.**</span><span class="sxs-lookup"><span data-stu-id="08d4c-128">Click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png) and then select **Create a new rule**.</span></span>

3. <span data-ttu-id="08d4c-129">Dans la page **Nouvelle règle** qui s'ouvre, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="08d4c-129">In the **New rule** page that opens, configure the following settings:</span></span>

   - <span data-ttu-id="08d4c-130">**Nom**: entrez un nom unique et descriptif pour la règle.</span><span class="sxs-lookup"><span data-stu-id="08d4c-130">**Name**: Enter a unique, descriptive name for the rule.</span></span> <span data-ttu-id="08d4c-131">Par exemple, messages Bcc signalés à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="08d4c-131">For example, Bcc Messages Reported to Microsoft.</span></span>

   - <span data-ttu-id="08d4c-132">Cliquez sur **Autres options**.</span><span class="sxs-lookup"><span data-stu-id="08d4c-132">Click **More Options**.</span></span>

   - <span data-ttu-id="08d4c-133">Appliquez cette règle  si **:** Sélectionnez L’adresse du destinataire inclut l’un de ces mots : dans la boîte de dialogue Spécifier des mots ou des expressions qui s’affiche, entrez l’une des valeurs suivantes, cliquez sur Ajouter une icône, puis répétez jusqu’à ce que vous avez entré toutes les \>  **valeurs.**  ![ ](../../media/ITPro-EAC-AddIcon.png)</span><span class="sxs-lookup"><span data-stu-id="08d4c-133">**Apply this rule if**: Select **The recipient** \> **address includes any of these words**: In the **Specify words or phrases** dialog that appears, enter one of the following values, click **Add** ![Add Icon](../../media/ITPro-EAC-AddIcon.png), and repeat until you've entered all the values.</span></span>

     - `junk@office365.microsoft.com`
     - `abuse@messaging.microsoft.com`
     - `phish@office365.microsoft.com`
     - `not_junk@office365.microsoft.com`

     <span data-ttu-id="08d4c-134">Pour modifier une entrée, sélectionnez-la et cliquez sur **Modifier** ![ ](../../media/ITPro-EAC-EditIcon.png) l’icône Modifier.</span><span class="sxs-lookup"><span data-stu-id="08d4c-134">To edit an entry, select it and click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png).</span></span> <span data-ttu-id="08d4c-135">Pour supprimer une entrée, sélectionnez-la et cliquez **sur Supprimer** ![ l’icône ](../../media/ITPro-EAC-DeleteIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="08d4c-135">To remove an entry, select it and click **Remove** ![Remove icon](../../media/ITPro-EAC-DeleteIcon.png).</span></span>

     <span data-ttu-id="08d4c-136">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="08d4c-136">When you're finished, click **OK**.</span></span>

   - <span data-ttu-id="08d4c-137">**Pour ce faire,** **sélectionnez Ajouter des destinataires** \> **dans la zone Bcc.**</span><span class="sxs-lookup"><span data-stu-id="08d4c-137">**Do the following**: Select **Add recipients** \> **to the Bcc box**.</span></span> <span data-ttu-id="08d4c-138">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez les destinataires à ajouter.</span><span class="sxs-lookup"><span data-stu-id="08d4c-138">In the dialog that appears, find and select the recipients that you want to add.</span></span> <span data-ttu-id="08d4c-139">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="08d4c-139">When you're finished, click **OK**.</span></span>

4. <span data-ttu-id="08d4c-140">Vous pouvez effectuer des sélections supplémentaires pour auditer la règle, la tester, activer la règle pendant une période spécifique et d’autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="08d4c-140">You can make additional selections to audit the rule, test the rule, activate the rule during a specific time period, and other settings.</span></span> <span data-ttu-id="08d4c-141">Nous vous recommandons de tester la règle avant de l’appliquer.</span><span class="sxs-lookup"><span data-stu-id="08d4c-141">We recommend testing the rule before you enforce it.</span></span>

5. <span data-ttu-id="08d4c-142">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="08d4c-142">When you're finished, click **Save**.</span></span>

## <a name="use-powershell-to-create-a-mail-flow-rule-to-receive-copies-of-reported-messages"></a><span data-ttu-id="08d4c-143">Utiliser PowerShell pour créer une règle de flux de messagerie pour recevoir des copies des messages signalés</span><span class="sxs-lookup"><span data-stu-id="08d4c-143">Use PowerShell to create a mail flow rule to receive copies of reported messages</span></span>

<span data-ttu-id="08d4c-144">Cet exemple crée une règle de flux de messagerie nommée Bcc Messages signalés à Microsoft qui recherche les messages électroniques signalés à Microsoft à l’aide des méthodes décrites dans cet article et ajoute les utilisateurs laura@contoso.com et julia@contoso.com en tant que destinataires Bcc.</span><span class="sxs-lookup"><span data-stu-id="08d4c-144">This example creates a new mail flow rule named Bcc Messages Reported to Microsoft that looks for email messages that are reported to Microsoft by using the methods described in this article, and adds the users laura@contoso.com and julia@contoso.com as Bcc recipients.</span></span>

```powershell
New-TransportRule -Name "Bcc Messages Reported to Microsoft" -RecipientAddressContainsWords "junk@office365.microsoft.com","abuse@messaging.microsoft.com","phish@office365.microsoft.com","false_positive@messaging.microsoft.com" -BlindCopyTo "laura@contoso.com","julia@contoso.com".
```

<span data-ttu-id="08d4c-145">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TransportRule](/powershell/module/exchange/new-transportrule).</span><span class="sxs-lookup"><span data-stu-id="08d4c-145">For detailed syntax and parameter information, see [New-TransportRule](/powershell/module/exchange/new-transportrule).</span></span>

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="08d4c-146">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="08d4c-146">How do you know this worked?</span></span>

<span data-ttu-id="08d4c-147">Pour vérifier que vous avez configuré des règles de flux de messagerie pour recevoir des copies des messages signalés, appliquez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="08d4c-147">To verify that you've configured a mail flow rules to receive copies of reported messages, do any of the following steps:</span></span>

- <span data-ttu-id="08d4c-148">Dans le EAC, sélectionnez Règles de **flux** de messagerie et sélectionnez l’icône Modifier, puis \>  \> \> vérifiez les  ![ ](../../media/ITPro-EAC-EditIcon.png) paramètres.</span><span class="sxs-lookup"><span data-stu-id="08d4c-148">In the EAC, go to **Mail flow** \> **Rules** \> select the rule \> click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png), and verify the settings.</span></span>

- <span data-ttu-id="08d4c-149">Dans PowerShell, exécutez la commande suivante pour vérifier les paramètres :</span><span class="sxs-lookup"><span data-stu-id="08d4c-149">In PowerShell, run the following command to verify the settings:</span></span>

  ```powershell
  Get-TransportRule -Identity "Bcc Messages Reported to Microsoft" | Format-List
  ```

- <span data-ttu-id="08d4c-150">Envoyez un message de test à l’une des adresses e-mail de rapport et vérifiez les résultats.</span><span class="sxs-lookup"><span data-stu-id="08d4c-150">Send a test messages to one of the reporting email addresses and verify the results.</span></span>