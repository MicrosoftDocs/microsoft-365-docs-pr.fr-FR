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
ms.openlocfilehash: 9b21472736cff2fd0eed7da5495ab6aae597032f
ms.sourcegitcommit: c0cfb9b354db56fdd329aec2a89a9b2cf160c4b0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "50094854"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="d0258-103">Activez le complément Signaler un message</span><span class="sxs-lookup"><span data-stu-id="d0258-103">Enable the Report Message add-in</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


> [!NOTE]
> <span data-ttu-id="d0258-104">Si vous êtes un administrateur d’une organisation Microsoft 365 avec des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="d0258-104">If you're an admin in a Microsoft 365 organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="d0258-105">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="d0258-105">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

<span data-ttu-id="d0258-106">Les add-ins Signaler le message et Signaler le hameçonnage pour Outlook et Outlook sur le web (anciennement Outlook Web App) permettent aux utilisateurs de signaler facilement les faux positifs (messages électroniques de qualité marqués comme faux) ou les faux négatifs (courrier électronique non autorisé) à Microsoft et à ses affiliés pour analyse.</span><span class="sxs-lookup"><span data-stu-id="d0258-106">The Report Message and Report Phishing add-ins for Outlook and Outlook on the web (formerly known as Outlook Web App) enables people to easily report false positives (good email marked as bad) or false negatives (bad email allowed) to Microsoft and its affiliates for analysis.</span></span>

<span data-ttu-id="d0258-107">Microsoft utilise ces soumissions pour améliorer l’efficacité des technologies de protection de la messagerie.</span><span class="sxs-lookup"><span data-stu-id="d0258-107">Microsoft uses these submissions to improve the effectiveness of email protection technologies.</span></span> <span data-ttu-id="d0258-108">Par exemple, si des personnes signalent un grand nombre de messages marqués comme courrier indésirable à l’aide du add-in Signaler un message, l’équipe de sécurité de votre organisation devra peut-être ajuster les stratégies [anti-courrier](configure-your-spam-filter-policies.md)indésirable.</span><span class="sxs-lookup"><span data-stu-id="d0258-108">For example, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-your-spam-filter-policies.md).</span></span>

<span data-ttu-id="d0258-109">Vous pouvez installer le add-in Signaler le message ou Signaler le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="d0258-109">You can install either the Report Message or Report Phishing add-in.</span></span> <span data-ttu-id="d0258-110">Si vous souhaitez que vos utilisateurs signalent uniquement les messages de hameçonnage, déployez le module de signalement du hameçonnage dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d0258-110">If you want your users to report only phishing messages, deploy the Report Phishing add-in in your organization.</span></span> <span data-ttu-id="d0258-111">Pour plus d’informations, [voir Enable the Report Phishing add-in](enable-the-report-phish-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="d0258-111">For more information, see [Enable the Report Phishing add-in](enable-the-report-phish-add-in.md).</span></span>

<span data-ttu-id="d0258-112">Le add-in Report Message offre la possibilité de signaler les messages de courrier indésirable et de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="d0258-112">The Report Message add-in provides the option to report both spam and phishing messages.</span></span> <span data-ttu-id="d0258-113">Les administrateurs peuvent activer le add-in Message de rapport pour l’organisation, et les utilisateurs individuels peuvent l’installer eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="d0258-113">Admins can enable the Report Message add-in for the organization, and individual users can install it for themselves.</span></span>

