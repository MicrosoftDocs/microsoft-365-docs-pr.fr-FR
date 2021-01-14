---
title: Activer le module de signalement du hameçonnage
f1.keywords:
- NOCSH
ms.author: siosulli
author: chrisda
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
ms.openlocfilehash: 2ea6a9bf9b00fc844aede6daeb9fc11f23c81e4a
ms.sourcegitcommit: cc354fd54400be0ff0401f60bbe68ed975b69cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/14/2021
ms.locfileid: "49865269"
---
# <a name="enable-the-report-phishing-add-in"></a><span data-ttu-id="825ea-103">Activer le module de signalement du hameçonnage</span><span class="sxs-lookup"><span data-stu-id="825ea-103">Enable the Report Phishing add-in</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


> [!NOTE]
> <span data-ttu-id="825ea-104">Si vous êtes un administrateur d’une organisation Microsoft 365 avec des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="825ea-104">If you're an admin in a Microsoft 365 organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="825ea-105">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="825ea-105">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

<span data-ttu-id="825ea-106">Les add-ins Signaler le message et Signaler le hameçonnage pour Outlook et Outlook sur le web (anciennement Outlook Web App) permettent aux utilisateurs de signaler facilement les faux positifs (messages électroniques de qualité marqués comme faux) ou les faux négatifs (courrier électronique non autorisé) à Microsoft et à ses affiliés pour analyse.</span><span class="sxs-lookup"><span data-stu-id="825ea-106">The Report Message and Report Phishing add-ins for Outlook and Outlook on the web (formerly known as Outlook Web App) enable people to easily report false positives (good email marked as bad) or false negatives (bad email allowed) to Microsoft and its affiliates for analysis.</span></span>

<span data-ttu-id="825ea-107">Microsoft utilise ces soumissions pour améliorer l’efficacité des technologies de protection de la messagerie.</span><span class="sxs-lookup"><span data-stu-id="825ea-107">Microsoft uses these submissions to improve the effectiveness of email protection technologies.</span></span> <span data-ttu-id="825ea-108">Par exemple, supposons que des personnes signalent de nombreux messages à l’aide du module de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="825ea-108">For example, suppose that people are reporting many messages using the Report Phishing add-in.</span></span> <span data-ttu-id="825ea-109">Ces informations sont disponibles dans le Tableau [de bord de](security-dashboard.md) sécurité et d’autres rapports.</span><span class="sxs-lookup"><span data-stu-id="825ea-109">This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports.</span></span> <span data-ttu-id="825ea-110">L’équipe de sécurité de votre organisation peut utiliser ces informations pour indiquer que les stratégies anti-hameçonnage peuvent avoir besoin d’être mises à jour.</span><span class="sxs-lookup"><span data-stu-id="825ea-110">Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated.</span></span>

<span data-ttu-id="825ea-111">Vous pouvez installer le module de rapport de message ou de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="825ea-111">You can install either the Report Message or Report Phishing add-in.</span></span> <span data-ttu-id="825ea-112">Si vous souhaitez que vos utilisateurs signalent à la fois le courrier indésirable et les messages de hameçonnage, déployez le add-in Signaler un message dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="825ea-112">If you want your users to report both spam and phishing messages, deploy the Report Message add-in in your organization.</span></span> <span data-ttu-id="825ea-113">Pour plus d’informations, [voir Activer le add-in Message de rapport.](enable-the-report-message-add-in.md)</span><span class="sxs-lookup"><span data-stu-id="825ea-113">For more information, see [Enable the Report Message add-in](enable-the-report-message-add-in.md).</span></span>

<span data-ttu-id="825ea-114">Le module de signalement du hameçonnage offre la possibilité de signaler uniquement les messages de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="825ea-114">The Report Phishing add-in provides the option to report only phishing messages.</span></span> <span data-ttu-id="825ea-115">Les administrateurs peuvent activer le module de signalement du hameçonnage pour l’organisation, et les utilisateurs individuels peuvent l’installer eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="825ea-115">Admins can enable the Report Phishing add-in for the organization, and individual users can install it for themselves.</span></span>

