---
title: Installer et utiliser le add-in Junk Email Reporting pour Microsoft Outlook
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
ms.assetid: 4650fec1-4ee3-4659-abbc-bf091718cb26
ms.collection:
- M365-security-compliance
description: Découvrez comment installer et utiliser le add-in De rapport de courrier indésirable Microsoft pour signaler le courrier indésirable, le courrier non indésirable et le hameçonnage à Microsoft.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 896ef89149e5ef65ea96b2b21e1010c29fa7a7fc
ms.sourcegitcommit: 537e513a4a232a01e44ecbc76d86a8bcaf142482
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50029419"
---
# <a name="install-and-use-the-junk-email-reporting-add-in-for-microsoft-outlook"></a><span data-ttu-id="a6576-103">Installer et utiliser le add-in Junk Email Reporting pour Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="a6576-103">Install and use the Junk Email Reporting add-in for Microsoft Outlook</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


> [!NOTE]
> <span data-ttu-id="a6576-104">Si vous n’utilisez pas actuellement le add-in Junk [](enable-the-report-message-add-in.md) E-mail Reporting, [](enable-the-report-phish-add-in.md) nous vous recommandons plutôt de le signaler ou de signaler le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="a6576-104">If you aren't currently using the Junk E-mail Reporting add-in, we recommend the [Report Message add-in](enable-the-report-message-add-in.md) or the [Report Phishing add-in](enable-the-report-phish-add-in.md) instead.</span></span> <span data-ttu-id="a6576-105">Pour plus d’informations, voir [Signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="a6576-105">For more information, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

<span data-ttu-id="a6576-106">Le junk email reporting Add-in pour Microsoft Outlook permet aux utilisateurs d’envoyer des faux positifs (message électronique de qualité marqué comme courrier indésirable), des faux négatifs (courrier indésirable autorisé) et des messages de hameçonnage à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a6576-106">The Junk Email Reporting Add-in for Microsoft Outlook allows users to submit false positives (good email marked as spam), false negatives (bad email allowed) and phishing messages to Microsoft.</span></span> <span data-ttu-id="a6576-107">Si votre organisation n’utilise pas Exchange Online Protection (par exemple, Exchange local ou des services de messagerie autres qu’Exchange Online), l’envoi de votre rapport de courrier indésirable n’affecte pas votre filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a6576-107">If your organization doesn't use Exchange Online Protection (for example, on-premises Exchange or email services other than Exchange Online), your junk email report submission will not affect your spam filtering.</span></span>

<span data-ttu-id="a6576-108">Cette rubrique explique comment installer et utiliser le add-in Junk Email Reporting.</span><span class="sxs-lookup"><span data-stu-id="a6576-108">This topic explains how to install and use the Junk Email Reporting add-in.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="a6576-109">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a6576-109">What do you need to know before you begin?</span></span>

