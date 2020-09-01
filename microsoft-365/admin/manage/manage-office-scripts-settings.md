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
description: Découvrez comment gérer les paramètres des scripts Office pour les utilisateurs de votre organisation.
ms.openlocfilehash: 44e2a5c0e0577db344fdbb00a110674df3e71bdc
ms.sourcegitcommit: 04f196528a7a91b404478553433af3fa94d7eee7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "47317492"
---
# <a name="manage-office-scripts-settings"></a><span data-ttu-id="c38c5-103">Gérer les paramètres de Office Scripts</span><span class="sxs-lookup"><span data-stu-id="c38c5-103">Manage Office Scripts settings</span></span>

<span data-ttu-id="c38c5-104">Les scripts Office permettent aux utilisateurs d’automatiser des tâches en enregistrant, modifiant et exécutant des scripts dans Excel sur le Web.</span><span class="sxs-lookup"><span data-stu-id="c38c5-104">Office Scripts‎ allows users to automate tasks by recording, editing, and running scripts in ‎Excel‎ on the web.</span></span> <span data-ttu-id="c38c5-105">Les scripts Office fonctionnent avec Power automate, et les utilisateurs exécutent des scripts sur des classeurs à l’aide du connecteur Excel Online (Business).</span><span class="sxs-lookup"><span data-stu-id="c38c5-105">‎Office Scripts‎ works with Power Automate, and users run scripts on workbooks by using the ‎Excel‎ Online (Business) connector.</span></span> <span data-ttu-id="c38c5-106">Les administrateurs 365 de Microsoft peuvent gérer les paramètres des scripts Office à partir du centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c38c5-106">Microsoft 365 admins can manage Office Scripts settings from the Microsoft 365 admin center.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="c38c5-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="c38c5-107">Before you begin</span></span>

