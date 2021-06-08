---
title: Microsoft Defender for Endpoint Device Control Printer Protection
description: Microsoft Defender pour endpoint Device Control Printer Protection empêche les personnes d’imprimer via des imprimantes non d’entreprise ou des imprimantes USB non approuvées.
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.localizationpriority: medium
ms.author: v-lsaldanha
author: lovina-saldanha
ms.reviewer: dansimp
manager: dansimp
audience: ITPro
ms.technology: mde
ms.openlocfilehash: 431497ded684543c33d91c49a0da47e92297321f
ms.sourcegitcommit: e1e275eb88153bafddf93327adf8f82318913a8d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52809229"
---
# <a name="device-control-printer-protection"></a><span data-ttu-id="456c0-103">Protection de l’imprimante des contrôles d’appareil</span><span class="sxs-lookup"><span data-stu-id="456c0-103">Device Control Printer Protection</span></span> 

<span data-ttu-id="456c0-104">Microsoft Defender pour endpoint Device Control Printer Protection empêche les personnes d’imprimer via des imprimantes non d’entreprise ou des imprimantes USB non approuvées.</span><span class="sxs-lookup"><span data-stu-id="456c0-104">Microsoft Defender for Endpoint Device Control Printer Protection blocks people from printing via non-corporate printers or non-approved USB printer.</span></span>

## <a name="licensing"></a><span data-ttu-id="456c0-105">Licence</span><span class="sxs-lookup"><span data-stu-id="456c0-105">Licensing</span></span> 

<span data-ttu-id="456c0-106">Avant de commencer à vous lancer avec printer Protection, vous devez [confirmer votre abonnement Microsoft 365.](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1)</span><span class="sxs-lookup"><span data-stu-id="456c0-106">Before you get started with Printer Protection, you should [confirm your Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1).</span></span> <span data-ttu-id="456c0-107">Pour accéder à printer Protection et l’utiliser, vous devez avoir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="456c0-107">To access and use Printer Protection, you must have the following:</span></span>

- <span data-ttu-id="456c0-108">Microsoft 365 E3 pour le déploiement des fonctionnalités/stratégies</span><span class="sxs-lookup"><span data-stu-id="456c0-108">Microsoft 365 E3 for functionality/policy deployment</span></span> 
- <span data-ttu-id="456c0-109">Microsoft 365 E5 de rapports</span><span class="sxs-lookup"><span data-stu-id="456c0-109">Microsoft 365 E5 for reporting</span></span> 

## <a name="permission"></a><span data-ttu-id="456c0-110">Autorisation</span><span class="sxs-lookup"><span data-stu-id="456c0-110">Permission</span></span> 

<span data-ttu-id="456c0-111">Pour le déploiement de stratégie dans Intune, pour déployer une stratégie via OMA-URI, le compte doit être autorisé à créer, modifier, mettre à jour ou supprimer des profils de configuration d’appareil.</span><span class="sxs-lookup"><span data-stu-id="456c0-111">For Policy deployment in Intune, to deploy policy via OMA-URI, the account must have permissions to create, edit, update, or delete device configuration profiles.</span></span> <span data-ttu-id="456c0-112">Vous pouvez créer des rôles personnalisés ou utiliser n’importe quel rôle intégré avec les autorisations ci-après :</span><span class="sxs-lookup"><span data-stu-id="456c0-112">You can create custom roles or use any of the built-in roles with these permissions:</span></span>  

- <span data-ttu-id="456c0-113">Rôle gestionnaire de stratégies et de profils.</span><span class="sxs-lookup"><span data-stu-id="456c0-113">Policy and profile Manager role.</span></span> 
- <span data-ttu-id="456c0-114">Ou rôle personnalisé avec les autorisations Créer/Modifier/Mettre à jour/Lecture/Supprimer/Afficher les rapports pour les profils de configuration d’appareil</span><span class="sxs-lookup"><span data-stu-id="456c0-114">Or custom role with Create/Edit/Update/Read/Delete/View Reports permissions turned on for Device Configuration profiles</span></span>  
- <span data-ttu-id="456c0-115">Ou administrateur global</span><span class="sxs-lookup"><span data-stu-id="456c0-115">Or Global admin</span></span>

