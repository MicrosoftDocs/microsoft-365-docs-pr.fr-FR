---
title: Gérer la clé client
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 02/05/2020
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Après avoir installé la clé client, découvrez comment la gérer en restaurant des clés AKV et en gérant les autorisations et vos stratégies de chiffrement de données.
ms.openlocfilehash: 8f55667254ce7f5cbd9d4de274623ca4a3c4aa9d
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50909946"
---
# <a name="manage-customer-key"></a><span data-ttu-id="0c1e1-103">Gérer la clé client</span><span class="sxs-lookup"><span data-stu-id="0c1e1-103">Manage Customer Key</span></span>

<span data-ttu-id="0c1e1-104">Après avoir installé la clé client pour Office 365, vous pouvez gérer vos clés comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-104">After you've set up Customer Key for Office 365, you can manage your keys as described in this article.</span></span> <span data-ttu-id="0c1e1-105">En savoir plus sur la clé client dans les rubriques connexes.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-105">Learn more about Customer Key in the related topics.</span></span>

## <a name="restore-azure-key-vault-keys"></a><span data-ttu-id="0c1e1-106">Restaurer les clés Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="0c1e1-106">Restore Azure Key Vault keys</span></span>

<span data-ttu-id="0c1e1-107">Avant d’effectuer une restauration, utilisez les fonctionnalités de récupération fournies par la suppression soft.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-107">Before performing a restore, use the recovery capabilities provided by soft delete.</span></span> <span data-ttu-id="0c1e1-108">Toutes les clés utilisées avec la clé client doivent être activées pour la suppression possible.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-108">All keys that are used with Customer Key are required to have soft delete enabled.</span></span> <span data-ttu-id="0c1e1-109">La suppression souple agit comme une corbeille et permet une récupération pendant 90 jours sans avoir à le restaurer.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-109">Soft delete acts like a recycle bin and allows recovery for up to 90 days without the need to restore.</span></span> <span data-ttu-id="0c1e1-110">La restauration ne doit être nécessaire que dans des circonstances extrêmes ou inhabituelles, par exemple si la clé ou le coffre de clés est perdu.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-110">Restore should only be required in extreme or unusual circumstances, for example if the key or key vault is lost.</span></span> <span data-ttu-id="0c1e1-111">Si vous devez restaurer une clé à utiliser avec la clé client, dans Azure PowerShell, exécutez l'Restore-AzureKeyVaultKey suivante :</span><span class="sxs-lookup"><span data-stu-id="0c1e1-111">If you must restore a key for use with Customer Key, in Azure PowerShell, run the Restore-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```powershell
Restore-AzKeyVaultKey -VaultName <vault name> -InputFile <filename>
```

<span data-ttu-id="0c1e1-112">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="0c1e1-112">For example:</span></span>
  
```powershell
Restore-AzKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

<span data-ttu-id="0c1e1-113">Si le coffre de clés contient déjà une clé du même nom, l’opération de restauration échoue.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-113">If the key vault already contains a key with the same name, the restore operation fails.</span></span> <span data-ttu-id="0c1e1-114">Restore-AzKeyVaultKey restaure toutes les versions clés et toutes les métadonnées de la clé, y compris le nom de la clé.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-114">Restore-AzKeyVaultKey restores all key versions and all metadata for the key including the key name.</span></span>
  
## <a name="manage-key-vault-permissions"></a><span data-ttu-id="0c1e1-115">Gérer les autorisations de coffre de clés</span><span class="sxs-lookup"><span data-stu-id="0c1e1-115">Manage key vault permissions</span></span>

<span data-ttu-id="0c1e1-116">Plusieurs cmdlets sont disponibles qui vous permettent d’afficher et, si nécessaire, de supprimer les autorisations de coffre de clés.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-116">Several cmdlets are available that enable you to view and, if necessary, remove key vault permissions.</span></span> <span data-ttu-id="0c1e1-117">Vous devrez peut-être supprimer des autorisations, par exemple, lorsqu’un employé quitte l’équipe.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-117">You might need to remove permissions, for example, when an employee leaves the team.</span></span> <span data-ttu-id="0c1e1-118">Pour chacune de ces tâches, vous allez utiliser Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-118">For each of these tasks, you will use Azure PowerShell.</span></span> <span data-ttu-id="0c1e1-119">Pour plus d’informations sur Azure Powershell, voir [Vue d’ensemble d’Azure PowerShell.](/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="0c1e1-119">For information about Azure Powershell, see [Overview of Azure PowerShell](/powershell/azure/).</span></span>

<span data-ttu-id="0c1e1-120">Pour afficher les autorisations de coffre de clés, exécutez Get-AzKeyVault cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-120">To view key vault permissions, run the Get-AzKeyVault cmdlet.</span></span>

