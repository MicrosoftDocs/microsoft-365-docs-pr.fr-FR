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
ms.openlocfilehash: 8949322b0b691d59e59e5f7b80d2b9650e4115d5
ms.sourcegitcommit: c70067b4ef9c6f8f04aca68c35bb5141857c4e4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "53029908"
---
# <a name="enable-the-report-message-or-the-report-phishing-add-ins"></a><span data-ttu-id="993d3-103">Activer le message de rapport ou les modules de signalement du hameçonnage</span><span class="sxs-lookup"><span data-stu-id="993d3-103">Enable the Report Message or the Report Phishing add-ins</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="993d3-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="993d3-104">**Applies to**</span></span>
- [<span data-ttu-id="993d3-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="993d3-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="993d3-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="993d3-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="993d3-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="993d3-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

> [!NOTE]
> <span data-ttu-id="993d3-108">Si vous êtes un administrateur d’une organisation Microsoft 365 avec des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail Soumissions dans le portail Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="993d3-108">If you're an admin in a Microsoft 365 organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Microsoft 365 Defender portal.</span></span> <span data-ttu-id="993d3-109">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="993d3-109">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

<span data-ttu-id="993d3-110">Les add-ins Signaler le message et Signaler le hameçonnage pour Outlook et Outlook sur le web (anciennement Outlook Web App) permettent aux utilisateurs de signaler facilement les faux positifs (messages électroniques de qualité marqués comme faux) ou les faux négatifs (courrier électronique non autorisé) à Microsoft et à ses affiliés pour analyse.</span><span class="sxs-lookup"><span data-stu-id="993d3-110">The Report Message and Report Phishing add-ins for Outlook and Outlook on the web (formerly known as Outlook Web App) enable people to easily report false positives (good email marked as bad) or false negatives (bad email allowed) to Microsoft and its affiliates for analysis.</span></span>

<span data-ttu-id="993d3-111">Microsoft utilise ces soumissions pour améliorer l’efficacité des technologies de protection de la messagerie.</span><span class="sxs-lookup"><span data-stu-id="993d3-111">Microsoft uses these submissions to improve the effectiveness of email protection technologies.</span></span> <span data-ttu-id="993d3-112">Par exemple, supposons que des personnes signalent de nombreux messages à l’aide du module de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="993d3-112">For example, suppose that people are reporting many messages using the Report Phishing add-in.</span></span> <span data-ttu-id="993d3-113">Ces informations sont disponibles dans le Tableau de bord de sécurité et d’autres rapports.</span><span class="sxs-lookup"><span data-stu-id="993d3-113">This information surfaces in the Security Dashboard and other reports.</span></span> <span data-ttu-id="993d3-114">L’équipe de sécurité de votre organisation peut utiliser ces informations pour indiquer que les stratégies anti-hameçonnage peuvent avoir besoin d’être mises à jour.</span><span class="sxs-lookup"><span data-stu-id="993d3-114">Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated.</span></span>

<span data-ttu-id="993d3-115">Vous pouvez installer le module de rapport de message ou de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="993d3-115">You can install either the Report Message or Report Phishing add-in.</span></span> <span data-ttu-id="993d3-116">Si vous souhaitez que vos utilisateurs signalent à la fois le courrier indésirable et les messages de hameçonnage, déployez le add-in Signaler un message dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="993d3-116">If you want your users to report both spam and phishing messages, deploy the Report Message add-in in your organization.</span></span> <span data-ttu-id="993d3-117">Pour plus d’informations, voir Enable the Report Message add-in.</span><span class="sxs-lookup"><span data-stu-id="993d3-117">For more information, see Enable the Report Message add-in.</span></span>

<span data-ttu-id="993d3-118">Le add-in Report Message offre la possibilité de signaler les messages de courrier indésirable et de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="993d3-118">The Report Message add-in provides the option to report both spam and phishing messages.</span></span> <span data-ttu-id="993d3-119">Les administrateurs peuvent activer le add-in Message de rapport pour l’organisation, et les utilisateurs individuels peuvent l’installer eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="993d3-119">Admins can enable the Report Message add-in for the organization, and individual users can install it for themselves.</span></span>

<span data-ttu-id="993d3-120">Le module de signalement du hameçonnage offre la possibilité de signaler uniquement les messages de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="993d3-120">The Report Phishing add-in provides the option to report only phishing messages.</span></span> <span data-ttu-id="993d3-121">Les administrateurs peuvent activer le module de signalement du hameçonnage pour l’organisation, et les utilisateurs individuels peuvent l’installer eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="993d3-121">Admins can enable the Report Phishing add-in for the organization, and individual users can install it for themselves.</span></span>

<span data-ttu-id="993d3-122">Si vous êtes un utilisateur individuel, vous pouvez activer les deux modules pour vous-même.</span><span class="sxs-lookup"><span data-stu-id="993d3-122">If you're an individual user, you can enable both the add-ins for yourself.</span></span>

<span data-ttu-id="993d3-123">Si vous êtes un administrateur général ou un administrateur Exchange Online et qu’Exchange est configuré pour utiliser l’authentification OAuth, vous pouvez activer le add-in Message de rapport et le module de signalement du hameçonnage pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="993d3-123">If you're a global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can enable the Report Message add-in and the Report Phishing add-in for your organization.</span></span> <span data-ttu-id="993d3-124">Les deux modules sont désormais disponibles via [le déploiement centralisé.](../../admin/manage/centralized-deployment-of-add-ins.md)</span><span class="sxs-lookup"><span data-stu-id="993d3-124">Both add-ins are now available through [Centralized Deployment](../../admin/manage/centralized-deployment-of-add-ins.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="993d3-125">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="993d3-125">What do you need to know before you begin?</span></span>

- <span data-ttu-id="993d3-126">Le add-in Report Message et le add-in Report Phishing fonctionnent avec la plupart des abonnements Microsoft 365 et les produits suivants :</span><span class="sxs-lookup"><span data-stu-id="993d3-126">Both the Report Message add-in and the Report Phishing add-in works with most Microsoft 365 subscriptions and the following products:</span></span>
  - <span data-ttu-id="993d3-127">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="993d3-127">Outlook on the web</span></span>
  - <span data-ttu-id="993d3-128">Outlook 2013 SP1 ou une édition ultérieure</span><span class="sxs-lookup"><span data-stu-id="993d3-128">Outlook 2013 SP1 or later</span></span>
  - <span data-ttu-id="993d3-129">Outlook 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="993d3-129">Outlook 2016 for Mac</span></span>
  - <span data-ttu-id="993d3-130">Outlook inclus dans les applications Microsoft 365 pour Entreprise</span><span class="sxs-lookup"><span data-stu-id="993d3-130">Outlook included with Microsoft 365 apps for Enterprise</span></span>
  - <span data-ttu-id="993d3-131">Application Outlook pour iOS et Android</span><span class="sxs-lookup"><span data-stu-id="993d3-131">Outlook app for iOS and Android</span></span>

- <span data-ttu-id="993d3-132">Les deux modules ne sont pas disponibles pour les boîtes aux lettres partagées ou les boîtes aux lettres dans les organisations Exchange locales.</span><span class="sxs-lookup"><span data-stu-id="993d3-132">Both add-ins are not available for shared mailboxes or mailboxes in on-premises Exchange organizations.</span></span>

- <span data-ttu-id="993d3-133">Votre navigateur web existant doit fonctionner à la fois avec les modules de rapport de message et de signalement du hameçonnage. Toutefois, si vous remarquez que le module n’est pas disponible ou ne fonctionne pas comme prévu, essayez un autre navigateur.</span><span class="sxs-lookup"><span data-stu-id="993d3-133">Your existing web browser should work with both the Report Message and Report Phishing add-ins. But, if you notice the add-in is not available or not working as expected, try a different browser.</span></span>

- <span data-ttu-id="993d3-134">Pour les installation organisationnelles, l’organisation doit être configurée pour utiliser l’authentification OAuth.</span><span class="sxs-lookup"><span data-stu-id="993d3-134">For organizational installs, the organization needs to be configured to use OAuth authentication.</span></span> <span data-ttu-id="993d3-135">Pour plus d’informations, [voir Determine if Centralized Deployment of add-ins works for your organization](../../admin/manage/centralized-deployment-of-add-ins.md).</span><span class="sxs-lookup"><span data-stu-id="993d3-135">For more information, see [Determine if Centralized Deployment of add-ins works for your organization](../../admin/manage/centralized-deployment-of-add-ins.md).</span></span>

- <span data-ttu-id="993d3-136">Les administrateurs doivent être membres du groupe de rôles Administrateurs globaux.</span><span class="sxs-lookup"><span data-stu-id="993d3-136">Admins need to be a member of the Global admins role group.</span></span> <span data-ttu-id="993d3-137">Pour plus d’informations, [voir Autorisations dans le portail Microsoft 365 Defender.](permissions-microsoft-365-security-center.md)</span><span class="sxs-lookup"><span data-stu-id="993d3-137">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-microsoft-365-security-center.md).</span></span>

