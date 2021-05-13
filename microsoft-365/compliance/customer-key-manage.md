---
title: Gérer la clé client
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
description: Après avoir installé la clé client, découvrez comment la gérer en restaurant des clés AKV, en gérant les autorisations et en créant et en attribuant des stratégies de chiffrement de données.
ms.openlocfilehash: da806ec9dcf1327ec5fdd6b0a0c9e7f22c89584e
ms.sourcegitcommit: 94e64afaf12f3d8813099d8ffa46baba65772763
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "52345057"
---
# <a name="manage-customer-key"></a><span data-ttu-id="a36d8-103">Gérer la clé client</span><span class="sxs-lookup"><span data-stu-id="a36d8-103">Manage Customer Key</span></span>

<span data-ttu-id="a36d8-104">Une fois que vous avez installé la clé client pour Office 365, vous devez créer et affecter une ou plusieurs stratégies de chiffrement de données (DEP).</span><span class="sxs-lookup"><span data-stu-id="a36d8-104">After you've set up Customer Key for Office 365, you'll need to create and assign one or more data encryption policies (DEP).</span></span> <span data-ttu-id="a36d8-105">Une fois que vous avez affecté vos dep, vous pouvez gérer vos clés comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a36d8-105">Once you've assigned your DEPs, you can manage your keys as described in this article.</span></span> <span data-ttu-id="a36d8-106">En savoir plus sur la clé client dans les rubriques connexes.</span><span class="sxs-lookup"><span data-stu-id="a36d8-106">Learn more about Customer Key in the related topics.</span></span>

## <a name="create-a-dep-for-use-with-multiple-workloads-for-all-tenant-users"></a><span data-ttu-id="a36d8-107">Créer une PD DEP pour une utilisation avec plusieurs charges de travail pour tous les utilisateurs clients</span><span class="sxs-lookup"><span data-stu-id="a36d8-107">Create a DEP for use with multiple workloads for all tenant users</span></span>

<span data-ttu-id="a36d8-108">Avant de commencer, assurez-vous d’avoir effectué les tâches requises pour configurer le client.</span><span class="sxs-lookup"><span data-stu-id="a36d8-108">Before you begin, ensure that you've completed the tasks required to set up Customer.</span></span> <span data-ttu-id="a36d8-109">Pour plus d’informations, [voir Configurer la clé client.](customer-key-set-up.md)</span><span class="sxs-lookup"><span data-stu-id="a36d8-109">For information, see [Set up Customer Key](customer-key-set-up.md).</span></span> <span data-ttu-id="a36d8-110">Pour créer le PED, vous avez besoin des URIs de coffre de clés que vous avez obtenus lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="a36d8-110">To create the DEP, you need the Key Vault URIs you obtained during setup.</span></span> <span data-ttu-id="a36d8-111">Pour plus d’informations, [voir Obtenir l’URI de chaque clé Azure Key Vault.](customer-key-set-up.md#obtain-the-uri-for-each-azure-key-vault-key)</span><span class="sxs-lookup"><span data-stu-id="a36d8-111">For information, see [Obtain the URI for each Azure Key Vault key](customer-key-set-up.md#obtain-the-uri-for-each-azure-key-vault-key).</span></span>

<span data-ttu-id="a36d8-112">Pour créer une PD DEP à charges multiples, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a36d8-112">To create a multi-workload DEP, follow these steps:</span></span>
  
1. <span data-ttu-id="a36d8-113">Sur votre ordinateur local, à l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général ou d’administrateur de conformité dans votre organisation, connectez-vous à [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) dans une fenêtre Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a36d8-113">On your local computer, using a work or school account that has global administrator or compliance admin permissions in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) in a Windows PowerShell window.</span></span>

2. <span data-ttu-id="a36d8-114">Pour créer une dep, utilisez l'New-M365DataAtRestEncryptionPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a36d8-114">To create a DEP, use the New-M365DataAtRestEncryptionPolicy cmdlet.</span></span>

   ```powershell
   New-M365DataAtRestEncryptionPolicy -Name <PolicyName> -AzureKeyIDs <KeyVaultURI1, KeyVaultURI2> [-Description <String>]
   ```

   <span data-ttu-id="a36d8-115">Où :</span><span class="sxs-lookup"><span data-stu-id="a36d8-115">Where:</span></span>

   - <span data-ttu-id="a36d8-116">*PolicyName est* le nom que vous souhaitez utiliser pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="a36d8-116">*PolicyName* is the name you want to use for the policy.</span></span> <span data-ttu-id="a36d8-117">Les noms ne peuvent pas contenir d’espaces.</span><span class="sxs-lookup"><span data-stu-id="a36d8-117">Names can't contain spaces.</span></span> <span data-ttu-id="a36d8-118">Par exemple, Contoso_Global.</span><span class="sxs-lookup"><span data-stu-id="a36d8-118">For example, Contoso_Global.</span></span>

   - <span data-ttu-id="a36d8-119">*KeyVaultURI1 est* l’URI de la première clé de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="a36d8-119">*KeyVaultURI1* is the URI for the first key in the policy.</span></span> <span data-ttu-id="a36d8-120">Par exemple : <https://contosoWestUSvault1.vault.azure.net/keys/Key_01>.</span><span class="sxs-lookup"><span data-stu-id="a36d8-120">For example, <https://contosoWestUSvault1.vault.azure.net/keys/Key_01>.</span></span>

   - <span data-ttu-id="a36d8-121">*KeyVaultURI2 est* l’URI de la deuxième clé de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="a36d8-121">*KeyVaultURI2* is the URI for the second key in the policy.</span></span> <span data-ttu-id="a36d8-122">Par exemple : <https://contosoCentralUSvault1.vault.azure.net/keys/Key_02>.</span><span class="sxs-lookup"><span data-stu-id="a36d8-122">For example, <https://contosoCentralUSvault1.vault.azure.net/keys/Key_02>.</span></span> <span data-ttu-id="a36d8-123">Séparez les deux URS par une virgule et un espace.</span><span class="sxs-lookup"><span data-stu-id="a36d8-123">Separate the two URIs by a comma and a space.</span></span>

   - <span data-ttu-id="a36d8-124">*La description de* la stratégie est une description conviviale de la stratégie qui vous aidera à vous souvenir de l’objectif de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="a36d8-124">*Policy Description* is a user-friendly description of the policy that will help you remember what the policy is for.</span></span> <span data-ttu-id="a36d8-125">Vous pouvez inclure des espaces dans la description.</span><span class="sxs-lookup"><span data-stu-id="a36d8-125">You can include spaces in the description.</span></span> <span data-ttu-id="a36d8-126">Par exemple, « Stratégie racine pour plusieurs charges de travail pour tous les utilisateurs du client ».</span><span class="sxs-lookup"><span data-stu-id="a36d8-126">For example, "Root policy for multiple workloads for all users in the tenant.".</span></span>

<span data-ttu-id="a36d8-127">Exemple :</span><span class="sxs-lookup"><span data-stu-id="a36d8-127">Example:</span></span>

```powershell
New-M365DataAtRestEncryptionPolicy -Name "Contoso_Global" -AzureKeyIDs "https://contosoWestUSvault1.vault.azure.net/keys/Key_01","https://contosoCentralUSvault1.vault.azure.net/keys/Key_02" -Description "Policy for multiple workloads for all users in the tenant."
```

### <a name="assign-multi-workload-policy"></a><span data-ttu-id="a36d8-128">Attribuer une stratégie multi-charges de travail</span><span class="sxs-lookup"><span data-stu-id="a36d8-128">Assign multi-workload policy</span></span>

<span data-ttu-id="a36d8-129">Attribuez le PDV à l’aide Set-M365DataAtRestEncryptionPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a36d8-129">Assign the DEP by using the Set-M365DataAtRestEncryptionPolicyAssignment cmdlet.</span></span> <span data-ttu-id="a36d8-130">Une fois la stratégie assignée, Microsoft 365 chiffre les données avec la clé identifiée dans le PDV.</span><span class="sxs-lookup"><span data-stu-id="a36d8-130">Once you assign the policy, Microsoft 365 encrypts the data with the key identified in the DEP.</span></span>

```powershell
Set-M365DataAtRestEncryptionPolicyAssignment -DataEncryptionPolicy <PolicyName or ID>
```

 <span data-ttu-id="a36d8-131">Où *PolicyName est* le nom de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="a36d8-131">Where *PolicyName* is the name of the policy.</span></span> <span data-ttu-id="a36d8-132">Par exemple, Contoso_Global.</span><span class="sxs-lookup"><span data-stu-id="a36d8-132">For example, Contoso_Global.</span></span>

<span data-ttu-id="a36d8-133">Exemple :</span><span class="sxs-lookup"><span data-stu-id="a36d8-133">Example:</span></span>

```powershell
Set-M365DataAtRestEncryptionPolicyAssignment -DataEncryptionPolicy "Contoso_Global"
```

## <a name="create-a-dep-for-use-with-exchange-online-mailboxes"></a><span data-ttu-id="a36d8-134">Créer une PD DEP à utiliser avec des boîtes Exchange Online aux lettres</span><span class="sxs-lookup"><span data-stu-id="a36d8-134">Create a DEP for use with Exchange Online mailboxes</span></span>

