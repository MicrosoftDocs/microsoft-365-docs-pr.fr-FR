---
title: Activer le message de rapport ou les modules de signalement du hameçonnage
f1.keywords:
- NOCSH
ms.author: siosulli
author: dansimp
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
description: Découvrez comment activer le message de rapport ou les add-ins Signaler le hameçonnage pour Outlook et Outlook sur le web, pour des utilisateurs individuels ou pour l’ensemble de votre organisation.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 25c4f7d67fd4fa876544a17df0f4bc1abfd7b3e7
ms.sourcegitcommit: 3b9fab82d63aea41d5f544938868c5d2cbf52d7a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "52782932"
---
# <a name="enable-the-report-message-or-the-report-phishing-add-ins"></a><span data-ttu-id="cb771-103">Activer le message de rapport ou les modules de signalement du hameçonnage</span><span class="sxs-lookup"><span data-stu-id="cb771-103">Enable the Report Message or the Report Phishing add-ins</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="cb771-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="cb771-104">**Applies to**</span></span>
- [<span data-ttu-id="cb771-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="cb771-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="cb771-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="cb771-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="cb771-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="cb771-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

> [!NOTE]
> <span data-ttu-id="cb771-108">Si vous êtes un administrateur d’une organisation Microsoft 365 avec des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="cb771-108">If you're an admin in a Microsoft 365 organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="cb771-109">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="cb771-109">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

<span data-ttu-id="cb771-110">Les add-ins Signaler les messages et signaler le hameçonnage pour Outlook et Outlook sur le web (anciennement appelés Outlook Web App) permettent aux utilisateurs de signaler facilement les faux positifs (messages électroniques de qualité marqués comme faux) ou les faux négatifs (courriers électroniques erronés autorisés) à Microsoft et à ses affiliés pour analyse.</span><span class="sxs-lookup"><span data-stu-id="cb771-110">The Report Message and Report Phishing add-ins for Outlook and Outlook on the web (formerly known as Outlook Web App) enable people to easily report false positives (good email marked as bad) or false negatives (bad email allowed) to Microsoft and its affiliates for analysis.</span></span> 

<span data-ttu-id="cb771-111">Microsoft utilise ces soumissions pour améliorer l’efficacité des technologies de protection de la messagerie.</span><span class="sxs-lookup"><span data-stu-id="cb771-111">Microsoft uses these submissions to improve the effectiveness of email protection technologies.</span></span> <span data-ttu-id="cb771-112">Par exemple, supposons que des personnes signalent de nombreux messages à l’aide du module de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="cb771-112">For example, suppose that people are reporting many messages using the Report Phishing add-in.</span></span> <span data-ttu-id="cb771-113">Ces informations sont disponibles dans le Tableau de bord de sécurité et d’autres rapports.</span><span class="sxs-lookup"><span data-stu-id="cb771-113">This information surfaces in the Security Dashboard and other reports.</span></span> <span data-ttu-id="cb771-114">L’équipe de sécurité de votre organisation peut utiliser ces informations pour indiquer que les stratégies anti-hameçonnage peuvent avoir besoin d’être mises à jour.</span><span class="sxs-lookup"><span data-stu-id="cb771-114">Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated.</span></span> 

<span data-ttu-id="cb771-115">Vous pouvez installer le module de rapport de message ou de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="cb771-115">You can install either the Report Message or Report Phishing add-in.</span></span> <span data-ttu-id="cb771-116">Si vous souhaitez que vos utilisateurs signalent à la fois le courrier indésirable et les messages de hameçonnage, déployez le add-in Signaler un message dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cb771-116">If you want your users to report both spam and phishing messages, deploy the Report Message add-in in your organization.</span></span> <span data-ttu-id="cb771-117">Pour plus d’informations, voir Enable the Report Message add-in.</span><span class="sxs-lookup"><span data-stu-id="cb771-117">For more information, see Enable the Report Message add-in.</span></span> 

<span data-ttu-id="cb771-118">Le add-in Report Message offre la possibilité de signaler les messages de courrier indésirable et de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="cb771-118">The Report Message add-in provides the option to report both spam and phishing messages.</span></span> <span data-ttu-id="cb771-119">Les administrateurs peuvent activer le add-in Message de rapport pour l’organisation, et les utilisateurs individuels peuvent l’installer eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="cb771-119">Admins can enable the Report Message add-in for the organization, and individual users can install it for themselves.</span></span> 

<span data-ttu-id="cb771-120">Le module de signalement du hameçonnage offre la possibilité de signaler uniquement les messages de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="cb771-120">The Report Phishing add-in provides the option to report only phishing messages.</span></span> <span data-ttu-id="cb771-121">Les administrateurs peuvent activer le module de signalement du hameçonnage pour l’organisation, et les utilisateurs individuels peuvent l’installer eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="cb771-121">Admins can enable the Report Phishing add-in for the organization, and individual users can install it for themselves.</span></span> 

<span data-ttu-id="cb771-122">Si vous êtes un utilisateur individuel, vous pouvez activer les deux modules pour vous-même.</span><span class="sxs-lookup"><span data-stu-id="cb771-122">If you're an individual user, you can enable both the add-ins for yourself.</span></span>

<span data-ttu-id="cb771-123">Si vous êtes un administrateur général ou un administrateur Exchange Online et que Exchange est configuré pour utiliser l’authentification OAuth, vous pouvez activer le module de signalement des messages et le module de signalement du hameçonnage pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cb771-123">If you're a global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can enable the Report Message add-in and the Report Phishing add-in for your organization.</span></span> <span data-ttu-id="cb771-124">Les deux modules sont désormais disponibles via [le déploiement centralisé.](../../admin/manage/centralized-deployment-of-add-ins.md)</span><span class="sxs-lookup"><span data-stu-id="cb771-124">Both add-ins are now available through [Centralized Deployment](../../admin/manage/centralized-deployment-of-add-ins.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="cb771-125">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="cb771-125">What do you need to know before you begin?</span></span>

- <span data-ttu-id="cb771-126">Le add-in Report Message et le add-in Report Phishing fonctionnent avec la plupart Microsoft 365 abonnements et les produits suivants :</span><span class="sxs-lookup"><span data-stu-id="cb771-126">Both the Report Message add-in and the Report Phishing add-in works with most Microsoft 365 subscriptions and the following products:</span></span>

  - <span data-ttu-id="cb771-127">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="cb771-127">Outlook on the web</span></span>
  - <span data-ttu-id="cb771-128">Outlook 2013 SP1 ou une ultérieure</span><span class="sxs-lookup"><span data-stu-id="cb771-128">Outlook 2013 SP1 or later</span></span>
  - <span data-ttu-id="cb771-129">Outlook 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="cb771-129">Outlook 2016 for Mac</span></span>
  - <span data-ttu-id="cb771-130">Outlook incluses dans Microsoft 365 applications pour Enterprise</span><span class="sxs-lookup"><span data-stu-id="cb771-130">Outlook included with Microsoft 365 apps for Enterprise</span></span>
  - <span data-ttu-id="cb771-131">Outlook application pour iOS et Android</span><span class="sxs-lookup"><span data-stu-id="cb771-131">Outlook app for iOS and Android</span></span>

- <span data-ttu-id="cb771-132">Les deux modules ne sont pas disponibles pour les boîtes aux lettres partagées ou les boîtes aux lettres dans des organisations Exchange locales.</span><span class="sxs-lookup"><span data-stu-id="cb771-132">Both add-ins are not available for shared mailboxes or mailboxes in on-premises Exchange organizations.</span></span>

- <span data-ttu-id="cb771-133">Votre navigateur web existant doit fonctionner à la fois avec les add-ins Message de rapport et Signaler le hameçonnage. Toutefois, si vous remarquez que le module n’est pas disponible ou ne fonctionne pas comme prévu, essayez un autre navigateur.</span><span class="sxs-lookup"><span data-stu-id="cb771-133">Your existing web browser should work with both the Report Message and Report Phishing add-ins. But, if you notice the add-in is not available or not working as expected, try a different browser.</span></span>

- <span data-ttu-id="cb771-134">Pour les installation organisationnelles, l’organisation doit être configurée pour utiliser l’authentification OAuth.</span><span class="sxs-lookup"><span data-stu-id="cb771-134">For organizational installs, the organization needs to be configured to use OAuth authentication.</span></span> <span data-ttu-id="cb771-135">Pour plus d’informations, [voir Determine if Centralized Deployment of add-ins works for your organization](../../admin/manage/centralized-deployment-of-add-ins.md).</span><span class="sxs-lookup"><span data-stu-id="cb771-135">For more information, see [Determine if Centralized Deployment of add-ins works for your organization](../../admin/manage/centralized-deployment-of-add-ins.md).</span></span>

- <span data-ttu-id="cb771-136">Les administrateurs doivent être membres du groupe de rôles Administrateurs globaux.</span><span class="sxs-lookup"><span data-stu-id="cb771-136">Admins need to be a member of the Global admins role group.</span></span> <span data-ttu-id="cb771-137">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="cb771-137">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="cb771-138">Pour plus d’informations sur la façon de signaler un message à l’aide de la fonctionnalité Signaler un message, voir Signaler les faux positifs et les [faux négatifs dans Outlook](report-false-positives-and-false-negatives.md).</span><span class="sxs-lookup"><span data-stu-id="cb771-138">For more information on how to report a message using the Report Message feature, see [Report false positives and false negatives in Outlook](report-false-positives-and-false-negatives.md).</span></span>

## <a name="get-the-report-message-add-in"></a><span data-ttu-id="cb771-139">Obtenir le add-in Message de rapport</span><span class="sxs-lookup"><span data-stu-id="cb771-139">Get the Report Message add-in</span></span>

### <a name="get-the-add-in-for-yourself"></a><span data-ttu-id="cb771-140">Obtenir le add-in pour vous-même</span><span class="sxs-lookup"><span data-stu-id="cb771-140">Get the add-in for yourself</span></span>

1. <span data-ttu-id="cb771-141">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Message add-in.</span><span class="sxs-lookup"><span data-stu-id="cb771-141">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Message add-in.</span></span> <span data-ttu-id="cb771-142">To go directly to the Report Message add-in, go to <https://appsource.microsoft.com/product/office/wa104381180> .</span><span class="sxs-lookup"><span data-stu-id="cb771-142">To go directly to the Report Message add-in, go to <https://appsource.microsoft.com/product/office/wa104381180>.</span></span>

2. <span data-ttu-id="cb771-143">Cliquez **sur GET IT NOW**.</span><span class="sxs-lookup"><span data-stu-id="cb771-143">Click **GET IT NOW**.</span></span>

   ![Message de rapport : l’obtenir maintenant](../../media/ReportMessageGETITNOW.png)

3. <span data-ttu-id="cb771-145">Dans la boîte de dialogue qui s’affiche, examinez les conditions d’utilisation et la politique de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="cb771-145">In the dialog that appears, review the terms of use and privacy policy, and then click **Continue**.</span></span>

4. <span data-ttu-id="cb771-146">Connectez-vous à l’aide de votre compte scolaire ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour un usage personnel).</span><span class="sxs-lookup"><span data-stu-id="cb771-146">Sign in using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>

