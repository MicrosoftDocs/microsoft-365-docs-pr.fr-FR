---
title: Activer les étiquettes de confidentialité pour les fichiers Office dans SharePoint et OneDrive
ms.author: cabailey
author: cabailey
manager: laurawi
audience: Admin
ms.topic: article
ms.date: 11/01/2019
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: Les administrateurs peuvent activer la prise en charge de l’étiquette de sensibilité pour les fichiers Word, Excel et PowerPoint dans SharePoint et OneDrive.
ms.openlocfilehash: c62db0d77ed805c607e79bf25cb9816a554cb6d2
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40802827"
---
# <a name="enable-sensitivity-labels-for-office-files-in-sharepoint-and-onedrive-public-preview"></a><span data-ttu-id="0092d-103">Activer les étiquettes de confidentialité pour les fichiers Office dans SharePoint et OneDrive (préversion publique)</span><span class="sxs-lookup"><span data-stu-id="0092d-103">Enable sensitivity labels for Office files in SharePoint and OneDrive (public preview)</span></span>

<span data-ttu-id="0092d-104">Auparavant, lorsque vous appliquiez des étiquettes de confidentialité incluant le chiffrement aux fichiers Office stockés dans SharePoint et OneDrive, le service n’a pas pu traiter le contenu de ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="0092d-104">Previously, when you applied sensitivity labels that included encryption to Office files stored in SharePoint and OneDrive, the service couldn't process the content of these files.</span></span> <span data-ttu-id="0092d-105">La co-création, la découverte électronique, la protection contre la perte de données, la recherche, l’Delve et d’autres fonctionnalités collaboratives ne fonctionnaient pas dans ces circonstances.</span><span class="sxs-lookup"><span data-stu-id="0092d-105">Coauthoring, eDiscovery, Data Loss Prevention, search, Delve, and other collaborative features didn't work under these circumstances.</span></span> <span data-ttu-id="0092d-106">Cet aperçu permet d’activer les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="0092d-106">This preview enables these features:</span></span>

- <span data-ttu-id="0092d-107">SharePoint reconnaît les étiquettes de confidentialité appliquées aux fichiers Word, Excel et PowerPoint dans SharePoint et OneDrive.</span><span class="sxs-lookup"><span data-stu-id="0092d-107">SharePoint recognizes sensitivity labels applied to Word, Excel, and PowerPoint files in SharePoint and OneDrive.</span></span> <span data-ttu-id="0092d-108">SharePoint applique également les paramètres qui correspondent à chaque étiquette.</span><span class="sxs-lookup"><span data-stu-id="0092d-108">SharePoint also enforces the settings that correspond with each label.</span></span>

- <span data-ttu-id="0092d-109">Lorsque vous téléchargez un fichier à partir de SharePoint ou de OneDrive, l’étiquette de sensibilité se déplace avec le fichier et les paramètres restent appliqués.</span><span class="sxs-lookup"><span data-stu-id="0092d-109">When you download a file from SharePoint or OneDrive, the sensitivity label travels with the file and the settings remain enforced.</span></span>

