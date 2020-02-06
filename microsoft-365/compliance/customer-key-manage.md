---
title: Gérer la clé client pour Office 365
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
description: Après avoir configuré la clé client, Découvrez comment la gérer en restaurant les clés AKV et en gérant les autorisations et vos stratégies de chiffrement de données.
ms.openlocfilehash: 112bdee7658334c251418903761866841625ff17
ms.sourcegitcommit: 5ff1dc62e8855be155cb2de45cf4ee5a02c321fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2020
ms.locfileid: "41804786"
---
# <a name="manage-customer-key-for-office-365"></a><span data-ttu-id="31c75-103">Gérer la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="31c75-103">Manage Customer Key for Office 365</span></span>

<span data-ttu-id="31c75-104">Une fois que vous avez configuré la clé client pour Office 365, vous pouvez gérer vos clés comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="31c75-104">After you've set up Customer Key for Office 365, you can manage your keys as described in this article.</span></span> <span data-ttu-id="31c75-105">Pour plus d’informations sur la clé client, consultez les rubriques connexes.</span><span class="sxs-lookup"><span data-stu-id="31c75-105">Learn more about Customer Key in the related topics.</span></span>

## <a name="restore-azure-key-vault-keys"></a><span data-ttu-id="31c75-106">Restaurer les clés Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="31c75-106">Restore Azure Key Vault keys</span></span>

<span data-ttu-id="31c75-107">Avant d’effectuer une restauration, utilisez les fonctionnalités de récupération fournies par la fonction de suppression récupérable.</span><span class="sxs-lookup"><span data-stu-id="31c75-107">Before performing a restore, use the recovery capabilities provided by soft delete.</span></span> <span data-ttu-id="31c75-108">Toutes les clés utilisées avec la clé client doivent être activées pour la suppression logicielle.</span><span class="sxs-lookup"><span data-stu-id="31c75-108">All keys that are used with Customer Key are required to have soft delete enabled.</span></span> <span data-ttu-id="31c75-109">La suppression douce se comporte comme une corbeille et permet la récupération jusqu’à 90 jours sans nécessiter de restauration.</span><span class="sxs-lookup"><span data-stu-id="31c75-109">Soft delete acts like a recycle bin and allows recovery for up to 90 days without the need to restore.</span></span> <span data-ttu-id="31c75-110">La restauration doit être uniquement requise dans des circonstances extrêmes ou inhabituelles, par exemple en cas de perte de la clé ou du coffre-fort.</span><span class="sxs-lookup"><span data-stu-id="31c75-110">Restore should only be required in extreme or unusual circumstances, for example if the key or key vault is lost.</span></span> <span data-ttu-id="31c75-111">Si vous devez restaurer une clé à utiliser avec la clé client, dans Azure PowerShell, exécutez la cmdlet Restore-AzureKeyVaultKey comme suit :</span><span class="sxs-lookup"><span data-stu-id="31c75-111">If you must restore a key for use with Customer Key, in Azure PowerShell, run the Restore-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```powershell
Restore-AzKeyVaultKey -VaultName <vault name> -InputFile <filename>
```

<span data-ttu-id="31c75-112">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="31c75-112">For example:</span></span>
  
```powershell
Restore-AzKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

<span data-ttu-id="31c75-113">Si le coffre-fort de clés contient déjà une clé portant le même nom, l’opération de restauration échoue.</span><span class="sxs-lookup"><span data-stu-id="31c75-113">If the key vault already contains a key with the same name, the restore operation fails.</span></span> <span data-ttu-id="31c75-114">Restore-AzKeyVaultKey restaure toutes les versions clés et toutes les métadonnées pour la clé, y compris le nom de la clé.</span><span class="sxs-lookup"><span data-stu-id="31c75-114">Restore-AzKeyVaultKey restores all key versions and all metadata for the key including the key name.</span></span>
  
## <a name="manage-key-vault-permissions"></a><span data-ttu-id="31c75-115">Gérer les autorisations de coffre-fort</span><span class="sxs-lookup"><span data-stu-id="31c75-115">Manage key vault permissions</span></span>

<span data-ttu-id="31c75-116">Plusieurs cmdlets sont disponibles, qui vous permettent d’afficher et, si nécessaire, de supprimer des autorisations de coffre-fort clé.</span><span class="sxs-lookup"><span data-stu-id="31c75-116">Several cmdlets are available that enable you to view and, if necessary, remove key vault permissions.</span></span> <span data-ttu-id="31c75-117">Vous devrez peut-être supprimer des autorisations, par exemple, lorsqu’un employé quitte l’équipe.</span><span class="sxs-lookup"><span data-stu-id="31c75-117">You might need to remove permissions, for example, when an employee leaves the team.</span></span> <span data-ttu-id="31c75-118">Pour chacune de ces tâches, vous allez utiliser Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="31c75-118">For each of these tasks, you will use Azure PowerShell.</span></span> <span data-ttu-id="31c75-119">Pour plus d’informations sur Azure PowerShell, consultez la rubrique [Overview of Azure PowerShell](https://docs.microsoft.com/powershell/azure/).</span><span class="sxs-lookup"><span data-stu-id="31c75-119">For information about Azure Powershell, see [Overview of Azure PowerShell](https://docs.microsoft.com/powershell/azure/).</span></span>

<span data-ttu-id="31c75-120">Pour afficher les autorisations de coffre-fort, exécutez la cmdlet Get-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="31c75-120">To view key vault permissions, run the Get-AzKeyVault cmdlet.</span></span>

```powershell
Get-AzKeyVault -VaultName <vault name>
```

<span data-ttu-id="31c75-121">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="31c75-121">For example:</span></span>

```powershell
Get-AzKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