<span data-ttu-id="cb771-147">Une fois que le module est installé et activé, les icônes suivantes s’offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="cb771-147">After the add-in is installed and enabled, you'll see the following icons:</span></span>

- <span data-ttu-id="cb771-148">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="cb771-148">In Outlook, the icon looks like this:</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="cb771-149">![Icône signaler le Outlook](../../media/OutlookReportMessageIcon.png)</span><span class="sxs-lookup"><span data-stu-id="cb771-149">![Report Message add-in icon for Outlook](../../media/OutlookReportMessageIcon.png)</span></span>

- <span data-ttu-id="cb771-150">Dans Outlook sur le web, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="cb771-150">In Outlook on the web, the icon looks like this:</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="cb771-151">![Outlook sur l’icône du add-in Message de rapport web](../../media/owa-report-message-icon.png)</span><span class="sxs-lookup"><span data-stu-id="cb771-151">![Outlook on the web Report Message add-in icon](../../media/owa-report-message-icon.png)</span></span>

### <a name="get-the-add-in-for-your-organization"></a><span data-ttu-id="cb771-152">Obtenir le add-in pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="cb771-152">Get the add-in for your organization</span></span>

> [!NOTE]
> <span data-ttu-id="cb771-153">L’apparition du module dans votre organisation peut prendre jusqu’à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="cb771-153">It could take up to 12 hours for the add-in to appear in your organization.</span></span>

