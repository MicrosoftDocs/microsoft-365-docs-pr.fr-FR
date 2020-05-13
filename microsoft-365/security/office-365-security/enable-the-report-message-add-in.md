---
title: Activez le complément Signaler un message
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Découvrez comment activer le complément de message de rapport pour Outlook et Outlook sur le Web, pour des utilisateurs individuels ou l’ensemble de votre organisation.
ms.openlocfilehash: 67fe2112e5d507ac1f0dc78ffa3534ebc9874916
ms.sourcegitcommit: 93c0088d272cd45f1632a1dcaf04159f234abccd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2020
ms.locfileid: "44209486"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="b7330-103">Activez le complément Signaler un message</span><span class="sxs-lookup"><span data-stu-id="b7330-103">Enable the Report Message add-in</span></span>

> [!NOTE]
> <span data-ttu-id="b7330-104">Si vous êtes administrateur dans une organisation Microsoft 365 avec des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail d’envoi dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="b7330-104">If you're an admin in a Microsoft 365 organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="b7330-105">Pour plus d’informations, consultez la rubrique [utiliser la soumission de l’administrateur pour envoyer des courriers indésirables, des hameçons, des URL et des fichiers à Microsoft](admin-submission.md).</span><span class="sxs-lookup"><span data-stu-id="b7330-105">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

<span data-ttu-id="b7330-106">Le complément de message de rapport pour Outlook et Outlook sur le Web (anciennement appelé Outlook Web App) permet aux utilisateurs de signaler facilement les faux positifs (courrier électronique marqué comme incorrect) ou les faux négatifs (courrier incorrect autorisé) à Microsoft et à ses filiales pour analyse.</span><span class="sxs-lookup"><span data-stu-id="b7330-106">The Report Message add-in for Outlook and Outlook on the web (formerly known as Outlook Web App) enables people to easily report false positives (good email marked as bad) or false negatives (bad email allowed) to Microsoft and its affiliates for analysis.</span></span> <span data-ttu-id="b7330-107">Microsoft utilise ces soumissions pour améliorer l’efficacité des technologies de protection de la messagerie.</span><span class="sxs-lookup"><span data-stu-id="b7330-107">Microsoft uses these submissions to improve the effectiveness of email protection technologies.</span></span>

<span data-ttu-id="b7330-108">Par exemple, supposons que des personnes signalent un grand nombre de messages comme hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="b7330-108">For example, suppose that people are reporting a lot of messages as phishing.</span></span> <span data-ttu-id="b7330-109">Ces informations sont représentées dans le [tableau de bord de sécurité](security-dashboard.md) et d’autres rapports.</span><span class="sxs-lookup"><span data-stu-id="b7330-109">This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports.</span></span> <span data-ttu-id="b7330-110">L’équipe de sécurité de votre organisation peut utiliser ces informations pour indiquer que les stratégies de détection d’hameçonnage doivent être mises à jour.</span><span class="sxs-lookup"><span data-stu-id="b7330-110">Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated.</span></span> <span data-ttu-id="b7330-111">Ou bien, si des personnes signalent un grand nombre de messages marqués comme légitimes comme légitimes à l’aide du complément de message de rapport, il se peut que l’équipe de sécurité de votre organisation doive ajuster les [stratégies de blocage du courrier](configure-your-spam-filter-policies.md)indésirable.</span><span class="sxs-lookup"><span data-stu-id="b7330-111">Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-your-spam-filter-policies.md).</span></span>

<span data-ttu-id="b7330-112">En outre, si votre organisation utilise [Office 365 Advanced Threat Protection Plan 1](office-365-atp.md) ou [plan 2](office-365-ti.md), le complément Report message fournit à l’équipe de sécurité de votre organisation des informations utiles qu’il peut utiliser pour examiner et mettre à jour les stratégies de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b7330-112">In addition, if your organization is using [Office 365 Advanced Threat Protection Plan 1](office-365-atp.md) or [Plan 2](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span>

