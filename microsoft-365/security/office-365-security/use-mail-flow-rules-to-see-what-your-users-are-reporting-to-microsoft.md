---
title: Utiliser des règles de transport pour bloquer le signalement des courriers indésirables à Microsoft
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
ms.collection:
- M365-security-compliance
description: Vous pouvez créer une règle de flux de messagerie Exchange pour empêcher vos utilisateurs d’envoyer des messages électroniques à Microsoft à des fins d’analyse et de les utiliser dans vos propres processus de sécurité.
ms.openlocfilehash: 530cc12fd83650f319da3f65e961c925a1de7409
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41598057"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a><span data-ttu-id="a33da-103">Utiliser des règles de transport pour bloquer le signalement des courriers indésirables à Microsoft</span><span class="sxs-lookup"><span data-stu-id="a33da-103">Use mail flow rules to see what your users are reporting to Microsoft</span></span>

<span data-ttu-id="a33da-104">Il existe plusieurs moyens d'envoyer des messages faux positifs et faux négatifs à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="a33da-104">There are multiple ways you can send false positive and false negative messages to Microsoft for analysis.</span></span> <span data-ttu-id="a33da-105">En tant qu'administrateur, vous pouvez utiliser des règles de flux de messagerie pour voir ce que vos utilisateurs signalent à Microsoft comme courrier indésirable et non indésirable, ou comme messages électroniques de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="a33da-105">As an administrator, you can use mail flow rules to see what your users are reporting to Microsoft as spam, non-spam, and phishing scams.</span></span> <span data-ttu-id="a33da-106">Pour plus d'informations, consultez la rubrique [Soumission des messages indésirables, légitimes ou des tentatives de hameçonnage à Microsoft pour analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a33da-106">For more information, see [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span></span> <span data-ttu-id="a33da-107">À l’inverse, vous pouvez créer une règle de flux de messagerie Exchange (également appelée règle de transport) pour empêcher vos utilisateurs d’envoyer des messages électroniques à Microsoft à des fins d’analyse et de les utiliser dans vos propres processus de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a33da-107">Conversely, you can create an Exchange mail flow rule (also known as a transport rule) to prevent your users from sending email messages to Microsoft for analysis and use them in your own security processes.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="a33da-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a33da-108">What do you need to know before you begin?</span></span>

<span data-ttu-id="a33da-109">Durée d’exécution estimée : 5 minutes</span><span class="sxs-lookup"><span data-stu-id="a33da-109">Estimated time to complete: 5 minutes</span></span>