<span data-ttu-id="456c0-116">Pour afficher les rapports de configuration d’appareil, le compte doit avoir les autorisations d’affichage des rapports.</span><span class="sxs-lookup"><span data-stu-id="456c0-116">To see device configuration reports, the account must have view reports permissions.</span></span> <span data-ttu-id="456c0-117">Vous pouvez créer des rôles personnalisés ou utiliser les rôles intégrés avec les autorisations ci-après :</span><span class="sxs-lookup"><span data-stu-id="456c0-117">You can create custom roles or use the built-in roles with these permissions:</span></span>  

- <span data-ttu-id="456c0-118">Administrateur de sécurité global</span><span class="sxs-lookup"><span data-stu-id="456c0-118">Global security admin</span></span>
- <span data-ttu-id="456c0-119">Administrateur de la sécurité</span><span class="sxs-lookup"><span data-stu-id="456c0-119">Security admin</span></span>
- <span data-ttu-id="456c0-120">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="456c0-120">Security Reader</span></span> 

## <a name="prepare-your-endpoints"></a><span data-ttu-id="456c0-121">Préparer vos points de terminaison</span><span class="sxs-lookup"><span data-stu-id="456c0-121">Prepare your endpoints</span></span>

<span data-ttu-id="456c0-122">Assurez-vous que les Windows 10 que vous prévoyez de déployer Printer Protection pour répondre à ces exigences.</span><span class="sxs-lookup"><span data-stu-id="456c0-122">Make sure that the Windows 10 devices that you plan on deploying Printer Protection to meet these requirements.</span></span>

1. <span data-ttu-id="456c0-123">Rejoignez le programme Insider.</span><span class="sxs-lookup"><span data-stu-id="456c0-123">Join the Insider Program.</span></span>

