---
title: Activer le complément Signaler le message
f1.keywords:
- NOCSH
ms.author: tracyp
author: msfttracyp
manager: dansimp
ms.date: 03/26/2019
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
ms.openlocfilehash: 77fa9c2766ee1e2392ad9ea962a43f4779238209
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41599461"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="c8ed9-103">Activer le complément Signaler le message</span><span class="sxs-lookup"><span data-stu-id="c8ed9-103">Enable the Report Message add-in</span></span>

> [!NOTE]
> <span data-ttu-id="c8ed9-104">Le complément de message de rapport pour Outlook et Outlook sur le Web n’est pas exactement identique au filtre de courrier [indésirable Outlook](https://support.office.com/article/5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), bien que ces deux types permettent de marquer le courrier comme légitime, non légitime ou une tentative de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-104">The Report Message add-in for Outlook and Outlook on the web is not exactly the same thing as the [Outlook Junk Email Filter](https://support.office.com/article/5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), although both can be used to mark email as junk, not junk, or a phishing attempt.</span></span> <span data-ttu-id="c8ed9-105">La différence réside dans le fait que le complément de message de rapport pour Outlook et Outlook sur le Web avertit Microsoft du courrier indésirable, tandis que le filtre de courrier indésirable d’Outlook est utilisé pour organiser les messages électroniques dans la boîte aux lettres d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-105">The difference is, the Report Message add-in for Outlook and Outlook on the web notifies Microsoft about misclassified email, whereas the Outlook Junk Email Filter is used to organize email messages in a user's mailbox.</span></span>

## <a name="overview"></a><span data-ttu-id="c8ed9-106">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="c8ed9-106">Overview</span></span>

<span data-ttu-id="c8ed9-107">Le complément de message de rapport pour Outlook et Outlook sur le Web permet aux utilisateurs de signaler facilement les messages électroniques, qu’ils soient fiables ou malveillants, à Microsoft et à ses filiales pour analyse.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-107">The Report Message add-in for Outlook and Outlook on the web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis.</span></span> <span data-ttu-id="c8ed9-108">Microsoft utilise ces soumissions pour améliorer l’efficacité des technologies de protection de la messagerie.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-108">Microsoft uses these submissions to improve the effectiveness of email protection technologies.</span></span> <span data-ttu-id="c8ed9-109">En outre, si votre organisation utilise [Office 365 Advanced Threat Protection Plan 1](office-365-atp.md) ou [plan 2](office-365-ti.md), le complément Report message fournit à l’équipe de sécurité de votre organisation des informations utiles qu’il peut utiliser pour examiner et mettre à jour les stratégies de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-109">In addition, if your organization is using [Office 365 Advanced Threat Protection Plan 1](office-365-atp.md) or [Plan 2](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span>

<span data-ttu-id="c8ed9-110">Par exemple, supposons que des personnes signalent un grand nombre de messages comme hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-110">For example, suppose that people are reporting a lot of messages as phishing.</span></span> <span data-ttu-id="c8ed9-111">Ces informations sont représentées dans le [tableau de bord de sécurité](security-dashboard.md) et d’autres rapports.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-111">This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports.</span></span> <span data-ttu-id="c8ed9-112">L’équipe de sécurité de votre organisation peut utiliser ces informations pour indiquer que les stratégies de détection d’hameçonnage doivent être mises à jour.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-112">Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated.</span></span> <span data-ttu-id="c8ed9-113">Ou bien, si des personnes signalent un grand nombre de messages marqués comme légitimes comme légitimes à l’aide du complément de message de rapport, il se peut que l’équipe de sécurité de votre organisation doive ajuster les [stratégies de blocage du courrier](configure-the-anti-spam-policies.md)indésirable.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-113">Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span>

<span data-ttu-id="c8ed9-114">Le complément de message de rapport fonctionne avec votre abonnement Office 365 et les produits suivants :</span><span class="sxs-lookup"><span data-stu-id="c8ed9-114">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="c8ed9-115">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="c8ed9-115">Outlook on the web</span></span>
 - <span data-ttu-id="c8ed9-116">Outlook 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="c8ed9-116">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="c8ed9-117">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8ed9-117">Outlook 2016</span></span>
 - <span data-ttu-id="c8ed9-118">Outlook 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="c8ed9-118">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="c8ed9-119">Outlook inclus avec Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="c8ed9-119">Outlook included with Office 365 ProPlus</span></span>

<span data-ttu-id="c8ed9-120">Votre navigateur Web existant doit être suffisant pour que le complément de message de rapport fonctionne ; Toutefois, si vous remarquez que le complément n’est pas disponible ou ne fonctionne pas comme prévu, essayez un autre navigateur.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-120">Your existing web browser should suffice for the Report Message add-in to work; however, if you notice the add-in is not available or not working as expected, try a different browser.</span></span>

<span data-ttu-id="c8ed9-121">Si vous êtes un utilisateur individuel, vous pouvez [activer le complément de rapport de message pour vous-même](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="c8ed9-121">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span>

<span data-ttu-id="c8ed9-122">Si vous êtes un administrateur général Office 365 ou un administrateur Exchange Online et qu’Exchange est configuré pour utiliser l’authentification OAuth, vous pouvez [activer le complément de message de rapport pour votre organisation](#get-and-enable-the-report-message-add-in-for-your-organization).</span><span class="sxs-lookup"><span data-stu-id="c8ed9-122">If you're an Office 365 global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization).</span></span> <span data-ttu-id="c8ed9-123">Le complément de message de rapport est désormais disponible via un [déploiement centralisé](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span><span class="sxs-lookup"><span data-stu-id="c8ed9-123">The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>

## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="c8ed9-124">Obtenir le complément de message de rapport pour vous-même</span><span class="sxs-lookup"><span data-stu-id="c8ed9-124">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="c8ed9-125">Dans [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), recherchez le [complément Report message](https://appsource.microsoft.com/product/office/wa104381180).</span><span class="sxs-lookup"><span data-stu-id="c8ed9-125">In [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), search for the [Report Message add-in](https://appsource.microsoft.com/product/office/wa104381180).</span></span>

2. <span data-ttu-id="c8ed9-126">Choisissez **obtenir maintenant**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-126">Choose **GET IT NOW**.</span></span>

   ![Message de rapport-Get it](../media/ReportMessageGETITNOW.png)

3. <span data-ttu-id="c8ed9-128">Passez en revue les conditions d’utilisation et la politique de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-128">Review the terms of use and privacy policy.</span></span> <span data-ttu-id="c8ed9-129">Sélectionnez **Continue (Continuer)**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-129">Then choose **Continue**.</span></span>

4. <span data-ttu-id="c8ed9-130">Connectez-vous à Office 365 à l’aide de votre compte professionnel ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour une utilisation personnelle).</span><span class="sxs-lookup"><span data-stu-id="c8ed9-130">Sign in to Office 365 using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>

<span data-ttu-id="c8ed9-131">Une fois le complément installé et activé, les icônes suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="c8ed9-131">After the add-in is installed and enabled, you'll see the following icons:</span></span>

- <span data-ttu-id="c8ed9-132">Dans Outlook, l’icône se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="c8ed9-132">In Outlook, the icon looks like this:</span></span>

  ![Icône de complément de rapport de message pour Outlook](../media/OutlookReportMessageIcon.png)

- <span data-ttu-id="c8ed9-134">Dans Outlook sur le Web (anciennement appelé Outlook Web App), l’icône se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="c8ed9-134">In Outlook on the web (formerly known as Outlook Web App), the icon looks like this:</span></span>

  ![Icône de complément de message de rapport Web Outlook sur le Web](../media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)

> [!TIP]
> <span data-ttu-id="c8ed9-136">En guise d’étape suivante, Découvrez comment [utiliser le complément Report message](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="c8ed9-136">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="c8ed9-137">Obtenir et activer le complément de message de rapport pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="c8ed9-137">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8ed9-138">Vous devez être un administrateur général Office 365 ou un administrateur Exchange Online pour effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-138">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span> <span data-ttu-id="c8ed9-139">De plus, Exchange doit être configuré pour utiliser l’authentification OAuth pour en savoir plus, consultez la rubrique [Exchange Requirements (déploiement centralisé des compléments)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span><span class="sxs-lookup"><span data-stu-id="c8ed9-139">In addition, Exchange must be configured to use OAuth authentication To learn more, see [Exchange requirements (Centralized Deployment of add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>

1. <span data-ttu-id="c8ed9-140">Accédez à la [page des compléments de Services &](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) dans le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-140">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span>

   ![Page services et compléments dans le nouveau centre d’administration Microsoft 365](../media/ServicesAddInsPageNewM365AdminCenter.png)

2. <span data-ttu-id="c8ed9-142">Choisissez **+ déployer le complément**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-142">Choose **+ Deploy Add-in**.</span></span>

   ![Choisir déployer le complément](../media/ServicesAddIns-ChooseDeployAddIn.png)

3. <span data-ttu-id="c8ed9-144">Dans l’écran **nouveau complément** , passez en revue les informations, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-144">In the **New Add-In** screen, review the information, and then choose **Next**.</span></span>

   ![Détails sur les nouveaux compléments](../media/NewAddInScreen1.png)

4. <span data-ttu-id="c8ed9-146">Sélectionnez **je veux ajouter un complément à partir de l’Office Store**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-146">Select **I want to add an Add-In from the Office Store**, and then choose **Next**.</span></span>

   ![Je veux ajouter un nouveau complément](../media/NewAddInScreen2.png)

5. <span data-ttu-id="c8ed9-148">Recherchez **message de rapport**, et dans la liste des résultats, en regard du **complément de message de rapport**, choisissez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-148">Search for **Report Message**, and in the list of results, next to the **Report Message Add-In**, choose **Add**.</span></span>

   ![Recherchez message de rapport, puis cliquez sur Ajouter.](../media/NewAddInScreen3.png)

6. <span data-ttu-id="c8ed9-150">Dans l’écran du **rapport** , passez en revue les informations, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-150">On the **Report Message** screen, review the information, and then choose **Next**.</span></span>

   ![Signaler les détails du message](../media/ReportMessageAdd-InNewScreen4.png)

7. <span data-ttu-id="c8ed9-152">Spécifiez les paramètres par défaut de l’utilisateur pour Outlook, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-152">Specify the user default settings for Outlook, and  then choose **Next**.</span></span>

   ![Paramètres par défaut des messages de rapport pour Outlook](../media/ReportMessageOptionsScreen5.png)

8. <span data-ttu-id="c8ed9-154">Spécifiez qui reçoit le complément de message de rapport, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-154">Specify who gets the Report Message Add-in, and then choose **Save**.</span></span>

   ![Qui obtient le complément de message de rapport](../media/ReportMessageOptionsScreen6.png)

> [!TIP]
> <span data-ttu-id="c8ed9-156">Nous vous recommandons de [configurer une règle pour obtenir une copie des messages électroniques signalés par vos utilisateurs](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span><span class="sxs-lookup"><span data-stu-id="c8ed9-156">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span></span>

<span data-ttu-id="c8ed9-157">En fonction de ce que vous avez sélectionné lors de la configuration du complément (étapes 7-8 ci-dessus), le complément de message de [rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) sera disponible pour les personnes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-157">Depending on what you selected when you set up the add-in (steps 7-8 above), people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available.</span></span> <span data-ttu-id="c8ed9-158">Les personnes de votre organisation verront les icônes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8ed9-158">People in your organization will see the following icons:</span></span>

- <span data-ttu-id="c8ed9-159">Dans Outlook, l’icône se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="c8ed9-159">In Outlook, the icon looks like this:</span></span>

  ![Icône de complément de rapport de message pour Outlook](../media/OutlookReportMessageIcon.png)

- <span data-ttu-id="c8ed9-161">Dans Outlook sur le Web, l’icône se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="c8ed9-161">In Outlook on the web, the icon looks like this:</span></span>

  ![Icône de complément de message de rapport Web Outlook sur le Web](../media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)

> [!TIP]
> <span data-ttu-id="c8ed9-163">Lorsque vous informez les utilisateurs du complément Report message, incluez un lien permettant d' [utiliser le complément Report message](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="c8ed9-163">When you notify users about the Report Message add-in, include a link to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="c8ed9-164">Configurer une règle pour obtenir une copie des messages électroniques signalés par vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="c8ed9-164">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8ed9-165">Vous devez être un administrateur Exchange Online pour effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-165">You must be an Exchange Online Administrator to perform this task.</span></span>

<span data-ttu-id="c8ed9-166">Vous pouvez configurer une règle pour obtenir une copie des messages électroniques signalés par les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-166">You can set up a rule to get a copy of email messages reported by users in your organization.</span></span> <span data-ttu-id="c8ed9-167">Vous effectuez cette opération après avoir téléchargé et activé le complément de message de rapport pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-167">You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>

1. <span data-ttu-id="c8ed9-168">Dans le centre d’administration Exchange, sélectionnez **règles**de **flux** \> de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-168">In the Exchange admin center, choose **mail flow** \> **rules**.</span></span>

2. <span data-ttu-id="c8ed9-169">Sélectionnez **+** \> **créer une nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-169">Choose **+** \> **Create a new rule**.</span></span>

3. <span data-ttu-id="c8ed9-170">Dans la zone **nom** , tapez un nom, tel que des envois.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-170">In the **Name** box, type a name, such as Submissions.</span></span>

4. <span data-ttu-id="c8ed9-171">Dans la liste **appliquer cette règle si** , choisissez **l’adresse du destinataire inclut...**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-171">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span>

5. <span data-ttu-id="c8ed9-172">Dans l' **écran spécifier des mots ou** des expressions `junk@office365.microsoft.com` , `phish@office365.microsoft.com`ajoutez et, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-172">In the **specify words or phrases** screen, add `junk@office365.microsoft.com` and `phish@office365.microsoft.com`, and then choose **OK**.</span></span>

   ![Spécifier les adresses de messagerie de courrier indésirable et de hameçonnage pour la règle](../media/018c1833-f336-4333-a45c-f2e8b75cd698.png)

6. <span data-ttu-id="c8ed9-174">Dans la liste **effectuer les opérations suivantes...** , choisissez **CCI le message à..**..</span><span class="sxs-lookup"><span data-stu-id="c8ed9-174">In the **Do the following...** list, choose **Bcc the message to...**.</span></span>

7. <span data-ttu-id="c8ed9-175">Ajoutez un administrateur général, un administrateur de sécurité et/ou un lecteur de sécurité qui doit recevoir une copie de chaque message électronique que les personnes signalent à Microsoft, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-175">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span>

   ![Ajoutez un administrateur général ou un administrateur de sécurité pour recevoir une copie de chaque message signalé.](../media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)

8. <span data-ttu-id="c8ed9-177">Sélectionnez **auditer cette règle avec le niveau de gravité**, puis choisissez **moyenne**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-177">Select **Audit this rule with severity level**, and choose **Medium**.</span></span>

9. <span data-ttu-id="c8ed9-178">Sous **choisir un mode pour cette règle**, choisissez **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-178">Under **Choose a mode for this rule**, choose **Enforce**.</span></span>

   ![Configurer une règle pour obtenir une copie de chaque message signalé](../media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)

10. <span data-ttu-id="c8ed9-180">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-180">Choose **Save**.</span></span>

<span data-ttu-id="c8ed9-181">Avec cette règle en place, chaque fois que quelqu’un de votre organisation signale un message électronique à l’aide du complément de message de rapport, votre administrateur général, votre administrateur de sécurité et/ou votre lecteur de sécurité recevront une copie de ce message.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-181">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message.</span></span> <span data-ttu-id="c8ed9-182">Ces informations vous permettent de configurer ou d’ajuster des stratégies, telles que [des stratégies de liens approuvés Office 365 ATP](atp-safe-links.md) ou vos paramètres de [blocage du courrier indésirable](anti-spam-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="c8ed9-182">This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies, or your [anti-spam](anti-spam-protection.md) settings.</span></span>

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="c8ed9-183">En savoir plus sur l’utilisation du complément de message de rapport</span><span class="sxs-lookup"><span data-stu-id="c8ed9-183">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="c8ed9-184">Voir [use the Report message Add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="c8ed9-184">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="c8ed9-185">Vérifier ou modifier les paramètres du complément de message de rapport</span><span class="sxs-lookup"><span data-stu-id="c8ed9-185">Review or edit settings for the Report Message add-in</span></span>

<span data-ttu-id="c8ed9-186">Vous pouvez consulter et modifier les paramètres par défaut du complément de message de rapport sur la [page des compléments & services](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span><span class="sxs-lookup"><span data-stu-id="c8ed9-186">You can review and edit the default settings for the Report Message add-in on the [Services & Add-Ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8ed9-187">Vous devez être un administrateur général Office 365 ou un administrateur Exchange Online pour effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-187">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>

1. <span data-ttu-id="c8ed9-188">Accédez à la [page des compléments de Services &](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) dans le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-188">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span>

   ![Page services et compléments dans le nouveau centre d’administration Microsoft 365](../media/ServicesAddInsPageNewM365AdminCenter.png)

2. <span data-ttu-id="c8ed9-190">Recherchez et sélectionnez le complément Report message.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-190">Find and select the Report Message add-in.</span></span>

   ![Rechercher et sélectionner le complément de message de rapport](../media/FindReportMessageAddIn.png)

3. <span data-ttu-id="c8ed9-192">Dans l’écran signaler un message, vérifiez et modifiez les paramètres en fonction de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c8ed9-192">On the Report Message screen, review and edit settings as appropriate for your organization.</span></span>

   ![Paramètres du complément de message de rapport](../media/EditReportMessageAddIn.png)

## <a name="related-topics"></a><span data-ttu-id="c8ed9-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8ed9-194">Related topics</span></span>

[<span data-ttu-id="c8ed9-195">Utiliser le complément de message de rapport</span><span class="sxs-lookup"><span data-stu-id="c8ed9-195">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)

[<span data-ttu-id="c8ed9-196">Afficher les rapports de sécurité de messagerie &amp; dans le centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="c8ed9-196">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="c8ed9-197">Afficher les rapports pour Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="c8ed9-197">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="c8ed9-198">Utiliser l’Explorateur dans le &amp; Centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="c8ed9-198">Use Explorer in the Security &amp; Compliance Center</span></span>](threat-explorer.md)
