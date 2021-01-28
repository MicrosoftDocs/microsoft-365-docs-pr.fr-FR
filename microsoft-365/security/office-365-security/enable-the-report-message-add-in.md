---
title: Activez le complément Signaler un message
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
audience: Admin
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Découvrez comment activer le add-in Message de rapport pour Outlook et Outlook sur le web, pour des utilisateurs individuels ou pour l’ensemble de votre organisation.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: a1f8cffaa6346ec7f426da3c862014ed85a9a367
ms.sourcegitcommit: 537e513a4a232a01e44ecbc76d86a8bcaf142482
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50029231"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="e12eb-103">Activez le complément Signaler un message</span><span class="sxs-lookup"><span data-stu-id="e12eb-103">Enable the Report Message add-in</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


> [!NOTE]
> <span data-ttu-id="e12eb-104">Si vous êtes un administrateur d’une organisation Microsoft 365 avec des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="e12eb-104">If you're an admin in a Microsoft 365 organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="e12eb-105">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="e12eb-105">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

<span data-ttu-id="e12eb-106">Les add-ins Signaler le message et Signaler le hameçonnage pour Outlook et Outlook sur le web (anciennement Outlook Web App) permettent aux utilisateurs de signaler facilement les faux positifs (messages électroniques de qualité marqués comme faux) ou les faux négatifs (courrier électronique non autorisé) à Microsoft et à ses affiliés pour analyse.</span><span class="sxs-lookup"><span data-stu-id="e12eb-106">The Report Message and Report Phishing add-ins for Outlook and Outlook on the web (formerly known as Outlook Web App) enables people to easily report false positives (good email marked as bad) or false negatives (bad email allowed) to Microsoft and its affiliates for analysis.</span></span>

<span data-ttu-id="e12eb-107">Microsoft utilise ces soumissions pour améliorer l’efficacité des technologies de protection de la messagerie.</span><span class="sxs-lookup"><span data-stu-id="e12eb-107">Microsoft uses these submissions to improve the effectiveness of email protection technologies.</span></span> <span data-ttu-id="e12eb-108">Par exemple, si des personnes signalent un grand nombre de messages marqués comme courrier indésirable à l’aide du add-in Signaler un message, l’équipe de sécurité de votre organisation devra peut-être ajuster les stratégies [anti-courrier](configure-your-spam-filter-policies.md)indésirable.</span><span class="sxs-lookup"><span data-stu-id="e12eb-108">For example, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-your-spam-filter-policies.md).</span></span>

<span data-ttu-id="e12eb-109">Vous pouvez installer le add-in Signaler le message ou Signaler le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="e12eb-109">You can install either the Report Message or Report Phishing add-in.</span></span> <span data-ttu-id="e12eb-110">Si vous souhaitez que vos utilisateurs signalent uniquement les messages de hameçonnage, déployez le module de signalement du hameçonnage dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e12eb-110">If you want your users to report only phishing messages, deploy the Report Phishing add-in in your organization.</span></span> <span data-ttu-id="e12eb-111">Pour plus d’informations, [voir Enable the Report Phishing add-in](enable-the-report-phish-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="e12eb-111">For more information, see [Enable the Report Phishing add-in](enable-the-report-phish-add-in.md).</span></span>

<span data-ttu-id="e12eb-112">Le add-in Report Message offre la possibilité de signaler les messages de courrier indésirable et de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="e12eb-112">The Report Message add-in provides the option to report both spam and phishing messages.</span></span> <span data-ttu-id="e12eb-113">Les administrateurs peuvent activer le add-in Message de rapport pour l’organisation, et les utilisateurs individuels peuvent l’installer eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="e12eb-113">Admins can enable the Report Message add-in for the organization, and individual users can install it for themselves.</span></span>

