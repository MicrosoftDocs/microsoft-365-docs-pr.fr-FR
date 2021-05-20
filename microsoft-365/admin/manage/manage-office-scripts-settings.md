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
description: Découvrez comment gérer les paramètres Office scripts pour les utilisateurs de votre organisation.
ms.openlocfilehash: e0cb52c4a8f48ff2310c83ffce61e08a0236ed59
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52572308"
---
# <a name="manage-office-scripts-settings"></a><span data-ttu-id="010d9-103">Gérer les paramètres de Office Scripts</span><span class="sxs-lookup"><span data-stu-id="010d9-103">Manage Office Scripts settings</span></span>

<span data-ttu-id="010d9-104">[Office scripts permet aux utilisateurs](/office/dev/scripts)d’automatiser les tâches en enregistrant, éditant et exécutant des scripts Excel sur le Web.</span><span class="sxs-lookup"><span data-stu-id="010d9-104">[Office Scripts](/office/dev/scripts)‎ allows users to automate tasks by recording, editing, and running scripts in ‎Excel‎ on the web.</span></span> <span data-ttu-id="010d9-105">Office Scripts fonctionne avec Power Automate, et les utilisateurs exécutent des scripts sur les cahiers de travail en utilisant le connecteur Excel en ligne (Business).</span><span class="sxs-lookup"><span data-stu-id="010d9-105">‎Office Scripts‎ works with Power Automate, and users run scripts on workbooks by using the ‎Excel‎ Online (Business) connector.</span></span> <span data-ttu-id="010d9-106">Microsoft 365 administrateurs peuvent gérer les paramètres Office scripts à partir du centre d Microsoft 365'administration.</span><span class="sxs-lookup"><span data-stu-id="010d9-106">Microsoft 365 admins can manage Office Scripts settings from the Microsoft 365 admin center.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="010d9-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="010d9-107">Before you begin</span></span>