<span data-ttu-id="a36d8-135">Avant de commencer, assurez-vous d’avoir effectué les tâches requises pour configurer Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a36d8-135">Before you begin, ensure that you've completed the tasks required to set up Azure Key Vault.</span></span> <span data-ttu-id="a36d8-136">Pour plus d’informations, [voir Configurer la clé client.](customer-key-set-up.md)</span><span class="sxs-lookup"><span data-stu-id="a36d8-136">For information, see [Set up Customer Key](customer-key-set-up.md).</span></span> <span data-ttu-id="a36d8-137">Vous effectuerez ces étapes en vous connectant à distance à Exchange Online avec Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a36d8-137">You'll complete these steps by remotely connecting to Exchange Online with Windows PowerShell.</span></span>

<span data-ttu-id="a36d8-138">Un deP est associé à un ensemble de clés stockées dans Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a36d8-138">A DEP is associated with a set of keys stored in Azure Key Vault.</span></span> <span data-ttu-id="a36d8-139">Vous affectez un deP à une boîte aux lettres dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a36d8-139">You assign a DEP to a mailbox in Microsoft 365.</span></span> <span data-ttu-id="a36d8-140">Microsoft 365 utiliser les clés identifiées dans la stratégie pour chiffrer la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a36d8-140">Microsoft 365 will then use the keys identified in the policy to encrypt the mailbox.</span></span> <span data-ttu-id="a36d8-141">Pour créer le PED, vous avez besoin des URIs de coffre de clés que vous avez obtenus lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="a36d8-141">To create the DEP, you need the Key Vault URIs you obtained during setup.</span></span> <span data-ttu-id="a36d8-142">Pour plus d’informations, [voir Obtenir l’URI de chaque clé Azure Key Vault.](customer-key-set-up.md#obtain-the-uri-for-each-azure-key-vault-key)</span><span class="sxs-lookup"><span data-stu-id="a36d8-142">For information, see [Obtain the URI for each Azure Key Vault key](customer-key-set-up.md#obtain-the-uri-for-each-azure-key-vault-key).</span></span>

<span data-ttu-id="a36d8-143">N’oubliez pas !</span><span class="sxs-lookup"><span data-stu-id="a36d8-143">Remember!</span></span> <span data-ttu-id="a36d8-144">Lorsque vous créez un deP, vous spécifiez deux clés dans deux coffres de clés Azure différents.</span><span class="sxs-lookup"><span data-stu-id="a36d8-144">When you create a DEP, you specify two keys in two different Azure Key Vaults.</span></span> <span data-ttu-id="a36d8-145">Créez ces clés dans deux régions Azure distinctes pour assurer la redondance géographique.</span><span class="sxs-lookup"><span data-stu-id="a36d8-145">Create these keys in two separate Azure regions to ensure geo-redundancy.</span></span>

<span data-ttu-id="a36d8-146">Pour créer un deP à utiliser avec une boîte aux lettres, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a36d8-146">To create a DEP to use with a mailbox, follow these steps:</span></span>
  
1. <span data-ttu-id="a36d8-147">Sur votre ordinateur local, à l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général ou d’administrateur Exchange Online dans votre organisation, connectez-vous à [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) dans une fenêtre Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a36d8-147">On your local computer, using a work or school account that has global administrator or Exchange Online admin permissions in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) in a Windows PowerShell window.</span></span>

2. <span data-ttu-id="a36d8-148">Pour créer une dep, utilisez la cmdlet New-DataEncryptionPolicy en tapant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="a36d8-148">To create a DEP, use the New-DataEncryptionPolicy cmdlet by typing the following command.</span></span>

   ```powershell
   New-DataEncryptionPolicy -Name <PolicyName> -Description "Policy Description" -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   <span data-ttu-id="a36d8-149">Où :</span><span class="sxs-lookup"><span data-stu-id="a36d8-149">Where:</span></span>

   - <span data-ttu-id="a36d8-150">*PolicyName est* le nom que vous souhaitez utiliser pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="a36d8-150">*PolicyName* is the name you want to use for the policy.</span></span> <span data-ttu-id="a36d8-151">Les noms ne peuvent pas contenir d’espaces.</span><span class="sxs-lookup"><span data-stu-id="a36d8-151">Names can't contain spaces.</span></span> <span data-ttu-id="a36d8-152">Par exemple, USA_mailboxes.</span><span class="sxs-lookup"><span data-stu-id="a36d8-152">For example, USA_mailboxes.</span></span>

   - <span data-ttu-id="a36d8-153">*La description de* la stratégie est une description conviviale de la stratégie qui vous aidera à vous souvenir de l’objectif de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="a36d8-153">*Policy Description* is a user-friendly description of the policy that will help you remember what the policy is for.</span></span> <span data-ttu-id="a36d8-154">Vous pouvez inclure des espaces dans la description.</span><span class="sxs-lookup"><span data-stu-id="a36d8-154">You can include spaces in the description.</span></span> <span data-ttu-id="a36d8-155">Par exemple, « Clé racine pour les boîtes aux lettres aux États-Unis et ses territoires ».</span><span class="sxs-lookup"><span data-stu-id="a36d8-155">For example, "Root key for mailboxes in USA and its territories".</span></span>

   - <span data-ttu-id="a36d8-156">*KeyVaultURI1 est* l’URI de la première clé de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="a36d8-156">*KeyVaultURI1* is the URI for the first key in the policy.</span></span> <span data-ttu-id="a36d8-157">Par exemple : <https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01>.</span><span class="sxs-lookup"><span data-stu-id="a36d8-157">For example, <https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01>.</span></span>

   - <span data-ttu-id="a36d8-158">*KeyVaultURI2 est* l’URI de la deuxième clé de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="a36d8-158">*KeyVaultURI2* is the URI for the second key in the policy.</span></span> <span data-ttu-id="a36d8-159">Par exemple : <https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02>.</span><span class="sxs-lookup"><span data-stu-id="a36d8-159">For example, <https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02>.</span></span> <span data-ttu-id="a36d8-160">Séparez les deux URS par une virgule et un espace.</span><span class="sxs-lookup"><span data-stu-id="a36d8-160">Separate the two URIs by a comma and a space.</span></span>

   <span data-ttu-id="a36d8-161">Exemple :</span><span class="sxs-lookup"><span data-stu-id="a36d8-161">Example:</span></span>
  
   ```powershell
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault02.vault.azure.net/keys/USA_key_01, https://contoso_CentralUSvault02.vault.azure.net/keys/USA_Key_02
   ```

<span data-ttu-id="a36d8-162">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-DataEncryptionPolicy](/powershell/module/exchange/new-data-encryptionpolicy).</span><span class="sxs-lookup"><span data-stu-id="a36d8-162">For detailed syntax and parameter information, see [New-DataEncryptionPolicy](/powershell/module/exchange/new-data-encryptionpolicy).</span></span>

### <a name="assign-a-dep-to-a-mailbox"></a><span data-ttu-id="a36d8-163">Affecter un deP à une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="a36d8-163">Assign a DEP to a mailbox</span></span>

<span data-ttu-id="a36d8-164">Affectez le deP à une boîte aux lettres à l’aide de Set-Mailbox cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a36d8-164">Assign the DEP to a mailbox by using the Set-Mailbox cmdlet.</span></span> <span data-ttu-id="a36d8-165">Une fois la stratégie assignée, Microsoft 365 pouvez chiffrer la boîte aux lettres avec la clé identifiée dans le PDV.</span><span class="sxs-lookup"><span data-stu-id="a36d8-165">Once you assign the policy, Microsoft 365 can encrypt the mailbox with the key identified in the DEP.</span></span>
  
```powershell
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

<span data-ttu-id="a36d8-166">Où *MailboxIdParameter* spécifie une boîte aux lettres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a36d8-166">Where *MailboxIdParameter* specifies a user mailbox.</span></span> <span data-ttu-id="a36d8-167">Pour plus d’informations sur la cmdlet Set-Mailbox, voir [Set-Mailbox](/powershell/module/exchange/set-mailbox).</span><span class="sxs-lookup"><span data-stu-id="a36d8-167">For more information about the Set-Mailbox cmdlet, see [Set-Mailbox](/powershell/module/exchange/set-mailbox).</span></span>

<span data-ttu-id="a36d8-168">Dans les environnements hybrides, vous pouvez affecter un deP aux données de boîte aux lettres sur site qui sont synchronisées dans votre Exchange Online client.</span><span class="sxs-lookup"><span data-stu-id="a36d8-168">In hybrid environments, you can assign a DEP to the on-premises mailbox data that is synchronized into your Exchange Online tenant.</span></span> <span data-ttu-id="a36d8-169">Pour affecter un dep à ces données de boîte aux lettres synchronisées, vous devez utiliser la cmdlet Set-MailUser de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a36d8-169">To assign a DEP to this synchronized mailbox data, you'll use the Set-MailUser cmdlet.</span></span> <span data-ttu-id="a36d8-170">Pour plus d’informations sur les données de boîte aux lettres dans l’environnement hybride, voir les boîtes aux lettres sur site utilisant Outlook pour iOS et Android avec l’authentification [moderne hybride.](/exchange/clients/outlook-for-ios-and-android/use-hybrid-modern-auth)</span><span class="sxs-lookup"><span data-stu-id="a36d8-170">For more information about mailbox data in the hybrid environment, see [on-premises mailboxes using Outlook for iOS and Android with hybrid Modern Authentication](/exchange/clients/outlook-for-ios-and-android/use-hybrid-modern-auth).</span></span>

