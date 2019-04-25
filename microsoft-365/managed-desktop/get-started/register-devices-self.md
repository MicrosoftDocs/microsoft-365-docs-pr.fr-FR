---
title: Inscrire vous-même les appareils dans le bureau géré Microsoft
description: Inscrire des appareils vous-même afin qu'ils puissent être gérés par le bureau géré Microsoft
ms.prod: w10
author: jaimeo
ms.author: jaimeo
ms.localizationpriority: medium
ms.openlocfilehash: 02b3b7ab32ff92304ab27ca8e8c805ade803c971
ms.sourcegitcommit: cf77e4bf69e6ae144563f1e764ea3437ed6fc836
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2019
ms.locfileid: "33296164"
---
# <a name="register-devices-in-microsoft-managed-desktop"></a><span data-ttu-id="22aec-103">Inscrire des appareils dans le bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="22aec-103">Register devices in Microsoft Managed Desktop</span></span>

>[!NOTE]
><span data-ttu-id="22aec-104">Cette rubrique décrit la procédure à suivre pour enregistrer des appareils de manière autonome.</span><span class="sxs-lookup"><span data-stu-id="22aec-104">This topic describes the steps for you to register devices on your own.</span></span> <span data-ttu-id="22aec-105">Le processus pour les partenaires est documenté dans [inscrire les appareils dans Microsoft Managed Desktop pour les partenaires](register-devices-partner.md).</span><span class="sxs-lookup"><span data-stu-id="22aec-105">The process for Partners is documented in [Register devices in Microsoft Managed Desktop for Partners](register-devices-partner.md).</span></span>

<span data-ttu-id="22aec-106">Microsoft maNaged Desktop peut fonctionner avec les nouveaux appareils ou vous pouvez réutiliser des appareils que vous avez peut-être déjà (ce qui vous obligera à les réimager).</span><span class="sxs-lookup"><span data-stu-id="22aec-106">Microsoft Managed Desktop can work with brand-new devices or you can re-use devices you might already have (which will require that you re-image them).</span></span> <span data-ttu-id="22aec-107">Vous pouvez enregistrer des appareils à l'aide de Microsoft maNaged Desktop sur le portail Azure ou gagner en flexibilité à l'aide d'une API.</span><span class="sxs-lookup"><span data-stu-id="22aec-107">You can register devices by using Microsoft Managed Desktop on the Azure Portal or gain flexibility by using an API.</span></span>

## <a name="prepare-to-register-devices"></a><span data-ttu-id="22aec-108">Préparer l'inscription des appareils</span><span class="sxs-lookup"><span data-stu-id="22aec-108">Prepare to register devices</span></span>

<span data-ttu-id="22aec-109">Si vous n'avez pas encore obtenu les appareils que vous souhaitez utiliser, vérifiez [Microsoft Managed Desktop](../service-description/device-list.md) Devices et travaillez avec un partenaire d'appareil pour obtenir des appareils pris en charge.</span><span class="sxs-lookup"><span data-stu-id="22aec-109">If you haven't already obtained the devices you want to use, check [Microsoft Managed Desktop devices](../service-description/device-list.md) and work with a device partner to procure supported devices.</span></span>

<span data-ttu-id="22aec-110">Que vous travailliez avec des périphériques entièrement nouveaux ou que vous réutilisiez des appareils existants, pour les enregistrer auprès du bureau géré Microsoft, vous devez préparer un **fichier CSV**.</span><span class="sxs-lookup"><span data-stu-id="22aec-110">Whether you're working with completely new devices or re-using existing ones, to register them with Microsoft Managed Desktop, you'll need to prepare a **comma-delimited (CSV) file**.</span></span> <span data-ttu-id="22aec-111">Ce fichier doit inclure les informations suivantes pour chaque périphérique:</span><span class="sxs-lookup"><span data-stu-id="22aec-111">This file should include the following information for each device:</span></span>

