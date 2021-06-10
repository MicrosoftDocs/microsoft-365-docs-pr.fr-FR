---
title: Echanger ou alterner entre une clé client ou de disponibilité
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Découvrez comment déployer les clés racine du client stockées dans Azure Key Vault qui sont utilisées avec la clé client. Les services incluent Exchange Online, Skype Entreprise, SharePoint Online, OneDrive Entreprise et Teams fichiers.
ms.openlocfilehash: 892d77959bec1fb33b0ea6bcfaa8c530dd9b8911
ms.sourcegitcommit: 94e64afaf12f3d8813099d8ffa46baba65772763
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "52345117"
---
# <a name="roll-or-rotate-a-customer-key-or-an-availability-key"></a><span data-ttu-id="d4c21-104">Echanger ou alterner entre une clé client ou de disponibilité</span><span class="sxs-lookup"><span data-stu-id="d4c21-104">Roll or rotate a Customer Key or an availability key</span></span>

> [!CAUTION]
> <span data-ttu-id="d4c21-105">Ne lancez qu’une clé de chiffrement que vous utilisez avec la clé client lorsque vos exigences de sécurité ou de conformité vous imposent de la mettre en place.</span><span class="sxs-lookup"><span data-stu-id="d4c21-105">Only roll an encryption key that you use with Customer Key when your security or compliance requirements dictate that you must roll the key.</span></span> <span data-ttu-id="d4c21-106">En outre, ne supprimez pas les clés qui sont ou qui ont été associées à des stratégies.</span><span class="sxs-lookup"><span data-stu-id="d4c21-106">In addition, do not delete any keys that are or were associated with policies.</span></span> <span data-ttu-id="d4c21-107">Lorsque vous rollez vos clés, le contenu est chiffré avec les clés précédentes.</span><span class="sxs-lookup"><span data-stu-id="d4c21-107">When you roll your keys, there will be content encrypted with the previous keys.</span></span> <span data-ttu-id="d4c21-108">Par exemple, alors que les boîtes aux lettres actives sont fréquemment chiffrées, les boîtes aux lettres inactives, déconnectées et désactivées peuvent toujours être chiffrées avec les clés précédentes.</span><span class="sxs-lookup"><span data-stu-id="d4c21-108">For example, while active mailboxes will be re-encrypted frequently, inactive, disconnected, and disabled mailboxes may still be encrypted with the previous keys.</span></span> <span data-ttu-id="d4c21-109">SharePoint Online effectue la sauvegarde du contenu à des fins de restauration et de récupération, de sorte qu’il peut toujours y avoir du contenu archivé à l’aide d’anciennes clés.</span><span class="sxs-lookup"><span data-stu-id="d4c21-109">SharePoint Online performs backup of content for restore and recovery purposes, so there may still be archived content using older keys.</span></span>

## <a name="about-rolling-the-availability-key"></a><span data-ttu-id="d4c21-110">À propos du déploiement de la clé de disponibilité</span><span class="sxs-lookup"><span data-stu-id="d4c21-110">About rolling the availability key</span></span>

