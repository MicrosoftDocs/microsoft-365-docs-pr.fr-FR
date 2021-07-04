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
ms.topic: article
ms.openlocfilehash: 0f089efedef1e4fb6b146692da3f1a630f2bacac
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53289690"
---
# <a name="device-control-printer-protection"></a><span data-ttu-id="3d2bf-103">Protection de l’Imprimante de Contrôle d’Appareil</span><span class="sxs-lookup"><span data-stu-id="3d2bf-103">Device Control Printer Protection</span></span>

<span data-ttu-id="3d2bf-104">Microsoft Defender pour endpoint Device Control Printer Protection empêche les personnes d’imprimer via des imprimantes non d’entreprise ou des imprimantes USB non approuvées.</span><span class="sxs-lookup"><span data-stu-id="3d2bf-104">Microsoft Defender for Endpoint Device Control Printer Protection blocks people from printing via non-corporate printers or non-approved USB printer.</span></span>

## <a name="licensing"></a><span data-ttu-id="3d2bf-105">Licences</span><span class="sxs-lookup"><span data-stu-id="3d2bf-105">Licensing</span></span>

<span data-ttu-id="3d2bf-106">Avant de commencer à vous lancer avec printer Protection, vous devez [confirmer votre abonnement Microsoft 365.](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1)</span><span class="sxs-lookup"><span data-stu-id="3d2bf-106">Before you get started with Printer Protection, you should [confirm your Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1).</span></span> <span data-ttu-id="3d2bf-107">Pour accéder à printer Protection et l’utiliser, vous devez avoir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d2bf-107">To access and use Printer Protection, you must have the following:</span></span>

- <span data-ttu-id="3d2bf-108">Microsoft 365 E3 pour le déploiement des fonctionnalités/stratégies</span><span class="sxs-lookup"><span data-stu-id="3d2bf-108">Microsoft 365 E3 for functionality/policy deployment</span></span>
- <span data-ttu-id="3d2bf-109">Microsoft 365 E5 de rapports</span><span class="sxs-lookup"><span data-stu-id="3d2bf-109">Microsoft 365 E5 for reporting</span></span>

## <a name="permission"></a><span data-ttu-id="3d2bf-110">Autorisation</span><span class="sxs-lookup"><span data-stu-id="3d2bf-110">Permission</span></span>

<span data-ttu-id="3d2bf-111">Pour le déploiement de stratégie dans Intune, pour déployer une stratégie via OMA-URI, le compte doit être autorisé à créer, modifier, mettre à jour ou supprimer des profils de configuration d’appareil.</span><span class="sxs-lookup"><span data-stu-id="3d2bf-111">For Policy deployment in Intune, to deploy policy via OMA-URI, the account must have permissions to create, edit, update, or delete device configuration profiles.</span></span> <span data-ttu-id="3d2bf-112">Vous pouvez créer des rôles personnalisés ou utiliser n’importe quel rôle intégré avec les autorisations ci-après :</span><span class="sxs-lookup"><span data-stu-id="3d2bf-112">You can create custom roles or use any of the built-in roles with these permissions:</span></span>

- <span data-ttu-id="3d2bf-113">Rôle gestionnaire de stratégies et de profils.</span><span class="sxs-lookup"><span data-stu-id="3d2bf-113">Policy and profile Manager role.</span></span>
- <span data-ttu-id="3d2bf-114">Ou rôle personnalisé avec les autorisations Créer/Modifier/Mettre à jour/Lecture/Supprimer/Afficher les rapports pour les profils de configuration d’appareil</span><span class="sxs-lookup"><span data-stu-id="3d2bf-114">Or custom role with Create/Edit/Update/Read/Delete/View Reports permissions turned on for Device Configuration profiles</span></span>
- <span data-ttu-id="3d2bf-115">Ou administrateur global</span><span class="sxs-lookup"><span data-stu-id="3d2bf-115">Or Global admin</span></span>

