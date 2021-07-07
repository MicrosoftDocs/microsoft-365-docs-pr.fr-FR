---
title: Contrôle d’appareil amovible Microsoft Defender for Endpoint Stockage Access Control
description: Une présentation de Microsoft Defender pour point de terminaison
keywords: support de stockage amovible
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 0b0f7c5a4a75fdc80509dbc02a43d28f7c93fd7c
ms.sourcegitcommit: 53aebd492a4b998805c70c8e06a2cfa5d453905c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53327046"
---
# <a name="microsoft-defender-for-endpoint-device-control-removable-storage-access-control"></a><span data-ttu-id="5dfab-104">Contrôle d’appareil amovible Microsoft Defender for Endpoint Stockage Access Control</span><span class="sxs-lookup"><span data-stu-id="5dfab-104">Microsoft Defender for Endpoint Device Control Removable Storage Access Control</span></span>

[!INCLUDE [Prerelease](../includes/prerelease.md)]

<span data-ttu-id="5dfab-105">Microsoft Defender for Endpoint Device Control Removable Stockage Access Control vous permet d’accomplir la tâche suivante :</span><span class="sxs-lookup"><span data-stu-id="5dfab-105">Microsoft Defender for Endpoint Device Control Removable Storage Access Control enables you to do the following task:</span></span>

- <span data-ttu-id="5dfab-106">audit, autoriser ou empêcher l’accès en lecture, écriture ou exécution au stockage amovible avec ou sans exclusion</span><span class="sxs-lookup"><span data-stu-id="5dfab-106">auditing, allowing or preventing the read, write or execute access to removable storage with or without exclusion</span></span>

|<span data-ttu-id="5dfab-107">Privilège</span><span class="sxs-lookup"><span data-stu-id="5dfab-107">Privilege</span></span> |<span data-ttu-id="5dfab-108">Autorisation</span><span class="sxs-lookup"><span data-stu-id="5dfab-108">Permission</span></span>  |
|---------|---------|
|<span data-ttu-id="5dfab-109">Access</span><span class="sxs-lookup"><span data-stu-id="5dfab-109">Access</span></span>    |  <span data-ttu-id="5dfab-110">Lecture, Écriture, Exécution</span><span class="sxs-lookup"><span data-stu-id="5dfab-110">Read, Write, Execute</span></span>       |
|<span data-ttu-id="5dfab-111">Action Mode</span><span class="sxs-lookup"><span data-stu-id="5dfab-111">Action Mode</span></span>    |    <span data-ttu-id="5dfab-112">Auditer, autoriser, empêcher</span><span class="sxs-lookup"><span data-stu-id="5dfab-112">Audit, Allow, Prevent</span></span>     |
|<span data-ttu-id="5dfab-113">Prise en charge du programme CSP</span><span class="sxs-lookup"><span data-stu-id="5dfab-113">CSP Support</span></span>   |   <span data-ttu-id="5dfab-114">Oui</span><span class="sxs-lookup"><span data-stu-id="5dfab-114">Yes</span></span>      |
|<span data-ttu-id="5dfab-115">Prise en charge des GPO</span><span class="sxs-lookup"><span data-stu-id="5dfab-115">GPO Support</span></span>    |   <span data-ttu-id="5dfab-116">Oui</span><span class="sxs-lookup"><span data-stu-id="5dfab-116">Yes</span></span>      |
|<span data-ttu-id="5dfab-117">Prise en charge basée sur l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="5dfab-117">User-based Support</span></span>     |   <span data-ttu-id="5dfab-118">Oui</span><span class="sxs-lookup"><span data-stu-id="5dfab-118">Yes</span></span>      |
|<span data-ttu-id="5dfab-119">Prise en charge basée sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="5dfab-119">Machine-based Support</span></span>    |    <span data-ttu-id="5dfab-120">Oui</span><span class="sxs-lookup"><span data-stu-id="5dfab-120">Yes</span></span>     |

## <a name="prepare-your-endpoints"></a><span data-ttu-id="5dfab-121">Préparer vos points de terminaison</span><span class="sxs-lookup"><span data-stu-id="5dfab-121">Prepare your endpoints</span></span>

<span data-ttu-id="5dfab-122">Déployez le contrôle d Stockage’accès amovible sur Windows 10 qui ont un client anti-programme malveillant version **4.18.2103.3** ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5dfab-122">Deploy Removable Storage Access Control on Windows 10 devices that have antimalware client version **4.18.2103.3 or later**.</span></span>

- <span data-ttu-id="5dfab-123">**4.18.2104** ou version ultérieure : Ajouter SerialNumberId, VID_PID, prise en charge des GPO basés sur filepath, ComputerSid</span><span class="sxs-lookup"><span data-stu-id="5dfab-123">**4.18.2104 or later**: Add SerialNumberId, VID_PID, filepath-based GPO support, ComputerSid</span></span>

- <span data-ttu-id="5dfab-124">**4.18.2105** ou version ultérieure : ajouter la prise en charge des caractères génériques pour HardwareId/DeviceId/InstancePathId/FriendlyNameId/SerialNumberId, la combinaison d’un utilisateur spécifique sur un ordinateur spécifique, la prise en charge du SSD (Un SSD Extrême SanDisk)/USB Attached SCSI (UAS)</span><span class="sxs-lookup"><span data-stu-id="5dfab-124">**4.18.2105 or later**: Add Wildcard support for HardwareId/DeviceId/InstancePathId/FriendlyNameId/SerialNumberId, the combination of specific user on specific machine, removeable SSD (a SanDisk Extreme SSD)/USB Attached SCSI (UAS) support</span></span>

- <span data-ttu-id="5dfab-125">**4.18.2107** ou une ultérieure : ajouter la prise en charge Windows appareil portable (WPD) (pour les appareils mobiles, tels que les tablettes)</span><span class="sxs-lookup"><span data-stu-id="5dfab-125">**4.18.2107 or later**: Add Windows Portable Device (WPD) support (for mobile devices, such as tablets)</span></span>

:::image type="content" source="images/powershell.png" alt-text="Interface PowerShell":::

> [!NOTE]
> <span data-ttu-id="5dfab-127">Aucun des Sécurité Windows ne doit être actif, vous pouvez exécuter le contrôle d’accès Stockage amovible indépendamment de l’état Sécurité Windows’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5dfab-127">None of Windows Security components need to be active, you can run Removable Storage Access Control independent of Windows Security status.</span></span>

## <a name="policy-properties"></a><span data-ttu-id="5dfab-128">Propriétés de stratégie</span><span class="sxs-lookup"><span data-stu-id="5dfab-128">Policy properties</span></span>

<span data-ttu-id="5dfab-129">Vous pouvez utiliser les propriétés suivantes pour créer un groupe de stockage amovible :</span><span class="sxs-lookup"><span data-stu-id="5dfab-129">You can use the following properties to create a removable storage group:</span></span>

<span data-ttu-id="5dfab-130">**Nom de la propriété : ID de groupe**</span><span class="sxs-lookup"><span data-stu-id="5dfab-130">**Property name: Group Id**</span></span>

