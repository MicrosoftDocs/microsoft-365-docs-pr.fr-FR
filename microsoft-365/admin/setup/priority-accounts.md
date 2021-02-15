---
title: Gérer et surveiller les comptes prioritaires
f1.keywords:
- CSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
ms.custom: AdminSurgePortfolio
description: Surveiller les messages électroniques ayant échoué et retardés envoyés vers ou depuis des comptes ayant un impact important sur l’entreprise.
ms.openlocfilehash: bc191873b3bbdcd84122a5430adeffe2b8c29fb1
ms.sourcegitcommit: 5ce64d510b15c6e2df32b78e6086f77156731e3c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49477612"
---
# <a name="manage-and-monitor-priority-accounts"></a><span data-ttu-id="edc4c-103">Gérer et surveiller les comptes prioritaires</span><span class="sxs-lookup"><span data-stu-id="edc4c-103">Manage and monitor priority accounts</span></span>

<span data-ttu-id="edc4c-104">Dans chaque organisation Microsoft 365, il existe des personnes essentielles, telles que des cadres, des responsables, des responsables ou d’autres utilisateurs qui ont accès à des informations sensibles, propriétaires ou prioritaires.</span><span class="sxs-lookup"><span data-stu-id="edc4c-104">In every Microsoft 365 organization, there are people that are essential, like executives, leaders, managers, or other users who have access to sensitive, proprietary, or high priority information.</span></span>

<span data-ttu-id="edc4c-105">Pour aider votre organisation à protéger ces comptes, vous pouvez désormais désigner des utilisateurs spécifiques en tant que comptes prioritaires et tirer parti des fonctionnalités propres à l’application qui leur offrent une protection supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="edc4c-105">To help your organization protect these accounts, you can now designate specific users as priority accounts and leverage app-specific features that provide them with extra protection.</span></span> <span data-ttu-id="edc4c-106">À l’avenir, d’autres applications et fonctionnalités ront en charge les comptes prioritaires. Pour commencer, nous avons annoncé deux fonctionnalités : la **protection** de compte prioritaire et la surveillance du flux de messagerie **premium.**</span><span class="sxs-lookup"><span data-stu-id="edc4c-106">In the future, more apps and features will support priority accounts, and to start with, we’ve announced two capabilities: **priority account protection** and **premium mail flow monitoring**.</span></span>