>[!NOTE]
><span data-ttu-id="22aec-112">Ce format est réservé à l'enregistrement en libre-service.</span><span class="sxs-lookup"><span data-stu-id="22aec-112">This format is for self-service registration only.</span></span> <span data-ttu-id="22aec-113">Le format que les partenaires doivent utiliser est documenté dans [inscrire les appareils dans le bureau géré Microsoft pour les partenaires](register-devices-partner.md).</span><span class="sxs-lookup"><span data-stu-id="22aec-113">The format Partners should use is documented in [Register devices in Microsoft Managed Desktop for Partners](register-devices-partner.md).</span></span>

<span data-ttu-id="22aec-114">Ces valeurs sont utilisées à des fins d'affichage et n'ont pas besoin de faire correspondre exactement les propriétés de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="22aec-114">These values are used for display purposes, and don't need to match properties from the device exactly.</span></span>
- <span data-ttu-id="22aec-115">Fabricant de l'appareil (exemple: SpiralOrbit)</span><span class="sxs-lookup"><span data-stu-id="22aec-115">Device manufacturer (example: SpiralOrbit)</span></span> 
- <span data-ttu-id="22aec-116">Modèle d'appareil (par exemple: ContosoABC)</span><span class="sxs-lookup"><span data-stu-id="22aec-116">Device model (example: ContosoABC)</span></span>
- <span data-ttu-id="22aec-117">Numéro de série du périphérique</span><span class="sxs-lookup"><span data-stu-id="22aec-117">Device serial number</span></span>

<span data-ttu-id="22aec-118">La hachage du matériel doit être une correspondance exacte.</span><span class="sxs-lookup"><span data-stu-id="22aec-118">The hardware hash must be an exact match.</span></span>
- <span data-ttu-id="22aec-119">Hachage matériel</span><span class="sxs-lookup"><span data-stu-id="22aec-119">Hardware hash</span></span>

<span data-ttu-id="22aec-120">Pour obtenir le hachage du matériel, vous pouvez demander de l'aide auprès de votre OEM ou de votre partenaire, ou suivez ces étapes pour chaque appareil:</span><span class="sxs-lookup"><span data-stu-id="22aec-120">To obtain the hardware hash you can ask for help from your OEM or Partner, or follow these steps for each device:</span></span>

1.  <span data-ttu-id="22aec-121">Ouvrez une invite PowerShell avec des droits d'administration.</span><span class="sxs-lookup"><span data-stu-id="22aec-121">Open a PowerShell prompt with administrative rights.</span></span>
2.  <span data-ttu-id="22aec-122">Générer`Install-Script -Name Get-WindowsAutoPilotInfo`</span><span class="sxs-lookup"><span data-stu-id="22aec-122">Run `Install-Script -Name Get-WindowsAutoPilotInfo`</span></span>
3.  <span data-ttu-id="22aec-123">Générer`powershell -ExecutionPolicy Unrestricted Get-WindowsAutopilotInfo -OutputFile <path>\hardwarehash.csv`</span><span class="sxs-lookup"><span data-stu-id="22aec-123">Run `powershell -ExecutionPolicy Unrestricted Get-WindowsAutopilotInfo -OutputFile <path>\hardwarehash.csv`</span></span>


<span data-ttu-id="22aec-124">Vous pouvez également suivre ces étapes sur un nouveau périphérique (avant de passer par OOBE pour la première fois):</span><span class="sxs-lookup"><span data-stu-id="22aec-124">Alternately, you can follow these steps on a brand-new device (before going through OOBE for the first time):</span></span>

