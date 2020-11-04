---
title: Installer et utiliser le complément de création de rapports de courrier indésirable pour Microsoft Outlook
f1.keywords:
- NOCSH
ms.author: siosulli
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 4650fec1-4ee3-4659-abbc-bf091718cb26
ms.collection:
- M365-security-compliance
description: Découvrez comment installer et utiliser le complément Microsoft Junk Email Reporting pour signaler les messages de courrier indésirable, de courrier indésirable et de hameçonnage à Microsoft.
ms.openlocfilehash: 6e4c16ed8efd781a6e8ecea422fe55fb6723209c
ms.sourcegitcommit: b64f36d3873fa0041b24bec029deb73ccfdfdbac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48877548"
---
# <a name="install-and-use-the-junk-email-reporting-add-in-for-microsoft-outlook"></a><span data-ttu-id="eda84-103">Installer et utiliser le complément de création de rapports de courrier indésirable pour Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="eda84-103">Install and use the Junk Email Reporting add-in for Microsoft Outlook</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


> [!NOTE]
> <span data-ttu-id="eda84-104">Si vous n’utilisez pas actuellement le complément de création de rapports de courrier indésirable, nous vous recommandons d’utiliser le [complément de rapport de message](enable-the-report-message-add-in.md) .</span><span class="sxs-lookup"><span data-stu-id="eda84-104">If you aren't currently using the Junk E-mail Reporting add-in, we recommend the [Report Message add-in](enable-the-report-message-add-in.md) instead.</span></span> <span data-ttu-id="eda84-105">Pour plus d’informations, voir [Signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="eda84-105">For more information, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

<span data-ttu-id="eda84-106">Le complément de création de rapports de courrier indésirable pour Microsoft Outlook permet aux utilisateurs de soumettre des faux positifs (courrier électronique marqué comme courrier indésirable), des faux négatifs (courrier incorrect autorisé) et des messages de hameçonnage à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="eda84-106">The Junk Email Reporting Add-in for Microsoft Outlook allows users to submit false positives (good email marked as spam), false negatives (bad email allowed) and phishing messages to Microsoft.</span></span> <span data-ttu-id="eda84-107">Si votre organisation n’utilise pas Exchange Online Protection (par exemple, les services de messagerie ou Exchange locaux autres qu’Exchange Online), votre envoi de rapports de courrier indésirable n’affecte pas le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="eda84-107">If your organization doesn't use Exchange Online Protection (for example, on-premises Exchange or email services other than Exchange Online), your junk email report submission will not affect your spam filtering.</span></span>

<span data-ttu-id="eda84-108">Cette rubrique explique comment installer et utiliser le complément de création de rapports de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="eda84-108">This topic explains how to install and use the Junk Email Reporting add-in.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="eda84-109">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="eda84-109">What do you need to know before you begin?</span></span>

- <span data-ttu-id="eda84-110">Pour installer le complément de création de rapports de courrier indésirable, voir la section relative à l' [installation du complément de création de rapports de courrier indésirable](#install-the-junk-email-reporting-add-in) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="eda84-110">To install the Junk Email Reporting add-in, see the [Install the Junk Email Reporting add-in](#install-the-junk-email-reporting-add-in) section later in this topic.</span></span>

- <span data-ttu-id="eda84-111">Le complément de création de rapports de courrier indésirable fonctionne avec les versions suivantes d’Outlook :</span><span class="sxs-lookup"><span data-stu-id="eda84-111">The Junk Email Reporting add-in works with the following versions of Outlook:</span></span>

  - <span data-ttu-id="eda84-112">Outlook 2013 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="eda84-112">Outlook 2013 or later</span></span>
  - <span data-ttu-id="eda84-113">Outlook inclus avec les applications Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="eda84-113">Outlook included with Microsoft 365 Apps for enterprise</span></span>

