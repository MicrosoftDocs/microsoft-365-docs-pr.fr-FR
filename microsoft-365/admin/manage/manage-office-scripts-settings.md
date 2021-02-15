---
title: Gérer les paramètres de Office Scripts
f1.keywords:
- NOCSH
ms.author: sharik
author: SKjerland
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid: MET150
description: Découvrez comment gérer les paramètres d’Office Scripts pour les utilisateurs de votre organisation.
ms.openlocfilehash: 75d0a9d9e98652fc11eab7e8a7d6c826be031f6e
ms.sourcegitcommit: 50f10d83fa21db8572adab90784146e5231e3321
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2021
ms.locfileid: "50058422"
---
# <a name="manage-office-scripts-settings"></a><span data-ttu-id="b0d12-103">Gérer les paramètres de Office Scripts</span><span class="sxs-lookup"><span data-stu-id="b0d12-103">Manage Office Scripts settings</span></span>

<span data-ttu-id="b0d12-104">Les scripts Office permettent aux utilisateurs d’automatiser les tâches en enregistrant, en éditant et en exécutant des scripts dans Excel sur le web.</span><span class="sxs-lookup"><span data-stu-id="b0d12-104">Office Scripts‎ allows users to automate tasks by recording, editing, and running scripts in ‎Excel‎ on the web.</span></span> <span data-ttu-id="b0d12-105">Office Scripts fonctionne avec Power Automate et les utilisateurs exécutent des scripts sur des workbooks à l’aide du connecteur Excel Online (Entreprise).</span><span class="sxs-lookup"><span data-stu-id="b0d12-105">‎Office Scripts‎ works with Power Automate, and users run scripts on workbooks by using the ‎Excel‎ Online (Business) connector.</span></span> <span data-ttu-id="b0d12-106">Les administrateurs Microsoft 365 peuvent gérer les paramètres des scripts Office à partir du Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b0d12-106">Microsoft 365 admins can manage Office Scripts settings from the Microsoft 365 admin center.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="b0d12-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b0d12-107">Before you begin</span></span>

- <span data-ttu-id="b0d12-108">Pour gérer les paramètres d’Office Scripts, vous devez être administrateur général. Pour plus d’informations, voir [à propos des rôles d’administrateur.](../add-users/about-admin-roles.md)</span><span class="sxs-lookup"><span data-stu-id="b0d12-108">To manage Office Scripts settings, you must be a Global admin. For more information, see [About admin roles](../add-users/about-admin-roles.md).</span></span>

- <span data-ttu-id="b0d12-109">Assurez-vous que les utilisateurs de votre organisation ont une licence valide pour un plan Microsoft 365 ou Office 365 commercial ou EDU qui inclut l’accès aux applications de bureau Office, telles que l’un des plans suivants :</span><span class="sxs-lookup"><span data-stu-id="b0d12-109">Ensure users in your organization have a valid license for a Microsoft 365 or Office 365 commercial or EDU plan that includes access to Office desktop apps, such as one of the following plans:</span></span>

    - <span data-ttu-id="b0d12-110">Microsoft 365 Business Standard</span><span class="sxs-lookup"><span data-stu-id="b0d12-110">Microsoft 365 Business Standard</span></span>
    - <span data-ttu-id="b0d12-111">Applications Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="b0d12-111">Microsoft 365 Apps for business</span></span>
    - <span data-ttu-id="b0d12-112">Applications Microsoft 365 for entreprise</span><span class="sxs-lookup"><span data-stu-id="b0d12-112">Microsoft 365 Apps for enterprise</span></span>
    - <span data-ttu-id="b0d12-113">Office 365 E3</span><span class="sxs-lookup"><span data-stu-id="b0d12-113">Office 365 E3</span></span>
    - <span data-ttu-id="b0d12-114">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="b0d12-114">Office 365 E5</span></span>
    - <span data-ttu-id="b0d12-115">Office 365 A3</span><span class="sxs-lookup"><span data-stu-id="b0d12-115">Office 365 A3</span></span>
    - <span data-ttu-id="b0d12-116">Office 365 A5</span><span class="sxs-lookup"><span data-stu-id="b0d12-116">Office 365 A5</span></span>

## <a name="manage-availability-of-office-scripts-and-sharing-of-scripts"></a><span data-ttu-id="b0d12-117">Gérer la disponibilité des scripts Office et le partage des scripts</span><span class="sxs-lookup"><span data-stu-id="b0d12-117">Manage availability of Office Scripts and sharing of scripts</span></span>