1. <span data-ttu-id="22aec-125">Sur un autre appareil, insérez un lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="22aec-125">On a different device, insert a USB drive.</span></span>
2. <span data-ttu-id="22aec-126">Ouvrez une invite PowerShell avec des droits d'administration.</span><span class="sxs-lookup"><span data-stu-id="22aec-126">Open a PowerShell prompt with administrative rights.</span></span>
3. <span data-ttu-id="22aec-127">Générer`Save-Script -Name Get-WindowsAutoPilotInfo -Path <pathToUsb>`</span><span class="sxs-lookup"><span data-stu-id="22aec-127">Run `Save-Script -Name Get-WindowsAutoPilotInfo -Path <pathToUsb>`</span></span>
4. <span data-ttu-id="22aec-128">Activez l'appareil cible, mais ne démarrez pas l'installation.</span><span class="sxs-lookup"><span data-stu-id="22aec-128">Turn on the target device, but do not start the setup experience.</span></span> <span data-ttu-id="22aec-129">Si vous démarrez accidentellement le programme d'installation, vous devrez réinitialiser ou recréer l'image de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="22aec-129">If you accidentally start the setup experience, you'll have to reset or reimage the device.</span></span>
5. <span data-ttu-id="22aec-130">Insérez le lecteur USB, puis appuyez sur MAJ + F10.</span><span class="sxs-lookup"><span data-stu-id="22aec-130">Insert the USB drive, and then press SHIFT + F10.</span></span>
6. <span data-ttu-id="22aec-131">Ouvrez une invite PowerShell avec des droits d'administration, puis `cd <pathToUsb>`exécutez.</span><span class="sxs-lookup"><span data-stu-id="22aec-131">Open a PowerShell prompt with administrative rights, and then run `cd <pathToUsb>`.</span></span>
7. <span data-ttu-id="22aec-132">Générer`Set-ExecutionPolicy -ExecutionPolicy Unrestricted`</span><span class="sxs-lookup"><span data-stu-id="22aec-132">Run `Set-ExecutionPolicy -ExecutionPolicy Unrestricted`</span></span>
8. <span data-ttu-id="22aec-133">Générer`.\Get-WindowsAutoPilotInfo -OutputFile <path>\hardwarehash.csv`</span><span class="sxs-lookup"><span data-stu-id="22aec-133">Run `.\Get-WindowsAutoPilotInfo -OutputFile <path>\hardwarehash.csv`</span></span>
3. <span data-ttu-id="22aec-134">Supprimez le lecteur USB, puis arrêtez l'appareil en exécutant`shutdown -s -t 0`</span><span class="sxs-lookup"><span data-stu-id="22aec-134">Remove the USB drive, and then shut down the device by running `shutdown -s -t 0`</span></span>

>[!IMPORTANT]
><span data-ttu-id="22aec-135">Ne mettez pas sous tension le périphérique cible tant que vous n'avez pas terminé son inscription.</span><span class="sxs-lookup"><span data-stu-id="22aec-135">Do not power on the target device again until you've completed registration for it.</span></span> 

>[!NOTE]
><span data-ttu-id="22aec-136">Pour des raisons de commodité, vous pouvez télécharger un [modèle](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/managed-desktop/get-started/downloads/device-registration-sample-partner.xlsx) pour ce fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="22aec-136">For your convenience, you can download a [template](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/managed-desktop/get-started/downloads/device-registration-sample-partner.xlsx) for this CSV file.</span></span>

<span data-ttu-id="22aec-137">Votre fichier doit inclure exactement les **mêmes en-têtes de colonne** que l'exemple (fabricant, modèle, etc.), mais vos propres données pour les autres lignes.</span><span class="sxs-lookup"><span data-stu-id="22aec-137">Your file needs to include the **exact same column headings** as the sample one (Manufacturer, Model, etc.), but your own data for the other rows.</span></span> <span data-ttu-id="22aec-138">Si vous utilisez le modèle, ouvrez-le dans un outil d'édition de texte tel que le bloc-notes, et pensez à laisser toutes les données de la ligne 1 uniquement, en entrant uniquement les données dans les lignes 2 et ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="22aec-138">If you use the template, open it in a text editing tool such as Notepad, and consider leaving all the data in row 1 alone, only entering data in rows 2 and below.</span></span> 
    
  ```
 Manufacturer,Model,Serial Number,Hardware Hash
  SpiralOrbit,ContosoABC,000000000000,dGhpc2RldmljZWlzYW5tbWRkZXZpY2U
  
  
  ```

>[!NOTE]
><span data-ttu-id="22aec-139">Si vous oubliez de modifier l'un des exemples de données, l'inscription échouera.</span><span class="sxs-lookup"><span data-stu-id="22aec-139">If you forget to change any of the sample data, registration will fail.</span></span>   