1. <span data-ttu-id="cb771-154">Dans le Microsoft 365 d’administration, allez à  la page Paramètres de l’utilisateur à \>  l’adresse <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> suivante :</span><span class="sxs-lookup"><span data-stu-id="cb771-154">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>.</span></span> <span data-ttu-id="cb771-155">Si vous ne voyez pas la page Des  applications intégrées, **rendez-vous** sur le lien Paramètres Applications intégrées en haut de la \>  \>  page **Applications intégrées.**</span><span class="sxs-lookup"><span data-stu-id="cb771-155">If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

2. <span data-ttu-id="cb771-156">Sélectionnez **Déployer le add-in** en haut de la page, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cb771-156">Select **Deploy Add-in** at the top of the page, and then select **Next**.</span></span>

   ![Page Services et add-ins dans le centre d’administration Microsoft 365'administration](../../media/ServicesAddInsPageNewM365AdminCenter.png)

3. <span data-ttu-id="cb771-158">Dans le **volant Déployer un** nouveau module complémentaire qui s’affiche, examinez les informations, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cb771-158">In the **Deploy a new add-in** flyout that appears, review the information, and then click **Next**.</span></span>

4. <span data-ttu-id="cb771-159">Sur la page suivante, cliquez sur **Choisir dans le Store.**</span><span class="sxs-lookup"><span data-stu-id="cb771-159">On the next page, click **Choose from the Store**.</span></span>

   ![Déployer une nouvelle page de modules](../../media/NewAddInScreen2.png)

5. <span data-ttu-id="cb771-161">Dans la page **Sélectionner un add-in** qui s’affiche, cliquez dans la zone De recherche, entrez Message de rapport, puis cliquez sur **Icône**   ![ ](../../media/search-icon.png) Rechercher.</span><span class="sxs-lookup"><span data-stu-id="cb771-161">In the **Select add-in** page that appears, click in the **Search** box, enter **Report Message**, and then click **Search** ![Search icon](../../media/search-icon.png).</span></span> <span data-ttu-id="cb771-162">Dans la liste des résultats, recherchez **Message de rapport,** puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="cb771-162">In the list of results, find **Report Message** and then click **Add**.</span></span>

   ![Sélectionner les résultats de la recherche de add-in](../../media/NewAddInScreen3.png)

6. <span data-ttu-id="cb771-164">Dans la boîte de dialogue qui s’affiche, examinez les informations de licence et de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="cb771-164">In the dialog that appears, review the licensing and privacy information, and then click **Continue**.</span></span>

7. <span data-ttu-id="cb771-165">Dans la page **Configurer le add-in** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="cb771-165">In the **Configure add-in** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="cb771-166">**Utilisateurs affectés**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb771-166">**Assigned users**: Select one of the following values:</span></span>

     - <span data-ttu-id="cb771-167">**Tout le monde** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="cb771-167">**Everyone** (default)</span></span>
     - <span data-ttu-id="cb771-168">**Utilisateurs/groupes spécifiques**</span><span class="sxs-lookup"><span data-stu-id="cb771-168">**Specific users / groups**</span></span>
     - <span data-ttu-id="cb771-169">**Juste moi**</span><span class="sxs-lookup"><span data-stu-id="cb771-169">**Just me**</span></span>

   - <span data-ttu-id="cb771-170">**Méthode de déploiement**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb771-170">**Deployment method**: Select one of the following values:</span></span>

     - <span data-ttu-id="cb771-171">**Fixe (par défaut)**: le add-in est automatiquement déployé pour les utilisateurs spécifiés et ils ne peuvent pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="cb771-171">**Fixed (Default)**: The add-in is automatically deployed to the specified users and they can't remove it.</span></span>
     - <span data-ttu-id="cb771-172">**Disponible**: les utilisateurs peuvent installer le add-in sur **Home** \> **Get add-ins** \> **géré par l’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="cb771-172">**Available**: Users can install the add-in at **Home** \> **Get add-ins** \> **Admin-managed**.</span></span>
     - <span data-ttu-id="cb771-173">**Facultatif**: le add-in est automatiquement déployé pour les utilisateurs spécifiés, mais ils peuvent choisir de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="cb771-173">**Optional**: The add-in is automatically deployed to the specified users, but they can choose to remove it.</span></span>

   ![Configurer la page de l’ajout](../../media/configure-add-in.png)

   <span data-ttu-id="cb771-175">Lorsque vous avez terminé, cliquez sur **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="cb771-175">When you're finished, click **Deploy**.</span></span>

8. <span data-ttu-id="cb771-176">Dans la page Déployer le **message** de rapport qui s’affiche, vous verrez un rapport d’avancement suivi d’une confirmation du déploiement du module.</span><span class="sxs-lookup"><span data-stu-id="cb771-176">In the **Deploy Report Message** page that appears, you'll see a progress report followed by a confirmation that the add-in was deployed.</span></span> <span data-ttu-id="cb771-177">Après avoir lu les informations, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cb771-177">After you read the information, click **Next**.</span></span>

   ![Page Déployer le message de rapport](../../media/deploy-report-message-page.png)

9. <span data-ttu-id="cb771-179">Dans la page **Annoncer le add-in** qui s’affiche, examinez les informations, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="cb771-179">On the **Announce add-in** page that appears, review the information, and then click **Close**.</span></span>

   ![Page Annoncer le add-in](../../media/announce-add-in-page.png)

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="cb771-181">Passer en revue ou modifier les paramètres du add-in Message de rapport</span><span class="sxs-lookup"><span data-stu-id="cb771-181">Review or edit settings for the Report Message add-in</span></span>

1. <span data-ttu-id="cb771-182">Dans le Microsoft 365 d’administration, allez à  la page Paramètres de l’utilisateur à \>  l’adresse <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> suivante :</span><span class="sxs-lookup"><span data-stu-id="cb771-182">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>.</span></span> <span data-ttu-id="cb771-183">Si vous ne voyez pas la page Des  applications intégrées, **rendez-vous** sur le lien Paramètres Applications intégrées en haut de la \>  \>  page **Applications intégrées.**</span><span class="sxs-lookup"><span data-stu-id="cb771-183">If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

   ![Page Services et Add-Ins dans la nouvelle page Microsoft 365 Admin Center](../../media/ServicesAddInsPageNewM365AdminCenter.png)

2. <span data-ttu-id="cb771-185">Recherchez et sélectionnez le add-in **Message** de rapport.</span><span class="sxs-lookup"><span data-stu-id="cb771-185">Find and select the **Report Message** add-in.</span></span>

3. <span data-ttu-id="cb771-186">Dans le volant **Modifier le message** de rapport qui s’affiche, examinez et modifiez les paramètres selon le cas pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cb771-186">In the **Edit Report Message** flyout that appears, review and edit settings as appropriate for your organization.</span></span> <span data-ttu-id="cb771-187">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cb771-187">When you're finished, click **Save**.</span></span>

   ![Paramètres pour le add-in Message de rapport](../../media/EditReportMessageAddIn.png)

## <a name="get-the-report-phishing-add-in"></a><span data-ttu-id="cb771-189">Obtenir le module de signalement du hameçonnage</span><span class="sxs-lookup"><span data-stu-id="cb771-189">Get the Report Phishing add-in</span></span>

### <a name="get-the-add-in-for-yourself"></a><span data-ttu-id="cb771-190">Obtenir le add-in pour vous-même</span><span class="sxs-lookup"><span data-stu-id="cb771-190">Get the add-in for yourself</span></span>

1. <span data-ttu-id="cb771-191">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Phishing add-in.</span><span class="sxs-lookup"><span data-stu-id="cb771-191">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Phishing add-in.</span></span>

2. <span data-ttu-id="cb771-192">Cliquez **sur GET IT NOW**.</span><span class="sxs-lookup"><span data-stu-id="cb771-192">Click **GET IT NOW**.</span></span>

3. <span data-ttu-id="cb771-193">Dans la boîte de dialogue qui s’affiche, examinez les conditions d’utilisation et la politique de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="cb771-193">In the dialog that appears, review the terms of use and privacy policy, and then click **Continue**.</span></span>

4. <span data-ttu-id="cb771-194">Connectez-vous à l’aide de votre compte scolaire ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour un usage personnel).</span><span class="sxs-lookup"><span data-stu-id="cb771-194">Sign in using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>