```powershell
Get-AzKeyVault -VaultName <vault name>
```

<span data-ttu-id="0c1e1-121">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="0c1e1-121">For example:</span></span>

```powershell
Get-AzKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

<span data-ttu-id="0c1e1-122">Pour supprimer les autorisations d’un administrateur, exécutez Remove-AzKeyVaultAccessPolicy cmdlet :</span><span class="sxs-lookup"><span data-stu-id="0c1e1-122">To remove an administrator's permissions, run the Remove-AzKeyVaultAccessPolicy cmdlet:</span></span>
  
```powershell
Remove-AzKeyVaultAccessPolicy -VaultName <vault name> -UserPrincipalName <UPN of user>
```

<span data-ttu-id="0c1e1-123">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="0c1e1-123">For example:</span></span>

```powershell
Remove-AzKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 -UserPrincipalName alice@contoso.com
```

## <a name="manage-data-encryption-policies-deps-with-customer-key"></a><span data-ttu-id="0c1e1-124">Gérer les stratégies de chiffrement de données (DEP) avec la clé client</span><span class="sxs-lookup"><span data-stu-id="0c1e1-124">Manage data encryption policies (DEPs) with Customer Key</span></span>

<span data-ttu-id="0c1e1-125">La clé client gère les ppp différemment entre les différents services.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-125">Customer Key handles DEPs differently between the different services.</span></span> <span data-ttu-id="0c1e1-126">Par exemple, vous pouvez créer un nombre différent de deP pour les différents services.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-126">For example, you can create a different number of DEPs for the different services.</span></span>

<span data-ttu-id="0c1e1-127">**Exchange Online et Skype Entreprise :** Vous pouvez créer jusqu’à 50 DEP.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-127">**Exchange Online and Skype for Business:** You can create up to 50 DEPs.</span></span> <span data-ttu-id="0c1e1-128">Pour obtenir des instructions, voir Créer une stratégie de chiffrement de données à utiliser avec [Exchange Online et Skype Entreprise.](customer-key-set-up.md#create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business)</span><span class="sxs-lookup"><span data-stu-id="0c1e1-128">For instructions, see [Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business](customer-key-set-up.md#create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business).</span></span>

<span data-ttu-id="0c1e1-129">**Fichiers SharePoint Online, OneDrive Entreprise et Teams :** Une PD DEP s’applique aux données dans un emplacement géographique, également appelé _géo_.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-129">**SharePoint Online, OneDrive for Business, and Teams files:** A DEP applies to data in one geographic location, also called a _geo_.</span></span> <span data-ttu-id="0c1e1-130">Si vous utilisez la fonctionnalité multigé géographique d’Office 365, vous pouvez en créer un par géo.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-130">If you use the multi-geo feature of Office 365, you can create one DEP per geo.</span></span> <span data-ttu-id="0c1e1-131">Si vous n’utilisez pas multigéogé, vous pouvez en créer un.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-131">If you are not using multi-geo, you can create one DEP.</span></span> <span data-ttu-id="0c1e1-132">Normalement, vous créez le PD DEP lorsque vous définissez la clé client.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-132">Normally, you create the DEP when you set up Customer Key.</span></span> <span data-ttu-id="0c1e1-133">Pour obtenir des instructions, voir Créer une stratégie de chiffrement de données [(DEP)](customer-key-set-up.md#create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo)pour chaque site géographique SharePoint Online et OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-133">For instructions, see [Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo](customer-key-set-up.md#create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo).</span></span>

### <a name="view-the-deps-youve-created-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="0c1e1-134">Afficher les deps que vous avez créés pour Exchange Online et Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="0c1e1-134">View the DEPs you've created for Exchange Online and Skype for Business</span></span>

<span data-ttu-id="0c1e1-135">Pour afficher la liste de tous les PDP que vous avez créés pour Exchange Online et Skype Entreprise à l’aide de la cmdlet PowerShell Get-DataEncryptionPolicy, complétez ces étapes.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-135">To view a list of all the DEPs you've created for Exchange Online and Skype for Business using the Get-DataEncryptionPolicy PowerShell cmdlet, complete these steps.</span></span>

1. <span data-ttu-id="0c1e1-136">À l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, connectez-vous [à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="0c1e1-136">Using a work or school account that has global administrator permissions in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="0c1e1-137">Pour retourner tous les DDP de votre organisation, exécutez l'Get-DataEncryptionPolicy cmdlet sans aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-137">To return all DEPs in your organization, run the Get-DataEncryptionPolicy cmdlet without any parameters.</span></span>

   ```powershell
   Get-DataEncryptionPolicy
   ```

   <span data-ttu-id="0c1e1-138">Pour plus d’informations sur la cmdlet Get-DataEncryptionPolicy, voir [Get-DataEncryptionPolicy](/powershell/module/exchange/get-dataencryptionpolicy).</span><span class="sxs-lookup"><span data-stu-id="0c1e1-138">For more information about the Get-DataEncryptionPolicy cmdlet, see [Get-DataEncryptionPolicy](/powershell/module/exchange/get-dataencryptionpolicy).</span></span>

### <a name="assign-a-dep-before-you-migrate-a-mailbox-to-the-cloud"></a><span data-ttu-id="0c1e1-139">Affecter un dep avant de migrer une boîte aux lettres vers le cloud</span><span class="sxs-lookup"><span data-stu-id="0c1e1-139">Assign a DEP before you migrate a mailbox to the cloud</span></span>

<span data-ttu-id="0c1e1-140">Lorsque vous affectez le deP, Microsoft 365 chiffre le contenu de la boîte aux lettres à l’aide de la dep affectée lors de la migration.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-140">When you assign the DEP, Microsoft 365 encrypts the contents of the mailbox using the assigned DEP during the migration.</span></span> <span data-ttu-id="0c1e1-141">Ce processus est plus efficace que la migration de la boîte aux lettres, l’affectation du dep, puis l’attente du chiffrement, ce qui peut prendre des heures, voire des jours.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-141">This process is more efficient than migrating the mailbox, assigning the DEP, and then waiting for encryption to take place, which can take hours or possibly days.</span></span>

<span data-ttu-id="0c1e1-142">Pour affecter un dep à une boîte aux lettres avant de la migrer vers Office 365, exécutez la cmdlet Set-MailUser dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="0c1e1-142">To assign a DEP to a mailbox before you migrate it to Office 365, run the Set-MailUser cmdlet in Exchange Online PowerShell:</span></span>

1. <span data-ttu-id="0c1e1-143">À l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, connectez-vous [à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="0c1e1-143">Using a work or school account that has global administrator permissions in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="0c1e1-144">Exécutez lSet-MailUser cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-144">Run the Set-MailUser cmdlet.</span></span>

   ```powershell
   Set-MailUser -Identity <GeneralMailboxOrMailUserIdParameter> -DataEncryptionPolicy <DataEncryptionPolicyIdParameter>
   ```

   <span data-ttu-id="0c1e1-145">Où *GeneralMailboxOrMailUserIdParameter* spécifie une boîte aux lettres et *DataEncryptionPolicyIdParameter* est l’ID du deP.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-145">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox, and *DataEncryptionPolicyIdParameter* is the ID of the DEP.</span></span> <span data-ttu-id="0c1e1-146">Pour plus d’informations sur la cmdlet Set-MailUser, voir [Set-MailUser](/powershell/module/exchange/set-mailuser).</span><span class="sxs-lookup"><span data-stu-id="0c1e1-146">For more information about the Set-MailUser cmdlet, see [Set-MailUser](/powershell/module/exchange/set-mailuser).</span></span>

### <a name="determine-the-dep-assigned-to-a-mailbox"></a><span data-ttu-id="0c1e1-147">Déterminer le deP affecté à une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="0c1e1-147">Determine the DEP assigned to a mailbox</span></span>

<span data-ttu-id="0c1e1-148">Pour déterminer le deP affecté à une boîte aux lettres, utilisez la cmdlet Get-MailboxStatistics de messagerie.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-148">To determine the DEP assigned to a mailbox, use the Get-MailboxStatistics cmdlet.</span></span> <span data-ttu-id="0c1e1-149">La cmdlet renvoie un identificateur unique (GUID).</span><span class="sxs-lookup"><span data-stu-id="0c1e1-149">The cmdlet returns a unique identifier (GUID).</span></span>
  
1. <span data-ttu-id="0c1e1-150">À l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, connectez-vous [à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="0c1e1-150">Using a work or school account that has global administrator permissions in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

   ```powershell
   Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
   ```

   <span data-ttu-id="0c1e1-151">Où *GeneralMailboxOrMailUserIdParameter* spécifie une boîte aux lettres et DataEncryptionPolicyID renvoie le GUID du deP.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-151">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox and DataEncryptionPolicyID returns the GUID of the DEP.</span></span> <span data-ttu-id="0c1e1-152">Pour plus d’informations sur Get-MailboxStatistics cmdlet, [voir Get-MailboxStatistics](/powershell/module/exchange/get-mailboxstatistics).</span><span class="sxs-lookup"><span data-stu-id="0c1e1-152">For more information about the Get-MailboxStatistics cmdlet, see [Get-MailboxStatistics](/powershell/module/exchange/get-mailboxstatistics).</span></span>
  
2. <span data-ttu-id="0c1e1-153">Exécutez Get-DataEncryptionPolicy cmdlet pour connaître le nom convivial du dep auquel la boîte aux lettres est affectée.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-153">Run the Get-DataEncryptionPolicy cmdlet to find out the friendly name of the DEP to which the mailbox is assigned.</span></span>
  
   ```powershell
   Get-DataEncryptionPolicy <GUID>
   ```

   <span data-ttu-id="0c1e1-154">Où *GUID est* le GUID renvoyé par l'Get-MailboxStatistics cmdlet à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-154">Where *GUID* is the GUID returned by the Get-MailboxStatistics cmdlet in the previous step.</span></span>

## <a name="verify-that-customer-key-has-finished-encryption"></a><span data-ttu-id="0c1e1-155">Vérifier que le chiffrement de la clé client est terminé</span><span class="sxs-lookup"><span data-stu-id="0c1e1-155">Verify that Customer Key has finished encryption</span></span>

<span data-ttu-id="0c1e1-156">Que vous venons d’inscrire une clé client, d’attribuer un nouveau dep ou de migrer une boîte aux lettres, utilisez les étapes de cette section pour vous assurer que le chiffrement est terminé.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-156">Whether you've just rolled a Customer Key, assigned a new DEP, or migrated a mailbox, use the steps in this section to ensure that encryption completes.</span></span>

### <a name="verify-encryption-completes-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="0c1e1-157">Vérifier que le chiffrement est terminé pour Exchange Online et Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="0c1e1-157">Verify encryption completes for Exchange Online and Skype for Business</span></span>

<span data-ttu-id="0c1e1-158">Le chiffrement d’une boîte aux lettres peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-158">Encrypting a mailbox can take some time.</span></span> <span data-ttu-id="0c1e1-159">Nous vous recommandons d’attendre 72 heures avant d’essayer de valider le chiffrement après avoir changé de dep ou la première fois que vous affectez un deP à une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-159">We recommend that you wait 72 hours before you attempt to validate encryption after you change a DEP or the first time you assign a DEP to a mailbox.</span></span>
  
<span data-ttu-id="0c1e1-160">Utilisez la cmdlet Get-MailboxStatistics pour déterminer si une boîte aux lettres est chiffrée.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-160">Use the Get-MailboxStatistics cmdlet to determine if a mailbox is encrypted.</span></span>
  
```powershell
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