<span data-ttu-id="d0258-114">Si vous êtes un utilisateur individuel, vous pouvez activer le module de rapport de [message pour vous-même.](#get-the-report-message-add-in-for-yourself)</span><span class="sxs-lookup"><span data-stu-id="d0258-114">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span>

<span data-ttu-id="d0258-115">Si vous êtes un administrateur général ou un administrateur Exchange Online et qu’Exchange est configuré pour utiliser l’authentification OAuth, vous pouvez activer le [add-in](#get-and-enable-the-report-message-add-in-for-your-organization)Message de rapport pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d0258-115">If you're a global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization).</span></span> <span data-ttu-id="d0258-116">Le message de Add-In est désormais disponible via [le déploiement centralisé.](https://docs.microsoft.com/microsoft-365/admin/manage/centralized-deployment-of-add-ins)</span><span class="sxs-lookup"><span data-stu-id="d0258-116">The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/microsoft-365/admin/manage/centralized-deployment-of-add-ins).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="d0258-117">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="d0258-117">What do you need to know before you begin?</span></span>

- <span data-ttu-id="d0258-118">Le add-in Message de rapport fonctionne avec la plupart des abonnements Microsoft 365 et les produits suivants :</span><span class="sxs-lookup"><span data-stu-id="d0258-118">The Report Message add-in works with most Microsoft 365 subscriptions and the following products:</span></span>

  - <span data-ttu-id="d0258-119">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="d0258-119">Outlook on the web</span></span>
  - <span data-ttu-id="d0258-120">Outlook 2013 SP1 ou une édition ultérieure</span><span class="sxs-lookup"><span data-stu-id="d0258-120">Outlook 2013 SP1 or later</span></span>
  - <span data-ttu-id="d0258-121">Outlook 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="d0258-121">Outlook 2016 for Mac</span></span>
  - <span data-ttu-id="d0258-122">Outlook inclus dans les applications Microsoft 365 pour Entreprise</span><span class="sxs-lookup"><span data-stu-id="d0258-122">Outlook included with Microsoft 365 apps for Enterprise</span></span>
  - <span data-ttu-id="d0258-123">Application Outlook pour iOS et Android</span><span class="sxs-lookup"><span data-stu-id="d0258-123">Outlook app for iOS and Android</span></span>

- <span data-ttu-id="d0258-124">Le module de rapport de message n’est pas disponible pour les boîtes aux lettres dans les organisations Exchange locales.</span><span class="sxs-lookup"><span data-stu-id="d0258-124">The Report Message add-in is not available for mailboxes in on-premises Exchange organizations.</span></span>

- <span data-ttu-id="d0258-125">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="d0258-125">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="d0258-126">Pour plus d’informations, voir [Stratégies d’envoi des utilisateurs.](user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="d0258-126">For more information, see [User submissions policies](user-submission.md).</span></span>

- <span data-ttu-id="d0258-127">Votre navigateur web existant doit fonctionner avec le add-in Message de rapport.</span><span class="sxs-lookup"><span data-stu-id="d0258-127">Your existing web browser should work with the Report Message add-in.</span></span> <span data-ttu-id="d0258-128">Toutefois, si vous remarquez que le module n’est pas disponible ou ne fonctionne pas comme prévu, essayez un autre navigateur.</span><span class="sxs-lookup"><span data-stu-id="d0258-128">But, if you notice the add-in is not available or not working as expected, try a different browser.</span></span>

- <span data-ttu-id="d0258-129">Pour les installation organisationnelles, l’organisation doit être configurée pour utiliser l’authentification OAuth.</span><span class="sxs-lookup"><span data-stu-id="d0258-129">For organizational installs, the organization needs to be configured to use OAuth authentication.</span></span> <span data-ttu-id="d0258-130">Pour plus d’informations, [voir Determine if Centralized Deployment of add-ins works for your organization.](../../admin/manage/centralized-deployment-of-add-ins.md)</span><span class="sxs-lookup"><span data-stu-id="d0258-130">For more information, see [Determine if Centralized Deployment of add-ins works for your organization](../../admin/manage/centralized-deployment-of-add-ins.md).</span></span>

- <span data-ttu-id="d0258-131">Les administrateurs doivent être membres du groupe de rôles Administrateurs globaux.</span><span class="sxs-lookup"><span data-stu-id="d0258-131">Admins need to be a member of the Global admins role group.</span></span> <span data-ttu-id="d0258-132">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="d0258-132">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="d0258-133">Obtenir le add-in Message de rapport pour vous-même</span><span class="sxs-lookup"><span data-stu-id="d0258-133">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="d0258-134">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Message add-in.</span><span class="sxs-lookup"><span data-stu-id="d0258-134">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Message add-in.</span></span> <span data-ttu-id="d0258-135">To go directly to the Report Message add-in, go to <https://appsource.microsoft.com/product/office/wa104381180> .</span><span class="sxs-lookup"><span data-stu-id="d0258-135">To go directly to the Report Message add-in, go to <https://appsource.microsoft.com/product/office/wa104381180>.</span></span>

2. <span data-ttu-id="d0258-136">Cliquez **sur GET IT NOW**.</span><span class="sxs-lookup"><span data-stu-id="d0258-136">Click **GET IT NOW**.</span></span>

   ![Message de rapport : l’obtenir maintenant](../../media/ReportMessageGETITNOW.png)

3. <span data-ttu-id="d0258-138">Dans la boîte de dialogue qui s’affiche, examinez les conditions d’utilisation et la politique de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="d0258-138">In the dialog that appears, review the terms of use and privacy policy, and then click **Continue**.</span></span>

4. <span data-ttu-id="d0258-139">Connectez-vous à l’aide de votre compte scolaire ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour un usage personnel).</span><span class="sxs-lookup"><span data-stu-id="d0258-139">Sign in using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>

<span data-ttu-id="d0258-140">Une fois le add-in installé et activé, les icônes suivantes s’offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="d0258-140">After the add-in is installed and enabled, you'll see the following icons:</span></span>

- <span data-ttu-id="d0258-141">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="d0258-141">In Outlook, the icon looks like this:</span></span>

  ![Icône signaler le add-in Message pour Outlook](../../media/OutlookReportMessageIcon.png)

- <span data-ttu-id="d0258-143">Dans Outlook sur le web, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="d0258-143">In Outlook on the web, the icon looks like this:</span></span>

  ![Icône du add-in Message de rapport Outlook sur le web](../../media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)

<span data-ttu-id="d0258-145">Pour savoir comment utiliser le add-in, voir Utiliser le [add-in Message de rapport.](https://support.microsoft.com/office/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)</span><span class="sxs-lookup"><span data-stu-id="d0258-145">To learn how to use the add-in, see [Use the Report Message add-in](https://support.microsoft.com/office/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="d0258-146">Obtenir et activer le add-in Message de rapport pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="d0258-146">Get and enable the Report Message add-in for your organization</span></span>

> [!NOTE]
> <span data-ttu-id="d0258-147">L’apparition du module dans votre organisation peut prendre jusqu’à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="d0258-147">It could take up to 12 hours for the add-in to appear in your organization.</span></span>

1. <span data-ttu-id="d0258-148">Dans le Centre d’administration Microsoft 365, rendez-vous sur la page **Paramètres** des applications à l’adresse suivante : Si vous ne voyez pas la page Des applications \>  <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> intégrées,   \>  \> **rendez-vous**  sur le lien Paramètres applications intégrées en haut de la page Applications intégrées.</span><span class="sxs-lookup"><span data-stu-id="d0258-148">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>, If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

2. <span data-ttu-id="d0258-149">Sélectionnez **Déployer le add-in** en haut de la page, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d0258-149">Select **Deploy Add-in** at the top of the page, and then select **Next**.</span></span>

   ![Page Services et modules dans le Centre d’administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

3. <span data-ttu-id="d0258-151">Dans le **volant Déployer un** nouveau module complémentaire qui s’affiche, examinez les informations, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d0258-151">In the **Deploy a new add-in** flyout that appears, review the information, and then click **Next**.</span></span>

4. <span data-ttu-id="d0258-152">Sur la page suivante, cliquez **sur Choisir dans le Store.**</span><span class="sxs-lookup"><span data-stu-id="d0258-152">On the next page, click **Choose from the Store**.</span></span>

   ![Déployer une nouvelle page de modules](../../media/NewAddInScreen2.png)

5. <span data-ttu-id="d0258-154">Dans la page **Sélectionner un add-in** qui s’affiche, cliquez dans la zone De recherche, entrez Message de rapport, puis cliquez sur **Icône**   ![ ](../../media/search-icon.png) Rechercher.</span><span class="sxs-lookup"><span data-stu-id="d0258-154">In the **Select add-in** page that appears, click in the **Search** box, enter **Report Message**, and then click **Search** ![Search icon](../../media/search-icon.png).</span></span> <span data-ttu-id="d0258-155">Dans la liste des résultats, recherchez **Message de rapport,** puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="d0258-155">In the list of results, find **Report Message** and then click **Add**.</span></span>

   ![Sélectionner des résultats de recherche de add-in](../../media/NewAddInScreen3.png)

6. <span data-ttu-id="d0258-157">Dans la boîte de dialogue qui s’affiche, examinez les informations de licence et de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="d0258-157">In the dialog that appears, review the licensing and privacy information, and then click **Continue**.</span></span>

7. <span data-ttu-id="d0258-158">Dans la page **Configurer le add-in** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="d0258-158">In the **Configure add-in** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="d0258-159">**Utilisateurs affectés**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d0258-159">**Assigned users**: Select one of the following values:</span></span>

     - <span data-ttu-id="d0258-160">**Tout le monde** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="d0258-160">**Everyone** (default)</span></span>
     - <span data-ttu-id="d0258-161">**Utilisateurs/groupes spécifiques**</span><span class="sxs-lookup"><span data-stu-id="d0258-161">**Specific users / groups**</span></span>
     - <span data-ttu-id="d0258-162">**Juste moi**</span><span class="sxs-lookup"><span data-stu-id="d0258-162">**Just me**</span></span>

   - <span data-ttu-id="d0258-163">**Méthode de déploiement**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d0258-163">**Deployment method**: Select one of the following values:</span></span>

     - <span data-ttu-id="d0258-164">**Fixe (par défaut)**: le add-in est automatiquement déployé pour les utilisateurs spécifiés et ils ne peuvent pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="d0258-164">**Fixed (Default)**: The add-in is automatically deployed to the specified users and they can't remove it.</span></span>
     - <span data-ttu-id="d0258-165">**Disponible**: les utilisateurs peuvent installer le add-in sur **Home** \> **Get add-ins** \> **géré par l’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="d0258-165">**Available**: Users can install the add-in at **Home** \> **Get add-ins** \> **Admin-managed**.</span></span>
     - <span data-ttu-id="d0258-166">**Facultatif**: le add-in est automatiquement déployé pour les utilisateurs spécifiés, mais ils peuvent choisir de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="d0258-166">**Optional**: The add-in is automatically deployed to the specified users, but they can choose to remove it.</span></span>

   ![Configurer la page de l’ajout](../../media/configure-add-in.png)

   <span data-ttu-id="d0258-168">Lorsque vous avez terminé, cliquez sur **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="d0258-168">When you're finished, click **Deploy**.</span></span>

8. <span data-ttu-id="d0258-169">Dans la page Déployer le **message** de rapport qui s’affiche, vous verrez un rapport d’avancement suivi d’une confirmation du déploiement du module.</span><span class="sxs-lookup"><span data-stu-id="d0258-169">In the **Deploy Report Message** page that appears, you'll see a progress report followed by a confirmation that the add-in was deployed.</span></span> <span data-ttu-id="d0258-170">Après avoir lu les informations, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d0258-170">After you read the information, click **Next**.</span></span>

   ![Page Déployer le message de rapport](../../media/deploy-report-message-page.png)

9. <span data-ttu-id="d0258-172">Dans la page **Annoncer le add-in** qui s’affiche, examinez les informations, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d0258-172">On the **Announce add-in** page that appears, review the information, and then click **Close**.</span></span>

   ![Page Annoncer le add-in](../../media/announce-add-in-page.png)

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="d0258-174">Découvrez comment utiliser le add-in Message de rapport</span><span class="sxs-lookup"><span data-stu-id="d0258-174">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="d0258-175">Les personnes à qui le add-in est affecté voient les icônes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d0258-175">People who have the add-in assigned to them will see the following icons:</span></span>

- <span data-ttu-id="d0258-176">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="d0258-176">In Outlook, the icon looks like this:</span></span>

  ![Icône Signaler un add-in de message pour Outlook](../../media/OutlookReportMessageIcon.png)

- <span data-ttu-id="d0258-178">Dans Outlook sur le web, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="d0258-178">In Outlook on the web, the icon looks like this:</span></span>

  ![Icône De message Outlook sur le web](../../media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)

<span data-ttu-id="d0258-180">Lorsque vous informez les utilisateurs du add-in Message de rapport, incluez un lien pour utiliser le [add-in Message de rapport.](https://support.microsoft.com/office/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)</span><span class="sxs-lookup"><span data-stu-id="d0258-180">When you notify users about the Report Message add-in, include a link to [Use the Report Message add-in](https://support.microsoft.com/office/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="d0258-181">Passer en revue ou modifier les paramètres du add-in Message de rapport</span><span class="sxs-lookup"><span data-stu-id="d0258-181">Review or edit settings for the Report Message add-in</span></span>

1. <span data-ttu-id="d0258-182">Dans le Centre d’administration Microsoft 365, rendez-vous sur la page **Paramètres** des applications à l’adresse suivante : Si vous ne voyez pas la page Des applications \>  <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> intégrées,   \>  \> **rendez-vous**  sur le lien Paramètres applications intégrées en haut de la page Applications intégrées.</span><span class="sxs-lookup"><span data-stu-id="d0258-182">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>, If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

   ![Page Services et Add-Ins dans le nouveau Centre d’administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

2. <span data-ttu-id="d0258-184">Recherchez et sélectionnez le add-in **Message** de rapport.</span><span class="sxs-lookup"><span data-stu-id="d0258-184">Find and select the **Report Message** add-in.</span></span>

3. <span data-ttu-id="d0258-185">Dans le **volant Modifier le message** de rapport qui s’affiche, examinez et modifiez les paramètres selon le cas pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d0258-185">In the **Edit Report Message** flyout that appears, review and edit settings as appropriate for your organization.</span></span> <span data-ttu-id="d0258-186">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="d0258-186">When you're finished, click **Save**.</span></span>

   ![Paramètres du add-in Message de rapport](../../media/EditReportMessageAddIn.png)

## <a name="view-and-review-reported-messages"></a><span data-ttu-id="d0258-188">Afficher et examiner les messages signalés</span><span class="sxs-lookup"><span data-stu-id="d0258-188">View and review reported messages</span></span>

<span data-ttu-id="d0258-189">Pour passer en revue les messages que les utilisateurs signalent à Microsoft, vous avez les options ci-après :</span><span class="sxs-lookup"><span data-stu-id="d0258-189">To review messages that users report to Microsoft, you have these options:</span></span>

- <span data-ttu-id="d0258-190">Utilisez le portail Soumissions d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d0258-190">Use the Admin Submissions portal.</span></span> <span data-ttu-id="d0258-191">Pour plus d’informations, voir [Afficher les soumissions d’utilisateurs à Microsoft.](admin-submission.md#view-user-submissions-to-microsoft)</span><span class="sxs-lookup"><span data-stu-id="d0258-191">For more information, see [View user submissions to Microsoft](admin-submission.md#view-user-submissions-to-microsoft).</span></span>

- <span data-ttu-id="d0258-192">Créez une règle de flux de messagerie (également appelée règle de transport) pour envoyer des copies des messages signalés.</span><span class="sxs-lookup"><span data-stu-id="d0258-192">Create a mail flow rule (also known as a transport rule) to send copies of reported messages.</span></span> <span data-ttu-id="d0258-193">Pour obtenir des instructions, voir Utiliser des règles de flux de messagerie pour voir ce [que vos utilisateurs rapportent à Microsoft.](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="d0258-193">For instructions, see [Use mail flow rules to see what your users are reporting to Microsoft](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md).</span></span>