1. <span data-ttu-id="5dfab-131">Description : [GUID](https://en.wikipedia.org/wiki/Universally_unique_identifier), un ID unique, représente le groupe et sera utilisé dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="5dfab-131">Description: [GUID](https://en.wikipedia.org/wiki/Universally_unique_identifier), a unique ID, represents the group and will be used in the policy.</span></span>

<span data-ttu-id="5dfab-132">**Nom de la propriété : DescriptorIdList**</span><span class="sxs-lookup"><span data-stu-id="5dfab-132">**Property name: DescriptorIdList**</span></span>

2. <span data-ttu-id="5dfab-133">Description : liste des propriétés d’appareil que vous souhaitez utiliser pour couvrir dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="5dfab-133">Description: List the device properties you want to use to cover in the group.</span></span>
<span data-ttu-id="5dfab-134">Pour chaque propriété d’appareil, voir la section **Propriétés de** l’appareil ci-dessus pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="5dfab-134">For each device property, see **Device Properties** section above for more detail.</span></span>

3. <span data-ttu-id="5dfab-135">Options :</span><span class="sxs-lookup"><span data-stu-id="5dfab-135">Options:</span></span>
    - <span data-ttu-id="5dfab-136">PrimaryId</span><span class="sxs-lookup"><span data-stu-id="5dfab-136">PrimaryId</span></span>
        - <span data-ttu-id="5dfab-137">RemovableMediaDevices</span><span class="sxs-lookup"><span data-stu-id="5dfab-137">RemovableMediaDevices</span></span>
        - <span data-ttu-id="5dfab-138">CdRomDevices</span><span class="sxs-lookup"><span data-stu-id="5dfab-138">CdRomDevices</span></span>
        - <span data-ttu-id="5dfab-139">WpdDevices</span><span class="sxs-lookup"><span data-stu-id="5dfab-139">WpdDevices</span></span>
    - <span data-ttu-id="5dfab-140">DeviceId</span><span class="sxs-lookup"><span data-stu-id="5dfab-140">DeviceId</span></span>
    - <span data-ttu-id="5dfab-141">HardwareId</span><span class="sxs-lookup"><span data-stu-id="5dfab-141">HardwareId</span></span>
    - <span data-ttu-id="5dfab-142">InstancePathId : InstancePathId est une chaîne qui identifie de manière unique l’appareil dans le système, par exemple USBSTOR\DISK&VEN_GENERIC&PROD_FLASH_DISK&REV_8.07\8735B611&0.</span><span class="sxs-lookup"><span data-stu-id="5dfab-142">InstancePathId: InstancePathId is a string that uniquely identifies the device in the system, for example, USBSTOR\DISK&VEN_GENERIC&PROD_FLASH_DISK&REV_8.07\8735B611&0.</span></span> <span data-ttu-id="5dfab-143">Le numéro à la fin (par **exemple,&0**) représente l’emplacement disponible et peut changer d’appareil à appareil.</span><span class="sxs-lookup"><span data-stu-id="5dfab-143">The number at the end (for example **&0**) represents the available slot and may change from device to device.</span></span> <span data-ttu-id="5dfab-144">Pour de meilleurs résultats, utilisez un caractère générique à la fin.</span><span class="sxs-lookup"><span data-stu-id="5dfab-144">For best results, use a wildcard at the end.</span></span> <span data-ttu-id="5dfab-145">Par exemple, USBSTOR\DISK&VEN_GENERIC&PROD_FLASH_DISK&REV_8.07\8735B611\*</span><span class="sxs-lookup"><span data-stu-id="5dfab-145">For example, USBSTOR\DISK&VEN_GENERIC&PROD_FLASH_DISK&REV_8.07\8735B611\*</span></span>
    - <span data-ttu-id="5dfab-146">FriendlyNameId</span><span class="sxs-lookup"><span data-stu-id="5dfab-146">FriendlyNameId</span></span>
    - <span data-ttu-id="5dfab-147">SerialNumberId</span><span class="sxs-lookup"><span data-stu-id="5dfab-147">SerialNumberId</span></span>
    - <span data-ttu-id="5dfab-148">VID</span><span class="sxs-lookup"><span data-stu-id="5dfab-148">VID</span></span>
    - <span data-ttu-id="5dfab-149">PID</span><span class="sxs-lookup"><span data-stu-id="5dfab-149">PID</span></span>
    - <span data-ttu-id="5dfab-150">VID_PID</span><span class="sxs-lookup"><span data-stu-id="5dfab-150">VID_PID</span></span>
        - <span data-ttu-id="5dfab-151">0751_55E0 : correspondre à cette paire VID/PID exacte</span><span class="sxs-lookup"><span data-stu-id="5dfab-151">0751_55E0: match this exact VID/PID pair</span></span>
        - <span data-ttu-id="5dfab-152">_55E0 : faire correspondre n’importe quel média avec PID=55E0</span><span class="sxs-lookup"><span data-stu-id="5dfab-152">_55E0: match any media with PID=55E0</span></span>
        - <span data-ttu-id="5dfab-153">0751_: faire correspondre n’importe quel média avec VID=0751</span><span class="sxs-lookup"><span data-stu-id="5dfab-153">0751_: match any media with VID=0751</span></span>
        
<span data-ttu-id="5dfab-154">**Nom de la propriété : MatchType**</span><span class="sxs-lookup"><span data-stu-id="5dfab-154">**Property name: MatchType**</span></span> 

1. <span data-ttu-id="5dfab-155">Description : lorsqu’il existe plusieurs propriétés d’appareil utilisées dans DescriptorIDList, MatchType définit la relation.</span><span class="sxs-lookup"><span data-stu-id="5dfab-155">Description: When there are multiple device properties being used in the DescriptorIDList, MatchType defines the relationship.</span></span>

2. <span data-ttu-id="5dfab-156">Options :</span><span class="sxs-lookup"><span data-stu-id="5dfab-156">Options:</span></span>

    - <span data-ttu-id="5dfab-157">MatchAll : tous les attributs sous la relation DescriptorIdList seront **And** ; par exemple, si l’administrateur place DeviceID et InstancePathID, pour chaque clé USB connectée, le système vérifie si la clé USB répond aux deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="5dfab-157">MatchAll: Any attributes under the DescriptorIdList will be **And** relationship; for example, if administrator puts DeviceID and InstancePathID, for every connected USB, system will check to see whether the USB meets both values.</span></span>
    - <span data-ttu-id="5dfab-158">MatchAny : les attributs sous la relation DescriptorIdList seront **Or** ; par exemple, si l’administrateur place DeviceID et InstancePathID, pour chaque clé USB connectée, le système appliquera l’application tant que la clé USB aura une valeur **DeviceID** ou **InstanceID** identique.</span><span class="sxs-lookup"><span data-stu-id="5dfab-158">MatchAny: The attributes under the DescriptorIdList will be **Or** relationship; for example, if administrator puts DeviceID and InstancePathID, for every connected USB, system will do the enforcement as long as the USB has either an identical **DeviceID** or **InstanceID** value.</span></span>

<span data-ttu-id="5dfab-159">Voici les propriétés de stratégie de contrôle d’accès :</span><span class="sxs-lookup"><span data-stu-id="5dfab-159">Following are the access control policy properties:</span></span>

<span data-ttu-id="5dfab-160">**Nom de la propriété : PolicyRuleId**</span><span class="sxs-lookup"><span data-stu-id="5dfab-160">**Property name: PolicyRuleId**</span></span>

1. <span data-ttu-id="5dfab-161">Description : [GUID](https://en.wikipedia.org/wiki/Universally_unique_identifier), un ID unique, représente la stratégie et sera utilisé dans le rapport et la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="5dfab-161">Description: [GUID](https://en.wikipedia.org/wiki/Universally_unique_identifier), a unique ID, represents the policy and will be used in the reporting and troubleshooting.</span></span>

<span data-ttu-id="5dfab-162">**Nom de la propriété : IncludedIdList**</span><span class="sxs-lookup"><span data-stu-id="5dfab-162">**Property name: IncludedIdList**</span></span>

1. <span data-ttu-id="5dfab-163">Description : groupe(s) à appliquer à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="5dfab-163">Description: The group(s) that the policy will be applied to.</span></span> <span data-ttu-id="5dfab-164">Si plusieurs groupes sont ajoutés, la stratégie est appliquée à n’importe quel média de tous ces groupes.</span><span class="sxs-lookup"><span data-stu-id="5dfab-164">If multiple groups are added, the policy will be applied to any media in all those groups.</span></span>

2. <span data-ttu-id="5dfab-165">Options : l’ID de groupe/GUID doit être utilisé à cette instance.</span><span class="sxs-lookup"><span data-stu-id="5dfab-165">Options: The Group ID/GUID must be used at this instance.</span></span>

<span data-ttu-id="5dfab-166">L’exemple suivant illustre l’utilisation de GroupID :</span><span class="sxs-lookup"><span data-stu-id="5dfab-166">The following example shows the usage of GroupID:</span></span>

`<IncludedIdList> <GroupId>{EAA4CCE5-F6C9-4760-8BAD-FDCC76A2ACA1}</GroupId> </IncludedIdList>`

<span data-ttu-id="5dfab-167">**Nom de la propriété : ExcludedIDList**</span><span class="sxs-lookup"><span data-stu-id="5dfab-167">**Property name: ExcludedIDList**</span></span>

<span data-ttu-id="5dfab-168">Description : groupe(s) à qui la stratégie ne sera pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="5dfab-168">Description: The group(s) that the policy will not be applied to.</span></span>

<span data-ttu-id="5dfab-169">Options : l’ID de groupe/GUID doit être utilisé à cette instance.</span><span class="sxs-lookup"><span data-stu-id="5dfab-169">Options: The Group ID/GUID must be used at this instance.</span></span>

<span data-ttu-id="5dfab-170">**Nom de la propriété : ID d’entrée**</span><span class="sxs-lookup"><span data-stu-id="5dfab-170">**Property name: Entry Id**</span></span>

1. <span data-ttu-id="5dfab-171">Description : un policyRule peut avoir plusieurs entrées ; chaque entrée avec un GUID unique indique à Device Control une restriction.</span><span class="sxs-lookup"><span data-stu-id="5dfab-171">Description: One PolicyRule can have multiple entries; each entry with a unique GUID tells Device Control one restriction.</span></span>

<span data-ttu-id="5dfab-172">**Nom de la propriété : Type**</span><span class="sxs-lookup"><span data-stu-id="5dfab-172">**Property name: Type**</span></span>

1. <span data-ttu-id="5dfab-173">Description : définit l’action pour les groupes de stockage amovibles dans IncludedIDList.</span><span class="sxs-lookup"><span data-stu-id="5dfab-173">Description: Defines the action for the removable storage groups in IncludedIDList.</span></span>
    - <span data-ttu-id="5dfab-174">Application : autoriser ou refuser</span><span class="sxs-lookup"><span data-stu-id="5dfab-174">Enforcement: Allow or Deny</span></span>
    - <span data-ttu-id="5dfab-175">Audit : AuditAllowed ou AuditDenied</span><span class="sxs-lookup"><span data-stu-id="5dfab-175">Audit: AuditAllowed or AuditDenied</span></span> 

2. <span data-ttu-id="5dfab-176">Options :</span><span class="sxs-lookup"><span data-stu-id="5dfab-176">Options:</span></span>

    - <span data-ttu-id="5dfab-177">Autoriser</span><span class="sxs-lookup"><span data-stu-id="5dfab-177">Allow</span></span>
    - <span data-ttu-id="5dfab-178">Refuser</span><span class="sxs-lookup"><span data-stu-id="5dfab-178">Deny</span></span>
    - <span data-ttu-id="5dfab-179">AuditAllowed : définit la notification et l’événement lorsque l’accès est autorisé</span><span class="sxs-lookup"><span data-stu-id="5dfab-179">AuditAllowed: Defines notification and event when access is allowed</span></span>
    - <span data-ttu-id="5dfab-180">AuditDenied : définit la notification et l’événement lorsque l’accès est refusé ; doit fonctionner avec **l’entrée** de refus.</span><span class="sxs-lookup"><span data-stu-id="5dfab-180">AuditDenied: Defines notification and event when access is denied; has to work together with **Deny** entry.</span></span>

<span data-ttu-id="5dfab-181">Lorsqu’il existe des types de conflit pour le même média, le système applique le premier de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="5dfab-181">When there are conflict types for the same media, the system will apply the first one in the policy.</span></span> <span data-ttu-id="5dfab-182">Un exemple de type de conflit est **Allow** et **Deny**.</span><span class="sxs-lookup"><span data-stu-id="5dfab-182">An example of a conflict type is **Allow** and **Deny**.</span></span>

<span data-ttu-id="5dfab-183">**Nom de la propriété : Sid**</span><span class="sxs-lookup"><span data-stu-id="5dfab-183">**Property name: Sid**</span></span>

<span data-ttu-id="5dfab-184">Description : sid de l’ordinateur local ou sid de l’objet AD, définit s’il faut appliquer cette stratégie sur un utilisateur ou un groupe d’utilisateurs spécifique ; une entrée peut avoir un maximum d’un Sid et une entrée sans sid signifie appliquer la stratégie sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5dfab-184">Description: Local computer Sid or the Sid of the AD object, defines whether to apply this policy over a specific user or user group; one entry can have a maximum of one Sid and an entry without any Sid means applying the policy over the machine.</span></span>

<span data-ttu-id="5dfab-185">**Nom de la propriété : ComputerSid**</span><span class="sxs-lookup"><span data-stu-id="5dfab-185">**Property name: ComputerSid**</span></span>

<span data-ttu-id="5dfab-186">Description : sid de l’ordinateur local ou sid de l’objet AD, définit s’il faut appliquer cette stratégie sur un ordinateur ou un groupe d’ordinateurs spécifique ; une entrée peut avoir un maximum d’un ComputerSid et une entrée sans ComputerSid signifie appliquer la stratégie sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5dfab-186">Description: Local computer Sid or the Sid of the AD object, defines whether to apply this policy over a specific machine or machine group; one entry can have a maximum of one ComputerSid and an entry without any ComputerSid means applying the policy over the machine.</span></span> <span data-ttu-id="5dfab-187">Si vous souhaitez appliquer une entrée à un utilisateur spécifique et à un ordinateur spécifique, ajoutez Sid et ComputerSid dans la même entrée.</span><span class="sxs-lookup"><span data-stu-id="5dfab-187">If you want to apply an Entry to a specific user and specific machine, add both Sid and ComputerSid into the same Entry.</span></span>

<span data-ttu-id="5dfab-188">**Nom de la propriété : Options**</span><span class="sxs-lookup"><span data-stu-id="5dfab-188">**Property name: Options**</span></span>

<span data-ttu-id="5dfab-189">Description : définit s’il faut afficher la notification ou non.</span><span class="sxs-lookup"><span data-stu-id="5dfab-189">Description: Defines whether to display notification or not.</span></span>

   :::image type="content" source="images/device-status.png" alt-text="Écran sur lequel l’état de l’appareil est visible":::

<span data-ttu-id="5dfab-191">Options : 0-4.</span><span class="sxs-lookup"><span data-stu-id="5dfab-191">Options: 0-4.</span></span> <span data-ttu-id="5dfab-192">Lorsque le type Autoriser ou Refuser est sélectionné :</span><span class="sxs-lookup"><span data-stu-id="5dfab-192">When Type Allow or Deny is selected:</span></span>

   - <span data-ttu-id="5dfab-193">0 : rien</span><span class="sxs-lookup"><span data-stu-id="5dfab-193">0: nothing</span></span>
   - <span data-ttu-id="5dfab-194">4 : désactivez **AuditAllowed** et **AuditDenied** pour cette entrée.</span><span class="sxs-lookup"><span data-stu-id="5dfab-194">4: disable **AuditAllowed** and **AuditDenied** for this Entry.</span></span> <span data-ttu-id="5dfab-195">Même si **le blocage** se produit et que le paramètre **AuditDenied** est configuré, le système n’affiche pas de notification.</span><span class="sxs-lookup"><span data-stu-id="5dfab-195">Even if **Block** happens and the **AuditDenied** is setting configured, the system will not show notification.</span></span>

   <span data-ttu-id="5dfab-196">Lorsque type **AuditAllowed ou** **AuditDenied** est sélectionné :</span><span class="sxs-lookup"><span data-stu-id="5dfab-196">When Type **AuditAllowed** or **AuditDenied** is selected:</span></span>

   - <span data-ttu-id="5dfab-197">0 : rien</span><span class="sxs-lookup"><span data-stu-id="5dfab-197">0: nothing</span></span>
   - <span data-ttu-id="5dfab-198">1 : afficher la notification</span><span class="sxs-lookup"><span data-stu-id="5dfab-198">1: show notification</span></span>
   - <span data-ttu-id="5dfab-199">2 : événement d’envoi</span><span class="sxs-lookup"><span data-stu-id="5dfab-199">2: send event</span></span>
   - <span data-ttu-id="5dfab-200">3 : afficher la notification et envoyer un événement</span><span class="sxs-lookup"><span data-stu-id="5dfab-200">3: show notification and send event</span></span>

<span data-ttu-id="5dfab-201">**Nom de la propriété : AccessMask**</span><span class="sxs-lookup"><span data-stu-id="5dfab-201">**Property name: AccessMask**</span></span>

<span data-ttu-id="5dfab-202">Description : définit l’accès.</span><span class="sxs-lookup"><span data-stu-id="5dfab-202">Description: Defines the access.</span></span>

<span data-ttu-id="5dfab-203">Options 1 à 7 :</span><span class="sxs-lookup"><span data-stu-id="5dfab-203">Options 1-7:</span></span>
  - <span data-ttu-id="5dfab-204">1 : lecture</span><span class="sxs-lookup"><span data-stu-id="5dfab-204">1: Read</span></span>
  - <span data-ttu-id="5dfab-205">2 : Écriture</span><span class="sxs-lookup"><span data-stu-id="5dfab-205">2: Write</span></span>
  - <span data-ttu-id="5dfab-206">3 : Lecture et écriture</span><span class="sxs-lookup"><span data-stu-id="5dfab-206">3: Read and Write</span></span>
  - <span data-ttu-id="5dfab-207">4 : Exécuter</span><span class="sxs-lookup"><span data-stu-id="5dfab-207">4: Execute</span></span>
  - <span data-ttu-id="5dfab-208">5 : Lecture et exécution</span><span class="sxs-lookup"><span data-stu-id="5dfab-208">5: Read and Execute</span></span>
  - <span data-ttu-id="5dfab-209">6 : Écriture et exécution</span><span class="sxs-lookup"><span data-stu-id="5dfab-209">6: Write and Execute</span></span>
  - <span data-ttu-id="5dfab-210">7 : Lecture et écriture et exécution</span><span class="sxs-lookup"><span data-stu-id="5dfab-210">7: Read and Write and Execute</span></span>

## <a name="common-removable-storage-access-control-scenarios"></a><span data-ttu-id="5dfab-211">Scénarios courants Stockage contrôle d’accès des périphériques amovibles</span><span class="sxs-lookup"><span data-stu-id="5dfab-211">Common Removable Storage Access Control scenarios</span></span>

<span data-ttu-id="5dfab-212">Pour vous aider à vous familiariser avec Microsoft Defender pour endpoint Removable Stockage Access Control, nous avons mis en place des scénarios courants que vous pouvez suivre.</span><span class="sxs-lookup"><span data-stu-id="5dfab-212">To help familiarize you with Microsoft Defender for Endpoint Removable Storage Access Control, we have put together some common scenarios for you to follow.</span></span>

### <a name="scenario-1-prevent-write-and-execute-access-to-all-but-allow-specific-approved-usbs"></a><span data-ttu-id="5dfab-213">Scénario 1 : empêcher l’accès en écriture et en exécution à tous les utilisateurs approuvés spécifiques, mais autoriser</span><span class="sxs-lookup"><span data-stu-id="5dfab-213">Scenario 1: Prevent Write and Execute access to all but allow specific approved USBs</span></span>

1. <span data-ttu-id="5dfab-214">Créer des groupes</span><span class="sxs-lookup"><span data-stu-id="5dfab-214">Create groups</span></span>

    1. <span data-ttu-id="5dfab-215">Groupe 1 : Tout stockage amovible et CD/DVD.</span><span class="sxs-lookup"><span data-stu-id="5dfab-215">Group 1: Any removable storage and CD/DVD.</span></span> <span data-ttu-id="5dfab-216">Un exemple de stockage amovible et de CD/DVD est le groupe **9b28fae8-72f7-4267-a1a5-685f747a7146** dans l’exemple de fichier de Group.xmlany [Removable Stockage et CD-DVD.](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples)</span><span class="sxs-lookup"><span data-stu-id="5dfab-216">An example of a removable storage and CD/DVD is: Group **9b28fae8-72f7-4267-a1a5-685f747a7146** in the sample [Any Removable Storage and CD-DVD Group.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span>
    
    2. <span data-ttu-id="5dfab-217">Groupe 2 : approbation de base de données américaines en fonction des propriétés de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5dfab-217">Group 2: Approved USBs based on device properties.</span></span> <span data-ttu-id="5dfab-218">Voici un exemple de ce cas d’utilisation : ID d’instance – Groupe **65fa649a-a111-4912-9294-fb6337a25038** dans l’exemple de fichier Group.xmlde base de données approuvé. [](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples)</span><span class="sxs-lookup"><span data-stu-id="5dfab-218">An example for this use case is: Instance ID – Group **65fa649a-a111-4912-9294-fb6337a25038** in the sample [Approved USBs Group.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5dfab-219">Vous devez remplacer `&` par `&amp;` dans la valeur.</span><span class="sxs-lookup"><span data-stu-id="5dfab-219">You have to replace `&` with `&amp;` in the value.</span></span>

2. <span data-ttu-id="5dfab-220">Création d’une stratégie</span><span class="sxs-lookup"><span data-stu-id="5dfab-220">Create policy</span></span>

    1. <span data-ttu-id="5dfab-221">Stratégie 1 : bloquer l’écriture et exécuter l’accès, mais autoriser les usbs approuvés.</span><span class="sxs-lookup"><span data-stu-id="5dfab-221">Policy 1: Block Write and Execute Access but allow approved USBs.</span></span> <span data-ttu-id="5dfab-222">Voici un exemple de ce cas d’utilisation : PolicyRule **c544a991-5786-4402-949e-a032cb790d0e dans** l’exemple Scénario [1](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) Bloquer l’écriture et exécuter l’accès, mais autoriser le fichier USBs.xmlapprouvé.</span><span class="sxs-lookup"><span data-stu-id="5dfab-222">An example for this use case is: PolicyRule **c544a991-5786-4402-949e-a032cb790d0e** in the sample [Scenario 1 Block Write and Execute Access but allow approved USBs.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span>
    
    2. <span data-ttu-id="5dfab-223">Stratégie 2 : auditer l’accès en écriture et en cours d’exécution aux usbs autorisés.</span><span class="sxs-lookup"><span data-stu-id="5dfab-223">Policy 2: Audit Write and Execute access to allowed USBs.</span></span> <span data-ttu-id="5dfab-224">Voici un exemple de ce cas d’utilisation : PolicyRule **36ae1037-a639-4cff-946b-b36c53089a4c** dans l’exemple scénario [1 Auditer](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) l’accès en écriture et en exécution au fichier USBs.xmlapprouvé.</span><span class="sxs-lookup"><span data-stu-id="5dfab-224">An example for this use case is: PolicyRule **36ae1037-a639-4cff-946b-b36c53089a4c** in the sample [Scenario 1 Audit Write and Execute access to approved USBs.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span>

### <a name="scenario-2-audit-write-and-execute-access-to-all-but-block-specific-unapproved-usbs"></a><span data-ttu-id="5dfab-225">Scénario 2 : Auditer l’accès en écriture et en exécution à toutes les stratégies de groupe de sécurité universels non désapprouvées, sauf bloquer</span><span class="sxs-lookup"><span data-stu-id="5dfab-225">Scenario 2: Audit Write and Execute access to all but block specific unapproved USBs</span></span>

1. <span data-ttu-id="5dfab-226">Créer des groupes</span><span class="sxs-lookup"><span data-stu-id="5dfab-226">Create groups</span></span>

    1. <span data-ttu-id="5dfab-227">Groupe 1 : Tout stockage amovible et CD/DVD.</span><span class="sxs-lookup"><span data-stu-id="5dfab-227">Group 1: Any removable storage and CD/DVD.</span></span> <span data-ttu-id="5dfab-228">Voici un exemple de ce cas d’utilisation : Groupe **9b28fae8-72f7-4267-a1a5-685f747a7146** dans l’exemple de fichier de Stockage amovible et [de CD-DVD Group.xml.](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples)</span><span class="sxs-lookup"><span data-stu-id="5dfab-228">An example for this use case is: Group **9b28fae8-72f7-4267-a1a5-685f747a7146** in the sample [Any Removable Storage and CD-DVD Group.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span>
    
    2. <span data-ttu-id="5dfab-229">Groupe 2 : listes de contrôle d’appareil non désapprouvées en fonction des propriétés de l’appareil, par exemple, ID fournisseur/ID de produit, nom convivial – Groupe **65fa649a-a111-4912-9294-fb6337a25038** dans l’exemple de fichier Group.xmlde base de données des [états-Group.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) non accepté.</span><span class="sxs-lookup"><span data-stu-id="5dfab-229">Group 2: Unapproved USBs based on device properties, for example, Vendor ID / Product ID, Friendly Name – Group **65fa649a-a111-4912-9294-fb6337a25038** in the sample [Unapproved USBs Group.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="5dfab-230">Vous devez remplacer `&` par `&amp;` dans la valeur.</span><span class="sxs-lookup"><span data-stu-id="5dfab-230">You have to replace `&` with `&amp;` in the value.</span></span>

2. <span data-ttu-id="5dfab-231">Création d’une stratégie</span><span class="sxs-lookup"><span data-stu-id="5dfab-231">Create policy</span></span>

    1. <span data-ttu-id="5dfab-232">Stratégie 1 : bloquer l’accès en écriture et en cours d’exécution à tous les usbs non désapprouvés spécifiques, sauf à les bloquer.</span><span class="sxs-lookup"><span data-stu-id="5dfab-232">Policy 1: Block Write and Execute access to all but block specific unapproved USBs.</span></span> <span data-ttu-id="5dfab-233">Voici un exemple de ce cas d’utilisation : PolicyRule **23b8e437-66ac-4b32-b3d7-24044637fc98** dans l’exemple Scénario [2 Auditer](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) l’accès à l’écriture et à l’exécution de tous les fichiers USBs.xmlnon désapprouvés, sauf bloquer.</span><span class="sxs-lookup"><span data-stu-id="5dfab-233">An example of this use case is: PolicyRule **23b8e437-66ac-4b32-b3d7-24044637fc98** in the sample [Scenario 2 Audit Write and Execute access to all but block specific unapproved USBs.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span>
    
    2. <span data-ttu-id="5dfab-234">Stratégie 2 : auditer l’écriture et exécuter l’accès à d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="5dfab-234">Policy 2: Audit Write and Execute access to others.</span></span> <span data-ttu-id="5dfab-235">Voici un exemple de ce cas d’utilisation : PolicyRule **b58ab853-9a6f-405c-a194-740e69422b48** dans l’exemple Scénario [2 Auditer](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) l’accès en écriture et en exécution au fichier others.xml.</span><span class="sxs-lookup"><span data-stu-id="5dfab-235">An example of this use case is: PolicyRule **b58ab853-9a6f-405c-a194-740e69422b48** in the sample [Scenario 2 Audit Write and Execute access to others.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span>

## <a name="deploying-and-managing-policy-via-group-policy"></a><span data-ttu-id="5dfab-236">Déploiement et gestion d’une stratégie via une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5dfab-236">Deploying and managing policy via Group Policy</span></span>

<span data-ttu-id="5dfab-237">La fonctionnalité de contrôle d Stockage’accès amovible vous permet d’appliquer une stratégie via la stratégie de groupe à l’utilisateur ou à l’appareil, ou aux deux.</span><span class="sxs-lookup"><span data-stu-id="5dfab-237">The Removable Storage Access Control feature enables you to apply policy via Group Policy to either user or device, or both.</span></span>

### <a name="licensing"></a><span data-ttu-id="5dfab-238">Licences</span><span class="sxs-lookup"><span data-stu-id="5dfab-238">Licensing</span></span>

<span data-ttu-id="5dfab-239">Avant de commencer avec le contrôle d’accès Stockage amovible, vous devez confirmer [votre abonnement Microsoft 365.](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=2)</span><span class="sxs-lookup"><span data-stu-id="5dfab-239">Before you get started with Removable Storage Access Control, you must confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=2).</span></span> <span data-ttu-id="5dfab-240">Pour accéder au contrôle d’accès Stockage et l’utiliser, vous devez Microsoft 365 E3 ou Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="5dfab-240">To access and use Removable Storage Access Control, you must have Microsoft 365 E3 or Microsoft 365 E5.</span></span>

### <a name="deploying-policy-via-group-policy"></a><span data-ttu-id="5dfab-241">Déploiement d’une stratégie via une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5dfab-241">Deploying policy via Group Policy</span></span>

1. <span data-ttu-id="5dfab-242">Combinez tous les groupes `<Groups>` `</Groups>` au sein d’un fichier xml.</span><span class="sxs-lookup"><span data-stu-id="5dfab-242">Combine all groups within `<Groups>` `</Groups>` into one xml file.</span></span> 

    <span data-ttu-id="5dfab-243">L’image suivante illustre l’exemple du scénario 1 : empêcher l’accès en écriture et en exécution à tous les [usbs approuvés spécifiques,](#scenario-1-prevent-write-and-execute-access-to-all-but-allow-specific-approved-usbs)sauf autoriser.</span><span class="sxs-lookup"><span data-stu-id="5dfab-243">The following image illustrates the example of [Scenario 1: Prevent Write and Execute access to all but allow specific approved USBs](#scenario-1-prevent-write-and-execute-access-to-all-but-allow-specific-approved-usbs).</span></span>
    
    :::image type="content" source="images/prevent-write-access-allow-usb.png" alt-text="Écran affichant les paramètres de configuration qui autorisent des usbs approuvés spécifiques sur les appareils":::
    
2. <span data-ttu-id="5dfab-245">Combinez toutes les règles `<PolicyRules>` `</PolicyRules>` dans un fichier xml.</span><span class="sxs-lookup"><span data-stu-id="5dfab-245">Combine all rules within `<PolicyRules>` `</PolicyRules>` into one xml file.</span></span> 

    <span data-ttu-id="5dfab-246">Si vous souhaitez limiter un utilisateur spécifique, utilisez la propriété SID dans l’entrée.</span><span class="sxs-lookup"><span data-stu-id="5dfab-246">If you want to restrict a specific user, then use SID property into the Entry.</span></span> <span data-ttu-id="5dfab-247">S’il n’existe aucun SID dans l’entrée de stratégie, l’entrée est appliquée à l’instance de connexion de tout le monde pour l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5dfab-247">If there is no SID in the policy Entry, the Entry will be applied to everyone login instance for the machine.</span></span>
    
    <span data-ttu-id="5dfab-248">L’image suivante illustre l’utilisation de la propriété SID et un exemple de scénario 1 : empêcher l’accès en écriture et en exécution à tous les [usbs approuvés spécifiques,](#scenario-1-prevent-write-and-execute-access-to-all-but-allow-specific-approved-usbs)sauf autoriser.</span><span class="sxs-lookup"><span data-stu-id="5dfab-248">The following image illustrates the usage of SID property, and an example of [Scenario 1: Prevent Write and Execute access to all but allow specific approved USBs](#scenario-1-prevent-write-and-execute-access-to-all-but-allow-specific-approved-usbs).</span></span>
    
    :::image type="content" source="images/usage-sid-property.png" alt-text="Écran affichant un code qui indique l’utilisation de l’attribut de propriété SID":::

3. <span data-ttu-id="5dfab-250">Enregistrez les fichiers XML de règle et de groupe sur le dossier de partage réseau et placez le chemin d’accès du dossier de partage réseau dans le paramètre de stratégie de groupe : Configuration ordinateur -> Modèles d’administration **-> Windows Composants -> Antivirus Microsoft Defender -> Contrôle** d’appareil : « Définir des groupes de stratégies de contrôle d’appareil » et « Définir des règles de stratégie de contrôle d’appareil ».</span><span class="sxs-lookup"><span data-stu-id="5dfab-250">Save both rule and group XML files on network share folder and put network share folder path into the Group Policy setting: **Computer Configuration -> Administrative Templates -> Windows Components -> Microsoft Defender Antivirus -> Device Control: ‘Define device control policy groups’ and ‘Define device control policy rules’**.</span></span>

    - <span data-ttu-id="5dfab-251">L’ordinateur cible doit pouvoir accéder au partage réseau pour avoir la stratégie.</span><span class="sxs-lookup"><span data-stu-id="5dfab-251">The target machine must be able to access the network share to have the policy.</span></span> <span data-ttu-id="5dfab-252">Toutefois, une fois la stratégie lue, la connexion de partage réseau n’est plus nécessaire, même après le redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5dfab-252">However, once the policy is read, the network share connection is no longer required, even after machine reboot.</span></span>

    :::image type="content" source="images/device-control.png" alt-text="Écran Contrôle d’appareil":::

## <a name="deploying-and-managing-policy-via-intune-oma-uri"></a><span data-ttu-id="5dfab-254">Déploiement et gestion d’une stratégie via Intune OMA-URI</span><span class="sxs-lookup"><span data-stu-id="5dfab-254">Deploying and managing policy via Intune OMA-URI</span></span>

<span data-ttu-id="5dfab-255">La fonctionnalité Stockage contrôle d’accès amovible vous permet d’appliquer une stratégie via OMA-URI à l’utilisateur ou à l’appareil, ou aux deux.</span><span class="sxs-lookup"><span data-stu-id="5dfab-255">The Removable Storage Access Control feature enables you to apply policy via OMA-URI to either user or device, or both.</span></span>

### <a name="licensing"></a><span data-ttu-id="5dfab-256">Licences</span><span class="sxs-lookup"><span data-stu-id="5dfab-256">Licensing</span></span>

<span data-ttu-id="5dfab-257">Avant de commencer avec le contrôle d’accès Stockage amovible, vous devez confirmer [votre abonnement Microsoft 365.](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=2)</span><span class="sxs-lookup"><span data-stu-id="5dfab-257">Before you get started with Removable Storage Access Control, you  must confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=2).</span></span> <span data-ttu-id="5dfab-258">Pour accéder au contrôle d’accès Stockage et l’utiliser, vous devez Microsoft 365 E3 ou Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="5dfab-258">To access and use Removable Storage Access Control, you must have Microsoft 365 E3 or Microsoft 365 E5.</span></span>

### <a name="permission"></a><span data-ttu-id="5dfab-259">Autorisation</span><span class="sxs-lookup"><span data-stu-id="5dfab-259">Permission</span></span>

<span data-ttu-id="5dfab-260">Pour le déploiement de stratégie dans Intune, le compte doit être autorisé à créer, modifier, mettre à jour ou supprimer des profils de configuration d’appareil.</span><span class="sxs-lookup"><span data-stu-id="5dfab-260">For policy deployment in Intune, the account must have permissions to create, edit, update, or delete device configuration profiles.</span></span> <span data-ttu-id="5dfab-261">Vous pouvez créer des rôles personnalisés ou utiliser n’importe quel rôle intégré avec ces autorisations.</span><span class="sxs-lookup"><span data-stu-id="5dfab-261">You can create custom roles or use any of the built-in roles with these permissions.</span></span>

- <span data-ttu-id="5dfab-262">Rôle gestionnaire de stratégies et de profils</span><span class="sxs-lookup"><span data-stu-id="5dfab-262">Policy and profile Manager role</span></span>
- <span data-ttu-id="5dfab-263">Rôle personnalisé avec les autorisations Créer/Modifier/Mettre à jour/Lecture/Supprimer/Afficher les rapports pour les profils de configuration d’appareil</span><span class="sxs-lookup"><span data-stu-id="5dfab-263">Custom role with Create/Edit/Update/Read/Delete/View Reports permissions turned on for Device Configuration profiles</span></span>
- <span data-ttu-id="5dfab-264">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="5dfab-264">Global administrator</span></span>

### <a name="deploying-policy-via-oma-uri"></a><span data-ttu-id="5dfab-265">Déploiement d’une stratégie via OMA-URI</span><span class="sxs-lookup"><span data-stu-id="5dfab-265">Deploying policy via OMA-URI</span></span>

<span data-ttu-id="5dfab-266">**Microsoft Endpoint Manager admin center ( https://endpoint.microsoft.com/) -> Devices -> Configuration profiles -> Create profile -> Platform: Windows 10 and later & Profile: Custom**</span><span class="sxs-lookup"><span data-stu-id="5dfab-266">**Microsoft Endpoint Manager admin center (https://endpoint.microsoft.com/) -> Devices -> Configuration profiles -> Create profile -> Platform: Windows 10 and later & Profile: Custom**</span></span>

1. <span data-ttu-id="5dfab-267">Pour chaque groupe, créez une règle OMA-URI :</span><span class="sxs-lookup"><span data-stu-id="5dfab-267">For each Group, create an OMA-URI rule:</span></span>
    - <span data-ttu-id="5dfab-268">OMA-URI : </span><span class="sxs-lookup"><span data-stu-id="5dfab-268">OMA-URI:</span></span>

      <span data-ttu-id="5dfab-269">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyGroups/%7b **GroupGUID**%7d/GroupData</span><span class="sxs-lookup"><span data-stu-id="5dfab-269">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyGroups/%7b **GroupGUID**%7d/GroupData</span></span>

      <span data-ttu-id="5dfab-270">Par exemple, pour tout stockage amovible et groupe **CD/DVD** dans l’exemple, le lien doit être :</span><span class="sxs-lookup"><span data-stu-id="5dfab-270">For example, for **any removable storage and CD/DVD** group in the sample, the link must be:</span></span>

      <span data-ttu-id="5dfab-271">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyGroups/%7b9b28fae8-72f7-4267-a1a5-685f747a7146%7d/GroupData</span><span class="sxs-lookup"><span data-stu-id="5dfab-271">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyGroups/%7b9b28fae8-72f7-4267-a1a5-685f747a7146%7d/GroupData</span></span>

    - <span data-ttu-id="5dfab-272">Type de données : chaîne (fichier XML)</span><span class="sxs-lookup"><span data-stu-id="5dfab-272">Data Type: String (XML file)</span></span>
    
      :::image type="content" source="images/xml-data-type-string.png" alt-text="Fichier xml pour le type de données STRING":::

2. <span data-ttu-id="5dfab-274">Pour chaque stratégie, créez également un OMA-URI :</span><span class="sxs-lookup"><span data-stu-id="5dfab-274">For each policy, also create an OMA-URI:</span></span>

    - <span data-ttu-id="5dfab-275">OMA-URI : </span><span class="sxs-lookup"><span data-stu-id="5dfab-275">OMA-URI:</span></span>

      <span data-ttu-id="5dfab-276">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyRules/%7bFA6BE102-0784-4A2A-B010-A0BEBEBF68E1%7d/RuleData</span><span class="sxs-lookup"><span data-stu-id="5dfab-276">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyRules/%7bFA6BE102-0784-4A2A-B010-A0BEBEBF68E1%7d/RuleData</span></span>

      <span data-ttu-id="5dfab-277">Par exemple, pour la règle Bloquer l’écriture et exécuter l’accès, mais autoriser les règles de base de données utilisateur **approuvées** dans l’exemple, le lien doit être :</span><span class="sxs-lookup"><span data-stu-id="5dfab-277">For example, for the **Block Write and Execute Access but allow approved USBs** rule in the sample, the link must be:</span></span> 

      <span data-ttu-id="5dfab-278">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyRules/%7bc544a991-5786-4402-949e-a032cb790d0e%7d/RuleData.</span><span class="sxs-lookup"><span data-stu-id="5dfab-278">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyRules/%7bc544a991-5786-4402-949e-a032cb790d0e%7d/RuleData.</span></span>

    - <span data-ttu-id="5dfab-279">Type de données : chaîne (fichier XML)</span><span class="sxs-lookup"><span data-stu-id="5dfab-279">Data Type: String (XML file)</span></span>

      :::image type="content" source="images/xml-data-type-string-2.png" lightbox="images/xml-data-type-string-2.png" alt-text="Affichage du fichier XML pour le type de données STRING":::

## <a name="deploying-and-managing-policy-by-using-intune-user-interface"></a><span data-ttu-id="5dfab-281">Déploiement et gestion d’une stratégie à l’aide de l’interface utilisateur Intune</span><span class="sxs-lookup"><span data-stu-id="5dfab-281">Deploying and managing policy by using Intune user interface</span></span>

<span data-ttu-id="5dfab-282">Cette fonctionnalité (dans le Centre d’administration Microsoft Endpoint Manager ( profils de configuration > Périphériques > > Créer un profil https://endpoint.microsoft.com/) > Platform: Windows 10 and later & Profile: Device Control) n’est pas encore disponible.</span><span class="sxs-lookup"><span data-stu-id="5dfab-282">This capability (in Microsoft Endpoint Manager admin center (https://endpoint.microsoft.com/) > Devices > Configuration profiles > Create profile > Platform: Windows 10 and later & Profile: Device Control) is not yet available.</span></span> 

## <a name="view-device-control-removable-storage-access-control-data-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="5dfab-283">Afficher les données de contrôle d’Stockage d’accès amovible dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5dfab-283">View Device Control Removable Storage Access Control data in Microsoft Defender for Endpoint</span></span>

<span data-ttu-id="5dfab-284">Le portail Microsoft 365 de sécurité affiche le stockage amovible bloqué par le contrôle d’Stockage d’accès.</span><span class="sxs-lookup"><span data-stu-id="5dfab-284">The Microsoft 365 security portal shows removable storage blocked by the Device Control Removable Storage Access Control.</span></span> <span data-ttu-id="5dfab-285">Pour accéder à la sécurité Microsoft 365, vous devez avoir l’abonnement suivant :</span><span class="sxs-lookup"><span data-stu-id="5dfab-285">To access the Microsoft 365 security, you must have the following subscription:</span></span>

- <span data-ttu-id="5dfab-286">Microsoft 365 de rapports E5</span><span class="sxs-lookup"><span data-stu-id="5dfab-286">Microsoft 365 for E5 reporting</span></span>

```kusto
//events triggered by RemovableStoragePolicyTriggered
DeviceEvents
| where ActionType == &quot;RemovableStoragePolicyTriggered&quot; 
| extend parsed=parse_json(AdditionalFields) 
| extend RemovableStorageAccess = tostring(parsed.RemovableStorageAccess)  
| extend RemovableStoragePolicyVerdict = tostring(parsed.RemovableStoragePolicyVerdict)  
| extend MediaBusType = tostring(parsed.BusType)  
| extend MediaClassGuid = tostring(parsed.ClassGuid)
| extend MediaClassName = tostring(parsed.ClassName)
| extend MediaDeviceId = tostring(parsed.DeviceId) 
| extend MediaInstanceId = tostring(parsed.DeviceInstanceId) 
| extend MediaName = tostring(parsed.MediaName) 
| extend RemovableStoragePolicy = tostring(parsed.RemovableStoragePolicy)  
| extend MediaProductId = tostring(parsed.ProductId)  
| extend MediaVendorId = tostring(parsed.VendorId)  
| extend MediaSerialNumber = tostring(parsed.SerialNumber)  
| extend MediaVolume = tostring(parsed.Volume)  
| project Timestamp, DeviceId, DeviceName, ActionType, RemovableStorageAccess, RemovableStoragePolicyVerdict, MediaBusType, MediaClassGuid, MediaClassName, MediaDeviceId, MediaInstanceId, MediaName, RemovableStoragePolicy, MediaProductId, MediaVendorId, MediaSerialNumber, MediaVolume 
| order by Timestamp desc
```

:::image type="content" source="images/block-removable-storage.png" alt-text="Écran illustrant le blocage du stockage amovible":::

## <a name="frequently-asked-questions"></a><span data-ttu-id="5dfab-288">Foire aux questions</span><span class="sxs-lookup"><span data-stu-id="5dfab-288">Frequently asked questions</span></span>

<span data-ttu-id="5dfab-289">**Quelle est la limite du support de stockage amovible pour le nombre maximal de objets de première utilisation ?**</span><span class="sxs-lookup"><span data-stu-id="5dfab-289">**What is the removable storage media limitation for the maximum number of USBs?**</span></span>

<span data-ttu-id="5dfab-290">Nous avons validé un groupe USB avec 100 000 supports , jusqu’à 7 Mo.</span><span class="sxs-lookup"><span data-stu-id="5dfab-290">We have validated one USB group with 100,000 media - up to 7 MB in size.</span></span> <span data-ttu-id="5dfab-291">La stratégie fonctionne dans Intune et LPO sans problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="5dfab-291">The policy works in both Intune and GPO without performance issues.</span></span>

<span data-ttu-id="5dfab-292">**Pourquoi la stratégie ne fonctionne-t-elle pas ?**</span><span class="sxs-lookup"><span data-stu-id="5dfab-292">**Why does the policy not work?**</span></span>

<span data-ttu-id="5dfab-293">La raison la plus courante est qu’il n’existe pas de [version de client anti-programme malveillant requise.](/microsoft-365/security/defender-endpoint/device-control-removable-storage-access-control#prepare-your-endpoints)</span><span class="sxs-lookup"><span data-stu-id="5dfab-293">The most common reason is there is no required [antimalware client version](/microsoft-365/security/defender-endpoint/device-control-removable-storage-access-control#prepare-your-endpoints).</span></span>

<span data-ttu-id="5dfab-294">Une autre raison peut être que le fichier XML n’est pas correctement formaté, par exemple, si vous n’utilisez pas la mise en forme markdown correcte pour le caractère « & » dans le fichier XML, ou que l’éditeur de texte peut ajouter une 0xEF 0xBB 0xBF d’ordre d’byte au début des fichiers, ce qui provoque le non-bon travail de l’examen XML.</span><span class="sxs-lookup"><span data-stu-id="5dfab-294">Another reason could be that the XML file is not correctly formatted, for example, not using the correct markdown formatting for the "&" character in the XML file, or the text editor might add a byte order mark (BOM) 0xEF 0xBB 0xBF at the beginning of the files which causes the XML parsing not to work.</span></span> <span data-ttu-id="5dfab-295">Une solution simple consiste à télécharger [l’exemple de fichier](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) (sélectionnez **Raw,** puis **Enregistrer sous),** puis à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="5dfab-295">One simple solution is to download the [sample file](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) (select **Raw** and then **Save as**) and then update.</span></span>

<span data-ttu-id="5dfab-296">S’il existe une valeur et que la stratégie est gérée via la stratégie de groupe, vérifiez si l’appareil client peut accéder au chemin d’accès XML de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="5dfab-296">If there is a value and the policy is managed via Group Policy, check whether the client device can access the policy XML path.</span></span>

<span data-ttu-id="5dfab-297">**Comment puis-je savoir quel ordinateur utilise la version du client anti-programme malveillant inaltérable dans l’organisation ?**</span><span class="sxs-lookup"><span data-stu-id="5dfab-297">**How can I know which machine is using out of date antimalware client version in the organization?**</span></span>

<span data-ttu-id="5dfab-298">Vous pouvez utiliser la requête suivante pour obtenir la version du client anti-programme malveillant sur le portail Microsoft 365 sécurité :</span><span class="sxs-lookup"><span data-stu-id="5dfab-298">You can use following query to get antimalware client version on the Microsoft 365 security portal:</span></span>
```kusto
//check the antimalware client version
DeviceFileEvents
| where FileName == "MsMpEng.exe"
| where FolderPath contains @"C:\ProgramData\Microsoft\Windows Defender\Platform\"
| extend PlatformVersion=tostring(split(FolderPath, "\\", 5))
//| project DeviceName, PlatformVersion // check which machine is using legacy platformVersion
| summarize dcount(DeviceName) by PlatformVersion // check how many machines are using which platformVersion
| order by PlatformVersion desc
```
