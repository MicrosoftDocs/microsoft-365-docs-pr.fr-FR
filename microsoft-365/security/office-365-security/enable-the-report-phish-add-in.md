---
title: Activer le module de signalement du hameçonnage
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Découvrez comment activer le module de signalement du hameçonnage pour Outlook et Outlook sur le web, pour des utilisateurs individuels ou pour l’ensemble de votre organisation.
ms.openlocfilehash: 44fa55a82462de336982d3af2e3996c14699fd7c
ms.sourcegitcommit: 686f192e1a650ec805fe8e908b46ca51771ed41f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52625388"
---
# <a name="enable-the-report-phishing-add-in"></a><span data-ttu-id="6f530-103">Activez le complément Signaler un message de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="6f530-103">Enable the Report Phishing add-in</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


> [!NOTE]
> <span data-ttu-id="6f530-104">Si vous êtes un administrateur d’une organisation Microsoft 365 avec des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="6f530-104">If you're an admin in a Microsoft 365 organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="6f530-105">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="6f530-105">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

<span data-ttu-id="6f530-106">Les add-ins Signaler les messages et signaler le hameçonnage pour Outlook et Outlook sur le web (anciennement appelés Outlook Web App) permettent aux utilisateurs de signaler facilement les faux positifs (messages électroniques de qualité marqués comme faux) ou les faux négatifs (courriers électroniques erronés autorisés) à Microsoft et à ses affiliés pour analyse.</span><span class="sxs-lookup"><span data-stu-id="6f530-106">The Report Message and Report Phishing add-ins for Outlook and Outlook on the web (formerly known as Outlook Web App) enable people to easily report false positives (good email marked as bad) or false negatives (bad email allowed) to Microsoft and its affiliates for analysis.</span></span>

<span data-ttu-id="6f530-107">Microsoft utilise ces soumissions pour améliorer l’efficacité des technologies de protection de la messagerie.</span><span class="sxs-lookup"><span data-stu-id="6f530-107">Microsoft uses these submissions to improve the effectiveness of email protection technologies.</span></span> <span data-ttu-id="6f530-108">Par exemple, supposons que des personnes signalent de nombreux messages à l’aide du module de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="6f530-108">For example, suppose that people are reporting many messages using the Report Phishing add-in.</span></span> <span data-ttu-id="6f530-109">Ces informations sont disponibles dans le Tableau [de bord de](security-dashboard.md) sécurité et d’autres rapports.</span><span class="sxs-lookup"><span data-stu-id="6f530-109">This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports.</span></span> <span data-ttu-id="6f530-110">L’équipe de sécurité de votre organisation peut utiliser ces informations pour indiquer que les stratégies anti-hameçonnage peuvent avoir besoin d’être mises à jour.</span><span class="sxs-lookup"><span data-stu-id="6f530-110">Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated.</span></span>

<span data-ttu-id="6f530-111">Vous pouvez installer le add-in Signaler le message ou Signaler le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="6f530-111">You can install either the Report Message or Report Phishing add-in.</span></span> <span data-ttu-id="6f530-112">Si vous souhaitez que vos utilisateurs signalent à la fois le courrier indésirable et les messages de hameçonnage, déployez le add-in Signaler un message dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6f530-112">If you want your users to report both spam and phishing messages, deploy the Report Message add-in in your organization.</span></span> <span data-ttu-id="6f530-113">Pour plus d’informations, [voir Activer le add-in Message de rapport.](enable-the-report-message-add-in.md)</span><span class="sxs-lookup"><span data-stu-id="6f530-113">For more information, see [Enable the Report Message add-in](enable-the-report-message-add-in.md).</span></span>

<span data-ttu-id="6f530-114">Le module de signalement du hameçonnage offre la possibilité de signaler uniquement les messages de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="6f530-114">The Report Phishing add-in provides the option to report only phishing messages.</span></span> <span data-ttu-id="6f530-115">Les administrateurs peuvent activer le module de signalement du hameçonnage pour l’organisation, et les utilisateurs individuels peuvent l’installer eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="6f530-115">Admins can enable the Report Phishing add-in for the organization, and individual users can install it for themselves.</span></span>