- <span data-ttu-id="edc4c-107">Protection des comptes prioritaires **:** Microsoft Defender pour Office 365 (anciennement Office 365 - Protection avancée contre les menaces) prend en charge les comptes prioritaires en tant que balises qui peuvent être utilisées dans les filtres dans les alertes, les rapports et les enquêtes.</span><span class="sxs-lookup"><span data-stu-id="edc4c-107">**Priority account protection** - Microsoft Defender for Office 365 (formerly Office 365 Advanced Threat Protection) supports priority accounts as tags that can be used in filters in alerts, reports, and investigations.</span></span> <span data-ttu-id="edc4c-108">Pour plus d’informations, consultez [balises utilisateur dans Microsoft Defender pour Office 365.](https://docs.microsoft.com/microsoft-365/security/office-365-security/user-tags?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="edc4c-108">For more information, check out [User tags in Microsoft Defender for Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/user-tags?view=o365-worldwide).</span></span>
- <span data-ttu-id="edc4c-109">**Surveillance du flux de messagerie premium** : un flux de messagerie sain peut être essentiel au succès de l’entreprise, et les retards ou défaillances de remise peuvent avoir un impact négatif sur l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="edc4c-109">**Premium Mail Flow Monitoring** - Healthy mail flow can be critical to business success, and delivery delays or failures can have a negative impact on the business.</span></span> <span data-ttu-id="edc4c-110">Vous pouvez choisir un seuil pour les e-mails en échec ou différés, recevoir des alertes lorsque ce seuil est dépassé et afficher un rapport des problèmes de messagerie pour les comptes prioritaires.</span><span class="sxs-lookup"><span data-stu-id="edc4c-110">You can choose a threshold for failed or delayed emails, receive alerts when that threshold is exceeded, and view a report of email issues for priority accounts.</span></span> <span data-ttu-id="edc4c-111">Pour plus d’informations, consultez le rapport Problèmes de messagerie pour le rapport des comptes [prioritaires dans le EAC moderne.](https://docs.microsoft.com/exchange/monitoring/mail-flow-reports/mfr-email-issues-for-priority-accounts-report)</span><span class="sxs-lookup"><span data-stu-id="edc4c-111">For more information, check out [Email issues for priority accounts report in the modern EAC](https://docs.microsoft.com/exchange/monitoring/mail-flow-reports/mfr-email-issues-for-priority-accounts-report).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="edc4c-112">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="edc4c-112">Before you begin</span></span>

<span data-ttu-id="edc4c-113">La **fonctionnalité de protection des** comptes prioritaires décrite dans cette rubrique est disponible uniquement pour les organisations qui répondent aux exigences suivantes :</span><span class="sxs-lookup"><span data-stu-id="edc4c-113">The **Priority account protection** feature that's described in this topic is available only to organizations that meet the following requirements:</span></span>

- <span data-ttu-id="edc4c-114">Microsoft Defender pour Office 365 Plan 2, y compris ceux avec Office 365 E3, Office 365 E5, Microsoft 365 E5 ou Microsoft 365 E5 Security.</span><span class="sxs-lookup"><span data-stu-id="edc4c-114">Microsoft Defender for Office 365 Plan 2, including those with Office 365 E3, Office 365 E5, Microsoft 365 E5, or Microsoft 365 E5 Security.</span></span>

<span data-ttu-id="edc4c-115">La **fonctionnalité De surveillance du flux** de messagerie Premium décrite dans cette rubrique est disponible uniquement pour les organisations qui répondent aux exigences suivantes :</span><span class="sxs-lookup"><span data-stu-id="edc4c-115">The **Premium Mail Flow Monitoring** feature that's described in this topic is available only to organizations that meet the following requirements:</span></span>

- <span data-ttu-id="edc4c-116">Votre organisation doit avoir un nombre de licences d’au moins 10 000, de l’un des produits suivants ou d’une combinaison des produits suivants : Office 365 E3, Microsoft 365 E3, Office 365 E5, Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="edc4c-116">Your organization needs to have a license count of at least 10,000, from either one of, or a combination of the following products: Office 365 E3, Microsoft 365 E3, Office 365 E5, Microsoft 365 E5.</span></span> <span data-ttu-id="edc4c-117">Par exemple, votre organisation peut avoir 3 000 licences Office 365 E3 et 8 500 Licences Microsoft 365 E5, pour un total de 11 500 licences provenant des produits éligibles.</span><span class="sxs-lookup"><span data-stu-id="edc4c-117">For example, your organization can have 3000 Office 365 E3 licenses and 8500 Microsoft 365 E5, for a total of 11,500 licenses from the qualifying products.</span></span>
- <span data-ttu-id="edc4c-118">Votre organisation doit avoir au moins 50 utilisateurs Exchange Online actifs par mois.</span><span class="sxs-lookup"><span data-stu-id="edc4c-118">Your organization needs to have at least 50 monthly active Exchange Online users.</span></span>

> [!NOTE]
> <span data-ttu-id="edc4c-119">Vous pouvez surveiller jusqu’à 250 comptes prioritaires.</span><span class="sxs-lookup"><span data-stu-id="edc4c-119">You can monitor up to 250 priority accounts.</span></span>

### <a name="add-priority-accounts-from-the-setup-page"></a><span data-ttu-id="edc4c-120">Ajouter des comptes de priorité à partir de la page d’installation</span><span class="sxs-lookup"><span data-stu-id="edc4c-120">Add priority accounts from the Setup page</span></span>

<span data-ttu-id="edc4c-121">Ajoutez des comptes de priorité à partir de la **page d’installation.**</span><span class="sxs-lookup"><span data-stu-id="edc4c-121">Add priority accounts from the **Setup page**.</span></span>

1. <span data-ttu-id="edc4c-122">Go to the Microsoft 365 admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> .</span><span class="sxs-lookup"><span data-stu-id="edc4c-122">Go to the Microsoft 365 admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

2. <span data-ttu-id="edc4c-123">Go to **Setup**  >  **Organizational knowledge**, and choose **View** under Monitor your most **important accounts**.</span><span class="sxs-lookup"><span data-stu-id="edc4c-123">Go to **Setup** > **Organizational knowledge**, and choose **View** under **Monitor your most important accounts**.</span></span>

3. <span data-ttu-id="edc4c-124">Sélectionnez **Commencer ou** **Gérer.**</span><span class="sxs-lookup"><span data-stu-id="edc4c-124">Select **Get Started** or **Manage**.</span></span>

4. <span data-ttu-id="edc4c-125">Dans **la** page Ajouter des comptes de priorité, dans le champ de recherche, tapez le nom ou l’adresse e-mail de la personne que vous souhaitez ajouter à la liste des comptes prioritaires.</span><span class="sxs-lookup"><span data-stu-id="edc4c-125">On the **Add Priority accounts** page, in the search field, type the name or email address of the person you want to add to the priority accounts list.</span></span> <span data-ttu-id="edc4c-126">Vous pouvez également définir votre seuil de courrier électronique pour les e-mails en échec ou différés et obtenir un rapport hebdomadaire des problèmes pour les comptes prioritaires.</span><span class="sxs-lookup"><span data-stu-id="edc4c-126">You can also set your email threshold for failed or delayed emails and get a weekly report of issues for priority accounts.</span></span>

5. <span data-ttu-id="edc4c-127">Sélectionnez l’utilisateur et choisissez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="edc4c-127">Select the user and choose **Save**.</span></span>

<span data-ttu-id="edc4c-128">Vous pouvez également ajouter des comptes de priorité à partir de la page Utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="edc4c-128">You can also add priority accounts from the Active users page.</span></span>

### <a name="add-priority-accounts-from-active-users-page"></a><span data-ttu-id="edc4c-129">Ajouter des comptes de priorité à partir de la page Utilisateurs actifs</span><span class="sxs-lookup"><span data-stu-id="edc4c-129">Add priority accounts from Active users page</span></span>

<span data-ttu-id="edc4c-130">Ajoutez des comptes de priorité à partir de la page Utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="edc4c-130">Add priority accounts from the Active users page.</span></span>

1. <span data-ttu-id="edc4c-131">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span><span class="sxs-lookup"><span data-stu-id="edc4c-131">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

2. <span data-ttu-id="edc4c-132">Go to **Users**  >  **Active users** and choose **...** at the top of the page.</span><span class="sxs-lookup"><span data-stu-id="edc4c-132">Go to **Users** > **Active users** and choose **...** at the top of the page.</span></span> <span data-ttu-id="edc4c-133">Sélectionnez **Gérer les comptes prioritaires.**</span><span class="sxs-lookup"><span data-stu-id="edc4c-133">Select **Manage priority accounts**.</span></span>

3. <span data-ttu-id="edc4c-134">Sélectionnez **Ajouter des** comptes et, dans la **page** Ajouter des comptes de priorité, dans le champ de recherche, tapez le nom de la personne que vous souhaitez ajouter à la liste des comptes prioritaires.</span><span class="sxs-lookup"><span data-stu-id="edc4c-134">Select **Add accounts**, and on the **Add Priority accounts** page, in the search field, type the name of the person you want to add to the priority accounts list.</span></span>

4. <span data-ttu-id="edc4c-135">Sélectionnez l’utilisateur et choisissez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="edc4c-135">Select the user and choose **Save**.</span></span>

## <a name="remove-a-user-from-the-priority-accounts-list"></a><span data-ttu-id="edc4c-136">Supprimer un utilisateur de la liste des comptes prioritaires</span><span class="sxs-lookup"><span data-stu-id="edc4c-136">Remove a user from the priority accounts list</span></span>

1. <span data-ttu-id="edc4c-137">Go to the Microsoft 365 admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> .</span><span class="sxs-lookup"><span data-stu-id="edc4c-137">Go to the Microsoft 365 admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

2. <span data-ttu-id="edc4c-138">Go to **Setup**  >  **Organizational knowledge**, and choose **View** under Monitor your most **important accounts**.</span><span class="sxs-lookup"><span data-stu-id="edc4c-138">Go to **Setup** > **Organizational knowledge**, and choose **View** under **Monitor your most important accounts**.</span></span>

3. <span data-ttu-id="edc4c-139">On the **Monitor your most accounts** page, choose **Priority accounts** under **Manage this feature**.</span><span class="sxs-lookup"><span data-stu-id="edc4c-139">On the **Monitor your most accounts** page, choose **Priority accounts** under **Manage this feature**.</span></span>

4. <span data-ttu-id="edc4c-140">Dans la page **Comptes prioritaires,** sélectionnez l’utilisateur ou les utilisateurs que vous souhaitez supprimer de la liste, puis choisissez Supprimer **des comptes.**</span><span class="sxs-lookup"><span data-stu-id="edc4c-140">On the **Priority accounts** page, select the user or users you want to remove from the list and choose, **Remove accounts**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edc4c-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="edc4c-141">Related topics</span></span>

[<span data-ttu-id="edc4c-142">Utilisation de comptes prioritaires dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="edc4c-142">Using Priority Accounts in Microsoft 365</span></span>](https://techcommunity.microsoft.com/t5/microsoft-365-blog/using-priority-accounts-in-microsoft-365/ba-p/1873314)