- <span data-ttu-id="0092d-110">Appliquer des étiquettes de confidentialité aux fichiers Office, et ouvrir et modifier les fichiers sur lesquels des étiquettes de sensibilité sont appliquées (si les autorisations de l’étiquette le permettent) à l’aide des versions Web de Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="0092d-110">Apply sensitivity labels to Office files, and open and edit files that have sensitivity labels applied (if the label's permissions allow it) by using the web versions of Word, Excel, and PowerPoint.</span></span> <span data-ttu-id="0092d-111">Avec Word sur le Web, vous pouvez également utiliser l’étiquetage automatique lorsque vous modifiez des documents.</span><span class="sxs-lookup"><span data-stu-id="0092d-111">With Word on the web, you can also use Auto labeling when you edit documents.</span></span>

- <span data-ttu-id="0092d-112">Office 365 eDiscovery prend en charge la recherche en texte intégral dans les fichiers sur lesquels des étiquettes de sensibilité sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="0092d-112">Office 365 eDiscovery supports full-text search in files that have sensitivity labels applied.</span></span> <span data-ttu-id="0092d-113">Les stratégies de protection contre la perte de données couvrent le contenu de ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="0092d-113">Data Loss Prevention (DLP) policies cover content in these files.</span></span>

- <span data-ttu-id="0092d-114">Trois nouveaux événements d’audit sont disponibles pour la surveillance des étiquettes de confidentialité :</span><span class="sxs-lookup"><span data-stu-id="0092d-114">Three new audit events are available for monitoring sensitivity labels:</span></span>
  - <span data-ttu-id="0092d-115">FileSensitivityApplied</span><span class="sxs-lookup"><span data-stu-id="0092d-115">FileSensitivityApplied</span></span>
  - <span data-ttu-id="0092d-116">FileSensitivityLabelChanged</span><span class="sxs-lookup"><span data-stu-id="0092d-116">FileSensitivityLabelChanged</span></span>
  - <span data-ttu-id="0092d-117">FileSensitivityLabelRemoved</span><span class="sxs-lookup"><span data-stu-id="0092d-117">FileSensitivityLabelRemoved</span></span>

<span data-ttu-id="0092d-118">Vous pouvez également appliquer des étiquettes de confidentialité à Microsoft Teams, aux groupes Office 365 et aux sites SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0092d-118">You can also now apply sensitivity labels to Microsoft Teams, Office 365 groups, and SharePoint sites.</span></span> <span data-ttu-id="0092d-119">[En savoir plus](sensitivity-labels-teams-groups-sites.md).</span><span class="sxs-lookup"><span data-stu-id="0092d-119">[Learn more](sensitivity-labels-teams-groups-sites.md).</span></span>

<span data-ttu-id="0092d-120">Si nécessaire, vous pouvez désactiver l’aperçu à tout moment.</span><span class="sxs-lookup"><span data-stu-id="0092d-120">If necessary, you can opt out of the preview at any time.</span></span>

## <a name="requirements"></a><span data-ttu-id="0092d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0092d-121">Requirements</span></span>

<span data-ttu-id="0092d-122">Ces fonctionnalités ne fonctionnent qu’avec des [étiquettes de sensibilité](sensitivity-labels.md).</span><span class="sxs-lookup"><span data-stu-id="0092d-122">These features work only with [sensitivity labels](sensitivity-labels.md).</span></span> <span data-ttu-id="0092d-123">Si vous avez utilisé des étiquettes Azure information protection, vous pouvez les convertir en étiquettes de sensibilité pour activer ces fonctionnalités pour les nouveaux fichiers que vous téléchargez.</span><span class="sxs-lookup"><span data-stu-id="0092d-123">If you used Azure Information Protection labels, you can convert them to sensitivity labels to enable these features for new files that you upload.</span></span> [<span data-ttu-id="0092d-124">Découvrez comment</span><span class="sxs-lookup"><span data-stu-id="0092d-124">Learn how</span></span>](https://docs.microsoft.com/azure/information-protection/configure-policy-migrate-labels)

<span data-ttu-id="0092d-125">Pour cet aperçu, utilisez la version 19.002.0121.0008 ou une version ultérieure de l’application de synchronisation OneDrive sur Windows et la version 19.002.0107.0008 ou ultérieure sur Mac.</span><span class="sxs-lookup"><span data-stu-id="0092d-125">For this preview, use the OneDrive sync app version 19.002.0121.0008 or later on Windows and version 19.002.0107.0008 or later on Mac.</span></span> <span data-ttu-id="0092d-126">Ces deux versions ont été publiées le 28 janvier 2019 et sont actuellement publiées sur toutes les sonneries.</span><span class="sxs-lookup"><span data-stu-id="0092d-126">Both of these versions were released on January 28, 2019, and are currently released to all rings.</span></span> <span data-ttu-id="0092d-127">[Consultez les notes de publication de OneDrive](https://support.office.com/article/845dcf18-f921-435e-bf28-4e24b95e5fc0).</span><span class="sxs-lookup"><span data-stu-id="0092d-127">[See the OneDrive release notes](https://support.office.com/article/845dcf18-f921-435e-bf28-4e24b95e5fc0).</span></span> <span data-ttu-id="0092d-128">Une fois cet aperçu activé, les utilisateurs qui exécutent une version plus ancienne de l’application de synchronisation sont invités à les mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="0092d-128">After you enable this preview, users who run an older version of the sync app will be prompted to update it.</span></span>

## <a name="limitations"></a><span data-ttu-id="0092d-129">Limites</span><span class="sxs-lookup"><span data-stu-id="0092d-129">Limitations</span></span>

- <span data-ttu-id="0092d-130">Lorsque vous activez cet aperçu, les utilisateurs qui appliquent une étiquette à un fichier à l’aide du bureau ou des applications mobiles Office peuvent ne pas être en mesure d’enregistrer les autres modifications qu’ils ont apportées au fichier.</span><span class="sxs-lookup"><span data-stu-id="0092d-130">When you enable this preview, users who apply a label to a file by using the Office desktop or mobile apps might be unable to save other changes they make to the file.</span></span> <span data-ttu-id="0092d-131">Au lieu de cela, l’application invite les utilisateurs à enregistrer les modifications locales ou à les ignorer.</span><span class="sxs-lookup"><span data-stu-id="0092d-131">Instead, the app prompts users to Save As or Discard local changes.</span></span> <span data-ttu-id="0092d-132">Pour éviter de perdre le travail, effectuez l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0092d-132">To avoid losing work, do one of these actions:</span></span>

  - <span data-ttu-id="0092d-133">Pour appliquer des étiquettes, utilisez les versions Web des applications Office.</span><span class="sxs-lookup"><span data-stu-id="0092d-133">To apply labels, use the web versions of the Office apps.</span></span>

  - <span data-ttu-id="0092d-134">Fermez un fichier après avoir appliqué une étiquette, puis rouvrez le fichier pour effectuer d’autres modifications.</span><span class="sxs-lookup"><span data-stu-id="0092d-134">Close a file after you apply a label and then reopen the file to make other changes.</span></span>

- <span data-ttu-id="0092d-135">SharePoint n’applique pas automatiquement les nouvelles étiquettes aux fichiers existants que vous avez déjà chiffrés à l’aide des étiquettes Azure information protection.</span><span class="sxs-lookup"><span data-stu-id="0092d-135">SharePoint doesn't automatically apply the new labels to existing files that you've already encrypted using Azure Information Protection labels.</span></span> <span data-ttu-id="0092d-136">À la place, pour que les fonctionnalités fonctionnent après avoir activé cet aperçu, effectuez les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="0092d-136">Instead, to get the features to work after you enable this preview, complete these tasks:</span></span>

  - <span data-ttu-id="0092d-137">Convertissez les étiquettes Azure information protection en étiquettes de sensibilité.</span><span class="sxs-lookup"><span data-stu-id="0092d-137">Convert the Azure Information Protection labels to sensitivity labels.</span></span>

  - <span data-ttu-id="0092d-138">Téléchargez les fichiers et téléchargez-les sur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0092d-138">Download the files and upload them to SharePoint.</span></span>

- <span data-ttu-id="0092d-139">SharePoint ne peut pas traiter les étiquettes avec des autorisations et des étiquettes personnalisées avec des dates d’expiration.</span><span class="sxs-lookup"><span data-stu-id="0092d-139">SharePoint can't process labels with custom permissions and labels with expiration dates.</span></span>

- <span data-ttu-id="0092d-140">Lorsque les utilisateurs disposent d’autorisations de modification, les versions Web des applications Office autorisent la copie, quel que soit le paramètre de stratégie copier dans l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="0092d-140">When users have edit permissions, the web versions of the Office apps allow copying regardless of the copy policy setting in the label.</span></span>

- <span data-ttu-id="0092d-141">La révocation RMS, le suivi et la création de rapports ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0092d-141">RMS revocation, tracking, and reporting are unsupported.</span></span>

- <span data-ttu-id="0092d-142">Les applications de bureau Office et les applications mobiles ne prennent pas en charge la co-création.</span><span class="sxs-lookup"><span data-stu-id="0092d-142">Office desktop apps and mobile apps don't support coauthoring.</span></span> <span data-ttu-id="0092d-143">Au lieu de cela, ces applications continuent à ouvrir des fichiers en mode d’édition exclusive.</span><span class="sxs-lookup"><span data-stu-id="0092d-143">Instead, these apps continue to open files in exclusive editing mode.</span></span>

- <span data-ttu-id="0092d-144">Si une étiquette inclut le chiffrement, la sécurité des applications Cloud Microsoft ne peut pas lire les informations d’étiquette pour les fichiers dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0092d-144">If a label includes encryption, Microsoft Cloud App Security isn't able to read the label information for the files in SharePoint.</span></span>

## <a name="prepare-the-sharepoint-online-management-shell-for-the-preview"></a><span data-ttu-id="0092d-145">Préparer SharePoint Online Management Shell pour l’aperçu</span><span class="sxs-lookup"><span data-stu-id="0092d-145">Prepare the SharePoint Online Management Shell for the preview</span></span>

<span data-ttu-id="0092d-146">Avant d’activer l’aperçu, vérifiez que vous exécutez SharePoint Online Management Shell version 16.0.19418.12000 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="0092d-146">Before you enable the preview, ensure that you're running SharePoint Online Management Shell version 16.0.19418.12000 or above.</span></span> <span data-ttu-id="0092d-147">Si vous disposez déjà de la dernière version, vous pouvez activer l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="0092d-147">If you already have the latest version, you can go ahead and enable the preview.</span></span>

1. <span data-ttu-id="0092d-148">Si vous avez installé une version antérieure de SharePoint Online Management Shell à partir de la Galerie PowerShell, vous pouvez mettre à jour le module en exécutant l’applet de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="0092d-148">If you have installed a previous version of the SharePoint Online Management Shell from PowerShell gallery, you can update the module by running the following cmdlet.</span></span>

    ```PowerShell
    Update-Module -Name Microsoft.Online.SharePoint.PowerShell
    ```

2. <span data-ttu-id="0092d-149">Par ailleurs, si vous avez installé une version antérieure de SharePoint Online Management Shell à partir du centre de téléchargement Microsoft, vous pouvez également accéder à la console **Ajout/suppression de programmes** et désinstaller SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="0092d-149">Alternatively, if you have installed a previous version of the SharePoint Online Management Shell from the Microsoft Download Center, you can also go to **Add or remove programs** and uninstall the SharePoint Online Management Shell.</span></span>

3. <span data-ttu-id="0092d-150">Dans un navigateur Web, accédez à la page du centre de téléchargement et [Téléchargez la dernière version de SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span><span class="sxs-lookup"><span data-stu-id="0092d-150">In a web browser, go to the Download Center page and [Download the latest SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span></span>

4. <span data-ttu-id="0092d-151">Sélectionnez votre langue, puis cliquez sur **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="0092d-151">Select your language and then click **Download**.</span></span>

5. <span data-ttu-id="0092d-152">Choisissez entre le fichier x64 et x86. msi.</span><span class="sxs-lookup"><span data-stu-id="0092d-152">Choose between the x64 and x86 .msi file.</span></span> <span data-ttu-id="0092d-153">Téléchargez le fichier x64 si vous exécutez la version 64 bits de Windows ou le fichier x86 si vous exécutez la version 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0092d-153">Download the x64 file if you run the 64-bit version of Windows or the x86 file if you run the 32-bit version.</span></span> <span data-ttu-id="0092d-154">Si vous ne le Sachez pas, consultez [la version du système d’exploitation Windows que je suis en cours d’exécution ?](https://support.microsoft.com/help/13443/windows-which-operating-system)</span><span class="sxs-lookup"><span data-stu-id="0092d-154">If you don’t know, see [Which version of Windows operating system am I running?](https://support.microsoft.com/help/13443/windows-which-operating-system)</span></span>


6. <span data-ttu-id="0092d-155">Une fois que vous avez téléchargé le fichier, exécutez le fichier et suivez les étapes de l’Assistant d’installation.</span><span class="sxs-lookup"><span data-stu-id="0092d-155">After you have downloaded the file, run the file and follow the steps in the Setup Wizard.</span></span>

## <a name="enable-the-preview-by-using-microsoft-powershell-opt-in"></a><span data-ttu-id="0092d-156">Activer l’aperçu à l’aide de Microsoft PowerShell (opt-in)</span><span class="sxs-lookup"><span data-stu-id="0092d-156">Enable the preview by using Microsoft PowerShell (opt-in)</span></span>

<span data-ttu-id="0092d-157">Pour activer l’aperçu, utilisez l’applet de commande Set-SPOTenant :</span><span class="sxs-lookup"><span data-stu-id="0092d-157">To enable the preview, use the Set-SPOTenant cmdlet:</span></span>

1. <span data-ttu-id="0092d-158">À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général ou d’administrateur SharePoint dans Office 365, connectez-vous à SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0092d-158">Using a work or school account that has global administrator or SharePoint admin privileges in Office 365, connect to SharePoint.</span></span> <span data-ttu-id="0092d-159">Pour savoir comment procéder, reportez-vous à l’article [Prise en main de SharePoint Online Management Shell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span><span class="sxs-lookup"><span data-stu-id="0092d-159">To learn how, see [Getting started with SharePoint Online Management Shell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span></span>

2. <span data-ttu-id="0092d-160">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0092d-160">Run the following command:</span></span>

    ```PowerShell
    Set-SPOTenant -EnableAIPIntegration $true  
    ```

## <a name="schedule-roll-out-after-you-create-or-change-a-sensitivity-label"></a><span data-ttu-id="0092d-161">Planifier le déploiement après la création ou la modification d’une étiquette de sensibilité</span><span class="sxs-lookup"><span data-stu-id="0092d-161">Schedule roll-out after you create or change a sensitivity label</span></span>

<span data-ttu-id="0092d-162">Une fois que vous avez créé ou modifié une étiquette de sensibilité dans le centre de conformité Microsoft 365, publiez-le par étapes.</span><span class="sxs-lookup"><span data-stu-id="0092d-162">After you create or change a sensitivity label in the Microsoft 365 compliance center, publish it in stages.</span></span> <span data-ttu-id="0092d-163">Si vous publiez des étiquettes qui n’ont pas été entièrement synchronisées, lorsque les utilisateurs appliquent les étiquettes aux fichiers et les chargent sur SharePoint, les fichiers ne peuvent pas être ouverts dans les versions Web des applications Office.</span><span class="sxs-lookup"><span data-stu-id="0092d-163">If you publish labels that haven't fully synchronized, when users apply the labels to files and upload them to SharePoint, the files can’t be opened in the web versions of the Office apps.</span></span> <span data-ttu-id="0092d-164">La recherche et eDiscovery ne fonctionnent pas non plus pour les fichiers.</span><span class="sxs-lookup"><span data-stu-id="0092d-164">Search and eDiscovery also don't work for the files.</span></span>

<span data-ttu-id="0092d-165">Nous vous recommandons de suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0092d-165">We recommend that you follow these steps:</span></span>

1. <span data-ttu-id="0092d-166">Publiez l’étiquette de confidentialité nouvelle ou modifiée uniquement sur une ou deux personnes.</span><span class="sxs-lookup"><span data-stu-id="0092d-166">Publish the new or modified sensitivity label only to one or two people.</span></span>

2. <span data-ttu-id="0092d-167">Patientez pendant au moins 24 heures après la publication initiale.</span><span class="sxs-lookup"><span data-stu-id="0092d-167">Wait for at least 24 hours after initial publication.</span></span> <span data-ttu-id="0092d-168">Vérifiez que l’étiquette est entièrement synchronisée.</span><span class="sxs-lookup"><span data-stu-id="0092d-168">Verify that the label has fully synchronized.</span></span>

3. <span data-ttu-id="0092d-169">Publiez l’étiquette plus largement.</span><span class="sxs-lookup"><span data-stu-id="0092d-169">Publish the label more broadly.</span></span>

## <a name="disable-the-preview-by-using-microsoft-powershell-opt-out"></a><span data-ttu-id="0092d-170">Désactiver l’aperçu à l’aide de Microsoft PowerShell (opt-out)</span><span class="sxs-lookup"><span data-stu-id="0092d-170">Disable the preview by using Microsoft PowerShell (opt-out)</span></span>

<span data-ttu-id="0092d-171">Si vous désactivez cet aperçu, les fichiers que vous avez téléchargés pendant l’aperçu continueront à être protégés par l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="0092d-171">If you disable this preview, files that you uploaded during the preview continue to be protected by the label.</span></span> <span data-ttu-id="0092d-172">Les paramètres correspondants continuent à être appliqués.</span><span class="sxs-lookup"><span data-stu-id="0092d-172">The corresponding settings continue to be enforced.</span></span> <span data-ttu-id="0092d-173">Lorsque vous appliquez des étiquettes à de nouveaux fichiers après avoir désactivé l’aperçu, la recherche de texte intégral, la découverte électronique et la co-création ne fonctionneront plus.</span><span class="sxs-lookup"><span data-stu-id="0092d-173">When you apply labels to new files after you disable the preview, full-text search, eDiscovery, and coauthoring will no longer work.</span></span>

<span data-ttu-id="0092d-174">Pour désactiver l’aperçu, utilisez l’applet de commande Set-SPOTenant :</span><span class="sxs-lookup"><span data-stu-id="0092d-174">To disable the preview, use the Set-SPOTenant cmdlet:</span></span>

1. <span data-ttu-id="0092d-175">À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général ou d’administrateur SharePoint dans Office 365, connectez-vous à SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0092d-175">Using a work or school account that has global administrator or SharePoint admin privileges in Office 365, connect to SharePoint.</span></span> <span data-ttu-id="0092d-176">Pour savoir comment procéder, reportez-vous à l’article [Prise en main de SharePoint Online Management Shell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span><span class="sxs-lookup"><span data-stu-id="0092d-176">To learn how, see [Getting started with SharePoint Online Management Shell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span></span>

2. <span data-ttu-id="0092d-177">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0092d-177">Run the following command:</span></span>

    ```PowerShell
    Set-SPOTenant -EnableAIPIntegration $false
    ```