<span data-ttu-id="0c1e1-161">La propriété IsEncrypted renvoie la valeur **true** si la boîte aux lettres est chiffrée et la valeur **false** si la boîte aux lettres n’est pas chiffrée.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-161">The IsEncrypted property returns a value of **true** if the mailbox is encrypted and a value of **false** if the mailbox is not encrypted.</span></span>

<span data-ttu-id="0c1e1-162">Le temps de déplacement des boîtes aux lettres dépend de la taille de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-162">The time to complete mailbox moves depends on the size of the mailbox.</span></span> <span data-ttu-id="0c1e1-163">Si la clé client n’a pas entièrement chiffré la boîte aux lettres après 72 heures après l’affectation d’un nouveau PED, contactez le support Microsoft pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-163">If Customer Key hasn't completely encrypted the mailbox after 72 hours from the time you assign a new DEP, contact Microsoft support for help.</span></span> <span data-ttu-id="0c1e1-164">La cmdlet New-MoveRequest n’est plus disponible pour les déplacements de boîtes aux lettres locales.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-164">The New-MoveRequest cmdlet is no longer available for local mailbox moves.</span></span> <span data-ttu-id="0c1e1-165">Pour plus [d’informations,](https://techcommunity.microsoft.com/t5/exchange-team-blog/disabling-new-moverequest-for-local-mailbox-moves/bc-p/1332141) reportez-vous à cette annonce.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-165">Refer to [this announcement](https://techcommunity.microsoft.com/t5/exchange-team-blog/disabling-new-moverequest-for-local-mailbox-moves/bc-p/1332141) for additional information.</span></span>

