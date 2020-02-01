---
title: Activer les étiquettes de confidentialité pour les fichiers Office dans SharePoint et OneDrive
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
audience: Admin
ms.topic: article
ms.date: ''
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: Les administrateurs peuvent activer la prise en charge de l’étiquette de sensibilité pour les fichiers Word, Excel et PowerPoint dans SharePoint et OneDrive.
ms.openlocfilehash: a1b42525984080d56a0f95018003cd251bff0122
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41597501"
---
# <a name="enable-sensitivity-labels-for-office-files-in-sharepoint-and-onedrive-public-preview"></a><span data-ttu-id="11550-103">Activer les étiquettes de confidentialité pour les fichiers Office dans SharePoint et OneDrive (préversion publique)</span><span class="sxs-lookup"><span data-stu-id="11550-103">Enable sensitivity labels for Office files in SharePoint and OneDrive (public preview)</span></span>

<span data-ttu-id="11550-104">Avant cet aperçu, lorsque vous avez appliqué des étiquettes de confidentialité incluant le chiffrement aux fichiers Office stockés dans SharePoint et OneDrive, le service n’a pas pu traiter le contenu de ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="11550-104">Before this preview, when you applied sensitivity labels that included encryption to Office files stored in SharePoint and OneDrive, the service couldn't process the content of these files.</span></span> <span data-ttu-id="11550-105">La co-création, la découverte électronique, la protection contre la perte de données, la recherche, l’Delve et d’autres fonctionnalités collaboratives ne fonctionnaient pas dans ces circonstances.</span><span class="sxs-lookup"><span data-stu-id="11550-105">Coauthoring, eDiscovery, Data Loss Prevention, search, Delve, and other collaborative features didn't work under these circumstances.</span></span> <span data-ttu-id="11550-106">Cet aperçu active ces fonctionnalités lorsque le chiffrement a été appliqué à l’aide d’une clé basée sur le Cloud :</span><span class="sxs-lookup"><span data-stu-id="11550-106">This preview enables these features when the encryption has been applied with a cloud-based key:</span></span>

- <span data-ttu-id="11550-107">SharePoint reconnaît les étiquettes de confidentialité appliquées aux fichiers Word, Excel et PowerPoint dans SharePoint et OneDrive.</span><span class="sxs-lookup"><span data-stu-id="11550-107">SharePoint recognizes sensitivity labels applied to Word, Excel, and PowerPoint files in SharePoint and OneDrive.</span></span> <span data-ttu-id="11550-108">SharePoint applique également les paramètres qui correspondent à chaque étiquette.</span><span class="sxs-lookup"><span data-stu-id="11550-108">SharePoint also enforces the settings that correspond with each label.</span></span>

- <span data-ttu-id="11550-109">Lorsque vous téléchargez un fichier à partir de SharePoint ou de OneDrive, l’étiquette de sensibilité se déplace avec le fichier et les paramètres restent appliqués.</span><span class="sxs-lookup"><span data-stu-id="11550-109">When you download a file from SharePoint or OneDrive, the sensitivity label travels with the file and the settings remain enforced.</span></span>