```powershell
Set-MailUser -Identity <MailUserIdParameter> -DataEncryptionPolicy <PolicyName>
```

<span data-ttu-id="a36d8-171">Où *MailUserIdParameter* spécifie un utilisateur de messagerie (également appelé utilisateur à messagerie).</span><span class="sxs-lookup"><span data-stu-id="a36d8-171">Where *MailUserIdParameter* specifies a mail user (also known as a mail-enabled user).</span></span> <span data-ttu-id="a36d8-172">Pour plus d’informations sur la cmdlet Set-MailUser, voir [Set-MailUser](/powershell/module/exchange/set-mailuser).</span><span class="sxs-lookup"><span data-stu-id="a36d8-172">For more information about the Set-MailUser cmdlet, see [Set-MailUser](/powershell/module/exchange/set-mailuser).</span></span>

## <a name="create-a-dep-for-use-with-sharepoint-online-onedrive-for-business-and-teams-files"></a><span data-ttu-id="a36d8-173">Créer une PD DEP à utiliser avec SharePoint Online, OneDrive Entreprise et Teams fichiers</span><span class="sxs-lookup"><span data-stu-id="a36d8-173">Create a DEP for use with SharePoint Online, OneDrive for Business, and Teams files</span></span>

<span data-ttu-id="a36d8-174">Avant de commencer, assurez-vous d’avoir effectué les tâches requises pour configurer Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a36d8-174">Before you begin, ensure that you've completed the tasks required to set up Azure Key Vault.</span></span> <span data-ttu-id="a36d8-175">Pour plus d’informations, [voir Configurer la clé client.](customer-key-set-up.md)</span><span class="sxs-lookup"><span data-stu-id="a36d8-175">For information, see [Set up Customer Key](customer-key-set-up.md).</span></span>
  
<span data-ttu-id="a36d8-176">Pour configurer la clé client pour les fichiers SharePoint Online, OneDrive Entreprise et Teams, vous devez effectuer ces étapes en vous connectant à distance à SharePoint Online avec Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a36d8-176">To set up Customer Key for SharePoint Online, OneDrive for Business, and Teams files you complete these steps by remotely connecting to SharePoint Online with Windows PowerShell.</span></span>
  
<span data-ttu-id="a36d8-177">Vous associez un deP à un ensemble de clés stockées dans Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a36d8-177">You associate a DEP with a set of keys stored in Azure Key Vault.</span></span> <span data-ttu-id="a36d8-178">Vous appliquez un deP à toutes vos données dans un emplacement géographique, également appelé géo.</span><span class="sxs-lookup"><span data-stu-id="a36d8-178">You apply a DEP to all of your data in one geographic location, also called a geo.</span></span> <span data-ttu-id="a36d8-179">Si vous utilisez la fonctionnalité multigéogé Office 365, vous pouvez créer une dep par géo avec la possibilité d’utiliser différentes clés par géo.</span><span class="sxs-lookup"><span data-stu-id="a36d8-179">If you use the multi-geo feature of Office 365, you can create one DEP per geo with the capability to use different keys per geo.</span></span> <span data-ttu-id="a36d8-180">Si vous n’utilisez pas multigéogé, vous pouvez en créer un dans votre organisation pour l’utiliser avec les fichiers SharePoint Online, OneDrive Entreprise et Teams.</span><span class="sxs-lookup"><span data-stu-id="a36d8-180">If you aren't using multi-geo, you can create one DEP in your organization for use with SharePoint Online, OneDrive for Business, and Teams files.</span></span> <span data-ttu-id="a36d8-181">Microsoft 365 utilise les clés identifiées dans la PD DEP pour chiffrer vos données dans cette géo.</span><span class="sxs-lookup"><span data-stu-id="a36d8-181">Microsoft 365 uses the keys identified in the DEP to encrypt your data in that geo.</span></span> <span data-ttu-id="a36d8-182">Pour créer le PED, vous avez besoin des URIs de coffre de clés que vous avez obtenus lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="a36d8-182">To create the DEP, you need the Key Vault URIs you obtained during setup.</span></span> <span data-ttu-id="a36d8-183">Pour plus d’informations, [voir Obtenir l’URI de chaque clé Azure Key Vault.](customer-key-set-up.md#obtain-the-uri-for-each-azure-key-vault-key)</span><span class="sxs-lookup"><span data-stu-id="a36d8-183">For information, see [Obtain the URI for each Azure Key Vault key](customer-key-set-up.md#obtain-the-uri-for-each-azure-key-vault-key).</span></span>
  
<span data-ttu-id="a36d8-184">N’oubliez pas !</span><span class="sxs-lookup"><span data-stu-id="a36d8-184">Remember!</span></span> <span data-ttu-id="a36d8-185">Lorsque vous créez un deP, vous spécifiez deux clés dans deux coffres de clés Azure différents.</span><span class="sxs-lookup"><span data-stu-id="a36d8-185">When you create a DEP, you specify two keys in two different Azure Key Vaults.</span></span> <span data-ttu-id="a36d8-186">Créez ces clés dans deux régions Azure distinctes pour assurer la redondance géographique.</span><span class="sxs-lookup"><span data-stu-id="a36d8-186">Create these keys in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="a36d8-187">Pour créer un dep, vous devez vous connecter à distance à SharePoint Online à l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a36d8-187">To create a DEP, you need to remotely connect to SharePoint Online by using Windows PowerShell.</span></span>
  
1. <span data-ttu-id="a36d8-188">Sur votre ordinateur local, à l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, Connecter [à SharePoint Online PowerShell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?preserve-view=true&view=sharepoint-ps).</span><span class="sxs-lookup"><span data-stu-id="a36d8-188">On your local computer, using a work or school account that has global administrator permissions in your organization, [Connect to SharePoint Online PowerShell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?preserve-view=true&view=sharepoint-ps).</span></span>

