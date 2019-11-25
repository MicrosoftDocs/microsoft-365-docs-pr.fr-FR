---
title: Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Nouvelles fonctionnalités de chiffrement de messages Office 365 basées sur Azure Information Protection, votre organisation peut utiliser une communication de messagerie protégée avec des personnes à l’intérieur et à l’extérieur de votre organisation. Les nouvelles fonctionnalités OME fonctionnent avec les autres organisations Office 365, Outlook.com, Gmail et d’autres services de messagerie.
ms.openlocfilehash: c772151250d30e62a3f2689df5cd853536af3ede
ms.sourcegitcommit: 1c962bd0d51dc12419c4e6e393bb734c972b7e38
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2019
ms.locfileid: "39218733"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a><span data-ttu-id="93ba2-104">Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="93ba2-104">Set up new Office 365 Message Encryption capabilities</span></span>

<span data-ttu-id="93ba2-105">Les nouvelles fonctionnalités de chiffrement de messages Office 365 (OME) permettent aux organisations de partager des courriers électroniques protégés avec n’importe quel appareil.</span><span class="sxs-lookup"><span data-stu-id="93ba2-105">The new Office 365 Message Encryption (OME) capabilities allow organizations to share protected email with anyone on any device.</span></span> <span data-ttu-id="93ba2-106">Les utilisateurs peuvent échanger des messages protégés avec d’autres organisations Office 365, ainsi que des clients non-Office 365 à l’aide de Outlook.com, Gmail et d’autres services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="93ba2-106">Users can exchange protected messages with other Office 365 organizations, as well as non-Office 365 customers using Outlook.com, Gmail, and other email services.</span></span>

<span data-ttu-id="93ba2-107">Suivez les étapes ci-dessous pour vous assurer que les nouvelles fonctionnalités OME sont disponibles dans votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="93ba2-107">Follow the steps below to ensure that the new OME capabilities are available in your Office 365 organization.</span></span>

## <a name="verify-that-azure-rights-management-is-active"></a><span data-ttu-id="93ba2-108">Vérifiez que Azure Rights Management est activé.</span><span class="sxs-lookup"><span data-stu-id="93ba2-108">Verify that Azure Rights Management is active</span></span>

