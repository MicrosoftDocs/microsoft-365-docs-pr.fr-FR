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
description: Le moniteur a échoué et retardé les messages envoyés vers ou à partir de comptes ayant un impact élevé sur l’activité.
ms.openlocfilehash: bc191873b3bbdcd84122a5430adeffe2b8c29fb1
ms.sourcegitcommit: 5ce64d510b15c6e2df32b78e6086f77156731e3c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49477612"
---
# <a name="manage-and-monitor-priority-accounts"></a><span data-ttu-id="b4966-103">Gérer et surveiller les comptes prioritaires</span><span class="sxs-lookup"><span data-stu-id="b4966-103">Manage and monitor priority accounts</span></span>

<span data-ttu-id="b4966-104">Dans chaque organisation Microsoft 365, il existe des personnes qui sont essentielles, comme des cadres, des dirigeants, des responsables ou d’autres utilisateurs qui ont accès à des informations sensibles, propriétaires ou à haute priorité.</span><span class="sxs-lookup"><span data-stu-id="b4966-104">In every Microsoft 365 organization, there are people that are essential, like executives, leaders, managers, or other users who have access to sensitive, proprietary, or high priority information.</span></span>

<span data-ttu-id="b4966-105">Pour aider votre organisation à protéger ces comptes, vous pouvez maintenant désigner des utilisateurs spécifiques comme comptes prioritaires et exploiter des fonctionnalités spécifiques aux applications qui leur fournissent une protection supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="b4966-105">To help your organization protect these accounts, you can now designate specific users as priority accounts and leverage app-specific features that provide them with extra protection.</span></span> <span data-ttu-id="b4966-106">À l’avenir, des applications et des fonctionnalités supplémentaires prendront en charge les comptes prioritaires et nous avons annoncé deux fonctionnalités : la **protection de compte prioritaire** et l' **analyse du flux de messagerie Premium**.</span><span class="sxs-lookup"><span data-stu-id="b4966-106">In the future, more apps and features will support priority accounts, and to start with, we’ve announced two capabilities: **priority account protection** and **premium mail flow monitoring**.</span></span>