<span data-ttu-id="31c75-122">Pour supprimer les autorisations d’un administrateur, exécutez l’applet de commande Remove-AzKeyVaultAccessPolicy :</span><span class="sxs-lookup"><span data-stu-id="31c75-122">To remove an administrator's permissions, run the Remove-AzKeyVaultAccessPolicy cmdlet:</span></span>
  
```powershell
Remove-AzKeyVaultAccessPolicy -VaultName <vault name> -UserPrincipalName <UPN of user>
```

<span data-ttu-id="31c75-123">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="31c75-123">For example:</span></span>

```powershell
Remove-AzKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 -UserPrincipalName alice@contoso.com
```

## <a name="manage-data-encryption-policies-deps-with-customer-key"></a><span data-ttu-id="31c75-124">Gérer les stratégies de chiffrement de données (DEPs) avec la clé client</span><span class="sxs-lookup"><span data-stu-id="31c75-124">Manage data encryption policies (DEPs) with Customer Key</span></span>

<span data-ttu-id="31c75-125">Les handles de clé du client DEPs différemment entre les différents services Office 365.</span><span class="sxs-lookup"><span data-stu-id="31c75-125">Customer Key handles DEPs differently between the different Office 365 services.</span></span> <span data-ttu-id="31c75-126">Par exemple, vous pouvez créer un nombre différent de DEPs pour les différents services.</span><span class="sxs-lookup"><span data-stu-id="31c75-126">For example, you can create a different number of DEPs for the different services.</span></span>