- <span data-ttu-id="11550-110">Appliquer des étiquettes de confidentialité aux fichiers Office, et ouvrir et modifier les fichiers sur lesquels des étiquettes de sensibilité sont appliquées (si les autorisations de l’étiquette le permettent) à l’aide des versions Web de Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="11550-110">Apply sensitivity labels to Office files, and open and edit files that have sensitivity labels applied (if the label's permissions allow it) by using the web versions of Word, Excel, and PowerPoint.</span></span> <span data-ttu-id="11550-111">Avec Word sur le Web, vous pouvez également utiliser l’étiquetage automatique lorsque vous modifiez des documents.</span><span class="sxs-lookup"><span data-stu-id="11550-111">With Word on the web, you can also use auto labeling when you edit documents.</span></span>

- <span data-ttu-id="11550-112">Office 365 eDiscovery prend en charge la recherche en texte intégral dans les fichiers sur lesquels des étiquettes de sensibilité sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="11550-112">Office 365 eDiscovery supports full-text search in files that have sensitivity labels applied.</span></span> <span data-ttu-id="11550-113">Les stratégies de protection contre la perte de données couvrent le contenu de ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="11550-113">Data Loss Prevention (DLP) policies cover content in these files.</span></span>

- <span data-ttu-id="11550-114">Trois nouveaux événements d’audit sont disponibles pour la surveillance des étiquettes de confidentialité :</span><span class="sxs-lookup"><span data-stu-id="11550-114">Three new audit events are available for monitoring sensitivity labels:</span></span>
  - <span data-ttu-id="11550-115">FileSensitivityApplied</span><span class="sxs-lookup"><span data-stu-id="11550-115">FileSensitivityApplied</span></span>
  - <span data-ttu-id="11550-116">FileSensitivityLabelChanged</span><span class="sxs-lookup"><span data-stu-id="11550-116">FileSensitivityLabelChanged</span></span>
  - <span data-ttu-id="11550-117">FileSensitivityLabelRemoved</span><span class="sxs-lookup"><span data-stu-id="11550-117">FileSensitivityLabelRemoved</span></span>

> [!NOTE]
> <span data-ttu-id="11550-118">Si le chiffrement n’a pas été appliqué avec une clé basée sur le Cloud, mais une clé locale, une topologie de gestion de clés est souvent appelée « conserver votre propre clé » (HYOK), le comportement de SharePoint ne change pas avec cet aperçu.</span><span class="sxs-lookup"><span data-stu-id="11550-118">If encryption hasn't been applied with a cloud-based key but an on-premises key, a key management topology often referred to as "hold your own key" (HYOK), the SharePoint behavior doesn't change with this preview.</span></span> 

<span data-ttu-id="11550-119">Vous pouvez également appliquer des étiquettes de confidentialité à Microsoft Teams, aux groupes Office 365 et aux sites SharePoint.</span><span class="sxs-lookup"><span data-stu-id="11550-119">You can also now apply sensitivity labels to Microsoft Teams, Office 365 groups, and SharePoint sites.</span></span> <span data-ttu-id="11550-120">Pour plus d’informations sur cet aperçu distinct, voir [use sensitive labels with Microsoft Teams, Office 365 Groups et SharePoint sites (public Preview)](sensitivity-labels-teams-groups-sites.md).</span><span class="sxs-lookup"><span data-stu-id="11550-120">For more information about this separate preview, see [Use sensitivity labels with Microsoft Teams, Office 365 groups, and SharePoint sites (public preview)](sensitivity-labels-teams-groups-sites.md).</span></span>

<span data-ttu-id="11550-121">Vous pouvez toujours choisir de désactiver cet aperçu à tout moment.</span><span class="sxs-lookup"><span data-stu-id="11550-121">You always have the choice to opt out of this preview at any time.</span></span>

<span data-ttu-id="11550-122">Regardez la vidéo suivante (pas de son) pour voir ces nouvelles fonctionnalités en action :</span><span class="sxs-lookup"><span data-stu-id="11550-122">Watch the following video (no audio) to see these new capabilities in action:</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed//RE4ornZ]

## <a name="requirements"></a><span data-ttu-id="11550-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11550-123">Requirements</span></span>

<span data-ttu-id="11550-124">Ces fonctionnalités fonctionnent avec les [étiquettes de confidentialité](sensitivity-labels.md) uniquement.</span><span class="sxs-lookup"><span data-stu-id="11550-124">These features work with [sensitivity labels](sensitivity-labels.md) only.</span></span> <span data-ttu-id="11550-125">Si vous disposez actuellement d’étiquettes Azure information protection, commencez par les migrer vers les étiquettes de confidentialité afin de pouvoir activer ces fonctionnalités pour les nouveaux fichiers que vous téléchargez.</span><span class="sxs-lookup"><span data-stu-id="11550-125">If you currently have Azure Information Protection labels, first migrate them to sensitivity labels so that you can enable these features for new files that you upload.</span></span> <span data-ttu-id="11550-126">Pour obtenir des instructions, voir [Comment migrer des étiquettes Azure information protection vers des étiquettes de confidentialité unifiée](https://docs.microsoft.com/azure/information-protection/configure-policy-migrate-labels)</span><span class="sxs-lookup"><span data-stu-id="11550-126">For instructions, see [How to migrate Azure Information Protection labels to unified sensitivity labels](https://docs.microsoft.com/azure/information-protection/configure-policy-migrate-labels)</span></span>

<span data-ttu-id="11550-127">Pour cet aperçu, utilisez la version 19.002.0121.0008 ou une version ultérieure de l’application de synchronisation OneDrive sur Windows et la version 19.002.0107.0008 ou ultérieure sur Mac.</span><span class="sxs-lookup"><span data-stu-id="11550-127">For this preview, use the OneDrive sync app version 19.002.0121.0008 or later on Windows, and version 19.002.0107.0008 or later on Mac.</span></span> <span data-ttu-id="11550-128">Ces deux versions ont été publiées le 28 janvier 2019 et sont actuellement publiées sur toutes les sonneries.</span><span class="sxs-lookup"><span data-stu-id="11550-128">Both these versions were released January 28, 2019, and are currently released to all rings.</span></span> <span data-ttu-id="11550-129">Pour plus d’informations, consultez les [notes de publication de OneDrive](https://support.office.com/article/845dcf18-f921-435e-bf28-4e24b95e5fc0).</span><span class="sxs-lookup"><span data-stu-id="11550-129">For more information, see the [OneDrive release notes](https://support.office.com/article/845dcf18-f921-435e-bf28-4e24b95e5fc0).</span></span> <span data-ttu-id="11550-130">Une fois cet aperçu activé, les utilisateurs qui exécutent une version plus ancienne de l’application de synchronisation sont invités à les mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="11550-130">After you enable this preview, users who run an older version of the sync app are prompted to update it.</span></span>

## <a name="limitations"></a><span data-ttu-id="11550-131">Limites</span><span class="sxs-lookup"><span data-stu-id="11550-131">Limitations</span></span>

- <span data-ttu-id="11550-132">Lorsque vous activez cet aperçu, les utilisateurs qui modifient une étiquette en un fichier dans un dossier de synchronisation OneDrive peuvent ne pas être en mesure d’enregistrer les autres modifications qu’ils ont apportées au fichier.</span><span class="sxs-lookup"><span data-stu-id="11550-132">When you enable this preview, users who change a label to a file in a OneDrive Sync folder might be unable to save other changes they make to the file.</span></span>  <span data-ttu-id="11550-133">Les utilisateurs voient un [cercle rouge avec une erreur d’icône en croix blanche](https://support.office.com/article/what-do-the-onedrive-icons-mean-11143026-8000-44f8-aaa9-67c985aa49b3)et ils sont invités à enregistrer les nouvelles modifications en tant que copie distincte.</span><span class="sxs-lookup"><span data-stu-id="11550-133">Users see a [red circle with a white cross icon error](https://support.office.com/article/what-do-the-onedrive-icons-mean-11143026-8000-44f8-aaa9-67c985aa49b3), and they are asked to save new changes as a separate copy.</span></span>  <span data-ttu-id="11550-134">En plus des modifications apportées aux étiquettes par les utilisateurs, le même comportement peut se produire si un administrateur modifie les paramètres d’une étiquette publiée qui est déjà appliquée aux fichiers téléchargés sur le client de synchronisation des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="11550-134">In addition to label changes that are initiated by users, the same behavior can occur if an admin changes settings for a published label that's already applied to files downloaded to users' sync client.</span></span>
    
    <span data-ttu-id="11550-135">Pour éviter de perdre le travail de ces scénarios, effectuez l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="11550-135">To avoid losing work for these scenarios, do one of these actions:</span></span>
    - <span data-ttu-id="11550-136">Pour appliquer des étiquettes, utilisez les versions Web des applications Office.</span><span class="sxs-lookup"><span data-stu-id="11550-136">To apply labels, use the web versions of the Office apps.</span></span>
    - <span data-ttu-id="11550-137">Fermez un fichier après avoir appliqué une étiquette, puis rouvrez le fichier pour effectuer d’autres modifications.</span><span class="sxs-lookup"><span data-stu-id="11550-137">Close a file after you apply a label, and then reopen the file to make other changes.</span></span>

- <span data-ttu-id="11550-138">SharePoint n’applique pas automatiquement les nouvelles étiquettes aux fichiers existants que vous avez déjà chiffrés à l’aide des étiquettes Azure information protection.</span><span class="sxs-lookup"><span data-stu-id="11550-138">SharePoint doesn't automatically apply the new labels to existing files that you've already encrypted using Azure Information Protection labels.</span></span> <span data-ttu-id="11550-139">À la place, pour que les fonctionnalités fonctionnent après avoir activé cet aperçu, effectuez les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="11550-139">Instead, to get the features to work after you enable this preview, complete these tasks:</span></span>
    
    1. <span data-ttu-id="11550-140">Assurez-vous que vous avez déplacé les étiquettes Azure information protection sur les étiquettes de confidentialité et les avez publiées à partir du centre de conformité Microsoft 365 ou du centre d’administration des étiquettes équivalent.</span><span class="sxs-lookup"><span data-stu-id="11550-140">Make sure you have migrated the Azure Information Protection labels to sensitivity labels and published them from the Microsoft 365 compliance center, or equivalent labeling admin center.</span></span>
    
    2. <span data-ttu-id="11550-141">Téléchargez les fichiers et téléchargez-les sur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="11550-141">Download the files and upload them to SharePoint.</span></span>

- <span data-ttu-id="11550-142">SharePoint ne peut pas traiter les fichiers chiffrés lorsque l’étiquette qui a appliqué le chiffrement a l’une des configurations suivantes pour le chiffrement :</span><span class="sxs-lookup"><span data-stu-id="11550-142">SharePoint can't process encrypted files when the label that applied the encryption has either of the following configurations for encryption:</span></span>
    - <span data-ttu-id="11550-143">**Autoriser les utilisateurs à attribuer des autorisations lors de l’application de l’étiquette** et **dans Word, PowerPoint et Excel, inviter les utilisateurs à spécifier des autorisations**</span><span class="sxs-lookup"><span data-stu-id="11550-143">**Let users assign permissions when they apply the label** and **In Word, PowerPoint, and Excel, prompt users to specify permissions**</span></span>
    - <span data-ttu-id="11550-144">**L’accès des utilisateurs au contenu expire** est défini sur une valeur autre que **jamais**.</span><span class="sxs-lookup"><span data-stu-id="11550-144">**User access to content expires** is set to a value other than **Never**.</span></span>

- <span data-ttu-id="11550-145">Pour un document chiffré qui accorde des autorisations de modification à un utilisateur, la copie ne peut pas être bloquée dans les versions Web des applications Office.</span><span class="sxs-lookup"><span data-stu-id="11550-145">For an encrypted document that grants edit permissions to a user, copying can't be blocked in the web versions of the Office apps.</span></span>

- <span data-ttu-id="11550-146">Le site de suivi des documents Azure information protection n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="11550-146">The Azure Information Protection document tracking site is not supported.</span></span>

- <span data-ttu-id="11550-147">Les applications de bureau Office et les applications mobiles ne prennent pas en charge la co-création.</span><span class="sxs-lookup"><span data-stu-id="11550-147">Office desktop apps and mobile apps don't support coauthoring.</span></span> <span data-ttu-id="11550-148">Au lieu de cela, ces applications continuent à ouvrir des fichiers en mode d’édition exclusive.</span><span class="sxs-lookup"><span data-stu-id="11550-148">Instead, these apps continue to open files in exclusive editing mode.</span></span>

- <span data-ttu-id="11550-149">Si une étiquette inclut le chiffrement, la sécurité des applications Cloud Microsoft ne peut pas lire les informations d’étiquette pour les fichiers dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="11550-149">If a label includes encryption, Microsoft Cloud App Security isn't able to read the label information for the files in SharePoint.</span></span>

## <a name="prepare-the-sharepoint-online-management-shell-for-the-preview"></a><span data-ttu-id="11550-150">Préparer SharePoint Online Management Shell pour l’aperçu</span><span class="sxs-lookup"><span data-stu-id="11550-150">Prepare the SharePoint Online Management Shell for the preview</span></span>

<span data-ttu-id="11550-151">Avant d’activer l’aperçu, vérifiez que vous exécutez SharePoint Online Management Shell version 16.0.19418.12000 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="11550-151">Before you enable the preview, ensure that you're running SharePoint Online Management Shell version 16.0.19418.12000 or above.</span></span> <span data-ttu-id="11550-152">Si vous disposez déjà de la dernière version, vous pouvez activer l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="11550-152">If you already have the latest version, you can go ahead and enable the preview.</span></span>

1. <span data-ttu-id="11550-153">Si vous avez installé une version antérieure de SharePoint Online Management Shell à partir de la Galerie PowerShell, vous pouvez mettre à jour le module en exécutant l’applet de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="11550-153">If you have installed a previous version of the SharePoint Online Management Shell from PowerShell gallery, you can update the module by running the following cmdlet.</span></span>

    ```PowerShell
    Update-Module -Name Microsoft.Online.SharePoint.PowerShell
    ```

2. <span data-ttu-id="11550-154">Par ailleurs, si vous avez installé une version antérieure de SharePoint Online Management Shell à partir du centre de téléchargement Microsoft, vous pouvez également accéder à la console **Ajout/suppression de programmes** et désinstaller SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="11550-154">Alternatively, if you have installed a previous version of the SharePoint Online Management Shell from the Microsoft Download Center, you can also go to **Add or remove programs** and uninstall the SharePoint Online Management Shell.</span></span>

3. <span data-ttu-id="11550-155">Dans un navigateur web, accédez à la page du Centre de téléchargement et [Téléchargez la dernière version de SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span><span class="sxs-lookup"><span data-stu-id="11550-155">In a web browser, go to the Download Center page and [Download the latest SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span></span>

4. <span data-ttu-id="11550-156">Sélectionnez votre langue, puis cliquez sur **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="11550-156">Select your language and then click **Download**.</span></span>

5. <span data-ttu-id="11550-157">Choisissez entre le fichier x64 et x86 .msi.</span><span class="sxs-lookup"><span data-stu-id="11550-157">Choose between the x64 and x86 .msi file.</span></span> <span data-ttu-id="11550-158">Téléchargez le fichier x64 si vous exécutez la version 64 bits de Windows ou le fichier x86 si vous exécutez la version 32 bits.</span><span class="sxs-lookup"><span data-stu-id="11550-158">Download the x64 file if you run the 64-bit version of Windows or the x86 file if you run the 32-bit version.</span></span> <span data-ttu-id="11550-159">Si vous ne le Sachez pas, consultez [la version du système d’exploitation Windows que je suis en cours d’exécution ?](https://support.microsoft.com/help/13443/windows-which-operating-system)</span><span class="sxs-lookup"><span data-stu-id="11550-159">If you don’t know, see [Which version of Windows operating system am I running?](https://support.microsoft.com/help/13443/windows-which-operating-system)</span></span>


6. <span data-ttu-id="11550-160">Une fois que vous avez téléchargé le fichier, exécutez le fichier et suivez les étapes de l’Assistant d’installation.</span><span class="sxs-lookup"><span data-stu-id="11550-160">After you have downloaded the file, run the file and follow the steps in the Setup Wizard.</span></span>

## <a name="enable-the-preview-by-using-microsoft-powershell-opt-in"></a><span data-ttu-id="11550-161">Activer l’aperçu à l’aide de Microsoft PowerShell (opt-in)</span><span class="sxs-lookup"><span data-stu-id="11550-161">Enable the preview by using Microsoft PowerShell (opt-in)</span></span>

<span data-ttu-id="11550-162">Pour activer l’aperçu, utilisez l’applet de commande Set-SPOTenant :</span><span class="sxs-lookup"><span data-stu-id="11550-162">To enable the preview, use the Set-SPOTenant cmdlet:</span></span>

1. <span data-ttu-id="11550-163">À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général ou d’administrateur SharePoint dans Office 365, connectez-vous à SharePoint.</span><span class="sxs-lookup"><span data-stu-id="11550-163">Using a work or school account that has global administrator or SharePoint admin privileges in Office 365, connect to SharePoint.</span></span> <span data-ttu-id="11550-164">Pour savoir comment procéder, reportez-vous à l’article [Prise en main de SharePoint Online Management Shell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span><span class="sxs-lookup"><span data-stu-id="11550-164">To learn how, see [Getting started with SharePoint Online Management Shell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span></span>

2. <span data-ttu-id="11550-165">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="11550-165">Run the following command:</span></span>

    ```PowerShell
    Set-SPOTenant -EnableAIPIntegration $true  
    ```

## <a name="schedule-roll-out-after-you-create-or-change-a-sensitivity-label"></a><span data-ttu-id="11550-166">Planifier le déploiement après la création ou la modification d’une étiquette de sensibilité</span><span class="sxs-lookup"><span data-stu-id="11550-166">Schedule roll-out after you create or change a sensitivity label</span></span>

<span data-ttu-id="11550-167">Une fois que vous avez créé ou modifié une étiquette de sensibilité dans le centre de conformité Microsoft 365, publiez-le par étapes.</span><span class="sxs-lookup"><span data-stu-id="11550-167">After you create or change a sensitivity label in the Microsoft 365 compliance center, publish it in stages.</span></span> <span data-ttu-id="11550-168">Si vous publiez des étiquettes qui n’ont pas été entièrement synchronisées, lorsque les utilisateurs appliquent les étiquettes aux fichiers et les chargent sur SharePoint, les fichiers ne peuvent pas être ouverts dans les versions Web des applications Office.</span><span class="sxs-lookup"><span data-stu-id="11550-168">If you publish labels that haven't fully synchronized, when users apply the labels to files and upload them to SharePoint, the files can’t be opened in the web versions of the Office apps.</span></span> <span data-ttu-id="11550-169">La recherche et eDiscovery ne fonctionnent pas non plus pour les fichiers.</span><span class="sxs-lookup"><span data-stu-id="11550-169">Search and eDiscovery also don't work for the files.</span></span>

<span data-ttu-id="11550-170">Nous vous recommandons de suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="11550-170">We recommend that you follow these steps:</span></span>

1. <span data-ttu-id="11550-171">Publiez l’étiquette de confidentialité nouvelle ou modifiée uniquement sur une ou deux personnes.</span><span class="sxs-lookup"><span data-stu-id="11550-171">Publish the new or modified sensitivity label only to one or two people.</span></span>

2. <span data-ttu-id="11550-172">Patientez pendant au moins 24 heures après la publication initiale.</span><span class="sxs-lookup"><span data-stu-id="11550-172">Wait for at least 24 hours after initial publication.</span></span> <span data-ttu-id="11550-173">Vérifiez que l’étiquette est entièrement synchronisée.</span><span class="sxs-lookup"><span data-stu-id="11550-173">Verify that the label has fully synchronized.</span></span>

3. <span data-ttu-id="11550-174">Publiez l’étiquette plus largement.</span><span class="sxs-lookup"><span data-stu-id="11550-174">Publish the label more broadly.</span></span>

## <a name="disable-the-preview-by-using-microsoft-powershell-opt-out"></a><span data-ttu-id="11550-175">Désactiver l’aperçu à l’aide de Microsoft PowerShell (opt-out)</span><span class="sxs-lookup"><span data-stu-id="11550-175">Disable the preview by using Microsoft PowerShell (opt-out)</span></span>

<span data-ttu-id="11550-176">Si vous désactivez cet aperçu, les fichiers que vous avez téléchargés pendant l’aperçu continueront à être protégés par l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="11550-176">If you disable this preview, files that you uploaded during the preview continue to be protected by the label.</span></span> <span data-ttu-id="11550-177">Les paramètres correspondants continuent à être appliqués.</span><span class="sxs-lookup"><span data-stu-id="11550-177">The corresponding settings continue to be enforced.</span></span> <span data-ttu-id="11550-178">Lorsque vous appliquez des étiquettes à de nouveaux fichiers après avoir désactivé l’aperçu, la recherche de texte intégral, la découverte électronique et la co-création ne fonctionneront plus.</span><span class="sxs-lookup"><span data-stu-id="11550-178">When you apply labels to new files after you disable the preview, full-text search, eDiscovery, and coauthoring will no longer work.</span></span>

<span data-ttu-id="11550-179">Pour désactiver l’aperçu, utilisez l’applet de commande Set-SPOTenant :</span><span class="sxs-lookup"><span data-stu-id="11550-179">To disable the preview, use the Set-SPOTenant cmdlet:</span></span>

1. <span data-ttu-id="11550-180">À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général ou d’administrateur SharePoint dans Office 365, connectez-vous à SharePoint.</span><span class="sxs-lookup"><span data-stu-id="11550-180">Using a work or school account that has global administrator or SharePoint admin privileges in Office 365, connect to SharePoint.</span></span> <span data-ttu-id="11550-181">Pour savoir comment procéder, reportez-vous à l’article [Prise en main de SharePoint Online Management Shell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span><span class="sxs-lookup"><span data-stu-id="11550-181">To learn how, see [Getting started with SharePoint Online Management Shell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span></span>

2. <span data-ttu-id="11550-182">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="11550-182">Run the following command:</span></span>

    ```PowerShell
    Set-SPOTenant -EnableAIPIntegration $false
    ```
