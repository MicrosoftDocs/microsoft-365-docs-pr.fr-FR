---
title: Utiliser des règles de transport pour bloquer le signalement des courriers indésirables à Microsoft
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
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à utiliser des règles de flux de messagerie (également appelées règles de transport) pour recevoir des copies de messages que les utilisateurs signalent à Microsoft.
ms.openlocfilehash: 9798e808470a506da3d6dff65a5ea91934c1690d
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48195866"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a><span data-ttu-id="56112-103">Utiliser des règles de transport pour bloquer le signalement des courriers indésirables à Microsoft</span><span class="sxs-lookup"><span data-stu-id="56112-103">Use mail flow rules to see what your users are reporting to Microsoft</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="56112-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîte aux lettres Exchange Online, les utilisateurs peuvent signaler des messages à Microsoft pour analyse, comme décrit dans la section [rapports de messages et de fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="56112-104">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, there are multiple ways for users to report messages to Microsoft for analysis as described in [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

<span data-ttu-id="56112-105">Vous pouvez créer une règle de flux de messagerie (également appelée règle de transport) qui recherche les messages que les utilisateurs signalent à Microsoft, et vous pouvez configurer les destinataires CCI de sorte qu’ils reçoivent des copies de ces messages signalés.</span><span class="sxs-lookup"><span data-stu-id="56112-105">You can create a mail flow rule (also known as a transport rule) that looks for messages that users report to Microsoft, and you can configure Bcc recipients to receive copies of these reported messages.</span></span>

<span data-ttu-id="56112-106">Vous pouvez créer la règle de flux de messagerie dans le centre d’administration Exchange et PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ; environnement de ligne de commande Exchange (PowerShell) autonome pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="56112-106">You can create the mail flow rule in the Exchange admin center (EAC) and PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="56112-107">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="56112-107">What do you need to know before you begin?</span></span>

- <span data-ttu-id="56112-108">Pour pouvoir effectuer ces procédures, vous devez disposer d’autorisations dans Exchange Online ou EOP.</span><span class="sxs-lookup"><span data-stu-id="56112-108">You need to be assigned permissions in Exchange Online or EOP before you can do these procedures.</span></span> <span data-ttu-id="56112-109">Plus précisément, vous devez disposer du rôle **de règles de transport** , qui est affecté aux rôles de gestion de l' **organisation**, de gestion de **la conformité**et de **gestion des enregistrements** par défaut.</span><span class="sxs-lookup"><span data-stu-id="56112-109">Specifically, you need to be assigned the **Transport Rules** role, which is assigned to the **Organization Management**, **Compliance Management**, and **Records Management** roles by default.</span></span> <span data-ttu-id="56112-110">Pour plus d’informations, voir [Gérer les groupes de rôles dans Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span><span class="sxs-lookup"><span data-stu-id="56112-110">For more information, see [Manage role groups in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span></span>

- <span data-ttu-id="56112-111">Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) ou [Centre d’administration Exchange dans la version autonome EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="56112-111">To open the EAC, see [Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) or [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="56112-112">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="56112-112">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="56112-113">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="56112-113">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="56112-114">Pour plus d’informations sur les règles de flux de messagerie dans Exchange Online et dans la version autonome d’EOP, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="56112-114">For more information about mail flow rules in Exchange Online and standalone EOP, see the following topics:</span></span>

  - [<span data-ttu-id="56112-115">Règles de flux de messagerie (règles de transport) dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="56112-115">Mail flow rules (transport rules) in Exchange Online</span></span>](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)

  - [<span data-ttu-id="56112-116">Conditions de règle de flux de messagerie et exceptions (prédicats) dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="56112-116">Mail flow rule conditions and exceptions (predicates) in Exchange Online</span></span>](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions)

  - [<span data-ttu-id="56112-117">Actions de règle de flux de courrier dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="56112-117">Mail flow rule actions in Exchange Online</span></span>](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions)

## <a name="use-the-eac-to-create-a-mail-flow-rule-to-receive-copies-of-reported-messages"></a><span data-ttu-id="56112-118">Utiliser le centre d’administration Exchange pour créer une règle de flux de messagerie pour recevoir des copies des messages signalés</span><span class="sxs-lookup"><span data-stu-id="56112-118">Use the EAC to create a mail flow rule to receive copies of reported messages</span></span>

1. <span data-ttu-id="56112-119">Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="56112-119">In the EAC, go to **Mail flow** \> **Rules**.</span></span>

2. <span data-ttu-id="56112-120">Cliquez sur **Ajouter** ![ une icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) , puis sélectionnez **créer une nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="56112-120">Click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png) and then select **Create a new rule**.</span></span>

3. <span data-ttu-id="56112-121">Dans la page **Nouvelle règle** qui s'ouvre, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="56112-121">In the **New rule** page that opens, configure the following settings:</span></span>

   - <span data-ttu-id="56112-122">**Nom**: entrez un nom unique et descriptif pour la règle.</span><span class="sxs-lookup"><span data-stu-id="56112-122">**Name**: Enter a unique, descriptive name for the rule.</span></span> <span data-ttu-id="56112-123">Par exemple, les messages CCI signalés à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="56112-123">For example, Bcc Messages Reported to Microsoft.</span></span>

   - <span data-ttu-id="56112-124">Cliquez sur **Autres options**.</span><span class="sxs-lookup"><span data-stu-id="56112-124">Click **More Options**.</span></span>

   - <span data-ttu-id="56112-125">**Appliquer cette règle si**: sélectionnez **l’adresse du destinataire** contient l’un \> **des mots**suivants : dans la boîte de dialogue **spécifier des mots ou des expressions** qui s’affiche, entrez l’une des valeurs suivantes, puis cliquez sur **Ajouter** une ![ icône ](../../media/ITPro-EAC-AddIcon.png) et répétez l’opération jusqu’à ce que vous ayez entré toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="56112-125">**Apply this rule if**: Select **The recipient** \> **address includes any of these words**: In the **Specify words or phrases** dialog that appears, enter one of the following values, click **Add** ![Add Icon](../../media/ITPro-EAC-AddIcon.png), and repeat until you've entered all the values.</span></span>

     - `junk@office365.microsoft.com`
     - `abuse@messaging.microsoft.com`
     - `phish@office365.microsoft.com`
     - `false_positive@messaging.microsoft.com`

     <span data-ttu-id="56112-126">Pour modifier une entrée, sélectionnez-la et cliquez sur **modifier** l' ![ icône modifier ](../../media/ITPro-EAC-EditIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="56112-126">To edit an entry, select it and click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png).</span></span> <span data-ttu-id="56112-127">Pour supprimer une entrée, sélectionnez-la et cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-DeleteIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="56112-127">To remove an entry, select it and click **Remove** ![Remove icon](../../media/ITPro-EAC-DeleteIcon.png).</span></span>

     <span data-ttu-id="56112-128">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="56112-128">When you're finished, click **OK**.</span></span>

   - <span data-ttu-id="56112-129">**Procédez comme suit**: sélectionnez **Ajouter des destinataires** \> **dans le champ CCI**.</span><span class="sxs-lookup"><span data-stu-id="56112-129">**Do the following**: Select **Add recipients** \> **to the Bcc box**.</span></span> <span data-ttu-id="56112-130">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez les destinataires que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="56112-130">In the dialog that appears, find and select the recipients that you want to add.</span></span> <span data-ttu-id="56112-131">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="56112-131">When you're finished, click **OK**.</span></span>

4. <span data-ttu-id="56112-132">Vous pouvez effectuer des sélections supplémentaires pour auditer la règle, tester la règle, activer la règle pendant une période spécifique, ainsi que d’autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="56112-132">You can make additional selections to audit the rule, test the rule, activate the rule during a specific time period, and other settings.</span></span> <span data-ttu-id="56112-133">Nous vous recommandons de tester la règle avant de l’appliquer.</span><span class="sxs-lookup"><span data-stu-id="56112-133">We recommend testing the rule before you enforce it.</span></span>

5. <span data-ttu-id="56112-134">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="56112-134">When you're finished, click **Save**.</span></span>

## <a name="use-powershell-to-create-a-mail-flow-rule-to-receive-copies-of-reported-messages"></a><span data-ttu-id="56112-135">Utiliser PowerShell pour créer une règle de flux de messagerie pour recevoir des copies des messages signalés</span><span class="sxs-lookup"><span data-stu-id="56112-135">Use PowerShell to create a mail flow rule to receive copies of reported messages</span></span>

<span data-ttu-id="56112-136">Cet exemple crée une règle de flux de messagerie nommée CCI messages signalés à Microsoft qui recherche les messages électroniques signalés à Microsoft à l’aide des méthodes décrites dans cette rubrique, et ajoute les utilisateurs laura@contoso.com et julia@contoso.com en tant que destinataires CCI.</span><span class="sxs-lookup"><span data-stu-id="56112-136">This example creates a new mail flow rule named Bcc Messages Reported to Microsoft that looks for email messages that are reported to Microsoft by using the methods described in this topic, and adds the users laura@contoso.com and julia@contoso.com as Bcc recipients.</span></span>

```powershell
New-TransportRule -Name "Bcc Messages Reported to Microsoft" -RecipientAddressContainsWords "junk@office365.microsoft.com","abuse@messaging.microsoft.com","phish@office365.microsoft.com","false_positive@messaging.microsoft.com" -BlindCopyTo "laura@contoso.com","julia@contoso.com".
```

<span data-ttu-id="56112-137">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/new-transportrule).</span><span class="sxs-lookup"><span data-stu-id="56112-137">For detailed syntax and parameter information, see [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/new-transportrule).</span></span>

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="56112-138">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="56112-138">How do you know this worked?</span></span>

<span data-ttu-id="56112-139">Pour vérifier que vous avez configuré des règles de flux de messagerie pour recevoir des copies de messages signalés, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="56112-139">To verify that you've configured a mail flow rules to receive copies of reported messages, do any of the following steps:</span></span>

- <span data-ttu-id="56112-140">Dans le centre d’administration Exchange, accédez à règles de **flux de messagerie** \> **Rules** \> Sélectionnez la règle \> , cliquez sur **modifier** ![ l’icône d’édition ](../../media/ITPro-EAC-EditIcon.png) et vérifiez les paramètres.</span><span class="sxs-lookup"><span data-stu-id="56112-140">In the EAC, go to **Mail flow** \> **Rules** \> select the rule \> click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png), and verify the settings.</span></span>

- <span data-ttu-id="56112-141">Dans PowerShell, exécutez la commande suivante pour vérifier les paramètres :</span><span class="sxs-lookup"><span data-stu-id="56112-141">In PowerShell, run the following command to verify the settings:</span></span>

  ```powershell
  Get-TransportRule -Identity "Bcc Messages Reported to Microsoft" | Format-List
  ```

- <span data-ttu-id="56112-142">Envoyez un message de test à l’une des adresses de messagerie de création de rapports et vérifiez les résultats.</span><span class="sxs-lookup"><span data-stu-id="56112-142">Send a test messages to one of the reporting email addresses and verify the results.</span></span>
