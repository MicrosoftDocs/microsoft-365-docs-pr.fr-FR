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
ms.author: v-smandalika
author: v-smandalika
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: cf8e74a6886d7086da062d6258e3e1e1a1cbd730
ms.sourcegitcommit: 3e971b31435d17ceeaa9871c01e88e25ead560fb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "52861718"
---
# <a name="microsoft-defender-for-endpoint-device-control-removable-storage-access-control"></a><span data-ttu-id="dbaef-104">Contrôle d’appareil amovible Microsoft Defender for Endpoint Stockage Access Control</span><span class="sxs-lookup"><span data-stu-id="dbaef-104">Microsoft Defender for Endpoint Device Control Removable Storage Access Control</span></span>

[!INCLUDE [Prerelease](../includes/prerelease.md)]

<span data-ttu-id="dbaef-105">Microsoft Defender for Endpoint Device Control Removable Stockage Access Control vous permet d’accomplir la tâche suivante :</span><span class="sxs-lookup"><span data-stu-id="dbaef-105">Microsoft Defender for Endpoint Device Control Removable Storage Access Control enables you to do the following task:</span></span>
- <span data-ttu-id="dbaef-106">audit, autoriser ou empêcher l’accès en lecture, écriture ou exécution au stockage amovible avec ou sans exclusion</span><span class="sxs-lookup"><span data-stu-id="dbaef-106">auditing, allowing or preventing the read, write or execute access to removable storage with or without exclusion</span></span>

|<span data-ttu-id="dbaef-107">Privilège</span><span class="sxs-lookup"><span data-stu-id="dbaef-107">Privilege</span></span> |<span data-ttu-id="dbaef-108">Autorisation</span><span class="sxs-lookup"><span data-stu-id="dbaef-108">Permission</span></span>  |
|---------|---------|
|<span data-ttu-id="dbaef-109">Accès</span><span class="sxs-lookup"><span data-stu-id="dbaef-109">Access</span></span>    |  <span data-ttu-id="dbaef-110">Lecture, Écriture, Exécution</span><span class="sxs-lookup"><span data-stu-id="dbaef-110">Read, Write, Execute</span></span>       |
|<span data-ttu-id="dbaef-111">Action Mode</span><span class="sxs-lookup"><span data-stu-id="dbaef-111">Action Mode</span></span>    |    <span data-ttu-id="dbaef-112">Auditer, autoriser, empêcher</span><span class="sxs-lookup"><span data-stu-id="dbaef-112">Audit, Allow, Prevent</span></span>     |
|<span data-ttu-id="dbaef-113">Prise en charge du programme CSP</span><span class="sxs-lookup"><span data-stu-id="dbaef-113">CSP Support</span></span>   |   <span data-ttu-id="dbaef-114">Oui</span><span class="sxs-lookup"><span data-stu-id="dbaef-114">Yes</span></span>      |
|<span data-ttu-id="dbaef-115">Prise en charge des GPO</span><span class="sxs-lookup"><span data-stu-id="dbaef-115">GPO Support</span></span>    |   <span data-ttu-id="dbaef-116">Oui</span><span class="sxs-lookup"><span data-stu-id="dbaef-116">Yes</span></span>      |
|<span data-ttu-id="dbaef-117">Prise en charge basée sur l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="dbaef-117">User-based Support</span></span>     |   <span data-ttu-id="dbaef-118">Oui</span><span class="sxs-lookup"><span data-stu-id="dbaef-118">Yes</span></span>      |
|<span data-ttu-id="dbaef-119">Prise en charge basée sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="dbaef-119">Machine-based Support</span></span>    |    <span data-ttu-id="dbaef-120">Oui</span><span class="sxs-lookup"><span data-stu-id="dbaef-120">Yes</span></span>     |

## <a name="prepare-your-endpoints"></a><span data-ttu-id="dbaef-121">Préparer vos points de terminaison</span><span class="sxs-lookup"><span data-stu-id="dbaef-121">Prepare your endpoints</span></span>

<span data-ttu-id="dbaef-122">Déployez le contrôle d Stockage d’accès amovible sur Windows 10 qui ont un client anti-programme malveillant version **4.18.2103.3** ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="dbaef-122">Deploy Removable Storage Access Control on Windows 10 devices that have Anti-malware Client Version **4.18.2103.3 or later**.</span></span>
1. <span data-ttu-id="dbaef-123">**4.18.2104** ou version ultérieure : Ajouter SerialNumberId, VID_PID, prise en charge des GPO basés sur des chemins d’fichiers, ComputerSid</span><span class="sxs-lookup"><span data-stu-id="dbaef-123">**4.18.2104 or later**: Add SerialNumberId, VID_PID, filepath-based GPO support, ComputerSid</span></span>

2. <span data-ttu-id="dbaef-124">**4.18.2105** ou version ultérieure : ajouter la prise en charge des caractères génériques pour HardwareId/DeviceId/InstancePathId/FriendlyNameId/SerialNumberId, la combinaison d’un utilisateur spécifique sur un ordinateur spécifique, la prise en charge du SSD (Un SSD Extrême SanDisk)/USB Attached SCSI (UAS)</span><span class="sxs-lookup"><span data-stu-id="dbaef-124">**4.18.2105 or later**: Add Wildcard support for HardwareId/DeviceId/InstancePathId/FriendlyNameId/SerialNumberId, the combination of specific user on specific machine, removeable SSD (a SanDisk Extreme SSD)/USB Attached SCSI (UAS) support</span></span>

:::image type="content" source="images/powershell.png" alt-text="Interface PowerShell":::

   > [!NOTE]
   > <span data-ttu-id="dbaef-126">Aucun des Sécurité Windows n’a besoin d’être actif, vous pouvez exécuter le contrôle d’accès Stockage amovible indépendamment de l’état Sécurité Windows’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dbaef-126">None of Windows Security components need to be active, you can run Removable Storage Access Control independent of Windows Security status.</span></span>

## <a name="policy-properties"></a><span data-ttu-id="dbaef-127">Propriétés de stratégie</span><span class="sxs-lookup"><span data-stu-id="dbaef-127">Policy properties</span></span>


<span data-ttu-id="dbaef-128">Vous pouvez utiliser les propriétés suivantes pour créer un groupe de stockage amovible :</span><span class="sxs-lookup"><span data-stu-id="dbaef-128">You can use the following properties to create a removable storage group:</span></span>