<span data-ttu-id="93ba2-109">Les nouvelles fonctionnalités OME tirent parti des fonctionnalités de protection dans [Azure Rights Management Services (Azure RMS)](https://docs.microsoft.com/azure/information-protection/what-is-information-protection), technologie utilisée par [Azure Information Protection](https://docs.microsoft.com/azure/information-protection/what-is-azure-rms) pour protéger les messages électroniques et les documents via les contrôles d’accès et de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="93ba2-109">The new OME capabilities leverage the protection features in [Azure Rights Management Services (Azure RMS)](https://docs.microsoft.com/azure/information-protection/what-is-information-protection), the technology used by [Azure Information Protection](https://docs.microsoft.com/azure/information-protection/what-is-azure-rms) to protect emails and documents via encryption and access controls.</span></span>

<span data-ttu-id="93ba2-110">La seule condition préalable à l’utilisation des nouvelles fonctionnalités OME est qu’[Azure Rights Management](https://docs.microsoft.com/azure/information-protection/what-is-azure-rms) doit être activé dans le client de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="93ba2-110">The only prerequisite for using the new OME capabilities is that [Azure Rights Management](https://docs.microsoft.com/azure/information-protection/what-is-azure-rms) must be activated in your organization's tenant.</span></span> <span data-ttu-id="93ba2-111">Si c’est le cas, Office 365 active les nouvelles fonctionnalités OME automatiquement et vous n’avez rien à faire.</span><span class="sxs-lookup"><span data-stu-id="93ba2-111">If it is, Office 365 activates the new OME capabilities automatically and you don't need to do anything.</span></span>

<span data-ttu-id="93ba2-112">Azure RMS est également activé automatiquement pour la plupart des offres éligibles, de sorte que vous n’avez probablement pas besoin d’effectuer quoi que ce soit à cet égard.</span><span class="sxs-lookup"><span data-stu-id="93ba2-112">Azure RMS is also activated automatically for most eligible plans, so you probably don't have to do anything in this regard either.</span></span> <span data-ttu-id="93ba2-113">Pour plus d’informations, reportez-vous à [Activation d’Azure Rights Management](https://docs.microsoft.com/azure/information-protection/activate-service).</span><span class="sxs-lookup"><span data-stu-id="93ba2-113">See [Activating Azure Rights Management](https://docs.microsoft.com/azure/information-protection/activate-service) for more information.</span></span>

>[!IMPORTANT]
><span data-ttu-id="93ba2-114">Si vous utilisez Active Directory Rights Management Services (AD RMS) avec Exchange Online, vous devez [migrer vers Azure Information Protection](https://docs.microsoft.com/azure/information-protection/migrate-from-ad-rms-to-azure-rms) avant de pouvoir utiliser les nouvelles fonctionnalités OME.</span><span class="sxs-lookup"><span data-stu-id="93ba2-114">If you use Active Directory Rights Management service (AD RMS) with Exchange Online, you need to [migrate to Azure Information Protection](https://docs.microsoft.com/azure/information-protection/migrate-from-ad-rms-to-azure-rms) before you can use the new OME capabilities.</span></span> <span data-ttu-id="93ba2-115">OME n’est pas compatible avec AD RMS.</span><span class="sxs-lookup"><span data-stu-id="93ba2-115">OME is not compatible with AD RMS.</span></span>  

<span data-ttu-id="93ba2-116">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="93ba2-116">For more information, see:</span></span>

- <span data-ttu-id="93ba2-117">[De quels abonnements ai-je besoin pour utiliser les nouvelles fonctionnalités OME ?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) pour vérifier si votre plan d’abonnement inclut Azure Information Protection (qui inclut les fonctionnalités Azure RMS).</span><span class="sxs-lookup"><span data-stu-id="93ba2-117">[What subscriptions do I need to use the new OME capabilities?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) to check whether your subscription plan includes Azure Information Protection (which includes Azure RMS functionality).</span></span>
- <span data-ttu-id="93ba2-118">[Azure Information Protection](https://azure.microsoft.com/services/information-protection/) pour plus d’informations sur l’achat d’un abonnement éligible.</span><span class="sxs-lookup"><span data-stu-id="93ba2-118">[Azure Information Protection](https://azure.microsoft.com/services/information-protection/) for information about purchasing an eligible subscription.</span></span>  

### <a name="manually-activating-azure-rights-management"></a><span data-ttu-id="93ba2-119">Activation manuelle d’Azure Rights Management</span><span class="sxs-lookup"><span data-stu-id="93ba2-119">Manually activating Azure Rights Management</span></span>

<span data-ttu-id="93ba2-120">Si vous avez désactivé Azure RMS, ou si le service n’a pas été automatiquement activé pour une raison quelconque, vous pouvez l’activer manuellement dans le :</span><span class="sxs-lookup"><span data-stu-id="93ba2-120">If you disabled Azure RMS, or if it was not automatically activated for any reason, you can activate it manually in the:</span></span>

- <span data-ttu-id="93ba2-121">**Centre d’administration Microsoft 365** : reportez-vous à [Comment activer Azure Rights Management à partir du centre d’administration](https://docs.microsoft.com/azure/information-protection/activate-office365) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="93ba2-121">**Microsoft 365 admin center**: See [How to activate Azure Rights Management from the admin center](https://docs.microsoft.com/azure/information-protection/activate-office365) for instructions.</span></span>
- <span data-ttu-id="93ba2-122">**Portail Azure** : reportez-vous à [Comment activer Azure Rights Management à partir du portail Azure](https://docs.microsoft.com/azure/information-protection/activate-azure) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="93ba2-122">**Azure portal**: See [How to activate Azure Rights Management from the Azure portal](https://docs.microsoft.com/azure/information-protection/activate-azure) for instructions.</span></span>

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a><span data-ttu-id="93ba2-123">Configurer la gestion de votre clé de client Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="93ba2-123">Configure management of your Azure Information Protection tenant key</span></span>

<span data-ttu-id="93ba2-124">Il s’agit d’une étape facultative.</span><span class="sxs-lookup"><span data-stu-id="93ba2-124">This is an optional step.</span></span> <span data-ttu-id="93ba2-125">Autoriser Microsoft à gérer la clé racine pour Azure Information Protection est le paramètre par défaut et la meilleure pratique recommandée pour la plupart des clients Office 365.</span><span class="sxs-lookup"><span data-stu-id="93ba2-125">Allowing Microsoft to manage the root key for Azure Information Protection is the default setting and recommended best practice for most Office 365 tenants.</span></span> <span data-ttu-id="93ba2-126">Si cela est le cas, vous n’avez rien à faire.</span><span class="sxs-lookup"><span data-stu-id="93ba2-126">If this is the case, you don't need to do anything.</span></span>

<span data-ttu-id="93ba2-127">Il existe de nombreuses raisons, par exemple des exigences de conformité, qui peuvent nécessiter de créer et gérer votre propre clé racine (également connue sous le nom Utilisation de votre propre clé (BYOK)).</span><span class="sxs-lookup"><span data-stu-id="93ba2-127">There are many reasons, for example compliance requirements, that may necessitate you generating and managing your own root key (also known as bring your own key (BYOK)).</span></span> <span data-ttu-id="93ba2-128">Si c’est le cas, nous vous recommandons d’effectuer les étapes requises avant de configurer les nouvelles fonctionnalités OME.</span><span class="sxs-lookup"><span data-stu-id="93ba2-128">If this is the case, we recommend that you complete the required steps before setting up the new OME capabilities.</span></span> <span data-ttu-id="93ba2-129">Pour plus d’informations, reportez-vous à [Planification et implémentation de votre clé de client Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key).</span><span class="sxs-lookup"><span data-stu-id="93ba2-129">See [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) for more.</span></span>

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a><span data-ttu-id="93ba2-130">Vérifier la nouvelle configuration OME dans Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="93ba2-130">Verify new OME configuration in Exchange Online PowerShell</span></span>

<span data-ttu-id="93ba2-131">Vous pouvez vérifier que votre client Office 365 est correctement configuré pour utiliser les nouvelles fonctionnalités OME dans [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="93ba2-131">You can verify that your Office 365 tenant is properly configured to use the new OME capabilities in [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>
  
1. <span data-ttu-id="93ba2-132">[Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) à l’aide d’un compte disposant des autorisations d’administrateur général dans votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="93ba2-132">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="93ba2-133">Exécutez la cmdlet Get-IRMConfiguration.</span><span class="sxs-lookup"><span data-stu-id="93ba2-133">Run the Get-SPOHubSite cmdlet.</span></span>

     <span data-ttu-id="93ba2-134">Une valeur de $True s’affiche pour le paramètre AzureRMSLicensingEnabled qui indique que OME est configuré dans votre client.</span><span class="sxs-lookup"><span data-stu-id="93ba2-134">You should see a value of $True for the AzureRMSLicensingEnabled parameter, which indicates that OME is configured in your tenant.</span></span> <span data-ttu-id="93ba2-135">Si ce n’est pas le cas, utilisez Set-IRMConfiguration pour activer la valeur d’AzureRMSLicensingEnabled sur $True pour activer OME.</span><span class="sxs-lookup"><span data-stu-id="93ba2-135">If it is not, use Set-IRMConfiguration to set the value of AzureRMSLicensingEnabled to $True to enable OME.</span></span>

3. <span data-ttu-id="93ba2-136">Exécutez la cmdlet Test-IRMConfiguration en utilisant la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="93ba2-136">Run the script by using the following syntax:</span></span>

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   <span data-ttu-id="93ba2-137">**Exemple** :</span><span class="sxs-lookup"><span data-stu-id="93ba2-137">**Example**:</span></span>

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - <span data-ttu-id="93ba2-138">La fourniture d’un courrier électronique d’expéditeur est facultative, mais oblige le système à effectuer des vérifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="93ba2-138">Providing a sender email is optional, but forces the system to perform additional checks.</span></span> <span data-ttu-id="93ba2-139">Utilisez l’adresse de courrier électronique de n’importe quel utilisateur de votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="93ba2-139">Use the email address of any user in your Office 365 tenant.</span></span>

     <span data-ttu-id="93ba2-140">Vos résultats doivent être similaires à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="93ba2-140">Your results should be similar to:</span></span>

     ```text
    Results : Acquiring RMS Templates ...
                - PASS: RMS Templates acquired.  Templates available: Contoso  - Confidential View Only, Contoso  - Confidential, Do Not
            Forward.
            Verifying encryption ...
                - PASS: Encryption verified successfully.
            Verifying decryption ...
                - PASS: Decryption verified successfully.
            Verifying IRM is enabled ...
                - PASS: IRM verified successfully.

            OVERALL RESULT: PASS
    ```

   - <span data-ttu-id="93ba2-141">Le nom de votre organisation Office 365 remplacera *Contoso*.</span><span class="sxs-lookup"><span data-stu-id="93ba2-141">Your Office 365 organization name will replace *Contoso*.</span></span>

   - <span data-ttu-id="93ba2-142">Les noms des modèles par défaut peuvent être différents de ceux affichés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="93ba2-142">The default template names may be different from those displayed above.</span></span> <span data-ttu-id="93ba2-143">Pour plus d’informations, reportez-vous à [Configurer et gérer des modèles pour Azure Information Protection](https://docs.microsoft.com/azure/information-protection/configure-policy-templates).</span><span class="sxs-lookup"><span data-stu-id="93ba2-143">See [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/configure-policy-templates) for more.</span></span>

4. <span data-ttu-id="93ba2-144">Exécutez la cmdlet Remove-PSSession pour vous déconnecter du service Rights Management.</span><span class="sxs-lookup"><span data-stu-id="93ba2-144">Run the Remove-PSSession cmdlet to disconnect from the Rights Management service.</span></span>

     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-mail-flow-rules-to-use-new-ome-capabilities"></a><span data-ttu-id="93ba2-145">Étapes suivantes : définir des règles de flux de messagerie pour utiliser les nouvelles fonctionnalités OME</span><span class="sxs-lookup"><span data-stu-id="93ba2-145">Next steps: Define mail flow rules to use new OME capabilities</span></span>

<span data-ttu-id="93ba2-146">S’il existe des règles de flux de messagerie précédemment configurées permettant de chiffrer le courrier électronique dans votre organisation Office 365, vous devez mettre à jour les règles existantes pour utiliser les nouvelles fonctionnalités OME.</span><span class="sxs-lookup"><span data-stu-id="93ba2-146">If there are previously configured mail flow rules to encrypt email in your Office 365 organization, you need to update the existing rules to use the new OME capabilities.</span></span> <span data-ttu-id="93ba2-147">Pour les nouveaux déploiements, vous devez créer des règles de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="93ba2-147">For new deployments, you need to create new mail flow rules.</span></span>

>[!IMPORTANT]
><span data-ttu-id="93ba2-148">Si vous ne mettez pas à jour les règles de flux de messagerie existantes, vos utilisateurs continueront à recevoir des e-mails chiffrés qui utilisent le format de pièces jointes HTML précédent, au lieu de la nouvelle expérience OME transparente.</span><span class="sxs-lookup"><span data-stu-id="93ba2-148">If you do not update existing mail flow rules, your users will continue to receive encrypted mail that uses the previous HTML attachment format, instead of the new seamless OME experience.</span></span>

<span data-ttu-id="93ba2-149">Les règles de flux de messagerie déterminent les conditions dans lesquelles les e-mails doivent être chiffrés, ainsi que les conditions pour supprimer ce chiffrement.</span><span class="sxs-lookup"><span data-stu-id="93ba2-149">Mail flow rules determine under what conditions email messages should be encrypted, as well as conditions for removing that encryption.</span></span> <span data-ttu-id="93ba2-150">Lorsque vous configurez une action pour une règle, tous les messages correspondant aux conditions de la règle sont chiffrés lorsqu’elles sont envoyées.</span><span class="sxs-lookup"><span data-stu-id="93ba2-150">When you set an action for a rule, any messages that match the rule conditions are encrypted when they're sent.</span></span>
  
<span data-ttu-id="93ba2-151">Pour plus d’informations sur la création de règles de flux de messagerie pour OME, reportez-vous à [Définir des règles de flux de courrier pour le chiffrement du courrier dans Office 365](define-mail-flow-rules-to-encrypt-email.md).</span><span class="sxs-lookup"><span data-stu-id="93ba2-151">For steps on creating mail flow rules for OME, see [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md).</span></span>

<span data-ttu-id="93ba2-152">Pour mettre à jour les règles existantes afin d’utiliser les nouvelles fonctionnalités OME :</span><span class="sxs-lookup"><span data-stu-id="93ba2-152">To update existing rules to use the new OME capabilities:</span></span>

1. <span data-ttu-id="93ba2-153">Dans le Centre d’administration Microsoft 365, accédez à **Centres d’administration > Exchange**.</span><span class="sxs-lookup"><span data-stu-id="93ba2-153">In the Office 365 admin center, navigate to Admin centers  Exchange.</span></span>
2. <span data-ttu-id="93ba2-154">Dans le Centre d’administration Exchange, accédez à **Flux de messagerie > Règles**.</span><span class="sxs-lookup"><span data-stu-id="93ba2-154">In the Exchange admin center (EAC), go to Mail flow  Rules.</span></span>
3. <span data-ttu-id="93ba2-155">Pour chaque règle, dans **Procédez comme suit** :</span><span class="sxs-lookup"><span data-stu-id="93ba2-155">For each rule, in **Do the following**:</span></span>
    - <span data-ttu-id="93ba2-156">Sélectionnez **Modifier la sécurité des messages**.</span><span class="sxs-lookup"><span data-stu-id="93ba2-156">Select **Modify the message security**.</span></span>
    - <span data-ttu-id="93ba2-157">Sélectionnez **Appliquer le chiffrement des messages Office 365 et la protection des droits**.</span><span class="sxs-lookup"><span data-stu-id="93ba2-157">Select **Apply Office 365 Message Encryption and rights protection**.</span></span>
    - <span data-ttu-id="93ba2-158">Sélectionnez un modèle RMS dans la liste.</span><span class="sxs-lookup"><span data-stu-id="93ba2-158">Select an RMS template from the list.</span></span>
    - <span data-ttu-id="93ba2-159">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="93ba2-159">Select **Save**.</span></span>
    - <span data-ttu-id="93ba2-160">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="93ba2-160">Select **OK**.</span></span>