- <span data-ttu-id="a6576-110">Pour installer le add-in Junk Email Reporting, consultez la section [Install the Junk Email Reporting add-in](#install-the-junk-email-reporting-add-in) later in this article.</span><span class="sxs-lookup"><span data-stu-id="a6576-110">To install the Junk Email Reporting add-in, see the [Install the Junk Email Reporting add-in](#install-the-junk-email-reporting-add-in) section later in this article.</span></span>

- <span data-ttu-id="a6576-111">Le add-in Junk Email Reporting fonctionne avec les versions suivantes d’Outlook :</span><span class="sxs-lookup"><span data-stu-id="a6576-111">The Junk Email Reporting add-in works with the following versions of Outlook:</span></span>

  - <span data-ttu-id="a6576-112">Outlook 2013 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a6576-112">Outlook 2013 or later</span></span>
  - <span data-ttu-id="a6576-113">Outlook inclus avec Microsoft 365 Apps for enterprise</span><span class="sxs-lookup"><span data-stu-id="a6576-113">Outlook included with Microsoft 365 Apps for enterprise</span></span>

- <span data-ttu-id="a6576-114">Pour plus d’informations sur la notification des messages à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="a6576-114">For more information about reporting messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="use-the-junk-email-reporting-add-in-to-report-spam-and-phishing-messages"></a><span data-ttu-id="a6576-115">Utiliser le add-in Junk Email Reporting (Signalement du courrier indésirable) pour signaler les messages de courrier indésirable et de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="a6576-115">Use the Junk Email Reporting add-in to report spam and phishing messages</span></span>

1. <span data-ttu-id="a6576-116">Pour les messages dans la boîte de réception ou tout autre dossier de courrier électronique à l’exception du courrier indésirable, utilisez l’une des méthodes suivantes pour signaler le courrier indésirable et les messages de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="a6576-116">For messages in the Inbox or any other email folder except Junk Email, use any of the following methods to report spam and phishing messages:</span></span>

   - <span data-ttu-id="a6576-117">Sélectionnez le message ou ouvrez-le.</span><span class="sxs-lookup"><span data-stu-id="a6576-117">Select the message or open the message.</span></span> <span data-ttu-id="a6576-118">Dans **l’onglet** Accueil **ou Message** du ruban,  cliquez sur Courrier **indésirable,** puis sélectionnez Signaler comme courrier indésirable ou Signaler **comme hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="a6576-118">In the **Home** or **Message** tab in the ribbon, click **Junk**, and then select **Report as Junk** or **Report as Phishing**.</span></span>

     ![Signaler le courrier indésirable ou le hameçonnage à partir du ruban](../../media/junk-email-reporting-ribbon.png)

   - <span data-ttu-id="a6576-120">Cliquez avec le bouton droit sur le  message, **sélectionnez** Courrier indésirable, puis sélectionnez Signaler comme courrier indésirable **ou Signaler comme hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="a6576-120">Right-click on the message, select **Junk**, and then select **Report as Junk** or **Report as Phishing**.</span></span>

     ![Signaler le courrier indésirable ou le hameçonnage à partir du clic droit](../../media/junk-email-reporting-right-click.png)

   - <span data-ttu-id="a6576-122">Sélectionnez plusieurs messages, cliquez avec le bouton droit, puis sélectionnez **Signaler comme** courrier indésirable ou Signaler **comme hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="a6576-122">Select multiple messages, right-click, and then select **Report as Junk** or **Report as Phishing**.</span></span>

     ![Signaler plusieurs messages électroniques de courrier indésirable ou de hameçonnage à partir du clic droit](../../media/junk-email-reporting-right-click-multiple.png)

2. <span data-ttu-id="a6576-124">Dans la boîte de dialogue qui s’affiche, lisez les informations et cliquez sur **Rapport.**</span><span class="sxs-lookup"><span data-stu-id="a6576-124">In the dialog that appears, read the information and click **Report**.</span></span> <span data-ttu-id="a6576-125">Si vous changez d’avis, cliquez sur **Ne pas signaler.**</span><span class="sxs-lookup"><span data-stu-id="a6576-125">If you change your mind, click **Don't Report**.</span></span>

   ![Boîte de dialogue Signaler comme courrier indésirable](../../media/junk-email-reporting-report-as-junk-dialog.png)

   ![Boîte de dialogue Signaler comme hameçonnage](../../media/junk-email-reporting-report-as-phishing-dialog.png)

3. <span data-ttu-id="a6576-128">Les messages sélectionnés sont envoyés à Microsoft pour analyse et :</span><span class="sxs-lookup"><span data-stu-id="a6576-128">The selected messages will be sent to Microsoft for analysis and:</span></span>

   - <span data-ttu-id="a6576-129">Déplacé vers le dossier Courrier indésirable s’il a été signalé comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a6576-129">Moved to the Junk Email folder if it was reported as spam.</span></span>
   - <span data-ttu-id="a6576-130">Supprimé s’il a été signalé comme hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="a6576-130">Deleted if it was reported as phishing.</span></span>

   <span data-ttu-id="a6576-131">Pour confirmer que les messages ont été envoyés, ouvrez le dossier **Éléments envoyés** pour afficher les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="a6576-131">To confirm that the messages have been submitted, open your **Sent Items** folder to view the submitted messages.</span></span>

## <a name="use-the-junk-email-reporting-add-in-to-report-non-spam-and-phishing-messages-from-the-junk-email-folder"></a><span data-ttu-id="a6576-132">Utiliser le add-in Junk Email Reporting (Signalement du courrier indésirable) pour signaler les messages de courrier non indésirable et de hameçonnage à partir du dossier Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="a6576-132">Use the Junk Email Reporting add-in to report non-spam and phishing messages from the Junk Email folder</span></span>

1. <span data-ttu-id="a6576-133">Dans le dossier Courrier indésirable, utilisez l’une des méthodes suivantes pour signaler les faux positifs du courrier indésirable ou les messages de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="a6576-133">In the Junk Email folder, use any of the following methods to report spam false positives or phishing messages:</span></span>

   - <span data-ttu-id="a6576-134">Sélectionnez le message ou ouvrez-le.</span><span class="sxs-lookup"><span data-stu-id="a6576-134">Select the message or open the message.</span></span> <span data-ttu-id="a6576-135">Dans **l’onglet** Accueil ou **Message** du ruban,  cliquez sur Ne pas courrier **indésirable,** puis sélectionnez Signaler comme courrier non indésirable ou Signaler **comme hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="a6576-135">In the **Home** or **Message** tab in the ribbon, click **Not Junk**, and then select **Report as Not Junk** or **Report as Phishing**.</span></span>

     ![Signaler le courrier indésirable ou le hameçonnage à partir du ruban dans le dossier Courrier indésirable](../../media/junk-email-reporting-junk-folder-ribbon.png)

   - <span data-ttu-id="a6576-137">Cliquez avec le bouton droit sur le  message, **cliquez** sur Courrier indésirable, puis sélectionnez Signaler comme courrier non indésirable ou Signaler **comme hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="a6576-137">Right-click on the message, click **Junk**, and then select **Report as Not Junk** or **Report as Phishing**.</span></span>

     ![Signaler le courrier indésirable ou le hameçonnage en cliquant avec le bouton droit dans le dossier Courrier indésirable](../../media/junk-email-reporting-junk-folder-right-click.png)

   - <span data-ttu-id="a6576-139">Sélectionnez plusieurs messages, cliquez avec le bouton droit, puis sélectionnez **Signaler comme** courrier non indésirable ou Signaler **comme hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="a6576-139">Select multiple messages, right-click, and then select **Report as Not Junk** or **Report as Phishing**.</span></span>

     ![Signaler plusieurs messages électroniques non indésirables ou de hameçonnage en cliquant avec le bouton droit dans le dossier Courrier indésirable](../../media/junk-email-reporting-junk-folder-right-click-multiple.png)

2. <span data-ttu-id="a6576-141">Dans la boîte de dialogue qui s’affiche, lisez les informations et cliquez sur **Rapport.**</span><span class="sxs-lookup"><span data-stu-id="a6576-141">In the dialog that appears, read the information and click **Report**.</span></span> <span data-ttu-id="a6576-142">Si vous changez d’avis, cliquez sur **Ne pas signaler.**</span><span class="sxs-lookup"><span data-stu-id="a6576-142">If you change your mind, click **Don't Report**.</span></span>

   ![Boîte de dialogue Signaler comme courrier indésirable](../../media/junk-email-reporting-report-as-not-junk-dialog.png)

   ![Boîte de dialogue Signaler comme hameçonnage](../../media/junk-email-reporting-report-as-phishing-dialog.png)

3. <span data-ttu-id="a6576-145">Les messages sélectionnés sont envoyés à Microsoft pour analyse et :</span><span class="sxs-lookup"><span data-stu-id="a6576-145">The selected messages will be sent to Microsoft for analysis and:</span></span>

   - <span data-ttu-id="a6576-146">Déplacé vers le dossier Courrier indésirable s’il a été signalé comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a6576-146">Moved to the Junk Email folder if it was reported as spam.</span></span>
   - <span data-ttu-id="a6576-147">Supprimé s’il a été signalé comme hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="a6576-147">Deleted if it was reported as phishing.</span></span>

   <span data-ttu-id="a6576-148">Pour confirmer que les messages ont été envoyés, ouvrez le dossier **Éléments envoyés** pour afficher les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="a6576-148">To confirm that the messages have been submitted, open your **Sent Items** folder to view the submitted messages.</span></span>

## <a name="install-the-junk-email-reporting-add-in"></a><span data-ttu-id="a6576-149">Installer le add-in Junk Email Reporting</span><span class="sxs-lookup"><span data-stu-id="a6576-149">Install the Junk Email Reporting add-in</span></span>

- <span data-ttu-id="a6576-150">Vous devez avoir des privilèges d’administrateur sur l’ordinateur sur lequel vous installez le module.</span><span class="sxs-lookup"><span data-stu-id="a6576-150">You need to have administrator privileges on the computer where you're installing the add-in.</span></span>

- <span data-ttu-id="a6576-151">Go to <https://www.microsoft.com/download/details.aspx?id=18275> and download the appropriate .msi file for your version of Office to a location that’s easy to find:</span><span class="sxs-lookup"><span data-stu-id="a6576-151">Go to <https://www.microsoft.com/download/details.aspx?id=18275> and download the appropriate .msi file for your version of Office to a location that's easy to find:</span></span>

  - <span data-ttu-id="a6576-152">**32 bits**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi`</span><span class="sxs-lookup"><span data-stu-id="a6576-152">**32-bit**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi`</span></span>
  - <span data-ttu-id="a6576-153">**64 bits**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi`</span><span class="sxs-lookup"><span data-stu-id="a6576-153">**64-bit**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi`</span></span>

- <span data-ttu-id="a6576-154">Pour Outlook 2013 ou une ultérieure, le seul prérequis est Microsoft .NET Framework 2.0.</span><span class="sxs-lookup"><span data-stu-id="a6576-154">For Outlook 2013 or later, the only prerequisite is the Microsoft .NET Framework 2.0.</span></span> <span data-ttu-id="a6576-155">Dans Windows 10, vous n’installez pas .NET Framework 2.0 à partir d’un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="a6576-155">In Windows 10, you don't install the .NET Framework 2.0 from a download.</span></span>

### <a name="install-the-junk-email-reporting-add-in-using-the-setup-wizard"></a><span data-ttu-id="a6576-156">Installer le add-in Junk Email Reporting à l’aide de l’Assistant Installation</span><span class="sxs-lookup"><span data-stu-id="a6576-156">Install the Junk Email Reporting Add-in using the Setup wizard</span></span>

1. <span data-ttu-id="a6576-157">Sur votre ordinateur, fermez Outlook.</span><span class="sxs-lookup"><span data-stu-id="a6576-157">On your computer, close Outlook.</span></span>

2. <span data-ttu-id="a6576-158">Dans Windows 10, vérifiez que .NET Framework 2.0 est activé.</span><span class="sxs-lookup"><span data-stu-id="a6576-158">In Windows 10, verify the .NET Framework 2.0 is enabled.</span></span> <span data-ttu-id="a6576-159">Pour obtenir des instructions, voir [Activer .NET Framework 3.5 dans le Panneau de contrôle.](https://docs.microsoft.com/dotnet/framework/install/dotnet-35-windows-10#enable-the-net-framework-35-in-control-panel)</span><span class="sxs-lookup"><span data-stu-id="a6576-159">For instructions, see [Enable the .NET Framework 3.5 in Control Panel](https://docs.microsoft.com/dotnet/framework/install/dotnet-35-windows-10#enable-the-net-framework-35-in-control-panel).</span></span>

3. <span data-ttu-id="a6576-160">Recherchez le fichier .msi que vous avez téléchargé et double-cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="a6576-160">Locate the .msi file you downloaded and double-click on it.</span></span>

4. <span data-ttu-id="a6576-161">Dans la page **Bienvenue à la configuration du complément Microsoft Junk Email Reporting**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a6576-161">On the **Welcome to Microsoft Junk Email Reporting Add-in Setup** page, click **Next**.</span></span>

5. <span data-ttu-id="a6576-162">Examinez le contrat de licence, cliquez **sur J’accepte** les termes du contrat de licence si vous acceptez les termes, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a6576-162">Review the license agreement, click **I accept the terms in the License Agreement** if you agree to the terms, and then click **Next**.</span></span>

6. <span data-ttu-id="a6576-163">Une fois l'exécution de l'Assistant terminée, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="a6576-163">When the wizard is complete, click **Finish**.</span></span>

<span data-ttu-id="a6576-164">Lancez Outlook.</span><span class="sxs-lookup"><span data-stu-id="a6576-164">Start Outlook.</span></span>

<span data-ttu-id="a6576-p109">Consultez le bouton **Courrier indésirable** sur votre ruban Outlook. Vous pouvez à présent signaler des messages de courrier indésirable à Microsoft en les sélectionnant dans votre boîte de réception, puis en cliquant sur le bouton permettant de **signaler le courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="a6576-p109">Look for the **Junk** button on your Outlook ribbon. You can now report junk email messages to Microsoft by selecting the junk email messages in your Inbox and clicking the **Report Junk** button.</span></span>

<span data-ttu-id="a6576-p110">Cliquez sur la flèche vers le bas en regard du bouton **Courrier indésirable** pour plus d'options, telles que le **signalement en tant que hameçonnage** si vous souhaitez signaler des messages électroniques d'hameçonnage à Microsoft. Dans votre dossier de courrier indésirable, vous pouvez également sélectionner l'option de **signalement en tant que courrier non indésirable** si un message électronique a été identifié à tort comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a6576-p110">Choose the down arrow next to **Junk** for more options such as **Report as Phishing** if you want to report phishing scam emails to Microsoft. In your junk mail folder, you can also select, **Report not junk** if an email was incorrectly identified as junk mail.</span></span>

### <a name="install-the-junk-email-reporting-add-in-using-silent-mode"></a><span data-ttu-id="a6576-169">Installation du complément de création de rapports de courrier indésirable en mode sans assistance</span><span class="sxs-lookup"><span data-stu-id="a6576-169">Install the Junk Email Reporting Add-In using Silent Mode</span></span>

1. <span data-ttu-id="a6576-170">Sur votre ordinateur, fermez Outlook.</span><span class="sxs-lookup"><span data-stu-id="a6576-170">On your computer, close Outlook.</span></span>

2. <span data-ttu-id="a6576-171">Dans Windows 10, installez .NET Framework 2.0 en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a6576-171">In Windows 10, install the .NET Framework 2.0 by running the following command:</span></span>

   ```dos
   DISM /Online /Enable-Feature /FeatureName:NetFx3 /All
   ```

3. <span data-ttu-id="a6576-172">Pour installer le module sans intervention de l’utilisateur, ouvrez une invite de commandes et utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a6576-172">To install the add-in without any user interaction, open a Command Prompt and use the following syntax:</span></span>

   ```dos
   msiexec /qn /i "<PathToMSIFile>\<MSIFile>" [MaxMessageSelection=<1-50>] [BccEmailAddress="<EmailAddress1>; <EmailAddress2>"...]
   ```

   - <span data-ttu-id="a6576-173">`MaxMessageSelection` spécifie le nombre maximal de messages que vous pouvez sélectionner pour une soumission unique.</span><span class="sxs-lookup"><span data-stu-id="a6576-173">`MaxMessageSelection` specifies the maximum number of messages that you can select for a single submission.</span></span> <span data-ttu-id="a6576-174">Les valeurs valides sont de 1 à 50.</span><span class="sxs-lookup"><span data-stu-id="a6576-174">Valid values are from 1 to 50.</span></span> <span data-ttu-id="a6576-175">Par défaut, la valeur 15 s’applique.</span><span class="sxs-lookup"><span data-stu-id="a6576-175">The default value is 15.</span></span>

   - <span data-ttu-id="a6576-176">`BccEmailAddress` spécifie les destinataires Bcc supplémentaires qui recevront une copie de toutes les soumissions d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a6576-176">`BccEmailAddress` specifies additional Bcc recipients who will receive a copy of all user submissions.</span></span> <span data-ttu-id="a6576-177">La valeur par défaut est vide (aucun destinataire Bcc supplémentaire).</span><span class="sxs-lookup"><span data-stu-id="a6576-177">The default value is blank (no additional Bcc recipients).</span></span>

   <span data-ttu-id="a6576-178">Cet exemple installe la version 64 bits du module à partir du chemin d’accès spécifié avec les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="a6576-178">This example installs the 64-bit version of the add-in from the specified path with the default settings.</span></span>

   ```dos
   msiexec /qn /i "C:\Downloads\Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi"
   ```

   <span data-ttu-id="a6576-179">Cet exemple installe la version 32 bits du complément à partir du chemin d’accès spécifié avec les paramètres supplémentaires suivants :</span><span class="sxs-lookup"><span data-stu-id="a6576-179">This example installs the 32-bit version of the add-in from the specified path with the following additional settings:</span></span>

   - <span data-ttu-id="a6576-180">Jusqu’à 20 messages peuvent être sélectionnés dans une seule soumission.</span><span class="sxs-lookup"><span data-stu-id="a6576-180">Up to 20 messages can be selected in a single submission.</span></span>
   - <span data-ttu-id="a6576-181">junkreports@contoso.com et hollyd@treyresearch.net recevoir des copies Bcc de toutes les soumissions.</span><span class="sxs-lookup"><span data-stu-id="a6576-181">junkreports@contoso.com and hollyd@treyresearch.net receive Bcc copies of all submissions.</span></span>

   ```dos
   msiexec /qn /i "C:\Downloads\Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi" MaxMessageSelection=20 BccEmailAddress="junkreports@contoso.com; hollyd@treyresearch.net"
   ```

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="a6576-182">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="a6576-182">How do you know this worked?</span></span>

<span data-ttu-id="a6576-183">Pour vérifier que vous avez correctement installé le service Junk Email Reporting Add-in, dans Outlook, vous devez suivre l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6576-183">To verify that you've successfully installed the Junk Email Reporting Add-in, do the any of the following steps in Outlook:</span></span>

- <span data-ttu-id="a6576-184">Sélectionnez le message ou ouvrez-le.</span><span class="sxs-lookup"><span data-stu-id="a6576-184">Select the message or open the message.</span></span> <span data-ttu-id="a6576-185">Dans **l’onglet** Accueil **ou Message** du ruban, cliquez sur Courrier indésirable **et** vérifiez que les options suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="a6576-185">In the **Home** or **Message** tab in the ribbon, click **Junk**, and verify that the following options are available:</span></span>

  - <span data-ttu-id="a6576-186">**Signaler comme courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="a6576-186">**Report as Junk**</span></span>
  - <span data-ttu-id="a6576-187">**Signaler comme hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="a6576-187">**Report as Phishing**</span></span>
  - <span data-ttu-id="a6576-188">**Options de signalement du courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="a6576-188">**Junk Reporting Options**</span></span>
  - <span data-ttu-id="a6576-189">**Signaler l’aide de Junk Online**</span><span class="sxs-lookup"><span data-stu-id="a6576-189">**Report Junk Online Help**</span></span>

  ![Signaler le courrier indésirable ou le hameçonnage à partir du ruban](../../media/junk-email-reporting-ribbon.png)

- <span data-ttu-id="a6576-191">Cliquez avec le bouton droit sur le message, **sélectionnez** Courrier indésirable et vérifiez que les options suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="a6576-191">Right-click on the message, select **Junk**, and verify that the following options are available:</span></span>

  - <span data-ttu-id="a6576-192">**Signaler comme courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="a6576-192">**Report as Junk**</span></span>
  - <span data-ttu-id="a6576-193">**Signaler comme hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="a6576-193">**Report as Phishing**</span></span>
  - <span data-ttu-id="a6576-194">**Options de signalement du courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="a6576-194">**Junk Reporting Options**</span></span>
  - <span data-ttu-id="a6576-195">**Signaler l’aide de Junk Online**</span><span class="sxs-lookup"><span data-stu-id="a6576-195">**Report Junk Online Help**</span></span>

  ![Signaler le courrier indésirable ou le hameçonnage à partir du clic droit](../../media/junk-email-reporting-right-click.png)

- <span data-ttu-id="a6576-197">Sélectionnez plusieurs messages, cliquez avec le bouton droit et vérifiez que les options suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="a6576-197">Select multiple messages, right click, and verify that the following options are available:</span></span>

  - <span data-ttu-id="a6576-198">**Signaler comme courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="a6576-198">**Report as Junk**</span></span>
  - <span data-ttu-id="a6576-199">**Signaler comme hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="a6576-199">**Report as Phishing**</span></span>

  ![Signaler plusieurs messages électroniques de courrier indésirable ou de hameçonnage à partir du clic droit](../../media/junk-email-reporting-right-click-multiple.png)

- <span data-ttu-id="a6576-201">Faites les actions précédentes dans le **dossier Courrier** indésirable et vérifiez que les options **de** signalement de courrier indésirable précédentes sont désormais **non** indésirables.</span><span class="sxs-lookup"><span data-stu-id="a6576-201">Do the previous actions in the **Junk Email** folder and verify the previous **Junk** reporting options are now **Not Junk**.</span></span>

  ![Signaler le courrier indésirable ou le hameçonnage à partir du ruban dans le dossier Courrier indésirable](../../media/junk-email-reporting-junk-folder-ribbon.png)

  ![Signaler le courrier indésirable ou le hameçonnage en cliquant avec le bouton droit dans le dossier Courrier indésirable](../../media/junk-email-reporting-junk-folder-right-click.png)

  ![Signaler plusieurs messages électroniques non indésirables ou de hameçonnage en cliquant avec le bouton droit dans le dossier Courrier indésirable](../../media/junk-email-reporting-junk-folder-right-click-multiple.png)

## <a name="uninstall-the-junk-email-reporting-add-in"></a><span data-ttu-id="a6576-205">Désinstallation du complément Junk Email Reporting</span><span class="sxs-lookup"><span data-stu-id="a6576-205">Uninstall the Junk Email Reporting Add-in</span></span>

<span data-ttu-id="a6576-206">Après avoir fermé Outlook, utilisez l’une des procédures suivantes pour désinstaller le add-in Junk Email Reporting :</span><span class="sxs-lookup"><span data-stu-id="a6576-206">After you close Outlook, use any of the following procedures to uninstall the Junk Email Reporting Add-in:</span></span>

- <span data-ttu-id="a6576-207">**Panneau de commande**: appuyez sur la touche Windows + R. Dans la **boîte de** dialogue Exécuter qui s’ouvre, `control appwiz.cpl` entrez, puis cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="a6576-207">**Control Panel**: Press the Windows key + R. In the **Run** dialog that opens, enter `control appwiz.cpl` and then click **OK**.</span></span>

  <span data-ttu-id="a6576-208">Recherchez et **sélectionnez le** module de rapport de courrier indésirable Microsoft dans la liste, puis cliquez sur **Désinstaller.**</span><span class="sxs-lookup"><span data-stu-id="a6576-208">Find and select **Microsoft Junk Email Reporting Add-in** in the list, and then click **Uninstall**.</span></span>

- <span data-ttu-id="a6576-209">**Package Windows Installer**: recherchez ou téléchargez le fichier .msi approprié, puis double-cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="a6576-209">**Windows Installer package**: Find or download the appropriate .msi file, and double-click on it.</span></span>

  - <span data-ttu-id="a6576-210">**32 bits**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi`</span><span class="sxs-lookup"><span data-stu-id="a6576-210">**32-bit**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi`</span></span>

  - <span data-ttu-id="a6576-211">**64 bits**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi`</span><span class="sxs-lookup"><span data-stu-id="a6576-211">**64-bit**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi`</span></span>

  <span data-ttu-id="a6576-212">Dans la boîte de dialogue qui s’affiche, sélectionnez Supprimer le **add-in** De rapport de courrier indésirable Microsoft pour Outlook, puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="a6576-212">In the dialog that appears, select **Remove Microsoft Junk Email Reporting Add-in for Outlook** and then click **Next**.</span></span>

- <span data-ttu-id="a6576-213">**Mode silencieux**: recherchez ou téléchargez le fichier .msi approprié.</span><span class="sxs-lookup"><span data-stu-id="a6576-213">**Silent Mode**: Find or download the appropriate .msi file.</span></span> <span data-ttu-id="a6576-214">Dans une fenêtre d’invite de commandes, remplacez-la par l’emplacement du fichier .msi et exécutez l’une \<PathToFile\> des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6576-214">In a Command Prompt window, replace \<PathToFile\> with the location of the .msi file, and run one of the following commands:</span></span>

  - <span data-ttu-id="a6576-215">**32 bits**:</span><span class="sxs-lookup"><span data-stu-id="a6576-215">**32-bit**:</span></span>

    ```dos
    msiexec /x "<PathToFile>\Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi" /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"
    ```

  - <span data-ttu-id="a6576-216">**64 bits**:</span><span class="sxs-lookup"><span data-stu-id="a6576-216">**64-bit**:</span></span>

    ```dos
    msiexec /x "<PathToFile>\Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi" /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"
    ```

<span data-ttu-id="a6576-217">Lorsque vous ouvrez Outlook après la désinstallation, les options de signalement du courrier indésirable, et non du courrier indésirable et du hameçonnage doivent avoir disparu.</span><span class="sxs-lookup"><span data-stu-id="a6576-217">When you open Outlook after the uninstall, the junk, not junk, and phishing reporting options should be gone.</span></span>

## <a name="troubleshooting-the-junk-email-reporting-add-in"></a><span data-ttu-id="a6576-218">Résolution des problèmes du add-in Junk Email Reporting</span><span class="sxs-lookup"><span data-stu-id="a6576-218">Troubleshooting the Junk Email Reporting add-in</span></span>

<span data-ttu-id="a6576-219">Parfois, vous pouvez avoir des difficultés avec Outlook après avoir ajouté le add-in Junk Email Reporting.</span><span class="sxs-lookup"><span data-stu-id="a6576-219">Occasionally, you might experience trouble with Outlook after adding the Junk Email Reporting Add-In.</span></span> <span data-ttu-id="a6576-220">Cette section décrit les problèmes que vous pouvez rencontrer, ainsi que des conseils pour résoudre ces problèmes.</span><span class="sxs-lookup"><span data-stu-id="a6576-220">This section describes problems that you might encounter, along with tips for resolving these issues.</span></span>

### <a name="troubleshooting-for-users"></a><span data-ttu-id="a6576-221">Résolution des problèmes pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a6576-221">Troubleshooting for users</span></span>

<span data-ttu-id="a6576-222">Vous devez faire l’expérience d’un ou de plusieurs des problèmes suivants :</span><span class="sxs-lookup"><span data-stu-id="a6576-222">You experience one or more of the following problems:</span></span>

- <span data-ttu-id="a6576-223">Rien ne se passe quand vous cliquez sur **Signaler le courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="a6576-223">Nothing happens when you click **Report Junk**</span></span>
- <span data-ttu-id="a6576-224">Outlook cesse de répondre après avoir sélectionné un message électronique</span><span class="sxs-lookup"><span data-stu-id="a6576-224">Outlook stops responding after you select an email message</span></span>
- <span data-ttu-id="a6576-225">Le courrier indésirable signalé ne peut pas être remis en raison d'une réponse « Non remis ».</span><span class="sxs-lookup"><span data-stu-id="a6576-225">Reported junk mail cannot be delivered due to an "undeliverable" reply</span></span>

<span data-ttu-id="a6576-226">Pour résoudre ce problème, faites les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6576-226">To fix this problem, do the following steps:</span></span>

1. <span data-ttu-id="a6576-227">Fermez et redémarrez Outlook.</span><span class="sxs-lookup"><span data-stu-id="a6576-227">Close and restart Outlook.</span></span>
2. <span data-ttu-id="a6576-228">Créez et envoyez un message de test, puis vérifiez que le destinataire a reçu le message.</span><span class="sxs-lookup"><span data-stu-id="a6576-228">Create and send a test message, and verify that the recipient received the message.</span></span>
3. <span data-ttu-id="a6576-229">Si le problème persiste, contactez votre administrateur.</span><span class="sxs-lookup"><span data-stu-id="a6576-229">If the problem persists, contact your admin.</span></span>

<span data-ttu-id="a6576-230">Pour d’autres méthodes que vous pouvez utiliser pour envoyer des messages à Microsoft, voir [Signaler les messages et les fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="a6576-230">For other methods that you can use to submit messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

### <a name="troubleshooting-for-admins"></a><span data-ttu-id="a6576-231">Résolution des problèmes pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="a6576-231">Troubleshooting for admins</span></span>

#### <a name="problem-an-error-message-continually-appears-that-asks-users-to-contact-their-system-administrator"></a><span data-ttu-id="a6576-232">Problème : un message d’erreur s’affiche en permanence pour demander aux utilisateurs de contacter leur administrateur système</span><span class="sxs-lookup"><span data-stu-id="a6576-232">Problem: An error message continually appears that asks users to contact their system administrator</span></span>

1. <span data-ttu-id="a6576-233">Vérifiez ou définissez `LoggingLevel` la clé de Registre sur la valeur « Verbose » :</span><span class="sxs-lookup"><span data-stu-id="a6576-233">Verify or set the `LoggingLevel` registry key to the value "Verbose":</span></span>

   - <span data-ttu-id="a6576-234">**Outlook 32 bits sur Windows 32 bits**:</span><span class="sxs-lookup"><span data-stu-id="a6576-234">**32-bit Outlook on 32-bit Windows**:</span></span>

     ```text
     Windows Registry Editor Version 5.00

     [HKEY_LOCAL_MACHINE\Software\Microsoft\Junk Email Reporting\Addins]
     "LoggingLevel"="Verbose"
     ```

   - <span data-ttu-id="a6576-235">**Outlook 32 bits sur Windows 64 bits**:</span><span class="sxs-lookup"><span data-stu-id="a6576-235">**32-bit Outlook on 64-bit Windows**:</span></span>

     ```text
     Windows Registry Editor Version 5.00

     [HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Junk Email Reporting\Addins]
     "LoggingLevel"="Verbose"
     ```

   - <span data-ttu-id="a6576-236">**Outlook 64 bits**:</span><span class="sxs-lookup"><span data-stu-id="a6576-236">**64-bit Outlook**:</span></span>

     ```text
     Windows Registry Editor Version 5.00

     [HKEY_LOCAL_MACHINE\Software\Microsoft\Junk E-mail Reporting\Addins]
     "LoggingLevel"="Verbose"
     ```

2. <span data-ttu-id="a6576-237">Redémarrez Outlook et demandez aux utilisateurs de les signaler lorsqu’ils voient le message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a6576-237">Restart Outlook and ask users to report back when they see the error message.</span></span>

3. <span data-ttu-id="a6576-238">Collectez les informations de journal se trouvant à l'emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="a6576-238">Collect the log information found at the following location:</span></span>

   `%LOCALAPPDATA%\Microsoft\Junk Email Reporting Add-in\SpamReporterAddinLog.txt`

4. <span data-ttu-id="a6576-239">Contactez les techniciens du support Exchange Online Protection et fournissez-leur les informations du journal.</span><span class="sxs-lookup"><span data-stu-id="a6576-239">Contact Exchange Online Protection Technical Support and provide them with the log information.</span></span>

#### <a name="problem-users-selected-not-to-receive-a-confirmation-prompt-when-they-report-messages-and-now-they-want-the-prompt-back"></a><span data-ttu-id="a6576-240">Problème : les utilisateurs ont choisi de ne pas recevoir d’invite de confirmation lorsqu’ils signalaient des messages, et veulent maintenant que l’invite soit de nouveau</span><span class="sxs-lookup"><span data-stu-id="a6576-240">Problem: Users selected not to receive a confirmation prompt when they report messages, and now they want the prompt back</span></span>

1. <span data-ttu-id="a6576-241">Créez `ConfirmReportJunk` la clé de Registre avec la valeur « True » :</span><span class="sxs-lookup"><span data-stu-id="a6576-241">Create the `ConfirmReportJunk`registry key with the value "True":</span></span>

   ```text
   Windows Registry Editor Version 5.00

   HKEY_CURRENT_USER\Software\Microsoft\Junk E-mail Reporting\Preferences]
   "ConfirmReportJunk"="True"
   ```

2. <span data-ttu-id="a6576-242">Redémarrez Outlook.</span><span class="sxs-lookup"><span data-stu-id="a6576-242">Restart Outlook.</span></span>