### <a name="verify-encryption-completes-for-sharepoint-online-onedrive-for-business-and-teams-files"></a><span data-ttu-id="0c1e1-166">Vérifier que le chiffrement est terminé pour les fichiers SharePoint Online, OneDrive Entreprise et Teams</span><span class="sxs-lookup"><span data-stu-id="0c1e1-166">Verify encryption completes for SharePoint Online, OneDrive for Business, and Teams files</span></span>

<span data-ttu-id="0c1e1-167">Vérifiez l’état du chiffrement en exécutant la cmdlet Get-SPODataEncryptionPolicy comme suit :</span><span class="sxs-lookup"><span data-stu-id="0c1e1-167">Check on the status of encryption by running the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>

```powershell
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

<span data-ttu-id="0c1e1-168">Le résultat de cette cmdlet inclut :</span><span class="sxs-lookup"><span data-stu-id="0c1e1-168">The output from this cmdlet includes:</span></span>
  
- <span data-ttu-id="0c1e1-169">URI de la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-169">The URI of the primary key.</span></span>

- <span data-ttu-id="0c1e1-170">URI de la clé secondaire.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-170">The URI of the secondary key.</span></span>

- <span data-ttu-id="0c1e1-171">État du chiffrement pour la géo.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-171">The encryption status for the geo.</span></span> <span data-ttu-id="0c1e1-172">Les états possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="0c1e1-172">Possible states include:</span></span>

  - <span data-ttu-id="0c1e1-173">**Non enregistré :** Le chiffrement de clé client n’a pas encore été appliqué.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-173">**Unregistered:** Customer Key encryption has not yet been applied.</span></span>

  - <span data-ttu-id="0c1e1-174">**Inscription :** Le chiffrement de la clé client a été appliqué et vos fichiers sont en cours de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-174">**Registering:** Customer Key encryption has been applied and your files are in the process of being encrypted.</span></span> <span data-ttu-id="0c1e1-175">Si la clé de la géo est inscrite, des informations sur le pourcentage de sites de la géo sont également affichées, ce qui vous permet de surveiller la progression du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-175">If the key for the geo is registering, you'll also be shown information on what percentage of sites in the geo are complete so that you can monitor encryption progress.</span></span>

  - <span data-ttu-id="0c1e1-176">**Inscrit :** Le chiffrement de la clé client a été appliqué et tous les fichiers de tous les sites ont été chiffrés.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-176">**Registered:** Customer Key encryption has been applied, and all files in all sites have been encrypted.</span></span>

  - <span data-ttu-id="0c1e1-177">**Déploiement :** Un roulis de touches est en cours.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-177">**Rolling:** A key roll is in progress.</span></span> <span data-ttu-id="0c1e1-178">Si la clé de la géo est en cours de déploiement, vous verrez également des informations sur le pourcentage de sites qui ont terminé l’opération de déploiement de clé afin de pouvoir surveiller la progression.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-178">If the key for the geo is rolling, you'll also be shown information on what percentage of sites have completed the key roll operation so that you can monitor progress.</span></span>

## <a name="unassign-a-dep-from-a-mailbox"></a><span data-ttu-id="0c1e1-179">Désattribuer un deP d’une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="0c1e1-179">Unassign a DEP from a mailbox</span></span>

<span data-ttu-id="0c1e1-180">Vous désattribuez un deP d’une boîte aux lettres à l’aide de la cmdlet Set-mailbox PowerShell et définissez le `DataEncryptionPolicy` paramètre sur `$NULL` .</span><span class="sxs-lookup"><span data-stu-id="0c1e1-180">You unassign a DEP from a mailbox using the Set-mailbox PowerShell cmdlet and setting the `DataEncryptionPolicy` to `$NULL`.</span></span> <span data-ttu-id="0c1e1-181">L’exécution de cette cmdlet désattribue le dep actuellement affecté et recrypte la boîte aux lettres à l’aide de la dep associée aux clés gérées par défaut de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-181">Running this cmdlet unassigns the currently assigned DEP and reencrypts the mailbox using the DEP associated with default Microsoft managed keys.</span></span> <span data-ttu-id="0c1e1-182">Vous ne pouvez pas désattribuer le deP utilisé par les clés gérées microsoft.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-182">You can't unassign the DEP used by Microsoft managed keys.</span></span> <span data-ttu-id="0c1e1-183">Si vous ne souhaitez pas utiliser de clés gérées par Microsoft, vous pouvez affecter un autre deP à la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-183">If you don't want to use Microsoft managed keys, you can assign another DEP to the mailbox.</span></span>

<span data-ttu-id="0c1e1-184">Pour désattribuer le dep d’une boîte aux lettres à l'Set-Mailbox cmdlet PowerShell, complétez ces étapes.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-184">To unassign the DEP from a mailbox using the Set-Mailbox PowerShell cmdlet, complete these steps.</span></span>

1. <span data-ttu-id="0c1e1-185">À l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, connectez-vous [à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="0c1e1-185">Using a work or school account that has global administrator permissions in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="0c1e1-186">Exécutez lSet-Mailbox cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-186">Run the Set-Mailbox cmdlet.</span></span>

   ```powershell
   Set-Mailbox -Identity <mailbox> -DataEncryptionPolicy $NULL
   ```

## <a name="revoke-your-keys-and-start-the-data-purge-path-process"></a><span data-ttu-id="0c1e1-187">Révoquer vos clés et démarrer le processus de purge des données</span><span class="sxs-lookup"><span data-stu-id="0c1e1-187">Revoke your keys and start the data purge path process</span></span>

<span data-ttu-id="0c1e1-188">Vous contrôlez la révocation de toutes les clés racine, y compris la clé de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-188">You control the revocation of all root keys including the availability key.</span></span> <span data-ttu-id="0c1e1-189">La clé client vous permet de contrôler l’aspect de planification de sortie des exigences réglementaires.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-189">Customer Key provides control of the exit planning aspect of the regulatory requirements for you.</span></span> <span data-ttu-id="0c1e1-190">Si vous décidez de révoquer vos clés pour vider vos données et quitter le service, le service supprime la clé de disponibilité une fois le processus de purge des données terminé.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-190">If you decide to revoke your keys to purge your data and exit the service, the service deletes the availability key once the data purge process completes.</span></span>

<span data-ttu-id="0c1e1-191">Microsoft 365 audite et valide le chemin de purge des données.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-191">Microsoft 365 audits and validates the data purge path.</span></span> <span data-ttu-id="0c1e1-192">Pour plus d’informations, voir le rapport SSAE 18 SOC 2 disponible sur le portail [d’confiance des services.](https://servicetrust.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="0c1e1-192">For more information, see the SSAE 18 SOC 2 Report available on the [Service Trust Portal](https://servicetrust.microsoft.com/).</span></span> <span data-ttu-id="0c1e1-193">En outre, Microsoft recommande les documents suivants :</span><span class="sxs-lookup"><span data-stu-id="0c1e1-193">In addition, Microsoft recommends the following documents:</span></span>

- [<span data-ttu-id="0c1e1-194">Guide d’évaluation et de conformité des risques pour les institutions financières dans microsoft cloud</span><span class="sxs-lookup"><span data-stu-id="0c1e1-194">Risk Assessment and Compliance Guide for Financial Institutions in the Microsoft Cloud</span></span>](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

- [<span data-ttu-id="0c1e1-195">Considérations sur la planification de sortie d’O365</span><span class="sxs-lookup"><span data-stu-id="0c1e1-195">O365 Exit Planning Considerations</span></span>](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=77ea7ebf-ce1b-4a5f-9972-d2d81a951d99&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

<span data-ttu-id="0c1e1-196">Le chemin d’accès de la purge des données diffère légèrement entre les différents services.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-196">The data purge path differs slightly between the different services.</span></span>

### <a name="revoke-your-customer-keys-and-the-availability-key-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="0c1e1-197">Révoquer vos clés client et la clé de disponibilité pour Exchange Online et Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="0c1e1-197">Revoke your Customer Keys and the availability key for Exchange Online and Skype for Business</span></span>

<span data-ttu-id="0c1e1-198">Lorsque vous lancez le chemin d’accès de purge des données pour Exchange Online et Skype Entreprise, vous définissez une demande de purge permanente des données sur un deP.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-198">When you initiate the data purge path for Exchange Online and Skype for Business, you set a permanent data purge request on a DEP.</span></span> <span data-ttu-id="0c1e1-199">Cela supprime définitivement les données chiffrées dans les boîtes aux lettres à laquelle ce dep est affecté.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-199">Doing so permanently deletes encrypted data within the mailboxes to which that DEP is assigned.</span></span>

<span data-ttu-id="0c1e1-200">Étant donné que vous ne pouvez exécuter l’cmdlet PowerShell que sur une seule dep à la fois, envisagez de réaffecter une seule dep à toutes vos boîtes aux lettres avant de lancer le chemin de purge des données.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-200">Since you can only run the PowerShell cmdlet against one DEP at a time, consider reassigning a single DEP to all of your mailboxes before you initiate the data purge path.</span></span>

> [!WARNING]
> <span data-ttu-id="0c1e1-201">N’utilisez pas le chemin de purge des données pour supprimer un sous-ensemble de vos boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-201">Do not use the data purge path to delete a subset of your mailboxes.</span></span> <span data-ttu-id="0c1e1-202">Ce processus est destiné uniquement aux clients qui quittent le service.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-202">This process is only intended for customers who are exiting the service.</span></span>

<span data-ttu-id="0c1e1-203">Pour lancer le chemin d’accès de la purge des données, effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0c1e1-203">To initiate the data purge path, complete these steps:</span></span>

1. <span data-ttu-id="0c1e1-204">Supprimez les autorisations wrap et unwrap pour « O365 Exchange Online » des coffres de clés Azure.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-204">Remove wrap and unwrap permissions for "O365 Exchange Online" from Azure Key Vaults.</span></span>

2. <span data-ttu-id="0c1e1-205">À l’aide d’un compte professionnel ou scolaire qui dispose de privilèges d’administrateur général dans votre organisation, connectez-vous [à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="0c1e1-205">Using a work or school account that has global administrator privileges in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

3. <span data-ttu-id="0c1e1-206">Pour chaque PDE qui contient des boîtes aux lettres à supprimer, exécutez la cmdlet [Set-DataEncryptionPolicy](/powershell/module/exchange/set-dataencryptionpolicy) comme suit.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-206">For each DEP that contains mailboxes that you want to delete, run the [Set-DataEncryptionPolicy](/powershell/module/exchange/set-dataencryptionpolicy) cmdlet as follows.</span></span>

    ```powershell
    Set-DataEncryptionPolicy <Policy ID> -PermanentDataPurgeRequested -PermanentDataPurgeReason <Reason> -PermanentDataPurgeContact <ContactName>
    ```

   <span data-ttu-id="0c1e1-207">Si la commande échoue, assurez-vous que vous avez supprimé les autorisations Exchange Online des deux clés dans Azure Key Vault, comme indiqué précédemment dans cette tâche.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-207">If the command fails, ensure that you've removed the Exchange Online permissions from both keys in Azure Key Vault as specified earlier in this task.</span></span><span data-ttu-id="0c1e1-208">Une fois que vous avez définie le commutateur PermanentDataPurgeRequested à l’aide de la cmdlet Set-DataEncryptionPolicy, vous ne pourrez plus affecter ce deP aux boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-208"> Once you've set the PermanentDataPurgeRequested switch using the Set-DataEncryptionPolicy cmdlet, you'll no longer be able to assign this DEP to mailboxes.</span></span>

4. <span data-ttu-id="0c1e1-209">Contactez le support Microsoft et demandez l’eDocument de purge des données.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-209">Contact Microsoft support and request the Data Purge eDocument.</span></span>

    <span data-ttu-id="0c1e1-210">À votre demande, Microsoft vous envoie un document juridique pour accusé de réception et autoriser la suppression des données.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-210">At your request, Microsoft sends you a legal document to acknowledge and authorize data deletion.</span></span> <span data-ttu-id="0c1e1-211">La personne de votre organisation qui s’est inscrite en tant qu’approuveur dans l’offre FastTrack lors de l’intégration doit signer ce document.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-211">The person in your organization who signed up as an approver in the FastTrack offer during onboarding needs to sign this document.</span></span> <span data-ttu-id="0c1e1-212">Normalement, il s’agit d’un cadre supérieur ou d’une autre personne désignée de votre entreprise qui est légalement autorisé à signer les formalités au nom de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-212">Normally, this is an executive or other designated person in your company who is legally authorized to sign the paperwork on behalf of your organization.</span></span>

5. <span data-ttu-id="0c1e1-213">Une fois que votre représentant a signé le document juridique, renvoyez-le à Microsoft (généralement via une signature eDoc).</span><span class="sxs-lookup"><span data-stu-id="0c1e1-213">Once your representative has signed the legal document, return it to Microsoft (usually through an eDoc signature).</span></span>

    <span data-ttu-id="0c1e1-214">Une fois que Microsoft a reçu le document juridique, Microsoft exécute des cmdlets pour déclencher la purge des données qui supprime d’abord la stratégie, marque les boîtes aux lettres pour suppression définitive, puis supprime la clé de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-214">Once Microsoft receives the legal document, Microsoft runs cmdlets to trigger the data purge which first deletes the policy, marks the mailboxes for permanent deletion, then deletes the availability key.</span></span> <span data-ttu-id="0c1e1-215">Une fois le processus de purge des données terminé, les données ont été purgées, sont inaccessibles à Exchange Online et ne sont pas récupérables.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-215">Once the data purge process completes, the data has been purged, is inaccessible to Exchange Online, and is not recoverable.</span></span>

### <a name="revoke-your-customer-keys-and-the-availability-key-for-sharepoint-online-onedrive-for-business-and-teams-files"></a><span data-ttu-id="0c1e1-216">Révoquer vos clés client et la clé de disponibilité pour les fichiers SharePoint Online, OneDrive Entreprise et Teams</span><span class="sxs-lookup"><span data-stu-id="0c1e1-216">Revoke your Customer Keys and the availability key for SharePoint Online, OneDrive for Business, and Teams files</span></span>

<span data-ttu-id="0c1e1-217">Pour lancer le chemin d’accès de purge des données pour les fichiers SharePoint Online, OneDrive Entreprise et Teams, effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0c1e1-217">To initiate the data purge path for SharePoint Online, OneDrive for Business, and Teams files, complete these steps:</span></span>

1. <span data-ttu-id="0c1e1-218">Révoquer l’accès à Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-218">Revoke Azure Key Vault access.</span></span> <span data-ttu-id="0c1e1-219">Tous les administrateurs de coffre de clés doivent accepter de révoquer l’accès.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-219">All key vault admins must agree to revoke access.</span></span>

   <span data-ttu-id="0c1e1-220">Vous ne supprimez pas le coffre de clés Azure pour SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-220">You do not delete the Azure Key Vault for SharePoint Online.</span></span> <span data-ttu-id="0c1e1-221">Les coffres de clés peuvent être partagés entre plusieurs locataires et deps SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-221">Key vaults may be shared among several SharePoint Online tenants and DEPs.</span></span>

2. <span data-ttu-id="0c1e1-222">Contactez Microsoft pour supprimer la clé de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-222">Contact Microsoft to delete the availability key.</span></span>

    <span data-ttu-id="0c1e1-223">Lorsque vous contactez Microsoft pour supprimer la clé de disponibilité, nous vous envoyons un document juridique.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-223">When you contact Microsoft to delete the availability key, we'll send you a legal document.</span></span> <span data-ttu-id="0c1e1-224">La personne de votre organisation qui s’est inscrite en tant qu’approuveur dans l’offre FastTrack lors de l’intégration doit signer ce document.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-224">The person in your organization who signed up as an approver in the FastTrack offer during onboarding needs to sign this document.</span></span> <span data-ttu-id="0c1e1-225">Normalement, il s’agit d’un cadre supérieur ou d’une autre personne désignée de votre entreprise qui est légalement autorisée à signer les formalités au nom de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-225">Normally, this is an executive or other designated person in your company who's legally authorized to sign the paperwork on behalf of your organization.</span></span>

3. <span data-ttu-id="0c1e1-226">Une fois que votre représentant signe le document juridique, renvoyez-le à Microsoft (généralement par le biais d’une signature eDoc).</span><span class="sxs-lookup"><span data-stu-id="0c1e1-226">Once your representative signs the legal document, return it to Microsoft (usually through an eDoc signature).</span></span>

   <span data-ttu-id="0c1e1-227">Une fois que Microsoft a reçu le document juridique, nous exécuterons des cmdlets pour déclencher la purge des données qui effectue la suppression de chiffrement de la clé de client, de la clé de site et de toutes les clés de document individuelles, ce qui a pour effet de rompre irrévocablement la hiérarchie des clés.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-227">Once Microsoft receives the legal document, we run cmdlets to trigger the data purge which performs crypto deletion of the tenant key, site key, and all individual per-document keys, irrevocably breaking the key hierarchy.</span></span> <span data-ttu-id="0c1e1-228">Une fois les cmdlets de purge des données terminées, vos données ont été purgées.</span><span class="sxs-lookup"><span data-stu-id="0c1e1-228">Once the data purge cmdlets complete, your data has been purged.</span></span>

## <a name="related-articles"></a><span data-ttu-id="0c1e1-229">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="0c1e1-229">Related articles</span></span>

- [<span data-ttu-id="0c1e1-230">Chiffrement du service avec la clé client</span><span class="sxs-lookup"><span data-stu-id="0c1e1-230">Service encryption with Customer Key</span></span>](customer-key-overview.md)

- [<span data-ttu-id="0c1e1-231">En savoir plus sur la clé de disponibilité</span><span class="sxs-lookup"><span data-stu-id="0c1e1-231">Learn about the availability key</span></span>](customer-key-availability-key-understand.md)

- [<span data-ttu-id="0c1e1-232">Configurer la clé client</span><span class="sxs-lookup"><span data-stu-id="0c1e1-232">Set up Customer Key</span></span>](customer-key-set-up.md)

- [<span data-ttu-id="0c1e1-233">Echanger ou alterner entre une clé client ou de disponibilité</span><span class="sxs-lookup"><span data-stu-id="0c1e1-233">Roll or rotate a Customer Key or an availability key</span></span>](customer-key-availability-key-roll.md)

- [<span data-ttu-id="0c1e1-234">Référentiel sécurisé client</span><span class="sxs-lookup"><span data-stu-id="0c1e1-234">Customer Lockbox</span></span>](customer-lockbox-requests.md)

- [<span data-ttu-id="0c1e1-235">Chiffrement de service</span><span class="sxs-lookup"><span data-stu-id="0c1e1-235">Service Encryption</span></span>](office-365-service-encryption.md)