<span data-ttu-id="825ea-116">Si vous êtes un utilisateur individuel, vous pouvez activer le module de signalement du hameçonnage [pour vous-même.](#get-the-report-phishing-add-in-for-yourself)</span><span class="sxs-lookup"><span data-stu-id="825ea-116">If you're an individual user, you can [enable the Report Phishing add-in for yourself](#get-the-report-phishing-add-in-for-yourself).</span></span>

<span data-ttu-id="825ea-117">Si vous êtes un administrateur général ou un administrateur Exchange Online et qu’Exchange est configuré pour utiliser l’authentification OAuth, vous pouvez activer le module de signalement du hameçonnage pour [votre organisation.](#get-and-enable-the-report-phishing-add-in-for-your-organization)</span><span class="sxs-lookup"><span data-stu-id="825ea-117">If you're a global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Phishing add-in for your organization](#get-and-enable-the-report-phishing-add-in-for-your-organization).</span></span> <span data-ttu-id="825ea-118">Le rapport d’hameçonnage Add-In est désormais disponible via [le déploiement centralisé.](https://docs.microsoft.com/microsoft-365/admin/manage/centralized-deployment-of-add-ins)</span><span class="sxs-lookup"><span data-stu-id="825ea-118">The Report Phishing Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/microsoft-365/admin/manage/centralized-deployment-of-add-ins).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="825ea-119">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="825ea-119">What do you need to know before you begin?</span></span>

- <span data-ttu-id="825ea-120">Le module de signalement du hameçonnage fonctionne avec la plupart des abonnements Microsoft 365 et les produits suivants :</span><span class="sxs-lookup"><span data-stu-id="825ea-120">The Report Phishing add-in works with most Microsoft 365 subscriptions and the following products:</span></span>

  - <span data-ttu-id="825ea-121">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="825ea-121">Outlook on the web</span></span>
  - <span data-ttu-id="825ea-122">Outlook 2013 SP1 ou une édition ultérieure</span><span class="sxs-lookup"><span data-stu-id="825ea-122">Outlook 2013 SP1 or later</span></span>
  - <span data-ttu-id="825ea-123">Outlook 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="825ea-123">Outlook 2016 for Mac</span></span>
  - <span data-ttu-id="825ea-124">Outlook inclus dans les applications Microsoft 365 pour Entreprise</span><span class="sxs-lookup"><span data-stu-id="825ea-124">Outlook included with Microsoft 365 apps for Enterprise</span></span>

- <span data-ttu-id="825ea-125">Le module de signalement du hameçonnage n’est pas disponible pour les boîtes aux lettres dans les organisations Exchange locales.</span><span class="sxs-lookup"><span data-stu-id="825ea-125">The Report Phishing add-in is not available for mailboxes in on-premises Exchange organizations.</span></span>

- <span data-ttu-id="825ea-126">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="825ea-126">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="825ea-127">Pour plus d’informations, voir [Stratégies d’envoi des utilisateurs.](user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="825ea-127">For more information, see [User submissions policies](user-submission.md).</span></span>

- <span data-ttu-id="825ea-128">Votre navigateur web existant doit fonctionner avec le module de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="825ea-128">Your existing web browser should work with the Report Phishing add-in.</span></span> <span data-ttu-id="825ea-129">Toutefois, si vous remarquez que le module n’est pas disponible ou ne fonctionne pas comme prévu, essayez un autre navigateur.</span><span class="sxs-lookup"><span data-stu-id="825ea-129">But, if you notice the add-in is not available or not working as expected, try a different browser.</span></span>

- <span data-ttu-id="825ea-130">Pour les installation organisationnelles, l’organisation doit être configurée pour utiliser l’authentification OAuth.</span><span class="sxs-lookup"><span data-stu-id="825ea-130">For organizational installs, the organization needs to be configured to use OAuth authentication.</span></span> <span data-ttu-id="825ea-131">Pour plus d’informations, [voir Determine if Centralized Deployment of add-ins works for your organization](../../admin/manage/centralized-deployment-of-add-ins.md).</span><span class="sxs-lookup"><span data-stu-id="825ea-131">For more information, see [Determine if Centralized Deployment of add-ins works for your organization](../../admin/manage/centralized-deployment-of-add-ins.md).</span></span>

- <span data-ttu-id="825ea-132">Les administrateurs doivent être membres du groupe de rôles Administrateurs globaux.</span><span class="sxs-lookup"><span data-stu-id="825ea-132">Admins need to be a member of the Global admins role group.</span></span> <span data-ttu-id="825ea-133">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="825ea-133">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="get-the-report-phishing-add-in-for-yourself"></a><span data-ttu-id="825ea-134">Obtenir le module de signalement du hameçonnage par vous-même</span><span class="sxs-lookup"><span data-stu-id="825ea-134">Get the Report Phishing add-in for yourself</span></span>

1. <span data-ttu-id="825ea-135">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Phishing add-in.</span><span class="sxs-lookup"><span data-stu-id="825ea-135">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Phishing add-in.</span></span>

2. <span data-ttu-id="825ea-136">Cliquez **sur GET IT NOW**.</span><span class="sxs-lookup"><span data-stu-id="825ea-136">Click **GET IT NOW**.</span></span>

3. <span data-ttu-id="825ea-137">Dans la boîte de dialogue qui s’affiche, examinez les conditions d’utilisation et la politique de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="825ea-137">In the dialog that appears, review the terms of use and privacy policy, and then click **Continue**.</span></span>

4. <span data-ttu-id="825ea-138">Connectez-vous à l’aide de votre compte scolaire ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour un usage personnel).</span><span class="sxs-lookup"><span data-stu-id="825ea-138">Sign in using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>

<span data-ttu-id="825ea-139">Une fois que le module est installé et activé, les icônes suivantes s’offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="825ea-139">After the add-in is installed and enabled, you'll see the following icons:</span></span>

- <span data-ttu-id="825ea-140">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="825ea-140">In Outlook, the icon looks like this:</span></span>

  ![Icône Signaler le hameçonnage d’un add-in pour Outlook](../../media/Outlook-ReportPhishing.png)

- <span data-ttu-id="825ea-142">Dans Outlook sur le web, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="825ea-142">In Outlook on the web, the icon looks like this:</span></span>

  ![Icône de l’application De hameçonnage de rapport Outlook sur le web](../../media/OWA-ReportPhishing.png)

## <a name="get-and-enable-the-report-phishing-add-in-for-your-organization"></a><span data-ttu-id="825ea-144">Obtenir et activer le module de signalement du hameçonnage pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="825ea-144">Get and enable the Report Phishing add-in for your organization</span></span>

> [!NOTE]
> <span data-ttu-id="825ea-145">L’apparition du module dans votre organisation peut prendre jusqu’à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="825ea-145">It could take up to 12 hours for the add-in to appear in your organization.</span></span>

1. <span data-ttu-id="825ea-146">Dans le Centre d’administration Microsoft 365, consultez la page **Paramètres,** Applications intégrées & Les applications et les applications à l’adresse , puis cliquez sur Déployer <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> un **application.**</span><span class="sxs-lookup"><span data-stu-id="825ea-146">In the Microsoft 365 admin center, go to the **Settings, integrated Apps & Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>, and then click **Deploy Add-In**.</span></span>

   ![Page Services et modules dans le Centre d’administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

2. <span data-ttu-id="825ea-148">Dans le **volant Déployer un** nouveau module complémentaire qui s’affiche, examinez les informations, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="825ea-148">In the **Deploy a new add-in** flyout that appears, review the information, and then click **Next**.</span></span>

3. <span data-ttu-id="825ea-149">Sur la page suivante, cliquez sur **Choisir dans le Store.**</span><span class="sxs-lookup"><span data-stu-id="825ea-149">On the next page, click **Choose from the Store**.</span></span>

   ![Déployer une nouvelle page de modules](../../media/NewAddInScreen2.png)

4. <span data-ttu-id="825ea-151">Dans la page Sélectionner **un add-in** qui s’affiche, cliquez dans  la zone De recherche, entrez **Hameçonnage** de rapport, puis cliquez sur Icône  ![ ](../../media/search-icon.png) Recherche.</span><span class="sxs-lookup"><span data-stu-id="825ea-151">In the **Select add-in** page that appears, click in the **Search** box, enter **Report Phishing**, and then click **Search** ![Search icon](../../media/search-icon.png).</span></span> <span data-ttu-id="825ea-152">Dans la liste des résultats, recherchez **l’hameçonnage** de rapport, puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="825ea-152">In the list of results, find **Report Phishing** and then click **Add**.</span></span>

5. <span data-ttu-id="825ea-153">Dans la boîte de dialogue qui s’affiche, examinez les informations de licence et de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="825ea-153">In the dialog that appears, review the licensing and privacy information, and then click **Continue**.</span></span>

6. <span data-ttu-id="825ea-154">Dans la page **Configurer le add-in** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="825ea-154">In the **Configure add-in** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="825ea-155">**Utilisateurs affectés**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="825ea-155">**Assigned users**: Select one of the following values:</span></span>

     - <span data-ttu-id="825ea-156">**Tout le monde** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="825ea-156">**Everyone** (default)</span></span>
     - <span data-ttu-id="825ea-157">**Utilisateurs/groupes spécifiques**</span><span class="sxs-lookup"><span data-stu-id="825ea-157">**Specific users / groups**</span></span>
     - <span data-ttu-id="825ea-158">**Juste moi**</span><span class="sxs-lookup"><span data-stu-id="825ea-158">**Just me**</span></span>

   - <span data-ttu-id="825ea-159">**Méthode de déploiement**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="825ea-159">**Deployment method**: Select one of the following values:</span></span>

     - <span data-ttu-id="825ea-160">**Fixe (par défaut)**: le add-in est automatiquement déployé pour les utilisateurs spécifiés et ils ne peuvent pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="825ea-160">**Fixed (Default)**: The add-in is automatically deployed to the specified users and they can't remove it.</span></span>
     - <span data-ttu-id="825ea-161">**Disponible**: les utilisateurs peuvent installer le add-in sur **home** \> **get add-ins** \> **admin-managed**.</span><span class="sxs-lookup"><span data-stu-id="825ea-161">**Available**: Users can install the add-in at **Home** \> **Get add-ins** \> **Admin-managed**.</span></span>
     - <span data-ttu-id="825ea-162">**Facultatif**: le add-in est automatiquement déployé pour les utilisateurs spécifiés, mais ils peuvent choisir de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="825ea-162">**Optional**: The add-in is automatically deployed to the specified users, but they can choose to remove it.</span></span>

   <span data-ttu-id="825ea-163">Lorsque vous avez terminé, cliquez sur **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="825ea-163">When you're finished, click **Deploy**.</span></span>

7. <span data-ttu-id="825ea-164">Dans la page **Déployer** le hameçonnage de rapport qui s’affiche, vous verrez un rapport d’avancement suivi d’une confirmation du déploiement du module.</span><span class="sxs-lookup"><span data-stu-id="825ea-164">In the **Deploy Report Phishing** page that appears, you'll see a progress report followed by a confirmation that the add-in was deployed.</span></span> <span data-ttu-id="825ea-165">Après avoir lu les informations, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="825ea-165">After you read the information, click **Next**.</span></span>

8. <span data-ttu-id="825ea-166">Dans la page **Annoncer le add-in** qui s’affiche, examinez les informations, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="825ea-166">On the **Announce add-in** page that appears, review the information, and then click **Close**.</span></span>

## <a name="learn-how-to-use-the-report-phishing-add-in"></a><span data-ttu-id="825ea-167">Découvrez comment utiliser le module de signalement du hameçonnage</span><span class="sxs-lookup"><span data-stu-id="825ea-167">Learn how to use the Report Phishing add-in</span></span>

<span data-ttu-id="825ea-168">Les personnes à qui le add-in est affecté voient les icônes suivantes :</span><span class="sxs-lookup"><span data-stu-id="825ea-168">People who have the add-in assigned to them will see the following icons:</span></span>

- <span data-ttu-id="825ea-169">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="825ea-169">In Outlook, the icon looks like this:</span></span>

  ![Icône Signaler le hameçonnage d’un add-in pour Outlook](../../media/Outlook-ReportPhishing.png)

- <span data-ttu-id="825ea-171">Dans Outlook sur le web, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="825ea-171">In Outlook on the web, the icon looks like this:</span></span>

  ![Icône de l’application de hameçonnage de rapport Outlook sur le web](../../media/OWA-ReportPhishing.png)

## <a name="review-or-edit-settings-for-the-report-phishing-add-in"></a><span data-ttu-id="825ea-173">Examiner ou modifier les paramètres du module de signalement du hameçonnage</span><span class="sxs-lookup"><span data-stu-id="825ea-173">Review or edit settings for the Report Phishing add-in</span></span>

1. <span data-ttu-id="825ea-174">In the Microsoft 365 admin center, go to the **Services & add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns> .</span><span class="sxs-lookup"><span data-stu-id="825ea-174">In the Microsoft 365 admin center, go to the **Services & add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns>.</span></span>

2. <span data-ttu-id="825ea-175">Recherchez et sélectionnez **le** module de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="825ea-175">Find and select the **Report Phishing** add-in.</span></span>

3. <span data-ttu-id="825ea-176">Dans le volant **Modifier le hameçonnage** du rapport qui s’affiche, examinez et modifiez les paramètres selon les cas de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="825ea-176">In the **Edit Report Phishing** flyout that appears, review, and edit settings as appropriate for your organization.</span></span> <span data-ttu-id="825ea-177">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="825ea-177">When you're finished, click **Save**.</span></span>

## <a name="view-and-review-reported-messages"></a><span data-ttu-id="825ea-178">Afficher et examiner les messages signalés</span><span class="sxs-lookup"><span data-stu-id="825ea-178">View and review reported messages</span></span>

<span data-ttu-id="825ea-179">Pour passer en revue les messages que les utilisateurs signalent à Microsoft, vous avez les options ci-après :</span><span class="sxs-lookup"><span data-stu-id="825ea-179">To review messages that users report to Microsoft, you have these options:</span></span>

- <span data-ttu-id="825ea-180">Utilisez le portail Soumissions d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="825ea-180">Use the Admin Submissions portal.</span></span> <span data-ttu-id="825ea-181">Pour plus d’informations, voir [Afficher les soumissions d’utilisateurs à Microsoft.](admin-submission.md#view-user-submissions-to-microsoft)</span><span class="sxs-lookup"><span data-stu-id="825ea-181">For more information, see [View user submissions to Microsoft](admin-submission.md#view-user-submissions-to-microsoft).</span></span>

- <span data-ttu-id="825ea-182">Créez une règle de flux de messagerie (également appelée règle de transport) pour envoyer des copies des messages signalés.</span><span class="sxs-lookup"><span data-stu-id="825ea-182">Create a mail flow rule (also known as a transport rule) to send copies of reported messages.</span></span> <span data-ttu-id="825ea-183">Pour obtenir des instructions, voir Utiliser des règles de flux de messagerie pour voir ce [que vos utilisateurs rapportent à Microsoft.](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="825ea-183">For instructions, see [Use mail flow rules to see what your users are reporting to Microsoft](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md).</span></span>