<span data-ttu-id="cb771-195">Une fois que le module est installé et activé, les icônes suivantes s’offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="cb771-195">After the add-in is installed and enabled, you'll see the following icons:</span></span>

- <span data-ttu-id="cb771-196">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="cb771-196">In Outlook, the icon looks like this:</span></span>

  ![Icône signaler le hameçonnage d’un Outlook](../../media/Outlook-ReportPhishing.png)

- <span data-ttu-id="cb771-198">Dans Outlook sur le web, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="cb771-198">In Outlook on the web, the icon looks like this:</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="cb771-199">![Outlook sur l’icône du add-in Rapport de hameçonnage sur le web](../../media/OWA-ReportPhishing.png)</span><span class="sxs-lookup"><span data-stu-id="cb771-199">![Outlook on the web Report Phishing add-in icon](../../media/OWA-ReportPhishing.png)</span></span>

### <a name="get-the-add-in-for-your-organization"></a><span data-ttu-id="cb771-200">Obtenir le add-in pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="cb771-200">Get the add-in for your organization</span></span>

> [!NOTE]
> <span data-ttu-id="cb771-201">L’apparition du module dans votre organisation peut prendre jusqu’à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="cb771-201">It could take up to 12 hours for the add-in to appear in your organization.</span></span>

1. <span data-ttu-id="cb771-202">Dans le Microsoft 365 d’administration, allez à  la page Paramètres de l’utilisateur à \>  l’adresse <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> suivante :</span><span class="sxs-lookup"><span data-stu-id="cb771-202">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>.</span></span> <span data-ttu-id="cb771-203">Si vous ne voyez pas la page Des  applications intégrées, **rendez-vous** sur le lien Paramètres Applications intégrées en haut de la \>  \>  page **Applications intégrées.**</span><span class="sxs-lookup"><span data-stu-id="cb771-203">If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