1. <span data-ttu-id="b0d12-118">Dans le Centre d’administration Microsoft 365, go to the **Settings** \> **Org settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2053743" target="_blank">Services</a> tab.</span><span class="sxs-lookup"><span data-stu-id="b0d12-118">In the Microsoft 365 admin center, go to the **Settings** \> **Org settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2053743" target="_blank">Services</a> tab.</span></span>

2. <span data-ttu-id="b0d12-119">Sélectionnez **Scripts Office**.</span><span class="sxs-lookup"><span data-stu-id="b0d12-119">Select **Office Scripts**.</span></span>

3. <span data-ttu-id="b0d12-120">Les scripts Office sont allumés par défaut, et tous les membres de votre organisation peuvent accéder à la fonctionnalité et les utiliser et partager des scripts.</span><span class="sxs-lookup"><span data-stu-id="b0d12-120">Office Scripts is turned on by default, and everyone in your organization can access and use the feature and share scripts.</span></span> <span data-ttu-id="b0d12-121">Pour désactiver les scripts Office pour votre organisation, désactiver la case à cocher Laisser les utilisateurs automatiser leurs tâches **dans Excel sur le web.**</span><span class="sxs-lookup"><span data-stu-id="b0d12-121">To turn off Office Scripts for your organization, clear the **Let users automate their tasks in Excel on the web** check box.</span></span>

4. <span data-ttu-id="b0d12-122">Si vous avez précédemment désactivé Les scripts Office pour votre organisation et que vous souhaitez le désactiver à nouveau, sélectionnez Laisser les utilisateurs automatiser leurs tâches dans **Excel sur le web,** puis spécifiez qui peut accéder à la fonctionnalité et l’utiliser :</span><span class="sxs-lookup"><span data-stu-id="b0d12-122">If you previously turned off Office Scripts for your organization and you want to turn it back on, select **Let users automate their tasks in Excel on the web**, and then specify who can access and use the feature:</span></span>

    - <span data-ttu-id="b0d12-123">Pour autoriser tous les utilisateurs de votre organisation à accéder aux scripts Office et à les utiliser, laissez Tout le monde **(par** défaut) sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b0d12-123">To allow all users in your organization to access and use Office Scripts, leave **Everyone** (the default) selected.</span></span>

    - <span data-ttu-id="b0d12-124">Pour autoriser uniquement les membres d’un groupe spécifique à accéder aux scripts Office et à les utiliser, sélectionnez Groupe **spécifique,** puis entrez le nom ou l’alias de messagerie du groupe pour l’ajouter à la liste d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b0d12-124">To allow only members of a specific group to access and use Office Scripts, select **Specific group**, and then enter the name or email alias of the group to add it to the allow list.</span></span> <span data-ttu-id="b0d12-125">Vous ne pouvez ajouter qu’un seul groupe à la liste d’utilisateurs et il doit s’agit de l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="b0d12-125">You may add only one group to the allow list, and it must be one of the following types:</span></span>
        - <span data-ttu-id="b0d12-126">Groupe Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b0d12-126">Microsoft 365 group</span></span>
        - <span data-ttu-id="b0d12-127">Groupe de distribution</span><span class="sxs-lookup"><span data-stu-id="b0d12-127">Distribution group</span></span>
        - <span data-ttu-id="b0d12-128">Groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="b0d12-128">Security group</span></span>
        - <span data-ttu-id="b0d12-129">Groupe de sécurité à extension messagerie</span><span class="sxs-lookup"><span data-stu-id="b0d12-129">Mail-enabled security group</span></span>
    
        <span data-ttu-id="b0d12-130">Pour en savoir plus sur les différents types de groupes, voir [Comparer les groupes.](../create-groups/compare-groups.md)</span><span class="sxs-lookup"><span data-stu-id="b0d12-130">To learn more about the different types of groups, see [Compare groups](../create-groups/compare-groups.md).</span></span>

5. <span data-ttu-id="b0d12-131">Pour permettre aux utilisateurs ayant accès aux scripts Office de partager leurs scripts avec d’autres membres de votre organisation, sélectionnez Autoriser les utilisateurs ayant accès à Office Scripts à partager leurs scripts avec d’autres membres de **l’organisation.**</span><span class="sxs-lookup"><span data-stu-id="b0d12-131">To allow users with access to Office Scripts to share their scripts with others in your organization, select **Let users with access to Office Scripts share their scripts with others in the organization**.</span></span> <span data-ttu-id="b0d12-132">Le partage de scripts en dehors d’une organisation n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="b0d12-132">Sharing scripts outside of an organization is not allowed.</span></span>
 
    > [!NOTE]
    > <span data-ttu-id="b0d12-133">Si vous désactiverez ultérieurement le partage de scripts pour votre organisation, les utilisateurs pourront toujours exécuter des scripts précédemment partagés.</span><span class="sxs-lookup"><span data-stu-id="b0d12-133">If you later turn off script sharing for your organization, users will still be able to run previously-shared scripts.</span></span>
 