- <span data-ttu-id="993d3-138">Pour plus d’informations sur la façon de signaler un message à l’aide de la fonctionnalité Signaler un message, voir Signaler les faux positifs et les [faux négatifs dans Outlook.](report-false-positives-and-false-negatives.md)</span><span class="sxs-lookup"><span data-stu-id="993d3-138">For more information on how to report a message using the Report Message feature, see [Report false positives and false negatives in Outlook](report-false-positives-and-false-negatives.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="993d3-139">Nous vous déconseillons d’utiliser l’expérience de rapport intégrée dans Outlook, car elle ne peut pas utiliser la stratégie [de soumission d’utilisateur.](./user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="993d3-139">We don't recommend the built-in reporting experience in Outlook because it can't use the [user submission policy](./user-submission.md).</span></span> <span data-ttu-id="993d3-140">Nous vous recommandons plutôt d’utiliser le add-in Report Message ou report Phishing.</span><span class="sxs-lookup"><span data-stu-id="993d3-140">We recommend using the Report Message add-in or the Report Phishing add-in instead.</span></span>

## <a name="get-the-report-message-add-in"></a><span data-ttu-id="993d3-141">Obtenir le add-in Message de rapport</span><span class="sxs-lookup"><span data-stu-id="993d3-141">Get the Report Message add-in</span></span>

### <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="993d3-142">Obtenir le add-in Message de rapport pour vous-même</span><span class="sxs-lookup"><span data-stu-id="993d3-142">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="993d3-143">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Message add-in.</span><span class="sxs-lookup"><span data-stu-id="993d3-143">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Message add-in.</span></span> <span data-ttu-id="993d3-144">To go directly to the Report Message add-in, go to <https://appsource.microsoft.com/product/office/wa104381180> .</span><span class="sxs-lookup"><span data-stu-id="993d3-144">To go directly to the Report Message add-in, go to <https://appsource.microsoft.com/product/office/wa104381180>.</span></span>

2. <span data-ttu-id="993d3-145">Cliquez **sur GET IT NOW**.</span><span class="sxs-lookup"><span data-stu-id="993d3-145">Click **GET IT NOW**.</span></span>

   ![Message de rapport : l’obtenir maintenant](../../media/ReportMessageGETITNOW.png)

3. <span data-ttu-id="993d3-147">Dans la boîte de dialogue qui s’affiche, examinez les conditions d’utilisation et la politique de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="993d3-147">In the dialog that appears, review the terms of use and privacy policy, and then click **Continue**.</span></span>

4. <span data-ttu-id="993d3-148">Connectez-vous à l’aide de votre compte scolaire ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour un usage personnel).</span><span class="sxs-lookup"><span data-stu-id="993d3-148">Sign in using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>

<span data-ttu-id="993d3-149">Une fois que le module est installé et activé, les icônes suivantes s’offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="993d3-149">After the add-in is installed and enabled, you'll see the following icons:</span></span>

- <span data-ttu-id="993d3-150">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="993d3-150">In Outlook, the icon looks like this:</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="993d3-151">![Icône signaler le add-in Message pour Outlook](../../media/OutlookReportMessageIcon.png)</span><span class="sxs-lookup"><span data-stu-id="993d3-151">![Report Message add-in icon for Outlook](../../media/OutlookReportMessageIcon.png)</span></span>

- <span data-ttu-id="993d3-152">Dans Outlook sur le web, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="993d3-152">In Outlook on the web, the icon looks like this:</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="993d3-153">![Icône du add-in Message de rapport Outlook sur le web](../../media/owa-report-message-icon.png)</span><span class="sxs-lookup"><span data-stu-id="993d3-153">![Outlook on the web Report Message add-in icon](../../media/owa-report-message-icon.png)</span></span>

### <a name="get-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="993d3-154">Obtenir le add-in Message de rapport pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="993d3-154">Get the Report Message add-in for your organization</span></span>

> [!NOTE]
> <span data-ttu-id="993d3-155">L’apparition du module dans votre organisation peut prendre jusqu’à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="993d3-155">It could take up to 12 hours for the add-in to appear in your organization.</span></span>

1. <span data-ttu-id="993d3-156">In the Microsoft 365 admin center, go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> .</span><span class="sxs-lookup"><span data-stu-id="993d3-156">In the Microsoft 365 admin center, go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>.</span></span> <span data-ttu-id="993d3-157">Si la **page** Des applications intégrées aux **paramètres** n’est pas consultez, rendez-vous sur le lien Applications \>  \> **intégrées paramètres** en haut de la page **Applications intégrées.**</span><span class="sxs-lookup"><span data-stu-id="993d3-157">If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

2. <span data-ttu-id="993d3-158">Sélectionnez **Déployer le add-in** en haut de la page, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="993d3-158">Select **Deploy Add-in** at the top of the page, and then select **Next**.</span></span>

   ![Page Services et modules dans le Centre d’administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

3. <span data-ttu-id="993d3-160">Dans le **volant Déployer un** nouveau module complémentaire qui s’affiche, examinez les informations, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="993d3-160">In the **Deploy a new add-in** flyout that appears, review the information, and then click **Next**.</span></span>

4. <span data-ttu-id="993d3-161">Sur la page suivante, cliquez sur **Choisir dans le Store.**</span><span class="sxs-lookup"><span data-stu-id="993d3-161">On the next page, click **Choose from the Store**.</span></span>

   ![Déployer une nouvelle page de modules](../../media/NewAddInScreen2.png)

5. <span data-ttu-id="993d3-163">Dans la page **Sélectionner un add-in** qui s’affiche, cliquez dans la zone De recherche, entrez Message de rapport, puis cliquez sur **Icône**   ![ ](../../media/search-icon.png) Rechercher.</span><span class="sxs-lookup"><span data-stu-id="993d3-163">In the **Select add-in** page that appears, click in the **Search** box, enter **Report Message**, and then click **Search** ![Search icon](../../media/search-icon.png).</span></span> <span data-ttu-id="993d3-164">Dans la liste des résultats, recherchez Message de **rapport,** puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="993d3-164">In the list of results, find **Report Message** and then click **Add**.</span></span>

   ![Sélectionner les résultats de la recherche de add-in](../../media/NewAddInScreen3.png)

6. <span data-ttu-id="993d3-166">Dans la boîte de dialogue qui s’affiche, examinez les informations de licence et de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="993d3-166">In the dialog that appears, review the licensing and privacy information, and then click **Continue**.</span></span>

7. <span data-ttu-id="993d3-167">Dans la page **Configurer le module de** configuration qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="993d3-167">In the **Configure add-in** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="993d3-168">**Utilisateurs affectés**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="993d3-168">**Assigned users**: Select one of the following values:</span></span>
     - <span data-ttu-id="993d3-169">**Tout le monde** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="993d3-169">**Everyone** (default)</span></span>
     - <span data-ttu-id="993d3-170">**Utilisateurs/groupes spécifiques**</span><span class="sxs-lookup"><span data-stu-id="993d3-170">**Specific users / groups**</span></span>
     - <span data-ttu-id="993d3-171">**Juste moi**</span><span class="sxs-lookup"><span data-stu-id="993d3-171">**Just me**</span></span>

   - <span data-ttu-id="993d3-172">**Méthode de déploiement**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="993d3-172">**Deployment method**: Select one of the following values:</span></span>
     - <span data-ttu-id="993d3-173">**Fixe (par défaut)**: le add-in est automatiquement déployé sur les utilisateurs spécifiés et ils ne peuvent pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="993d3-173">**Fixed (Default)**: The add-in is automatically deployed to the specified users and they can't remove it.</span></span>
     - <span data-ttu-id="993d3-174">**Disponible**: les utilisateurs peuvent installer le add-in sur **home** \> **get add-ins** \> **admin-managed**.</span><span class="sxs-lookup"><span data-stu-id="993d3-174">**Available**: Users can install the add-in at **Home** \> **Get add-ins** \> **Admin-managed**.</span></span>
     - <span data-ttu-id="993d3-175">**Facultatif**: le add-in est automatiquement déployé pour les utilisateurs spécifiés, mais ils peuvent choisir de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="993d3-175">**Optional**: The add-in is automatically deployed to the specified users, but they can choose to remove it.</span></span>

   ![Configurer la page de l’ajout](../../media/configure-add-in.png)

   <span data-ttu-id="993d3-177">Lorsque vous avez terminé, cliquez sur **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="993d3-177">When you're finished, click **Deploy**.</span></span>

8. <span data-ttu-id="993d3-178">Dans la page Déployer le **message** de rapport qui s’affiche, vous verrez un rapport d’avancement suivi d’une confirmation du déploiement du module.</span><span class="sxs-lookup"><span data-stu-id="993d3-178">In the **Deploy Report Message** page that appears, you'll see a progress report followed by a confirmation that the add-in was deployed.</span></span> <span data-ttu-id="993d3-179">Après avoir lu les informations, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="993d3-179">After you read the information, click **Next**.</span></span>

   ![Page Déployer le message de rapport](../../media/deploy-report-message-page.png)

9. <span data-ttu-id="993d3-181">Dans la page **Annoncer le add-in** qui s’affiche, examinez les informations, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="993d3-181">On the **Announce add-in** page that appears, review the information, and then click **Close**.</span></span>

   ![Page d’annonce du add-in](../../media/announce-add-in-page.png)

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="993d3-183">Passer en revue ou modifier les paramètres du add-in Message de rapport</span><span class="sxs-lookup"><span data-stu-id="993d3-183">Review or edit settings for the Report Message add-in</span></span>

1. <span data-ttu-id="993d3-184">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> .</span><span class="sxs-lookup"><span data-stu-id="993d3-184">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>.</span></span> <span data-ttu-id="993d3-185">Si la **page** Des applications intégrées aux **paramètres** n’est pas consultez, rendez-vous sur le lien Applications \>  \> **intégrées paramètres** en haut de la page **Applications intégrées.**</span><span class="sxs-lookup"><span data-stu-id="993d3-185">If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

   ![Page Services et Add-Ins dans le nouveau Centre d’administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

2. <span data-ttu-id="993d3-187">Recherchez et sélectionnez le add-in **Message** de rapport.</span><span class="sxs-lookup"><span data-stu-id="993d3-187">Find and select the **Report Message** add-in.</span></span>

3. <span data-ttu-id="993d3-188">Dans le **volant Modifier le message** de rapport qui s’affiche, examinez et modifiez les paramètres selon le cas pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="993d3-188">In the **Edit Report Message** flyout that appears, review and edit settings as appropriate for your organization.</span></span> <span data-ttu-id="993d3-189">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="993d3-189">When you're finished, click **Save**.</span></span>

   ![Paramètres du add-in Message de rapport](../../media/EditReportMessageAddIn.png)

## <a name="get-the-report-phishing-add-in"></a><span data-ttu-id="993d3-191">Obtenir le module de signalement du hameçonnage</span><span class="sxs-lookup"><span data-stu-id="993d3-191">Get the Report Phishing add-in</span></span>

### <a name="get-the-report-phishing-add-in-for-yourself"></a><span data-ttu-id="993d3-192">Obtenir le module de signalement du hameçonnage par vous-même</span><span class="sxs-lookup"><span data-stu-id="993d3-192">Get the Report Phishing add-in for yourself</span></span>

1. <span data-ttu-id="993d3-193">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Phishing add-in.</span><span class="sxs-lookup"><span data-stu-id="993d3-193">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Phishing add-in.</span></span>

2. <span data-ttu-id="993d3-194">Cliquez **sur GET IT NOW**.</span><span class="sxs-lookup"><span data-stu-id="993d3-194">Click **GET IT NOW**.</span></span>

3. <span data-ttu-id="993d3-195">Dans la boîte de dialogue qui s’affiche, examinez les conditions d’utilisation et la politique de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="993d3-195">In the dialog that appears, review the terms of use and privacy policy, and then click **Continue**.</span></span>

4. <span data-ttu-id="993d3-196">Connectez-vous à l’aide de votre compte scolaire ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour un usage personnel).</span><span class="sxs-lookup"><span data-stu-id="993d3-196">Sign in using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>

<span data-ttu-id="993d3-197">Une fois que le module est installé et activé, les icônes suivantes s’offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="993d3-197">After the add-in is installed and enabled, you'll see the following icons:</span></span>

- <span data-ttu-id="993d3-198">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="993d3-198">In Outlook, the icon looks like this:</span></span>

  ![Icône Signaler le hameçonnage d’un add-in pour Outlook](../../media/Outlook-ReportPhishing.png)

- <span data-ttu-id="993d3-200">Dans Outlook sur le web, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="993d3-200">In Outlook on the web, the icon looks like this:</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="993d3-201">![Icône de l’application De hameçonnage de rapport Outlook sur le web](../../media/OWA-ReportPhishing.png)</span><span class="sxs-lookup"><span data-stu-id="993d3-201">![Outlook on the web Report Phishing add-in icon](../../media/OWA-ReportPhishing.png)</span></span>

### <a name="get-the-report-phishing-add-in-for-your-organization"></a><span data-ttu-id="993d3-202">Obtenir le module de signalement du hameçonnage pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="993d3-202">Get the Report Phishing add-in for your organization</span></span>

> [!NOTE]
> <span data-ttu-id="993d3-203">L’apparition du module dans votre organisation peut prendre jusqu’à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="993d3-203">It could take up to 12 hours for the add-in to appear in your organization.</span></span>

1. <span data-ttu-id="993d3-204">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> .</span><span class="sxs-lookup"><span data-stu-id="993d3-204">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>.</span></span> <span data-ttu-id="993d3-205">Si la **page** Des applications intégrées aux **paramètres** n’est pas consultez, rendez-vous sur le lien Applications \>  \> **intégrées paramètres** en haut de la page **Applications intégrées.**</span><span class="sxs-lookup"><span data-stu-id="993d3-205">If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

2. <span data-ttu-id="993d3-206">Sélectionnez **Déployer le add-in** en haut de la page, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="993d3-206">Select **Deploy Add-in** at the top of the page, and then select **Next**.</span></span>

   ![Page Services et modules dans le Centre d’administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

3. <span data-ttu-id="993d3-208">Dans le **volant Déployer un** nouveau module complémentaire qui s’affiche, examinez les informations, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="993d3-208">In the **Deploy a new add-in** flyout that appears, review the information, and then click **Next**.</span></span>

4. <span data-ttu-id="993d3-209">Sur la page suivante, cliquez sur **Choisir dans le Store.**</span><span class="sxs-lookup"><span data-stu-id="993d3-209">On the next page, click **Choose from the Store**.</span></span>

   ![Déployer une nouvelle page de modules](../../media/NewAddInScreen2.png)

5. <span data-ttu-id="993d3-211">Dans la page Sélectionner **un add-in** qui s’affiche, cliquez dans  la zone De recherche, entrez **Hameçonnage** de rapport, puis cliquez sur Icône  ![ ](../../media/search-icon.png) Recherche.</span><span class="sxs-lookup"><span data-stu-id="993d3-211">In the **Select add-in** page that appears, click in the **Search** box, enter **Report Phishing**, and then click **Search** ![Search icon](../../media/search-icon.png).</span></span> <span data-ttu-id="993d3-212">Dans la liste des résultats, recherchez **l’hameçonnage** de rapport, puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="993d3-212">In the list of results, find **Report Phishing** and then click **Add**.</span></span>

6. <span data-ttu-id="993d3-213">Dans la boîte de dialogue qui s’affiche, examinez les informations de licence et de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="993d3-213">In the dialog that appears, review the licensing and privacy information, and then click **Continue**.</span></span>

7. <span data-ttu-id="993d3-214">Dans la page **Configurer le module de** configuration qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="993d3-214">In the **Configure add-in** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="993d3-215">**Utilisateurs affectés**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="993d3-215">**Assigned users**: Select one of the following values:</span></span>
     - <span data-ttu-id="993d3-216">**Tout le monde** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="993d3-216">**Everyone** (default)</span></span>
     - <span data-ttu-id="993d3-217">**Utilisateurs/groupes spécifiques**</span><span class="sxs-lookup"><span data-stu-id="993d3-217">**Specific users / groups**</span></span>
     - <span data-ttu-id="993d3-218">**Juste moi**</span><span class="sxs-lookup"><span data-stu-id="993d3-218">**Just me**</span></span>

   - <span data-ttu-id="993d3-219">**Méthode de déploiement**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="993d3-219">**Deployment method**: Select one of the following values:</span></span>
     - <span data-ttu-id="993d3-220">**Fixe (par défaut)**: le add-in est automatiquement déployé sur les utilisateurs spécifiés et ils ne peuvent pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="993d3-220">**Fixed (Default)**: The add-in is automatically deployed to the specified users and they can't remove it.</span></span>
     - <span data-ttu-id="993d3-221">**Disponible**: les utilisateurs peuvent installer le add-in sur **home** \> **get add-ins** \> **admin-managed**.</span><span class="sxs-lookup"><span data-stu-id="993d3-221">**Available**: Users can install the add-in at **Home** \> **Get add-ins** \> **Admin-managed**.</span></span>
     - <span data-ttu-id="993d3-222">**Facultatif**: le add-in est automatiquement déployé pour les utilisateurs spécifiés, mais ils peuvent choisir de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="993d3-222">**Optional**: The add-in is automatically deployed to the specified users, but they can choose to remove it.</span></span>

   <span data-ttu-id="993d3-223">Lorsque vous avez terminé, cliquez sur **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="993d3-223">When you're finished, click **Deploy**.</span></span>

8. <span data-ttu-id="993d3-224">Dans la page **Déployer** le hameçonnage de rapport qui s’affiche, vous verrez un rapport d’avancement suivi d’une confirmation du déploiement du module.</span><span class="sxs-lookup"><span data-stu-id="993d3-224">In the **Deploy Report Phishing** page that appears, you'll see a progress report followed by a confirmation that the add-in was deployed.</span></span> <span data-ttu-id="993d3-225">Après avoir lu les informations, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="993d3-225">After you read the information, click **Next**.</span></span>

9. <span data-ttu-id="993d3-226">Dans la page **Annoncer le add-in** qui s’affiche, examinez les informations, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="993d3-226">On the **Announce add-in** page that appears, review the information, and then click **Close**.</span></span>

## <a name="review-or-edit-settings-for-the-report-phishing-add-in"></a><span data-ttu-id="993d3-227">Examiner ou modifier les paramètres du module de signalement du hameçonnage</span><span class="sxs-lookup"><span data-stu-id="993d3-227">Review or edit settings for the Report Phishing add-in</span></span>

1. <span data-ttu-id="993d3-228">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> .</span><span class="sxs-lookup"><span data-stu-id="993d3-228">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>.</span></span> <span data-ttu-id="993d3-229">Si la **page** Des applications intégrées aux **paramètres** n’est pas consultez, rendez-vous sur le lien Applications \>  \> **intégrées paramètres** en haut de la page **Applications intégrées.**</span><span class="sxs-lookup"><span data-stu-id="993d3-229">If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

2. <span data-ttu-id="993d3-230">Recherchez et sélectionnez **le** module de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="993d3-230">Find and select the **Report Phishing** add-in.</span></span>

3. <span data-ttu-id="993d3-231">Dans le volant **Modifier le hameçonnage** du rapport qui s’affiche, examinez et modifiez les paramètres selon les cas de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="993d3-231">In the **Edit Report Phishing** flyout that appears, review, and edit settings as appropriate for your organization.</span></span> <span data-ttu-id="993d3-232">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="993d3-232">When you're finished, click **Save**.</span></span>