<span data-ttu-id="dbaef-129">**Nom de la propriété : ID de groupe**</span><span class="sxs-lookup"><span data-stu-id="dbaef-129">**Property name: Group Id**</span></span>

1. <span data-ttu-id="dbaef-130">Description : [GUID](https://en.wikipedia.org/wiki/Universally_unique_identifier), un ID unique, représente le groupe et sera utilisé dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="dbaef-130">Description: [GUID](https://en.wikipedia.org/wiki/Universally_unique_identifier), a unique ID, represents the group and will be used in the policy.</span></span>

<span data-ttu-id="dbaef-131">**Nom de la propriété : DescriptorIdList**</span><span class="sxs-lookup"><span data-stu-id="dbaef-131">**Property name: DescriptorIdList**</span></span>

1. <span data-ttu-id="dbaef-132">Description : liste des propriétés d’appareil que vous souhaitez utiliser pour couvrir dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="dbaef-132">Description: List the device properties you want to use to cover in the group.</span></span>
<span data-ttu-id="dbaef-133">List the device properties you want to use to cover in the group.</span><span class="sxs-lookup"><span data-stu-id="dbaef-133">List the device properties you want to use to cover in the group.</span></span>
<span data-ttu-id="dbaef-134">Pour chaque propriété d’appareil, voir la section **Propriétés de** l’appareil ci-dessus pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="dbaef-134">For each device property, see **Device Properties** section above for more detail.</span></span>

1. <span data-ttu-id="dbaef-135">Options :</span><span class="sxs-lookup"><span data-stu-id="dbaef-135">Options:</span></span>
    - <span data-ttu-id="dbaef-136">ID principal</span><span class="sxs-lookup"><span data-stu-id="dbaef-136">Primary ID</span></span>
        - <span data-ttu-id="dbaef-137">RemovableMediaDevices</span><span class="sxs-lookup"><span data-stu-id="dbaef-137">RemovableMediaDevices</span></span>
        - <span data-ttu-id="dbaef-138">CdRomDevices</span><span class="sxs-lookup"><span data-stu-id="dbaef-138">CdRomDevices</span></span>
    - <span data-ttu-id="dbaef-139">DeviceId</span><span class="sxs-lookup"><span data-stu-id="dbaef-139">DeviceId</span></span>
    - <span data-ttu-id="dbaef-140">HardwareId</span><span class="sxs-lookup"><span data-stu-id="dbaef-140">HardwareId</span></span>
    - <span data-ttu-id="dbaef-141">InstancePathId : InstancePathId est une chaîne qui identifie de manière unique l’appareil dans le système, par exemple USBSTOR\DISK&VEN_GENERIC&PROD_FLASH_DISK&REV_8.07\8735B611&0.</span><span class="sxs-lookup"><span data-stu-id="dbaef-141">InstancePathId: InstancePathId is a string that uniquely identifies the device in the system, for example, USBSTOR\DISK&VEN_GENERIC&PROD_FLASH_DISK&REV_8.07\8735B611&0.</span></span> <span data-ttu-id="dbaef-142">Le numéro à la fin (par **exemple,&0**) représente l’emplacement disponible et peut changer d’appareil à appareil.</span><span class="sxs-lookup"><span data-stu-id="dbaef-142">The number at the end (for example **&0**) represents the available slot and may change from device to device.</span></span> <span data-ttu-id="dbaef-143">Pour de meilleurs résultats, utilisez un caractère générique à la fin.</span><span class="sxs-lookup"><span data-stu-id="dbaef-143">For best results, use a wildcard at the end.</span></span> <span data-ttu-id="dbaef-144">Par exemple, USBSTOR\DISK&VEN_GENERIC&PROD_FLASH_DISK&REV_8.07\8735B611\*</span><span class="sxs-lookup"><span data-stu-id="dbaef-144">For example, USBSTOR\DISK&VEN_GENERIC&PROD_FLASH_DISK&REV_8.07\8735B611\*</span></span>
    - <span data-ttu-id="dbaef-145">FriendlyNameId</span><span class="sxs-lookup"><span data-stu-id="dbaef-145">FriendlyNameId</span></span>
    - <span data-ttu-id="dbaef-146">SerialNumberId</span><span class="sxs-lookup"><span data-stu-id="dbaef-146">SerialNumberId</span></span>
    - <span data-ttu-id="dbaef-147">VID</span><span class="sxs-lookup"><span data-stu-id="dbaef-147">VID</span></span>
    - <span data-ttu-id="dbaef-148">PID</span><span class="sxs-lookup"><span data-stu-id="dbaef-148">PID</span></span>
    - <span data-ttu-id="dbaef-149">VID_PID</span><span class="sxs-lookup"><span data-stu-id="dbaef-149">VID_PID</span></span>
        - <span data-ttu-id="dbaef-150">0751_55E0 : correspondre à cette paire VID/PID exacte</span><span class="sxs-lookup"><span data-stu-id="dbaef-150">0751_55E0: match this exact VID/PID pair</span></span>
        - <span data-ttu-id="dbaef-151">_55E0 : faire correspondre n’importe quel média avec PID=55E0</span><span class="sxs-lookup"><span data-stu-id="dbaef-151">_55E0: match any media with PID=55E0</span></span>
        - <span data-ttu-id="dbaef-152">0751_: faire correspondre n’importe quel média avec VID=0751</span><span class="sxs-lookup"><span data-stu-id="dbaef-152">0751_: match any media with VID=0751</span></span>
        
<span data-ttu-id="dbaef-153">**Nom de la propriété : MatchType**</span><span class="sxs-lookup"><span data-stu-id="dbaef-153">**Property name: MatchType**</span></span> 

1. <span data-ttu-id="dbaef-154">Description : lorsque plusieurs propriétés d’appareil sont utilisées dans DescriptorIDList, MatchType définit la relation.</span><span class="sxs-lookup"><span data-stu-id="dbaef-154">Description: When there are multiple device properties being used in the DescriptorIDList, MatchType defines the relationship.</span></span>

1. <span data-ttu-id="dbaef-155">Options :</span><span class="sxs-lookup"><span data-stu-id="dbaef-155">Options:</span></span>
    - <span data-ttu-id="dbaef-156">MatchAll : tous les attributs sous la relation DescriptorIdList seront **And** ; par exemple, si l’administrateur place DeviceID et InstancePathID, pour chaque clé USB connectée, le système vérifie si la clé USB répond aux deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="dbaef-156">MatchAll: Any attributes under the DescriptorIdList will be **And** relationship; for example, if administrator puts DeviceID and InstancePathID, for every connected USB, system will check to see whether the USB meets both values.</span></span>

    - <span data-ttu-id="dbaef-157">MatchAny : les attributs sous la relation DescriptorIdList seront **Or** ; par exemple, si l’administrateur place DeviceID et InstancePathID, pour chaque clé USB connectée, le système appliquera l’application tant que la clé USB aura une valeur **DeviceID** ou **InstanceID** identique.</span><span class="sxs-lookup"><span data-stu-id="dbaef-157">MatchAny: The attributes under the DescriptorIdList will be **Or** relationship; for example, if administrator puts DeviceID and InstancePathID, for every connected USB, system will do the enforcement as long as the USB has either an identical **DeviceID** or **InstanceID** value.</span></span>



<span data-ttu-id="dbaef-158">Voici les propriétés de stratégie de contrôle d’accès :</span><span class="sxs-lookup"><span data-stu-id="dbaef-158">Following are the access control policy properties:</span></span>

<span data-ttu-id="dbaef-159">**Nom de la propriété : PolicyRuleId**</span><span class="sxs-lookup"><span data-stu-id="dbaef-159">**Property name: PolicyRuleId**</span></span>

1. <span data-ttu-id="dbaef-160">Description : [GUID](https://en.wikipedia.org/wiki/Universally_unique_identifier), un ID unique, représente la stratégie et sera utilisé dans le rapport et la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="dbaef-160">Description: [GUID](https://en.wikipedia.org/wiki/Universally_unique_identifier), a unique ID, represents the policy and will be used in the reporting and troubleshooting.</span></span>

<span data-ttu-id="dbaef-161">**Nom de la propriété : IncludedIdList**</span><span class="sxs-lookup"><span data-stu-id="dbaef-161">**Property name: IncludedIdList**</span></span>

1. <span data-ttu-id="dbaef-162">Description : groupe(s) à appliquer à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="dbaef-162">Description: The group(s) that the policy will be applied to.</span></span> <span data-ttu-id="dbaef-163">Si plusieurs groupes sont ajoutés, la stratégie est appliquée à n’importe quel média de tous ces groupes.</span><span class="sxs-lookup"><span data-stu-id="dbaef-163">If multiple groups are added, the policy will be applied to any media in all those groups.</span></span>

1. <span data-ttu-id="dbaef-164">Options : l’ID de groupe/GUID doit être utilisé à cette instance.</span><span class="sxs-lookup"><span data-stu-id="dbaef-164">Options: The Group ID/GUID must be used at this instance.</span></span>

<span data-ttu-id="dbaef-165">L’exemple suivant illustre l’utilisation de GroupID :</span><span class="sxs-lookup"><span data-stu-id="dbaef-165">The following example shows the usage of GroupID:</span></span>

`<IncludedIdList> <GroupId>{EAA4CCE5-F6C9-4760-8BAD-FDCC76A2ACA1}</GroupId> </IncludedIdList>`

<span data-ttu-id="dbaef-166">**Nom de la propriété : ExcludedIDList**</span><span class="sxs-lookup"><span data-stu-id="dbaef-166">**Property name: ExcludedIDList**</span></span>

1. <span data-ttu-id="dbaef-167">Description : groupe(s) à qui la stratégie ne sera pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="dbaef-167">Description: The group(s) that the policy will not be applied to.</span></span>
1. <span data-ttu-id="dbaef-168">Options : l’ID de groupe/GUID doit être utilisé à cette instance.</span><span class="sxs-lookup"><span data-stu-id="dbaef-168">Options: The Group ID/GUID must be used at this instance.</span></span>

<span data-ttu-id="dbaef-169">**Nom de la propriété : ID d’entrée**</span><span class="sxs-lookup"><span data-stu-id="dbaef-169">**Property name: Entry Id**</span></span>

1. <span data-ttu-id="dbaef-170">Description : un policyRule peut avoir plusieurs entrées ; chaque entrée avec un GUID unique indique à Device Control une restriction.</span><span class="sxs-lookup"><span data-stu-id="dbaef-170">Description: One PolicyRule can have multiple entries; each entry with a unique GUID tells Device Control one restriction.</span></span>

<span data-ttu-id="dbaef-171">**Nom de la propriété : Type**</span><span class="sxs-lookup"><span data-stu-id="dbaef-171">**Property name: Type**</span></span>

1. <span data-ttu-id="dbaef-172">Description : définit l’action pour les groupes de stockage amovibles dans IncludedIDList.</span><span class="sxs-lookup"><span data-stu-id="dbaef-172">Description: Defines the action for the removable storage groups in IncludedIDList.</span></span>
    - <span data-ttu-id="dbaef-173">Application : autoriser ou refuser</span><span class="sxs-lookup"><span data-stu-id="dbaef-173">Enforcement: Allow or Deny</span></span>
    - <span data-ttu-id="dbaef-174">Audit : AuditAllowed ou AuditDenied</span><span class="sxs-lookup"><span data-stu-id="dbaef-174">Audit: AuditAllowed or AuditDenied</span></span> 
1. <span data-ttu-id="dbaef-175">Options :</span><span class="sxs-lookup"><span data-stu-id="dbaef-175">Options:</span></span>
    - <span data-ttu-id="dbaef-176">Autoriser</span><span class="sxs-lookup"><span data-stu-id="dbaef-176">Allow</span></span>
    - <span data-ttu-id="dbaef-177">Refuser</span><span class="sxs-lookup"><span data-stu-id="dbaef-177">Deny</span></span>
    - <span data-ttu-id="dbaef-178">AuditAllowed : définit la notification et l’événement lorsque l’accès est autorisé</span><span class="sxs-lookup"><span data-stu-id="dbaef-178">AuditAllowed: Defines notification and event when access is allowed</span></span>
    - <span data-ttu-id="dbaef-179">AuditDenied : définit la notification et l’événement lorsque l’accès est refusé ; doit fonctionner avec **l’entrée** de refus.</span><span class="sxs-lookup"><span data-stu-id="dbaef-179">AuditDenied: Defines notification and event when access is denied; has to work together with **Deny** entry.</span></span>

<span data-ttu-id="dbaef-180">Lorsqu’il existe des types de conflit pour le même média, le système applique le premier de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="dbaef-180">When there are conflict types for the same media, the system will apply the first one in the policy.</span></span> <span data-ttu-id="dbaef-181">Un exemple de type de conflit est **Allow** et **Deny**.</span><span class="sxs-lookup"><span data-stu-id="dbaef-181">An example of a conflict type is **Allow** and **Deny**.</span></span>

<span data-ttu-id="dbaef-182">**Nom de la propriété : Sid**</span><span class="sxs-lookup"><span data-stu-id="dbaef-182">**Property name: Sid**</span></span>

1. <span data-ttu-id="dbaef-183">Description : définit si cette stratégie est appliquée à un utilisateur ou à un groupe d’utilisateurs spécifique ; une entrée peut avoir un sid et une entrée sans sid signifie appliquer la stratégie sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dbaef-183">Description: Defines whether apply this policy over specific user or user group; one entry can have maximum one Sid and an entry without any Sid means applying the policy over the machine.</span></span>

<span data-ttu-id="dbaef-184">**Nom de la propriété : ComputerSid**</span><span class="sxs-lookup"><span data-stu-id="dbaef-184">**Property name: ComputerSid**</span></span>

1. <span data-ttu-id="dbaef-185">Description : définit si cette stratégie est appliquée sur un ordinateur ou un groupe d’ordinateurs spécifique ; Une entrée peut avoir un maximum d’un ComputerSid et une entrée sans ComputerSid signifie appliquer la stratégie sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dbaef-185">Description: Defines whether apply this policy over specific machine or machine group; one entry can have maximum one ComputerSid and an entry without any ComputerSid means applying the policy over the machine.</span></span> <span data-ttu-id="dbaef-186">Si vous souhaitez appliquer une entrée à un utilisateur spécifique et à un ordinateur spécifique, ajoutez Sid et ComputerSid dans la même entrée.</span><span class="sxs-lookup"><span data-stu-id="dbaef-186">If you want to apply an Entry to a specific user and specific machine, add both Sid and ComputerSid into the same Entry.</span></span>

<span data-ttu-id="dbaef-187">**Nom de la propriété : Options**</span><span class="sxs-lookup"><span data-stu-id="dbaef-187">**Property name: Options**</span></span>

1. <span data-ttu-id="dbaef-188">Description : définit s’il faut afficher la notification ou non.</span><span class="sxs-lookup"><span data-stu-id="dbaef-188">Description: Defines whether to display notification or not.</span></span>

   :::image type="content" source="images/device-status.png" alt-text="Écran sur lequel l’état de l’appareil est visible":::

1. <span data-ttu-id="dbaef-190">Options : 0-4.</span><span class="sxs-lookup"><span data-stu-id="dbaef-190">Options: 0-4.</span></span> <span data-ttu-id="dbaef-191">Lorsque le type Autoriser ou Refuser est sélectionné :</span><span class="sxs-lookup"><span data-stu-id="dbaef-191">When Type Allow or Deny is selected:</span></span>

   - <span data-ttu-id="dbaef-192">0 : rien</span><span class="sxs-lookup"><span data-stu-id="dbaef-192">0: nothing</span></span>
   - <span data-ttu-id="dbaef-193">4 : désactivez **AuditAllowed** et **AuditDenied** pour cette entrée.</span><span class="sxs-lookup"><span data-stu-id="dbaef-193">4: disable **AuditAllowed** and **AuditDenied** for this Entry.</span></span> <span data-ttu-id="dbaef-194">Même si **le blocage** se produit et que le paramètre **AuditDenied** est configuré, le système n’affiche pas de notification.</span><span class="sxs-lookup"><span data-stu-id="dbaef-194">Even if **Block** happens and the **AuditDenied** is setting configured, the system will not show notification.</span></span>

   <span data-ttu-id="dbaef-195">Lorsque type **AuditAllowed ou** **AuditDenied** est sélectionné :</span><span class="sxs-lookup"><span data-stu-id="dbaef-195">When Type **AuditAllowed** or **AuditDenied** is selected:</span></span>

   - <span data-ttu-id="dbaef-196">0 : rien</span><span class="sxs-lookup"><span data-stu-id="dbaef-196">0: nothing</span></span>
   - <span data-ttu-id="dbaef-197">1 : afficher la notification</span><span class="sxs-lookup"><span data-stu-id="dbaef-197">1: show notification</span></span>
   - <span data-ttu-id="dbaef-198">2 : événement d’envoi</span><span class="sxs-lookup"><span data-stu-id="dbaef-198">2: send event</span></span>
   - <span data-ttu-id="dbaef-199">3 : afficher la notification et envoyer un événement</span><span class="sxs-lookup"><span data-stu-id="dbaef-199">3: show notification and send event</span></span>

<span data-ttu-id="dbaef-200">**Nom de la propriété : AccessMask**</span><span class="sxs-lookup"><span data-stu-id="dbaef-200">**Property name: AccessMask**</span></span>

1. <span data-ttu-id="dbaef-201">Description : définit l’accès.</span><span class="sxs-lookup"><span data-stu-id="dbaef-201">Description: Defines the access.</span></span>

1. <span data-ttu-id="dbaef-202">Options : 1-7 :</span><span class="sxs-lookup"><span data-stu-id="dbaef-202">Options: 1-7:</span></span>
    - <span data-ttu-id="dbaef-203">1 : lecture</span><span class="sxs-lookup"><span data-stu-id="dbaef-203">1: Read</span></span>
    - <span data-ttu-id="dbaef-204">2 : Écriture</span><span class="sxs-lookup"><span data-stu-id="dbaef-204">2: Write</span></span>
    - <span data-ttu-id="dbaef-205">3 : Lecture et écriture</span><span class="sxs-lookup"><span data-stu-id="dbaef-205">3: Read and Write</span></span>
    - <span data-ttu-id="dbaef-206">4 : Exécuter</span><span class="sxs-lookup"><span data-stu-id="dbaef-206">4: Execute</span></span>
    - <span data-ttu-id="dbaef-207">5 : Lecture et exécution</span><span class="sxs-lookup"><span data-stu-id="dbaef-207">5: Read and Execute</span></span>
    - <span data-ttu-id="dbaef-208">6 : Écriture et exécution</span><span class="sxs-lookup"><span data-stu-id="dbaef-208">6: Write and Execute</span></span>
    - <span data-ttu-id="dbaef-209">7 : Lecture et écriture et exécution</span><span class="sxs-lookup"><span data-stu-id="dbaef-209">7: Read and Write and Execute</span></span>

## <a name="common-removable-storage-access-control-scenarios"></a><span data-ttu-id="dbaef-210">Scénarios courants Stockage contrôle d’accès des périphériques amovibles</span><span class="sxs-lookup"><span data-stu-id="dbaef-210">Common Removable Storage Access Control scenarios</span></span>

<span data-ttu-id="dbaef-211">Pour vous aider à vous familiariser avec Microsoft Defender pour endpoint Removable Stockage Access Control, nous avons mis en place des scénarios courants que vous pouvez suivre.</span><span class="sxs-lookup"><span data-stu-id="dbaef-211">To help familiarize you with Microsoft Defender for Endpoint Removable Storage Access Control, we have put together some common scenarios for you to follow.</span></span>

### <a name="scenario-1-prevent-write-and-execute-access-to-all-but-allow-specific-approved-usbs"></a><span data-ttu-id="dbaef-212">Scénario 1 : empêcher l’accès en écriture et en exécution à tous les utilisateurs approuvés spécifiques, mais autoriser</span><span class="sxs-lookup"><span data-stu-id="dbaef-212">Scenario 1: Prevent Write and Execute access to all but allow specific approved USBs</span></span>

1. <span data-ttu-id="dbaef-213">Créer des groupes</span><span class="sxs-lookup"><span data-stu-id="dbaef-213">Create groups</span></span>
    1. <span data-ttu-id="dbaef-214">Groupe 1 : Tout stockage amovible et CD/DVD.</span><span class="sxs-lookup"><span data-stu-id="dbaef-214">Group 1: Any removable storage and CD/DVD.</span></span> <span data-ttu-id="dbaef-215">Un exemple de stockage amovible et de CD/DVD est le groupe **9b28fae8-72f7-4267-a1a5-685f747a7146** dans l’exemple de fichier de Group.xmlany [Removable Stockage et CD-DVD.](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples)</span><span class="sxs-lookup"><span data-stu-id="dbaef-215">An example of a removable storage and CD/DVD is: Group **9b28fae8-72f7-4267-a1a5-685f747a7146** in the sample [Any Removable Storage and CD-DVD Group.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span>
    
    2. <span data-ttu-id="dbaef-216">Groupe 2 : approbation de base de données américaines en fonction des propriétés de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dbaef-216">Group 2: Approved USBs based on device properties.</span></span> <span data-ttu-id="dbaef-217">Exemple de ce cas d’utilisation : ID d’instance – Groupe **65fa649a-a111-4912-9294-fb6337a25038** dans l’exemple de fichier Group.xmlde base de données approuvé. [](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples)</span><span class="sxs-lookup"><span data-stu-id="dbaef-217">An example for this use case is: Instance ID – Group **65fa649a-a111-4912-9294-fb6337a25038** in the sample [Approved USBs Group.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dbaef-218">Vous devez remplacer `&` par `&amp;` dans la valeur.</span><span class="sxs-lookup"><span data-stu-id="dbaef-218">You have to replace `&` with `&amp;` in the value.</span></span>

2. <span data-ttu-id="dbaef-219">Création d’une stratégie</span><span class="sxs-lookup"><span data-stu-id="dbaef-219">Create policy</span></span>
    1. <span data-ttu-id="dbaef-220">Stratégie 1 : bloquer l’écriture et exécuter l’accès, mais autoriser les usbs approuvés.</span><span class="sxs-lookup"><span data-stu-id="dbaef-220">Policy 1: Block Write and Execute Access but allow approved USBs.</span></span> <span data-ttu-id="dbaef-221">Voici un exemple de ce cas d’utilisation : PolicyRule **c544a991-5786-4402-949e-a032cb790d0e dans** l’exemple Scénario [1](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) Bloquer l’écriture et exécuter l’accès, mais autoriser le fichier .xmlapprouvé.</span><span class="sxs-lookup"><span data-stu-id="dbaef-221">An example for this use case is: PolicyRule **c544a991-5786-4402-949e-a032cb790d0e** in the sample [Scenario 1 Block Write and Execute Access but allow approved USBs .xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span>
    
    2. <span data-ttu-id="dbaef-222">Stratégie 2 : auditer l’accès en écriture et en cours d’exécution aux usbs autorisés.</span><span class="sxs-lookup"><span data-stu-id="dbaef-222">Policy 2: Audit Write and Execute access to allowed USBs.</span></span> <span data-ttu-id="dbaef-223">Voici un exemple de ce cas d’utilisation : PolicyRule **36ae1037-a639-4cff-946b-b36c53089a4c** dans l’exemple scénario [1 Auditer](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) l’accès en écriture et en exécution au fichier USBs.xmlapprouvé.</span><span class="sxs-lookup"><span data-stu-id="dbaef-223">An example for this use case is: PolicyRule **36ae1037-a639-4cff-946b-b36c53089a4c** in the sample [Scenario 1 Audit Write and Execute access to approved USBs.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span>

### <a name="scenario-2-audit-write-and-execute-access-to-all-but-block-specific-unapproved-usbs"></a><span data-ttu-id="dbaef-224">Scénario 2 : Auditer l’accès en écriture et en exécution à tous les services de sécurité universels non désapprouvés, sauf bloquer</span><span class="sxs-lookup"><span data-stu-id="dbaef-224">Scenario 2: Audit Write and Execute access to all but block specific unapproved USBs</span></span>

1. <span data-ttu-id="dbaef-225">Créer des groupes</span><span class="sxs-lookup"><span data-stu-id="dbaef-225">Create groups</span></span>
    1. <span data-ttu-id="dbaef-226">Groupe 1 : Tout stockage amovible et CD/DVD.</span><span class="sxs-lookup"><span data-stu-id="dbaef-226">Group 1: Any removable storage and CD/DVD.</span></span> <span data-ttu-id="dbaef-227">Voici un exemple de ce cas d’utilisation : Groupe **9b28fae8-72f7-4267-a1a5-685f747a7146** dans l’exemple de fichier de Stockage amovible et [de CD-DVD Group.xml.](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples)</span><span class="sxs-lookup"><span data-stu-id="dbaef-227">An example for this use case is: Group **9b28fae8-72f7-4267-a1a5-685f747a7146** in the sample [Any Removable Storage and CD-DVD Group.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span>
    
    2. <span data-ttu-id="dbaef-228">Groupe 2 : listes de contrôle d’appareil non désapprouvées en fonction des propriétés de l’appareil, par exemple, ID fournisseur/ID de produit, nom convivial – Groupe **65fa649a-a111-4912-9294-fb6337a25038** dans l’exemple de fichier Group.xmlde base de données des [états-Group.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) non accepté.</span><span class="sxs-lookup"><span data-stu-id="dbaef-228">Group 2: Unapproved USBs based on device properties, for example, Vendor ID / Product ID, Friendly Name – Group **65fa649a-a111-4912-9294-fb6337a25038** in the sample [Unapproved USBs Group.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="dbaef-229">Vous devez remplacer `&` par `&amp;` dans la valeur.</span><span class="sxs-lookup"><span data-stu-id="dbaef-229">You have to replace `&` with `&amp;` in the value.</span></span>

2. <span data-ttu-id="dbaef-230">Création d’une stratégie</span><span class="sxs-lookup"><span data-stu-id="dbaef-230">Create policy</span></span>
    1. <span data-ttu-id="dbaef-231">Stratégie 1 : bloquer l’accès en écriture et en exécution à tous les usbs non désapprouvés spécifiques, sauf à les bloquer.</span><span class="sxs-lookup"><span data-stu-id="dbaef-231">Policy 1: Block Write and Execute access to all but block specific unapproved USBs.</span></span> <span data-ttu-id="dbaef-232">Voici un exemple de ce cas d’utilisation : PolicyRule **23b8e437-66ac-4b32-b3d7-24044637fc98** dans l’exemple Scénario [2 Auditer](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) l’écriture et l’exécution de l’accès à tous les fichiers USBs.xmlnon acceptés, sauf bloquer.</span><span class="sxs-lookup"><span data-stu-id="dbaef-232">An example of this use case is: PolicyRule **23b8e437-66ac-4b32-b3d7-24044637fc98** in the sample [Scenario 2 Audit Write and Execute access to all but block specific unapproved USBs.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span>
    
    2. <span data-ttu-id="dbaef-233">Stratégie 2 : auditer l’accès en écriture et exécuter l’accès à d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="dbaef-233">Policy 2: Audit Write and Execute access to others.</span></span> <span data-ttu-id="dbaef-234">Voici un exemple de ce cas d’utilisation : PolicyRule **b58ab853-9a6f-405c-a194-740e69422b48** dans l’exemple Scénario [2 Auditer](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) l’accès en écriture et en exécution au fichier others.xml.</span><span class="sxs-lookup"><span data-stu-id="dbaef-234">An example of this use case is: PolicyRule **b58ab853-9a6f-405c-a194-740e69422b48** in the sample [Scenario 2 Audit Write and Execute access to others.xml](https://github.com/microsoft/mdatp-devicecontrol/tree/main/Removable%20Storage%20Access%20Control%20Samples) file.</span></span>

## <a name="deploying-and-managing-policy-via-group-policy"></a><span data-ttu-id="dbaef-235">Déploiement et gestion d’une stratégie via une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="dbaef-235">Deploying and managing policy via Group Policy</span></span>

<span data-ttu-id="dbaef-236">La fonctionnalité de contrôle d Stockage’accès amovible vous permet d’appliquer une stratégie via la stratégie de groupe à l’utilisateur ou à l’appareil, ou aux deux.</span><span class="sxs-lookup"><span data-stu-id="dbaef-236">The Removable Storage Access Control feature enables you to apply policy via Group Policy to either user or device, or both.</span></span>

### <a name="licensing"></a><span data-ttu-id="dbaef-237">Licences</span><span class="sxs-lookup"><span data-stu-id="dbaef-237">Licensing</span></span>

<span data-ttu-id="dbaef-238">Avant de commencer avec le contrôle d’accès Stockage amovible, vous devez confirmer [votre abonnement Microsoft 365.](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=2)</span><span class="sxs-lookup"><span data-stu-id="dbaef-238">Before you get started with Removable Storage Access Control, you must confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=2).</span></span> <span data-ttu-id="dbaef-239">Pour accéder au contrôle d’accès Stockage et l’utiliser, vous devez Microsoft 365 E3 ou Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="dbaef-239">To access and use Removable Storage Access Control, you must have Microsoft 365 E3 or Microsoft 365 E5.</span></span>

### <a name="deploying-policy-via-group-policy"></a><span data-ttu-id="dbaef-240">Déploiement d’une stratégie via une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="dbaef-240">Deploying policy via Group Policy</span></span>

1. <span data-ttu-id="dbaef-241">Combinez tous les groupes `<Groups>` `</Groups>` au sein d’un fichier xml.</span><span class="sxs-lookup"><span data-stu-id="dbaef-241">Combine all groups within `<Groups>` `</Groups>` into one xml file.</span></span> 

    <span data-ttu-id="dbaef-242">L’image suivante illustre l’exemple du scénario 1 : empêcher l’accès en écriture et en exécution à tous les [usbs approuvés spécifiques,](#scenario-1-prevent-write-and-execute-access-to-all-but-allow-specific-approved-usbs)sauf autoriser.</span><span class="sxs-lookup"><span data-stu-id="dbaef-242">The following image illustrates the example of [Scenario 1: Prevent Write and Execute access to all but allow specific approved USBs](#scenario-1-prevent-write-and-execute-access-to-all-but-allow-specific-approved-usbs).</span></span>
    
    :::image type="content" source="images/prevent-write-access-allow-usb.png" alt-text="Écran affichant les paramètres de configuration qui autorisent des usbs approuvés spécifiques sur les appareils":::
    
2. <span data-ttu-id="dbaef-244">Combinez toutes les règles `<PolicyRules>` `</PolicyRules>` dans un fichier xml.</span><span class="sxs-lookup"><span data-stu-id="dbaef-244">Combine all rules within `<PolicyRules>` `</PolicyRules>` into one xml file.</span></span> 

    <span data-ttu-id="dbaef-245">Si vous souhaitez limiter un utilisateur spécifique, utilisez la propriété SID dans l’entrée.</span><span class="sxs-lookup"><span data-stu-id="dbaef-245">If you want to restrict a specific user, then use SID property into the Entry.</span></span> <span data-ttu-id="dbaef-246">S’il n’existe aucun SID dans l’entrée de stratégie, l’entrée est appliquée à l’instance de connexion de tout le monde pour l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dbaef-246">If there is no SID in the policy Entry, the Entry will be applied to everyone login instance for the machine.</span></span>
    
    <span data-ttu-id="dbaef-247">L’image suivante illustre l’utilisation de la propriété SID et un exemple de scénario 1 : empêcher l’accès en écriture et en exécution à tous les [usbs approuvés spécifiques,](#scenario-1-prevent-write-and-execute-access-to-all-but-allow-specific-approved-usbs)sauf autoriser.</span><span class="sxs-lookup"><span data-stu-id="dbaef-247">The following image illustrates the usage of SID property, and an example of [Scenario 1: Prevent Write and Execute access to all but allow specific approved USBs](#scenario-1-prevent-write-and-execute-access-to-all-but-allow-specific-approved-usbs).</span></span>
    
    :::image type="content" source="images/usage-sid-property.png" alt-text="Écran affichant un code qui indique l’utilisation de l’attribut de propriété SID":::

3. <span data-ttu-id="dbaef-249">Enregistrez les fichiers XML de règle et de groupe sur le dossier de partage réseau et placez le chemin d’accès du dossier de partage réseau dans le paramètre de stratégie de groupe : Configuration ordinateur -> Modèles d’administration **-> Windows Composants -> Antivirus Microsoft Defender -> Contrôle** d’appareil : « Définir des groupes de stratégies de contrôle d’appareil » et « Définir des règles de stratégie de contrôle d’appareil ».</span><span class="sxs-lookup"><span data-stu-id="dbaef-249">Save both rule and group XML files on network share folder and put network share folder path into the Group Policy setting: **Computer Configuration -> Administrative Templates -> Windows Components -> Microsoft Defender Antivirus -> Device Control: ‘Define device control policy groups’ and ‘Define device control policy rules’**.</span></span>

    - <span data-ttu-id="dbaef-250">L’ordinateur cible doit pouvoir accéder au partage réseau pour avoir la stratégie.</span><span class="sxs-lookup"><span data-stu-id="dbaef-250">The target machine must be able to access the network share to have the policy.</span></span> <span data-ttu-id="dbaef-251">Toutefois, une fois la stratégie lue, la connexion de partage réseau n’est plus nécessaire, même après le redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dbaef-251">However, once the policy is read, the network share connection is no longer required, even after machine reboot.</span></span>

    :::image type="content" source="images/device-control.png" alt-text="Écran Contrôle d’appareil":::

## <a name="deploying-and-managing-policy-via-intune-oma-uri"></a><span data-ttu-id="dbaef-253">Déploiement et gestion d’une stratégie via Intune OMA-URI</span><span class="sxs-lookup"><span data-stu-id="dbaef-253">Deploying and managing policy via Intune OMA-URI</span></span>

<span data-ttu-id="dbaef-254">La fonctionnalité Stockage contrôle d’accès amovible vous permet d’appliquer une stratégie via OMA-URI à l’utilisateur ou à l’appareil, ou aux deux.</span><span class="sxs-lookup"><span data-stu-id="dbaef-254">The Removable Storage Access Control feature enables you to apply policy via OMA-URI to either user or device, or both.</span></span>

### <a name="licensing"></a><span data-ttu-id="dbaef-255">Licences</span><span class="sxs-lookup"><span data-stu-id="dbaef-255">Licensing</span></span>

<span data-ttu-id="dbaef-256">Avant de commencer avec le contrôle d’accès Stockage amovible, vous devez confirmer [votre abonnement Microsoft 365.](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=2)</span><span class="sxs-lookup"><span data-stu-id="dbaef-256">Before you get started with Removable Storage Access Control, you  must confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=2).</span></span> <span data-ttu-id="dbaef-257">Pour accéder au contrôle d’accès Stockage et l’utiliser, vous devez Microsoft 365 E3 ou Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="dbaef-257">To access and use Removable Storage Access Control, you must have Microsoft 365 E3 or Microsoft 365 E5.</span></span>

### <a name="permission"></a><span data-ttu-id="dbaef-258">Autorisation</span><span class="sxs-lookup"><span data-stu-id="dbaef-258">Permission</span></span>

<span data-ttu-id="dbaef-259">Pour le déploiement de stratégie dans Intune, le compte doit être autorisé à créer, modifier, mettre à jour ou supprimer des profils de configuration d’appareil.</span><span class="sxs-lookup"><span data-stu-id="dbaef-259">For policy deployment in Intune, the account must have permissions to create, edit, update, or delete device configuration profiles.</span></span> <span data-ttu-id="dbaef-260">Vous pouvez créer des rôles personnalisés ou utiliser n’importe quel rôle intégré avec ces autorisations.</span><span class="sxs-lookup"><span data-stu-id="dbaef-260">You can create custom roles or use any of the built-in roles with these permissions.</span></span>

- <span data-ttu-id="dbaef-261">Rôle gestionnaire de stratégies et de profils</span><span class="sxs-lookup"><span data-stu-id="dbaef-261">Policy and profile Manager role</span></span>
- <span data-ttu-id="dbaef-262">Rôle personnalisé avec les autorisations Créer/Modifier/Mettre à jour/Lecture/Supprimer/Afficher les rapports pour les profils de configuration d’appareil</span><span class="sxs-lookup"><span data-stu-id="dbaef-262">Custom role with Create/Edit/Update/Read/Delete/View Reports permissions turned on for Device Configuration profiles</span></span>
- <span data-ttu-id="dbaef-263">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="dbaef-263">Global administrator</span></span>

### <a name="deploying-policy-via-oma-uri"></a><span data-ttu-id="dbaef-264">Déploiement d’une stratégie via OMA-URI</span><span class="sxs-lookup"><span data-stu-id="dbaef-264">Deploying policy via OMA-URI</span></span>

<span data-ttu-id="dbaef-265">**Microsoft Endpoint Manager admin center ( https://endpoint.microsoft.com/) -> Devices -> Configuration profiles -> Create profile -> Platform: Windows 10 and later & Profile: Custom**</span><span class="sxs-lookup"><span data-stu-id="dbaef-265">**Microsoft Endpoint Manager admin center (https://endpoint.microsoft.com/) -> Devices -> Configuration profiles -> Create profile -> Platform: Windows 10 and later & Profile: Custom**</span></span>

1. <span data-ttu-id="dbaef-266">Pour chaque groupe, créez une règle OMA-URI :</span><span class="sxs-lookup"><span data-stu-id="dbaef-266">For each Group, create an OMA-URI rule:</span></span>
    - <span data-ttu-id="dbaef-267">OMA-URI : </span><span class="sxs-lookup"><span data-stu-id="dbaef-267">OMA-URI:</span></span>

      <span data-ttu-id="dbaef-268">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyGroups/%7b **GroupGUID**%7d/GroupData</span><span class="sxs-lookup"><span data-stu-id="dbaef-268">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyGroups/%7b **GroupGUID**%7d/GroupData</span></span>

      <span data-ttu-id="dbaef-269">Par exemple, pour tout stockage amovible et groupe **CD/DVD** dans l’exemple, le lien doit être :</span><span class="sxs-lookup"><span data-stu-id="dbaef-269">For example, for **any removable storage and CD/DVD** group in the sample, the link must be:</span></span>

      <span data-ttu-id="dbaef-270">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyGroups/%7b9b28fae8-72f7-4267-a1a5-685f747a7146%7d/GroupData</span><span class="sxs-lookup"><span data-stu-id="dbaef-270">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyGroups/%7b9b28fae8-72f7-4267-a1a5-685f747a7146%7d/GroupData</span></span>

    - <span data-ttu-id="dbaef-271">Type de données : chaîne (fichier XML)</span><span class="sxs-lookup"><span data-stu-id="dbaef-271">Data Type: String (XML file)</span></span>
    
      :::image type="content" source="images/xml-data-type-string.png" alt-text="Fichier xml pour le type de données STRING":::

2. <span data-ttu-id="dbaef-273">Pour chaque stratégie, créez également un OMA-URI :</span><span class="sxs-lookup"><span data-stu-id="dbaef-273">For each policy, also create an OMA-URI:</span></span>

    - <span data-ttu-id="dbaef-274">OMA-URI : </span><span class="sxs-lookup"><span data-stu-id="dbaef-274">OMA-URI:</span></span>

      <span data-ttu-id="dbaef-275">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyRules/%7bFA6BE102-0784-4A2A-B010-A0BEBEBF68E1%7d/RuleData</span><span class="sxs-lookup"><span data-stu-id="dbaef-275">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyRules/%7bFA6BE102-0784-4A2A-B010-A0BEBEBF68E1%7d/RuleData</span></span>

      <span data-ttu-id="dbaef-276">Par exemple, pour la règle Bloquer l’écriture et exécuter l’accès, mais autoriser les règles de base de données utilisateur **approuvées** dans l’exemple, le lien doit être :</span><span class="sxs-lookup"><span data-stu-id="dbaef-276">For example, for the **Block Write and Execute Access but allow approved USBs** rule in the sample, the link must be:</span></span> 

      <span data-ttu-id="dbaef-277">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyRules/%7bc544a991-5786-4402-949e-a032cb790d0e%7d/RuleData.</span><span class="sxs-lookup"><span data-stu-id="dbaef-277">./Vendor/MSFT/Defender/Configuration/DeviceControl/PolicyRules/%7bc544a991-5786-4402-949e-a032cb790d0e%7d/RuleData.</span></span>

    - <span data-ttu-id="dbaef-278">Type de données : chaîne (fichier XML)</span><span class="sxs-lookup"><span data-stu-id="dbaef-278">Data Type: String (XML file)</span></span>

      :::image type="content" source="images/xml-data-type-string-2.png" lightbox="images/xml-data-type-string-2.png" alt-text="Affichage du fichier XML pour le type de données STRING":::

## <a name="deploying-and-managing-policy-by-using-intune-user-interface"></a><span data-ttu-id="dbaef-280">Déploiement et gestion d’une stratégie à l’aide de l’interface utilisateur Intune</span><span class="sxs-lookup"><span data-stu-id="dbaef-280">Deploying and managing policy by using Intune user interface</span></span>

<span data-ttu-id="dbaef-281">Cette fonctionnalité (dans le Centre d’administration Microsoft Endpoint Manager ( profils de configuration > Périphériques > > Créer un profil https://endpoint.microsoft.com/) > Platform: Windows 10 and later & Profile: Device Control) n’est pas encore disponible.</span><span class="sxs-lookup"><span data-stu-id="dbaef-281">This capability (in Microsoft Endpoint Manager admin center (https://endpoint.microsoft.com/) > Devices > Configuration profiles > Create profile > Platform: Windows 10 and later & Profile: Device Control) is not yet available.</span></span> 

## <a name="view-device-control-removable-storage-access-control-data-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="dbaef-282">Afficher les données de contrôle d’Stockage d’accès amovible dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="dbaef-282">View Device Control Removable Storage Access Control data in Microsoft Defender for Endpoint</span></span>

<span data-ttu-id="dbaef-283">Le portail Microsoft 365 de sécurité affiche le stockage amovible bloqué par le contrôle d’Stockage d’accès.</span><span class="sxs-lookup"><span data-stu-id="dbaef-283">The Microsoft 365 security portal shows removable storage blocked by the Device Control Removable Storage Access Control.</span></span> <span data-ttu-id="dbaef-284">Pour accéder à la sécurité Microsoft 365, vous devez avoir l’abonnement suivant :</span><span class="sxs-lookup"><span data-stu-id="dbaef-284">To access the Microsoft 365 security, you must have the following subscription:</span></span>

- <span data-ttu-id="dbaef-285">Microsoft 365 de rapports E5</span><span class="sxs-lookup"><span data-stu-id="dbaef-285">Microsoft 365 for E5 reporting</span></span>

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