6. <span data-ttu-id="b0d12-134">Spécifiez les utilisateurs ayant accès aux scripts Office qui peuvent partager leurs scripts :</span><span class="sxs-lookup"><span data-stu-id="b0d12-134">Specify which users with access to Office Scripts can share their scripts:</span></span>
    
    - <span data-ttu-id="b0d12-135">Pour autoriser tous les utilisateurs ayant accès aux scripts Office à partager leurs scripts, laissez Tout le monde **(par** défaut) sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b0d12-135">To allow all users with access to Office Scripts to share their scripts, leave **Everyone** (the default) selected.</span></span>

    - <span data-ttu-id="b0d12-136">Pour autoriser uniquement les membres d’un groupe spécifique ayant accès aux scripts Office à partager leurs scripts, sélectionnez **Un** groupe spécifique, puis entrez le nom ou l’alias de messagerie du groupe pour l’ajouter à la liste d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b0d12-136">To allow only members of a specific group with access to Office Scripts to share their scripts, select **Specific group**, and then enter the name or email alias of the group to add it to the allow list.</span></span> <span data-ttu-id="b0d12-137">Vous ne pouvez ajouter qu’un seul groupe à la liste d’utilisateurs et il doit s’agit de l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="b0d12-137">You may add only one group to the allow list, and it must be one of the following types:</span></span>
        - <span data-ttu-id="b0d12-138">Groupe Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b0d12-138">Microsoft 365 group</span></span>
        - <span data-ttu-id="b0d12-139">Groupe de distribution</span><span class="sxs-lookup"><span data-stu-id="b0d12-139">Distribution group</span></span>
        - <span data-ttu-id="b0d12-140">Groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="b0d12-140">Security group</span></span>
        - <span data-ttu-id="b0d12-141">Groupe de sécurité à extension messagerie</span><span class="sxs-lookup"><span data-stu-id="b0d12-141">Mail-enabled security group</span></span>
    
        <span data-ttu-id="b0d12-142">Pour en savoir plus sur les différents types de groupes, voir [Comparer les groupes.](../create-groups/compare-groups.md)</span><span class="sxs-lookup"><span data-stu-id="b0d12-142">To learn more about the different types of groups, see [Compare groups](../create-groups/compare-groups.md).</span></span>