2. <span data-ttu-id="cb771-204">Sélectionnez **Déployer le add-in** en haut de la page, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cb771-204">Select **Deploy Add-in** at the top of the page, and then select **Next**.</span></span>

   ![Page Services et add-ins dans le centre d’administration Microsoft 365'administration](../../media/ServicesAddInsPageNewM365AdminCenter.png)

3. <span data-ttu-id="cb771-206">Dans le **volant Déployer un** nouveau module complémentaire qui s’affiche, examinez les informations, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cb771-206">In the **Deploy a new add-in** flyout that appears, review the information, and then click **Next**.</span></span>

4. <span data-ttu-id="cb771-207">Sur la page suivante, cliquez sur **Choisir dans le Store.**</span><span class="sxs-lookup"><span data-stu-id="cb771-207">On the next page, click **Choose from the Store**.</span></span>

   ![Déployer une nouvelle page de modules](../../media/NewAddInScreen2.png)

5. <span data-ttu-id="cb771-209">Dans la page Sélectionner **un add-in** qui s’affiche, cliquez dans  la zone De recherche, entrez **Hameçonnage** de rapport, puis cliquez sur Icône  ![ ](../../media/search-icon.png) Recherche.</span><span class="sxs-lookup"><span data-stu-id="cb771-209">In the **Select add-in** page that appears, click in the **Search** box, enter **Report Phishing**, and then click **Search** ![Search icon](../../media/search-icon.png).</span></span> <span data-ttu-id="cb771-210">Dans la liste des résultats, recherchez **l’hameçonnage** de rapport, puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="cb771-210">In the list of results, find **Report Phishing** and then click **Add**.</span></span>

6. <span data-ttu-id="cb771-211">Dans la boîte de dialogue qui s’affiche, examinez les informations de licence et de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="cb771-211">In the dialog that appears, review the licensing and privacy information, and then click **Continue**.</span></span>

7. <span data-ttu-id="cb771-212">Dans la page **Configurer le add-in** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="cb771-212">In the **Configure add-in** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="cb771-213">**Utilisateurs affectés**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb771-213">**Assigned users**: Select one of the following values:</span></span>

     - <span data-ttu-id="cb771-214">**Tout le monde** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="cb771-214">**Everyone** (default)</span></span>
     - <span data-ttu-id="cb771-215">**Utilisateurs/groupes spécifiques**</span><span class="sxs-lookup"><span data-stu-id="cb771-215">**Specific users / groups**</span></span>
     - <span data-ttu-id="cb771-216">**Juste moi**</span><span class="sxs-lookup"><span data-stu-id="cb771-216">**Just me**</span></span>

   - <span data-ttu-id="cb771-217">**Méthode de déploiement**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb771-217">**Deployment method**: Select one of the following values:</span></span>

     - <span data-ttu-id="cb771-218">**Fixe (par défaut)**: le add-in est automatiquement déployé pour les utilisateurs spécifiés et ils ne peuvent pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="cb771-218">**Fixed (Default)**: The add-in is automatically deployed to the specified users and they can't remove it.</span></span>
     - <span data-ttu-id="cb771-219">**Disponible**: les utilisateurs peuvent installer le add-in sur **Home** \> **Get add-ins** \> **géré par l’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="cb771-219">**Available**: Users can install the add-in at **Home** \> **Get add-ins** \> **Admin-managed**.</span></span>
     - <span data-ttu-id="cb771-220">**Facultatif**: le add-in est automatiquement déployé pour les utilisateurs spécifiés, mais ils peuvent choisir de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="cb771-220">**Optional**: The add-in is automatically deployed to the specified users, but they can choose to remove it.</span></span>

   <span data-ttu-id="cb771-221">Lorsque vous avez terminé, cliquez sur **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="cb771-221">When you're finished, click **Deploy**.</span></span>

8. <span data-ttu-id="cb771-222">Dans la page **Déployer** le hameçonnage de rapport qui s’affiche, vous verrez un rapport d’avancement suivi d’une confirmation du déploiement du module.</span><span class="sxs-lookup"><span data-stu-id="cb771-222">In the **Deploy Report Phishing** page that appears, you'll see a progress report followed by a confirmation that the add-in was deployed.</span></span> <span data-ttu-id="cb771-223">Après avoir lu les informations, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cb771-223">After you read the information, click **Next**.</span></span>

9. <span data-ttu-id="cb771-224">Dans la page **Annoncer le add-in** qui s’affiche, examinez les informations, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="cb771-224">On the **Announce add-in** page that appears, review the information, and then click **Close**.</span></span>

## <a name="review-or-edit-settings-for-the-report-phishing-add-in"></a><span data-ttu-id="cb771-225">Examiner ou modifier les paramètres du module de signalement du hameçonnage</span><span class="sxs-lookup"><span data-stu-id="cb771-225">Review or edit settings for the Report Phishing add-in</span></span>

1. <span data-ttu-id="cb771-226">Dans le Microsoft 365 d’administration, allez à  la page Paramètres de l’utilisateur à \>  l’adresse <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> suivante :</span><span class="sxs-lookup"><span data-stu-id="cb771-226">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>.</span></span> <span data-ttu-id="cb771-227">Si vous ne voyez pas la page Des  applications intégrées, **rendez-vous** sur le lien Paramètres Applications intégrées en haut de la \>  \>  page **Applications intégrées.**</span><span class="sxs-lookup"><span data-stu-id="cb771-227">If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

2. <span data-ttu-id="cb771-228">Recherchez et sélectionnez **le** module de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="cb771-228">Find and select the **Report Phishing** add-in.</span></span>

3. <span data-ttu-id="cb771-229">Dans le volant **Modifier le hameçonnage** du rapport qui s’affiche, examinez et modifiez les paramètres selon les cas de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cb771-229">In the **Edit Report Phishing** flyout that appears, review, and edit settings as appropriate for your organization.</span></span> <span data-ttu-id="cb771-230">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cb771-230">When you're finished, click **Save**.</span></span>
