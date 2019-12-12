---
title: Installation du complément de création de rapports de courrier indésirable pour Microsoft Outlook
ms.author: MSFTTracyP
author: tracyp
manager: dansimp
ms.date: 12/9/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 8dcc752f-e22e-44ce-a104-4cc4d7e439f3
ms.collection:
- M365-security-compliance
description: Dans cette articleSupported LanguagesInstall le dossier Junk Email Reporting Add-ununinstall the Junk Email Reporting Add-inFor more information
ms.openlocfilehash: 14c3914601ab8a6b3273b56a3915df9c909fc06c
ms.sourcegitcommit: 5710ce729c55d95b8b452d99ffb7ea92b5cb254a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2019
ms.locfileid: "39970390"
---
# <a name="install-the-junk-email-reporting-add-in-for-microsoft-outlook"></a><span data-ttu-id="c87de-103">Installation du complément de création de rapports de courrier indésirable pour Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="c87de-103">Install the Junk Email Reporting Add-in for Microsoft Outlook</span></span>

<span data-ttu-id="c87de-104">Cette rubrique explique comment installer (et désinstaller) le complément Microsoft de création de rapports de courrier indésirable pour Outlook sur des ordinateurs clients au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c87de-104">This topic describes how to install (and uninstall) the Microsoft Junk Email Reporting Add-in for Outlook on client computers in your organization.</span></span> <span data-ttu-id="c87de-105">La version actuelle du complément (janvier 2016) inclut la prise en charge d’Outlook 2016, Outlook 2013 et Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="c87de-105">The current version of the add-in (January 2016) includes support for Outlook 2016, Outlook 2013, and Outlook 2010.</span></span>

<span data-ttu-id="c87de-p102">Le complément (pour toutes les langues prises en charge) vous permet de signaler du courrier indésirable directement à partir du ruban Outlook. La version anglaise du complément inclut des options supplémentaires pour signaler des problèmes liés à la messagerie à Microsoft directement à partir du ruban :</span><span class="sxs-lookup"><span data-stu-id="c87de-p102">The add-in (for all supported languages) allows you to report junk email directly from the Outlook ribbon. The English version of the add-in includes additional options for reporting email issues to Microsoft, directly from the ribbon:</span></span>

- <span data-ttu-id="c87de-108">Signaler les messages électroniques de hameçonnage que vous recevez</span><span class="sxs-lookup"><span data-stu-id="c87de-108">Report phishing scam emails that you receive</span></span>

- <span data-ttu-id="c87de-109">Signalez les messages électroniques identifiés à tort comme du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c87de-109">Report email incorrectly identified as junk mail.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="c87de-110">Langues prises en charge</span><span class="sxs-lookup"><span data-stu-id="c87de-110">Supported Languages</span></span>
<span data-ttu-id="c87de-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="c87de-111"></span></span>

<span data-ttu-id="c87de-112">Le complément Junk Email Reporting prend en charge les langues suivantes :</span><span class="sxs-lookup"><span data-stu-id="c87de-112">The Junk Email Reporting Add-in supports the following languages:</span></span>

- <span data-ttu-id="c87de-113">Chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="c87de-113">Simplified Chinese</span></span>

- <span data-ttu-id="c87de-114">Chinois traditionnel</span><span class="sxs-lookup"><span data-stu-id="c87de-114">Traditional Chinese</span></span>

- <span data-ttu-id="c87de-115">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="c87de-115">Dutch</span></span>

- <span data-ttu-id="c87de-116">Anglais</span><span class="sxs-lookup"><span data-stu-id="c87de-116">English</span></span>

- <span data-ttu-id="c87de-117">Français</span><span class="sxs-lookup"><span data-stu-id="c87de-117">French</span></span>

- <span data-ttu-id="c87de-118">Allemand</span><span class="sxs-lookup"><span data-stu-id="c87de-118">German</span></span>

- <span data-ttu-id="c87de-119">Italien</span><span class="sxs-lookup"><span data-stu-id="c87de-119">Italian</span></span>

- <span data-ttu-id="c87de-120">Japonais</span><span class="sxs-lookup"><span data-stu-id="c87de-120">Japanese</span></span>

- <span data-ttu-id="c87de-121">Coréen</span><span class="sxs-lookup"><span data-stu-id="c87de-121">Korean</span></span>

- <span data-ttu-id="c87de-122">Portugais</span><span class="sxs-lookup"><span data-stu-id="c87de-122">Portuguese</span></span>