## <a name="register-devices-by-using-the-azure-portal"></a><span data-ttu-id="22aec-140">Inscrire des appareils à l'aide du portail Azure</span><span class="sxs-lookup"><span data-stu-id="22aec-140">Register devices by using the Azure Portal</span></span>

<span data-ttu-id="22aec-141">Dans le portail Microsoft maNaged Desktop [Azure](https://aka.ms/mmdportal), sélectionnez **périphériques** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="22aec-141">From the Microsoft Managed Desktop [Azure Portal](https://aka.ms/mmdportal), select **Devices** in the left navigation pane.</span></span> <span data-ttu-id="22aec-142">Sélectionnez **+ inscrire les appareils**; le survol s'ouvre:</span><span class="sxs-lookup"><span data-stu-id="22aec-142">Select **+ Register devices**; the fly-in opens:</span></span>

<span data-ttu-id="22aec-143">[![Entrée brusque après la sélection d'appareils de Registre](images/register-devices-flyin-sterile.png)](images/register-devices-flyin-sterile.png)</span><span class="sxs-lookup"><span data-stu-id="22aec-143">[![Fly-in after selecting Register devices](images/register-devices-flyin-sterile.png)](images/register-devices-flyin-sterile.png)</span></span>


[//]: # (Malheureusement, cela n'est pas vrai. Nous pouvons supprimer cette note, mais la laisser maintenant jusqu'à ce que nous ayons la possibilité de discuter.)

<!--Registering any existing devices with Managed Desktop will completely re-image them; make sure you've backed up any important data prior to starting the registration process.-->


<span data-ttu-id="22aec-145">Procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="22aec-145">Follow these steps:</span></span>

1. <span data-ttu-id="22aec-146">Dans **chargement du fichier**, indiquez le chemin d'accès au fichier CSV que vous avez créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="22aec-146">In **File upload**, provide a path to the CSV file you created previously.</span></span>
2. <span data-ttu-id="22aec-147">Si vous le souhaitez, vous pouvez ajouter un **ID de commande** ou un **ID d'achat** à vos fins de suivi.</span><span class="sxs-lookup"><span data-stu-id="22aec-147">Optionally, you can add an **Order ID** or **Purchase ID** for your own tracking purposes.</span></span> <span data-ttu-id="22aec-148">Il n'y a pas de mise en forme requise pour ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="22aec-148">There are no format requirements for these values.</span></span>
3. <span data-ttu-id="22aec-149">Sélectionnez **inscrire les appareils**.</span><span class="sxs-lookup"><span data-stu-id="22aec-149">Select **Register devices**.</span></span> <span data-ttu-id="22aec-150">Le système ajoute les périphériques à votre liste d'appareils sur le panneau des **appareils**, marqué comme **inscription en attente**.</span><span class="sxs-lookup"><span data-stu-id="22aec-150">The system will add the devices to your list of devices on the **Devices blade**, marked as **Registration Pending**.</span></span> <span data-ttu-id="22aec-151">L'inscription prend généralement moins de 10 minutes et, lorsque le périphérique s'affiche comme **prêt pour l'utilisateur** , ce qui signifie qu'il est prêt et qu'il attend qu'un utilisateur final commence à utiliser.</span><span class="sxs-lookup"><span data-stu-id="22aec-151">Registration typically takes less than 10 minutes, and when successful the device will show as **Ready for user** meaning it's ready and waiting for an end-user to start using.</span></span>


<span data-ttu-id="22aec-152">Vous pouvez surveiller la progression de l'inscription de l'appareil sur la page principale **des périphériques de bureau gérés par Microsoft** .</span><span class="sxs-lookup"><span data-stu-id="22aec-152">You can monitor the progress of device registration on the main **Microsoft Managed Desktop - Devices** page.</span></span> <span data-ttu-id="22aec-153">Les États possibles sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="22aec-153">Possible states reported there include:</span></span>

| <span data-ttu-id="22aec-154">État</span><span class="sxs-lookup"><span data-stu-id="22aec-154">State</span></span> | <span data-ttu-id="22aec-155">Description</span><span class="sxs-lookup"><span data-stu-id="22aec-155">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="22aec-156">Inscription en attente</span><span class="sxs-lookup"><span data-stu-id="22aec-156">Registration pending</span></span> | <span data-ttu-id="22aec-157">L'inscription n'est pas encore terminée.</span><span class="sxs-lookup"><span data-stu-id="22aec-157">Registration is not done yet.</span></span> <span data-ttu-id="22aec-158">RéActivez-vous plus tard.</span><span class="sxs-lookup"><span data-stu-id="22aec-158">Check back later.</span></span> |
| <span data-ttu-id="22aec-159">Échec de l'inscription</span><span class="sxs-lookup"><span data-stu-id="22aec-159">Registration failed</span></span> | <span data-ttu-id="22aec-160">L'inscription n'a pas pu aboutir.</span><span class="sxs-lookup"><span data-stu-id="22aec-160">Registration could not be completed.</span></span> <span data-ttu-id="22aec-161">Pour plus [](register-devices-self.md#troubleshooting) d'informations, rePortez-vous à la rubrique Troubleshooting.</span><span class="sxs-lookup"><span data-stu-id="22aec-161">Refer to [Troubleshooting](register-devices-self.md#troubleshooting) for more information.</span></span> |
| <span data-ttu-id="22aec-162">Prêt pour l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="22aec-162">Ready for user</span></span> | <span data-ttu-id="22aec-163">L'inscription a réussi et l'appareil est maintenant prêt à être remis à l'utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="22aec-163">Registration succeeded and the device is now ready to be delivered to the end user.</span></span> <span data-ttu-id="22aec-164">Microsoft maNaged Desktop les guide tout au long du paramétrage, il n'est donc pas nécessaire d'effectuer d'autres préparatifs.</span><span class="sxs-lookup"><span data-stu-id="22aec-164">Microsoft Managed Desktop will guide them through first time set-up, so there’s no need for you to do any further preparations.</span></span> |
| <span data-ttu-id="22aec-165">Actif</span><span class="sxs-lookup"><span data-stu-id="22aec-165">Active</span></span> | <span data-ttu-id="22aec-166">L'appareil a été remis à l'utilisateur final et il a été enregistré auprès de votre client.</span><span class="sxs-lookup"><span data-stu-id="22aec-166">The device has been delivered to the end user and they have registered with your tenant.</span></span> <span data-ttu-id="22aec-167">Cela indique également qu'ils utilisent régulièrement l'appareil.</span><span class="sxs-lookup"><span data-stu-id="22aec-167">This also indicates that they are regularly using the device.</span></span> |
| <span data-ttu-id="22aec-168">Inactive</span><span class="sxs-lookup"><span data-stu-id="22aec-168">Inactive</span></span> | <span data-ttu-id="22aec-169">L'appareil a été remis à l'utilisateur final et il a été enregistré auprès de votre client.</span><span class="sxs-lookup"><span data-stu-id="22aec-169">The device has been delivered to the end user and they have registered with your tenant.</span></span> <span data-ttu-id="22aec-170">Toutefois, ils n'ont pas utilisé le périphérique récemment (au cours des 7 derniers jours).</span><span class="sxs-lookup"><span data-stu-id="22aec-170">However, they have not used the device recently (in the last 7 days).</span></span>  | 


## <a name="register-devices-by-using-an-api"></a><span data-ttu-id="22aec-171">Inscrire des appareils à l'aide d'une API</span><span class="sxs-lookup"><span data-stu-id="22aec-171">Register devices by using an API</span></span>

<span data-ttu-id="22aec-172">Une API REST est disponible pour vous permettre de bénéficier d'une plus grande flexibilité et d'une répétabilité avec des enregistrements de périphérique fréquemment séparés.</span><span class="sxs-lookup"><span data-stu-id="22aec-172">A REST API is available to allow you greater flexibility and repeatability with frequent separate device registrations.</span></span> <span data-ttu-id="22aec-173">Actuellement, pour utiliser l'API, demandez de l'aide auprès de votre contact Microsoft pour rejoindre un aperçu de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="22aec-173">Currently, to use the API, ask for help from your Microsoft contact to join a preview of this capability.</span></span>



## <a name="troubleshooting"></a><span data-ttu-id="22aec-174">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="22aec-174">Troubleshooting</span></span>

| <span data-ttu-id="22aec-175">Message d’erreur</span><span class="sxs-lookup"><span data-stu-id="22aec-175">Error message</span></span> | <span data-ttu-id="22aec-176">Détails</span><span class="sxs-lookup"><span data-stu-id="22aec-176">Details</span></span> |
|---------------|-------------|
| <span data-ttu-id="22aec-177">Appareil introuvable</span><span class="sxs-lookup"><span data-stu-id="22aec-177">Device not found</span></span> | <span data-ttu-id="22aec-178">Nous n'avons pas pu inscrire cet appareil, car nous n'avons pas pu trouver de correspondance pour le fabricant, le modèle ou le numéro de série fourni.</span><span class="sxs-lookup"><span data-stu-id="22aec-178">We couldn’t register this device because we could not find a match for the provided manufacturer, model, or serial number.</span></span> <span data-ttu-id="22aec-179">Vérifiez ces valeurs auprès de votre fournisseur d'appareils.</span><span class="sxs-lookup"><span data-stu-id="22aec-179">Confirm these values with your device supplier.</span></span> |
| <span data-ttu-id="22aec-180">Appareil introuvable</span><span class="sxs-lookup"><span data-stu-id="22aec-180">Device not found</span></span> | <span data-ttu-id="22aec-181">Nous n'avons pas pu enregistrer cet appareil, car il n'existe pas dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="22aec-181">We couldn’t de-register this device because it does not exist in your organization.</span></span> <span data-ttu-id="22aec-182">Aucune autre action n'est requise.</span><span class="sxs-lookup"><span data-stu-id="22aec-182">No further action required.</span></span> |
| <span data-ttu-id="22aec-183">Hachage matériel non valide</span><span class="sxs-lookup"><span data-stu-id="22aec-183">Hardware hash not valid</span></span> | <span data-ttu-id="22aec-184">Le hachage matériel que vous avez fourni pour cet appareil n'a pas été correctement mis en forme.</span><span class="sxs-lookup"><span data-stu-id="22aec-184">The hardware hash you provided for this device was not formatted correctly.</span></span> <span data-ttu-id="22aec-185">Vérifiez le hachage matériel, puis renvoyez-le.</span><span class="sxs-lookup"><span data-stu-id="22aec-185">Double-check the hardware hash and then resubmit.</span></span> |
| <span data-ttu-id="22aec-186">L'appareil est déjà enregistré</span><span class="sxs-lookup"><span data-stu-id="22aec-186">Device already registered</span></span> | <span data-ttu-id="22aec-187">Ce périphérique est déjà enregistré dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="22aec-187">This device is already registered to your organization.</span></span> <span data-ttu-id="22aec-188">Aucune autre action n'est requise.</span><span class="sxs-lookup"><span data-stu-id="22aec-188">No further action required.</span></span> |
| <span data-ttu-id="22aec-189">Appareil revendiqué par une autre organisation</span><span class="sxs-lookup"><span data-stu-id="22aec-189">Device claimed by another organization</span></span> | <span data-ttu-id="22aec-190">Ce périphérique a déjà été revendiqué par une autre organisation.</span><span class="sxs-lookup"><span data-stu-id="22aec-190">This device has already been claimed by another organization.</span></span> <span data-ttu-id="22aec-191">Vérifiez auprès de votre fournisseur d'appareils.</span><span class="sxs-lookup"><span data-stu-id="22aec-191">Check with your device supplier.</span></span> |
| <span data-ttu-id="22aec-192">Erreur inattendue</span><span class="sxs-lookup"><span data-stu-id="22aec-192">Unexpected error</span></span> | <span data-ttu-id="22aec-193">Votre demande n'a pas pu être traitée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="22aec-193">Your request could not be automatically processed.</span></span> <span data-ttu-id="22aec-194">Contactez le support technique et indiquez l'ID de la demande:<requestId></span><span class="sxs-lookup"><span data-stu-id="22aec-194">Contact Support and provide the Request ID: <requestId></span></span> |