- <span data-ttu-id="010d9-108">Pour gérer Office paramètres scripts, vous devez être un administrateur global. Pour plus d’informations, voir [Sur les rôles admin](../add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="010d9-108">To manage Office Scripts settings, you must be a Global admin. For more information, see [About admin roles](../add-users/about-admin-roles.md).</span></span>

- <span data-ttu-id="010d9-109">Assurez-vous que les utilisateurs de votre organisation ont une licence valide pour un plan commercial ou UDI Microsoft 365 ou Office 365 qui inclut l’accès à des applications de bureau Office, telles que l’un des plans suivants :</span><span class="sxs-lookup"><span data-stu-id="010d9-109">Ensure users in your organization have a valid license for a Microsoft 365 or Office 365 commercial or EDU plan that includes access to Office desktop apps, such as one of the following plans:</span></span>

    - <span data-ttu-id="010d9-110">Microsoft 365 Business Standard</span><span class="sxs-lookup"><span data-stu-id="010d9-110">Microsoft 365 Business Standard</span></span>
    - <span data-ttu-id="010d9-111">Applications Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="010d9-111">Microsoft 365 Apps for business</span></span>
    - <span data-ttu-id="010d9-112">Microsoft 365 Apps for enterprise</span><span class="sxs-lookup"><span data-stu-id="010d9-112">Microsoft 365 Apps for enterprise</span></span>
    - <span data-ttu-id="010d9-113">Office 365 E3</span><span class="sxs-lookup"><span data-stu-id="010d9-113">Office 365 E3</span></span>
    - <span data-ttu-id="010d9-114">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="010d9-114">Office 365 E5</span></span>
    - <span data-ttu-id="010d9-115">Office 365 A3</span><span class="sxs-lookup"><span data-stu-id="010d9-115">Office 365 A3</span></span>
    - <span data-ttu-id="010d9-116">Office 365 A5</span><span class="sxs-lookup"><span data-stu-id="010d9-116">Office 365 A5</span></span>

## <a name="manage-availability-of-office-scripts-and-sharing-of-scripts"></a><span data-ttu-id="010d9-117">Gérer la disponibilité Office scripts et le partage de scripts</span><span class="sxs-lookup"><span data-stu-id="010d9-117">Manage availability of Office Scripts and sharing of scripts</span></span>

1. <span data-ttu-id="010d9-118">Dans le Microsoft 365 d’administration, rendez-vous sur **l’onglet Paramètres** \> **paramètres Org** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2053743" target="_blank">Services.</a></span><span class="sxs-lookup"><span data-stu-id="010d9-118">In the Microsoft 365 admin center, go to the **Settings** \> **Org settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2053743" target="_blank">Services</a> tab.</span></span>

2. <span data-ttu-id="010d9-119">Sélectionnez **Office scripts**.</span><span class="sxs-lookup"><span data-stu-id="010d9-119">Select **Office Scripts**.</span></span>

3. <span data-ttu-id="010d9-120">Office Les scripts sont activés par défaut, et tous les membres de votre organisation peuvent accéder et utiliser la fonctionnalité et partager des scripts.</span><span class="sxs-lookup"><span data-stu-id="010d9-120">Office Scripts is turned on by default, and everyone in your organization can access and use the feature and share scripts.</span></span> <span data-ttu-id="010d9-121">Pour désactiver les Office pour votre organisation, effacer les utilisateurs **Let automatiser leurs tâches dans la case Excel sur le Web** cochée.</span><span class="sxs-lookup"><span data-stu-id="010d9-121">To turn off Office Scripts for your organization, clear the **Let users automate their tasks in Excel on the web** check box.</span></span>

4. <span data-ttu-id="010d9-122">Si vous avez déjà désactivé les scripts Office pour votre organisation et que vous souhaitez l’activer, **sélectionnez Laissez les utilisateurs automatiser leurs tâches en Excel sur le Web,** puis spécifiez qui peut accéder et utiliser la fonctionnalité :</span><span class="sxs-lookup"><span data-stu-id="010d9-122">If you previously turned off Office Scripts for your organization and you want to turn it back on, select **Let users automate their tasks in Excel on the web**, and then specify who can access and use the feature:</span></span>

    - <span data-ttu-id="010d9-123">Pour permettre à tous les utilisateurs de votre organisation d’accéder et d’utiliser Office scripts, **laissez Tout le** monde (par défaut) sélectionné.</span><span class="sxs-lookup"><span data-stu-id="010d9-123">To allow all users in your organization to access and use Office Scripts, leave **Everyone** (the default) selected.</span></span>

    - <span data-ttu-id="010d9-124">Pour permettre aux membres d’un groupe spécifique d’accéder et d’utiliser Office Scripts, **sélectionnez Groupe spécifique,** puis entrez le nom ou l’alias e-mail du groupe pour l’ajouter à la liste de permis.</span><span class="sxs-lookup"><span data-stu-id="010d9-124">To allow only members of a specific group to access and use Office Scripts, select **Specific group**, and then enter the name or email alias of the group to add it to the allow list.</span></span> <span data-ttu-id="010d9-125">Vous pouvez ajouter un seul groupe à la liste d’autoriser, et il doit être l’un des types suivants:</span><span class="sxs-lookup"><span data-stu-id="010d9-125">You may add only one group to the allow list, and it must be one of the following types:</span></span>
        - <span data-ttu-id="010d9-126">Microsoft 365 groupe</span><span class="sxs-lookup"><span data-stu-id="010d9-126">Microsoft 365 group</span></span>
        - <span data-ttu-id="010d9-127">Groupe de distribution</span><span class="sxs-lookup"><span data-stu-id="010d9-127">Distribution group</span></span>
        - <span data-ttu-id="010d9-128">Groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="010d9-128">Security group</span></span>
        - <span data-ttu-id="010d9-129">Groupe de sécurité à extension messagerie</span><span class="sxs-lookup"><span data-stu-id="010d9-129">Mail-enabled security group</span></span>
    
        <span data-ttu-id="010d9-130">Pour en savoir plus sur les différents types de groupes, consultez [Comparez les groupes](../create-groups/compare-groups.md).</span><span class="sxs-lookup"><span data-stu-id="010d9-130">To learn more about the different types of groups, see [Compare groups](../create-groups/compare-groups.md).</span></span>

5. <span data-ttu-id="010d9-131">Pour permettre aux utilisateurs ayant accès à Office Scripts de partager leurs scripts avec d’autres membres de votre organisation, **sélectionnez Laissez les utilisateurs ayant accès à Office Scripts partager leurs scripts avec d’autres membres de l’organisation.**</span><span class="sxs-lookup"><span data-stu-id="010d9-131">To allow users with access to Office Scripts to share their scripts with others in your organization, select **Let users with access to Office Scripts share their scripts with others in the organization**.</span></span> <span data-ttu-id="010d9-132">Le partage de scripts en dehors d’une organisation n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="010d9-132">Sharing scripts outside of an organization is not allowed.</span></span>
 
    > [!NOTE]
    > <span data-ttu-id="010d9-133">Si vous éteignez plus tard le partage de script pour votre organisation, les utilisateurs pourront toujours exécuter des scripts précédemment partagés.</span><span class="sxs-lookup"><span data-stu-id="010d9-133">If you later turn off script sharing for your organization, users will still be able to run previously-shared scripts.</span></span>
 
6. <span data-ttu-id="010d9-134">Spécifiez quels utilisateurs ayant accès Office scripts peuvent partager leurs scripts :</span><span class="sxs-lookup"><span data-stu-id="010d9-134">Specify which users with access to Office Scripts can share their scripts:</span></span>
    
    - <span data-ttu-id="010d9-135">Pour permettre à tous les utilisateurs ayant accès Office scripts de partager leurs scripts, laissez **Tout le monde** (par défaut) sélectionné.</span><span class="sxs-lookup"><span data-stu-id="010d9-135">To allow all users with access to Office Scripts to share their scripts, leave **Everyone** (the default) selected.</span></span>

    - <span data-ttu-id="010d9-136">Pour permettre aux membres d’un groupe spécifique ayant accès à Office Scripts de partager leurs scripts, sélectionnez **Groupe spécifique,** puis entrez le nom ou l’alias e-mail du groupe pour l’ajouter à la liste d’autoriser.</span><span class="sxs-lookup"><span data-stu-id="010d9-136">To allow only members of a specific group with access to Office Scripts to share their scripts, select **Specific group**, and then enter the name or email alias of the group to add it to the allow list.</span></span> <span data-ttu-id="010d9-137">Vous pouvez ajouter un seul groupe à la liste d’autoriser, et il doit être l’un des types suivants:</span><span class="sxs-lookup"><span data-stu-id="010d9-137">You may add only one group to the allow list, and it must be one of the following types:</span></span>
        - <span data-ttu-id="010d9-138">Microsoft 365 groupe</span><span class="sxs-lookup"><span data-stu-id="010d9-138">Microsoft 365 group</span></span>
        - <span data-ttu-id="010d9-139">Groupe de distribution</span><span class="sxs-lookup"><span data-stu-id="010d9-139">Distribution group</span></span>
        - <span data-ttu-id="010d9-140">Groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="010d9-140">Security group</span></span>
        - <span data-ttu-id="010d9-141">Groupe de sécurité à extension messagerie</span><span class="sxs-lookup"><span data-stu-id="010d9-141">Mail-enabled security group</span></span>
    
        <span data-ttu-id="010d9-142">Pour en savoir plus sur les différents types de groupes, consultez [Comparez les groupes](../create-groups/compare-groups.md).</span><span class="sxs-lookup"><span data-stu-id="010d9-142">To learn more about the different types of groups, see [Compare groups](../create-groups/compare-groups.md).</span></span>

7. <span data-ttu-id="010d9-143">Pour permettre aux utilisateurs d’exécuter leurs scripts Office à l’intérieur des flux Power Automate, **sélectionnez Laissez les utilisateurs ayant accès à Office Scripts** exécuter leurs scripts avec Power Automate .</span><span class="sxs-lookup"><span data-stu-id="010d9-143">To allow users to run their Office Scripts inside Power Automate flows, select **Let users with access to Office Scripts run their scripts with Power Automate**.</span></span> <span data-ttu-id="010d9-144">Cela permet aux utilisateurs d’ajouter des étapes de [flux avec l’option Excel](/connectors/excelonlinebusiness) de **script** Run de Connector en ligne (Business).</span><span class="sxs-lookup"><span data-stu-id="010d9-144">This allows users to add flow steps with the [Excel Online (Business) Connector's](/connectors/excelonlinebusiness) **Run script** option.</span></span>

    - <span data-ttu-id="010d9-145">Pour permettre à tous les utilisateurs ayant accès Office scripts d’utiliser leurs scripts dans les flux, **laissez Tout le** monde (par défaut) sélectionné.</span><span class="sxs-lookup"><span data-stu-id="010d9-145">To allow all users with access to Office Scripts to use their scripts in flows, leave **Everyone** (the default) selected.</span></span>

    - <span data-ttu-id="010d9-146">Pour permettre aux membres d’un groupe spécifique ayant accès à Office Scripts d’utiliser leurs scripts dans les flux, sélectionnez **Groupe spécifique,** puis entrez le nom ou l’alias e-mail du groupe pour l’ajouter à la liste d’autoriser.</span><span class="sxs-lookup"><span data-stu-id="010d9-146">To allow only members of a specific group with access to Office Scripts to use their scripts in flows, select **Specific group**, and then enter the name or email alias of the group to add it to the allow list.</span></span> <span data-ttu-id="010d9-147">Vous pouvez ajouter un seul groupe à la liste d’autoriser, et il doit être l’un des types suivants:</span><span class="sxs-lookup"><span data-stu-id="010d9-147">You may add only one group to the allow list, and it must be one of the following types:</span></span>
        - <span data-ttu-id="010d9-148">Microsoft 365 groupe</span><span class="sxs-lookup"><span data-stu-id="010d9-148">Microsoft 365 group</span></span>
        - <span data-ttu-id="010d9-149">Groupe de distribution</span><span class="sxs-lookup"><span data-stu-id="010d9-149">Distribution group</span></span>
        - <span data-ttu-id="010d9-150">Groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="010d9-150">Security group</span></span>
        - <span data-ttu-id="010d9-151">Groupe de sécurité à extension messagerie</span><span class="sxs-lookup"><span data-stu-id="010d9-151">Mail-enabled security group</span></span>

        <span data-ttu-id="010d9-152">Pour en savoir plus sur les différents types de groupes, consultez [Comparez les groupes](../create-groups/compare-groups.md).</span><span class="sxs-lookup"><span data-stu-id="010d9-152">To learn more about the different types of groups, see [Compare groups](../create-groups/compare-groups.md).</span></span>

    - <span data-ttu-id="010d9-153">Pour en savoir plus sur l’utilisation Office scripts avec Power Automate, [consultez Exécuter Office scripts avec Power Automate](/office/dev/scripts/develop/power-automate-integration).</span><span class="sxs-lookup"><span data-stu-id="010d9-153">To learn more about using Office Scripts with Power Automate, see [Run Office Scripts with Power Automate](/office/dev/scripts/develop/power-automate-integration).</span></span>

8. <span data-ttu-id="010d9-154">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="010d9-154">Select **Save**.</span></span>

    <span data-ttu-id="010d9-155">L’entrée en vigueur des modifications apportées aux paramètres des scripts Office jusqu’à 48 heures peut prendre effet.</span><span class="sxs-lookup"><span data-stu-id="010d9-155">It can take up to 48 hours for changes to Office Scripts settings to take effect.</span></span>

## <a name="next-steps"></a><span data-ttu-id="010d9-156">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="010d9-156">Next steps</span></span>

<span data-ttu-id="010d9-157">Étant donné Office Scripts fonctionne avec Power Automate, nous vous recommandons d’examiner vos politiques existantes de prévention des pertes de données (DLP) pour vous assurer que les données de votre organisation restent protégées pendant que les utilisateurs utilisent Office Scripts.</span><span class="sxs-lookup"><span data-stu-id="010d9-157">Because Office Scripts works with Power Automate, we recommend that you review your existing data loss prevention (DLP) policies to ensure your organization's data remains protected while users use ‎Office Scripts‎.</span></span> <span data-ttu-id="010d9-158">Pour plus d’informations, [consultez les politiques de prévention des pertes de données (DLP).](/power-automate/prevent-data-loss)</span><span class="sxs-lookup"><span data-stu-id="010d9-158">For more information, see [Data loss prevention (DLP) policies](/power-automate/prevent-data-loss).</span></span>

## <a name="related-content"></a><span data-ttu-id="010d9-159">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="010d9-159">Related content</span></span>

<span data-ttu-id="010d9-160">[Office Documentation technique scripts (page](/office/dev/scripts/) de lien)</span><span class="sxs-lookup"><span data-stu-id="010d9-160">[Office Scripts technical documentation](/office/dev/scripts/) (link page)</span></span>\
<span data-ttu-id="010d9-161">[Introduction aux Office scripts dans Excel](https://support.microsoft.com/office/9fbe283d-adb8-4f13-a75b-a81c6baf163a) (article)</span><span class="sxs-lookup"><span data-stu-id="010d9-161">[Introduction to Office Scripts in Excel](https://support.microsoft.com/office/9fbe283d-adb8-4f13-a75b-a81c6baf163a) (article)</span></span>\
<span data-ttu-id="010d9-162">[Partage Office scripts en Excel pour le Web](https://support.microsoft.com/office/226eddbc-3a44-4540-acfe-fccda3d1122b) (article)</span><span class="sxs-lookup"><span data-stu-id="010d9-162">[Sharing Office Scripts in Excel for the Web](https://support.microsoft.com/office/226eddbc-3a44-4540-acfe-fccda3d1122b) (article)</span></span>\
<span data-ttu-id="010d9-163">[Enregistrer, modifier et créer des scripts Office dans Excel sur le Web](/office/dev/scripts/tutorials/excel-tutorial) (article)</span><span class="sxs-lookup"><span data-stu-id="010d9-163">[Record, edit, and create Office Scripts in Excel on the web](/office/dev/scripts/tutorials/excel-tutorial) (article)</span></span>
