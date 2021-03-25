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
ms.openlocfilehash: e120ceec355ffc135e00e13a89a0f29085946a3b
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204238"
---
# <a name="install-and-use-the-junk-email-reporting-add-in-for-microsoft-outlook"></a><span data-ttu-id="b757e-103">Installer et utiliser le add-in Junk Email Reporting pour Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="b757e-103">Install and use the Junk Email Reporting add-in for Microsoft Outlook</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="b757e-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b757e-104">**Applies to**</span></span>
- [<span data-ttu-id="b757e-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="b757e-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="b757e-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="b757e-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="b757e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b757e-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

> [!NOTE]
> <span data-ttu-id="b757e-108">Si vous n’utilisez pas actuellement le add-in Junk [](enable-the-report-message-add-in.md) E-mail Reporting, [](enable-the-report-phish-add-in.md) nous vous recommandons plutôt de le signaler ou de le signaler comme hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="b757e-108">If you aren't currently using the Junk E-mail Reporting add-in, we recommend the [Report Message add-in](enable-the-report-message-add-in.md) or the [Report Phishing add-in](enable-the-report-phish-add-in.md) instead.</span></span> <span data-ttu-id="b757e-109">Pour plus d’informations, voir [Signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="b757e-109">For more information, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

<span data-ttu-id="b757e-110">Le add-in Junk Email Reporting pour Microsoft Outlook permet aux utilisateurs de soumettre des faux positifs (courrier électronique de qualité marqué comme courrier indésirable), des faux négatifs (courrier indésirable autorisé) et des messages de hameçonnage à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b757e-110">The Junk Email Reporting Add-in for Microsoft Outlook allows users to submit false positives (good email marked as spam), false negatives (bad email allowed) and phishing messages to Microsoft.</span></span> <span data-ttu-id="b757e-111">Si votre organisation n’utilise pas Exchange Online Protection (par exemple, Exchange local ou des services de messagerie autres qu’Exchange Online), l’envoi de votre rapport de courrier indésirable n’affecte pas votre filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="b757e-111">If your organization doesn't use Exchange Online Protection (for example, on-premises Exchange or email services other than Exchange Online), your junk email report submission will not affect your spam filtering.</span></span>

<span data-ttu-id="b757e-112">Cette rubrique explique comment installer et utiliser le add-in Junk Email Reporting.</span><span class="sxs-lookup"><span data-stu-id="b757e-112">This topic explains how to install and use the Junk Email Reporting add-in.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="b757e-113">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b757e-113">What do you need to know before you begin?</span></span>

- <span data-ttu-id="b757e-114">Pour installer le add-in Junk Email Reporting, consultez la section Installer le [add-in Junk Email Reporting](#install-the-junk-email-reporting-add-in) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="b757e-114">To install the Junk Email Reporting add-in, see the [Install the Junk Email Reporting add-in](#install-the-junk-email-reporting-add-in) section later in this article.</span></span>

- <span data-ttu-id="b757e-115">Le add-in Junk Email Reporting fonctionne avec les versions suivantes d’Outlook :</span><span class="sxs-lookup"><span data-stu-id="b757e-115">The Junk Email Reporting add-in works with the following versions of Outlook:</span></span>

  - <span data-ttu-id="b757e-116">Outlook 2013 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b757e-116">Outlook 2013 or later</span></span>
  - <span data-ttu-id="b757e-117">Outlook inclus avec Microsoft 365 Apps for enterprise</span><span class="sxs-lookup"><span data-stu-id="b757e-117">Outlook included with Microsoft 365 Apps for enterprise</span></span>

- <span data-ttu-id="b757e-118">Pour plus d’informations sur la notification des messages à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="b757e-118">For more information about reporting messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="use-the-junk-email-reporting-add-in-to-report-spam-and-phishing-messages"></a><span data-ttu-id="b757e-119">Utiliser le add-in Junk Email Reporting (Signalement du courrier indésirable) pour signaler les messages de courrier indésirable et de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b757e-119">Use the Junk Email Reporting add-in to report spam and phishing messages</span></span>

1. <span data-ttu-id="b757e-120">Pour les messages dans la boîte de réception ou tout autre dossier de courrier électronique à l’exception du courrier indésirable, utilisez l’une des méthodes suivantes pour signaler le courrier indésirable et les messages de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="b757e-120">For messages in the Inbox or any other email folder except Junk Email, use any of the following methods to report spam and phishing messages:</span></span>

   - <span data-ttu-id="b757e-121">Sélectionnez le message ou ouvrez-le.</span><span class="sxs-lookup"><span data-stu-id="b757e-121">Select the message or open the message.</span></span> <span data-ttu-id="b757e-122">Dans **l’onglet** Accueil **ou Message** du ruban,  cliquez sur Courrier **indésirable,** puis sélectionnez Signaler comme courrier indésirable ou Signaler **comme hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="b757e-122">In the **Home** or **Message** tab in the ribbon, click **Junk**, and then select **Report as Junk** or **Report as Phishing**.</span></span>

     ![Signaler le courrier indésirable ou le hameçonnage à partir du ruban](../../media/junk-email-reporting-ribbon.png)

   - <span data-ttu-id="b757e-124">Cliquez avec le bouton droit sur le  message, **sélectionnez** Courrier indésirable, puis sélectionnez Signaler comme courrier indésirable **ou Signaler comme hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="b757e-124">Right-click on the message, select **Junk**, and then select **Report as Junk** or **Report as Phishing**.</span></span>

     ![Signaler le courrier indésirable ou le hameçonnage à partir du clic droit](../../media/junk-email-reporting-right-click.png)

   - <span data-ttu-id="b757e-126">Sélectionnez plusieurs messages, cliquez avec le bouton droit, puis sélectionnez **Signaler comme** courrier indésirable ou Signaler **comme hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="b757e-126">Select multiple messages, right-click, and then select **Report as Junk** or **Report as Phishing**.</span></span>

     ![Signaler plusieurs messages électroniques de courrier indésirable ou de hameçonnage à partir du clic droit](../../media/junk-email-reporting-right-click-multiple.png)

2. <span data-ttu-id="b757e-128">Dans la boîte de dialogue qui s’affiche, lisez les informations et cliquez sur **Rapport.**</span><span class="sxs-lookup"><span data-stu-id="b757e-128">In the dialog that appears, read the information and click **Report**.</span></span> <span data-ttu-id="b757e-129">Si vous changez d’avis, cliquez sur **Ne pas signaler.**</span><span class="sxs-lookup"><span data-stu-id="b757e-129">If you change your mind, click **Don't Report**.</span></span>

   ![Boîte de dialogue Signaler comme courrier indésirable](../../media/junk-email-reporting-report-as-junk-dialog.png)

   ![Boîte de dialogue Signaler comme hameçonnage](../../media/junk-email-reporting-report-as-phishing-dialog.png)

3. <span data-ttu-id="b757e-132">Les messages sélectionnés sont envoyés à Microsoft pour analyse et :</span><span class="sxs-lookup"><span data-stu-id="b757e-132">The selected messages will be sent to Microsoft for analysis and:</span></span>

   - <span data-ttu-id="b757e-133">Déplacé vers le dossier Courrier indésirable s’il a été signalé comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="b757e-133">Moved to the Junk Email folder if it was reported as spam.</span></span>
   - <span data-ttu-id="b757e-134">Supprimé s’il a été signalé comme hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="b757e-134">Deleted if it was reported as phishing.</span></span>

   <span data-ttu-id="b757e-135">Pour confirmer que les messages ont été envoyés, ouvrez le dossier **Éléments envoyés** pour afficher les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="b757e-135">To confirm that the messages have been submitted, open your **Sent Items** folder to view the submitted messages.</span></span>

## <a name="use-the-junk-email-reporting-add-in-to-report-non-spam-and-phishing-messages-from-the-junk-email-folder"></a><span data-ttu-id="b757e-136">Utiliser le add-in Junk Email Reporting (Signalement du courrier indésirable) pour signaler les messages de courrier non indésirable et de hameçonnage à partir du dossier Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="b757e-136">Use the Junk Email Reporting add-in to report non-spam and phishing messages from the Junk Email folder</span></span>

1. <span data-ttu-id="b757e-137">Dans le dossier Courrier indésirable, utilisez l’une des méthodes suivantes pour signaler les faux positifs du courrier indésirable ou les messages de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="b757e-137">In the Junk Email folder, use any of the following methods to report spam false positives or phishing messages:</span></span>

   - <span data-ttu-id="b757e-138">Sélectionnez le message ou ouvrez-le.</span><span class="sxs-lookup"><span data-stu-id="b757e-138">Select the message or open the message.</span></span> <span data-ttu-id="b757e-139">Dans **l’onglet** Accueil ou **Message** du ruban,  cliquez sur Ne pas courrier **indésirable,** puis sélectionnez Signaler comme courrier non indésirable ou Signaler **comme hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="b757e-139">In the **Home** or **Message** tab in the ribbon, click **Not Junk**, and then select **Report as Not Junk** or **Report as Phishing**.</span></span>

     ![Signaler le courrier indésirable ou le hameçonnage à partir du ruban dans le dossier Courrier indésirable](../../media/junk-email-reporting-junk-folder-ribbon.png)

   - <span data-ttu-id="b757e-141">Cliquez avec le bouton droit sur le  message, **cliquez** sur Courrier indésirable, puis sélectionnez Signaler comme courrier non indésirable ou Signaler **comme hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="b757e-141">Right-click on the message, click **Junk**, and then select **Report as Not Junk** or **Report as Phishing**.</span></span>

     ![Signaler le courrier indésirable ou le hameçonnage en cliquant avec le bouton droit dans le dossier Courrier indésirable](../../media/junk-email-reporting-junk-folder-right-click.png)

   - <span data-ttu-id="b757e-143">Sélectionnez plusieurs messages, cliquez avec le bouton droit, puis sélectionnez **Signaler comme** courrier non indésirable ou Signaler **comme hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="b757e-143">Select multiple messages, right-click, and then select **Report as Not Junk** or **Report as Phishing**.</span></span>

     ![Signaler plusieurs messages électroniques non indésirables ou de hameçonnage en cliquant avec le bouton droit dans le dossier Courrier indésirable](../../media/junk-email-reporting-junk-folder-right-click-multiple.png)

2. <span data-ttu-id="b757e-145">Dans la boîte de dialogue qui s’affiche, lisez les informations et cliquez sur **Rapport.**</span><span class="sxs-lookup"><span data-stu-id="b757e-145">In the dialog that appears, read the information and click **Report**.</span></span> <span data-ttu-id="b757e-146">Si vous changez d’avis, cliquez sur **Ne pas signaler.**</span><span class="sxs-lookup"><span data-stu-id="b757e-146">If you change your mind, click **Don't Report**.</span></span>

   ![Boîte de dialogue Signaler comme courrier indésirable](../../media/junk-email-reporting-report-as-not-junk-dialog.png)

   ![Boîte de dialogue Signaler comme hameçonnage](../../media/junk-email-reporting-report-as-phishing-dialog.png)

3. <span data-ttu-id="b757e-149">Les messages sélectionnés sont envoyés à Microsoft pour analyse et :</span><span class="sxs-lookup"><span data-stu-id="b757e-149">The selected messages will be sent to Microsoft for analysis and:</span></span>

   - <span data-ttu-id="b757e-150">Déplacé vers le dossier Courrier indésirable s’il a été signalé comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="b757e-150">Moved to the Junk Email folder if it was reported as spam.</span></span>
   - <span data-ttu-id="b757e-151">Supprimé s’il a été signalé comme hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="b757e-151">Deleted if it was reported as phishing.</span></span>

   <span data-ttu-id="b757e-152">Pour confirmer que les messages ont été envoyés, ouvrez le dossier **Éléments envoyés** pour afficher les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="b757e-152">To confirm that the messages have been submitted, open your **Sent Items** folder to view the submitted messages.</span></span>

## <a name="install-the-junk-email-reporting-add-in"></a><span data-ttu-id="b757e-153">Installer le add-in Junk Email Reporting</span><span class="sxs-lookup"><span data-stu-id="b757e-153">Install the Junk Email Reporting add-in</span></span>

- <span data-ttu-id="b757e-154">Vous devez avoir des privilèges d’administrateur sur l’ordinateur sur lequel vous installez le module.</span><span class="sxs-lookup"><span data-stu-id="b757e-154">You need to have administrator privileges on the computer where you're installing the add-in.</span></span>

- <span data-ttu-id="b757e-155">Go to <https://www.microsoft.com/download/details.aspx?id=18275> and download the appropriate .msi file for your version of Office to a location that’s easy to find:</span><span class="sxs-lookup"><span data-stu-id="b757e-155">Go to <https://www.microsoft.com/download/details.aspx?id=18275> and download the appropriate .msi file for your version of Office to a location that's easy to find:</span></span>

  - <span data-ttu-id="b757e-156">**32 bits**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi`</span><span class="sxs-lookup"><span data-stu-id="b757e-156">**32-bit**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi`</span></span>
  - <span data-ttu-id="b757e-157">**64 bits**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi`</span><span class="sxs-lookup"><span data-stu-id="b757e-157">**64-bit**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi`</span></span>

- <span data-ttu-id="b757e-158">Pour Outlook 2013 ou une ultérieure, le seul prérequis est Microsoft .NET Framework 2.0.</span><span class="sxs-lookup"><span data-stu-id="b757e-158">For Outlook 2013 or later, the only prerequisite is the Microsoft .NET Framework 2.0.</span></span> <span data-ttu-id="b757e-159">Dans Windows 10, vous n’installez pas .NET Framework 2.0 à partir d’un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="b757e-159">In Windows 10, you don't install the .NET Framework 2.0 from a download.</span></span>

### <a name="install-the-junk-email-reporting-add-in-using-the-setup-wizard"></a><span data-ttu-id="b757e-160">Installer le add-in Junk Email Reporting à l’aide de l’Assistant Installation</span><span class="sxs-lookup"><span data-stu-id="b757e-160">Install the Junk Email Reporting Add-in using the Setup wizard</span></span>

1. <span data-ttu-id="b757e-161">Sur votre ordinateur, fermez Outlook.</span><span class="sxs-lookup"><span data-stu-id="b757e-161">On your computer, close Outlook.</span></span>

2. <span data-ttu-id="b757e-162">Dans Windows 10, vérifiez que .NET Framework 2.0 est activé.</span><span class="sxs-lookup"><span data-stu-id="b757e-162">In Windows 10, verify the .NET Framework 2.0 is enabled.</span></span> <span data-ttu-id="b757e-163">Pour obtenir des instructions, voir [Activer la .NET Framework 3.5 dans le Panneau de contrôle.](/dotnet/framework/install/dotnet-35-windows-10#enable-the-net-framework-35-in-control-panel)</span><span class="sxs-lookup"><span data-stu-id="b757e-163">For instructions, see [Enable the .NET Framework 3.5 in Control Panel](/dotnet/framework/install/dotnet-35-windows-10#enable-the-net-framework-35-in-control-panel).</span></span>

3. <span data-ttu-id="b757e-164">Recherchez le fichier .msi que vous avez téléchargé et double-cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="b757e-164">Locate the .msi file you downloaded and double-click on it.</span></span>

4. <span data-ttu-id="b757e-165">Dans la page **Bienvenue à la configuration du complément Microsoft Junk Email Reporting**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b757e-165">On the **Welcome to Microsoft Junk Email Reporting Add-in Setup** page, click **Next**.</span></span>

5. <span data-ttu-id="b757e-166">Examinez le contrat de licence, cliquez **sur J’accepte** les termes du contrat de licence si vous acceptez les termes, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b757e-166">Review the license agreement, click **I accept the terms in the License Agreement** if you agree to the terms, and then click **Next**.</span></span>

6. <span data-ttu-id="b757e-167">Une fois l'exécution de l'Assistant terminée, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="b757e-167">When the wizard is complete, click **Finish**.</span></span>

<span data-ttu-id="b757e-168">Lancez Outlook.</span><span class="sxs-lookup"><span data-stu-id="b757e-168">Start Outlook.</span></span>

<span data-ttu-id="b757e-p109">Consultez le bouton **Courrier indésirable** sur votre ruban Outlook. Vous pouvez à présent signaler des messages de courrier indésirable à Microsoft en les sélectionnant dans votre boîte de réception, puis en cliquant sur le bouton permettant de **signaler le courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="b757e-p109">Look for the **Junk** button on your Outlook ribbon. You can now report junk email messages to Microsoft by selecting the junk email messages in your Inbox and clicking the **Report Junk** button.</span></span>

<span data-ttu-id="b757e-p110">Cliquez sur la flèche vers le bas en regard du bouton **Courrier indésirable** pour plus d'options, telles que le **signalement en tant que hameçonnage** si vous souhaitez signaler des messages électroniques d'hameçonnage à Microsoft. Dans votre dossier de courrier indésirable, vous pouvez également sélectionner l'option de **signalement en tant que courrier non indésirable** si un message électronique a été identifié à tort comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="b757e-p110">Choose the down arrow next to **Junk** for more options such as **Report as Phishing** if you want to report phishing scam emails to Microsoft. In your junk mail folder, you can also select, **Report not junk** if an email was incorrectly identified as junk mail.</span></span>

### <a name="install-the-junk-email-reporting-add-in-using-silent-mode"></a><span data-ttu-id="b757e-173">Installation du complément de création de rapports de courrier indésirable en mode sans assistance</span><span class="sxs-lookup"><span data-stu-id="b757e-173">Install the Junk Email Reporting Add-In using Silent Mode</span></span>

1. <span data-ttu-id="b757e-174">Sur votre ordinateur, fermez Outlook.</span><span class="sxs-lookup"><span data-stu-id="b757e-174">On your computer, close Outlook.</span></span>

2. <span data-ttu-id="b757e-175">Dans Windows 10, installez .NET Framework 2.0 en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b757e-175">In Windows 10, install the .NET Framework 2.0 by running the following command:</span></span>

   ```dos
   DISM /Online /Enable-Feature /FeatureName:NetFx3 /All
   ```

3. <span data-ttu-id="b757e-176">Pour installer le module sans intervention de l’utilisateur, ouvrez une invite de commandes et utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b757e-176">To install the add-in without any user interaction, open a Command Prompt and use the following syntax:</span></span>

   ```dos
   msiexec /qn /i "<PathToMSIFile>\<MSIFile>" [MaxMessageSelection=<1-50>] [BccEmailAddress="<EmailAddress1>; <EmailAddress2>"...]
   ```

   - <span data-ttu-id="b757e-177">`MaxMessageSelection` spécifie le nombre maximal de messages que vous pouvez sélectionner pour une soumission unique.</span><span class="sxs-lookup"><span data-stu-id="b757e-177">`MaxMessageSelection` specifies the maximum number of messages that you can select for a single submission.</span></span> <span data-ttu-id="b757e-178">Les valeurs valides sont de 1 à 50.</span><span class="sxs-lookup"><span data-stu-id="b757e-178">Valid values are from 1 to 50.</span></span> <span data-ttu-id="b757e-179">Par défaut, la valeur 15 s’applique.</span><span class="sxs-lookup"><span data-stu-id="b757e-179">The default value is 15.</span></span>

   - <span data-ttu-id="b757e-180">`BccEmailAddress` spécifie les destinataires Bcc supplémentaires qui recevront une copie de toutes les soumissions d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b757e-180">`BccEmailAddress` specifies additional Bcc recipients who will receive a copy of all user submissions.</span></span> <span data-ttu-id="b757e-181">La valeur par défaut est vide (aucun destinataire Bcc supplémentaire).</span><span class="sxs-lookup"><span data-stu-id="b757e-181">The default value is blank (no additional Bcc recipients).</span></span>

   <span data-ttu-id="b757e-182">Cet exemple installe la version 64 bits du module à partir du chemin d’accès spécifié avec les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="b757e-182">This example installs the 64-bit version of the add-in from the specified path with the default settings.</span></span>

   ```dos
   msiexec /qn /i "C:\Downloads\Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi"
   ```

   <span data-ttu-id="b757e-183">Cet exemple installe la version 32 bits du complément à partir du chemin d’accès spécifié avec les paramètres supplémentaires suivants :</span><span class="sxs-lookup"><span data-stu-id="b757e-183">This example installs the 32-bit version of the add-in from the specified path with the following additional settings:</span></span>

   - <span data-ttu-id="b757e-184">Jusqu’à 20 messages peuvent être sélectionnés dans une seule soumission.</span><span class="sxs-lookup"><span data-stu-id="b757e-184">Up to 20 messages can be selected in a single submission.</span></span>
   - <span data-ttu-id="b757e-185">junkreports@contoso.com et hollyd@treyresearch.net recevoir des copies Bcc de toutes les soumissions.</span><span class="sxs-lookup"><span data-stu-id="b757e-185">junkreports@contoso.com and hollyd@treyresearch.net receive Bcc copies of all submissions.</span></span>

   ```dos
   msiexec /qn /i "C:\Downloads\Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi" MaxMessageSelection=20 BccEmailAddress="junkreports@contoso.com; hollyd@treyresearch.net"
   ```

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="b757e-186">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="b757e-186">How do you know this worked?</span></span>

<span data-ttu-id="b757e-187">Pour vérifier que vous avez correctement installé le service Junk Email Reporting Add-in, dans Outlook, vous devez suivre l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b757e-187">To verify that you've successfully installed the Junk Email Reporting Add-in, do the any of the following steps in Outlook:</span></span>

- <span data-ttu-id="b757e-188">Sélectionnez le message ou ouvrez-le.</span><span class="sxs-lookup"><span data-stu-id="b757e-188">Select the message or open the message.</span></span> <span data-ttu-id="b757e-189">Dans **l’onglet** Accueil **ou Message** du ruban, cliquez sur Courrier indésirable **et** vérifiez que les options suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="b757e-189">In the **Home** or **Message** tab in the ribbon, click **Junk**, and verify that the following options are available:</span></span>

  - <span data-ttu-id="b757e-190">**Signaler comme courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="b757e-190">**Report as Junk**</span></span>
  - <span data-ttu-id="b757e-191">**Signaler comme hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="b757e-191">**Report as Phishing**</span></span>
  - <span data-ttu-id="b757e-192">**Options de signalement du courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="b757e-192">**Junk Reporting Options**</span></span>
  - <span data-ttu-id="b757e-193">**Signaler l’aide de Junk Online**</span><span class="sxs-lookup"><span data-stu-id="b757e-193">**Report Junk Online Help**</span></span>

  ![Signaler le courrier indésirable ou le hameçonnage à partir du ruban](../../media/junk-email-reporting-ribbon.png)

- <span data-ttu-id="b757e-195">Cliquez avec le bouton droit sur le message, sélectionnez **Courrier** indésirable et vérifiez que les options suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="b757e-195">Right-click on the message, select **Junk**, and verify that the following options are available:</span></span>

  - <span data-ttu-id="b757e-196">**Signaler comme courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="b757e-196">**Report as Junk**</span></span>
  - <span data-ttu-id="b757e-197">**Signaler comme hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="b757e-197">**Report as Phishing**</span></span>
  - <span data-ttu-id="b757e-198">**Options de signalement du courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="b757e-198">**Junk Reporting Options**</span></span>
  - <span data-ttu-id="b757e-199">**Signaler l’aide de Junk Online**</span><span class="sxs-lookup"><span data-stu-id="b757e-199">**Report Junk Online Help**</span></span>

  ![Signaler le courrier indésirable ou le hameçonnage à partir du clic droit](../../media/junk-email-reporting-right-click.png)

- <span data-ttu-id="b757e-201">Sélectionnez plusieurs messages, cliquez avec le bouton droit et vérifiez que les options suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="b757e-201">Select multiple messages, right click, and verify that the following options are available:</span></span>

  - <span data-ttu-id="b757e-202">**Signaler comme courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="b757e-202">**Report as Junk**</span></span>
  - <span data-ttu-id="b757e-203">**Signaler comme hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="b757e-203">**Report as Phishing**</span></span>

  ![Signaler plusieurs messages électroniques de courrier indésirable ou de hameçonnage à partir du clic droit](../../media/junk-email-reporting-right-click-multiple.png)

- <span data-ttu-id="b757e-205">Faites les actions précédentes dans le **dossier Courrier** indésirable et vérifiez que les options **de** signalement de courrier indésirable précédentes sont désormais **non** indésirables.</span><span class="sxs-lookup"><span data-stu-id="b757e-205">Do the previous actions in the **Junk Email** folder and verify the previous **Junk** reporting options are now **Not Junk**.</span></span>

  ![Signaler le courrier indésirable ou le hameçonnage à partir du ruban dans le dossier Courrier indésirable](../../media/junk-email-reporting-junk-folder-ribbon.png)

  ![Signaler le courrier indésirable ou le hameçonnage en cliquant avec le bouton droit dans le dossier Courrier indésirable](../../media/junk-email-reporting-junk-folder-right-click.png)

  ![Signaler plusieurs messages électroniques non indésirables ou de hameçonnage en cliquant avec le bouton droit dans le dossier Courrier indésirable](../../media/junk-email-reporting-junk-folder-right-click-multiple.png)

## <a name="uninstall-the-junk-email-reporting-add-in"></a><span data-ttu-id="b757e-209">Désinstallation du complément Junk Email Reporting</span><span class="sxs-lookup"><span data-stu-id="b757e-209">Uninstall the Junk Email Reporting Add-in</span></span>

<span data-ttu-id="b757e-210">Après avoir fermé Outlook, utilisez l’une des procédures suivantes pour désinstaller le add-in Junk Email Reporting :</span><span class="sxs-lookup"><span data-stu-id="b757e-210">After you close Outlook, use any of the following procedures to uninstall the Junk Email Reporting Add-in:</span></span>

- <span data-ttu-id="b757e-211">**Panneau de commande**: appuyez sur la touche Windows + R. Dans la **boîte de** dialogue Exécuter qui s’ouvre, `control appwiz.cpl` entrez, puis cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="b757e-211">**Control Panel**: Press the Windows key + R. In the **Run** dialog that opens, enter `control appwiz.cpl` and then click **OK**.</span></span>

  <span data-ttu-id="b757e-212">Recherchez et **sélectionnez le** module de rapport de courrier indésirable Microsoft dans la liste, puis cliquez sur **Désinstaller.**</span><span class="sxs-lookup"><span data-stu-id="b757e-212">Find and select **Microsoft Junk Email Reporting Add-in** in the list, and then click **Uninstall**.</span></span>

- <span data-ttu-id="b757e-213">**Package Windows Installer**: recherchez ou téléchargez le fichier .msi approprié, puis double-cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="b757e-213">**Windows Installer package**: Find or download the appropriate .msi file, and double-click on it.</span></span>

  - <span data-ttu-id="b757e-214">**32 bits**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi`</span><span class="sxs-lookup"><span data-stu-id="b757e-214">**32-bit**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi`</span></span>

  - <span data-ttu-id="b757e-215">**64 bits**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi`</span><span class="sxs-lookup"><span data-stu-id="b757e-215">**64-bit**: `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi`</span></span>

  <span data-ttu-id="b757e-216">Dans la boîte de dialogue qui s’affiche, **sélectionnez Supprimer** le nouveau rapport de courrier indésirable Microsoft pour Outlook, puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="b757e-216">In the dialog that appears, select **Remove Microsoft Junk Email Reporting Add-in for Outlook** and then click **Next**.</span></span>

- <span data-ttu-id="b757e-217">**Mode silencieux**: recherchez ou téléchargez le fichier .msi approprié.</span><span class="sxs-lookup"><span data-stu-id="b757e-217">**Silent Mode**: Find or download the appropriate .msi file.</span></span> <span data-ttu-id="b757e-218">Dans une fenêtre d’invite de commandes, remplacez-la par l’emplacement du fichier .msi et exécutez l’une \<PathToFile\> des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b757e-218">In a Command Prompt window, replace \<PathToFile\> with the location of the .msi file, and run one of the following commands:</span></span>

  - <span data-ttu-id="b757e-219">**32 bits**:</span><span class="sxs-lookup"><span data-stu-id="b757e-219">**32-bit**:</span></span>

    ```dos
    msiexec /x "<PathToFile>\Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi" /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"
    ```

  - <span data-ttu-id="b757e-220">**64 bits**:</span><span class="sxs-lookup"><span data-stu-id="b757e-220">**64-bit**:</span></span>

    ```dos
    msiexec /x "<PathToFile>\Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi" /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"
    ```

<span data-ttu-id="b757e-221">Lorsque vous ouvrez Outlook après la désinstallation, les options de signalement du courrier indésirable, et non du courrier indésirable et du hameçonnage doivent avoir disparu.</span><span class="sxs-lookup"><span data-stu-id="b757e-221">When you open Outlook after the uninstall, the junk, not junk, and phishing reporting options should be gone.</span></span>

## <a name="troubleshooting-the-junk-email-reporting-add-in"></a><span data-ttu-id="b757e-222">Résolution des problèmes du add-in Junk Email Reporting</span><span class="sxs-lookup"><span data-stu-id="b757e-222">Troubleshooting the Junk Email Reporting add-in</span></span>

<span data-ttu-id="b757e-223">Parfois, vous pouvez avoir des difficultés avec Outlook après avoir ajouté le add-in Junk Email Reporting.</span><span class="sxs-lookup"><span data-stu-id="b757e-223">Occasionally, you might experience trouble with Outlook after adding the Junk Email Reporting Add-In.</span></span> <span data-ttu-id="b757e-224">Cette section décrit les problèmes que vous pouvez rencontrer, ainsi que des conseils pour résoudre ces problèmes.</span><span class="sxs-lookup"><span data-stu-id="b757e-224">This section describes problems that you might encounter, along with tips for resolving these issues.</span></span>

### <a name="troubleshooting-for-users"></a><span data-ttu-id="b757e-225">Résolution des problèmes pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="b757e-225">Troubleshooting for users</span></span>

<span data-ttu-id="b757e-226">Vous devez faire l’expérience d’un ou de plusieurs des problèmes suivants :</span><span class="sxs-lookup"><span data-stu-id="b757e-226">You experience one or more of the following problems:</span></span>

- <span data-ttu-id="b757e-227">Rien ne se passe quand vous cliquez sur **Signaler le courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="b757e-227">Nothing happens when you click **Report Junk**</span></span>
- <span data-ttu-id="b757e-228">Outlook cesse de répondre après avoir sélectionné un message électronique</span><span class="sxs-lookup"><span data-stu-id="b757e-228">Outlook stops responding after you select an email message</span></span>
- <span data-ttu-id="b757e-229">Le courrier indésirable signalé ne peut pas être remis en raison d'une réponse « Non remis ».</span><span class="sxs-lookup"><span data-stu-id="b757e-229">Reported junk mail cannot be delivered due to an "undeliverable" reply</span></span>

<span data-ttu-id="b757e-230">Pour résoudre ce problème, faites les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b757e-230">To fix this problem, do the following steps:</span></span>

1. <span data-ttu-id="b757e-231">Fermez et redémarrez Outlook.</span><span class="sxs-lookup"><span data-stu-id="b757e-231">Close and restart Outlook.</span></span>
2. <span data-ttu-id="b757e-232">Créez et envoyez un message de test, puis vérifiez que le destinataire a reçu le message.</span><span class="sxs-lookup"><span data-stu-id="b757e-232">Create and send a test message, and verify that the recipient received the message.</span></span>
3. <span data-ttu-id="b757e-233">Si le problème persiste, contactez votre administrateur.</span><span class="sxs-lookup"><span data-stu-id="b757e-233">If the problem persists, contact your admin.</span></span>

<span data-ttu-id="b757e-234">Pour d’autres méthodes que vous pouvez utiliser pour envoyer des messages à Microsoft, voir Signaler les messages et [les fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="b757e-234">For other methods that you can use to submit messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

### <a name="troubleshooting-for-admins"></a><span data-ttu-id="b757e-235">Résolution des problèmes pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="b757e-235">Troubleshooting for admins</span></span>

#### <a name="problem-an-error-message-continually-appears-that-asks-users-to-contact-their-system-administrator"></a><span data-ttu-id="b757e-236">Problème : un message d’erreur s’affiche en permanence pour demander aux utilisateurs de contacter leur administrateur système</span><span class="sxs-lookup"><span data-stu-id="b757e-236">Problem: An error message continually appears that asks users to contact their system administrator</span></span>

1. <span data-ttu-id="b757e-237">Vérifiez ou définissez `LoggingLevel` la clé de Registre sur la valeur « Verbose » :</span><span class="sxs-lookup"><span data-stu-id="b757e-237">Verify or set the `LoggingLevel` registry key to the value "Verbose":</span></span>

   - <span data-ttu-id="b757e-238">**Outlook 32 bits sur Windows 32 bits**:</span><span class="sxs-lookup"><span data-stu-id="b757e-238">**32-bit Outlook on 32-bit Windows**:</span></span>

     ```text
     Windows Registry Editor Version 5.00

     [HKEY_LOCAL_MACHINE\Software\Microsoft\Junk Email Reporting\Addins]
     "LoggingLevel"="Verbose"
     ```

   - <span data-ttu-id="b757e-239">**Outlook 32 bits sur Windows 64 bits**:</span><span class="sxs-lookup"><span data-stu-id="b757e-239">**32-bit Outlook on 64-bit Windows**:</span></span>

     ```text
     Windows Registry Editor Version 5.00

     [HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Junk Email Reporting\Addins]
     "LoggingLevel"="Verbose"
     ```

   - <span data-ttu-id="b757e-240">**Outlook 64 bits**:</span><span class="sxs-lookup"><span data-stu-id="b757e-240">**64-bit Outlook**:</span></span>

     ```text
     Windows Registry Editor Version 5.00

     [HKEY_LOCAL_MACHINE\Software\Microsoft\Junk E-mail Reporting\Addins]
     "LoggingLevel"="Verbose"
     ```

2. <span data-ttu-id="b757e-241">Redémarrez Outlook et demandez aux utilisateurs de les signaler lorsqu’ils voient le message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b757e-241">Restart Outlook and ask users to report back when they see the error message.</span></span>

3. <span data-ttu-id="b757e-242">Collectez les informations de journal se trouvant à l'emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="b757e-242">Collect the log information found at the following location:</span></span>

   `%LOCALAPPDATA%\Microsoft\Junk Email Reporting Add-in\SpamReporterAddinLog.txt`

4. <span data-ttu-id="b757e-243">Contactez les techniciens du support Exchange Online Protection et fournissez-leur les informations du journal.</span><span class="sxs-lookup"><span data-stu-id="b757e-243">Contact Exchange Online Protection Technical Support and provide them with the log information.</span></span>

#### <a name="problem-users-selected-not-to-receive-a-confirmation-prompt-when-they-report-messages-and-now-they-want-the-prompt-back"></a><span data-ttu-id="b757e-244">Problème : les utilisateurs ont choisi de ne pas recevoir d’invite de confirmation lorsqu’ils signalaient des messages, et veulent maintenant que l’invite soit de nouveau</span><span class="sxs-lookup"><span data-stu-id="b757e-244">Problem: Users selected not to receive a confirmation prompt when they report messages, and now they want the prompt back</span></span>

1. <span data-ttu-id="b757e-245">Créez `ConfirmReportJunk` la clé de Registre avec la valeur « True » :</span><span class="sxs-lookup"><span data-stu-id="b757e-245">Create the `ConfirmReportJunk`registry key with the value "True":</span></span>

   ```text
   Windows Registry Editor Version 5.00

   HKEY_CURRENT_USER\Software\Microsoft\Junk E-mail Reporting\Preferences]
   "ConfirmReportJunk"="True"
   ```

2. <span data-ttu-id="b757e-246">Redémarrez Outlook.</span><span class="sxs-lookup"><span data-stu-id="b757e-246">Restart Outlook.</span></span>