<span data-ttu-id="d4c21-111">Microsoft n’expose pas le contrôle direct de la clé de disponibilité aux clients.</span><span class="sxs-lookup"><span data-stu-id="d4c21-111">Microsoft does not expose direct control of the availability key to customers.</span></span> <span data-ttu-id="d4c21-112">Par exemple, vous pouvez uniquement faire pivoter (faire pivoter) les clés que vous possédez dans Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d4c21-112">For example, you can only roll (rotate) the keys that you own in Azure Key Vault.</span></span> <span data-ttu-id="d4c21-113">Microsoft 365 les clés de disponibilité selon une planification définie en interne.</span><span class="sxs-lookup"><span data-stu-id="d4c21-113">Microsoft 365 rolls the availability keys on an internally-defined schedule.</span></span> <span data-ttu-id="d4c21-114">Il n’existe aucun contrat de niveau de service (SLA) client pour ces chiffres clés.</span><span class="sxs-lookup"><span data-stu-id="d4c21-114">There is no customer-facing, service-level agreement (SLA) for these key rolls.</span></span> <span data-ttu-id="d4c21-115">Microsoft 365 la clé de disponibilité à l’aide Microsoft 365 code de service dans un processus automatisé et non manuel.</span><span class="sxs-lookup"><span data-stu-id="d4c21-115">Microsoft 365 rotates the availability key using Microsoft 365 service code in an automated, non-manual process.</span></span> <span data-ttu-id="d4c21-116">Les administrateurs Microsoft peuvent lancer le processus de déploiement.</span><span class="sxs-lookup"><span data-stu-id="d4c21-116">Microsoft administrators may initiate the roll process.</span></span> <span data-ttu-id="d4c21-117">La clé est déployée à l’aide de mécanismes automatisés sans accès direct au magasin de clés.</span><span class="sxs-lookup"><span data-stu-id="d4c21-117">The key is rolled using automated mechanisms without direct access to the key store.</span></span> <span data-ttu-id="d4c21-118">L’accès au magasin de clés secrètes de disponibilité n’est pas disponible pour les administrateurs Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d4c21-118">Access to the availability key secret store is not provisioned to Microsoft administrators.</span></span> <span data-ttu-id="d4c21-119">Le déploiement de clé de disponibilité utilise le même mécanisme que celui utilisé pour générer initialement la clé.</span><span class="sxs-lookup"><span data-stu-id="d4c21-119">Availability key rolling leverages the same mechanism used to initially generate the key.</span></span> <span data-ttu-id="d4c21-120">Pour plus d’informations sur la clé de disponibilité, voir [Comprendre la clé de disponibilité.](customer-key-availability-key-understand.md)</span><span class="sxs-lookup"><span data-stu-id="d4c21-120">For more information about the availability key, see [Understand the availability key](customer-key-availability-key-understand.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4c21-121">Exchange Online et Skype Entreprise clés de disponibilité peuvent être correctement déployées par les clients qui créent une nouvelle dep, car une clé de disponibilité unique est générée pour chaque deP que vous créez.</span><span class="sxs-lookup"><span data-stu-id="d4c21-121">Exchange Online and Skype for Business availability keys can be effectively rolled by customers creating a new DEP, since a unique availability key is generated for each DEP you create.</span></span> <span data-ttu-id="d4c21-122">Les clés de disponibilité pour les fichiers SharePoint Online, OneDrive Entreprise et Teams existent au niveau de la forêt et sont partagées entre les PD DEP et les clients, ce qui signifie que le déploiement se produit uniquement selon une planification définie en interne par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d4c21-122">Availability keys for SharePoint Online, OneDrive for Business, and Teams files exist at the forest level and are shared across DEPs and customers, which means rolling only occurs at a Microsoft internally defined schedule.</span></span> <span data-ttu-id="d4c21-123">Pour atténuer le risque de ne pas déployer la clé de disponibilité chaque fois qu’un nouveau dep est créé, SharePoint, OneDrive et Teams la clé intermédiaire du client (TIK), la clé wrapped par les clés racine du client et la clé de disponibilité, chaque fois qu’un nouveau dep est créé.</span><span class="sxs-lookup"><span data-stu-id="d4c21-123">To mitigate the risk of not rolling the availability key each time a new DEP is created, SharePoint, OneDrive, and Teams roll the tenant intermediate key (TIK), the key wrapped by the customer root keys and availability key, each time a new DEP is created.</span></span>

## <a name="request-a-new-version-of-each-existing-root-key-you-want-to-roll"></a><span data-ttu-id="d4c21-124">Demander une nouvelle version de chaque clé racine existante que vous souhaitez déployer</span><span class="sxs-lookup"><span data-stu-id="d4c21-124">Request a new version of each existing root key you want to roll</span></span>

<span data-ttu-id="d4c21-125">Lorsque vous rollez une clé, vous demandez une nouvelle version d’une clé existante.</span><span class="sxs-lookup"><span data-stu-id="d4c21-125">When you roll a key, you request a new version of an existing key.</span></span> <span data-ttu-id="d4c21-126">Pour demander une nouvelle version d’une clé existante, utilisez la même cmdlet, [Add-AzKeyVaultKey,](/powershell/module/az.keyvault/add-azkeyvaultkey)avec la même syntaxe que celle utilisée pour créer la clé.</span><span class="sxs-lookup"><span data-stu-id="d4c21-126">To request a new version of an existing key, you use the same cmdlet, [Add-AzKeyVaultKey](/powershell/module/az.keyvault/add-azkeyvaultkey), with the same syntax that you used to create the key in the first place.</span></span> <span data-ttu-id="d4c21-127">Une fois que vous avez terminé le déploiement d’une clé associée à une stratégie de chiffrement de données ( DEP), vous exécutez une autre cmdlet pour vous assurer que la clé client commence à utiliser la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="d4c21-127">After you've finished rolling any key associated with a Data Encryption Policy (DEP), you run another cmdlet to ensure that Customer Key begins using the new key.</span></span> <span data-ttu-id="d4c21-128">Faites cette étape dans chaque coffre de clés Azure (AKV).</span><span class="sxs-lookup"><span data-stu-id="d4c21-128">Do this step in each Azure Key Vault (AKV).</span></span>

<span data-ttu-id="d4c21-129">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="d4c21-129">For example:</span></span>

1. <span data-ttu-id="d4c21-130">Connectez-vous à votre abonnement Azure avec Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d4c21-130">Sign in to your Azure subscription with Azure PowerShell.</span></span> <span data-ttu-id="d4c21-131">Pour obtenir des instructions, [voir Se Azure PowerShell](/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="d4c21-131">For instructions, see [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps).</span></span>

2. <span data-ttu-id="d4c21-132">Exécutez la cmdlet Add-AzKeyVaultKey comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="d4c21-132">Run the Add-AzKeyVaultKey cmdlet as shown in the following example:</span></span>

   ```powershell
   Add-AzKeyVaultKey -VaultName Contoso-CK-EX-NA-VaultA1 -Name Contoso-CK-EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
   ```

   <span data-ttu-id="d4c21-133">Dans cet exemple, étant donné qu’une clé nommée **Contoso-CK-EX-NA-VaultA1-Key001** existe dans le coffre **Contoso-CK-EX-NA-VaultA1,** l’cmdlet crée une nouvelle version de la clé.</span><span class="sxs-lookup"><span data-stu-id="d4c21-133">In this example, since a key named **Contoso-CK-EX-NA-VaultA1-Key001** exists in the **Contoso-CK-EX-NA-VaultA1** vault, the cmdlet creates a new version of the key.</span></span> <span data-ttu-id="d4c21-134">Cette opération conserve les versions de clé précédentes dans l’historique des versions de la clé.</span><span class="sxs-lookup"><span data-stu-id="d4c21-134">This operation preserves the previous key versions in the version history for the key.</span></span> <span data-ttu-id="d4c21-135">Vous avez besoin de la version de clé précédente pour déchiffrer les données qu’elle chiffre toujours.</span><span class="sxs-lookup"><span data-stu-id="d4c21-135">You need the previous key version to decrypt the data that it still encrypts.</span></span> <span data-ttu-id="d4c21-136">Une fois que vous avez terminé le déploiement d’une clé associée à une dep, exécutez une cmdlet supplémentaire pour vous assurer que la clé client commence à utiliser la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="d4c21-136">Once you complete rolling any key associated with a DEP,  run an extra cmdlet to ensure that Customer Key begins using the new key.</span></span> <span data-ttu-id="d4c21-137">Les sections suivantes décrivent les cmdlets plus en détail.</span><span class="sxs-lookup"><span data-stu-id="d4c21-137">The following sections describe the cmdlets in more detail.</span></span>
  
## <a name="update-the-keys-for-multi-workload-deps"></a><span data-ttu-id="d4c21-138">Mettre à jour les clés pour les ppp multi-charges de travail</span><span class="sxs-lookup"><span data-stu-id="d4c21-138">Update the keys for multi-workload DEPs</span></span>

<span data-ttu-id="d4c21-139">Lorsque vous rollez l’une des clés Azure Key Vault associées à un dep utilisé avec plusieurs charges de travail, vous devez mettre à jour le dep pour pointer vers la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="d4c21-139">When you roll either of the Azure Key Vault keys associated with a DEP used with multiple workloads, you must update the DEP to point to the new key.</span></span> <span data-ttu-id="d4c21-140">Ce processus ne fait pas pivoter la clé de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="d4c21-140">This process does not rotate the availability key.</span></span>

<span data-ttu-id="d4c21-141">Pour demander à la clé client d’utiliser la nouvelle clé pour chiffrer plusieurs charges de travail, complétez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c21-141">To instruct Customer Key to use the new key to encrypt multiple workloads, complete these steps:</span></span>

1. <span data-ttu-id="d4c21-142">Sur votre ordinateur local, à l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général ou d’administrateur de conformité dans votre organisation, connectez-vous à [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) dans une fenêtre Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d4c21-142">On your local computer, using a work or school account that has global administrator or compliance admin permissions in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) in a Windows PowerShell window.</span></span>

2. <span data-ttu-id="d4c21-143">Exécutez lSet-M365DataAtRestEncryptionPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4c21-143">Run the Set-M365DataAtRestEncryptionPolicy cmdlet.</span></span>
  
   ```powershell
   Set-M365DataAtRestEncryptionPolicy -[Identity] "PolicyName" -Refresh
   ```

<span data-ttu-id="d4c21-144">Où *PolicyName est* le nom ou l’ID unique de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="d4c21-144">Where *PolicyName* is the name or unique ID of the policy.</span></span> <span data-ttu-id="d4c21-145">Par exemple, Contoso_Global.</span><span class="sxs-lookup"><span data-stu-id="d4c21-145">For example, Contoso_Global.</span></span>

<span data-ttu-id="d4c21-146">Exemple :</span><span class="sxs-lookup"><span data-stu-id="d4c21-146">Example:</span></span>

```powershell
Set-M365DataAtRestEncryptionPolicy -Identity "Contoso_Global" -Refresh
```

## <a name="update-the-keys-for-exchange-online-deps"></a><span data-ttu-id="d4c21-147">Mettre à jour les clés pour Exchange Online DEP</span><span class="sxs-lookup"><span data-stu-id="d4c21-147">Update the keys for Exchange Online DEPs</span></span>

<span data-ttu-id="d4c21-148">Lorsque vous rollez l’une des clés Azure Key Vault associées à un dep utilisé avec Exchange Online et Skype Entreprise, vous devez mettre à jour le dep pour pointer vers la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="d4c21-148">When you roll either of the Azure Key Vault keys associated with a DEP used with Exchange Online and Skype for Business, you must update the DEP to point to the new key.</span></span> <span data-ttu-id="d4c21-149">Cela ne fait pas pivoter la clé de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="d4c21-149">This does not rotate the availability key.</span></span>

<span data-ttu-id="d4c21-150">Pour demander à la clé client d’utiliser la nouvelle clé pour chiffrer les boîtes aux lettres, exécutez la cmdlet Set-DataEncryptionPolicy comme suit :</span><span class="sxs-lookup"><span data-stu-id="d4c21-150">To instruct Customer Key to use the new key to encrypt mailboxes, run the Set-DataEncryptionPolicy cmdlet as follows:</span></span>

1. <span data-ttu-id="d4c21-151">Exécutez la cmdlet Set-DataEncryptionPolicy dans Azure PowerShell :</span><span class="sxs-lookup"><span data-stu-id="d4c21-151">Run the Set-DataEncryptionPolicy cmdlet in Azure PowerShell:</span></span>
  
   ```powershell
   Set-DataEncryptionPolicy -Identity <DataEncryptionPolicyID> -Refresh
   ```

2. <span data-ttu-id="d4c21-152">Pour vérifier la valeur de la propriété DataEncryptionPolicyID pour la boîte aux lettres, utilisez les étapes de déterminer le [dep](customer-key-manage.md#determine-the-dep-assigned-to-a-mailbox)affecté à une boîte aux lettres .</span><span class="sxs-lookup"><span data-stu-id="d4c21-152">To check the value for the DataEncryptionPolicyID property for the mailbox, use the steps in [Determine the DEP assigned to a mailbox](customer-key-manage.md#determine-the-dep-assigned-to-a-mailbox).</span></span> <span data-ttu-id="d4c21-153">La valeur de cette propriété change une fois que le service applique la clé mise à jour.</span><span class="sxs-lookup"><span data-stu-id="d4c21-153">The value for this property changes once the service applies the updated key.</span></span>
  
## <a name="update-the-keys-for-sharepoint-online-onedrive-for-business-and-teams-files"></a><span data-ttu-id="d4c21-154">Mettre à jour les clés pour SharePoint en ligne, OneDrive Entreprise et Teams fichiers</span><span class="sxs-lookup"><span data-stu-id="d4c21-154">Update the keys for SharePoint Online, OneDrive for Business, and Teams files</span></span>

<span data-ttu-id="d4c21-155">SharePoint Online ne vous permet de déployer qu’une seule clé à la fois.</span><span class="sxs-lookup"><span data-stu-id="d4c21-155">SharePoint Online only allows you to roll one key at a time.</span></span> <span data-ttu-id="d4c21-156">Si vous souhaitez mettre les deux clés dans un coffre de clés, attendez la fin de la première opération.</span><span class="sxs-lookup"><span data-stu-id="d4c21-156">If you want to roll both keys in a key vault, wait for the first operation to complete.</span></span> <span data-ttu-id="d4c21-157">Microsoft vous recommande d’échelonner vos opérations pour éviter ce problème.</span><span class="sxs-lookup"><span data-stu-id="d4c21-157">Microsoft recommends that you stagger your operations to avoid this issue.</span></span> <span data-ttu-id="d4c21-158">Lorsque vous rollez l’une des clés Azure Key Vault associées à un dep utilisé avec SharePoint Online et OneDrive Entreprise, vous devez mettre à jour le dep pour pointer vers la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="d4c21-158">When you roll either of the Azure Key Vault keys associated with a DEP used with SharePoint Online and OneDrive for Business, you must update the DEP to point to the new key.</span></span> <span data-ttu-id="d4c21-159">Cela ne fait pas pivoter la clé de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="d4c21-159">This does not rotate the availability key.</span></span>

1. <span data-ttu-id="d4c21-160">Exécutez la cmdlet Update-SPODataEncryptionPolicy suivante :</span><span class="sxs-lookup"><span data-stu-id="d4c21-160">Run the Update-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
   ```powershell
   Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
   ```

   <span data-ttu-id="d4c21-161">Bien que cette cmdlet démarre l’opération de SharePoint Online et OneDrive Entreprise, l’action ne se termine pas immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d4c21-161">While this cmdlet starts the key roll operation for SharePoint Online and OneDrive for Business, the action doesn't complete immediately.</span></span>

2. <span data-ttu-id="d4c21-162">Pour voir la progression de l’opération de roulis de touches, exécutez Get-SPODataEncryptionPolicy cmdlet comme suit :</span><span class="sxs-lookup"><span data-stu-id="d4c21-162">To see the progress of the key roll operation, run the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>

   ```powershell
   Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
   ```

## <a name="related-articles"></a><span data-ttu-id="d4c21-163">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="d4c21-163">Related articles</span></span>

- [<span data-ttu-id="d4c21-164">Chiffrement de service avec clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="d4c21-164">Service encryption with Customer Key for Office 365</span></span>](customer-key-overview.md)

- [<span data-ttu-id="d4c21-165">Configurer la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="d4c21-165">Set up Customer Key for Office 365</span></span>](customer-key-set-up.md)

- [<span data-ttu-id="d4c21-166">Gérer la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="d4c21-166">Manage Customer Key for Office 365</span></span>](customer-key-manage.md)

- [<span data-ttu-id="d4c21-167">En savoir plus sur la clé de disponibilité</span><span class="sxs-lookup"><span data-stu-id="d4c21-167">Learn about the availability key</span></span>](customer-key-availability-key-understand.md)