2. <span data-ttu-id="a36d8-189">Dans l’Microsoft Office SharePoint Online Management Shell, exécutez la cmdlet Register-SPODataEncryptionPolicy suivante :</span><span class="sxs-lookup"><span data-stu-id="a36d8-189">In the Microsoft SharePoint Online Management Shell, run the Register-SPODataEncryptionPolicy cmdlet as follows:</span></span>

   ```powershell
   Register-SPODataEncryptionPolicy -Identity <adminSiteCollectionURL> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   <span data-ttu-id="a36d8-190">Exemple :</span><span class="sxs-lookup"><span data-stu-id="a36d8-190">Example:</span></span>
  
   ```powershell
   Register-SPODataEncryptionPolicy -Identity https://contoso.sharepoint.com -PrimaryKeyVaultName 'stageRG3vault' -PrimaryKeyName 'SPKey3' -PrimaryKeyVersion 'f635a23bd4a44b9996ff6aadd88d42ba' -SecondaryKeyVaultName 'stageRG5vault' -SecondaryKeyName 'SPKey5' -SecondaryKeyVersion '2b3e8f1d754f438dacdec1f0945f251a’
   ```

   <span data-ttu-id="a36d8-191">Lorsque vous inscrivez la PD DEP, le chiffrement commence sur les données de la géo.</span><span class="sxs-lookup"><span data-stu-id="a36d8-191">When you register the DEP, encryption begins on the data in the geo.</span></span> <span data-ttu-id="a36d8-192">Le chiffrement peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="a36d8-192">Encryption can take some time.</span></span> <span data-ttu-id="a36d8-193">Pour plus d’informations sur l’utilisation de ce paramètre, voir [Register-SPODataEncryptionPolicy](/powershell/module/sharepoint-online/register-spodataencryptionpolicy?preserve-view=true&view=sharepoint-ps).</span><span class="sxs-lookup"><span data-stu-id="a36d8-193">For more information on using this parameter, see [Register-SPODataEncryptionPolicy](/powershell/module/sharepoint-online/register-spodataencryptionpolicy?preserve-view=true&view=sharepoint-ps).</span></span>

### <a name="view-the-deps-youve-created-for-exchange-online-mailboxes"></a><span data-ttu-id="a36d8-194">Afficher les deps que vous avez créés pour Exchange Online boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="a36d8-194">View the DEPs you've created for Exchange Online mailboxes</span></span>

<span data-ttu-id="a36d8-195">Pour afficher la liste de tous les dep que vous avez créés pour les boîtes aux lettres, utilisez la cmdlet PowerShell Get-DataEncryptionPolicy'accès.</span><span class="sxs-lookup"><span data-stu-id="a36d8-195">To view a list of all the DEPs you've created for mailboxes, use the Get-DataEncryptionPolicy PowerShell cmdlet.</span></span>

1. <span data-ttu-id="a36d8-196">À l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, connectez-vous [Exchange Online PowerShell.](/powershell/exchange/connect-to-exchange-online-powershell)</span><span class="sxs-lookup"><span data-stu-id="a36d8-196">Using a work or school account that has global administrator permissions in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="a36d8-197">Pour retourner tous les DDP de votre organisation, exécutez l'Get-DataEncryptionPolicy cmdlet sans aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a36d8-197">To return all DEPs in your organization, run the Get-DataEncryptionPolicy cmdlet without any parameters.</span></span>

   ```powershell
   Get-DataEncryptionPolicy
   ```

   <span data-ttu-id="a36d8-198">Pour plus d’informations sur la cmdlet Get-DataEncryptionPolicy, voir [Get-DataEncryptionPolicy](/powershell/module/exchange/get-dataencryptionpolicy).</span><span class="sxs-lookup"><span data-stu-id="a36d8-198">For more information about the Get-DataEncryptionPolicy cmdlet, see [Get-DataEncryptionPolicy](/powershell/module/exchange/get-dataencryptionpolicy).</span></span>

### <a name="assign-a-dep-before-you-migrate-a-mailbox-to-the-cloud"></a><span data-ttu-id="a36d8-199">Affecter un dep avant de migrer une boîte aux lettres vers le cloud</span><span class="sxs-lookup"><span data-stu-id="a36d8-199">Assign a DEP before you migrate a mailbox to the cloud</span></span>

<span data-ttu-id="a36d8-200">Lorsque vous affectez le deP, Microsoft 365 chiffre le contenu de la boîte aux lettres à l’aide de la dep affectée lors de la migration.</span><span class="sxs-lookup"><span data-stu-id="a36d8-200">When you assign the DEP, Microsoft 365 encrypts the contents of the mailbox using the assigned DEP during the migration.</span></span> <span data-ttu-id="a36d8-201">Ce processus est plus efficace que la migration de la boîte aux lettres, l’affectation du dep, puis l’attente du chiffrement, ce qui peut prendre des heures, voire des jours.</span><span class="sxs-lookup"><span data-stu-id="a36d8-201">This process is more efficient than migrating the mailbox, assigning the DEP, and then waiting for encryption to take place, which can take hours or possibly days.</span></span>

<span data-ttu-id="a36d8-202">Pour affecter un dep à une boîte aux lettres avant de la migrer vers Office 365, exécutez la cmdlet Set-MailUser dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="a36d8-202">To assign a DEP to a mailbox before you migrate it to Office 365, run the Set-MailUser cmdlet in Exchange Online PowerShell:</span></span>

1. <span data-ttu-id="a36d8-203">À l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, connectez-vous [Exchange Online PowerShell.](/powershell/exchange/connect-to-exchange-online-powershell)</span><span class="sxs-lookup"><span data-stu-id="a36d8-203">Using a work or school account that has global administrator permissions in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="a36d8-204">Exécutez lSet-MailUser cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a36d8-204">Run the Set-MailUser cmdlet.</span></span>

   ```powershell
   Set-MailUser -Identity <GeneralMailboxOrMailUserIdParameter> -DataEncryptionPolicy <DataEncryptionPolicyIdParameter>
   ```

   <span data-ttu-id="a36d8-205">Où *GeneralMailboxOrMailUserIdParameter* spécifie une boîte aux lettres et *DataEncryptionPolicyIdParameter* est l’ID du deP.</span><span class="sxs-lookup"><span data-stu-id="a36d8-205">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox, and *DataEncryptionPolicyIdParameter* is the ID of the DEP.</span></span> <span data-ttu-id="a36d8-206">Pour plus d’informations sur la cmdlet Set-MailUser, voir [Set-MailUser](/powershell/module/exchange/set-mailuser).</span><span class="sxs-lookup"><span data-stu-id="a36d8-206">For more information about the Set-MailUser cmdlet, see [Set-MailUser](/powershell/module/exchange/set-mailuser).</span></span>

### <a name="determine-the-dep-assigned-to-a-mailbox"></a><span data-ttu-id="a36d8-207">Déterminer le deP affecté à une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="a36d8-207">Determine the DEP assigned to a mailbox</span></span>

<span data-ttu-id="a36d8-208">Pour déterminer le deP affecté à une boîte aux lettres, utilisez la cmdlet Get-MailboxStatistics de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a36d8-208">To determine the DEP assigned to a mailbox, use the Get-MailboxStatistics cmdlet.</span></span> <span data-ttu-id="a36d8-209">La cmdlet renvoie un identificateur unique (GUID).</span><span class="sxs-lookup"><span data-stu-id="a36d8-209">The cmdlet returns a unique identifier (GUID).</span></span>
  
1. <span data-ttu-id="a36d8-210">À l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, connectez-vous [Exchange Online PowerShell.](/powershell/exchange/connect-to-exchange-online-powershell)</span><span class="sxs-lookup"><span data-stu-id="a36d8-210">Using a work or school account that has global administrator permissions in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

   ```powershell
   Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
   ```

   <span data-ttu-id="a36d8-211">Où *GeneralMailboxOrMailUserIdParameter* spécifie une boîte aux lettres et DataEncryptionPolicyID renvoie le GUID du deP.</span><span class="sxs-lookup"><span data-stu-id="a36d8-211">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox and DataEncryptionPolicyID returns the GUID of the DEP.</span></span> <span data-ttu-id="a36d8-212">Pour plus d’informations sur Get-MailboxStatistics cmdlet, [voir Get-MailboxStatistics](/powershell/module/exchange/get-mailboxstatistics).</span><span class="sxs-lookup"><span data-stu-id="a36d8-212">For more information about the Get-MailboxStatistics cmdlet, see [Get-MailboxStatistics](/powershell/module/exchange/get-mailboxstatistics).</span></span>
  
2. <span data-ttu-id="a36d8-213">Exécutez Get-DataEncryptionPolicy cmdlet pour connaître le nom convivial du dep auquel la boîte aux lettres est affectée.</span><span class="sxs-lookup"><span data-stu-id="a36d8-213">Run the Get-DataEncryptionPolicy cmdlet to find out the friendly name of the DEP to which the mailbox is assigned.</span></span>
  
   ```powershell
   Get-DataEncryptionPolicy <GUID>
   ```

   <span data-ttu-id="a36d8-214">Où *GUID est* le GUID renvoyé par l'Get-MailboxStatistics cmdlet à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="a36d8-214">Where *GUID* is the GUID returned by the Get-MailboxStatistics cmdlet in the previous step.</span></span>

## <a name="verify-that-customer-key-has-finished-encryption"></a><span data-ttu-id="a36d8-215">Vérifier que le chiffrement de la clé client est terminé</span><span class="sxs-lookup"><span data-stu-id="a36d8-215">Verify that Customer Key has finished encryption</span></span>

<span data-ttu-id="a36d8-216">Que vous avez inscrit une clé client, affecté un nouveau dep ou migré une boîte aux lettres, utilisez les étapes de cette section pour vous assurer que le chiffrement est terminé.</span><span class="sxs-lookup"><span data-stu-id="a36d8-216">Whether you've rolled a Customer Key, assigned a new DEP, or migrated a mailbox, use the steps in this section to ensure that encryption completes.</span></span>

### <a name="verify-encryption-completes-for-exchange-online-mailboxes"></a><span data-ttu-id="a36d8-217">Vérifier que le chiffrement est terminé pour Exchange Online boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="a36d8-217">Verify encryption completes for Exchange Online mailboxes</span></span>

<span data-ttu-id="a36d8-218">Le chiffrement d’une boîte aux lettres peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="a36d8-218">Encrypting a mailbox can take some time.</span></span> <span data-ttu-id="a36d8-219">Pour le premier chiffrement, la boîte aux lettres doit également passer complètement d’une base de données à une autre pour que le service puisse chiffrer la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a36d8-219">For first time encryption, the mailbox must also completely move from one database to another before the service can encrypt the mailbox.</span></span>
  
<span data-ttu-id="a36d8-220">Utilisez la cmdlet Get-MailboxStatistics pour déterminer si une boîte aux lettres est chiffrée.</span><span class="sxs-lookup"><span data-stu-id="a36d8-220">Use the Get-MailboxStatistics cmdlet to determine if a mailbox is encrypted.</span></span>
  
```powershell
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

<span data-ttu-id="a36d8-221">La propriété IsEncrypted renvoie la valeur **true** si la boîte aux lettres est chiffrée et la valeur **false** si la boîte aux lettres n’est pas chiffrée.</span><span class="sxs-lookup"><span data-stu-id="a36d8-221">The IsEncrypted property returns a value of **true** if the mailbox is encrypted and a value of **false** if the mailbox isn't encrypted.</span></span> <span data-ttu-id="a36d8-222">Le temps de déplacement des boîtes aux lettres dépend du nombre de boîtes aux lettres à laquelle vous attribuez une dep pour la première fois et de la taille des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a36d8-222">The time to complete mailbox moves depends on the number of mailboxes to which you assign a DEP for the first time, and the size of the mailboxes.</span></span> <span data-ttu-id="a36d8-223">Si les boîtes aux lettres n’ont pas été chiffrées après une semaine à partir de l’heure à partir de la PED, contactez Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a36d8-223">If the mailboxes haven't been encrypted after a week from the time you assigned the DEP, contact Microsoft.</span></span>