- <span data-ttu-id="b4966-107">**Protection des comptes prioritaires** : Microsoft Defender pour Office 365 (anciennement Office 365 Advanced Threat Protection) prend en charge les comptes prioritaires en tant que balises pouvant être utilisées dans les filtres dans les alertes, les rapports et les enquêtes.</span><span class="sxs-lookup"><span data-stu-id="b4966-107">**Priority account protection** - Microsoft Defender for Office 365 (formerly Office 365 Advanced Threat Protection) supports priority accounts as tags that can be used in filters in alerts, reports, and investigations.</span></span> <span data-ttu-id="b4966-108">Pour plus d’informations, consultez les [balises utilisateur dans Microsoft Defender pour Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/user-tags?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="b4966-108">For more information, check out [User tags in Microsoft Defender for Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/user-tags?view=o365-worldwide).</span></span>
- <span data-ttu-id="b4966-109">**Surveillance du flux de messagerie Premium** : le flux de messagerie intègre peut être essentiel à la réussite de l’entreprise, et les délais de remise ou les échecs peuvent avoir un impact négatif sur l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b4966-109">**Premium Mail Flow Monitoring** - Healthy mail flow can be critical to business success, and delivery delays or failures can have a negative impact on the business.</span></span> <span data-ttu-id="b4966-110">Vous pouvez choisir un seuil pour les e-mails ayant échoué ou retardé, recevoir des alertes en cas de dépassement de ce seuil et afficher un rapport des problèmes de messagerie pour les comptes prioritaires.</span><span class="sxs-lookup"><span data-stu-id="b4966-110">You can choose a threshold for failed or delayed emails, receive alerts when that threshold is exceeded, and view a report of email issues for priority accounts.</span></span> <span data-ttu-id="b4966-111">Pour plus d’informations, consultez [l’e-mail problèmes liés aux comptes prioritaires dans le centre d'](https://docs.microsoft.com/exchange/monitoring/mail-flow-reports/mfr-email-issues-for-priority-accounts-report)administration Exchange moderne.</span><span class="sxs-lookup"><span data-stu-id="b4966-111">For more information, check out [Email issues for priority accounts report in the modern EAC](https://docs.microsoft.com/exchange/monitoring/mail-flow-reports/mfr-email-issues-for-priority-accounts-report).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="b4966-112">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b4966-112">Before you begin</span></span>

<span data-ttu-id="b4966-113">La fonctionnalité de **protection des comptes prioritaires** décrite dans cette rubrique est disponible uniquement pour les organisations qui répondent aux exigences suivantes :</span><span class="sxs-lookup"><span data-stu-id="b4966-113">The **Priority account protection** feature that's described in this topic is available only to organizations that meet the following requirements:</span></span>

- <span data-ttu-id="b4966-114">Microsoft Defender pour Office 365 plan 2, y compris ceux avec Office 365 E3, Office 365 E5, Microsoft 365 E5 ou Microsoft 365 E5 sécurité.</span><span class="sxs-lookup"><span data-stu-id="b4966-114">Microsoft Defender for Office 365 Plan 2, including those with Office 365 E3, Office 365 E5, Microsoft 365 E5, or Microsoft 365 E5 Security.</span></span>

<span data-ttu-id="b4966-115">La fonctionnalité de **surveillance du flux de messagerie Premium** décrite dans cette rubrique est disponible uniquement pour les organisations qui remplissent les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b4966-115">The **Premium Mail Flow Monitoring** feature that's described in this topic is available only to organizations that meet the following requirements:</span></span>

- <span data-ttu-id="b4966-116">Votre organisation doit avoir un nombre de licences d’au moins 10 000, soit de l’une ou l’autre des produits suivants : Office 365 E3, Microsoft 365 E3, Office 365 E5, Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="b4966-116">Your organization needs to have a license count of at least 10,000, from either one of, or a combination of the following products: Office 365 E3, Microsoft 365 E3, Office 365 E5, Microsoft 365 E5.</span></span> <span data-ttu-id="b4966-117">Par exemple, votre organisation peut avoir 3000 Office 365 E3 licences et 8500 Microsoft 365 E5, soit un total de 11 500 licences des produits qualifiants.</span><span class="sxs-lookup"><span data-stu-id="b4966-117">For example, your organization can have 3000 Office 365 E3 licenses and 8500 Microsoft 365 E5, for a total of 11,500 licenses from the qualifying products.</span></span>
- <span data-ttu-id="b4966-118">Votre organisation doit disposer d’au moins 50 utilisateurs Exchange Online actifs mensuels.</span><span class="sxs-lookup"><span data-stu-id="b4966-118">Your organization needs to have at least 50 monthly active Exchange Online users.</span></span>

> [!NOTE]
> <span data-ttu-id="b4966-119">Vous pouvez surveiller jusqu’à 250 comptes de priorité.</span><span class="sxs-lookup"><span data-stu-id="b4966-119">You can monitor up to 250 priority accounts.</span></span>

### <a name="add-priority-accounts-from-the-setup-page"></a><span data-ttu-id="b4966-120">Ajouter des comptes de priorité à partir de la page de configuration</span><span class="sxs-lookup"><span data-stu-id="b4966-120">Add priority accounts from the Setup page</span></span>

<span data-ttu-id="b4966-121">Ajoutez des comptes de priorité à partir de la **page de configuration**.</span><span class="sxs-lookup"><span data-stu-id="b4966-121">Add priority accounts from the **Setup page**.</span></span>

1. <span data-ttu-id="b4966-122">Accédez au centre d’administration Microsoft 365 à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> .</span><span class="sxs-lookup"><span data-stu-id="b4966-122">Go to the Microsoft 365 admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

2. <span data-ttu-id="b4966-123">Accédez à **configurer**  >  les connaissances de l'**organisation**, puis choisissez **affichage** sous **surveiller vos comptes les plus importants**.</span><span class="sxs-lookup"><span data-stu-id="b4966-123">Go to **Setup** > **Organizational knowledge**, and choose **View** under **Monitor your most important accounts**.</span></span>

3. <span data-ttu-id="b4966-124">Sélectionnez **prise en main** ou **gestion**.</span><span class="sxs-lookup"><span data-stu-id="b4966-124">Select **Get Started** or **Manage**.</span></span>

4. <span data-ttu-id="b4966-125">Dans la page **Ajouter un compte prioritaire** , dans le champ de recherche, tapez le nom ou l’adresse de messagerie de la personne que vous souhaitez ajouter à la liste comptes prioritaires.</span><span class="sxs-lookup"><span data-stu-id="b4966-125">On the **Add Priority accounts** page, in the search field, type the name or email address of the person you want to add to the priority accounts list.</span></span> <span data-ttu-id="b4966-126">Vous pouvez également définir le seuil de courrier électronique pour les messages ayant échoué ou différé et obtenir un rapport hebdomadaire des problèmes liés aux comptes prioritaires.</span><span class="sxs-lookup"><span data-stu-id="b4966-126">You can also set your email threshold for failed or delayed emails and get a weekly report of issues for priority accounts.</span></span>

5. <span data-ttu-id="b4966-127">Sélectionnez l’utilisateur, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b4966-127">Select the user and choose **Save**.</span></span>

<span data-ttu-id="b4966-128">Vous pouvez également ajouter des comptes de priorité à partir de la page utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="b4966-128">You can also add priority accounts from the Active users page.</span></span>

### <a name="add-priority-accounts-from-active-users-page"></a><span data-ttu-id="b4966-129">Ajouter des comptes prioritaires à partir de la page utilisateurs actifs</span><span class="sxs-lookup"><span data-stu-id="b4966-129">Add priority accounts from Active users page</span></span>

<span data-ttu-id="b4966-130">Ajoutez des comptes de priorité à partir de la page utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="b4966-130">Add priority accounts from the Active users page.</span></span>

1. <span data-ttu-id="b4966-131">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span><span class="sxs-lookup"><span data-stu-id="b4966-131">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

2. <span data-ttu-id="b4966-132">Accédez à **utilisateurs**  >  **actifs** et sélectionnez **...** en haut de la page.</span><span class="sxs-lookup"><span data-stu-id="b4966-132">Go to **Users** > **Active users** and choose **...** at the top of the page.</span></span> <span data-ttu-id="b4966-133">Sélectionnez **Manage Priority Accounts**.</span><span class="sxs-lookup"><span data-stu-id="b4966-133">Select **Manage priority accounts**.</span></span>

3. <span data-ttu-id="b4966-134">Sélectionnez **Ajouter des comptes**, puis, dans la page **Ajouter un compte prioritaire** , dans le champ de recherche, tapez le nom de la personne que vous souhaitez ajouter à la liste comptes prioritaires.</span><span class="sxs-lookup"><span data-stu-id="b4966-134">Select **Add accounts**, and on the **Add Priority accounts** page, in the search field, type the name of the person you want to add to the priority accounts list.</span></span>

4. <span data-ttu-id="b4966-135">Sélectionnez l’utilisateur, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b4966-135">Select the user and choose **Save**.</span></span>

## <a name="remove-a-user-from-the-priority-accounts-list"></a><span data-ttu-id="b4966-136">Supprimer un utilisateur de la liste des comptes prioritaires</span><span class="sxs-lookup"><span data-stu-id="b4966-136">Remove a user from the priority accounts list</span></span>

1. <span data-ttu-id="b4966-137">Accédez au centre d’administration Microsoft 365 à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> .</span><span class="sxs-lookup"><span data-stu-id="b4966-137">Go to the Microsoft 365 admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

2. <span data-ttu-id="b4966-138">Accédez à **configurer**  >  les connaissances de l'**organisation**, puis choisissez **affichage** sous **surveiller vos comptes les plus importants**.</span><span class="sxs-lookup"><span data-stu-id="b4966-138">Go to **Setup** > **Organizational knowledge**, and choose **View** under **Monitor your most important accounts**.</span></span>

3. <span data-ttu-id="b4966-139">Sur la page **surveiller votre plus grand nombre de comptes** , choisissez **comptes prioritaires** sous **gérer cette fonctionnalité**.</span><span class="sxs-lookup"><span data-stu-id="b4966-139">On the **Monitor your most accounts** page, choose **Priority accounts** under **Manage this feature**.</span></span>

4. <span data-ttu-id="b4966-140">Sur la page **comptes prioritaires** , sélectionnez l’utilisateur ou les utilisateurs que vous souhaitez supprimer de la liste, puis choisissez **supprimer des comptes**.</span><span class="sxs-lookup"><span data-stu-id="b4966-140">On the **Priority accounts** page, select the user or users you want to remove from the list and choose, **Remove accounts**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4966-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4966-141">Related topics</span></span>

[<span data-ttu-id="b4966-142">Utilisation de comptes prioritaires dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b4966-142">Using Priority Accounts in Microsoft 365</span></span>](https://techcommunity.microsoft.com/t5/microsoft-365-blog/using-priority-accounts-in-microsoft-365/ba-p/1873314)