<span data-ttu-id="3d2bf-116">Pour afficher les rapports de configuration d’appareil, le compte doit avoir les autorisations d’affichage des rapports.</span><span class="sxs-lookup"><span data-stu-id="3d2bf-116">To see device configuration reports, the account must have view reports permissions.</span></span> <span data-ttu-id="3d2bf-117">Vous pouvez créer des rôles personnalisés ou utiliser les rôles intégrés avec les autorisations ci-après :</span><span class="sxs-lookup"><span data-stu-id="3d2bf-117">You can create custom roles or use the built-in roles with these permissions:</span></span>

- <span data-ttu-id="3d2bf-118">Administrateur de sécurité global</span><span class="sxs-lookup"><span data-stu-id="3d2bf-118">Global security admin</span></span>
- <span data-ttu-id="3d2bf-119">Administrateur de la sécurité</span><span class="sxs-lookup"><span data-stu-id="3d2bf-119">Security admin</span></span>
- <span data-ttu-id="3d2bf-120">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="3d2bf-120">Security Reader</span></span>

## <a name="prepare-your-endpoints"></a><span data-ttu-id="3d2bf-121">Préparer vos points de terminaison</span><span class="sxs-lookup"><span data-stu-id="3d2bf-121">Prepare your endpoints</span></span>

<span data-ttu-id="3d2bf-122">Assurez-vous que les Windows 10 que vous prévoyez de déployer Printer Protection pour répondre à ces exigences.</span><span class="sxs-lookup"><span data-stu-id="3d2bf-122">Make sure that the Windows 10 devices that you plan on deploying Printer Protection to meet these requirements.</span></span>

1. <span data-ttu-id="3d2bf-123">Rejoignez le programme Insider.</span><span class="sxs-lookup"><span data-stu-id="3d2bf-123">Join the Insider Program.</span></span>