<span data-ttu-id="e12eb-114">Si vous êtes un utilisateur individuel, vous pouvez activer le module de rapport de [message pour vous-même.](#get-the-report-message-add-in-for-yourself)</span><span class="sxs-lookup"><span data-stu-id="e12eb-114">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span>

<span data-ttu-id="e12eb-115">Si vous êtes un administrateur général ou un administrateur Exchange Online et qu’Exchange est configuré pour utiliser l’authentification OAuth, vous pouvez activer le [add-in](#get-and-enable-the-report-message-add-in-for-your-organization)Message de rapport pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e12eb-115">If you're a global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization).</span></span> <span data-ttu-id="e12eb-116">Le message de Add-In est désormais disponible via [le déploiement centralisé.](https://docs.microsoft.com/microsoft-365/admin/manage/centralized-deployment-of-add-ins)</span><span class="sxs-lookup"><span data-stu-id="e12eb-116">The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/microsoft-365/admin/manage/centralized-deployment-of-add-ins).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="e12eb-117">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="e12eb-117">What do you need to know before you begin?</span></span>

- <span data-ttu-id="e12eb-118">Le add-in Message de rapport fonctionne avec la plupart des abonnements Microsoft 365 et les produits suivants :</span><span class="sxs-lookup"><span data-stu-id="e12eb-118">The Report Message add-in works with most Microsoft 365 subscriptions and the following products:</span></span>

  - <span data-ttu-id="e12eb-119">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="e12eb-119">Outlook on the web</span></span>
  - <span data-ttu-id="e12eb-120">Outlook 2013 SP1 ou une édition ultérieure</span><span class="sxs-lookup"><span data-stu-id="e12eb-120">Outlook 2013 SP1 or later</span></span>
  - <span data-ttu-id="e12eb-121">Outlook 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="e12eb-121">Outlook 2016 for Mac</span></span>
  - <span data-ttu-id="e12eb-122">Outlook inclus dans les applications Microsoft 365 pour Entreprise</span><span class="sxs-lookup"><span data-stu-id="e12eb-122">Outlook included with Microsoft 365 apps for Enterprise</span></span>

- <span data-ttu-id="e12eb-123">Le module de rapport de message n’est pas disponible pour les boîtes aux lettres dans les organisations Exchange locales.</span><span class="sxs-lookup"><span data-stu-id="e12eb-123">The Report Message add-in is not available for mailboxes in on-premises Exchange organizations.</span></span>

- <span data-ttu-id="e12eb-124">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="e12eb-124">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="e12eb-125">Pour plus d’informations, voir [Stratégies d’envoi des utilisateurs.](user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="e12eb-125">For more information, see [User submissions policies](user-submission.md).</span></span>

- <span data-ttu-id="e12eb-126">Votre navigateur web existant doit fonctionner avec le add-in Message de rapport.</span><span class="sxs-lookup"><span data-stu-id="e12eb-126">Your existing web browser should work with the Report Message add-in.</span></span> <span data-ttu-id="e12eb-127">Toutefois, si vous remarquez que le module n’est pas disponible ou ne fonctionne pas comme prévu, essayez un autre navigateur.</span><span class="sxs-lookup"><span data-stu-id="e12eb-127">But, if you notice the add-in is not available or not working as expected, try a different browser.</span></span>

- <span data-ttu-id="e12eb-128">Pour les installation organisationnelles, l’organisation doit être configurée pour utiliser l’authentification OAuth.</span><span class="sxs-lookup"><span data-stu-id="e12eb-128">For organizational installs, the organization needs to be configured to use OAuth authentication.</span></span> <span data-ttu-id="e12eb-129">Pour plus d’informations, [voir Determine if Centralized Deployment of add-ins works for your organization](../../admin/manage/centralized-deployment-of-add-ins.md).</span><span class="sxs-lookup"><span data-stu-id="e12eb-129">For more information, see [Determine if Centralized Deployment of add-ins works for your organization](../../admin/manage/centralized-deployment-of-add-ins.md).</span></span>

- <span data-ttu-id="e12eb-130">Les administrateurs doivent être membres du groupe de rôles Administrateurs globaux.</span><span class="sxs-lookup"><span data-stu-id="e12eb-130">Admins need to be a member of the Global admins role group.</span></span> <span data-ttu-id="e12eb-131">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="e12eb-131">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="e12eb-132">Obtenir le add-in Message de rapport pour vous-même</span><span class="sxs-lookup"><span data-stu-id="e12eb-132">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="e12eb-133">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Message add-in.</span><span class="sxs-lookup"><span data-stu-id="e12eb-133">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Message add-in.</span></span> <span data-ttu-id="e12eb-134">To go directly to the Report Message add-in, go to <https://appsource.microsoft.com/product/office/wa104381180> .</span><span class="sxs-lookup"><span data-stu-id="e12eb-134">To go directly to the Report Message add-in, go to <https://appsource.microsoft.com/product/office/wa104381180>.</span></span>

2. <span data-ttu-id="e12eb-135">Cliquez **sur GET IT NOW**.</span><span class="sxs-lookup"><span data-stu-id="e12eb-135">Click **GET IT NOW**.</span></span>

   ![Message de rapport : l’obtenir maintenant](../../media/ReportMessageGETITNOW.png)

3. <span data-ttu-id="e12eb-137">Dans la boîte de dialogue qui s’affiche, examinez les conditions d’utilisation et la politique de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="e12eb-137">In the dialog that appears, review the terms of use and privacy policy, and then click **Continue**.</span></span>

4. <span data-ttu-id="e12eb-138">Connectez-vous à l’aide de votre compte scolaire ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour un usage personnel).</span><span class="sxs-lookup"><span data-stu-id="e12eb-138">Sign in using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>

<span data-ttu-id="e12eb-139">Une fois le add-in installé et activé, les icônes suivantes s’offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="e12eb-139">After the add-in is installed and enabled, you'll see the following icons:</span></span>

- <span data-ttu-id="e12eb-140">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="e12eb-140">In Outlook, the icon looks like this:</span></span>

  ![Icône signaler le add-in Message pour Outlook](../../media/OutlookReportMessageIcon.png)

- <span data-ttu-id="e12eb-142">Dans Outlook sur le web, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="e12eb-142">In Outlook on the web, the icon looks like this:</span></span>

  ![Icône du add-in Message de rapport Outlook sur le web](../../media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)

<span data-ttu-id="e12eb-144">Pour savoir comment utiliser le add-in, voir Utiliser le [add-in Message de rapport.](https://support.microsoft.com/office/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)</span><span class="sxs-lookup"><span data-stu-id="e12eb-144">To learn how to use the add-in, see [Use the Report Message add-in](https://support.microsoft.com/office/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="e12eb-145">Obtenir et activer le add-in Message de rapport pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="e12eb-145">Get and enable the Report Message add-in for your organization</span></span>

> [!NOTE]
> <span data-ttu-id="e12eb-146">L’apparition du module dans votre organisation peut prendre jusqu’à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="e12eb-146">It could take up to 12 hours for the add-in to appear in your organization.</span></span>

1. <span data-ttu-id="e12eb-147">Dans le Centre d’administration Microsoft 365, rendez-vous sur la page **Paramètres** des applications à l’adresse suivante : Si vous ne voyez pas la page Des applications \>  <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> intégrées,   \>  \> **rendez-vous**  sur le lien Paramètres applications intégrées en haut de la page Applications intégrées.</span><span class="sxs-lookup"><span data-stu-id="e12eb-147">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>, If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

2. <span data-ttu-id="e12eb-148">Sélectionnez **Déployer le add-in** en haut de la page, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e12eb-148">Select **Deploy Add-in** at the top of the page, and then select **Next**.</span></span>

   ![Page Services et modules dans le Centre d’administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

3. <span data-ttu-id="e12eb-150">Dans le **volant Déployer un** nouveau module complémentaire qui s’affiche, examinez les informations, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e12eb-150">In the **Deploy a new add-in** flyout that appears, review the information, and then click **Next**.</span></span>

4. <span data-ttu-id="e12eb-151">Sur la page suivante, cliquez sur **Choisir dans le Store.**</span><span class="sxs-lookup"><span data-stu-id="e12eb-151">On the next page, click **Choose from the Store**.</span></span>

   ![Déployer une nouvelle page de modules](../../media/NewAddInScreen2.png)

5. <span data-ttu-id="e12eb-153">Dans la page **Sélectionner un add-in** qui s’affiche, cliquez dans la zone De recherche, entrez Message de rapport, puis cliquez sur **Icône**   ![ ](../../media/search-icon.png) Rechercher.</span><span class="sxs-lookup"><span data-stu-id="e12eb-153">In the **Select add-in** page that appears, click in the **Search** box, enter **Report Message**, and then click **Search** ![Search icon](../../media/search-icon.png).</span></span> <span data-ttu-id="e12eb-154">Dans la liste des résultats, recherchez Message de **rapport,** puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="e12eb-154">In the list of results, find **Report Message** and then click **Add**.</span></span>

   ![Sélectionner les résultats de la recherche de add-in](../../media/NewAddInScreen3.png)

6. <span data-ttu-id="e12eb-156">Dans la boîte de dialogue qui s’affiche, examinez les informations de licence et de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="e12eb-156">In the dialog that appears, review the licensing and privacy information, and then click **Continue**.</span></span>

7. <span data-ttu-id="e12eb-157">Dans la page **Configurer le add-in** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e12eb-157">In the **Configure add-in** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="e12eb-158">**Utilisateurs affectés**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e12eb-158">**Assigned users**: Select one of the following values:</span></span>

     - <span data-ttu-id="e12eb-159">**Tout le monde** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="e12eb-159">**Everyone** (default)</span></span>
     - <span data-ttu-id="e12eb-160">**Utilisateurs/groupes spécifiques**</span><span class="sxs-lookup"><span data-stu-id="e12eb-160">**Specific users / groups**</span></span>
     - <span data-ttu-id="e12eb-161">**Juste moi**</span><span class="sxs-lookup"><span data-stu-id="e12eb-161">**Just me**</span></span>

   - <span data-ttu-id="e12eb-162">**Méthode de déploiement**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e12eb-162">**Deployment method**: Select one of the following values:</span></span>

     - <span data-ttu-id="e12eb-163">**Fixe (par défaut)**: le add-in est automatiquement déployé pour les utilisateurs spécifiés et ils ne peuvent pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="e12eb-163">**Fixed (Default)**: The add-in is automatically deployed to the specified users and they can't remove it.</span></span>
     - <span data-ttu-id="e12eb-164">**Disponible**: les utilisateurs peuvent installer le add-in sur **home** \> **get add-ins** \> **admin-managed**.</span><span class="sxs-lookup"><span data-stu-id="e12eb-164">**Available**: Users can install the add-in at **Home** \> **Get add-ins** \> **Admin-managed**.</span></span>
     - <span data-ttu-id="e12eb-165">**Facultatif**: le add-in est automatiquement déployé pour les utilisateurs spécifiés, mais ils peuvent choisir de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="e12eb-165">**Optional**: The add-in is automatically deployed to the specified users, but they can choose to remove it.</span></span>

   ![Configurer la page de l’ajout](../../media/configure-add-in.png)

   <span data-ttu-id="e12eb-167">Lorsque vous avez terminé, cliquez sur **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="e12eb-167">When you're finished, click **Deploy**.</span></span>

8. <span data-ttu-id="e12eb-168">Dans la page Déployer le **message** de rapport qui s’affiche, vous verrez un rapport d’avancement suivi d’une confirmation du déploiement du module.</span><span class="sxs-lookup"><span data-stu-id="e12eb-168">In the **Deploy Report Message** page that appears, you'll see a progress report followed by a confirmation that the add-in was deployed.</span></span> <span data-ttu-id="e12eb-169">Après avoir lu les informations, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e12eb-169">After you read the information, click **Next**.</span></span>

   ![Page Déployer le message de rapport](../../media/deploy-report-message-page.png)

9. <span data-ttu-id="e12eb-171">Dans la page **Annoncer le add-in** qui s’affiche, examinez les informations, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e12eb-171">On the **Announce add-in** page that appears, review the information, and then click **Close**.</span></span>

   ![Page Annoncer le add-in](../../media/announce-add-in-page.png)

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="e12eb-173">Découvrez comment utiliser le add-in Message de rapport</span><span class="sxs-lookup"><span data-stu-id="e12eb-173">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="e12eb-174">Les personnes à qui le add-in est affecté voient les icônes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e12eb-174">People who have the add-in assigned to them will see the following icons:</span></span>

- <span data-ttu-id="e12eb-175">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="e12eb-175">In Outlook, the icon looks like this:</span></span>

  ![Icône Signaler un add-in de message pour Outlook](../../media/OutlookReportMessageIcon.png)

- <span data-ttu-id="e12eb-177">Dans Outlook sur le web, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="e12eb-177">In Outlook on the web, the icon looks like this:</span></span>

  ![Icône De message Outlook sur le web](../../media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)

<span data-ttu-id="e12eb-179">Lorsque vous informez les utilisateurs du add-in Message de rapport, incluez un lien pour utiliser le [add-in Message de rapport.](https://support.microsoft.com/office/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)</span><span class="sxs-lookup"><span data-stu-id="e12eb-179">When you notify users about the Report Message add-in, include a link to [Use the Report Message add-in](https://support.microsoft.com/office/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="e12eb-180">Passer en revue ou modifier les paramètres du add-in Message de rapport</span><span class="sxs-lookup"><span data-stu-id="e12eb-180">Review or edit settings for the Report Message add-in</span></span>

1. <span data-ttu-id="e12eb-181">Dans le Centre d’administration Microsoft 365, rendez-vous sur la page **Paramètres** des applications à l’adresse suivante : Si vous ne voyez pas la page Des applications \>  <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> intégrées,   \>  \> **rendez-vous**  sur le lien Paramètres applications intégrées en haut de la page Applications intégrées.</span><span class="sxs-lookup"><span data-stu-id="e12eb-181">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>, If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

   ![Page Services et Add-Ins dans le nouveau Centre d’administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

2. <span data-ttu-id="e12eb-183">Recherchez et sélectionnez le add-in **Message** de rapport.</span><span class="sxs-lookup"><span data-stu-id="e12eb-183">Find and select the **Report Message** add-in.</span></span>

3. <span data-ttu-id="e12eb-184">Dans le volant **Modifier le message** de rapport qui s’affiche, examinez et modifiez les paramètres selon le cas pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e12eb-184">In the **Edit Report Message** flyout that appears, review and edit settings as appropriate for your organization.</span></span> <span data-ttu-id="e12eb-185">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e12eb-185">When you're finished, click **Save**.</span></span>

   ![Paramètres du add-in Message de rapport](../../media/EditReportMessageAddIn.png)

## <a name="view-and-review-reported-messages"></a><span data-ttu-id="e12eb-187">Afficher et examiner les messages signalés</span><span class="sxs-lookup"><span data-stu-id="e12eb-187">View and review reported messages</span></span>

<span data-ttu-id="e12eb-188">Pour passer en revue les messages que les utilisateurs signalent à Microsoft, vous avez les options ci-après :</span><span class="sxs-lookup"><span data-stu-id="e12eb-188">To review messages that users report to Microsoft, you have these options:</span></span>

- <span data-ttu-id="e12eb-189">Utilisez le portail Soumissions d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="e12eb-189">Use the Admin Submissions portal.</span></span> <span data-ttu-id="e12eb-190">Pour plus d’informations, voir [Afficher les soumissions d’utilisateurs à Microsoft.](admin-submission.md#view-user-submissions-to-microsoft)</span><span class="sxs-lookup"><span data-stu-id="e12eb-190">For more information, see [View user submissions to Microsoft](admin-submission.md#view-user-submissions-to-microsoft).</span></span>

- <span data-ttu-id="e12eb-191">Créez une règle de flux de messagerie (également appelée règle de transport) pour envoyer des copies des messages signalés.</span><span class="sxs-lookup"><span data-stu-id="e12eb-191">Create a mail flow rule (also known as a transport rule) to send copies of reported messages.</span></span> <span data-ttu-id="e12eb-192">Pour obtenir des instructions, voir Utiliser des règles de flux de messagerie pour voir ce [que vos utilisateurs rapportent à Microsoft.](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="e12eb-192">For instructions, see [Use mail flow rules to see what your users are reporting to Microsoft](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md).</span></span>