<span data-ttu-id="b7330-113">Les administrateurs peuvent activer le complément de message de rapport pour l’organisation, et les utilisateurs individuels peuvent l’installer pour eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="b7330-113">Admins can enable the Report Message add-in for the organization, and individual users can install it for themselves.</span></span>

<span data-ttu-id="b7330-114">Si vous êtes un utilisateur individuel, vous pouvez [activer le complément de rapport de message pour vous-même](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="b7330-114">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span>

<span data-ttu-id="b7330-115">Si vous êtes un administrateur général ou un administrateur Exchange Online et qu’Exchange est configuré pour utiliser l’authentification OAuth, vous pouvez [activer le complément de message de rapport pour votre organisation](#get-and-enable-the-report-message-add-in-for-your-organization).</span><span class="sxs-lookup"><span data-stu-id="b7330-115">If you're a global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization).</span></span> <span data-ttu-id="b7330-116">Le complément de message de rapport est désormais disponible via un [déploiement centralisé](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span><span class="sxs-lookup"><span data-stu-id="b7330-116">The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="b7330-117">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b7330-117">What do you need to know before you begin?</span></span>

- <span data-ttu-id="b7330-118">Le complément de message de rapport fonctionne avec la plupart des abonnements Microsoft 365 et les produits suivants :</span><span class="sxs-lookup"><span data-stu-id="b7330-118">The Report Message add-in works with most Microsoft 365 subscriptions and the following products:</span></span>

  - <span data-ttu-id="b7330-119">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="b7330-119">Outlook on the web</span></span>
  - <span data-ttu-id="b7330-120">Outlook 2013 SP1 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b7330-120">Outlook 2013 SP1 or later</span></span>
  - <span data-ttu-id="b7330-121">Outlook 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="b7330-121">Outlook 2016 for Mac</span></span>
  - <span data-ttu-id="b7330-122">Outlook inclus avec les applications Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="b7330-122">Outlook included with Microsoft 365 apps for Enterprise</span></span>

- <span data-ttu-id="b7330-123">Le complément de message de rapport n’est pas disponible pour l’instant :</span><span class="sxs-lookup"><span data-stu-id="b7330-123">The Report Message add-in is currently not available for:</span></span>

  - <span data-ttu-id="b7330-124">Boîtes aux lettres dans l’organisation Exchange locale</span><span class="sxs-lookup"><span data-stu-id="b7330-124">Mailboxes in on-premises Exchange organizations</span></span>
  - <span data-ttu-id="b7330-125">Abonnements GCC, GCC HIGH ou DoD</span><span class="sxs-lookup"><span data-stu-id="b7330-125">GCC, GCC HIGH, or DoD subscriptions</span></span>

- <span data-ttu-id="b7330-126">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="b7330-126">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="b7330-127">Pour plus d’informations, consultez [la rubrique spécifier une boîte aux lettres pour les soumissions utilisateur de messages de courrier indésirable et de hameçonnage dans Exchange Online](user-submission.md).</span><span class="sxs-lookup"><span data-stu-id="b7330-127">For more information, see [Specify a mailbox for user submissions of spam and phishing messages in Exchange Online](user-submission.md).</span></span>

- <span data-ttu-id="b7330-128">Votre navigateur Web existant doit fonctionner avec le complément de message de rapport.</span><span class="sxs-lookup"><span data-stu-id="b7330-128">Your existing web browser should work with the Report Message add-in.</span></span> <span data-ttu-id="b7330-129">Toutefois, si vous remarquez que le complément n’est pas disponible ou ne fonctionne pas comme prévu, essayez un autre navigateur.</span><span class="sxs-lookup"><span data-stu-id="b7330-129">But, if you notice the add-in is not available or not working as expected, try a different browser.</span></span>

- <span data-ttu-id="b7330-130">Pour les installations organisationnelles, l’organisation doit être configurée pour utiliser l’authentification OAuth.</span><span class="sxs-lookup"><span data-stu-id="b7330-130">For organizational installs, the organization needs to be configured to use OAuth authentication.</span></span> <span data-ttu-id="b7330-131">Pour plus d’informations, reportez-vous à [la rubrique déterminer si un déploiement centralisé de compléments fonctionne pour votre organisation](../../admin/manage/centralized-deployment-of-add-ins.md).</span><span class="sxs-lookup"><span data-stu-id="b7330-131">For more information, see [Determine if Centralized Deployment of add-ins works for your organization](../../admin/manage/centralized-deployment-of-add-ins.md).</span></span>

- <span data-ttu-id="b7330-132">Les administrateurs doivent être membres du groupe de rôles global admins.</span><span class="sxs-lookup"><span data-stu-id="b7330-132">Admins need to be a member of the Global admins role group.</span></span> <span data-ttu-id="b7330-133">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="b7330-133">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="b7330-134">Obtenir le complément de message de rapport pour vous-même</span><span class="sxs-lookup"><span data-stu-id="b7330-134">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="b7330-135">Accédez au site Microsoft AppSource à l’adresse <https://appsource.microsoft.com/marketplace/apps> et recherchez le complément de message de rapport.</span><span class="sxs-lookup"><span data-stu-id="b7330-135">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Message add-in.</span></span> <span data-ttu-id="b7330-136">Pour accéder directement au complément de message de rapport, accédez à <https://appsource.microsoft.com/product/office/wa104381180> .</span><span class="sxs-lookup"><span data-stu-id="b7330-136">To go directly to the Report Message add-in, go to <https://appsource.microsoft.com/product/office/wa104381180>.</span></span>

2. <span data-ttu-id="b7330-137">Cliquez sur **obtenir maintenant**.</span><span class="sxs-lookup"><span data-stu-id="b7330-137">Click **GET IT NOW**.</span></span>

   ![Message de rapport-Get it](../../media/ReportMessageGETITNOW.png)

3. <span data-ttu-id="b7330-139">Dans la boîte de dialogue qui s’affiche, passez en revue les conditions d’utilisation et la politique de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="b7330-139">In the dialog that appears, review the terms of use and privacy policy, and then click **Continue**.</span></span>

4. <span data-ttu-id="b7330-140">Connectez-vous à l’aide de votre compte professionnel ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour une utilisation personnelle).</span><span class="sxs-lookup"><span data-stu-id="b7330-140">Sign in using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>

<span data-ttu-id="b7330-141">Une fois le complément installé et activé, les icônes suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="b7330-141">After the add-in is installed and enabled, you'll see the following icons:</span></span>

- <span data-ttu-id="b7330-142">Dans Outlook, l’icône se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="b7330-142">In Outlook, the icon looks like this:</span></span>

  ![Icône de complément de rapport de message pour Outlook](../../media/OutlookReportMessageIcon.png)

- <span data-ttu-id="b7330-144">Dans Outlook sur le Web, l’icône se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="b7330-144">In Outlook on the web, the icon looks like this:</span></span>

  ![Icône de complément de message de rapport Web Outlook sur le Web](../../media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)

<span data-ttu-id="b7330-146">Pour savoir comment utiliser le complément, voir [use the Report message Add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="b7330-146">To learn how to use the add-in, see [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="b7330-147">Obtenir et activer le complément de message de rapport pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="b7330-147">Get and enable the Report Message add-in for your organization</span></span>

> [!NOTE]
> <span data-ttu-id="b7330-148">Le complément peut prendre jusqu’à 12 heures pour apparaître dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b7330-148">It could take up to 12 hours for the add-in to appear in your organization.</span></span>

1. <span data-ttu-id="b7330-149">Dans le centre d’administration Microsoft 365, accédez à la page des **compléments de Services &** , puis <https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns> cliquez sur **déployer le complément**.</span><span class="sxs-lookup"><span data-stu-id="b7330-149">In the Microsoft 365 admin center, go to the **Services & add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns>, and then click **Deploy Add-In**.</span></span>

   ![Page services et compléments dans le centre d’administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

2. <span data-ttu-id="b7330-151">Dans le menu **déroulant déployer un nouveau complément** qui s’affiche, passez en revue les informations, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b7330-151">In the **Deploy a new add-in** flyout that appears, review the information, and then click **Next**.</span></span>

3. <span data-ttu-id="b7330-152">Sur la page suivante, cliquez sur **choisir dans le Store**.</span><span class="sxs-lookup"><span data-stu-id="b7330-152">On the next page, click **Choose from the Store**.</span></span>

   ![Déployer une nouvelle page de complément](../../media/NewAddInScreen2.png)

4. <span data-ttu-id="b7330-154">Dans la page **Sélectionner un complément** qui s’affiche, cliquez sur dans la zone de **recherche** , entrez **message de rapport**, **puis cliquez sur** ![ icône de recherche de recherche ](../../media/search-icon.png) .</span><span class="sxs-lookup"><span data-stu-id="b7330-154">In the **Select add-in** page that appears, click in the **Search** box, enter **Report Message**, and then click **Search** ![Search icon](../../media/search-icon.png).</span></span> <span data-ttu-id="b7330-155">Dans la liste des résultats, recherchez **message de rapport** , puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b7330-155">In the list of results, find **Report Message** and then click **Add**.</span></span>

   ![Sélectionner les résultats de la recherche de complément](../../media/NewAddInScreen3.png)

5. <span data-ttu-id="b7330-157">Dans la boîte de dialogue qui s’affiche, vérifiez les informations de licence et de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="b7330-157">In the dialog that appears, review the licensing and privacy information, and then click **Continue**.</span></span>

6. <span data-ttu-id="b7330-158">Dans la page **configurer le complément** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="b7330-158">In the **Configure add-in** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="b7330-159">**Utilisateurs affectés**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7330-159">**Assigned users**: Select one of the following values:</span></span>

     - <span data-ttu-id="b7330-160">**Tout le monde** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b7330-160">**Everyone** (default)</span></span>
     - <span data-ttu-id="b7330-161">**Utilisateurs/groupes spécifiques**</span><span class="sxs-lookup"><span data-stu-id="b7330-161">**Specific users / groups**</span></span>
     - <span data-ttu-id="b7330-162">**Juste moi**</span><span class="sxs-lookup"><span data-stu-id="b7330-162">**Just me**</span></span>

   - <span data-ttu-id="b7330-163">**Méthode de déploiement**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7330-163">**Deployment method**: Select one of the following values:</span></span>

     - <span data-ttu-id="b7330-164">**Fixed (valeur par défaut)**: le complément est déployé automatiquement sur les utilisateurs spécifiés et ils ne peuvent pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="b7330-164">**Fixed (Default)**: The add-in is automatically deployed to the specified users and they can't remove it.</span></span>
     - <span data-ttu-id="b7330-165">**Disponible**: les utilisateurs peuvent installer le complément à **leur domicile** \> **obtenir des compléments** \> **gérés par l’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="b7330-165">**Available**: Users can install the add-in at **Home** \> **Get add-ins** \> **Admin-managed**.</span></span>
     - <span data-ttu-id="b7330-166">**Facultatif**: le complément est déployé automatiquement sur les utilisateurs spécifiés, mais ils peuvent choisir de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="b7330-166">**Optional**: The add-in is automatically deployed to the specified users, but they can choose to remove it.</span></span>

   ![Page Configurer le complément](../../media/configure-add-in.png)

   <span data-ttu-id="b7330-168">Lorsque vous avez terminé, cliquez sur **déployer**.</span><span class="sxs-lookup"><span data-stu-id="b7330-168">When you're finished, click **Deploy**.</span></span>

7. <span data-ttu-id="b7330-169">Dans la page **déployer un message de rapport** qui s’affiche, vous verrez un rapport d’avancement suivi d’une confirmation de déploiement du complément.</span><span class="sxs-lookup"><span data-stu-id="b7330-169">In the **Deploy Report Message** page that appears, you'll see a progress report followed by a confirmation that the add-in was deployed.</span></span> <span data-ttu-id="b7330-170">Une fois que vous avez lu les informations, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b7330-170">After you read the information, click **Next**.</span></span>

   ![Page déployer un message de rapport](../../media/deploy-report-message-page.png)

8. <span data-ttu-id="b7330-172">Sur la page **complément annonce** , vérifiez les informations, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b7330-172">On the **Announce add-in** page that appears, review the information, and then click **Close**.</span></span>

   ![Annoncer la page de complément](../../media/announce-add-in-page.png)

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="b7330-174">En savoir plus sur l’utilisation du complément de message de rapport</span><span class="sxs-lookup"><span data-stu-id="b7330-174">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="b7330-175">Les personnes auxquelles le complément est attribué voient les icônes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7330-175">People who have the add-in assigned to them will see the following icons:</span></span>

- <span data-ttu-id="b7330-176">Dans Outlook, l’icône se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="b7330-176">In Outlook, the icon looks like this:</span></span>

  ![Icône de complément de rapport de message pour Outlook](../../media/OutlookReportMessageIcon.png)

- <span data-ttu-id="b7330-178">Dans Outlook sur le Web, l’icône se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="b7330-178">In Outlook on the web, the icon looks like this:</span></span>

  ![Icône de complément de message de rapport Web Outlook sur le Web](../../media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)

<span data-ttu-id="b7330-180">Lorsque vous informez les utilisateurs du complément Report message, incluez un lien permettant d' [utiliser le complément Report message](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="b7330-180">When you notify users about the Report Message add-in, include a link to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="b7330-181">Vérifier ou modifier les paramètres du complément de message de rapport</span><span class="sxs-lookup"><span data-stu-id="b7330-181">Review or edit settings for the Report Message add-in</span></span>

1. <span data-ttu-id="b7330-182">Dans le centre d’administration Microsoft 365, accédez à la page des **compléments de Services &** à l’adresse <https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns> .</span><span class="sxs-lookup"><span data-stu-id="b7330-182">In the Microsoft 365 admin center, go to the **Services & add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns>.</span></span>

   ![Page services et compléments dans le nouveau centre d’administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

2. <span data-ttu-id="b7330-184">Recherchez et sélectionnez le complément **Report message** .</span><span class="sxs-lookup"><span data-stu-id="b7330-184">Find and select the **Report Message** add-in.</span></span>

3. <span data-ttu-id="b7330-185">Dans la fenêtre mobile **modifier un message** qui s’affiche, vérifiez et modifiez les paramètres en fonction de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b7330-185">In the **Edit Report Message** flyout that appears, review and edit settings as appropriate for your organization.</span></span> <span data-ttu-id="b7330-186">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b7330-186">When you're finished, click **Save**.</span></span>

   ![Paramètres du complément de message de rapport](../../media/EditReportMessageAddIn.png)

## <a name="view-and-review-reported-messages"></a><span data-ttu-id="b7330-188">Afficher et consulter les messages signalés</span><span class="sxs-lookup"><span data-stu-id="b7330-188">View and review reported messages</span></span>

<span data-ttu-id="b7330-189">Pour passer en revue les messages que les utilisateurs signalent à Microsoft, vous disposez des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7330-189">To review messages that users report to Microsoft, you have these options:</span></span>

- <span data-ttu-id="b7330-190">Utiliser le portail de soumission des administrateurs.</span><span class="sxs-lookup"><span data-stu-id="b7330-190">Use the Admin Submissions portal.</span></span> <span data-ttu-id="b7330-191">Pour plus d’informations, consultez la rubrique [afficher les soumissions des utilisateurs à Microsoft](admin-submission.md#view-user-submissions-to-microsoft).</span><span class="sxs-lookup"><span data-stu-id="b7330-191">For more information, see [View user submissions to Microsoft](admin-submission.md#view-user-submissions-to-microsoft).</span></span>

- <span data-ttu-id="b7330-192">Créer une règle de flux de messagerie (également appelée règle de transport) pour envoyer des copies des messages signalés.</span><span class="sxs-lookup"><span data-stu-id="b7330-192">Create a mail flow rule (also known as a transport rule) to send copies of reported messages.</span></span> <span data-ttu-id="b7330-193">Pour obtenir des instructions, consultez [la rubrique utiliser des règles de flux de messagerie pour voir ce que vos utilisateurs signalent à Microsoft](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="b7330-193">For instructions, see [Use mail flow rules to see what your users are reporting to Microsoft](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md).</span></span>