<span data-ttu-id="a33da-110">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="a33da-110">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="a33da-111">Pour voir les autorisations qui vous sont nécessaires, consultez les entrées « flux de messagerie » et « stratégies de boîte aux lettres Outlook sur le Web » dans [autorisations Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions#exchange-online-permissions).</span><span class="sxs-lookup"><span data-stu-id="a33da-111">To see what permissions you need, see the "Mail flow"  and "Outlook on the web mailbox policies" entries in [Exchange Online permissions](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions#exchange-online-permissions).</span></span>

<span data-ttu-id="a33da-112">Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span><span class="sxs-lookup"><span data-stu-id="a33da-112">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a><span data-ttu-id="a33da-113">Utiliser le CAE pour créer une règle de flux de messagerie afin d’afficher le courrier signalé comme indésirable, comme hameçonnage et comme non indésirable par les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a33da-113">Use the EAC to create a mail flow rule to view users' manual junk, phishing, and not junk reports</span></span>

1. <span data-ttu-id="a33da-114">Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="a33da-114">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>

2. <span data-ttu-id="a33da-115">Cliquez sur ![Icône Ajouter](../media/ITPro-EAC-AddIcon.gif), puis sélectionnez **Créer une règle**.</span><span class="sxs-lookup"><span data-stu-id="a33da-115">Click ![Add Icon](../media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>

3. <span data-ttu-id="a33da-116">Nommez la règle, puis cliquez sur **Autres options**.</span><span class="sxs-lookup"><span data-stu-id="a33da-116">Give the rule a name and then click **More options**.</span></span>

4. <span data-ttu-id="a33da-117">Sous **Appliquer cette règle si**, sélectionnez **Le destinataire**, puis **l'adresse comprend l'un des mots suivants**.</span><span class="sxs-lookup"><span data-stu-id="a33da-117">Under **Apply this rule if**, select **The recipient** and then choose **address includes any of these words**.</span></span>

5. <span data-ttu-id="a33da-118">Dans la zone **spécifier des mots ou des expressions** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a33da-118">In the **specify words or phrases** box, do the following steps:</span></span>

   - <span data-ttu-id="a33da-119">Tapez `abuse@messaging.microsoft.com`, cliquez **sur Ajouter** ![une](../media/ITPro-EAC-AddIcon.gif)icône, `junk@office365.microsoft.com` tapez, puis cliquez sur **Ajouter** ![une icône](../media/ITPro-EAC-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="a33da-119">Type `abuse@messaging.microsoft.com`, click **Add** ![Add Icon](../media/ITPro-EAC-AddIcon.gif), type `junk@office365.microsoft.com` and then click **Add** ![Add Icon](../media/ITPro-EAC-AddIcon.gif).</span></span> <span data-ttu-id="a33da-120">Ces adresses de messagerie sont utilisées pour envoyer les messages faux négatifs à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a33da-120">These email addresses are used to submit false negative messages to Microsoft.</span></span>

   - <span data-ttu-id="a33da-121">Tapez `phish@office365.microsoft.com` , puis cliquez sur **Ajouter** ![une](../media/ITPro-EAC-AddIcon.gif)icône Ajouter.</span><span class="sxs-lookup"><span data-stu-id="a33da-121">Type `phish@office365.microsoft.com` and then click **Add** ![Add Icon](../media/ITPro-EAC-AddIcon.gif).</span></span> <span data-ttu-id="a33da-122">Cette adresse de messagerie est utilisée pour envoyer des messages de tentative de hameçonnage à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a33da-122">This email address is used to submit missed phishing messages to Microsoft.</span></span>

   - <span data-ttu-id="a33da-123">Type `false_positive@messaging.microsoft.com`, cliquez sur **Ajouter** ![une](../media/ITPro-EAC-AddIcon.gif)icône Ajouter `not_junk@office365.microsoft.com`, tapez, puis cliquez sur **Ajouter** ![Ajouter icône](../media/ITPro-EAC-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="a33da-123">Type `false_positive@messaging.microsoft.com`, click **Add** ![Add Icon](../media/ITPro-EAC-AddIcon.gif), type `not_junk@office365.microsoft.com`, and then click **Add** ![Add Icon](../media/ITPro-EAC-AddIcon.gif).</span></span> <span data-ttu-id="a33da-124">Ces adresses de messagerie sont utilisées pour envoyer les messages faux positifs à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a33da-124">These email addresses are used to submit false positive messages to Microsoft.</span></span>

   - <span data-ttu-id="a33da-125">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a33da-125">Click **OK**.</span></span>

6. <span data-ttu-id="a33da-126">Sous **Effectuer les opérations suivantes**, sélectionnez **Envoyer le message en Cci vers...**, puis sélectionnez les boîtes aux lettres où vous voulez recevoir les messages.</span><span class="sxs-lookup"><span data-stu-id="a33da-126">Under **Do the following**, select **Bcc the message to...** and then and then select the mailboxes where you'd like to receive the messages.</span></span>

7. <span data-ttu-id="a33da-127">Si vous le souhaitez, vous pouvez effectuer des sélections pour auditer, tester et activer la règle sur une période spécifique, etc.</span><span class="sxs-lookup"><span data-stu-id="a33da-127">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections.</span></span> <span data-ttu-id="a33da-128">Nous vous recommandons de tester la règle pendant un certain temps avant de l'appliquer.</span><span class="sxs-lookup"><span data-stu-id="a33da-128">We recommend testing the rule for a period before you enforce it.</span></span> <span data-ttu-id="a33da-129">Voir [les procédures pour les règles de flux de messagerie](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures).</span><span class="sxs-lookup"><span data-stu-id="a33da-129">See [Procedures for mail flow rules](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures).</span></span>

8. <span data-ttu-id="a33da-p107">Pour enregistrer la règle, cliquez sur **Enregistrer**. Elle apparaît dans votre liste de règles.</span><span class="sxs-lookup"><span data-stu-id="a33da-p107">Click the **save** button to save the rule. It appears in your list of rules.</span></span>

<span data-ttu-id="a33da-132">Une fois la règle créée et appliquée, tous les messages envoyés à partir de votre organisation aux adresses de messagerie spécifiées seront copiés vers la boîte aux lettres spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a33da-132">After you create and enforce the rule, any messages that are sent from your organization to specified email addresses will be copied to the specified mailbox.</span></span>