7. <span data-ttu-id="b0d12-143">Pour permettre aux utilisateurs d’exécuter leurs scripts Office à l’intérieur de flux Power Automate, sélectionnez Autoriser les utilisateurs ayant accès à Des scripts Office à exécuter leurs scripts avec **Power Automate.**</span><span class="sxs-lookup"><span data-stu-id="b0d12-143">To allow users to run their Office Scripts inside Power Automate flows, select **Let users with access to Office Scripts run their scripts with Power Automate**.</span></span> <span data-ttu-id="b0d12-144">Cela permet aux utilisateurs d’ajouter des étapes de flux avec l’option de **script** Exécuter [d’Excel Online (Business) Connector.](/connectors/excelonlinebusiness)</span><span class="sxs-lookup"><span data-stu-id="b0d12-144">This allows users to add flow steps with the [Excel Online (Business) Connector's](/connectors/excelonlinebusiness) **Run script** option.</span></span>

    - <span data-ttu-id="b0d12-145">Pour autoriser tous les utilisateurs ayant accès aux scripts Office à utiliser leurs scripts dans les flux, laissez Tout le monde **(par** défaut) sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b0d12-145">To allow all users with access to Office Scripts to use their scripts in flows, leave **Everyone** (the default) selected.</span></span>

    - <span data-ttu-id="b0d12-146">Pour autoriser uniquement les membres d’un groupe spécifique ayant accès aux scripts Office à utiliser leurs scripts dans les flux, sélectionnez Groupe **spécifique,** puis entrez le nom ou l’alias de messagerie du groupe pour l’ajouter à la liste d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b0d12-146">To allow only members of a specific group with access to Office Scripts to use their scripts in flows, select **Specific group**, and then enter the name or email alias of the group to add it to the allow list.</span></span> <span data-ttu-id="b0d12-147">Vous ne pouvez ajouter qu’un seul groupe à la liste d’utilisateurs et il doit s’agit de l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="b0d12-147">You may add only one group to the allow list, and it must be one of the following types:</span></span>
        - <span data-ttu-id="b0d12-148">Groupe Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b0d12-148">Microsoft 365 group</span></span>
        - <span data-ttu-id="b0d12-149">Groupe de distribution</span><span class="sxs-lookup"><span data-stu-id="b0d12-149">Distribution group</span></span>
        - <span data-ttu-id="b0d12-150">Groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="b0d12-150">Security group</span></span>
        - <span data-ttu-id="b0d12-151">Groupe de sécurité à extension messagerie</span><span class="sxs-lookup"><span data-stu-id="b0d12-151">Mail-enabled security group</span></span>

        <span data-ttu-id="b0d12-152">Pour en savoir plus sur les différents types de groupes, voir [Comparer les groupes.](../create-groups/compare-groups.md)</span><span class="sxs-lookup"><span data-stu-id="b0d12-152">To learn more about the different types of groups, see [Compare groups](../create-groups/compare-groups.md).</span></span>

    - <span data-ttu-id="b0d12-153">Pour en savoir plus sur l’utilisation des scripts Office avec Power Automate, notamment sur l’impact de vos stratégies de protection contre la perte de données, voir Exécuter des scripts Office avec [Power Automate.](/office/dev/scripts/develop/power-automate-integration)</span><span class="sxs-lookup"><span data-stu-id="b0d12-153">To learn more about using Office Scripts with Power Automate, including how your data loss prevention policies may be impacted, see [Run Office Scripts with Power Automate](/office/dev/scripts/develop/power-automate-integration).</span></span>

8. <span data-ttu-id="b0d12-154">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b0d12-154">Select **Save**.</span></span>

    <span data-ttu-id="b0d12-155">L’application des modifications apportées aux paramètres Office Scripts peut prendre jusqu’à 48 heures.</span><span class="sxs-lookup"><span data-stu-id="b0d12-155">It can take up to 48 hours for changes to Office Scripts settings to take effect.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b0d12-156">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="b0d12-156">Next steps</span></span>

<span data-ttu-id="b0d12-157">Étant donné que Les scripts Office fonctionnent avec Power Automate, nous vous recommandons de passer en revue vos stratégies de protection contre la perte de données (DLP) existantes pour vous assurer que les données de votre organisation restent protégées pendant que les utilisateurs utilisent Des scripts Office.</span><span class="sxs-lookup"><span data-stu-id="b0d12-157">Because Office Scripts works with Power Automate, we recommend that you review your existing data loss prevention (DLP) policies to ensure your organization's data remains protected while users use ‎Office Scripts‎.</span></span> <span data-ttu-id="b0d12-158">Pour plus d’informations, voir Stratégies de protection contre la perte de [données (DLP).](/power-automate/prevent-data-loss)</span><span class="sxs-lookup"><span data-stu-id="b0d12-158">For more information, see [Data loss prevention (DLP) policies](/power-automate/prevent-data-loss).</span></span>

## <a name="related-content"></a><span data-ttu-id="b0d12-159">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="b0d12-159">Related content</span></span>

<span data-ttu-id="b0d12-160">Documentation technique relative aux [scripts Office](/office/dev/scripts/) (page de liens)</span><span class="sxs-lookup"><span data-stu-id="b0d12-160">[Office Scripts technical documentation](/office/dev/scripts/) (link page)</span></span>\
<span data-ttu-id="b0d12-161">[Introduction aux scripts Office dans Excel](https://support.microsoft.com/office/9fbe283d-adb8-4f13-a75b-a81c6baf163a) (article)</span><span class="sxs-lookup"><span data-stu-id="b0d12-161">[Introduction to Office Scripts in Excel](https://support.microsoft.com/office/9fbe283d-adb8-4f13-a75b-a81c6baf163a) (article)</span></span>\
<span data-ttu-id="b0d12-162">[Partage de scripts Office dans Excel pour le Web](https://support.microsoft.com/office/226eddbc-3a44-4540-acfe-fccda3d1122b) (article)</span><span class="sxs-lookup"><span data-stu-id="b0d12-162">[Sharing Office Scripts in Excel for the Web](https://support.microsoft.com/office/226eddbc-3a44-4540-acfe-fccda3d1122b) (article)</span></span>\
<span data-ttu-id="b0d12-163">[Enregistrer, modifier et créer des scripts Office dans Excel sur le web](/office/dev/scripts/tutorials/excel-tutorial) (article)</span><span class="sxs-lookup"><span data-stu-id="b0d12-163">[Record, edit, and create Office Scripts in Excel on the web](/office/dev/scripts/tutorials/excel-tutorial) (article)</span></span>