- <span data-ttu-id="c38c5-108">Pour gérer les paramètres des scripts Office, vous devez être un administrateur général. Pour plus d’informations, consultez la rubrique [à propos des rôles d’administrateur](../add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="c38c5-108">To manage Office Scripts settings, you must be a Global admin. For more information, see [About admin roles](../add-users/about-admin-roles.md).</span></span>

- <span data-ttu-id="c38c5-109">Assurez-vous que les utilisateurs de votre organisation disposent d’une licence valide pour un plan commercial ou EDU Microsoft 365 ou Office 365 qui inclut l’accès aux applications de bureau Office, telles que l’un des plans suivants :</span><span class="sxs-lookup"><span data-stu-id="c38c5-109">Ensure users in your organization have a valid license for a Microsoft 365 or Office 365 commercial or EDU plan that includes access to Office desktop apps, such as one of the following plans:</span></span>

    - <span data-ttu-id="c38c5-110">Microsoft 365 Business Standard</span><span class="sxs-lookup"><span data-stu-id="c38c5-110">Microsoft 365 Business Standard</span></span>
    - <span data-ttu-id="c38c5-111">Applications Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="c38c5-111">Microsoft 365 Apps for business</span></span>
    - <span data-ttu-id="c38c5-112">Applications Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="c38c5-112">Microsoft 365 Apps for enterprise</span></span>
    - <span data-ttu-id="c38c5-113">Office 365 E3</span><span class="sxs-lookup"><span data-stu-id="c38c5-113">Office 365 E3</span></span>
    - <span data-ttu-id="c38c5-114">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="c38c5-114">Office 365 E5</span></span>
    - <span data-ttu-id="c38c5-115">Office 365 A3</span><span class="sxs-lookup"><span data-stu-id="c38c5-115">Office 365 A3</span></span>
    - <span data-ttu-id="c38c5-116">Office 365 A5</span><span class="sxs-lookup"><span data-stu-id="c38c5-116">Office 365 A5</span></span>

## <a name="manage-availability-of-office-scripts-and-sharing-of-scripts"></a><span data-ttu-id="c38c5-117">Gestion de la disponibilité des scripts et du partage de scripts Office</span><span class="sxs-lookup"><span data-stu-id="c38c5-117">Manage availability of Office Scripts and sharing of scripts</span></span>

1. <span data-ttu-id="c38c5-118">Dans le centre d’administration Microsoft 365, accédez à **l'** \> **Org settings** \> onglet <a href="https://go.microsoft.com/fwlink/p/?linkid=2053743" target="_blank">services</a> de paramètres d’organisation.</span><span class="sxs-lookup"><span data-stu-id="c38c5-118">In the Microsoft 365 admin center, go to the **Settings** \> **Org settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2053743" target="_blank">Services</a> tab.</span></span>

2. <span data-ttu-id="c38c5-119">Sélectionnez **scripts Office**.</span><span class="sxs-lookup"><span data-stu-id="c38c5-119">Select **Office Scripts**.</span></span>

3. <span data-ttu-id="c38c5-120">Les scripts Office sont activés par défaut et tous les membres de votre organisation peuvent accéder et utiliser les scripts de fonctionnalité et de partage.</span><span class="sxs-lookup"><span data-stu-id="c38c5-120">Office Scripts is turned on by default, and everyone in your organization can access and use the feature and share scripts.</span></span> <span data-ttu-id="c38c5-121">Pour désactiver les scripts Office pour votre organisation, désactivez la case à cocher **autoriser les utilisateurs à automatiser leurs tâches dans Excel sur le Web** .</span><span class="sxs-lookup"><span data-stu-id="c38c5-121">To turn off Office Scripts for your organization, clear the **Let users automate their tasks in Excel on the web** check box.</span></span>

4. <span data-ttu-id="c38c5-122">Si vous avez précédemment désactivé les scripts Office pour votre organisation et que vous souhaitez le réactiver, sélectionnez **autoriser les utilisateurs à automatiser leurs tâches dans Excel sur le Web**, puis indiquez qui peut accéder à la fonctionnalité et comment l’utiliser :</span><span class="sxs-lookup"><span data-stu-id="c38c5-122">If you previously turned off Office Scripts for your organization and you want to turn it back on, select **Let users automate their tasks in Excel on the web**, and then specify who can access and use the feature:</span></span>

    - <span data-ttu-id="c38c5-123">Pour autoriser tous les utilisateurs de votre organisation à accéder et à utiliser des scripts Office, laissez **tout le monde** (valeur par défaut) sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="c38c5-123">To allow all users in your organization to access and use Office Scripts, leave **Everyone** (the default) selected.</span></span> 

    - <span data-ttu-id="c38c5-124">Pour autoriser uniquement les membres d’un groupe spécifique à accéder à des scripts Office et à les utiliser, sélectionnez **groupe spécifique**, puis entrez le nom ou l’alias de messagerie du groupe pour l’ajouter à la liste verte.</span><span class="sxs-lookup"><span data-stu-id="c38c5-124">To allow only members of a specific group to access and use Office Scripts, select **Specific group**, and then enter the name or email alias of the group to add it to the allow list.</span></span> <span data-ttu-id="c38c5-125">Vous pouvez ajouter un seul groupe à la liste verte, et il doit s’agir de l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="c38c5-125">You may add only one group to the allow list, and it must be one of the following types:</span></span>
        - <span data-ttu-id="c38c5-126">Groupe Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="c38c5-126">Microsoft 365 group</span></span>
        - <span data-ttu-id="c38c5-127">Groupe de distribution</span><span class="sxs-lookup"><span data-stu-id="c38c5-127">Distribution group</span></span>
        - <span data-ttu-id="c38c5-128">Groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="c38c5-128">Security group</span></span>
        - <span data-ttu-id="c38c5-129">Groupe de sécurité à extension messagerie</span><span class="sxs-lookup"><span data-stu-id="c38c5-129">Mail-enabled security group</span></span>
    
        <span data-ttu-id="c38c5-130">Pour en savoir plus sur les différents types de groupes, consultez la rubrique [compare Groups](../create-groups/compare-groups.md).</span><span class="sxs-lookup"><span data-stu-id="c38c5-130">To learn more about the different types of groups, see [Compare groups](../create-groups/compare-groups.md).</span></span>

5. <span data-ttu-id="c38c5-131">Pour permettre aux utilisateurs disposant d’un accès à des scripts Office de partager leurs scripts avec d’autres membres de votre organisation, sélectionnez **permettre aux utilisateurs ayant accès à des scripts Office de partager leurs scripts avec d’autres membres de l’organisation**.</span><span class="sxs-lookup"><span data-stu-id="c38c5-131">To allow users with access to Office Scripts to share their scripts with others in your organization, select **Let users with access to Office Scripts share their scripts with others in the organization**.</span></span> <span data-ttu-id="c38c5-132">Les scripts de partage en dehors d’une organisation ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="c38c5-132">Sharing scripts outside of an organization is not allowed.</span></span>
 
    > [!NOTE]
    > <span data-ttu-id="c38c5-133">Si, par la suite, vous désactivez le partage de script pour votre organisation, les utilisateurs pourront toujours exécuter des scripts déjà partagés.</span><span class="sxs-lookup"><span data-stu-id="c38c5-133">If you later turn off script sharing for your organization, users will still be able to run previously-shared scripts.</span></span>
 
6. <span data-ttu-id="c38c5-134">Spécifier les utilisateurs ayant accès aux scripts Office peuvent partager leurs scripts :</span><span class="sxs-lookup"><span data-stu-id="c38c5-134">Specify which users with access to Office Scripts can share their scripts:</span></span>
    
    - <span data-ttu-id="c38c5-135">Pour permettre à tous les utilisateurs ayant accès aux scripts Office de partager leurs scripts, laissez **tout le monde** (valeur par défaut) sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="c38c5-135">To allow all users with access to Office Scripts to share their scripts, leave **Everyone** (the default) selected.</span></span>

    - <span data-ttu-id="c38c5-136">Pour autoriser uniquement les membres d’un groupe spécifique à accéder aux scripts Office afin de partager leurs scripts, sélectionnez **groupe spécifique**, puis entrez le nom ou l’alias de messagerie du groupe pour l’ajouter à la liste verte.</span><span class="sxs-lookup"><span data-stu-id="c38c5-136">To allow only members of a specific group with access to Office Scripts to share their scripts, select **Specific group**, and then enter the name or email alias of the group to add it to the allow list.</span></span> <span data-ttu-id="c38c5-137">Vous pouvez ajouter un seul groupe à la liste verte, et il doit s’agir de l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="c38c5-137">You may add only one group to the allow list, and it must be one of the following types:</span></span>
        - <span data-ttu-id="c38c5-138">Groupe Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="c38c5-138">Microsoft 365 group</span></span>
        - <span data-ttu-id="c38c5-139">Groupe de distribution</span><span class="sxs-lookup"><span data-stu-id="c38c5-139">Distribution group</span></span>
        - <span data-ttu-id="c38c5-140">Groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="c38c5-140">Security group</span></span>
        - <span data-ttu-id="c38c5-141">Groupe de sécurité à extension messagerie</span><span class="sxs-lookup"><span data-stu-id="c38c5-141">Mail-enabled security group</span></span>
    
        <span data-ttu-id="c38c5-142">Pour en savoir plus sur les différents types de groupes, consultez la rubrique [compare Groups](../create-groups/compare-groups.md).</span><span class="sxs-lookup"><span data-stu-id="c38c5-142">To learn more about the different types of groups, see [Compare groups](../create-groups/compare-groups.md).</span></span>

7. <span data-ttu-id="c38c5-143">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c38c5-143">Select **Save**.</span></span>

    <span data-ttu-id="c38c5-144">L’application des modifications apportées aux paramètres des scripts Office peut prendre jusqu’à 48 heures.</span><span class="sxs-lookup"><span data-stu-id="c38c5-144">It can take up to 48 hours for changes to Office Scripts settings to take effect.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c38c5-145">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="c38c5-145">Next steps</span></span>

<span data-ttu-id="c38c5-146">Étant donné que les scripts Office fonctionnent avec Power Automated, nous vous recommandons de consulter vos stratégies de protection contre la perte de données (DLP) existantes pour vous assurer que les données de votre organisation restent protégées pendant que les utilisateurs utilisent des scripts Office.</span><span class="sxs-lookup"><span data-stu-id="c38c5-146">Because Office Scripts works with Power Automate, we recommend that you review your existing data loss prevention (DLP) policies to ensure your organization's data remains protected while users use ‎Office Scripts‎.</span></span> <span data-ttu-id="c38c5-147">Pour plus d’informations, consultez la rubrique [stratégies de protection contre la perte de données (DLP)](/power-automate/prevent-data-loss).</span><span class="sxs-lookup"><span data-stu-id="c38c5-147">For more information, see [Data loss prevention (DLP) policies](/power-automate/prevent-data-loss).</span></span>

## <a name="related-content"></a><span data-ttu-id="c38c5-148">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="c38c5-148">Related content</span></span>

<span data-ttu-id="c38c5-149">[Documentation technique relative aux scripts Office](/office/dev/scripts/) (page lien) </span><span class="sxs-lookup"><span data-stu-id="c38c5-149">[Office Scripts technical documentation](/office/dev/scripts/) (link page)</span></span>\
<span data-ttu-id="c38c5-150">[Introduction aux scripts Office dans Excel](https://support.microsoft.com/office/9fbe283d-adb8-4f13-a75b-a81c6baf163a) (article) </span><span class="sxs-lookup"><span data-stu-id="c38c5-150">[Introduction to Office Scripts in Excel](https://support.microsoft.com/office/9fbe283d-adb8-4f13-a75b-a81c6baf163a) (article)</span></span>\
<span data-ttu-id="c38c5-151">[Partage de scripts Office dans Excel pour le Web](https://support.microsoft.com/office/226eddbc-3a44-4540-acfe-fccda3d1122b) (article) </span><span class="sxs-lookup"><span data-stu-id="c38c5-151">[Sharing Office Scripts in Excel for the Web](https://support.microsoft.com/office/226eddbc-3a44-4540-acfe-fccda3d1122b) (article)</span></span>\
<span data-ttu-id="c38c5-152">[Enregistrer, modifier et créer des scripts Office dans Excel sur le Web](/office/dev/scripts/tutorials/excel-tutorial) (article)</span><span class="sxs-lookup"><span data-stu-id="c38c5-152">[Record, edit, and create Office Scripts in Excel on the web](/office/dev/scripts/tutorials/excel-tutorial) (article)</span></span>