<span data-ttu-id="6f530-116">Si vous êtes un utilisateur individuel, vous pouvez activer le module de signalement du hameçonnage [pour vous-même.](#get-the-report-phishing-add-in-for-yourself)</span><span class="sxs-lookup"><span data-stu-id="6f530-116">If you're an individual user, you can [enable the Report Phishing add-in for yourself](#get-the-report-phishing-add-in-for-yourself).</span></span>

<span data-ttu-id="6f530-117">Si vous êtes administrateur général ou administrateur Exchange Online et que Exchange est configuré pour utiliser l’authentification OAuth, vous pouvez activer le module de signalement du hameçonnage pour votre [organisation.](#get-and-enable-the-report-phishing-add-in-for-your-organization)</span><span class="sxs-lookup"><span data-stu-id="6f530-117">If you're a global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Phishing add-in for your organization](#get-and-enable-the-report-phishing-add-in-for-your-organization).</span></span> <span data-ttu-id="6f530-118">Le rapport d’hameçonnage Add-In est désormais disponible via [le déploiement centralisé.](../../admin/manage/centralized-deployment-of-add-ins.md)</span><span class="sxs-lookup"><span data-stu-id="6f530-118">The Report Phishing Add-In is now available through [Centralized Deployment](../../admin/manage/centralized-deployment-of-add-ins.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="6f530-119">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="6f530-119">What do you need to know before you begin?</span></span>

- <span data-ttu-id="6f530-120">Le module de signalement du hameçonnage fonctionne avec la plupart Microsoft 365 abonnements et les produits suivants :</span><span class="sxs-lookup"><span data-stu-id="6f530-120">The Report Phishing add-in works with most Microsoft 365 subscriptions and the following products:</span></span>

  - <span data-ttu-id="6f530-121">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="6f530-121">Outlook on the web</span></span>
  - <span data-ttu-id="6f530-122">Outlook 2013 SP1 ou une ultérieure</span><span class="sxs-lookup"><span data-stu-id="6f530-122">Outlook 2013 SP1 or later</span></span>
  - <span data-ttu-id="6f530-123">Outlook 2016 pour Mac ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="6f530-123">Outlook 2016 for Mac or later</span></span>
  - <span data-ttu-id="6f530-124">Outlook incluses dans Microsoft 365 applications pour Enterprise</span><span class="sxs-lookup"><span data-stu-id="6f530-124">Outlook included with Microsoft 365 apps for Enterprise</span></span>
  - <span data-ttu-id="6f530-125">Outlook application pour iOS et Android</span><span class="sxs-lookup"><span data-stu-id="6f530-125">Outlook app for iOS and Android</span></span>

- <span data-ttu-id="6f530-126">Le module de signalement du hameçonnage n’est pas disponible pour les boîtes aux lettres partagées ou les boîtes aux lettres dans les organisations Exchange locales.</span><span class="sxs-lookup"><span data-stu-id="6f530-126">The Report Phishing add-in is not available for shared mailboxes or mailboxes in on-premises Exchange organizations.</span></span>

- <span data-ttu-id="6f530-127">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="6f530-127">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="6f530-128">Pour plus d’informations, voir [Stratégies d’envoi des utilisateurs.](user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="6f530-128">For more information, see [User submissions policies](user-submission.md).</span></span>

- <span data-ttu-id="6f530-129">Votre navigateur web existant doit fonctionner avec le module de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="6f530-129">Your existing web browser should work with the Report Phishing add-in.</span></span> <span data-ttu-id="6f530-130">Toutefois, si vous remarquez que le module n’est pas disponible ou ne fonctionne pas comme prévu, essayez un autre navigateur.</span><span class="sxs-lookup"><span data-stu-id="6f530-130">But, if you notice the add-in is not available or not working as expected, try a different browser.</span></span>

- <span data-ttu-id="6f530-131">Pour les installation organisationnelles, l’organisation doit être configurée pour utiliser l’authentification OAuth.</span><span class="sxs-lookup"><span data-stu-id="6f530-131">For organizational installs, the organization needs to be configured to use OAuth authentication.</span></span> <span data-ttu-id="6f530-132">Pour plus d’informations, [voir Determine if Centralized Deployment of add-ins works for your organization](../../admin/manage/centralized-deployment-of-add-ins.md).</span><span class="sxs-lookup"><span data-stu-id="6f530-132">For more information, see [Determine if Centralized Deployment of add-ins works for your organization](../../admin/manage/centralized-deployment-of-add-ins.md).</span></span>

- <span data-ttu-id="6f530-133">Les administrateurs doivent être membres du groupe de rôles Administrateurs globaux.</span><span class="sxs-lookup"><span data-stu-id="6f530-133">Admins need to be a member of the Global admins role group.</span></span> <span data-ttu-id="6f530-134">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="6f530-134">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="get-the-report-phishing-add-in-for-yourself"></a><span data-ttu-id="6f530-135">Obtenir le module de signalement du hameçonnage par vous-même</span><span class="sxs-lookup"><span data-stu-id="6f530-135">Get the Report Phishing add-in for yourself</span></span>

1. <span data-ttu-id="6f530-136">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Phishing add-in.</span><span class="sxs-lookup"><span data-stu-id="6f530-136">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Phishing add-in.</span></span>

2. <span data-ttu-id="6f530-137">Cliquez **sur GET IT NOW**.</span><span class="sxs-lookup"><span data-stu-id="6f530-137">Click **GET IT NOW**.</span></span>

3. <span data-ttu-id="6f530-138">Dans la boîte de dialogue qui s’affiche, examinez les conditions d’utilisation et la politique de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="6f530-138">In the dialog that appears, review the terms of use and privacy policy, and then click **Continue**.</span></span>

4. <span data-ttu-id="6f530-139">Connectez-vous à l’aide de votre compte scolaire ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour un usage personnel).</span><span class="sxs-lookup"><span data-stu-id="6f530-139">Sign in using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>

<span data-ttu-id="6f530-140">Une fois le add-in installé et activé, les icônes suivantes s’offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="6f530-140">After the add-in is installed and enabled, you'll see the following icons:</span></span>

- <span data-ttu-id="6f530-141">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="6f530-141">In Outlook, the icon looks like this:</span></span>

  ![Icône signaler le hameçonnage du Outlook](../../media/Outlook-ReportPhishing.png)

- <span data-ttu-id="6f530-143">Dans Outlook sur le web, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="6f530-143">In Outlook on the web, the icon looks like this:</span></span>

  ![Outlook sur l’icône du add-in Rapport de hameçonnage sur le web](../../media/OWA-ReportPhishing.png)

## <a name="get-and-enable-the-report-phishing-add-in-for-your-organization"></a><span data-ttu-id="6f530-145">Obtenir et activer le module de signalement du hameçonnage pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="6f530-145">Get and enable the Report Phishing add-in for your organization</span></span>

> [!NOTE]
> <span data-ttu-id="6f530-146">L’apparition du module dans votre organisation peut prendre jusqu’à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="6f530-146">It could take up to 12 hours for the add-in to appear in your organization.</span></span>

1. <span data-ttu-id="6f530-147">Dans le Centre d’administration Microsoft 365,  \> **rendez-vous** sur la page Des applications Paramètres à l’adresse suivante : Si vous ne voyez pas la page Des applications intégrées, consultez le lien Paramètres Applications intégrées en haut de la page Applications <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>   \>  \> **intégrées.** </span><span class="sxs-lookup"><span data-stu-id="6f530-147">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>, If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

2. <span data-ttu-id="6f530-148">Sélectionnez **Déployer le add-in** en haut de la page, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6f530-148">Select **Deploy Add-in** at the top of the page, and then select **Next**.</span></span>

   ![Page Services et add-ins dans le centre d Microsoft 365'administration](../../media/ServicesAddInsPageNewM365AdminCenter.png)

3. <span data-ttu-id="6f530-150">Dans le **volant Déployer un** nouveau module complémentaire qui s’affiche, examinez les informations, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6f530-150">In the **Deploy a new add-in** flyout that appears, review the information, and then click **Next**.</span></span>

4. <span data-ttu-id="6f530-151">Sur la page suivante, cliquez sur **Choisir dans le Store.**</span><span class="sxs-lookup"><span data-stu-id="6f530-151">On the next page, click **Choose from the Store**.</span></span>

   ![Déployer une nouvelle page de modules](../../media/NewAddInScreen2.png)

5. <span data-ttu-id="6f530-153">Dans la page Sélectionner un **add-in** qui s’affiche, cliquez dans  la zone De recherche, entrez  **Hameçonnage** de rapport, puis cliquez sur Icône ![ ](../../media/search-icon.png) Recherche.</span><span class="sxs-lookup"><span data-stu-id="6f530-153">In the **Select add-in** page that appears, click in the **Search** box, enter **Report Phishing**, and then click **Search** ![Search icon](../../media/search-icon.png).</span></span> <span data-ttu-id="6f530-154">Dans la liste des résultats, recherchez **l’hameçonnage** de rapport, puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="6f530-154">In the list of results, find **Report Phishing** and then click **Add**.</span></span>

6. <span data-ttu-id="6f530-155">Dans la boîte de dialogue qui s’affiche, examinez les informations de licence et de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="6f530-155">In the dialog that appears, review the licensing and privacy information, and then click **Continue**.</span></span>

7. <span data-ttu-id="6f530-156">Dans la page **Configurer le module de** configuration qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6f530-156">In the **Configure add-in** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="6f530-157">**Utilisateurs affectés**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f530-157">**Assigned users**: Select one of the following values:</span></span>

     - <span data-ttu-id="6f530-158">**Tout le monde** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="6f530-158">**Everyone** (default)</span></span>
     - <span data-ttu-id="6f530-159">**Utilisateurs/groupes spécifiques**</span><span class="sxs-lookup"><span data-stu-id="6f530-159">**Specific users / groups**</span></span>
     - <span data-ttu-id="6f530-160">**Juste moi**</span><span class="sxs-lookup"><span data-stu-id="6f530-160">**Just me**</span></span>

   - <span data-ttu-id="6f530-161">**Méthode de déploiement**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f530-161">**Deployment method**: Select one of the following values:</span></span>

     - <span data-ttu-id="6f530-162">**Fixe (par défaut)**: le add-in est automatiquement déployé sur les utilisateurs spécifiés et ils ne peuvent pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="6f530-162">**Fixed (Default)**: The add-in is automatically deployed to the specified users and they can't remove it.</span></span>
     - <span data-ttu-id="6f530-163">**Disponible**: les utilisateurs peuvent installer le add-in sur **Home** \> **Get add-ins** \> **géré par l’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="6f530-163">**Available**: Users can install the add-in at **Home** \> **Get add-ins** \> **Admin-managed**.</span></span>
     - <span data-ttu-id="6f530-164">**Facultatif**: le add-in est automatiquement déployé pour les utilisateurs spécifiés, mais ils peuvent choisir de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="6f530-164">**Optional**: The add-in is automatically deployed to the specified users, but they can choose to remove it.</span></span>

   <span data-ttu-id="6f530-165">Lorsque vous avez terminé, cliquez sur **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="6f530-165">When you're finished, click **Deploy**.</span></span>

8. <span data-ttu-id="6f530-166">Dans la page **Déployer** le hameçonnage de rapport qui s’affiche, vous verrez un rapport d’avancement suivi d’une confirmation du déploiement du module.</span><span class="sxs-lookup"><span data-stu-id="6f530-166">In the **Deploy Report Phishing** page that appears, you'll see a progress report followed by a confirmation that the add-in was deployed.</span></span> <span data-ttu-id="6f530-167">Après avoir lu les informations, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6f530-167">After you read the information, click **Next**.</span></span>

9. <span data-ttu-id="6f530-168">Dans la page **Annoncer le add-in** qui s’affiche, examinez les informations, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="6f530-168">On the **Announce add-in** page that appears, review the information, and then click **Close**.</span></span>

## <a name="learn-how-to-use-the-report-phishing-add-in"></a><span data-ttu-id="6f530-169">Découvrez comment utiliser le module de signalement du hameçonnage</span><span class="sxs-lookup"><span data-stu-id="6f530-169">Learn how to use the Report Phishing add-in</span></span>

<span data-ttu-id="6f530-170">Les personnes à qui le add-in est affecté voient les icônes suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f530-170">People who have the add-in assigned to them will see the following icons:</span></span>

- <span data-ttu-id="6f530-171">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="6f530-171">In Outlook, the icon looks like this:</span></span>

  ![Icône signaler le hameçonnage du Outlook](../../media/Outlook-ReportPhishing.png)

- <span data-ttu-id="6f530-173">Dans Outlook sur le web, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="6f530-173">In Outlook on the web, the icon looks like this:</span></span>

  ![Outlook sur l’icône du module de hameçonnage de rapport web](../../media/OWA-ReportPhishing.png)

## <a name="review-or-edit-settings-for-the-report-phishing-add-in"></a><span data-ttu-id="6f530-175">Examiner ou modifier les paramètres du module de signalement du hameçonnage</span><span class="sxs-lookup"><span data-stu-id="6f530-175">Review or edit settings for the Report Phishing add-in</span></span>

1. <span data-ttu-id="6f530-176">Dans le Centre d’administration Microsoft 365,  \> **rendez-vous** sur la page Des applications Paramètres à l’adresse suivante : Si vous ne voyez pas la page Des applications intégrées, consultez le lien Paramètres Applications intégrées en haut de la page Applications <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>   \>  \> **intégrées.** </span><span class="sxs-lookup"><span data-stu-id="6f530-176">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>, If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

2. <span data-ttu-id="6f530-177">Recherchez et sélectionnez **le** module de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="6f530-177">Find and select the **Report Phishing** add-in.</span></span>

3. <span data-ttu-id="6f530-178">Dans le volant **Modifier le hameçonnage** du rapport qui s’affiche, examinez et modifiez les paramètres selon les cas de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6f530-178">In the **Edit Report Phishing** flyout that appears, review, and edit settings as appropriate for your organization.</span></span> <span data-ttu-id="6f530-179">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6f530-179">When you're finished, click **Save**.</span></span>

## <a name="view-and-review-reported-messages"></a><span data-ttu-id="6f530-180">Afficher et examiner les messages signalés</span><span class="sxs-lookup"><span data-stu-id="6f530-180">View and review reported messages</span></span>

<span data-ttu-id="6f530-181">Pour passer en revue les messages que les utilisateurs signalent à Microsoft, vous avez les options ci-après :</span><span class="sxs-lookup"><span data-stu-id="6f530-181">To review messages that users report to Microsoft, you have these options:</span></span>

- <span data-ttu-id="6f530-182">Utilisez le portail Soumissions d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="6f530-182">Use the Admin Submissions portal.</span></span> <span data-ttu-id="6f530-183">Pour plus d’informations, voir [Afficher les soumissions d’utilisateurs à Microsoft.](admin-submission.md#view-user-submissions-to-microsoft)</span><span class="sxs-lookup"><span data-stu-id="6f530-183">For more information, see [View user submissions to Microsoft](admin-submission.md#view-user-submissions-to-microsoft).</span></span>

- <span data-ttu-id="6f530-184">Créez une règle de flux de messagerie (également appelée règle de transport) pour envoyer des copies des messages signalés.</span><span class="sxs-lookup"><span data-stu-id="6f530-184">Create a mail flow rule (also known as a transport rule) to send copies of reported messages.</span></span> <span data-ttu-id="6f530-185">Pour obtenir des instructions, voir Utiliser des règles de flux de messagerie pour voir [quels utilisateurs font des rapports à Microsoft.](/exchange/security-and-compliance/mail-flow-rules/use-rules-to-see-what-users-are-reporting-to-microsoft)</span><span class="sxs-lookup"><span data-stu-id="6f530-185">For instructions, see [Use mail flow rules to see what users are reporting to Microsoft](/exchange/security-and-compliance/mail-flow-rules/use-rules-to-see-what-users-are-reporting-to-microsoft).</span></span>