<span data-ttu-id="a36d8-224">La cmdlet New-MoveRequest n’est plus disponible pour les déplacements de boîtes aux lettres locaux.</span><span class="sxs-lookup"><span data-stu-id="a36d8-224">The New-MoveRequest cmdlet is no longer available for local mailbox moves.</span></span> <span data-ttu-id="a36d8-225">Pour plus [d’informations,](https://techcommunity.microsoft.com/t5/exchange-team-blog/disabling-new-moverequest-for-local-mailbox-moves/bc-p/1332141) reportez-vous à cette annonce.</span><span class="sxs-lookup"><span data-stu-id="a36d8-225">Refer to [this announcement](https://techcommunity.microsoft.com/t5/exchange-team-blog/disabling-new-moverequest-for-local-mailbox-moves/bc-p/1332141) for additional information.</span></span>

### <a name="verify-encryption-completes-for-sharepoint-online-onedrive-for-business-and-teams-files"></a><span data-ttu-id="a36d8-226">Vérifier que le chiffrement est terminé pour SharePoint online, OneDrive Entreprise et Teams fichiers</span><span class="sxs-lookup"><span data-stu-id="a36d8-226">Verify encryption completes for SharePoint Online, OneDrive for Business, and Teams files</span></span>

<span data-ttu-id="a36d8-227">Vérifiez l’état du chiffrement en exécutant la cmdlet Get-SPODataEncryptionPolicy comme suit :</span><span class="sxs-lookup"><span data-stu-id="a36d8-227">Check on the status of encryption by running the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>

```PowerShell
   Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

<span data-ttu-id="a36d8-228">Le résultat de cette cmdlet inclut :</span><span class="sxs-lookup"><span data-stu-id="a36d8-228">The output from this cmdlet includes:</span></span>
  
- <span data-ttu-id="a36d8-229">URI de la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="a36d8-229">The URI of the primary key.</span></span>

- <span data-ttu-id="a36d8-230">URI de la clé secondaire.</span><span class="sxs-lookup"><span data-stu-id="a36d8-230">The URI of the secondary key.</span></span>

- <span data-ttu-id="a36d8-231">État du chiffrement pour la géo.</span><span class="sxs-lookup"><span data-stu-id="a36d8-231">The encryption status for the geo.</span></span> <span data-ttu-id="a36d8-232">Les états possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="a36d8-232">Possible states include:</span></span>

  - <span data-ttu-id="a36d8-233">**Non enregistré :** Le chiffrement de clé client n’a pas encore été appliqué.</span><span class="sxs-lookup"><span data-stu-id="a36d8-233">**Unregistered:** Customer Key encryption has not yet been applied.</span></span>

  - <span data-ttu-id="a36d8-234">**Inscription :** Le chiffrement de la clé client a été appliqué et vos fichiers sont en cours de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="a36d8-234">**Registering:** Customer Key encryption has been applied and your files are in the process of being encrypted.</span></span> <span data-ttu-id="a36d8-235">Si la clé de la géo est inscrite, des informations sur le pourcentage de sites de la géo sont également affichées, ce qui vous permet de surveiller la progression du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="a36d8-235">If the key for the geo is registering, you'll also be shown information on what percentage of sites in the geo are complete so that you can monitor encryption progress.</span></span>

  - <span data-ttu-id="a36d8-236">**Inscrit :** Le chiffrement de la clé client a été appliqué et tous les fichiers de tous les sites ont été chiffrés.</span><span class="sxs-lookup"><span data-stu-id="a36d8-236">**Registered:** Customer Key encryption has been applied, and all files in all sites have been encrypted.</span></span>

  - <span data-ttu-id="a36d8-237">**Déploiement :** Un roulis de touches est en cours.</span><span class="sxs-lookup"><span data-stu-id="a36d8-237">**Rolling:** A key roll is in progress.</span></span> <span data-ttu-id="a36d8-238">Si la clé de la géo est en cours de déploiement, vous verrez également des informations sur le pourcentage de sites qui ont terminé l’opération de déploiement de clé afin de pouvoir surveiller la progression.</span><span class="sxs-lookup"><span data-stu-id="a36d8-238">If the key for the geo is rolling, you'll also be shown information on what percentage of sites have completed the key roll operation so that you can monitor progress.</span></span>

## <a name="get-details-about-deps-you-use-with-multiple-workloads"></a><span data-ttu-id="a36d8-239">Obtenir des détails sur les PD DEP que vous utilisez avec plusieurs charges de travail</span><span class="sxs-lookup"><span data-stu-id="a36d8-239">Get details about DEPs you use with multiple workloads</span></span>

<span data-ttu-id="a36d8-240">Pour obtenir des détails sur tous les dep que vous avez créés pour une utilisation avec plusieurs charges de travail, complétez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a36d8-240">To get details about all of the DEPs you've created to use with multiple workloads, complete these steps:</span></span>

1. <span data-ttu-id="a36d8-241">Sur votre ordinateur local, à l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général ou d’administrateur de conformité dans votre organisation, connectez-vous à [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) dans une fenêtre Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a36d8-241">On your local computer, using a work or school account that has global administrator or compliance admin permissions in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) in a Windows PowerShell window.</span></span>

   - <span data-ttu-id="a36d8-242">Pour renvoyer la liste de tous les dep de charges de travail multiples dans l’organisation, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="a36d8-242">To return the list of all multi-workload DEPs in the organization, run this command.</span></span>

     ```powershell
        Get-M365DataAtRestEncryptionPolicy
     ```

   - <span data-ttu-id="a36d8-243">Pour renvoyer des détails sur un deP spécifique, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="a36d8-243">To return details about a specific DEP, run this command.</span></span> <span data-ttu-id="a36d8-244">Cet exemple renvoie des informations détaillées sur la PED nommée « Contoso_Global ».</span><span class="sxs-lookup"><span data-stu-id="a36d8-244">This example returns detailed information for the DEP named "Contoso_Global".</span></span>

     ```powershell
        Get-M365DataAtRestEncryptionPolicy -Identity "Contoso_Global"
     ```

## <a name="get-multi-workload-dep-assignment-information"></a><span data-ttu-id="a36d8-245">Obtenir des informations sur les affectations PDN à charges multiples</span><span class="sxs-lookup"><span data-stu-id="a36d8-245">Get multi-workload DEP assignment information</span></span>

<span data-ttu-id="a36d8-246">Pour savoir quel deP est actuellement affecté à votre client, suivez ces étapes.</span><span class="sxs-lookup"><span data-stu-id="a36d8-246">To find out which DEP is currently assigned to your tenant, follow these steps.</span></span> 

1. <span data-ttu-id="a36d8-247">Sur votre ordinateur local, à l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général ou d’administrateur de conformité dans votre organisation, connectez-vous à [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) dans une fenêtre Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a36d8-247">On your local computer, using a work or school account that has global administrator or compliance admin permissions in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) in a Windows PowerShell window.</span></span>

2. <span data-ttu-id="a36d8-248">Tapez cette commande.</span><span class="sxs-lookup"><span data-stu-id="a36d8-248">Type this command.</span></span>

   ```powershell
      Get-M365DataAtRestEncryptionPolicyAssignment
   ```

## <a name="disable-a-multi-workload-dep"></a><span data-ttu-id="a36d8-249">Désactiver un PD DEP à charges multiples</span><span class="sxs-lookup"><span data-stu-id="a36d8-249">Disable a multi-workload DEP</span></span>

<span data-ttu-id="a36d8-250">Avant de désactiver une PD DEP à charges multiples, désattribuez-la des charges de travail de votre client.</span><span class="sxs-lookup"><span data-stu-id="a36d8-250">Before you disable a multi-workload DEP, unassign the DEP from workloads in your tenant.</span></span> <span data-ttu-id="a36d8-251">Pour désactiver un deP utilisé avec plusieurs charges de travail, effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a36d8-251">To disable a DEP used with multiple workloads, complete these steps:</span></span>

1. <span data-ttu-id="a36d8-252">Sur votre ordinateur local, à l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général ou d’administrateur de conformité dans votre organisation, connectez-vous à [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) dans une fenêtre Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a36d8-252">On your local computer, using a work or school account that has global administrator or compliance admin permissions in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) in a Windows PowerShell window.</span></span>

2. <span data-ttu-id="a36d8-253">Exécutez lSet-M365DataAtRestEncryptionPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a36d8-253">Run the Set-M365DataAtRestEncryptionPolicy cmdlet.</span></span>
  
   ```powershell
   Set-M365DataAtRestEncryptionPolicy -[Identity] "PolicyName" -Enabled $false
   ```

<span data-ttu-id="a36d8-254">Où *PolicyName est* le nom ou l’ID unique de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="a36d8-254">Where *PolicyName* is the name or unique ID of the policy.</span></span> <span data-ttu-id="a36d8-255">Par exemple, Contoso_Global.</span><span class="sxs-lookup"><span data-stu-id="a36d8-255">For example, Contoso_Global.</span></span>

<span data-ttu-id="a36d8-256">Exemple :</span><span class="sxs-lookup"><span data-stu-id="a36d8-256">Example:</span></span>

```powershell
Set-M365DataAtRestEncryptionPolicy -Identity "Contoso_Global" -Enabled $false
```

## <a name="restore-azure-key-vault-keys"></a><span data-ttu-id="a36d8-257">Restaurer les clés Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a36d8-257">Restore Azure Key Vault keys</span></span>

<span data-ttu-id="a36d8-258">Avant d’effectuer une restauration, utilisez les fonctionnalités de récupération fournies par la suppression soft.</span><span class="sxs-lookup"><span data-stu-id="a36d8-258">Before performing a restore, use the recovery capabilities provided by soft delete.</span></span> <span data-ttu-id="a36d8-259">Toutes les clés utilisées avec la clé client doivent être activées pour la suppression possible.</span><span class="sxs-lookup"><span data-stu-id="a36d8-259">All keys that are used with Customer Key are required to have soft delete enabled.</span></span> <span data-ttu-id="a36d8-260">La suppression souple agit comme une corbeille et permet une récupération pendant 90 jours sans avoir à le restaurer.</span><span class="sxs-lookup"><span data-stu-id="a36d8-260">Soft delete acts like a recycle bin and allows recovery for up to 90 days without the need to restore.</span></span> <span data-ttu-id="a36d8-261">La restauration ne doit être nécessaire que dans des circonstances extrêmes ou inhabituelles, par exemple si la clé ou le coffre de clés est perdu.</span><span class="sxs-lookup"><span data-stu-id="a36d8-261">Restore should only be required in extreme or unusual circumstances, for example if the key or key vault is lost.</span></span> <span data-ttu-id="a36d8-262">Si vous devez restaurer une clé à utiliser avec la clé client, dans Azure PowerShell, exécutez la cmdlet Restore-AzureKeyVaultKey comme suit :</span><span class="sxs-lookup"><span data-stu-id="a36d8-262">If you must restore a key for use with Customer Key, in Azure PowerShell, run the Restore-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```powershell
Restore-AzKeyVaultKey -VaultName <vault name> -InputFile <filename>
```

<span data-ttu-id="a36d8-263">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a36d8-263">For example:</span></span>
  
```powershell
Restore-AzKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

<span data-ttu-id="a36d8-264">Si le coffre de clés contient déjà une clé du même nom, l’opération de restauration échoue.</span><span class="sxs-lookup"><span data-stu-id="a36d8-264">If the key vault already contains a key with the same name, the restore operation fails.</span></span> <span data-ttu-id="a36d8-265">Restore-AzKeyVaultKey toutes les versions clés et toutes les métadonnées de la clé, y compris le nom de la clé.</span><span class="sxs-lookup"><span data-stu-id="a36d8-265">Restore-AzKeyVaultKey restores all key versions and all metadata for the key including the key name.</span></span>
  
## <a name="manage-key-vault-permissions"></a><span data-ttu-id="a36d8-266">Gérer les autorisations de coffre de clés</span><span class="sxs-lookup"><span data-stu-id="a36d8-266">Manage key vault permissions</span></span>

<span data-ttu-id="a36d8-267">Plusieurs cmdlets sont disponibles qui vous permettent d’afficher et, si nécessaire, de supprimer les autorisations de coffre de clés.</span><span class="sxs-lookup"><span data-stu-id="a36d8-267">Several cmdlets are available that enable you to view and, if necessary, remove key vault permissions.</span></span> <span data-ttu-id="a36d8-268">Vous devrez peut-être supprimer des autorisations, par exemple, lorsqu’un employé quitte l’équipe.</span><span class="sxs-lookup"><span data-stu-id="a36d8-268">You might need to remove permissions, for example, when an employee leaves the team.</span></span> <span data-ttu-id="a36d8-269">Pour chacune de ces tâches, vous utiliserez Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a36d8-269">For each of these tasks, you will use Azure PowerShell.</span></span> <span data-ttu-id="a36d8-270">Pour plus d’informations Azure PowerShell, voir [Vue d’ensemble Azure PowerShell](/powershell/azure/).</span><span class="sxs-lookup"><span data-stu-id="a36d8-270">For information about Azure PowerShell, see [Overview of Azure PowerShell](/powershell/azure/).</span></span>

<span data-ttu-id="a36d8-271">Pour afficher les autorisations de coffre de clés, exécutez Get-AzKeyVault cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a36d8-271">To view key vault permissions, run the Get-AzKeyVault cmdlet.</span></span>

```powershell
Get-AzKeyVault -VaultName <vault name>
```

<span data-ttu-id="a36d8-272">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a36d8-272">For example:</span></span>

```powershell
Get-AzKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

<span data-ttu-id="a36d8-273">Pour supprimer les autorisations d’un administrateur, exécutez l'Remove-AzKeyVaultAccessPolicy cmdlet :</span><span class="sxs-lookup"><span data-stu-id="a36d8-273">To remove an administrator's permissions, run the Remove-AzKeyVaultAccessPolicy cmdlet:</span></span>
  
```powershell
Remove-AzKeyVaultAccessPolicy -VaultName <vault name> -UserPrincipalName <UPN of user>
```

<span data-ttu-id="a36d8-274">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a36d8-274">For example:</span></span>

```powershell
Remove-AzKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 -UserPrincipalName alice@contoso.com
```

## <a name="roll-back-from-customer-key-to-microsoft-managed-keys"></a><span data-ttu-id="a36d8-275">Revenir de la clé client aux clés gérées Microsoft</span><span class="sxs-lookup"><span data-stu-id="a36d8-275">Roll back from Customer Key to Microsoft managed Keys</span></span>

<span data-ttu-id="a36d8-276">Si vous devez revenir aux clés gérées par Microsoft, vous pouvez le faire.</span><span class="sxs-lookup"><span data-stu-id="a36d8-276">If you need to revert to Microsoft-managed keys, you can.</span></span> <span data-ttu-id="a36d8-277">Lorsque vous déboardez, vos données sont re-chiffrées à l’aide du chiffrement par défaut pris en charge par chaque charge de travail individuelle.</span><span class="sxs-lookup"><span data-stu-id="a36d8-277">When you offboard, your data is re-encrypted using default encryption supported by each individual workload.</span></span> <span data-ttu-id="a36d8-278">Par exemple, Exchange Online prend en charge le chiffrement par défaut à l’aide de clés gérées par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a36d8-278">For example, Exchange Online supports default encryption using Microsoft-managed keys.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a36d8-279">Laboarding n’est pas la même chose qu’une purge de données.</span><span class="sxs-lookup"><span data-stu-id="a36d8-279">Offboarding is not the same as a data purge.</span></span> <span data-ttu-id="a36d8-280">Une purge des données supprime définitivement les données de votre organisation de l’Microsoft 365, ce qui n’est pas le cas de la suppression de l’board.</span><span class="sxs-lookup"><span data-stu-id="a36d8-280">A data purge permanently crypto-deletes your organization's data from Microsoft 365, offboarding does not.</span></span> <span data-ttu-id="a36d8-281">Vous ne pouvez pas effectuer de purge de données pour une stratégie de charge de travail multiple.</span><span class="sxs-lookup"><span data-stu-id="a36d8-281">You can't perform a data purge for a multiple workload policy.</span></span>

<span data-ttu-id="a36d8-282">Si vous décidez de ne plus utiliser la clé client pour affecter des depx de travail multiples, vous devrez joindre le support Microsoft avec une demande de « désintégration » à partir de la clé client.</span><span class="sxs-lookup"><span data-stu-id="a36d8-282">If you decide not to use Customer Key for assigning multi-workload DEPs anymore then you'll need to reach out to Microsoft support with a request to “offboard” from Customer Key.</span></span> <span data-ttu-id="a36d8-283">Demandez à l’équipe de support de déposer une demande de service auprès Microsoft 365'équipe de clé client.</span><span class="sxs-lookup"><span data-stu-id="a36d8-283">Ask the support team to file a service request against Microsoft 365 Customer Key team.</span></span> <span data-ttu-id="a36d8-284">Si vous avez des questions, m365-ck@service.microsoft.com posent des questions.</span><span class="sxs-lookup"><span data-stu-id="a36d8-284">Reach out to m365-ck@service.microsoft.com if you have any questions.</span></span>

<span data-ttu-id="a36d8-285">Si vous ne souhaitez plus chiffrer des boîtes aux lettres individuelles à l’aide de deps au niveau de la boîte aux lettres, vous pouvez désattribuer les DPS de niveau boîte aux lettres de toutes vos boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a36d8-285">If you do not want to encrypt individual mailboxes using mailbox level DEPs anymore, then you can unassign mailbox level DEPs from all your mailboxes.</span></span>

<span data-ttu-id="a36d8-286">Pour désattribuer des DPS de boîte aux lettres, utilisez Set-Mailbox cmdlet PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a36d8-286">To unassign mailbox DEPs, use the Set-Mailbox PowerShell cmdlet.</span></span>

1. <span data-ttu-id="a36d8-287">À l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, connectez-vous [Exchange Online PowerShell.](/powershell/exchange/connect-to-exchange-online-powershell)</span><span class="sxs-lookup"><span data-stu-id="a36d8-287">Using a work or school account that has global administrator permissions in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="a36d8-288">Exécutez lSet-Mailbox cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a36d8-288">Run the Set-Mailbox cmdlet.</span></span>

   ```powershell
   Set-Mailbox -Identity <mailbox> -DataEncryptionPolicy $NULL
   ```

<span data-ttu-id="a36d8-289">L’exécution de cette cmdlet désattribue le dep actuellement affecté et recrypte la boîte aux lettres à l’aide de la dep associée aux clés gérées par Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="a36d8-289">Running this cmdlet unassigns the currently assigned DEP and reencrypts the mailbox using the DEP associated with default Microsoft-managed keys.</span></span> <span data-ttu-id="a36d8-290">Vous ne pouvez pas désattribuer le deP utilisé par les clés gérées microsoft.</span><span class="sxs-lookup"><span data-stu-id="a36d8-290">You can't unassign the DEP used by Microsoft managed keys.</span></span> <span data-ttu-id="a36d8-291">Si vous ne souhaitez pas utiliser de clés gérées par Microsoft, vous pouvez affecter une autre clé client DEP à la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a36d8-291">If you don't want to use Microsoft-managed keys, you can assign another Customer Key DEP to the mailbox.</span></span>

## <a name="revoke-your-keys-and-start-the-data-purge-path-process"></a><span data-ttu-id="a36d8-292">Révoquer vos clés et démarrer le processus de purge des données</span><span class="sxs-lookup"><span data-stu-id="a36d8-292">Revoke your keys and start the data purge path process</span></span>

<span data-ttu-id="a36d8-293">Vous contrôlez la révocation de toutes les clés racine, y compris la clé de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="a36d8-293">You control the revocation of all root keys including the availability key.</span></span> <span data-ttu-id="a36d8-294">La clé client vous permet de contrôler l’aspect de planification de sortie des exigences réglementaires.</span><span class="sxs-lookup"><span data-stu-id="a36d8-294">Customer Key provides control of the exit planning aspect of the regulatory requirements for you.</span></span> <span data-ttu-id="a36d8-295">Si vous décidez de révoquer vos clés pour vider vos données et quitter le service, le service supprime la clé de disponibilité une fois le processus de purge des données terminé.</span><span class="sxs-lookup"><span data-stu-id="a36d8-295">If you decide to revoke your keys to purge your data and exit the service, the service deletes the availability key once the data purge process completes.</span></span> <span data-ttu-id="a36d8-296">Ceci est pris en charge pour les DPS de clé client qui sont affectés à des boîtes aux lettres individuelles.</span><span class="sxs-lookup"><span data-stu-id="a36d8-296">This is supported for Customer Key DEPs that are assigned to individual mailboxes.</span></span>

<span data-ttu-id="a36d8-297">Microsoft 365 audite et valide le chemin de purge des données.</span><span class="sxs-lookup"><span data-stu-id="a36d8-297">Microsoft 365 audits and validates the data purge path.</span></span> <span data-ttu-id="a36d8-298">Pour plus d’informations, voir le rapport SSAE 18 SOC 2 disponible sur le portail [d’confiance des services.](https://servicetrust.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="a36d8-298">For more information, see the SSAE 18 SOC 2 Report available on the [Service Trust Portal](https://servicetrust.microsoft.com/).</span></span> <span data-ttu-id="a36d8-299">En outre, Microsoft recommande les documents suivants :</span><span class="sxs-lookup"><span data-stu-id="a36d8-299">In addition, Microsoft recommends the following documents:</span></span>

- [<span data-ttu-id="a36d8-300">Guide d’évaluation et de conformité des risques pour les institutions financières dans microsoft cloud</span><span class="sxs-lookup"><span data-stu-id="a36d8-300">Risk Assessment and Compliance Guide for Financial Institutions in the Microsoft Cloud</span></span>](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

- [<span data-ttu-id="a36d8-301">Considérations sur la planification de sortie d’O365</span><span class="sxs-lookup"><span data-stu-id="a36d8-301">O365 Exit Planning Considerations</span></span>](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=77ea7ebf-ce1b-4a5f-9972-d2d81a951d99&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

<span data-ttu-id="a36d8-302">La purge de la PDV à charges multiples n’est pas prise en charge Microsoft 365 clé client.</span><span class="sxs-lookup"><span data-stu-id="a36d8-302">Purging of multi-workload DEP is not supported for Microsoft 365 Customer Key.</span></span> <span data-ttu-id="a36d8-303">Le PD DEP à charges multiples est utilisé pour chiffrer des données sur plusieurs charges de travail entre tous les utilisateurs du client.</span><span class="sxs-lookup"><span data-stu-id="a36d8-303">The multi-workload DEP is used to encrypt data across multiple workloads across all tenant users.</span></span> <span data-ttu-id="a36d8-304">La purge de ce type de PDN entraînerait l’in inaccessible des données provenant de plusieurs charges de travail.</span><span class="sxs-lookup"><span data-stu-id="a36d8-304">Purging such DEP would result into data from across multiple workloads become inaccessible.</span></span> <span data-ttu-id="a36d8-305">Si vous décidez de quitter Microsoft 365 services, vous pouvez suivre le chemin d’accès à la suppression du client selon le processus documenté.</span><span class="sxs-lookup"><span data-stu-id="a36d8-305">If you decide to exit Microsoft 365 services altogether then you could pursue the path of tenant deletion per the documented process.</span></span> <span data-ttu-id="a36d8-306">Découvrez [comment supprimer un client dans Azure Active Directoy.](/azure/active-directory/enterprise-users/directory-delete-howto)</span><span class="sxs-lookup"><span data-stu-id="a36d8-306">See [how to delete a tenant in Azure Active Directoy](/azure/active-directory/enterprise-users/directory-delete-howto).</span></span>

### <a name="revoke-your-customer-keys-and-the-availability-key-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="a36d8-307">Révoquer vos clés client et la clé de disponibilité Exchange Online et Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="a36d8-307">Revoke your Customer Keys and the availability key for Exchange Online and Skype for Business</span></span>

<span data-ttu-id="a36d8-308">Lorsque vous lancez le chemin d’accès de purge des données pour Exchange Online et Skype Entreprise, vous définissez une demande de purge permanente des données sur un deP.</span><span class="sxs-lookup"><span data-stu-id="a36d8-308">When you initiate the data purge path for Exchange Online and Skype for Business, you set a permanent data purge request on a DEP.</span></span> <span data-ttu-id="a36d8-309">Cela supprime définitivement les données chiffrées dans les boîtes aux lettres à laquelle ce dep est affecté.</span><span class="sxs-lookup"><span data-stu-id="a36d8-309">Doing so permanently deletes encrypted data within the mailboxes to which that DEP is assigned.</span></span>

<span data-ttu-id="a36d8-310">Étant donné que vous ne pouvez exécuter l’cmdlet PowerShell que sur une seule dep à la fois, envisagez de réaffecter une seule dep à toutes vos boîtes aux lettres avant de lancer le chemin de purge des données.</span><span class="sxs-lookup"><span data-stu-id="a36d8-310">Since you can only run the PowerShell cmdlet against one DEP at a time, consider reassigning a single DEP to all of your mailboxes before you initiate the data purge path.</span></span>

> [!WARNING]
> <span data-ttu-id="a36d8-311">N’utilisez pas le chemin de purge des données pour supprimer un sous-ensemble de vos boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a36d8-311">Do not use the data purge path to delete a subset of your mailboxes.</span></span> <span data-ttu-id="a36d8-312">Ce processus est destiné uniquement aux clients qui quittent le service.</span><span class="sxs-lookup"><span data-stu-id="a36d8-312">This process is only intended for customers who are exiting the service.</span></span>

<span data-ttu-id="a36d8-313">Pour lancer le chemin d’accès de la purge des données, effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a36d8-313">To initiate the data purge path, complete these steps:</span></span>

1. <span data-ttu-id="a36d8-314">Supprimez les autorisations wrap et unwrap pour « O365 Exchange Online » des coffres de clés Azure.</span><span class="sxs-lookup"><span data-stu-id="a36d8-314">Remove wrap and unwrap permissions for "O365 Exchange Online" from Azure Key Vaults.</span></span>

2. <span data-ttu-id="a36d8-315">À l’aide d’un compte professionnel ou scolaire qui dispose de privilèges d’administrateur général dans votre [organisation, connectez-vous Exchange Online PowerShell.](/powershell/exchange/connect-to-exchange-online-powershell)</span><span class="sxs-lookup"><span data-stu-id="a36d8-315">Using a work or school account that has global administrator privileges in your organization, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

3. <span data-ttu-id="a36d8-316">Pour chaque PDE qui contient des boîtes aux lettres à supprimer, exécutez la cmdlet [Set-DataEncryptionPolicy](/powershell/module/exchange/set-dataencryptionpolicy) comme suit.</span><span class="sxs-lookup"><span data-stu-id="a36d8-316">For each DEP that contains mailboxes that you want to delete, run the [Set-DataEncryptionPolicy](/powershell/module/exchange/set-dataencryptionpolicy) cmdlet as follows.</span></span>

    ```powershell
    Set-DataEncryptionPolicy <Policy ID> -PermanentDataPurgeRequested -PermanentDataPurgeReason <Reason> -PermanentDataPurgeContact <ContactName>
    ```

   <span data-ttu-id="a36d8-317">Si la commande échoue, assurez-vous que vous avez supprimé les autorisations Exchange Online des deux clés dans Azure Key Vault, comme indiqué précédemment dans cette tâche.</span><span class="sxs-lookup"><span data-stu-id="a36d8-317">If the command fails, ensure that you've removed the Exchange Online permissions from both keys in Azure Key Vault as specified earlier in this task.</span></span><span data-ttu-id="a36d8-318">Une fois que vous avez définie le commutateur PermanentDataPurgeRequested à l’aide de la cmdlet Set-DataEncryptionPolicy, vous ne pourrez plus affecter ce deP aux boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a36d8-318"> Once you've set the PermanentDataPurgeRequested switch using the Set-DataEncryptionPolicy cmdlet, you'll no longer be able to assign this DEP to mailboxes.</span></span>

4. <span data-ttu-id="a36d8-319">Contactez le support Microsoft et demandez l’eDocument de purge des données.</span><span class="sxs-lookup"><span data-stu-id="a36d8-319">Contact Microsoft support and request the Data Purge eDocument.</span></span>

    <span data-ttu-id="a36d8-320">À votre demande, Microsoft vous envoie un document juridique pour accusé de réception et autoriser la suppression des données.</span><span class="sxs-lookup"><span data-stu-id="a36d8-320">At your request, Microsoft sends you a legal document to acknowledge and authorize data deletion.</span></span> <span data-ttu-id="a36d8-321">La personne de votre organisation qui s’est inscrite en tant qu’approuveur dans l’offre FastTrack lors de l’intégration doit signer ce document.</span><span class="sxs-lookup"><span data-stu-id="a36d8-321">The person in your organization who signed up as an approver in the FastTrack offer during onboarding needs to sign this document.</span></span> <span data-ttu-id="a36d8-322">Normalement, il s’agit d’un cadre supérieur ou d’une autre personne désignée dans votre entreprise qui est légalement autorisé à signer les formalités au nom de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a36d8-322">Normally, this is an executive or other designated person in your company who is legally authorized to sign the paperwork on behalf of your organization.</span></span>

5. <span data-ttu-id="a36d8-323">Une fois que votre représentant a signé le document juridique, renvoyez-le à Microsoft (généralement via une signature eDoc).</span><span class="sxs-lookup"><span data-stu-id="a36d8-323">Once your representative has signed the legal document, return it to Microsoft (usually through an eDoc signature).</span></span>

    <span data-ttu-id="a36d8-324">Une fois que Microsoft a reçu le document juridique, Microsoft exécute des cmdlets pour déclencher la purge des données qui supprime d’abord la stratégie, marque les boîtes aux lettres pour suppression définitive, puis supprime la clé de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="a36d8-324">Once Microsoft receives the legal document, Microsoft runs cmdlets to trigger the data purge which first deletes the policy, marks the mailboxes for permanent deletion, then deletes the availability key.</span></span> <span data-ttu-id="a36d8-325">Une fois le processus de purge des données terminé, les données ont été purgées, sont inaccessibles Exchange Online et ne sont pas récupérables.</span><span class="sxs-lookup"><span data-stu-id="a36d8-325">Once the data purge process completes, the data has been purged, is inaccessible to Exchange Online, and is not recoverable.</span></span>

### <a name="revoke-your-customer-keys-and-the-availability-key-for-sharepoint-online-onedrive-for-business-and-teams-files"></a><span data-ttu-id="a36d8-326">Révoquer vos clés client et la clé de disponibilité pour les fichiers SharePoint Online, OneDrive Entreprise et Teams client</span><span class="sxs-lookup"><span data-stu-id="a36d8-326">Revoke your Customer Keys and the availability key for SharePoint Online, OneDrive for Business, and Teams files</span></span>

<span data-ttu-id="a36d8-327">Pour lancer le chemin d’accès de purge des données pour SharePoint Online, OneDrive Entreprise et Teams fichiers, effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a36d8-327">To initiate the data purge path for SharePoint Online, OneDrive for Business, and Teams files, complete these steps:</span></span>

1. <span data-ttu-id="a36d8-328">Révoquer l’accès à Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a36d8-328">Revoke Azure Key Vault access.</span></span> <span data-ttu-id="a36d8-329">Tous les administrateurs de coffre de clés doivent accepter de révoquer l’accès.</span><span class="sxs-lookup"><span data-stu-id="a36d8-329">All key vault admins must agree to revoke access.</span></span>

   <span data-ttu-id="a36d8-330">Vous ne supprimez pas le coffre de clés Azure pour SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="a36d8-330">You do not delete the Azure Key Vault for SharePoint Online.</span></span> <span data-ttu-id="a36d8-331">Les coffres de clés peuvent être partagés entre plusieurs locataires SharePoint online et de dép.</span><span class="sxs-lookup"><span data-stu-id="a36d8-331">Key vaults may be shared among several SharePoint Online tenants and DEPs.</span></span>

2. <span data-ttu-id="a36d8-332">Contactez Microsoft pour supprimer la clé de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="a36d8-332">Contact Microsoft to delete the availability key.</span></span>

    <span data-ttu-id="a36d8-333">Lorsque vous contactez Microsoft pour supprimer la clé de disponibilité, nous vous envoyons un document juridique.</span><span class="sxs-lookup"><span data-stu-id="a36d8-333">When you contact Microsoft to delete the availability key, we'll send you a legal document.</span></span> <span data-ttu-id="a36d8-334">La personne de votre organisation qui s’est inscrite en tant qu’approuveur dans l’offre FastTrack lors de l’intégration doit signer ce document.</span><span class="sxs-lookup"><span data-stu-id="a36d8-334">The person in your organization who signed up as an approver in the FastTrack offer during onboarding needs to sign this document.</span></span> <span data-ttu-id="a36d8-335">Normalement, il s’agit d’un cadre supérieur ou d’une autre personne désignée de votre entreprise qui est légalement autorisée à signer les formalités au nom de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a36d8-335">Normally, this is an executive or other designated person in your company who's legally authorized to sign the paperwork on behalf of your organization.</span></span>

3. <span data-ttu-id="a36d8-336">Une fois que votre représentant signe le document juridique, renvoyez-le à Microsoft (généralement par le biais d’une signature eDoc).</span><span class="sxs-lookup"><span data-stu-id="a36d8-336">Once your representative signs the legal document, return it to Microsoft (usually through an eDoc signature).</span></span>

   <span data-ttu-id="a36d8-337">Une fois que Microsoft a reçu le document juridique, nous exécuterons des cmdlets pour déclencher la purge des données qui effectue la suppression de chiffrement de la clé de client, de la clé de site et de toutes les clés de document individuelles, ce qui a pour effet de rompre irrévocablement la hiérarchie des clés.</span><span class="sxs-lookup"><span data-stu-id="a36d8-337">Once Microsoft receives the legal document, we run cmdlets to trigger the data purge which performs crypto deletion of the tenant key, site key, and all individual per-document keys, irrevocably breaking the key hierarchy.</span></span> <span data-ttu-id="a36d8-338">Une fois les cmdlets de purge des données terminées, vos données ont été purgées.</span><span class="sxs-lookup"><span data-stu-id="a36d8-338">Once the data purge cmdlets complete, your data has been purged.</span></span>

## <a name="related-articles"></a><span data-ttu-id="a36d8-339">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="a36d8-339">Related articles</span></span>

- [<span data-ttu-id="a36d8-340">Chiffrement du service avec la clé client</span><span class="sxs-lookup"><span data-stu-id="a36d8-340">Service encryption with Customer Key</span></span>](customer-key-overview.md)

- [<span data-ttu-id="a36d8-341">En savoir plus sur la clé de disponibilité</span><span class="sxs-lookup"><span data-stu-id="a36d8-341">Learn about the availability key</span></span>](customer-key-availability-key-understand.md)

- [<span data-ttu-id="a36d8-342">Configurer la clé client</span><span class="sxs-lookup"><span data-stu-id="a36d8-342">Set up Customer Key</span></span>](customer-key-set-up.md)

- [<span data-ttu-id="a36d8-343">Echanger ou alterner entre une clé client ou de disponibilité</span><span class="sxs-lookup"><span data-stu-id="a36d8-343">Roll or rotate a Customer Key or an availability key</span></span>](customer-key-availability-key-roll.md)

- [<span data-ttu-id="a36d8-344">Référentiel sécurisé client</span><span class="sxs-lookup"><span data-stu-id="a36d8-344">Customer Lockbox</span></span>](customer-lockbox-requests.md)

- [<span data-ttu-id="a36d8-345">Chiffrement de service</span><span class="sxs-lookup"><span data-stu-id="a36d8-345">Service Encryption</span></span>](office-365-service-encryption.md)