1. <span data-ttu-id="456c0-124">Les mises à jour Windows suivantes sont installées.</span><span class="sxs-lookup"><span data-stu-id="456c0-124">The following Windows Updates are installed.</span></span> 

    - <span data-ttu-id="456c0-125">For Windows 1809: install Windows Update [KB5003217](https://support.microsoft.com/en-us/topic/may-20-2021-kb5003217-os-build-17763-1971-preview-08687c95-0740-421b-a205-54aa2c716b46)</span><span class="sxs-lookup"><span data-stu-id="456c0-125">For Windows 1809: install Windows Update [KB5003217](https://support.microsoft.com/en-us/topic/may-20-2021-kb5003217-os-build-17763-1971-preview-08687c95-0740-421b-a205-54aa2c716b46)</span></span> 
    - <span data-ttu-id="456c0-126">For Windows 1909: install Windows Update [KB5003212](https://support.microsoft.com/en-us/topic/may-20-2021-kb5003212-os-build-18363-1593-preview-05381524-8380-4b30-b783-e330cad3d4a1)</span><span class="sxs-lookup"><span data-stu-id="456c0-126">For Windows 1909: install Windows Update [KB5003212](https://support.microsoft.com/en-us/topic/may-20-2021-kb5003212-os-build-18363-1593-preview-05381524-8380-4b30-b783-e330cad3d4a1)</span></span>
    - <span data-ttu-id="456c0-127">Pour Windows 2004 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="456c0-127">For Windows 2004 or later</span></span> 
    
1. <span data-ttu-id="456c0-128">Si vous envisagez de déployer une stratégie via une stratégie de groupe, l’appareil doit être MDATP joint ; Si vous envisagez de déployer une stratégie via MEM, l’appareil doit être joint à Intune.</span><span class="sxs-lookup"><span data-stu-id="456c0-128">If you're planning to deploy policy via Group Policy, the device must be MDATP joined; if you're planning to deploy policy via MEM, the device must be Intune joined.</span></span>

## <a name="deploy-device-control-printer-protection-policy"></a><span data-ttu-id="456c0-129">Déployer une stratégie de protection de l’imprimante de contrôle d’appareil</span><span class="sxs-lookup"><span data-stu-id="456c0-129">Deploy Device Control Printer Protection policy</span></span>

<span data-ttu-id="456c0-130">Vous pouvez déployer la stratégie via la stratégie de groupe ou Intune.</span><span class="sxs-lookup"><span data-stu-id="456c0-130">You can deploy the policy via Group Policy or Intune.</span></span>

| <span data-ttu-id="456c0-131">Titre</span><span class="sxs-lookup"><span data-stu-id="456c0-131">Title</span></span> | <span data-ttu-id="456c0-132">Description</span><span class="sxs-lookup"><span data-stu-id="456c0-132">Description</span></span> | <span data-ttu-id="456c0-133">Prise en charge du programme CSP</span><span class="sxs-lookup"><span data-stu-id="456c0-133">CSP Support</span></span> | <span data-ttu-id="456c0-134">Prise en charge des GPO</span><span class="sxs-lookup"><span data-stu-id="456c0-134">GPO Support</span></span> | <span data-ttu-id="456c0-135">Prise en charge basée sur l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="456c0-135">User-based Support</span></span> | <span data-ttu-id="456c0-136">Prise en charge basée sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="456c0-136">Machine-based Support</span></span> |
|:--|:--|:--|:--|:--|:--|
|<span data-ttu-id="456c0-137">**Activer les restrictions d’impression des contrôles d’appareil**</span><span class="sxs-lookup"><span data-stu-id="456c0-137">**Enable Device control Printing Restrictions**</span></span>|<span data-ttu-id="456c0-138">Empêcher les personnes d’imprimer via une imprimante non d’entreprise</span><span class="sxs-lookup"><span data-stu-id="456c0-138">Block people from printing via non-corporate printer</span></span>|<span data-ttu-id="456c0-139">Oui</span><span class="sxs-lookup"><span data-stu-id="456c0-139">Yes</span></span>|<span data-ttu-id="456c0-140">Oui</span><span class="sxs-lookup"><span data-stu-id="456c0-140">Yes</span></span>|<span data-ttu-id="456c0-141">Oui</span><span class="sxs-lookup"><span data-stu-id="456c0-141">Yes</span></span>|<span data-ttu-id="456c0-142">Oui</span><span class="sxs-lookup"><span data-stu-id="456c0-142">Yes</span></span>|
|<span data-ttu-id="456c0-143">**Liste des appareils d’impression connectés usb approuvés**\*</span><span class="sxs-lookup"><span data-stu-id="456c0-143">**List of Approved USB-connected print devices** \*</span></span>|<span data-ttu-id="456c0-144">Autoriser une imprimante USB spécifique</span><span class="sxs-lookup"><span data-stu-id="456c0-144">Allow specific USB printer</span></span>|<span data-ttu-id="456c0-145">Oui</span><span class="sxs-lookup"><span data-stu-id="456c0-145">Yes</span></span>|<span data-ttu-id="456c0-146">Oui</span><span class="sxs-lookup"><span data-stu-id="456c0-146">Yes</span></span>|<span data-ttu-id="456c0-147">Oui</span><span class="sxs-lookup"><span data-stu-id="456c0-147">Yes</span></span>|<span data-ttu-id="456c0-148">Oui</span><span class="sxs-lookup"><span data-stu-id="456c0-148">Yes</span></span>|
|||||||

<span data-ttu-id="456c0-149">\* Cette stratégie doit être utilisée avec les restrictions d’impression **d’activer le contrôle d’appareil**</span><span class="sxs-lookup"><span data-stu-id="456c0-149">\* This policy must be used together with **Enable Device control Printing Restrictions**</span></span>
## <a name="deploy-policy-via-intune"></a><span data-ttu-id="456c0-150">Déployer une stratégie via Intune</span><span class="sxs-lookup"><span data-stu-id="456c0-150">Deploy policy via Intune</span></span> 

<span data-ttu-id="456c0-151">Pour Intune, la protection de l’imprimante de contrôle d’appareil prend uniquement en charge l’OMA-URI.</span><span class="sxs-lookup"><span data-stu-id="456c0-151">For Intune, currently Device Control Printer Protection supports OMA-URI only.</span></span>

<span data-ttu-id="456c0-152">**Scénario 1 : empêcher les personnes d’imprimer via n’importe quelle imprimante non d’entreprise**</span><span class="sxs-lookup"><span data-stu-id="456c0-152">**Scenario 1: Block people from printing via any non-corporate printer**</span></span> 

 - <span data-ttu-id="456c0-153">Appliquez la stratégie sur l’ordinateur :</span><span class="sxs-lookup"><span data-stu-id="456c0-153">Apply policy over machine:</span></span> 

    - <span data-ttu-id="456c0-154">./Vendor/MSFT/Policy/Config/Printers/EnableDeviceControl</span><span class="sxs-lookup"><span data-stu-id="456c0-154">./Vendor/MSFT/Policy/Config/Printers/EnableDeviceControl</span></span> 

- <span data-ttu-id="456c0-155">Appliquez la stratégie à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="456c0-155">Apply policy over user:</span></span> 

    - <span data-ttu-id="456c0-156">./Vendor/MSFT/Policy/Config/Printers/EnableDeviceControlUser</span><span class="sxs-lookup"><span data-stu-id="456c0-156">./Vendor/MSFT/Policy/Config/Printers/EnableDeviceControlUser</span></span> 

<span data-ttu-id="456c0-157">Chaîne de prise en charge du programme CSP avec `` <enabled/>`` :</span><span class="sxs-lookup"><span data-stu-id="456c0-157">The CSP support string with `` <enabled/>``:</span></span> 

:::image type="content" source="../../media/customeditrow.png" alt-text="ligne d’édition personnalisée":::

<span data-ttu-id="456c0-159">**Scénario 2 : autoriser des imprimantes USB approuvées spécifiques**</span><span class="sxs-lookup"><span data-stu-id="456c0-159">**Scenario 2: Allow specific approved USB printers**</span></span>

- <span data-ttu-id="456c0-160">Appliquez la stratégie sur l’ordinateur :</span><span class="sxs-lookup"><span data-stu-id="456c0-160">Apply policy over machine:</span></span> 

    - <span data-ttu-id="456c0-161">./Vendor/MSFT/Policy/Config/Printers/ApprovedUsbPrintDevices</span><span class="sxs-lookup"><span data-stu-id="456c0-161">./Vendor/MSFT/Policy/Config/Printers/ApprovedUsbPrintDevices</span></span> 

- <span data-ttu-id="456c0-162">Appliquez la stratégie à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="456c0-162">Apply policy over user:</span></span> 

    - <span data-ttu-id="456c0-163">./Vendor/MSFT/Policy/Config/Printers/ApprovedUsbPrintDevicesUser</span><span class="sxs-lookup"><span data-stu-id="456c0-163">./Vendor/MSFT/Policy/Config/Printers/ApprovedUsbPrintDevicesUser</span></span>  

<span data-ttu-id="456c0-164">La chaîne de prise en charge du programme CSP avec des imprimantes USB approuvées via la propriété « ApprovedUsbPrintDevices » (par `` <enabled/><data id="ApprovedUsbPrintDevices_List" value="03F0/0853,0351/0872"/>`` exemple :</span><span class="sxs-lookup"><span data-stu-id="456c0-164">The CSP support string with approved USB printers via ‘ApprovedUsbPrintDevices’ property, example `` <enabled/><data id="ApprovedUsbPrintDevices_List" value="03F0/0853,0351/0872"/>``:</span></span> 

:::image type="content" source="../../media/editrow.png" alt-text="modifier la ligne":::

## <a name="deploy-policy-via-group-policy"></a><span data-ttu-id="456c0-166">Déployer une stratégie via une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="456c0-166">Deploy policy via Group Policy</span></span> 

<span data-ttu-id="456c0-167">Si l’appareil n’est pas joint à Intune, vous pouvez également déployer la stratégie via la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="456c0-167">If the device isn't Intune joined, you can also deploy the policy via Group Policy.</span></span> 

<span data-ttu-id="456c0-168">**Scénario 1 : empêcher les personnes d’imprimer via n’importe quelle imprimante non d’entreprise**</span><span class="sxs-lookup"><span data-stu-id="456c0-168">**Scenario 1: Block people from printing via any non-corporate printer**</span></span> 

- <span data-ttu-id="456c0-169">Appliquez la stratégie sur l’ordinateur :</span><span class="sxs-lookup"><span data-stu-id="456c0-169">Apply policy over machine:</span></span> 

    - <span data-ttu-id="456c0-170">Configuration ordinateur > modèles d’administration > imprimante : activer les restrictions d’impression des contrôles d’appareil</span><span class="sxs-lookup"><span data-stu-id="456c0-170">Computer Configuration > Administrative Templates > Printer: Enable Device control Printing Restrictions</span></span> 

- <span data-ttu-id="456c0-171">Appliquez la stratégie à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="456c0-171">Apply policy over user:</span></span> 

    - <span data-ttu-id="456c0-172">Configuration utilisateur > modèles d’administration > Panneau de configuration > imprimantes : activer les restrictions d’impression des contrôles d’appareil</span><span class="sxs-lookup"><span data-stu-id="456c0-172">User Configuration > Administrative Templates > Control Panel > Printers: Enable Device control Printing Restrictions</span></span> 

:::image type="content" source="../../media/enable-device-ctrl-printing-restrictions.png" alt-text="activer les restrictions d’impression d’appareil":::
 

<span data-ttu-id="456c0-174">**Scénario 2 : autoriser des imprimantes USB approuvées spécifiques**</span><span class="sxs-lookup"><span data-stu-id="456c0-174">**Scenario 2: Allow specific approved USB printers**</span></span>

- <span data-ttu-id="456c0-175">Appliquez la stratégie sur l’ordinateur :</span><span class="sxs-lookup"><span data-stu-id="456c0-175">Apply policy over machine:</span></span> 

    - <span data-ttu-id="456c0-176">Configuration ordinateur > modèles d’administration > imprimante : liste des périphériques d’impression connectés USB approuvés</span><span class="sxs-lookup"><span data-stu-id="456c0-176">Computer Configuration > Administrative Templates > Printer:  List of Approved USB-connected print devices</span></span> 

- <span data-ttu-id="456c0-177">Appliquez la stratégie à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="456c0-177">Apply policy over user:</span></span>  

    - <span data-ttu-id="456c0-178">Configuration utilisateur > modèles d’administration > panneau de configuration > imprimantes : liste des périphériques d’impression connectés USB approuvés</span><span class="sxs-lookup"><span data-stu-id="456c0-178">User Configuration > Administrative Templates > Control Panel > Printers: List of Approved USB-connected print devices</span></span> 
 
 :::image type="content" source="../../media/list-of-approved-connected-print-devices.png" alt-text="liste des périphériques d’impression connectés usb approuvés":::

## <a name="view-device-control-printer-protection-data-in-microsoft-defender-for-endpoint-portal"></a><span data-ttu-id="456c0-180">Afficher les données de protection des imprimantes des contrôles d’appareil dans le portail Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="456c0-180">View Device Control Printer Protection data in Microsoft Defender for Endpoint portal</span></span> 

<span data-ttu-id="456c0-181">Le centre [Microsoft 365 de sécurité affiche](https://security.microsoft.com) l’impression bloquée par la stratégie Device Control Printer Protection ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="456c0-181">The [Microsoft 365 security center](https://security.microsoft.com) shows printing blocked by the Device Control Printer Protection policy above.</span></span>
 
```sql
DeviceEvents 

|where ActionType == 'PrintJobBlocked' 

| extend parsed=parse_json(AdditionalFields) 

| extend PrintedFile=tostring(parsed.JobOrDocumentName) 

| extend PrintPortName=tostring(parsed.PortName) 

| extend PrinterName=tostring(parsed.PrinterName) 

| extend Policy=tostring(parsed.RestrictionReason)  

| project Timestamp, DeviceId, DeviceName, ActionType, InitiatingProcessAccountName,Policy, PrintedFile, PrinterName, PrintPortName, AdditionalFields 

| order by Timestamp desc 
```

 :::image type="content" source="../../media/device-control-advanced-hunting.png" alt-text="recherche avancée":::