- <span data-ttu-id="c87de-123">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="c87de-123">Portuguese (Brazil)</span></span>

- <span data-ttu-id="c87de-124">Espagnol</span><span class="sxs-lookup"><span data-stu-id="c87de-124">Spanish</span></span>

## <a name="install-the-junk-email-reporting-add-in"></a><span data-ttu-id="c87de-125">Installation du complément Junk Email Reporting</span><span class="sxs-lookup"><span data-stu-id="c87de-125">Install the Junk Email Reporting Add-in</span></span>

<span data-ttu-id="c87de-126">Vous pouvez installer le complément de création de rapports de courrier indésirable de deux façons :</span><span class="sxs-lookup"><span data-stu-id="c87de-126">You can install the Junk Email Reporting Add-in:</span></span>

- <span data-ttu-id="c87de-127">En exécutant le package Windows Installer comme vous le feriez pour tout autre fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="c87de-127">By running the Windows Installer package as you would any other .msi file.</span></span> <span data-ttu-id="c87de-128">Lorsque vous installez le complément, une interface GUI s’ouvre et vous invite à parcourir les écrans d’installation.</span><span class="sxs-lookup"><span data-stu-id="c87de-128">When you install the add-in, a GUI interface opens and prompts you through the installation screens.</span></span> <span data-ttu-id="c87de-129">Pour plus d’informations, consultez la rubrique [installer le complément de création de rapports de courrier indésirable à l’aide de l’Assistant Installation](#install-the-junk-email-reporting-add-in-using-the-setup-wizard).</span><span class="sxs-lookup"><span data-stu-id="c87de-129">For more information, see [Install the Junk Email Reporting Add-In using the Setup wizard](#install-the-junk-email-reporting-add-in-using-the-setup-wizard).</span></span>

<span data-ttu-id="c87de-130">OU</span><span class="sxs-lookup"><span data-stu-id="c87de-130">OR</span></span>

- <span data-ttu-id="c87de-p104">En exécutant une installation sans assistance, c'est-à-dire sans interface utilisateur d'installation. Au lieu d'utiliser cette dernière, vous spécifiez des options de ligne de commande qui exécutent un script d'installation. Lorsque vous installez le complément, vous disposez d'options de configuration supplémentaires qui sont indisponibles dans l'interface GUI. Pour plus d'informations, consultez la rubrique relative à [Installation du complément de création de rapports de courrier indésirable en mode sans assistance](#install-the-junk-email-reporting-add-in-using-silent-mode).</span><span class="sxs-lookup"><span data-stu-id="c87de-p104">By running a silent installation which suppresses the installation user interface. Instead, you specify command-line options which run an installation script. When you install the add-in, additional configuration options are available which are not available through the GUI interface. For more information, see [Install the Junk Email Reporting Add-In using Silent Mode](#install-the-junk-email-reporting-add-in-using-silent-mode).</span></span>

### <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="c87de-135">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="c87de-135">What do you need to know before you begin?</span></span>

- <span data-ttu-id="c87de-136">Voir la **Configuration requise** pour le complément Junk Email Reporting à [https://www.microsoft.com/download/details.aspx?id=18275](https://www.microsoft.com/download/details.aspx?id=18275)l’adresse.</span><span class="sxs-lookup"><span data-stu-id="c87de-136">See the **System Requirements** for the Junk Email Reporting Add-in at [https://www.microsoft.com/download/details.aspx?id=18275](https://www.microsoft.com/download/details.aspx?id=18275).</span></span>

> [!NOTE]
> <span data-ttu-id="c87de-137">Vous devez disposer de droits d'administrateur sur l'ordinateur sur lequel vous installez le complément.</span><span class="sxs-lookup"><span data-stu-id="c87de-137">You must have administrator privileges on the computer on which you are installing the add-in.</span></span>

### <a name="install-the-junk-email-reporting-add-in-using-the-setup-wizard"></a><span data-ttu-id="c87de-138">Installer le complément de création de rapports de courrier indésirable à l’aide de l’Assistant Installation</span><span class="sxs-lookup"><span data-stu-id="c87de-138">Install the Junk Email Reporting Add-in using the Setup wizard</span></span>

1. <span data-ttu-id="c87de-139">Sur votre ordinateur, fermez Outlook.</span><span class="sxs-lookup"><span data-stu-id="c87de-139">On your computer, close Outlook.</span></span>

2. <span data-ttu-id="c87de-140">Dans la section **Détails** du [complément Microsoft Junk Email Reporting pour Microsoft Outlook](https://www.microsoft.com/download/details.aspx?id=18275), téléchargez le fichier. msi approprié pour votre version d’Office.</span><span class="sxs-lookup"><span data-stu-id="c87de-140">In the **Details** section at [Microsoft Junk E-mail Reporting Add-In for Microsoft Outlook](https://www.microsoft.com/download/details.aspx?id=18275), download the appropriate .msi file for your version of Office.</span></span>

3. <span data-ttu-id="c87de-141">Double-cliquez sur le fichier .msi.</span><span class="sxs-lookup"><span data-stu-id="c87de-141">Double-click the .msi file.</span></span>

4. <span data-ttu-id="c87de-142">Dans la page **Bienvenue à la configuration du complément Microsoft Junk Email Reporting**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c87de-142">On the **Welcome to Microsoft Junk Email Reporting Add-in Setup** page, click **Next**.</span></span>

5. <span data-ttu-id="c87de-p105">Lisez le contrat de licence, puis, si vous consentez aux conditions d'installation, cliquez sur **J'accepte les termes du contrat de licence** (obligatoire pour continuer l'installation). Cliquez sur **Suivant** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="c87de-p105">Review the license agreement, and then click **I accept the terms in the License Agreement** if you agree to the terms of installation (required to continue installation). Click **Next** to continue.</span></span>

6. <span data-ttu-id="c87de-145">Une fois l'exécution de l'Assistant terminée, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="c87de-145">When the wizard is complete, click **Finish**.</span></span>

7. <span data-ttu-id="c87de-146">Lancez Outlook.</span><span class="sxs-lookup"><span data-stu-id="c87de-146">Start Outlook.</span></span>

8. <span data-ttu-id="c87de-p106">Consultez le bouton **Courrier indésirable** sur votre ruban Outlook. Vous pouvez à présent signaler des messages de courrier indésirable à Microsoft en les sélectionnant dans votre boîte de réception, puis en cliquant sur le bouton permettant de **signaler le courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="c87de-p106">Look for the **Junk** button on your Outlook ribbon. You can now report junk email messages to Microsoft by selecting the junk email messages in your Inbox and clicking the **Report Junk** button.</span></span>

9. <span data-ttu-id="c87de-p107">Cliquez sur la flèche vers le bas en regard du bouton **Courrier indésirable** pour plus d'options, telles que le **signalement en tant que hameçonnage** si vous souhaitez signaler des messages électroniques d'hameçonnage à Microsoft. Dans votre dossier de courrier indésirable, vous pouvez également sélectionner l'option de **signalement en tant que courrier non indésirable** si un message électronique a été identifié à tort comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c87de-p107">Choose the down arrow next to **Junk** for more options such as **Report as Phishing** if you want to report phishing scam emails to Microsoft. In your junk mail folder, you can also select, **Report not junk** if an email was incorrectly identified as junk mail.</span></span>

### <a name="install-the-junk-email-reporting-add-in-using-silent-mode"></a><span data-ttu-id="c87de-151">Installation du complément de création de rapports de courrier indésirable en mode sans assistance</span><span class="sxs-lookup"><span data-stu-id="c87de-151">Install the Junk Email Reporting Add-In using Silent Mode</span></span>

1. <span data-ttu-id="c87de-152">Sur votre ordinateur, fermez Outlook.</span><span class="sxs-lookup"><span data-stu-id="c87de-152">On your computer, close Outlook.</span></span>

2. <span data-ttu-id="c87de-153">Ouvrez une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="c87de-153">Open a command prompt.</span></span>

3. <span data-ttu-id="c87de-154">Pour effectuer une installation simple du complément, sans paramètre facultatif, spécifiez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="c87de-154">If you want to perform a straight installation of the add-in, without any optional parameters, specify the following:</span></span>

   - <span data-ttu-id="c87de-155">Ordinateurs exécutant x86 Outlook :`msiexec /qn /i JunkReportingAdd-in.x86-en.msi`</span><span class="sxs-lookup"><span data-stu-id="c87de-155">Computers running x86 Outlook: `msiexec /qn /i JunkReportingAdd-in.x86-en.msi`</span></span>

   - <span data-ttu-id="c87de-156">Ordinateurs exécutant x64 Outlook :  `msiexec /qn /i JunkReportingAdd-in.x64-en.msi`</span><span class="sxs-lookup"><span data-stu-id="c87de-156">Computers running x64 Outlook:  `msiexec /qn /i JunkReportingAdd-in.x64-en.msi`</span></span>

    <span data-ttu-id="c87de-157">Vous pouvez également spécifier les paramètres facultatifs MaxMessageSelection et BccEmailAddress :</span><span class="sxs-lookup"><span data-stu-id="c87de-157">You can also specify the optional MaxMessageSelection and BccEmailAddress parameters:</span></span>

   - <span data-ttu-id="c87de-p108">MaxMessageSelection Permet aux administrateurs de définir le nombre maximal de messages que les utilisateurs peuvent sélectionner pour soumission en un seul clic. La plage s'étend de 1 à 50 messages, et la valeur par défaut est de 10 messages.</span><span class="sxs-lookup"><span data-stu-id="c87de-p108">MaxMessageSelection Allows administrators to define the maximum number of messages that can be selected by users for submission in a single click. The range is 1 to 50 messages, and the default value is 10 messages.</span></span>

     <span data-ttu-id="c87de-160">Exemple : Si vous voulez définir le nombre maximal de messages qu'un utilisateur peut sélectionner pour soumission en un seul clic sur 16, utilisez l'option suivante dans la commande d'installation :  `MaxMessageSelection=16`</span><span class="sxs-lookup"><span data-stu-id="c87de-160">Example: If you want to set the maximum number of messages that can be selected by users for submission in a single click to 16, use the following option as part of the installation command:  `MaxMessageSelection=16`</span></span>

   - <span data-ttu-id="c87de-p109">BccEmailAddress Permet aux administrateurs de configurer une boîte aux lettres pour recevoir une copie de toutes les soumissions de leurs utilisateurs en définissant une adresse de messagerie Cci. Après configuration de la boîte aux lettres, une copie des tous les messages électroniques soumis est envoyée à l'adresse BccEmailAddress. Autrement, le paramètre par défaut est « pas d'adresse de messagerie Cci ».</span><span class="sxs-lookup"><span data-stu-id="c87de-p109">BccEmailAddress Allows Administrators to set up a mailbox to receive a copy of all their user submissions by setting a Bcc email address. When the mailbox is set up, a copy of all submitted emails will be sent to the BccEmailAddress. Otherwise, the default setting is no Bcc email address.</span></span>

     <span data-ttu-id="c87de-164">Exemple : Si vous voulez utiliser junkReports@contoso.com comme adresse de messagerie Cci pour toutes les soumissions, utilisez la commande suivante :  `BccEmailAddress="junkReports@contoso.com"`</span><span class="sxs-lookup"><span data-stu-id="c87de-164">Example: If you want to use junkReports@contoso.com as the Bcc email address for all submissions, use the following command:  `BccEmailAddress="junkReports@contoso.com"`</span></span>

     > [!NOTE]
     > <span data-ttu-id="c87de-p110">Vous pouvez entrer plusieurs adresses de messagerie Cci en les séparant par des points-virgules. Exemple :  `BccEmailAddress="junkReports@contoso.com; hollyd@treyresearch.net"`</span><span class="sxs-lookup"><span data-stu-id="c87de-p110">You can set multiple Bcc email addresses by entering them with a semicolon delimiter. Example:  `BccEmailAddress="junkReports@contoso.com; hollyd@treyresearch.net"`</span></span>

     <span data-ttu-id="c87de-167">Pour ajouter ces deux paramètres facultatifs en fonction des exemples précédents, exécutez la commande suivante sur un ordinateur exécutant x86 Outlook :</span><span class="sxs-lookup"><span data-stu-id="c87de-167">To add both of these optional parameters based on the previous examples, you would run the following command on a computer running x86 Outlook:</span></span>

     ```
     msiexec /qn /i JunkReportingAdd-in.x86-en.msi. MaxMessageSelection=16 BccEmailAddress="junkReports@contoso.com; hollyd@treyresearch.net"
     ```

4. <span data-ttu-id="c87de-168">Une fois l'installation terminée, lancez Outlook.</span><span class="sxs-lookup"><span data-stu-id="c87de-168">After the installation is complete, start Outlook.</span></span>

5. <span data-ttu-id="c87de-p111">Consultez le bouton **Courrier indésirable** sur votre ruban Outlook. Vous pouvez à présent signaler des messages de courrier indésirable à Microsoft en les sélectionnant dans votre boîte de réception, puis en cliquant sur le bouton permettant de **signaler le courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="c87de-p111">Look for the **Junk** button on your Outlook ribbon. You can now report junk email messages to Microsoft by selecting the junk email messages in your Inbox and clicking the **Report Junk** button.</span></span>

6. <span data-ttu-id="c87de-p112">Cliquez sur la flèche vers le bas en regard du bouton **Courrier indésirable** pour plus d'options, telles que le **signalement en tant que hameçonnage** si vous souhaitez signaler des messages électroniques d'hameçonnage à Microsoft. Dans votre dossier de courrier indésirable, vous pouvez également sélectionner l'option de **signalement en tant que courrier non indésirable** si un message électronique a été identifié à tort comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c87de-p112">Choose the down arrow next to **Junk** for more options such as **Report as Phishing** if you want to report phishing scam emails to Microsoft. In your junk mail folder, you can also select, **Report not junk** if an email was incorrectly identified as junk mail.</span></span>

## <a name="uninstall-the-junk-email-reporting-add-in"></a><span data-ttu-id="c87de-173">Désinstallation du complément Junk Email Reporting</span><span class="sxs-lookup"><span data-stu-id="c87de-173">Uninstall the Junk Email Reporting Add-in</span></span>

<span data-ttu-id="c87de-174">Utilisez l’une des options décrites dans la section suivante pour désinstaller le complément de création de rapports de courrier indésirable :</span><span class="sxs-lookup"><span data-stu-id="c87de-174">Use one of the options described in this to uninstall the Junk Email Reporting Add-in:</span></span>

- <span data-ttu-id="c87de-175">Supprimez le complément à l’aide du panneau de configuration Windows.</span><span class="sxs-lookup"><span data-stu-id="c87de-175">Remove the add-in using Windows Control Panel.</span></span>

- <span data-ttu-id="c87de-176">Exécutez le package Windows Installer, puis sélectionnez l'option de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="c87de-176">Run the Windows installer package and select the uninstall option.</span></span>

- <span data-ttu-id="c87de-177">Exécutez une installation à l'aide de l'option de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="c87de-177">Run a silent installation using the uninstall option.</span></span>

> [!NOTE]
> <span data-ttu-id="c87de-178">Vous devez disposer de droits d'administrateur sur l'ordinateur sur lequel vous désinstallez le complément.</span><span class="sxs-lookup"><span data-stu-id="c87de-178">You must have administrator privileges on the computer on which you are uninstalling the add-in.</span></span>

### <a name="uninstall-the-junk-email-reporting-add-in-from-control-panel"></a><span data-ttu-id="c87de-179">Désinstallation du complément Junk Email Reporting à partir du Panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="c87de-179">Uninstall the Junk Email Reporting Add-in from Control Panel</span></span>

1. <span data-ttu-id="c87de-180">Sur votre ordinateur, fermez Outlook.</span><span class="sxs-lookup"><span data-stu-id="c87de-180">On your computer, close Outlook.</span></span>

2. <span data-ttu-id="c87de-181">Dans le menu Démarrer de votre ordinateur, sélectionnez **Panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="c87de-181">From the Start menu on your computer, select **Control Panel**.</span></span>

3. <span data-ttu-id="c87de-182">Sélectionnez **Programmes et fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="c87de-182">Select **Programs and Features**.</span></span>

4. <span data-ttu-id="c87de-183">Sélectionnez **Complément Microsoft Junk E-mail Reporting pour Microsoft Office Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c87de-183">Select **Microsoft Junk E-mail Reporting Add-In for Microsoft Office Outlook**.</span></span>

5. <span data-ttu-id="c87de-184">Sélectionnez **Désinstaller**.</span><span class="sxs-lookup"><span data-stu-id="c87de-184">Select **Uninstall**.</span></span>

6. <span data-ttu-id="c87de-185">Redémarrez Outlook pour vérifier que le complément ne s'affiche plus dans le ruban Outlook.</span><span class="sxs-lookup"><span data-stu-id="c87de-185">Start Outlook again to confirm that the add-in is no longer displayed on your Outlook ribbon.</span></span>

### <a name="uninstall-the-junk-email-reporting-add-in-by-running-the-windows-installer-package"></a><span data-ttu-id="c87de-186">Désinstallation du complément Junk Email Reporting en exécutant le package Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c87de-186">Uninstall the Junk Email Reporting Add-in by Running the Windows Installer Package</span></span>

1. <span data-ttu-id="c87de-187">Sur votre ordinateur, fermez Outlook.</span><span class="sxs-lookup"><span data-stu-id="c87de-187">On your computer, close Outlook.</span></span>

   > [!NOTE]
   > <span data-ttu-id="c87de-188">Si Outlook est en cours d'exécution durant le processus de désinstallation, vous devrez le redémarrer pour achever la désinstallation du complément.</span><span class="sxs-lookup"><span data-stu-id="c87de-188">If Outlook is running during the uninstall process, it will need to be restarted in order for the add-in to be completely uninstalled.</span></span>

2. <span data-ttu-id="c87de-189">Réexécutez le fichier .msi que vous avez précédemment exécuté pour installer le complément.</span><span class="sxs-lookup"><span data-stu-id="c87de-189">Re-run the .msi file you previously ran to install the add-in.</span></span>

   <span data-ttu-id="c87de-190">(Dans la section **Détails** du [complément Microsoft Junk Email Reporting pour Microsoft Outlook](https://www.microsoft.com/download/details.aspx?id=18275), téléchargez le fichier. msi approprié pour votre version d’Office, puis double-cliquez sur le fichier. msi.)</span><span class="sxs-lookup"><span data-stu-id="c87de-190">(In the **Details** section at [Microsoft Junk E-mail Reporting Add-In for Microsoft Outlook](https://www.microsoft.com/download/details.aspx?id=18275), download the appropriate .msi file for your version of Office, and then double-click the .msi file.)</span></span>

3. <span data-ttu-id="c87de-191">Suivez les invites pour désinstaller le complément.</span><span class="sxs-lookup"><span data-stu-id="c87de-191">Follow the prompts to uninstall the add-in.</span></span>

4. <span data-ttu-id="c87de-192">Redémarrez Outlook pour vérifier que le complément ne s'affiche plus dans le ruban Outlook.</span><span class="sxs-lookup"><span data-stu-id="c87de-192">Start Outlook again to confirm that the add-in is no longer displayed on your Outlook ribbon.</span></span>

### <a name="uninstall-the-junk-email-reporting-add-in-in-silent-mode"></a><span data-ttu-id="c87de-193">Désinstallation du complément Junk Email Reporting en mode sans assistance</span><span class="sxs-lookup"><span data-stu-id="c87de-193">Uninstall the Junk Email Reporting Add-in in Silent Mode</span></span>

1. <span data-ttu-id="c87de-194">Sur votre ordinateur, fermez Outlook.</span><span class="sxs-lookup"><span data-stu-id="c87de-194">On your computer, close Outlook.</span></span>

   > [!NOTE]
   > <span data-ttu-id="c87de-195">Si Outlook est en cours d'exécution durant le processus de désinstallation, vous devrez le redémarrer pour achever la désinstallation du complément.</span><span class="sxs-lookup"><span data-stu-id="c87de-195">If Outlook is running during the uninstall process, it will need to be restarted in order for the add-in to be completely uninstalled.</span></span>

2. <span data-ttu-id="c87de-196">Ouvrez une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="c87de-196">Open a command prompt.</span></span>

3. <span data-ttu-id="c87de-197">Spécifiez le paramètre de ligne de commande suivant :</span><span class="sxs-lookup"><span data-stu-id="c87de-197">Specify the following command line parameter:</span></span>

   <span data-ttu-id="c87de-198">Outlook x86 :`msiexec /x JunkReportingAdd-in.x86-en.msi /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"`</span><span class="sxs-lookup"><span data-stu-id="c87de-198">Outlook x86: `msiexec /x JunkReportingAdd-in.x86-en.msi /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"`</span></span>

   <span data-ttu-id="c87de-199">Outlook x64 :`msiexec /x JunkReportingAdd-in.x64-en.msi /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"`</span><span class="sxs-lookup"><span data-stu-id="c87de-199">Outlook x64: `msiexec /x JunkReportingAdd-in.x64-en.msi /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"`</span></span>

4. <span data-ttu-id="c87de-200">Redémarrez Outlook pour vérifier que le complément ne s'affiche plus dans le ruban Outlook.</span><span class="sxs-lookup"><span data-stu-id="c87de-200">Start Outlook again to confirm that the add-in is no longer displayed on your Outlook ribbon.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="c87de-201">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="c87de-201">For more information</span></span>

[<span data-ttu-id="c87de-202">Signaler les messages de courrier indésirable à Microsoft</span><span class="sxs-lookup"><span data-stu-id="c87de-202">Report junk email messages to Microsoft</span></span>](report-junk-email-messages-to-microsoft.md)

[<span data-ttu-id="c87de-203">Résolution des problèmes et informations de support technique</span><span class="sxs-lookup"><span data-stu-id="c87de-203">Troubleshooting and support information</span></span>](troubleshooting-and-support-information.md)
