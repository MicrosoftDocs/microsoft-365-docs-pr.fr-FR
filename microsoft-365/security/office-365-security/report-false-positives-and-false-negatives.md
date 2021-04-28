---
title: Signaler les faux positifs et les faux négatifs dans Outlook
f1.keywords:
- NOCSH
ms.author: dansimp
author: dansimp
manager: dansimp
audience: Admin
ms.topic: how-to
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: Découvrez comment signaler les faux positifs et les faux négatifs dans Outlook et activer les modules de signalement des messages et du signalement du hameçonnage.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 38f940a98581c5678eef0c57c95f6349cdb41de8
ms.sourcegitcommit: ddb1bf56bcba4f03c803f79492e8cd0dc41a3d7a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "52065177"
---
# <a name="report-false-positives-and-false-negatives-in-outlook"></a><span data-ttu-id="e3113-103">Signaler les faux positifs et les faux négatifs dans Outlook</span><span class="sxs-lookup"><span data-stu-id="e3113-103">Report false positives and false negatives in Outlook</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="e3113-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="e3113-104">**Applies to**</span></span>
- [<span data-ttu-id="e3113-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="e3113-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="e3113-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="e3113-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="e3113-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e3113-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

> [!NOTE]
> <span data-ttu-id="e3113-108">Si vous êtes un administrateur d'une organisation Microsoft 365 avec des boîtes aux lettres Exchange Online, nous vous recommandons d'utiliser le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="e3113-108">If you're an admin in a Microsoft 365 organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="e3113-109">Pour plus d'informations, voir Utiliser la soumission d'administrateur pour soumettre des messages suspects de courrier indésirable, d'hameçonnage, d'URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="e3113-109">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

<span data-ttu-id="e3113-110">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou locales utilisant l'authentification moderne hybride, vous pouvez envoyer des faux positifs (messages électroniques de qualité marqués comme courrier indésirable) et des faux négatifs (courrier électronique et hameçonnage autorisés) à Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="e3113-110">In Microsoft 365 organizations with mailboxes in Exchange Online or on-premises mailboxes using hybrid modern authentication, you can submit false positives (good email marked as spam) and false negatives (bad email and phish allowed) to Exchange Online Protection (EOP).</span></span>

## <a name="things-to-remember-before-you-use-the-report-message-feature"></a><span data-ttu-id="e3113-111">Éléments à retenir avant d'utiliser la fonctionnalité Signaler un message</span><span class="sxs-lookup"><span data-stu-id="e3113-111">Things to remember before you use the Report Message feature</span></span>

- <span data-ttu-id="e3113-112">Pour une meilleure expérience de soumission d'utilisateurs, utilisez le add-in Report Message ou report Phishing.</span><span class="sxs-lookup"><span data-stu-id="e3113-112">For the best user submission experience, use the Report Message add-in or the Report Phishing add-in.</span></span>

- <span data-ttu-id="e3113-113">Notez que ce add-in fonctionne pour Outlook sur toutes les plateformes , sur le web, iOS, Android et Bureau.</span><span class="sxs-lookup"><span data-stu-id="e3113-113">Note that this add-in works for Outlook in all platforms—on the web, iOS, Android, and Desktop.</span></span>

- <span data-ttu-id="e3113-114">Si vous êtes un administrateur d'une organisation ayant des boîtes aux lettres Exchange Online, utilisez le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="e3113-114">If you're an admin in an organization with Exchange Online mailboxes, use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="e3113-115">Pour plus d'informations, voir Utiliser la soumission d'administrateur pour soumettre des messages suspects de courrier indésirable, d'hameçonnage, d'URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="e3113-115">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

- <span data-ttu-id="e3113-116">Vous pouvez configurer pour envoyer des messages directement à Microsoft, une boîte aux lettres que vous spécifiez, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="e3113-116">You can configure to send messages directly to Microsoft, a mailbox you specify, or both.</span></span> <span data-ttu-id="e3113-117">Pour plus d'informations, voir [Stratégies d'envoi des utilisateurs.](user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="e3113-117">For more information, see [User submissions policies](user-submission.md).</span></span>

- <span data-ttu-id="e3113-118">Pour plus d'informations sur la notification des messages à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="e3113-118">For more information about reporting messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="use-the-report-message-feature"></a><span data-ttu-id="e3113-119">Utiliser la fonctionnalité Message de rapport</span><span class="sxs-lookup"><span data-stu-id="e3113-119">Use the Report Message feature</span></span>

### <a name="report-junk-and-phishing-messages"></a><span data-ttu-id="e3113-120">Signaler les messages de courrier indésirable et de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="e3113-120">Report junk and phishing messages</span></span>

<span data-ttu-id="e3113-121">Pour les messages dans la boîte de réception ou tout autre dossier de courrier électronique à l'exception du courrier indésirable, utilisez la méthode suivante pour signaler le courrier indésirable et les messages de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="e3113-121">For messages in the Inbox or any other email folder except Junk Email, use the following method to report spam and phishing messages:</span></span>

1. <span data-ttu-id="e3113-122">Cliquez sur les **ellipses** Autres actions dans le coin supérieur droit du message sélectionné,  cliquez sur Signaler **le message** dans le menu déroulant, puis sélectionnez Courrier indésirable ou **Hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="e3113-122">Click the **More actions** ellipses on the top-right corner of the selected message, click **Report message** from the dropdown menu, and then select **Junk** or **Phishing**.</span></span>
  
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="e3113-123">![Message de rapport - Plus d'actions](../../media/report-message-more-actions.png)</span><span class="sxs-lookup"><span data-stu-id="e3113-123">![Report Message - More actions](../../media/report-message-more-actions.png)</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="e3113-124">![Message de rapport : courrier indésirable et hameçonnage](../../media/report-message-junk-phishing.png)</span><span class="sxs-lookup"><span data-stu-id="e3113-124">![Report Message - Junk and Phishing](../../media/report-message-junk-phishing.png)</span></span>

2. <span data-ttu-id="e3113-125">Les messages sélectionnés sont envoyés à Microsoft pour analyse et :</span><span class="sxs-lookup"><span data-stu-id="e3113-125">The selected messages will be sent to Microsoft for analysis and:</span></span>

   - <span data-ttu-id="e3113-126">Déplacé vers le dossier Courrier indésirable s'il a été signalé comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="e3113-126">Moved to the Junk Email folder if it was reported as spam.</span></span>

   - <span data-ttu-id="e3113-127">Supprimé s'il a été signalé comme hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="e3113-127">Deleted if it was reported as phishing.</span></span>
   
### <a name="report-messages-that-are-not-junk"></a><span data-ttu-id="e3113-128">Signaler les messages qui ne sont pas indésirables</span><span class="sxs-lookup"><span data-stu-id="e3113-128">Report messages that are not junk</span></span>

1. <span data-ttu-id="e3113-129">Cliquez sur les ellipses Autres **actions** dans le coin supérieur droit du message sélectionné, cliquez sur Signaler **le message** dans le menu déroulant, puis cliquez sur Non indésirable **.**</span><span class="sxs-lookup"><span data-stu-id="e3113-129">Click the **More actions** ellipses on the top-right corner of the selected message, click **Report message** from the dropdown menu, and then click **Not Junk**.</span></span>  

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="e3113-130">![Message de rapport - Plus d'actions](../../media/report-message-more-actions.png)</span><span class="sxs-lookup"><span data-stu-id="e3113-130">![Report Message - More actions](../../media/report-message-more-actions.png)</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="e3113-131">![Message de rapport - Courrier non indésirable](../../media/report-message-not-junk.png)</span><span class="sxs-lookup"><span data-stu-id="e3113-131">![Report Message - Not junk](../../media/report-message-not-junk.png)</span></span>

2. <span data-ttu-id="e3113-132">Le message sélectionné est envoyé à Microsoft pour analyse et déplacé vers la boîte de réception ou tout autre dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="e3113-132">The selected message will be sent to Microsoft for analysis and moved to Inbox or any other specified folder.</span></span>

## <a name="enable-the-report-message-and-report-phishing-add-ins"></a><span data-ttu-id="e3113-133">Activer les add-ins Signaler le message et Signaler le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="e3113-133">Enable the Report Message and Report Phishing add-ins</span></span>

<span data-ttu-id="e3113-134">Les add-ins Signaler le message et Signaler le hameçonnage pour Outlook et Outlook sur le web (anciennement Outlook Web App) permettent aux utilisateurs de signaler facilement les faux positifs (messages électroniques de qualité marqués comme faux) ou les faux négatifs (courrier électronique non autorisé) à Microsoft et à ses affiliés pour analyse.</span><span class="sxs-lookup"><span data-stu-id="e3113-134">The Report Message and Report Phishing add-ins for Outlook and Outlook on the web (formerly known as Outlook Web App) enable people to easily report false positives (good email marked as bad) or false negatives (bad email allowed) to Microsoft and its affiliates for analysis.</span></span> 

<span data-ttu-id="e3113-135">Microsoft utilise ces soumissions pour améliorer l'efficacité des technologies de protection de la messagerie.</span><span class="sxs-lookup"><span data-stu-id="e3113-135">Microsoft uses these submissions to improve the effectiveness of email protection technologies.</span></span> <span data-ttu-id="e3113-136">Par exemple, supposons que des personnes signalent de nombreux messages à l'aide du module de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="e3113-136">For example, suppose that people are reporting many messages using the Report Phishing add-in.</span></span> <span data-ttu-id="e3113-137">Ces informations sont disponibles dans le Tableau de bord de sécurité et d'autres rapports.</span><span class="sxs-lookup"><span data-stu-id="e3113-137">This information surfaces in the Security Dashboard and other reports.</span></span> <span data-ttu-id="e3113-138">L'équipe de sécurité de votre organisation peut utiliser ces informations pour indiquer que les stratégies anti-hameçonnage peuvent avoir besoin d'être mises à jour.</span><span class="sxs-lookup"><span data-stu-id="e3113-138">Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated.</span></span> 

<span data-ttu-id="e3113-139">Vous pouvez installer le module de rapport de message ou de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="e3113-139">You can install either the Report Message or Report Phishing add-in.</span></span> <span data-ttu-id="e3113-140">Si vous souhaitez que vos utilisateurs signalent à la fois le courrier indésirable et les messages de hameçonnage, déployez le add-in Signaler un message dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e3113-140">If you want your users to report both spam and phishing messages, deploy the Report Message add-in in your organization.</span></span> <span data-ttu-id="e3113-141">Pour plus d'informations, voir Activer le add-in Message de rapport.</span><span class="sxs-lookup"><span data-stu-id="e3113-141">For more information, see Enable the Report Message add-in.</span></span> 

<span data-ttu-id="e3113-142">Le add-in Report Message offre la possibilité de signaler les messages de courrier indésirable et de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="e3113-142">The Report Message add-in provides the option to report both spam and phishing messages.</span></span> <span data-ttu-id="e3113-143">Les administrateurs peuvent activer le add-in Message de rapport pour l'organisation, et les utilisateurs individuels peuvent l'installer eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="e3113-143">Admins can enable the Report Message add-in for the organization, and individual users can install it for themselves.</span></span> 

<span data-ttu-id="e3113-144">Le module de signalement du hameçonnage offre la possibilité de signaler uniquement les messages de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="e3113-144">The Report Phishing add-in provides the option to report only phishing messages.</span></span> <span data-ttu-id="e3113-145">Les administrateurs peuvent activer le module de signalement du hameçonnage pour l'organisation, et les utilisateurs individuels peuvent l'installer eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="e3113-145">Admins can enable the Report Phishing add-in for the organization, and individual users can install it for themselves.</span></span> 

<span data-ttu-id="e3113-146">Si vous êtes un utilisateur individuel, vous pouvez activer les deux modules pour vous-même.</span><span class="sxs-lookup"><span data-stu-id="e3113-146">If you're an individual user, you can enable both the add-ins for yourself.</span></span>

<span data-ttu-id="e3113-147">Si vous êtes un administrateur général ou un administrateur Exchange Online, et qu'Exchange est configuré pour utiliser l'authentification OAuth, vous pouvez activer le add-in Message de rapport et le module de signalement du hameçonnage pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e3113-147">f you're a global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can enable the Report Message add-in and the Report Phishing add-in for your organization.</span></span> <span data-ttu-id="e3113-148">Les deux modules sont désormais disponibles via [le déploiement centralisé.](../../admin/manage/centralized-deployment-of-add-ins.md)</span><span class="sxs-lookup"><span data-stu-id="e3113-148">Both add-ins are now available through [Centralized Deployment](../../admin/manage/centralized-deployment-of-add-ins.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="e3113-149">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="e3113-149">What do you need to know before you begin?</span></span>

- <span data-ttu-id="e3113-150">Le add-in Report Message et le add-in Report Phishing fonctionnent avec la plupart des abonnements Microsoft 365 et les produits suivants :</span><span class="sxs-lookup"><span data-stu-id="e3113-150">Both the Report Message add-in and the Report Phishing add-in works with most Microsoft 365 subscriptions and the following products:</span></span>

  - <span data-ttu-id="e3113-151">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="e3113-151">Outlook on the web</span></span>
  - <span data-ttu-id="e3113-152">Outlook 2013 SP1 ou une édition ultérieure</span><span class="sxs-lookup"><span data-stu-id="e3113-152">Outlook 2013 SP1 or later</span></span>
  - <span data-ttu-id="e3113-153">Outlook 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="e3113-153">Outlook 2016 for Mac</span></span>
  - <span data-ttu-id="e3113-154">Outlook inclus dans les applications Microsoft 365 pour Entreprise</span><span class="sxs-lookup"><span data-stu-id="e3113-154">Outlook included with Microsoft 365 apps for Enterprise</span></span>
  - <span data-ttu-id="e3113-155">Application Outlook pour iOS et Android</span><span class="sxs-lookup"><span data-stu-id="e3113-155">Outlook app for iOS and Android</span></span>

- <span data-ttu-id="e3113-156">Les deux modules ne sont pas disponibles pour les boîtes aux lettres partagées ou les boîtes aux lettres dans les organisations Exchange locales.</span><span class="sxs-lookup"><span data-stu-id="e3113-156">Both add-ins are not available for shared mailboxes or mailboxes in on-premises Exchange organizations.</span></span>

- <span data-ttu-id="e3113-157">Votre navigateur web existant doit fonctionner à la fois avec les modules de rapport de message et de signalement du hameçonnage. Toutefois, si vous remarquez que le module n'est pas disponible ou ne fonctionne pas comme prévu, essayez un autre navigateur.</span><span class="sxs-lookup"><span data-stu-id="e3113-157">Your existing web browser should work with both the Report Message and Report Phishing add-ins. But, if you notice the add-in is not available or not working as expected, try a different browser.</span></span>

- <span data-ttu-id="e3113-158">Pour les installation organisationnelles, l'organisation doit être configurée pour utiliser l'authentification OAuth.</span><span class="sxs-lookup"><span data-stu-id="e3113-158">For organizational installs, the organization needs to be configured to use OAuth authentication.</span></span> <span data-ttu-id="e3113-159">Pour plus d'informations, [voir Determine if Centralized Deployment of add-ins works for your organization.](../../admin/manage/centralized-deployment-of-add-ins.md)</span><span class="sxs-lookup"><span data-stu-id="e3113-159">For more information, see [Determine if Centralized Deployment of add-ins works for your organization](../../admin/manage/centralized-deployment-of-add-ins.md).</span></span>

- <span data-ttu-id="e3113-160">Les administrateurs doivent être membres du groupe de rôles Administrateurs globaux.</span><span class="sxs-lookup"><span data-stu-id="e3113-160">Admins need to be a member of the Global admins role group.</span></span> <span data-ttu-id="e3113-161">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="e3113-161">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="get-the-report-message-add-in"></a><span data-ttu-id="e3113-162">Obtenir le add-in Message de rapport</span><span class="sxs-lookup"><span data-stu-id="e3113-162">Get the Report Message add-in</span></span>

### <a name="get-the-add-in-for-yourself"></a><span data-ttu-id="e3113-163">Obtenir le add-in pour vous-même</span><span class="sxs-lookup"><span data-stu-id="e3113-163">Get the add-in for yourself</span></span>

1. <span data-ttu-id="e3113-164">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Message add-in.</span><span class="sxs-lookup"><span data-stu-id="e3113-164">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Message add-in.</span></span> <span data-ttu-id="e3113-165">To go directly to the Report Message add-in, go to <https://appsource.microsoft.com/product/office/wa104381180> .</span><span class="sxs-lookup"><span data-stu-id="e3113-165">To go directly to the Report Message add-in, go to <https://appsource.microsoft.com/product/office/wa104381180>.</span></span>

2. <span data-ttu-id="e3113-166">Cliquez **sur GET IT NOW**.</span><span class="sxs-lookup"><span data-stu-id="e3113-166">Click **GET IT NOW**.</span></span>

   ![Message de rapport : l'obtenir maintenant](../../media/ReportMessageGETITNOW.png)

3. <span data-ttu-id="e3113-168">Dans la boîte de dialogue qui s'affiche, examinez les conditions d'utilisation et la politique de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="e3113-168">In the dialog that appears, review the terms of use and privacy policy, and then click **Continue**.</span></span>

4. <span data-ttu-id="e3113-169">Connectez-vous à l'aide de votre compte scolaire ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour un usage personnel).</span><span class="sxs-lookup"><span data-stu-id="e3113-169">Sign in using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>

<span data-ttu-id="e3113-170">Une fois le add-in installé et activé, les icônes suivantes s'offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="e3113-170">After the add-in is installed and enabled, you'll see the following icons:</span></span>

- <span data-ttu-id="e3113-171">Dans Outlook, l'icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="e3113-171">In Outlook, the icon looks like this:</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="e3113-172">![Icône signaler le add-in Message pour Outlook](../../media/OutlookReportMessageIcon.png)</span><span class="sxs-lookup"><span data-stu-id="e3113-172">![Report Message add-in icon for Outlook](../../media/OutlookReportMessageIcon.png)</span></span>

- <span data-ttu-id="e3113-173">Dans Outlook sur le web, l'icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="e3113-173">In Outlook on the web, the icon looks like this:</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="e3113-174">![Icône du add-in Message de rapport Outlook sur le web](../../media/owa-report-message-icon.png)</span><span class="sxs-lookup"><span data-stu-id="e3113-174">![Outlook on the web Report Message add-in icon](../../media/owa-report-message-icon.png)</span></span>

### <a name="get-the-add-in-for-your-organization"></a><span data-ttu-id="e3113-175">Obtenir le add-in pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="e3113-175">Get the add-in for your organization</span></span>

> [!NOTE]
> <span data-ttu-id="e3113-176">L'apparition du module dans votre organisation peut prendre jusqu'à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="e3113-176">It could take up to 12 hours for the add-in to appear in your organization.</span></span>

1. <span data-ttu-id="e3113-177">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> .</span><span class="sxs-lookup"><span data-stu-id="e3113-177">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>.</span></span> <span data-ttu-id="e3113-178">Si la **page** Des applications intégrées aux **paramètres** n'est pas consultez, rendez-vous sur le lien Applications \>  \> **intégrées paramètres** en haut de la page **Applications intégrées.**</span><span class="sxs-lookup"><span data-stu-id="e3113-178">If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

2. <span data-ttu-id="e3113-179">Sélectionnez **Déployer le add-in** en haut de la page, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e3113-179">Select **Deploy Add-in** at the top of the page, and then select **Next**.</span></span>

   ![Page Services et modules dans le Centre d'administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

3. <span data-ttu-id="e3113-181">Dans le **volant Déployer un** nouveau module complémentaire qui s'affiche, examinez les informations, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e3113-181">In the **Deploy a new add-in** flyout that appears, review the information, and then click **Next**.</span></span>

4. <span data-ttu-id="e3113-182">Sur la page suivante, cliquez sur **Choisir dans le Store.**</span><span class="sxs-lookup"><span data-stu-id="e3113-182">On the next page, click **Choose from the Store**.</span></span>

   ![Déployer une nouvelle page de modules](../../media/NewAddInScreen2.png)

5. <span data-ttu-id="e3113-184">Dans la page **Sélectionner un add-in** qui s'affiche, cliquez dans la zone De recherche, entrez Message de rapport, puis cliquez sur **Icône**   ![ ](../../media/search-icon.png) Rechercher.</span><span class="sxs-lookup"><span data-stu-id="e3113-184">In the **Select add-in** page that appears, click in the **Search** box, enter **Report Message**, and then click **Search** ![Search icon](../../media/search-icon.png).</span></span> <span data-ttu-id="e3113-185">Dans la liste des résultats, recherchez **Message de rapport,** puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="e3113-185">In the list of results, find **Report Message** and then click **Add**.</span></span>

   ![Sélectionner des résultats de recherche de add-in](../../media/NewAddInScreen3.png)

6. <span data-ttu-id="e3113-187">Dans la boîte de dialogue qui s'affiche, examinez les informations de licence et de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="e3113-187">In the dialog that appears, review the licensing and privacy information, and then click **Continue**.</span></span>

7. <span data-ttu-id="e3113-188">Dans la page **Configurer le add-in** qui s'affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e3113-188">In the **Configure add-in** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="e3113-189">**Utilisateurs affectés**: sélectionnez l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e3113-189">**Assigned users**: Select one of the following values:</span></span>

     - <span data-ttu-id="e3113-190">**Tout le monde** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="e3113-190">**Everyone** (default)</span></span>
     - <span data-ttu-id="e3113-191">**Utilisateurs/groupes spécifiques**</span><span class="sxs-lookup"><span data-stu-id="e3113-191">**Specific users / groups**</span></span>
     - <span data-ttu-id="e3113-192">**Juste moi**</span><span class="sxs-lookup"><span data-stu-id="e3113-192">**Just me**</span></span>

   - <span data-ttu-id="e3113-193">**Méthode de déploiement**: sélectionnez l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e3113-193">**Deployment method**: Select one of the following values:</span></span>

     - <span data-ttu-id="e3113-194">**Fixe (par défaut)**: le add-in est automatiquement déployé sur les utilisateurs spécifiés et ils ne peuvent pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="e3113-194">**Fixed (Default)**: The add-in is automatically deployed to the specified users and they can't remove it.</span></span>
     - <span data-ttu-id="e3113-195">**Disponible**: les utilisateurs peuvent installer le add-in sur **home** \> **get add-ins** \> **admin-managed**.</span><span class="sxs-lookup"><span data-stu-id="e3113-195">**Available**: Users can install the add-in at **Home** \> **Get add-ins** \> **Admin-managed**.</span></span>
     - <span data-ttu-id="e3113-196">**Facultatif**: le add-in est automatiquement déployé pour les utilisateurs spécifiés, mais ils peuvent choisir de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="e3113-196">**Optional**: The add-in is automatically deployed to the specified users, but they can choose to remove it.</span></span>

   ![Configurer la page de l'ajout](../../media/configure-add-in.png)

   <span data-ttu-id="e3113-198">Lorsque vous avez terminé, cliquez sur **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="e3113-198">When you're finished, click **Deploy**.</span></span>

8. <span data-ttu-id="e3113-199">Dans la page Déployer le **message** de rapport qui s'affiche, vous verrez un rapport d'avancement suivi d'une confirmation du déploiement du module.</span><span class="sxs-lookup"><span data-stu-id="e3113-199">In the **Deploy Report Message** page that appears, you'll see a progress report followed by a confirmation that the add-in was deployed.</span></span> <span data-ttu-id="e3113-200">Après avoir lu les informations, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e3113-200">After you read the information, click **Next**.</span></span>

   ![Page Déployer le message de rapport](../../media/deploy-report-message-page.png)

9. <span data-ttu-id="e3113-202">Dans la page **Annoncer le add-in** qui s'affiche, examinez les informations, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e3113-202">On the **Announce add-in** page that appears, review the information, and then click **Close**.</span></span>

   ![Page d'annonce du add-in](../../media/announce-add-in-page.png)

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="e3113-204">Passer en revue ou modifier les paramètres du add-in Message de rapport</span><span class="sxs-lookup"><span data-stu-id="e3113-204">Review or edit settings for the Report Message add-in</span></span>

1. <span data-ttu-id="e3113-205">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> .</span><span class="sxs-lookup"><span data-stu-id="e3113-205">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>.</span></span> <span data-ttu-id="e3113-206">Si la **page** Des applications intégrées aux **paramètres** n'est pas consultez, rendez-vous sur le lien Applications \>  \> **intégrées paramètres** en haut de la page **Applications intégrées.**</span><span class="sxs-lookup"><span data-stu-id="e3113-206">If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

   ![Page Services et Add-Ins dans le nouveau Centre d'administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

2. <span data-ttu-id="e3113-208">Recherchez et sélectionnez le add-in **Message** de rapport.</span><span class="sxs-lookup"><span data-stu-id="e3113-208">Find and select the **Report Message** add-in.</span></span>

3. <span data-ttu-id="e3113-209">Dans le **volant Modifier le message** de rapport qui s'affiche, examinez et modifiez les paramètres selon le cas pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e3113-209">In the **Edit Report Message** flyout that appears, review and edit settings as appropriate for your organization.</span></span> <span data-ttu-id="e3113-210">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e3113-210">When you're finished, click **Save**.</span></span>

   ![Paramètres du add-in Message de rapport](../../media/EditReportMessageAddIn.png)

## <a name="get-the-report-phishing-add-in"></a><span data-ttu-id="e3113-212">Obtenir le module de signalement du hameçonnage</span><span class="sxs-lookup"><span data-stu-id="e3113-212">Get the Report Phishing add-in</span></span>

### <a name="get-the-add-in-for-yourself"></a><span data-ttu-id="e3113-213">Obtenir le add-in pour vous-même</span><span class="sxs-lookup"><span data-stu-id="e3113-213">Get the add-in for yourself</span></span>

1. <span data-ttu-id="e3113-214">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Phishing add-in.</span><span class="sxs-lookup"><span data-stu-id="e3113-214">Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Phishing add-in.</span></span>

2. <span data-ttu-id="e3113-215">Cliquez **sur GET IT NOW**.</span><span class="sxs-lookup"><span data-stu-id="e3113-215">Click **GET IT NOW**.</span></span>

3. <span data-ttu-id="e3113-216">Dans la boîte de dialogue qui s'affiche, examinez les conditions d'utilisation et la politique de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="e3113-216">In the dialog that appears, review the terms of use and privacy policy, and then click **Continue**.</span></span>

4. <span data-ttu-id="e3113-217">Connectez-vous à l'aide de votre compte scolaire ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour un usage personnel).</span><span class="sxs-lookup"><span data-stu-id="e3113-217">Sign in using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>

<span data-ttu-id="e3113-218">Une fois le add-in installé et activé, les icônes suivantes s'offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="e3113-218">After the add-in is installed and enabled, you'll see the following icons:</span></span>

- <span data-ttu-id="e3113-219">Dans Outlook, l'icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="e3113-219">In Outlook, the icon looks like this:</span></span>

  ![Icône Signaler le hameçonnage d'un add-in pour Outlook](../../media/Outlook-ReportPhishing.png)

- <span data-ttu-id="e3113-221">Dans Outlook sur le web, l'icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="e3113-221">In Outlook on the web, the icon looks like this:</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="e3113-222">![Icône de l'application De hameçonnage de rapport Outlook sur le web](../../media/OWA-ReportPhishing.png)</span><span class="sxs-lookup"><span data-stu-id="e3113-222">![Outlook on the web Report Phishing add-in icon](../../media/OWA-ReportPhishing.png)</span></span>

### <a name="get-the-add-in-for-your-organization"></a><span data-ttu-id="e3113-223">Obtenir le add-in pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="e3113-223">Get the add-in for your organization</span></span>

> [!NOTE]
> <span data-ttu-id="e3113-224">L'apparition du module dans votre organisation peut prendre jusqu'à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="e3113-224">It could take up to 12 hours for the add-in to appear in your organization.</span></span>

1. <span data-ttu-id="e3113-225">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> .</span><span class="sxs-lookup"><span data-stu-id="e3113-225">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>.</span></span> <span data-ttu-id="e3113-226">Si la **page** Des applications intégrées aux **paramètres** n'est pas consultez, rendez-vous sur le lien Applications \>  \> **intégrées paramètres** en haut de la page **Applications intégrées.**</span><span class="sxs-lookup"><span data-stu-id="e3113-226">If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

2. <span data-ttu-id="e3113-227">Sélectionnez **Déployer le add-in** en haut de la page, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e3113-227">Select **Deploy Add-in** at the top of the page, and then select **Next**.</span></span>

   ![Page Services et modules dans le Centre d'administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

3. <span data-ttu-id="e3113-229">Dans le **volant Déployer un** nouveau module complémentaire qui s'affiche, examinez les informations, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e3113-229">In the **Deploy a new add-in** flyout that appears, review the information, and then click **Next**.</span></span>

4. <span data-ttu-id="e3113-230">Sur la page suivante, cliquez sur **Choisir dans le Store.**</span><span class="sxs-lookup"><span data-stu-id="e3113-230">On the next page, click **Choose from the Store**.</span></span>

   ![Déployer une nouvelle page de modules](../../media/NewAddInScreen2.png)

5. <span data-ttu-id="e3113-232">Dans la page Sélectionner **un add-in** qui s'affiche, cliquez dans  la zone De recherche, entrez **Hameçonnage** de rapport, puis cliquez sur Icône  ![ ](../../media/search-icon.png) Recherche.</span><span class="sxs-lookup"><span data-stu-id="e3113-232">In the **Select add-in** page that appears, click in the **Search** box, enter **Report Phishing**, and then click **Search** ![Search icon](../../media/search-icon.png).</span></span> <span data-ttu-id="e3113-233">Dans la liste des résultats, recherchez **l'hameçonnage** de rapport, puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="e3113-233">In the list of results, find **Report Phishing** and then click **Add**.</span></span>

6. <span data-ttu-id="e3113-234">Dans la boîte de dialogue qui s'affiche, examinez les informations de licence et de confidentialité, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="e3113-234">In the dialog that appears, review the licensing and privacy information, and then click **Continue**.</span></span>

7. <span data-ttu-id="e3113-235">Dans la page **Configurer le add-in** qui s'affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e3113-235">In the **Configure add-in** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="e3113-236">**Utilisateurs affectés**: sélectionnez l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e3113-236">**Assigned users**: Select one of the following values:</span></span>

     - <span data-ttu-id="e3113-237">**Tout le monde** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="e3113-237">**Everyone** (default)</span></span>
     - <span data-ttu-id="e3113-238">**Utilisateurs/groupes spécifiques**</span><span class="sxs-lookup"><span data-stu-id="e3113-238">**Specific users / groups**</span></span>
     - <span data-ttu-id="e3113-239">**Juste moi**</span><span class="sxs-lookup"><span data-stu-id="e3113-239">**Just me**</span></span>

   - <span data-ttu-id="e3113-240">**Méthode de déploiement**: sélectionnez l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e3113-240">**Deployment method**: Select one of the following values:</span></span>

     - <span data-ttu-id="e3113-241">**Fixe (par défaut)**: le add-in est automatiquement déployé sur les utilisateurs spécifiés et ils ne peuvent pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="e3113-241">**Fixed (Default)**: The add-in is automatically deployed to the specified users and they can't remove it.</span></span>
     - <span data-ttu-id="e3113-242">**Disponible**: les utilisateurs peuvent installer le add-in sur **home** \> **get add-ins** \> **admin-managed**.</span><span class="sxs-lookup"><span data-stu-id="e3113-242">**Available**: Users can install the add-in at **Home** \> **Get add-ins** \> **Admin-managed**.</span></span>
     - <span data-ttu-id="e3113-243">**Facultatif**: le add-in est automatiquement déployé pour les utilisateurs spécifiés, mais ils peuvent choisir de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="e3113-243">**Optional**: The add-in is automatically deployed to the specified users, but they can choose to remove it.</span></span>

   <span data-ttu-id="e3113-244">Lorsque vous avez terminé, cliquez sur **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="e3113-244">When you're finished, click **Deploy**.</span></span>

8. <span data-ttu-id="e3113-245">Dans la page **Déployer** le hameçonnage de rapport qui s'affiche, vous verrez un rapport d'avancement suivi d'une confirmation du déploiement du module.</span><span class="sxs-lookup"><span data-stu-id="e3113-245">In the **Deploy Report Phishing** page that appears, you'll see a progress report followed by a confirmation that the add-in was deployed.</span></span> <span data-ttu-id="e3113-246">Après avoir lu les informations, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e3113-246">After you read the information, click **Next**.</span></span>

9. <span data-ttu-id="e3113-247">Dans la page **Annoncer le add-in** qui s'affiche, examinez les informations, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e3113-247">On the **Announce add-in** page that appears, review the information, and then click **Close**.</span></span>

## <a name="review-or-edit-settings-for-the-report-phishing-add-in"></a><span data-ttu-id="e3113-248">Examiner ou modifier les paramètres du module de signalement du hameçonnage</span><span class="sxs-lookup"><span data-stu-id="e3113-248">Review or edit settings for the Report Phishing add-in</span></span>

1. <span data-ttu-id="e3113-249">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> .</span><span class="sxs-lookup"><span data-stu-id="e3113-249">In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns>.</span></span> <span data-ttu-id="e3113-250">Si la **page** Des applications intégrées aux **paramètres** n'est pas consultez, rendez-vous sur le lien Applications \>  \> **intégrées paramètres** en haut de la page **Applications intégrées.**</span><span class="sxs-lookup"><span data-stu-id="e3113-250">If you don't see the **Add-in** Page, go to the **Settings** \> **Integrated apps** \> **Add-ins** link on the top of the **Integrated apps** page.</span></span>

2. <span data-ttu-id="e3113-251">Recherchez et sélectionnez **le** module de signalement du hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="e3113-251">Find and select the **Report Phishing** add-in.</span></span>

3. <span data-ttu-id="e3113-252">Dans le flyout **Modifier le hameçonnage** du rapport qui s'affiche, examinez et modifiez les paramètres selon le cas pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e3113-252">In the **Edit Report Phishing** flyout that appears, review, and edit settings as appropriate for your organization.</span></span> <span data-ttu-id="e3113-253">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e3113-253">When you're finished, click **Save**.</span></span>

## <a name="view-and-review-reported-messages"></a><span data-ttu-id="e3113-254">Afficher et examiner les messages signalés</span><span class="sxs-lookup"><span data-stu-id="e3113-254">View and review reported messages</span></span>

<span data-ttu-id="e3113-255">Pour passer en revue les messages que les utilisateurs signalent à Microsoft, vous avez les options ci-après :</span><span class="sxs-lookup"><span data-stu-id="e3113-255">To review messages that users report to Microsoft, you have these options:</span></span>

- <span data-ttu-id="e3113-256">Utilisez le portail Soumissions d'administrateur.</span><span class="sxs-lookup"><span data-stu-id="e3113-256">Use the Admin Submissions portal.</span></span> <span data-ttu-id="e3113-257">Pour plus d'informations, voir [Afficher les soumissions d'utilisateurs à Microsoft.](admin-submission.md#view-user-submissions-to-microsoft)</span><span class="sxs-lookup"><span data-stu-id="e3113-257">For more information, see [View user submissions to Microsoft](admin-submission.md#view-user-submissions-to-microsoft).</span></span>

- <span data-ttu-id="e3113-258">Créez une règle de flux de messagerie (également appelée règle de transport) pour envoyer des copies des messages signalés.</span><span class="sxs-lookup"><span data-stu-id="e3113-258">Create a mail flow rule (also known as a transport rule) to send copies of reported messages.</span></span> <span data-ttu-id="e3113-259">Pour obtenir des instructions, voir Utiliser des règles de flux de messagerie pour voir ce [que vos utilisateurs rapportent à Microsoft.](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="e3113-259">For instructions, see [Use mail flow rules to see what your users are reporting to Microsoft](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md).</span></span>