1. <span data-ttu-id="3d2bf-124">Les mises à jour Windows suivantes sont installées.</span><span class="sxs-lookup"><span data-stu-id="3d2bf-124">The following Windows Updates are installed.</span></span>
    - <span data-ttu-id="3d2bf-125">For Windows 1809: install Windows Update [KB5003217](https://support.microsoft.com/topic/may-20-2021-kb5003217-os-build-17763-1971-preview-08687c95-0740-421b-a205-54aa2c716b46)</span><span class="sxs-lookup"><span data-stu-id="3d2bf-125">For Windows 1809: install Windows Update [KB5003217](https://support.microsoft.com/topic/may-20-2021-kb5003217-os-build-17763-1971-preview-08687c95-0740-421b-a205-54aa2c716b46)</span></span>
    - <span data-ttu-id="3d2bf-126">For Windows 1909: install Windows Update [KB5003212](https://support.microsoft.com/topic/may-20-2021-kb5003212-os-build-18363-1593-preview-05381524-8380-4b30-b783-e330cad3d4a1)</span><span class="sxs-lookup"><span data-stu-id="3d2bf-126">For Windows 1909: install Windows Update [KB5003212](https://support.microsoft.com/topic/may-20-2021-kb5003212-os-build-18363-1593-preview-05381524-8380-4b30-b783-e330cad3d4a1)</span></span>
    - <span data-ttu-id="3d2bf-127">Pour Windows 2004 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="3d2bf-127">For Windows 2004 or later</span></span>

1. <span data-ttu-id="3d2bf-128">Si vous envisagez de déployer une stratégie via une stratégie de groupe, l’appareil doit être joint à MDATP . Si vous envisagez de déployer une stratégie via MEM, l’appareil doit être joint à Intune.</span><span class="sxs-lookup"><span data-stu-id="3d2bf-128">If you're planning to deploy policy via Group Policy, the device must be MDATP joined; if you're planning to deploy policy via MEM, the device must be Intune joined.</span></span>

## <a name="deploy-device-control-printer-protection-policy"></a><span data-ttu-id="3d2bf-129">Déployer une stratégie de protection de l’imprimante de contrôle d’appareil</span><span class="sxs-lookup"><span data-stu-id="3d2bf-129">Deploy Device Control Printer Protection policy</span></span>

<span data-ttu-id="3d2bf-130">Vous pouvez déployer la stratégie via la stratégie de groupe ou Intune.</span><span class="sxs-lookup"><span data-stu-id="3d2bf-130">You can deploy the policy via Group Policy or Intune.</span></span>

<br>

****

|<span data-ttu-id="3d2bf-131">Titre</span><span class="sxs-lookup"><span data-stu-id="3d2bf-131">Title</span></span>|<span data-ttu-id="3d2bf-132">Description</span><span class="sxs-lookup"><span data-stu-id="3d2bf-132">Description</span></span>|<span data-ttu-id="3d2bf-133">Prise en charge du programme CSP</span><span class="sxs-lookup"><span data-stu-id="3d2bf-133">CSP Support</span></span> | <span data-ttu-id="3d2bf-134">Prise en charge des GPO</span><span class="sxs-lookup"><span data-stu-id="3d2bf-134">GPO Support</span></span> | <span data-ttu-id="3d2bf-135">Prise en charge basée sur l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="3d2bf-135">User-based Support</span></span> | <span data-ttu-id="3d2bf-136">Prise en charge basée sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="3d2bf-136">Machine-based Support</span></span> |
|---|---|:---:|:---:|:---:|:---:|
|<span data-ttu-id="3d2bf-137">**Activer les restrictions d’impression des contrôles d’appareil**</span><span class="sxs-lookup"><span data-stu-id="3d2bf-137">**Enable Device control Printing Restrictions**</span></span>|<span data-ttu-id="3d2bf-138">Empêcher les personnes d’imprimer via une imprimante non d’entreprise</span><span class="sxs-lookup"><span data-stu-id="3d2bf-138">Block people from printing via non-corporate printer</span></span>|<span data-ttu-id="3d2bf-139">Oui</span><span class="sxs-lookup"><span data-stu-id="3d2bf-139">Yes</span></span>|<span data-ttu-id="3d2bf-140">Oui</span><span class="sxs-lookup"><span data-stu-id="3d2bf-140">Yes</span></span>|<span data-ttu-id="3d2bf-141">Oui</span><span class="sxs-lookup"><span data-stu-id="3d2bf-141">Yes</span></span>|<span data-ttu-id="3d2bf-142">Oui</span><span class="sxs-lookup"><span data-stu-id="3d2bf-142">Yes</span></span>|
|<span data-ttu-id="3d2bf-143">**Liste des appareils d’impression connectés usb approuvés**\*</span><span class="sxs-lookup"><span data-stu-id="3d2bf-143">**List of Approved USB-connected print devices**\*</span></span>|<span data-ttu-id="3d2bf-144">Autoriser une imprimante USB spécifique</span><span class="sxs-lookup"><span data-stu-id="3d2bf-144">Allow specific USB printer</span></span>|<span data-ttu-id="3d2bf-145">Oui</span><span class="sxs-lookup"><span data-stu-id="3d2bf-145">Yes</span></span>|<span data-ttu-id="3d2bf-146">Oui</span><span class="sxs-lookup"><span data-stu-id="3d2bf-146">Yes</span></span>|<span data-ttu-id="3d2bf-147">Oui</span><span class="sxs-lookup"><span data-stu-id="3d2bf-147">Yes</span></span>|<span data-ttu-id="3d2bf-148">Oui</span><span class="sxs-lookup"><span data-stu-id="3d2bf-148">Yes</span></span>|
|

<span data-ttu-id="3d2bf-149">\*Cette stratégie doit être utilisée avec activer les **restrictions d’impression des contrôles d’appareil.**</span><span class="sxs-lookup"><span data-stu-id="3d2bf-149">\* This policy must be used together with **Enable Device control Printing Restrictions**.</span></span>

## <a name="deploy-policy-via-intune"></a><span data-ttu-id="3d2bf-150">Déployer une stratégie via Intune</span><span class="sxs-lookup"><span data-stu-id="3d2bf-150">Deploy policy via Intune</span></span>

<span data-ttu-id="3d2bf-151">Pour Intune, la protection de l’imprimante de contrôle d’appareil prend uniquement en charge l’OMA-URI.</span><span class="sxs-lookup"><span data-stu-id="3d2bf-151">For Intune, currently Device Control Printer Protection supports OMA-URI only.</span></span>

### <a name="scenario-1-block-people-from-printing-via-any-non-corporate-printer-using-intune"></a><span data-ttu-id="3d2bf-152">Scénario 1 : empêcher les personnes d’imprimer via une imprimante non d’entreprise à l’aide d’Intune</span><span class="sxs-lookup"><span data-stu-id="3d2bf-152">Scenario 1: Block people from printing via any non-corporate printer using Intune</span></span>

- <span data-ttu-id="3d2bf-153">Appliquez la stratégie sur l’ordinateur :</span><span class="sxs-lookup"><span data-stu-id="3d2bf-153">Apply policy over machine:</span></span>

  `./Vendor/MSFT/Policy/Config/Printers/EnableDeviceControl`

- <span data-ttu-id="3d2bf-154">Appliquez la stratégie à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="3d2bf-154">Apply policy over user:</span></span>

  `./Vendor/MSFT/Policy/Config/Printers/EnableDeviceControlUser`

<span data-ttu-id="3d2bf-155">Chaîne de prise en charge du programme CSP avec `<enabled/>` :</span><span class="sxs-lookup"><span data-stu-id="3d2bf-155">The CSP support string with `<enabled/>`:</span></span>

:::image type="content" source="../../media/customeditrow.png" alt-text="ligne d’édition personnalisée":::

### <a name="scenario-2-allow-specific-approved-usb-printers-using-intune"></a><span data-ttu-id="3d2bf-157">Scénario 2 : autoriser des imprimantes USB approuvées spécifiques à l’aide d’Intune</span><span class="sxs-lookup"><span data-stu-id="3d2bf-157">Scenario 2: Allow specific approved USB printers using Intune</span></span>

- <span data-ttu-id="3d2bf-158">Appliquez la stratégie sur l’ordinateur :</span><span class="sxs-lookup"><span data-stu-id="3d2bf-158">Apply policy over machine:</span></span>

  `./Vendor/MSFT/Policy/Config/Printers/ApprovedUsbPrintDevices`

- <span data-ttu-id="3d2bf-159">Appliquez la stratégie à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="3d2bf-159">Apply policy over user:</span></span>

  `./Vendor/MSFT/Policy/Config/Printers/ApprovedUsbPrintDevicesUser`

<span data-ttu-id="3d2bf-160">La chaîne de prise en charge du programme CSP avec des imprimantes USB approuvées via la propriété « ApprovedUsbPrintDevices » (par `<enabled><data id="ApprovedUsbPrintDevices_List" value="03F0/0853,0351/0872">` exemple :</span><span class="sxs-lookup"><span data-stu-id="3d2bf-160">The CSP support string with approved USB printers via 'ApprovedUsbPrintDevices' property, example `<enabled><data id="ApprovedUsbPrintDevices_List" value="03F0/0853,0351/0872">`:</span></span>

:::image type="content" source="../../media/editrow.png" alt-text="modifier la ligne":::

## <a name="deploy-policy-via-group-policy"></a><span data-ttu-id="3d2bf-162">Déployer une stratégie via une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="3d2bf-162">Deploy policy via Group Policy</span></span>

<span data-ttu-id="3d2bf-163">Si l’appareil n’est pas joint à Intune, vous pouvez également déployer la stratégie via la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="3d2bf-163">If the device isn't Intune joined, you can also deploy the policy via Group Policy.</span></span>

### <a name="scenario-1-block-people-from-printing-via-any-non-corporate-printer-using-group-policy"></a><span data-ttu-id="3d2bf-164">Scénario 1 : empêcher les personnes d’imprimer via une imprimante non d’entreprise à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="3d2bf-164">Scenario 1: Block people from printing via any non-corporate printer using Group Policy</span></span>

- <span data-ttu-id="3d2bf-165">Appliquez la stratégie sur l’ordinateur :</span><span class="sxs-lookup"><span data-stu-id="3d2bf-165">Apply policy over machine:</span></span>

  <span data-ttu-id="3d2bf-166">Imprimante de \> modèles d’administration de configuration \> ordinateur : activer les restrictions d’impression des contrôles d’appareil</span><span class="sxs-lookup"><span data-stu-id="3d2bf-166">Computer Configuration \> Administrative Templates \> Printer: Enable Device control Printing Restrictions</span></span>

- <span data-ttu-id="3d2bf-167">Appliquez la stratégie à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="3d2bf-167">Apply policy over user:</span></span>

  <span data-ttu-id="3d2bf-168">Imprimantes du Panneau de configuration Des modèles d’administration de configuration utilisateur : \> \> activer les \> restrictions d’impression des contrôles d’appareil</span><span class="sxs-lookup"><span data-stu-id="3d2bf-168">User Configuration \> Administrative Templates \> Control Panel \> Printers: Enable Device control Printing Restrictions</span></span>

:::image type="content" source="../../media/enable-device-ctrl-printing-restrictions.png" alt-text="activer les restrictions d’impression d’appareil":::

### <a name="scenario-2-allow-specific-approved-usb-printers-using-group-policy"></a><span data-ttu-id="3d2bf-170">Scénario 2 : autoriser des imprimantes USB approuvées spécifiques à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="3d2bf-170">Scenario 2: Allow specific approved USB printers using Group Policy</span></span>

- <span data-ttu-id="3d2bf-171">Appliquez la stratégie sur l’ordinateur :</span><span class="sxs-lookup"><span data-stu-id="3d2bf-171">Apply policy over machine:</span></span>

  <span data-ttu-id="3d2bf-172">Imprimante de \> modèles d’administration de configuration \> ordinateur : liste des périphériques d’impression connectés usb approuvés</span><span class="sxs-lookup"><span data-stu-id="3d2bf-172">Computer Configuration \> Administrative Templates \> Printer:  List of Approved USB-connected print devices</span></span>

- <span data-ttu-id="3d2bf-173">Appliquez la stratégie à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="3d2bf-173">Apply policy over user:</span></span>

  <span data-ttu-id="3d2bf-174">Imprimantes du Panneau de configuration des modèles d’administration de configuration utilisateur : liste des \> périphériques d’impression connectés \> \> usb approuvés</span><span class="sxs-lookup"><span data-stu-id="3d2bf-174">User Configuration \> Administrative Templates \> Control Panel \> Printers: List of Approved USB-connected print devices</span></span>

:::image type="content" source="../../media/list-of-approved-connected-print-devices.png" alt-text="liste des périphériques d’impression connectés usb approuvés":::

## <a name="view-device-control-printer-protection-data-in-microsoft-defender-for-endpoint-portal"></a><span data-ttu-id="3d2bf-176">Afficher les données de protection des imprimantes des contrôles d’appareil dans le portail Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="3d2bf-176">View Device Control Printer Protection data in Microsoft Defender for Endpoint portal</span></span>

<span data-ttu-id="3d2bf-177">Le centre [Microsoft 365 de sécurité affiche](https://security.microsoft.com) l’impression bloquée par la stratégie Device Control Printer Protection ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="3d2bf-177">The [Microsoft 365 security center](https://security.microsoft.com) shows printing blocked by the Device Control Printer Protection policy above.</span></span>

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