<span data-ttu-id="31c75-127">**Exchange Online et Skype entreprise :** Vous pouvez créer jusqu’à 50 DEPs.</span><span class="sxs-lookup"><span data-stu-id="31c75-127">**Exchange Online and Skype for Business:** You can create up to 50 DEPs.</span></span> <span data-ttu-id="31c75-128">Pour obtenir des instructions, voir [Create a Data Encryption Policy (DEP) for use with Exchange Online and Skype for Business](customer-key-set-up.md#create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business).</span><span class="sxs-lookup"><span data-stu-id="31c75-128">For instructions, see [Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business](customer-key-set-up.md#create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business).</span></span>

<span data-ttu-id="31c75-129">**SharePoint Online, OneDrive entreprise et fichiers teams :** Une DEP s’applique aux données d’un emplacement géographique, également appelé _géo_.</span><span class="sxs-lookup"><span data-stu-id="31c75-129">**SharePoint Online, OneDrive for Business, and Teams files:** A DEP applies to data in one geographic location, also called a _geo_.</span></span> <span data-ttu-id="31c75-130">Si vous utilisez la fonctionnalité multigéographique d’Office 365, vous pouvez créer une DEP par zone géographique.</span><span class="sxs-lookup"><span data-stu-id="31c75-130">If you use the multi-geo feature of Office 365, you can create one DEP per geo.</span></span> <span data-ttu-id="31c75-131">Si vous n’utilisez pas de multi-géo, vous pouvez créer une DEP.</span><span class="sxs-lookup"><span data-stu-id="31c75-131">If you are not using multi-geo, you can create one DEP.</span></span> <span data-ttu-id="31c75-132">Normalement, vous créez la DEP lorsque vous configurez la clé client.</span><span class="sxs-lookup"><span data-stu-id="31c75-132">Normally, you create the DEP when you set up Customer Key.</span></span> <span data-ttu-id="31c75-133">Pour obtenir des instructions, consultez [la rubrique créer une stratégie de chiffrement de données (DEP) pour chaque zone géographique SharePoint Online et OneDrive entreprise](customer-key-set-up.md#create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo).</span><span class="sxs-lookup"><span data-stu-id="31c75-133">For instructions, see [Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo](customer-key-set-up.md#create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo).</span></span>

### <a name="view-the-deps-youve-created-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="31c75-134">Afficher le DEPs que vous avez créé pour Exchange Online et Skype entreprise</span><span class="sxs-lookup"><span data-stu-id="31c75-134">View the DEPs you've created for Exchange Online and Skype for Business</span></span>

<span data-ttu-id="31c75-135">Pour afficher la liste de tous les DEPs que vous avez créés pour Exchange Online et Skype entreprise à l’aide de l’applet de commande Get-DataEncryptionPolicy PowerShell, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="31c75-135">To view a list of all the DEPs you've created for Exchange Online and Skype for Business using the Get-DataEncryptionPolicy PowerShell cmdlet, complete these steps.</span></span>

1. <span data-ttu-id="31c75-136">À l’aide d’un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365, [Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="31c75-136">Using a work or school account that has global administrator permissions in your Office 365 organization, [connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>

2. <span data-ttu-id="31c75-137">Pour renvoyer tous les DEPs de votre organisation, exécutez la cmdlet Get-DataEncryptionPolicy sans aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="31c75-137">To return all DEPs in your organization, run the Get-DataEncryptionPolicy cmdlet without any parameters.</span></span>

  ```powershell
  Get-DataEncryptionPolicy
  ```

  <span data-ttu-id="31c75-138">Pour plus d’informations sur la cmdlet Get-DataEncryptionPolicy, consultez la rubrique [Get-DataEncryptionPolicy](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/get-dataencryptionpolicy?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="31c75-138">For more information about the Get-DataEncryptionPolicy cmdlet, see [Get-DataEncryptionPolicy](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/get-dataencryptionpolicy?view=exchange-ps).</span></span>

### <a name="assign-a-dep-before-you-migrate-a-mailbox-to-the-cloud"></a><span data-ttu-id="31c75-139">Affectation d’une DEP avant la migration d’une boîte aux lettres vers le Cloud</span><span class="sxs-lookup"><span data-stu-id="31c75-139">Assign a DEP before you migrate a mailbox to the cloud</span></span>

<span data-ttu-id="31c75-140">Lorsque vous affectez la DEP, Office 365 chiffre le contenu de la boîte aux lettres à l’aide de la DEP attribuée lors de la migration.</span><span class="sxs-lookup"><span data-stu-id="31c75-140">When you assign the DEP, Office 365 encrypts the contents of the mailbox using the assigned DEP during the migration.</span></span> <span data-ttu-id="31c75-141">Ce processus est plus efficace que la migration de la boîte aux lettres, l’affectation de la DEP, puis l’attente du chiffrement, ce qui peut prendre des heures voire des jours.</span><span class="sxs-lookup"><span data-stu-id="31c75-141">This process is more efficient than migrating the mailbox, assigning the DEP, and then waiting for encryption to take place, which can take hours or possibly days.</span></span>

<span data-ttu-id="31c75-142">Pour affecter une DEP à une boîte aux lettres avant de la migrer vers Office 365, exécutez la cmdlet Set-MailUser dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="31c75-142">To assign a DEP to a mailbox before you migrate it to Office 365, run the Set-MailUser cmdlet in Exchange Online PowerShell:</span></span>

1. <span data-ttu-id="31c75-143">À l’aide d’un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365, [Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="31c75-143">Using a work or school account that has global administrator permissions in your Office 365 organization, [connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>

2. <span data-ttu-id="31c75-144">Exécutez la cmdlet Set-MailUser.</span><span class="sxs-lookup"><span data-stu-id="31c75-144">Run the Set-MailUser cmdlet.</span></span>

  ```powershell
  Set-MailUser -Identity <GeneralMailboxOrMailUserIdParameter> -DataEncryptionPolicy <DataEncryptionPolicyIdParameter>
  ```

  <span data-ttu-id="31c75-145">Où *GeneralMailboxOrMailUserIdParameter* spécifie une boîte aux lettres et *DATAENCRYPTIONPOLICYIDPARAMETER* est l’ID de la DEP.</span><span class="sxs-lookup"><span data-stu-id="31c75-145">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox, and *DataEncryptionPolicyIdParameter* is the ID of the DEP.</span></span> <span data-ttu-id="31c75-146">Pour plus d’informations sur la cmdlet Set-MailUser, voir [Set-MailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/set-mailuser?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="31c75-146">For more information about the Set-MailUser cmdlet, see [Set-MailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/set-mailuser?view=exchange-ps).</span></span>

### <a name="determine-the-dep-assigned-to-a-mailbox"></a><span data-ttu-id="31c75-147">Déterminer la DEP affectée à une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="31c75-147">Determine the DEP assigned to a mailbox</span></span>

<span data-ttu-id="31c75-148">Pour déterminer la DEP affectée à une boîte aux lettres, utilisez la cmdlet Get-MailboxStatistics.</span><span class="sxs-lookup"><span data-stu-id="31c75-148">To determine the DEP assigned to a mailbox, use the Get-MailboxStatistics cmdlet.</span></span> <span data-ttu-id="31c75-149">L’applet de commande renvoie un identificateur unique (GUID).</span><span class="sxs-lookup"><span data-stu-id="31c75-149">The cmdlet returns a unique identifier (GUID).</span></span>
  
1. <span data-ttu-id="31c75-150">À l’aide d’un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365, [Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="31c75-150">Using a work or school account that has global administrator permissions in your Office 365 organization, [connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>

   ```powershell
   Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
   ```

   <span data-ttu-id="31c75-151">Où *GeneralMailboxOrMailUserIdParameter* spécifie une boîte aux lettres et DataEncryptionPolicyID renvoie le GUID de la DEP.</span><span class="sxs-lookup"><span data-stu-id="31c75-151">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox and DataEncryptionPolicyID returns the GUID of the DEP.</span></span> <span data-ttu-id="31c75-152">Pour plus d’informations sur la cmdlet Get-MailboxStatistics, consultez la rubrique [Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/get-mailboxstatistics?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="31c75-152">For more information about the Get-MailboxStatistics cmdlet, see [Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/get-mailboxstatistics?view=exchange-ps).</span></span>
  
2. <span data-ttu-id="31c75-153">Exécutez la cmdlet Get-DataEncryptionPolicy pour connaître le nom convivial de la DEP à laquelle la boîte aux lettres est affectée.</span><span class="sxs-lookup"><span data-stu-id="31c75-153">Run the Get-DataEncryptionPolicy cmdlet to find out the friendly name of the DEP to which the mailbox is assigned.</span></span>
  
   ```powershell
   Get-DataEncryptionPolicy <GUID>
   ```

   <span data-ttu-id="31c75-154">Où *GUID* est le GUID renvoyé par la cmdlet Get-MailboxStatistics à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="31c75-154">Where *GUID* is the GUID returned by the Get-MailboxStatistics cmdlet in the previous step.</span></span>

## <a name="verify-that-customer-key-has-finished-encryption"></a><span data-ttu-id="31c75-155">Vérifier que la clé client a terminé le chiffrement</span><span class="sxs-lookup"><span data-stu-id="31c75-155">Verify that Customer Key has finished encryption</span></span>

<span data-ttu-id="31c75-156">Qu’il s’agisse d’une clé client, d’une nouvelle DEP ou d’une migration de boîte aux lettres, utilisez les étapes de cette section pour vous assurer que le chiffrement est terminé.</span><span class="sxs-lookup"><span data-stu-id="31c75-156">Whether you've just rolled a Customer Key, assigned a new DEP, or migrated a mailbox, use the steps in this section to ensure that encryption completes.</span></span>

### <a name="verify-encryption-completes-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="31c75-157">Vérifier que le chiffrement est terminé pour Exchange Online et Skype entreprise</span><span class="sxs-lookup"><span data-stu-id="31c75-157">Verify encryption completes for Exchange Online and Skype for Business</span></span>

<span data-ttu-id="31c75-158">Le chiffrement d’une boîte aux lettres peut prendre du temps.</span><span class="sxs-lookup"><span data-stu-id="31c75-158">Encrypting a mailbox can take some time.</span></span> <span data-ttu-id="31c75-159">Nous vous recommandons d’attendre 72 heures avant de valider le chiffrement après avoir modifié une DEP ou la première fois que vous affectez une DEP à une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="31c75-159">We recommend that you wait 72 hours before you attempt to validate encryption after you change a DEP or the first time you assign a DEP to a mailbox.</span></span>
  
<span data-ttu-id="31c75-160">Utilisez la cmdlet Get-MailboxStatistics pour déterminer si une boîte aux lettres est chiffrée.</span><span class="sxs-lookup"><span data-stu-id="31c75-160">Use the Get-MailboxStatistics cmdlet to determine if a mailbox is encrypted.</span></span>
  
```powershell
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

<span data-ttu-id="31c75-161">La propriété IsEncrypted renvoie la valeur **true** si la boîte aux lettres est chiffrée et la valeur **false** si la boîte aux lettres n’est pas chiffrée.</span><span class="sxs-lookup"><span data-stu-id="31c75-161">The IsEncrypted property returns a value of **true** if the mailbox is encrypted and a value of **false** if the mailbox is not encrypted.</span></span>

<span data-ttu-id="31c75-162">Le temps nécessaire pour effectuer des déplacements de boîtes aux lettres dépend de la taille de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="31c75-162">The time to complete mailbox moves depends on the size of the mailbox.</span></span> <span data-ttu-id="31c75-163">Si la clé client n’a pas entièrement chiffré la boîte aux lettres après 72 heures après l’heure où vous affectez une nouvelle DEP, lancez un déplacement de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="31c75-163">If Customer Key hasn't completely encrypted the mailbox after 72 hours from the time you assign a new DEP, initiate a mailbox move.</span></span> <span data-ttu-id="31c75-164">Pour ce faire, utilisez la cmdlet New-MoveRequest et fournissez l’alias de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="31c75-164">To do this, use the New-MoveRequest cmdlet and provide the alias of the mailbox.</span></span> <span data-ttu-id="31c75-165">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="31c75-165">For example:</span></span>
  
```powershell
New-MoveRequest <alias>
```

<span data-ttu-id="31c75-166">Pour plus d’informations sur cette cmdlet, consultez la rubrique [Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/new-moverequest?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="31c75-166">For more information about this cmdlet, see [Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/new-moverequest?view=exchange-ps).</span></span>

### <a name="verify-encryption-completes-for-sharepointonlineonedriveforbusinessandteamsfiles"></a><span data-ttu-id="31c75-167">Vérifier que le chiffrement est terminé pour SharePoint Online, OneDrive entreprise et les fichiers teams</span><span class="sxs-lookup"><span data-stu-id="31c75-167">Verify encryption completes for SharePoint Online, OneDrive for Business, and Teams files</span></span>

<span data-ttu-id="31c75-168">Vérifiez l’état du chiffrement en exécutant la cmdlet Get-SPODataEncryptionPolicy comme suit :</span><span class="sxs-lookup"><span data-stu-id="31c75-168">Check on the status of encryption by running the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>

```powershell
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

<span data-ttu-id="31c75-169">La sortie de cette cmdlet comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="31c75-169">The output from this cmdlet includes:</span></span>
  
- <span data-ttu-id="31c75-170">URI de la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="31c75-170">The URI of the primary key.</span></span>

- <span data-ttu-id="31c75-171">URI de la clé secondaire.</span><span class="sxs-lookup"><span data-stu-id="31c75-171">The URI of the secondary key.</span></span>

- <span data-ttu-id="31c75-172">État de chiffrement de la zone géographique.</span><span class="sxs-lookup"><span data-stu-id="31c75-172">The encryption status for the geo.</span></span> <span data-ttu-id="31c75-173">Les États possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="31c75-173">Possible states include:</span></span>

  - <span data-ttu-id="31c75-174">Non **enregistré :** Le chiffrement de clé client n’a pas encore été appliqué.</span><span class="sxs-lookup"><span data-stu-id="31c75-174">**Unregistered:** Customer Key encryption has not yet been applied.</span></span>

  - <span data-ttu-id="31c75-175">**Inscription :** Le chiffrement de clés client a été appliqué et vos fichiers sont en cours de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="31c75-175">**Registering:** Customer Key encryption has been applied and your files are in the process of being encrypted.</span></span> <span data-ttu-id="31c75-176">Si la clé de la zone géographique est inscrite, vous verrez également des informations sur le pourcentage de sites dans la zone géographique, afin que vous puissiez surveiller la progression du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="31c75-176">If the key for the geo is registering, you'll also be shown information on what percentage of sites in the geo are complete so that you can monitor encryption progress.</span></span>

  - <span data-ttu-id="31c75-177">**Inscrit :** Le chiffrement de clés client a été appliqué et tous les fichiers de tous les sites ont été chiffrés.</span><span class="sxs-lookup"><span data-stu-id="31c75-177">**Registered:** Customer Key encryption has been applied, and all files in all sites have been encrypted.</span></span>

  - <span data-ttu-id="31c75-178">**Roulement :** Un roulement de clé est en cours.</span><span class="sxs-lookup"><span data-stu-id="31c75-178">**Rolling:** A key roll is in progress.</span></span> <span data-ttu-id="31c75-179">Si la clé pour le géo est propagée, vous verrez également des informations sur le pourcentage de sites ayant terminé l’opération de Roll Key afin de pouvoir surveiller la progression.</span><span class="sxs-lookup"><span data-stu-id="31c75-179">If the key for the geo is rolling, you'll also be shown information on what percentage of sites have completed the key roll operation so that you can monitor progress.</span></span>

## <a name="revoke-your-keys-and-start-the-data-purge-path-process"></a><span data-ttu-id="31c75-180">Révoquer vos clés et démarrer le processus de purge des données</span><span class="sxs-lookup"><span data-stu-id="31c75-180">Revoke your keys and start the data purge path process</span></span>

<span data-ttu-id="31c75-181">Vous contrôlez la révocation de toutes les clés racines, y compris la clé de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="31c75-181">You control the revocation of all root keys including the availability key.</span></span> <span data-ttu-id="31c75-182">La clé client permet de contrôler l’aspect de la planification de sortie des exigences réglementaires.</span><span class="sxs-lookup"><span data-stu-id="31c75-182">Customer Key provides control of the exit planning aspect of the regulatory requirements for you.</span></span> <span data-ttu-id="31c75-183">Si vous décidez d’annuler vos clés pour purger vos données et quitter le service, le service supprime la clé de disponibilité une fois le processus de purge des données terminé.</span><span class="sxs-lookup"><span data-stu-id="31c75-183">If you decide to revoke your keys to purge your data and exit the service, the service deletes the availability key once the data purge process completes.</span></span>

<span data-ttu-id="31c75-184">Office 365 audite et valide le chemin de purge des données.</span><span class="sxs-lookup"><span data-stu-id="31c75-184">Office 365 audits and validates the data purge path.</span></span> <span data-ttu-id="31c75-185">Pour plus d’informations, reportez-vous au rapport SSAE 18 SOC 2 disponible sur le [portail d’approbation de services](https://servicetrust.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="31c75-185">For more information, see the SSAE 18 SOC 2 Report available on the [Service Trust Portal](https://servicetrust.microsoft.com/).</span></span> <span data-ttu-id="31c75-186">En outre, Microsoft recommande les documents suivants :</span><span class="sxs-lookup"><span data-stu-id="31c75-186">In addition, Microsoft recommends the following documents:</span></span>

- [<span data-ttu-id="31c75-187">Guide de conformité et d’évaluation des risques pour les établissements financiers dans le Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="31c75-187">Risk Assessment and Compliance Guide for Financial Institutions in the Microsoft Cloud</span></span>](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

- [<span data-ttu-id="31c75-188">Considérations relatives à la planification de la sortie de O365</span><span class="sxs-lookup"><span data-stu-id="31c75-188">O365 Exit Planning Considerations</span></span>](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=77ea7ebf-ce1b-4a5f-9972-d2d81a951d99&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

<span data-ttu-id="31c75-189">Le chemin de purge des données diffère légèrement entre les différents services Office 365.</span><span class="sxs-lookup"><span data-stu-id="31c75-189">The data purge path differs slightly between the different Office 365 services.</span></span>

### <a name="revoke-your-customer-keys-and-the-availability-key-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="31c75-190">Révoquer vos clés client et la clé de disponibilité pour Exchange Online et Skype entreprise</span><span class="sxs-lookup"><span data-stu-id="31c75-190">Revoke your Customer Keys and the availability key for Exchange Online and Skype for Business</span></span>

<span data-ttu-id="31c75-191">Lorsque vous lancez le chemin de purge des données pour Exchange Online et Skype entreprise, vous définissez une demande de purge des données permanente sur une DEP.</span><span class="sxs-lookup"><span data-stu-id="31c75-191">When you initiate the data purge path for Exchange Online and Skype for Business, you set a permanent data purge request on a DEP.</span></span> <span data-ttu-id="31c75-192">Cette opération supprime définitivement les données chiffrées dans les boîtes aux lettres auxquelles cette DEP est attribuée.</span><span class="sxs-lookup"><span data-stu-id="31c75-192">Doing so permanently deletes encrypted data within the mailboxes to which that DEP is assigned.</span></span>

<span data-ttu-id="31c75-193">Étant donné que vous ne pouvez exécuter l’applet de commande PowerShell que sur une seule DEP à la fois, envisagez de réaffecter une seule DEP à toutes vos boîtes aux lettres avant d’initier le chemin de purge des données.</span><span class="sxs-lookup"><span data-stu-id="31c75-193">Since you can only run the PowerShell cmdlet against one DEP at a time, consider reassigning a single DEP to all of your mailboxes before you initiate the data purge path.</span></span>

> [!WARNING]
> <span data-ttu-id="31c75-194">N’utilisez pas le chemin de purge des données pour supprimer un sous-ensemble de vos boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="31c75-194">Do not use the data purge path to delete a subset of your mailboxes.</span></span> <span data-ttu-id="31c75-195">Ce processus est destiné uniquement aux clients qui quittent le service.</span><span class="sxs-lookup"><span data-stu-id="31c75-195">This process is only intended for customers who are exiting the service.</span></span>

<span data-ttu-id="31c75-196">Pour lancer le chemin de purge des données, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="31c75-196">To initiate the data purge path, complete these steps:</span></span>

1. <span data-ttu-id="31c75-197">Supprimez les autorisations Wrap et Unwrap pour « O365 Exchange Online » à partir de coffres de clés Azure.</span><span class="sxs-lookup"><span data-stu-id="31c75-197">Remove wrap and unwrap permissions for “O365 Exchange Online” from Azure Key Vaults.</span></span>

2. <span data-ttu-id="31c75-198">À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général dans votre organisation Office 365, [Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="31c75-198">Using a work or school account that has global administrator privileges in your Office 365 organization, [connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>

3. <span data-ttu-id="31c75-199">Pour chaque DEP contenant des boîtes aux lettres que vous souhaitez supprimer, exécutez la cmdlet [Set-DataEncryptionPolicy](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/set-dataencryptionpolicy) comme suit.</span><span class="sxs-lookup"><span data-stu-id="31c75-199">For each DEP that contains mailboxes that you want to delete, run the [Set-DataEncryptionPolicy](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/set-dataencryptionpolicy) cmdlet as follows.</span></span>

    ```powershell
    Set-DataEncryptionPolicy <Policy ID> -PermanentDataPurgeRequested -PermanentDataPurgeReason <Reason> -PermanentDataPurgeContact <ContactName>
    ```

   <span data-ttu-id="31c75-200">Si la commande échoue, vérifiez que vous avez supprimé les autorisations Exchange Online des deux clés dans le coffre de clés Azure, comme indiqué précédemment dans cette tâche.</span><span class="sxs-lookup"><span data-stu-id="31c75-200">If the command fails, ensure that you've removed the Exchange Online permissions from both keys in Azure Key Vault as specified earlier in this task.</span></span><span data-ttu-id="31c75-201">Une fois que vous avez défini le commutateur PermanentDataPurgeRequested à l’aide de l’applet de commande Set-DataEncryptionPolicy, vous ne pourrez plus affecter cette DEP à des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="31c75-201"> Once you've set the PermanentDataPurgeRequested switch using the Set-DataEncryptionPolicy cmdlet, you'll no longer be able to assign this DEP to mailboxes.</span></span>

4. <span data-ttu-id="31c75-202">Contactez le support Microsoft et demandez la purge des données eDocument.</span><span class="sxs-lookup"><span data-stu-id="31c75-202">Contact Microsoft support and request the Data Purge eDocument.</span></span>

    <span data-ttu-id="31c75-203">À votre demande, Microsoft vous envoie un document légal pour valider et autoriser la suppression des données.</span><span class="sxs-lookup"><span data-stu-id="31c75-203">At your request, Microsoft sends you a legal document to acknowledge and authorize data deletion.</span></span> <span data-ttu-id="31c75-204">La personne de votre organisation qui s’est inscrite en tant qu’approbateur dans l’offre FastTrack pendant l’intégration doit signer ce document.</span><span class="sxs-lookup"><span data-stu-id="31c75-204">The person in your organization who signed up as an approver in the FastTrack offer during onboarding needs to sign this document.</span></span> <span data-ttu-id="31c75-205">En règle générale, il s’agit d’un cadre ou d’une autre personne désignée dans votre société qui est légalement autorisée à signer les documents au nom de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="31c75-205">Normally, this is an executive or other designated person in your company who is legally authorized to sign the paperwork on behalf of your organization.</span></span>

5. <span data-ttu-id="31c75-206">Une fois que votre représentant a signé le document juridique, renvoyez-le à Microsoft (généralement par le biais d’une signature eDoc).</span><span class="sxs-lookup"><span data-stu-id="31c75-206">Once your representative has signed the legal document, return it to Microsoft (usually through an eDoc signature).</span></span>

    <span data-ttu-id="31c75-207">Une fois que Microsoft reçoit le document juridique, Microsoft exécute des applets de commande pour déclencher la purge des données qui supprime la stratégie, marque les boîtes aux lettres pour la suppression définitive, puis supprime la clé de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="31c75-207">Once Microsoft receives the legal document, Microsoft runs cmdlets to trigger the data purge which first deletes the policy, marks the mailboxes for permanent deletion, then deletes the availability key.</span></span> <span data-ttu-id="31c75-208">Une fois le processus de purge des données terminé, les données ont été purgées, sont inaccessibles à Exchange Online et ne sont pas récupérables.</span><span class="sxs-lookup"><span data-stu-id="31c75-208">Once the data purge process completes, the data has been purged, is inaccessible to Exchange Online, and is not recoverable.</span></span>

### <a name="revoke-your-customer-keys-and-the-availability-key-for-sharepointonlineonedriveforbusinessandteamsfiles"></a><span data-ttu-id="31c75-209">Révoquer vos clés client et la clé de disponibilité pour les fichiers SharePoint Online, OneDrive entreprise et Teams</span><span class="sxs-lookup"><span data-stu-id="31c75-209">Revoke your Customer Keys and the availability key for SharePoint Online, OneDrive for Business, and Teams files</span></span>

<span data-ttu-id="31c75-210">Pour lancer le chemin de purge des données pour SharePoint Online, OneDrive entreprise et les fichiers Teams, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="31c75-210">To initiate the data purge path for SharePoint Online, OneDrive for Business, and Teams files, complete these steps:</span></span>

1. <span data-ttu-id="31c75-211">Révoquer l’accès au coffre de clés Azure.</span><span class="sxs-lookup"><span data-stu-id="31c75-211">Revoke Azure Key Vault access.</span></span> <span data-ttu-id="31c75-212">Tous les administrateurs de coffre-fort principal doivent accepter de révoquer l’accès.</span><span class="sxs-lookup"><span data-stu-id="31c75-212">All key vault admins must agree to revoke access.</span></span>

   <span data-ttu-id="31c75-213">Vous ne supprimez pas le coffre-fort de clés Azure pour SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="31c75-213">You do not delete the Azure Key Vault for SharePoint Online.</span></span> <span data-ttu-id="31c75-214">Les coffres clés peuvent être partagés entre plusieurs clients SharePoint Online et DEPs.</span><span class="sxs-lookup"><span data-stu-id="31c75-214">Key vaults may be shared among several SharePoint Online tenants and DEPs.</span></span>

2. <span data-ttu-id="31c75-215">Contactez Microsoft pour supprimer la clé de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="31c75-215">Contact Microsoft to delete the availability key.</span></span>

    <span data-ttu-id="31c75-216">Lorsque vous contactez Microsoft pour supprimer la clé de disponibilité, nous vous enverrons un document légal.</span><span class="sxs-lookup"><span data-stu-id="31c75-216">When you contact Microsoft to delete the availability key, we'll send you a legal document.</span></span> <span data-ttu-id="31c75-217">La personne de votre organisation qui s’est inscrite en tant qu’approbateur dans l’offre FastTrack pendant l’intégration doit signer ce document.</span><span class="sxs-lookup"><span data-stu-id="31c75-217">The person in your organization who signed up as an approver in the FastTrack offer during onboarding needs to sign this document.</span></span> <span data-ttu-id="31c75-218">En règle générale, il s’agit d’un cadre ou d’une autre personne désignée dans votre société qui est légalement habilitée à signer des documents au nom de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="31c75-218">Normally, this is an executive or other designated person in your company who's legally authorized to sign the paperwork on behalf of your organization.</span></span>

3. <span data-ttu-id="31c75-219">Une fois que votre représentant signe le document juridique, renvoyez-le à Microsoft (généralement par le biais d’une signature eDoc).</span><span class="sxs-lookup"><span data-stu-id="31c75-219">Once your representative signs the legal document, return it to Microsoft (usually through an eDoc signature).</span></span>

   <span data-ttu-id="31c75-220">Une fois que Microsoft reçoit le document juridique, nous exécutons des cmdlets pour déclencher la purge des données qui effectue la suppression de chiffrement de la clé de client, de la clé de site et de toutes les clés individuelles par document, tout en fractionnant la hiérarchie de clés.</span><span class="sxs-lookup"><span data-stu-id="31c75-220">Once Microsoft receives the legal document, we run cmdlets to trigger the data purge which performs crypto deletion of the tenant key, site key, and all individual per-document keys, irrevocably breaking the key hierarchy.</span></span> <span data-ttu-id="31c75-221">Une fois les cmdlets de purge des données terminées, vos données ont été purgées.</span><span class="sxs-lookup"><span data-stu-id="31c75-221">Once the data purge cmdlets complete, your data has been purged.</span></span>

## <a name="related-articles"></a><span data-ttu-id="31c75-222">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="31c75-222">Related articles</span></span>

- [<span data-ttu-id="31c75-223">Chiffrement de service avec la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="31c75-223">Service encryption with Customer Key for Office 365</span></span>](customer-key-overview.md)

- [<span data-ttu-id="31c75-224">En savoir plus sur la clé de disponibilité</span><span class="sxs-lookup"><span data-stu-id="31c75-224">Learn about the availability key</span></span>](customer-key-availability-key-understand.md)

- [<span data-ttu-id="31c75-225">Configurer la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="31c75-225">Set up Customer Key for Office 365</span></span>](customer-key-set-up.md)

- [<span data-ttu-id="31c75-226">Faire pivoter ou faire pivoter une clé client ou une clé de disponibilité</span><span class="sxs-lookup"><span data-stu-id="31c75-226">Roll or rotate a Customer Key or an availability key</span></span>](customer-key-availability-key-roll.md)

- [<span data-ttu-id="31c75-227">Référentiel sécurisé du client dans Office 365</span><span class="sxs-lookup"><span data-stu-id="31c75-227">Customer Lockbox in Office 365</span></span>](customer-lockbox-requests.md)

- [<span data-ttu-id="31c75-228">Chiffrement du service Office 365</span><span class="sxs-lookup"><span data-stu-id="31c75-228">Office 365 Service Encryption</span></span>](office-365-service-encryption.md)