- <span data-ttu-id="eda84-114">Pour plus d’informations sur la création de rapports de messages à Microsoft, consultez la rubrique [signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="eda84-114">For more information about reporting messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="use-the-junk-email-reporting-add-in-to-report-spam-and-phishing-messages"></a><span data-ttu-id="eda84-115">Utiliser le complément de création de rapports de courrier indésirable pour signaler les messages de courrier indésirable et de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="eda84-115">Use the Junk Email Reporting add-in to report spam and phishing messages</span></span>

1. <span data-ttu-id="eda84-116">Pour les messages de la boîte de réception ou de tout autre dossier de messagerie, à l’exception du courrier indésirable, utilisez l’une des méthodes suivantes pour signaler les messages de courrier indésirable et de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="eda84-116">For messages in the Inbox or any other email folder except Junk Email, use any of the following methods to report spam and phishing messages:</span></span>

   - <span data-ttu-id="eda84-117">Sélectionnez le message ou ouvrez le message.</span><span class="sxs-lookup"><span data-stu-id="eda84-117">Select the message or open the message.</span></span> <span data-ttu-id="eda84-118">Dans l’onglet **Accueil** ou **message** du ruban, cliquez sur **courrier indésirable** , puis sélectionnez **signaler comme courrier indésirable** ou **signaler comme hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="eda84-118">In the **Home** or **Message** tab in the ribbon, click **Junk** , and then select **Report as Junk** or **Report as Phishing**.</span></span>

     ![Signaler le courrier indésirable ou de hameçonnage à partir du ruban](../../media/junk-email-reporting-ribbon.png)

   - <span data-ttu-id="eda84-120">Cliquez avec le bouton droit sur le message, sélectionnez **courrier indésirable** , puis **signaler comme courrier indésirable** ou **signaler comme hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="eda84-120">Right-click on the message, select **Junk** , and then select **Report as Junk** or **Report as Phishing**.</span></span>

     ![Signaler le courrier indésirable ou le courrier indésirable en cliquant avec le bouton droit](../../media/junk-email-reporting-right-click.png)

   - <span data-ttu-id="eda84-122">Sélectionnez plusieurs messages, cliquez avec le bouton droit, puis sélectionnez **signaler comme courrier indésirable** ou **signaler comme hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="eda84-122">Select multiple messages, right-click, and then select **Report as Junk** or **Report as Phishing**.</span></span>

     ![Signaler plusieurs messages de courrier indésirable ou de hameçonnage à partir d’un clic droit](../../media/junk-email-reporting-right-click-multiple.png)

2. <span data-ttu-id="eda84-124">Dans la boîte de dialogue qui s’affiche, lisez les informations, puis cliquez sur **rapport**.</span><span class="sxs-lookup"><span data-stu-id="eda84-124">In the dialog that appears, read the information and click **Report**.</span></span> <span data-ttu-id="eda84-125">Si vous changez d’avis, cliquez sur **ne pas signaler**.</span><span class="sxs-lookup"><span data-stu-id="eda84-125">If you change your mind, click **Don't Report**.</span></span>

   ![Boîte de dialogue signaler comme courrier indésirable](../../media/junk-email-reporting-report-as-junk-dialog.png)

   ![Boîte de dialogue signaler en tant que hameçonnage](../../media/junk-email-reporting-report-as-phishing-dialog.png)

3. <span data-ttu-id="eda84-128">Les messages sélectionnés seront envoyés à Microsoft pour analyse et :</span><span class="sxs-lookup"><span data-stu-id="eda84-128">The selected messages will be sent to Microsoft for analysis and:</span></span>

   - <span data-ttu-id="eda84-129">Déplacé vers le dossier courrier indésirable s’il a été signalé comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="eda84-129">Moved to the Junk Email folder if it was reported as spam.</span></span>
   - <span data-ttu-id="eda84-130">Supprimé s’il a été signalé comme hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="eda84-130">Deleted if it was reported as phishing.</span></span>
   
   <span data-ttu-id="eda84-131">Pour confirmer que les messages ont été envoyés, ouvrez le dossier **Éléments envoyés** pour afficher les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="eda84-131">To confirm that the messages have been submitted, open your **Sent Items** folder to view the submitted messages.</span></span>

## <a name="use-the-junk-email-reporting-add-in-to-report-non-spam-and-phishing-messages-from-the-junk-email-folder"></a><span data-ttu-id="eda84-132">Utiliser le complément de création de rapports de courrier indésirable pour signaler les messages de courrier indésirable et de hameçonnage dans le dossier courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="eda84-132">Use the Junk Email Reporting add-in to report non-spam and phishing messages from the Junk Email folder</span></span>

1. <span data-ttu-id="eda84-133">Dans le dossier courrier indésirable, utilisez l’une des méthodes suivantes pour signaler les fausses alertes de courrier indésirable ou les messages de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="eda84-133">In the Junk Email folder, use any of the following methods to report spam false positives or phishing messages:</span></span>

   - <span data-ttu-id="eda84-134">Sélectionnez le message ou ouvrez le message.</span><span class="sxs-lookup"><span data-stu-id="eda84-134">Select the message or open the message.</span></span> <span data-ttu-id="eda84-135">Dans l’onglet **Accueil** ou **message** du ruban, cliquez sur **légitime** , puis sélectionnez **signaler comme légitime** ou **signaler comme hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="eda84-135">In the **Home** or **Message** tab in the ribbon, click **Not Junk** , and then select **Report as Not Junk** or **Report as Phishing**.</span></span>

     ![Signaler des courriers indésirables ou de hameçonnage à partir du ruban dans le dossier courrier indésirable](../../media/junk-email-reporting-junk-folder-ribbon.png)

   - <span data-ttu-id="eda84-137">Cliquez avec le bouton droit sur le message, cliquez sur **courrier indésirable** , puis sélectionnez **signaler comme légitime** ou **signaler comme hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="eda84-137">Right-click on the message, click **Junk** , and then select **Report as Not Junk** or **Report as Phishing**.</span></span>

     ![Signaler le courrier indésirable ou le courrier indésirable dans le dossier courrier indésirable](../../media/junk-email-reporting-junk-folder-right-click.png)

   - <span data-ttu-id="eda84-139">Sélectionnez plusieurs messages, cliquez avec le bouton droit, puis sélectionnez **signaler comme légitime** ou **signaler comme hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="eda84-139">Select multiple messages, right-click, and then select **Report as Not Junk** or **Report as Phishing**.</span></span>

     ![Signaler plusieurs messages électroniques de courrier indésirable ou de hameçonnage dans le dossier courrier indésirable](../../media/junk-email-reporting-junk-folder-right-click-multiple.png)

2. <span data-ttu-id="eda84-141">Dans la boîte de dialogue qui s’affiche, lisez les informations, puis cliquez sur **rapport**.</span><span class="sxs-lookup"><span data-stu-id="eda84-141">In the dialog that appears, read the information and click **Report**.</span></span> <span data-ttu-id="eda84-142">Si vous changez d’avis, cliquez sur **ne pas signaler**.</span><span class="sxs-lookup"><span data-stu-id="eda84-142">If you change your mind, click **Don't Report**.</span></span>

   ![Boîte de dialogue signaler comme légitime](../../media/junk-email-reporting-report-as-not-junk-dialog.png)

   ![Boîte de dialogue signaler en tant que hameçonnage](../../media/junk-email-reporting-report-as-phishing-dialog.png)

3. <span data-ttu-id="eda84-145">Les messages sélectionnés seront envoyés à Microsoft pour analyse et :</span><span class="sxs-lookup"><span data-stu-id="eda84-145">The selected messages will be sent to Microsoft for analysis and:</span></span>

   - <span data-ttu-id="eda84-146">Déplacé vers le dossier courrier indésirable s’il a été signalé comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="eda84-146">Moved to the Junk Email folder if it was reported as spam.</span></span>
   - <span data-ttu-id="eda84-147">Supprimé s’il a été signalé comme hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="eda84-147">Deleted if it was reported as phishing.</span></span>

   <span data-ttu-id="eda84-148">Pour confirmer que les messages ont été envoyés, ouvrez le dossier **Éléments envoyés** pour afficher les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="eda84-148">To confirm that the messages have been submitted, open your **Sent Items** folder to view the submitted messages.</span></span>

## <a name="install-the-junk-email-reporting-add-in"></a><span data-ttu-id="eda84-149">Installer le complément de création de rapports de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="eda84-149">Install the Junk Email Reporting add-in</span></span>

- <span data-ttu-id="eda84-150">Vous devez disposer des privilèges d’administrateur sur l’ordinateur sur lequel vous installez le complément.</span><span class="sxs-lookup"><span data-stu-id="eda84-150">You need to have administrator privileges on the computer where you're installing the add-in.</span></span>

- <span data-ttu-id="eda84-151">Accédez au <https://www.microsoft.com/download/details.aspx?id=18275> fichier. msi approprié pour votre version d’Office et téléchargez-le dans un emplacement facile à trouver :</span><span class="sxs-lookup"><span data-stu-id="eda84-151">Go to <https://www.microsoft.com/download/details.aspx?id=18275> and download the appropriate .msi file for your version of Office to a location that's easy to find:</span></span>

  - <span data-ttu-id="eda84-152">**32-bit** : `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi`</span><span class="sxs-lookup"><span data-stu-id="eda84-152">**32-bit** : `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi`</span></span>
  - <span data-ttu-id="eda84-153">**64-bit** : `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi`</span><span class="sxs-lookup"><span data-stu-id="eda84-153">**64-bit** : `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi`</span></span>

- <span data-ttu-id="eda84-154">Pour Outlook 2013 ou version ultérieure, la seule condition requise est Microsoft .NET Framework 2,0.</span><span class="sxs-lookup"><span data-stu-id="eda84-154">For Outlook 2013 or later, the only prerequisite is the Microsoft .NET Framework 2.0.</span></span> <span data-ttu-id="eda84-155">Dans Windows 10, vous n’installez pas .NET Framework 2,0 à partir d’un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="eda84-155">In Windows 10, you don't install the .NET Framework 2.0 from a download.</span></span>

### <a name="install-the-junk-email-reporting-add-in-using-the-setup-wizard"></a><span data-ttu-id="eda84-156">Installer le complément de création de rapports de courrier indésirable à l’aide de l’Assistant Installation</span><span class="sxs-lookup"><span data-stu-id="eda84-156">Install the Junk Email Reporting Add-in using the Setup wizard</span></span>

1. <span data-ttu-id="eda84-157">Sur votre ordinateur, fermez Outlook.</span><span class="sxs-lookup"><span data-stu-id="eda84-157">On your computer, close Outlook.</span></span>

2. <span data-ttu-id="eda84-158">Dans Windows 10, vérifiez que .NET Framework 2,0 est activé.</span><span class="sxs-lookup"><span data-stu-id="eda84-158">In Windows 10, verify the .NET Framework 2.0 is enabled.</span></span> <span data-ttu-id="eda84-159">Pour obtenir des instructions, consultez [la rubrique activer le .NET Framework 3,5 dans le panneau de configuration](https://docs.microsoft.com/dotnet/framework/install/dotnet-35-windows-10#enable-the-net-framework-35-in-control-panel).</span><span class="sxs-lookup"><span data-stu-id="eda84-159">For instructions, see [Enable the .NET Framework 3.5 in Control Panel](https://docs.microsoft.com/dotnet/framework/install/dotnet-35-windows-10#enable-the-net-framework-35-in-control-panel).</span></span>

3. <span data-ttu-id="eda84-160">Recherchez le fichier. msi que vous avez téléchargé et double-cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="eda84-160">Locate the .msi file you downloaded and double-click on it.</span></span>

4. <span data-ttu-id="eda84-161">Dans la page **Bienvenue à la configuration du complément Microsoft Junk Email Reporting** , cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="eda84-161">On the **Welcome to Microsoft Junk Email Reporting Add-in Setup** page, click **Next**.</span></span>

5. <span data-ttu-id="eda84-162">Consultez le contrat de licence, cliquez sur **J’accepte les termes du contrat de licence** si vous acceptez les termes, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="eda84-162">Review the license agreement, click **I accept the terms in the License Agreement** if you agree to the terms, and then click **Next**.</span></span>

6. <span data-ttu-id="eda84-163">Une fois l'exécution de l'Assistant terminée, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="eda84-163">When the wizard is complete, click **Finish**.</span></span>

<span data-ttu-id="eda84-164">Lancez Outlook.</span><span class="sxs-lookup"><span data-stu-id="eda84-164">Start Outlook.</span></span>

<span data-ttu-id="eda84-p109">Consultez le bouton **Courrier indésirable** sur votre ruban Outlook. Vous pouvez à présent signaler des messages de courrier indésirable à Microsoft en les sélectionnant dans votre boîte de réception, puis en cliquant sur le bouton permettant de **signaler le courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="eda84-p109">Look for the **Junk** button on your Outlook ribbon. You can now report junk email messages to Microsoft by selecting the junk email messages in your Inbox and clicking the **Report Junk** button.</span></span>

<span data-ttu-id="eda84-p110">Cliquez sur la flèche vers le bas en regard du bouton **Courrier indésirable** pour plus d'options, telles que le **signalement en tant que hameçonnage** si vous souhaitez signaler des messages électroniques d'hameçonnage à Microsoft. Dans votre dossier de courrier indésirable, vous pouvez également sélectionner l'option de **signalement en tant que courrier non indésirable** si un message électronique a été identifié à tort comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="eda84-p110">Choose the down arrow next to **Junk** for more options such as **Report as Phishing** if you want to report phishing scam emails to Microsoft. In your junk mail folder, you can also select, **Report not junk** if an email was incorrectly identified as junk mail.</span></span>

### <a name="install-the-junk-email-reporting-add-in-using-silent-mode"></a><span data-ttu-id="eda84-169">Installation du complément de création de rapports de courrier indésirable en mode sans assistance</span><span class="sxs-lookup"><span data-stu-id="eda84-169">Install the Junk Email Reporting Add-In using Silent Mode</span></span>

1. <span data-ttu-id="eda84-170">Sur votre ordinateur, fermez Outlook.</span><span class="sxs-lookup"><span data-stu-id="eda84-170">On your computer, close Outlook.</span></span>

2. <span data-ttu-id="eda84-171">Dans Windows 10, installez .NET Framework 2,0 en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="eda84-171">In Windows 10, install the .NET Framework 2.0 by running the following command:</span></span>

   ```dos
   DISM /Online /Enable-Feature /FeatureName:NetFx3 /All
   ```

3. <span data-ttu-id="eda84-172">Pour installer le complément sans intervention de l’utilisateur, ouvrez une invite de commandes et utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="eda84-172">To install the add-in without any user interaction, open a Command Prompt and use the following syntax:</span></span>

   ```dos
   msiexec /qn /i "<PathToMSIFile>\<MSIFile>" [MaxMessageSelection=<1-50>] [BccEmailAddress="<EmailAddress1>; <EmailAddress2>"...]
   ```

   - <span data-ttu-id="eda84-173">`MaxMessageSelection` Spécifie le nombre maximal de messages que vous pouvez sélectionner pour une seule soumission.</span><span class="sxs-lookup"><span data-stu-id="eda84-173">`MaxMessageSelection` specifies the maximum number of messages that you can select for a single submission.</span></span> <span data-ttu-id="eda84-174">Les valeurs valides sont comprises entre 1 et 50.</span><span class="sxs-lookup"><span data-stu-id="eda84-174">Valid values are from 1 to 50.</span></span> <span data-ttu-id="eda84-175">Par défaut, la valeur 15 s’applique.</span><span class="sxs-lookup"><span data-stu-id="eda84-175">The default value is 15.</span></span>

   - <span data-ttu-id="eda84-176">`BccEmailAddress` spécifie les destinataires CCI supplémentaires qui recevront une copie de tous les envois de tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="eda84-176">`BccEmailAddress` specifies additional Bcc recipients who will receive a copy of all user submissions.</span></span> <span data-ttu-id="eda84-177">La valeur par défaut est vide (pas de destinataires CCI supplémentaires).</span><span class="sxs-lookup"><span data-stu-id="eda84-177">The default value is blank (no additional Bcc recipients).</span></span>

   <span data-ttu-id="eda84-178">Cet exemple installe la version 64 bits du complément à partir du chemin d’accès spécifié avec les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="eda84-178">This example installs the 64-bit version of the add-in from the specified path with the default settings.</span></span>

   ```dos
   msiexec /qn /i "C:\Downloads\Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi"
   ```

   <span data-ttu-id="eda84-179">Cet exemple installe la version 32 bits du complément à partir du chemin d’accès spécifié avec les paramètres supplémentaires suivants :</span><span class="sxs-lookup"><span data-stu-id="eda84-179">This example installs the 32-bit version of the add-in from the specified path with the following additional settings:</span></span>

   - <span data-ttu-id="eda84-180">Vous pouvez sélectionner jusqu’à 20 messages en une seule soumission.</span><span class="sxs-lookup"><span data-stu-id="eda84-180">Up to 20 messages can be selected in a single submission.</span></span>
   - <span data-ttu-id="eda84-181">junkreports@contoso.com et hollyd@treyresearch.net reçoivent des copies CCI de toutes les soumissions.</span><span class="sxs-lookup"><span data-stu-id="eda84-181">junkreports@contoso.com and hollyd@treyresearch.net receive Bcc copies of all submissions.</span></span>

   ```dos
   msiexec /qn /i "C:\Downloads\Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi" MaxMessageSelection=20 BccEmailAddress="junkreports@contoso.com; hollyd@treyresearch.net"
   ```

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="eda84-182">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="eda84-182">How do you know this worked?</span></span>

<span data-ttu-id="eda84-183">Pour vérifier que vous avez correctement installé le complément de création de rapports de courrier indésirable, effectuez l’une des opérations suivantes dans Outlook :</span><span class="sxs-lookup"><span data-stu-id="eda84-183">To verify that you've successfully installed the Junk Email Reporting Add-in, do the any of the following steps in Outlook:</span></span>

- <span data-ttu-id="eda84-184">Sélectionnez le message ou ouvrez le message.</span><span class="sxs-lookup"><span data-stu-id="eda84-184">Select the message or open the message.</span></span> <span data-ttu-id="eda84-185">Dans l’onglet **Accueil** ou **message** du ruban, cliquez sur **courrier indésirable** et vérifiez que les options suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="eda84-185">In the **Home** or **Message** tab in the ribbon, click **Junk** , and verify that the following options are available:</span></span>

  - <span data-ttu-id="eda84-186">**Signaler comme courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="eda84-186">**Report as Junk**</span></span>
  - <span data-ttu-id="eda84-187">**Signaler comme hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="eda84-187">**Report as Phishing**</span></span>
  - <span data-ttu-id="eda84-188">**Options de signalement de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="eda84-188">**Junk Reporting Options**</span></span>
  - <span data-ttu-id="eda84-189">**Signaler une aide en ligne indésirable**</span><span class="sxs-lookup"><span data-stu-id="eda84-189">**Report Junk Online Help**</span></span>

  ![Signaler le courrier indésirable ou de hameçonnage à partir du ruban](../../media/junk-email-reporting-ribbon.png)

- <span data-ttu-id="eda84-191">Cliquez avec le bouton droit sur le message, sélectionnez **courrier indésirable** et assurez-vous que les options suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="eda84-191">Right-click on the message, select **Junk** , and verify that the following options are available:</span></span>

  - <span data-ttu-id="eda84-192">**Signaler comme courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="eda84-192">**Report as Junk**</span></span>
  - <span data-ttu-id="eda84-193">**Signaler comme hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="eda84-193">**Report as Phishing**</span></span>
  - <span data-ttu-id="eda84-194">**Options de signalement de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="eda84-194">**Junk Reporting Options**</span></span>
  - <span data-ttu-id="eda84-195">**Signaler une aide en ligne indésirable**</span><span class="sxs-lookup"><span data-stu-id="eda84-195">**Report Junk Online Help**</span></span>

  ![Signaler le courrier indésirable ou le courrier indésirable en cliquant avec le bouton droit](../../media/junk-email-reporting-right-click.png)

- <span data-ttu-id="eda84-197">Sélectionnez plusieurs messages, cliquez avec le bouton droit et vérifiez que les options suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="eda84-197">Select multiple messages, right click, and verify that the following options are available:</span></span>

  - <span data-ttu-id="eda84-198">**Signaler comme courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="eda84-198">**Report as Junk**</span></span>
  - <span data-ttu-id="eda84-199">**Signaler comme hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="eda84-199">**Report as Phishing**</span></span>

  ![Signaler plusieurs messages de courrier indésirable ou de hameçonnage à partir d’un clic droit](../../media/junk-email-reporting-right-click-multiple.png)

- <span data-ttu-id="eda84-201">Effectuez les actions précédentes dans le dossier courrier **indésirable** et vérifiez que les options de signalement de **courrier** indésirable précédentes ne sont **pas des courriers indésirables**.</span><span class="sxs-lookup"><span data-stu-id="eda84-201">Do the previous actions in the **Junk Email** folder and verify the previous **Junk** reporting options are now **Not Junk**.</span></span>

  ![Signaler des courriers indésirables ou de hameçonnage à partir du ruban dans le dossier courrier indésirable](../../media/junk-email-reporting-junk-folder-ribbon.png)

  ![Signaler le courrier indésirable ou le courrier indésirable dans le dossier courrier indésirable](../../media/junk-email-reporting-junk-folder-right-click.png)

  ![Signaler plusieurs messages électroniques de courrier indésirable ou de hameçonnage dans le dossier courrier indésirable](../../media/junk-email-reporting-junk-folder-right-click-multiple.png)

## <a name="uninstall-the-junk-email-reporting-add-in"></a><span data-ttu-id="eda84-205">Désinstallation du complément Junk Email Reporting</span><span class="sxs-lookup"><span data-stu-id="eda84-205">Uninstall the Junk Email Reporting Add-in</span></span>

<span data-ttu-id="eda84-206">Une fois que vous avez fermé Outlook, utilisez l’une des procédures suivantes pour désinstaller le complément de création de rapports de courrier indésirable :</span><span class="sxs-lookup"><span data-stu-id="eda84-206">After you close Outlook, use any of the following procedures to uninstall the Junk Email Reporting Add-in:</span></span>

- <span data-ttu-id="eda84-207">**Panneau de configuration** : Appuyez sur la touche Windows + R. Dans la boîte de dialogue **exécuter** qui s’ouvre, saisissez `control appwiz.cpl` puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="eda84-207">**Control Panel** : Press the Windows key + R. In the **Run** dialog that opens, enter `control appwiz.cpl` and then click **OK**.</span></span>

  <span data-ttu-id="eda84-208">Recherchez et sélectionnez **complément Microsoft Junk Email Reporting** dans la liste, puis cliquez sur **désinstaller**.</span><span class="sxs-lookup"><span data-stu-id="eda84-208">Find and select **Microsoft Junk Email Reporting Add-in** in the list, and then click **Uninstall**.</span></span>

- <span data-ttu-id="eda84-209">**Package Windows Installer** : recherchez ou téléchargez le fichier. msi approprié, puis double-cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="eda84-209">**Windows Installer package** : Find or download the appropriate .msi file, and double-click on it.</span></span>

  - <span data-ttu-id="eda84-210">**32-bit** : `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi`</span><span class="sxs-lookup"><span data-stu-id="eda84-210">**32-bit** : `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi`</span></span>

  - <span data-ttu-id="eda84-211">**64-bit** : `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi`</span><span class="sxs-lookup"><span data-stu-id="eda84-211">**64-bit** : `Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi`</span></span>

  <span data-ttu-id="eda84-212">Dans la boîte de dialogue qui s’affiche, sélectionnez **supprimer le complément Microsoft Junk Email Reporting pour Outlook** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="eda84-212">In the dialog that appears, select **Remove Microsoft Junk Email Reporting Add-in for Outlook** and then click **Next**.</span></span>

- <span data-ttu-id="eda84-213">**Mode silencieux** : recherchez ou téléchargez le fichier. msi approprié.</span><span class="sxs-lookup"><span data-stu-id="eda84-213">**Silent Mode** : Find or download the appropriate .msi file.</span></span> <span data-ttu-id="eda84-214">Dans une fenêtre d’invite de commandes, remplacez \<PathToFile\> par l’emplacement du fichier. msi et exécutez l’une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="eda84-214">In a Command Prompt window, replace \<PathToFile\> with the location of the .msi file, and run one of the following commands:</span></span>

  - <span data-ttu-id="eda84-215">**32-bit** :</span><span class="sxs-lookup"><span data-stu-id="eda84-215">**32-bit** :</span></span>

    ```dos
    msiexec /x "<PathToFile>\Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (32-bit).msi" /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"
    ```

  - <span data-ttu-id="eda84-216">**64-bit** :</span><span class="sxs-lookup"><span data-stu-id="eda84-216">**64-bit** :</span></span>

    ```dos
    msiexec /x "<PathToFile>\Junk Reporting Add-in for Office 2007, 2010, 2013, and 2016 (64-bit).msi" /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"
    ```

<span data-ttu-id="eda84-217">Lorsque vous ouvrez Outlook après la désinstallation, les options de signalement de courrier indésirable, de courrier indésirable et de hameçonnage doivent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="eda84-217">When you open Outlook after the uninstall, the junk, not junk, and phishing reporting options should be gone.</span></span>

## <a name="troubleshooting-the-junk-email-reporting-add-in"></a><span data-ttu-id="eda84-218">Dépannage du complément de création de rapports de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="eda84-218">Troubleshooting the Junk Email Reporting add-in</span></span>

<span data-ttu-id="eda84-219">Parfois, vous pouvez rencontrer des problèmes avec Outlook après avoir ajouté le complément de création de rapports de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="eda84-219">Occasionally, you might experience trouble with Outlook after adding the Junk Email Reporting Add-In.</span></span> <span data-ttu-id="eda84-220">Cette section décrit les problèmes que vous pouvez rencontrer, ainsi que des conseils pour la résolution de ces problèmes.</span><span class="sxs-lookup"><span data-stu-id="eda84-220">This section describes problems that you might encounter, along with tips for resolving these issues.</span></span>

### <a name="troubleshooting-for-users"></a><span data-ttu-id="eda84-221">Résolution des problèmes pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="eda84-221">Troubleshooting for users</span></span>

<span data-ttu-id="eda84-222">Vous rencontrez un ou plusieurs des problèmes suivants :</span><span class="sxs-lookup"><span data-stu-id="eda84-222">You experience one or more of the following problems:</span></span>

- <span data-ttu-id="eda84-223">Rien ne se passe quand vous cliquez sur **Signaler le courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="eda84-223">Nothing happens when you click **Report Junk**</span></span>
- <span data-ttu-id="eda84-224">Outlook cesse de répondre après avoir sélectionné un message électronique</span><span class="sxs-lookup"><span data-stu-id="eda84-224">Outlook stops responding after you select an email message</span></span>
- <span data-ttu-id="eda84-225">Le courrier indésirable signalé ne peut pas être remis en raison d'une réponse « Non remis ».</span><span class="sxs-lookup"><span data-stu-id="eda84-225">Reported junk mail cannot be delivered due to an "undeliverable" reply</span></span>

<span data-ttu-id="eda84-226">Pour résoudre ce problème, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="eda84-226">To fix this problem, do the following steps:</span></span>

1. <span data-ttu-id="eda84-227">Fermez et redémarrez Outlook.</span><span class="sxs-lookup"><span data-stu-id="eda84-227">Close and restart Outlook.</span></span>
2. <span data-ttu-id="eda84-228">Créez et envoyez un message de test, puis vérifiez que le destinataire a reçu le message.</span><span class="sxs-lookup"><span data-stu-id="eda84-228">Create and send a test message, and verify that the recipient received the message.</span></span>
3. <span data-ttu-id="eda84-229">Si le problème persiste, contactez votre administrateur.</span><span class="sxs-lookup"><span data-stu-id="eda84-229">If the problem persists, contact your admin.</span></span>

<span data-ttu-id="eda84-230">Pour les autres méthodes que vous pouvez utiliser pour envoyer des messages à Microsoft, consultez la rubrique [signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="eda84-230">For other methods that you can use to submit messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

### <a name="troubleshooting-for-admins"></a><span data-ttu-id="eda84-231">Résolution des problèmes liés aux administrateurs</span><span class="sxs-lookup"><span data-stu-id="eda84-231">Troubleshooting for admins</span></span>

#### <a name="problem-an-error-message-continually-appears-that-asks-users-to-contact-their-system-administrator"></a><span data-ttu-id="eda84-232">Problème : un message d’erreur s’affiche en continu qui demande aux utilisateurs de contacter leur administrateur système.</span><span class="sxs-lookup"><span data-stu-id="eda84-232">Problem: An error message continually appears that asks users to contact their system administrator</span></span>

1. <span data-ttu-id="eda84-233">Vérifiez ou définissez la `LoggingLevel` clé de Registre sur la valeur « verbose » :</span><span class="sxs-lookup"><span data-stu-id="eda84-233">Verify or set the `LoggingLevel` registry key to the value "Verbose":</span></span>

   - <span data-ttu-id="eda84-234">**Outlook 32 bits sur Windows 32 bits** :</span><span class="sxs-lookup"><span data-stu-id="eda84-234">**32-bit Outlook on 32-bit Windows** :</span></span>

     ```text
     Windows Registry Editor Version 5.00

     [HKEY_LOCAL_MACHINE\Software\Microsoft\Junk Email Reporting\Addins]
     "LoggingLevel"="Verbose"
     ```

   - <span data-ttu-id="eda84-235">**Outlook 32 bits sur Windows 64 bits** :</span><span class="sxs-lookup"><span data-stu-id="eda84-235">**32-bit Outlook on 64-bit Windows** :</span></span>

     ```text
     Windows Registry Editor Version 5.00

     [HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Junk Email Reporting\Addins]
     "LoggingLevel"="Verbose"
     ```

   - <span data-ttu-id="eda84-236">**Outlook 64 bits** :</span><span class="sxs-lookup"><span data-stu-id="eda84-236">**64-bit Outlook** :</span></span>

     ```text
     Windows Registry Editor Version 5.00

     [HKEY_LOCAL_MACHINE\Software\Microsoft\Junk E-mail Reporting\Addins]
     "LoggingLevel"="Verbose"
     ```

2. <span data-ttu-id="eda84-237">Redémarrez Outlook et demandez aux utilisateurs de revenir en arrière lorsqu’ils voient le message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="eda84-237">Restart Outlook and ask users to report back when they see the error message.</span></span>

3. <span data-ttu-id="eda84-238">Collectez les informations de journal se trouvant à l'emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="eda84-238">Collect the log information found at the following location:</span></span>

   `%LOCALAPPDATA%\Microsoft\Junk Email Reporting Add-in\SpamReporterAddinLog.txt`

4. <span data-ttu-id="eda84-239">Contactez les techniciens du support Exchange Online Protection et fournissez-leur les informations du journal.</span><span class="sxs-lookup"><span data-stu-id="eda84-239">Contact Exchange Online Protection Technical Support and provide them with the log information.</span></span>

#### <a name="problem-users-selected-not-to-receive-a-confirmation-prompt-when-they-report-messages-and-now-they-want-the-prompt-back"></a><span data-ttu-id="eda84-240">Problème : les utilisateurs sélectionnés ne reçoivent pas d’invite de confirmation lorsqu’ils signalent des messages, et souhaitent maintenant que l’invite se redirige.</span><span class="sxs-lookup"><span data-stu-id="eda84-240">Problem: Users selected not to receive a confirmation prompt when they report messages, and now they want the prompt back</span></span>

1. <span data-ttu-id="eda84-241">Créez la `ConfirmReportJunk` clé de Registre avec la valeur « true » :</span><span class="sxs-lookup"><span data-stu-id="eda84-241">Create the `ConfirmReportJunk`registry key with the value "True":</span></span>

   ```text
   Windows Registry Editor Version 5.00

   HKEY_CURRENT_USER\Software\Microsoft\Junk E-mail Reporting\Preferences]
   "ConfirmReportJunk"="True"
   ```

2. <span data-ttu-id="eda84-242">Redémarrez Outlook.</span><span class="sxs-lookup"><span data-stu-id="eda84-242">Restart Outlook.</span></span>
