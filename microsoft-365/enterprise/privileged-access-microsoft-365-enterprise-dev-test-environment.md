---
title: Gestion des accès privilégiés pour votre environnement de test Microsoft 365 Entreprise
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- M365-security-compliance
ms.custom: Ent_TLGs
description: Utilisez ce guide de laboratoire de test pour activer la gestion des accès privilégiés dans votre environnement de test Microsoft 365 Enterprise.
ms.openlocfilehash: ce637b94333f088d25e479e61ad2a98176a2f7c6
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42085373"
---
# <a name="privileged-access-management-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="ab100-103">Gestion des accès privilégiés pour votre environnement de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="ab100-103">Privileged access management for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="ab100-104">*Ce Guide de Laboratoire Test peut être utilisé pour les environnements de test Microsoft 365 Entreprise et Office 365 Entreprise*.</span><span class="sxs-lookup"><span data-stu-id="ab100-104">*This Test Lab Guide can be used for both Microsoft 365 Enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="ab100-105">Avec les instructions de cet article, vous configurez la gestion des accès privilégiés pour renforcer la sécurité dans votre environnement de test Microsoft 365 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="ab100-105">With the instructions in this article, you configure privileged access management to increase security in your Microsoft 365 Enterprise test environment.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

>[!TIP]
><span data-ttu-id="ab100-107">Cliquez [ici](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="ab100-107">Click [here](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="ab100-108">Phase 1 : Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="ab100-108">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="ab100-109">Si vous souhaitez simplement configurer la gestion des accès privilégiés de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="ab100-109">If you just want to configure privileged access management in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="ab100-110">Si vous souhaitez configurer la gestion des accès privilégiés dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ab100-110">If you want to configure privileged access management in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
>[!NOTE]
><span data-ttu-id="ab100-111">Le test de la gestion des accès privilégiés ne nécessite pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt AD DS.</span><span class="sxs-lookup"><span data-stu-id="ab100-111">Testing privileged access management does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an AD DS forest.</span></span> <span data-ttu-id="ab100-112">Elle est fournie ici en tant qu’option qui vous permet de tester la gestion des accès privilégiés et de l’expérimenter dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="ab100-112">It is provided here as an option so that you can test privileged access management and experiment with it in an environment that represents a typical organization.</span></span> 

## <a name="phase-2-configure-privileged-access-management"></a><span data-ttu-id="ab100-113">Phase 2 : configurer la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="ab100-113">Phase 2: Configure privileged access management</span></span>

<span data-ttu-id="ab100-114">Dans cette phase, vous allez configurer un groupe approbateurs et activer la gestion des accès privilégiés pour votre environnement de test Microsoft 365 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="ab100-114">In this phase, you configure an approvers group and enable privileged access management for your Microsoft 365 Enterprise test environment.</span></span> <span data-ttu-id="ab100-115">Pour plus d’informations et pour obtenir une vue d’ensemble de la gestion des accès privilégiés, consultez la rubrique [gestion des accès privilégiés dans Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-overview).</span><span class="sxs-lookup"><span data-stu-id="ab100-115">For additional details and an overview of privileged access management, see [Privileged access management in Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-overview).</span></span>

<span data-ttu-id="ab100-116">Procédez comme suit pour configurer et utiliser l’accès privilégié dans votre organisation Office 365 :</span><span class="sxs-lookup"><span data-stu-id="ab100-116">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="ab100-117">Étape 1 : créer un groupe d’approbateurs</span><span class="sxs-lookup"><span data-stu-id="ab100-117">Step 1: Create an approver's group</span></span>](https://docs.microsoft.com/microsoft-365/compliance/privileged-access-management-configuration#step-1-create-an-approvers-group)

    <span data-ttu-id="ab100-118">Avant de commencer à utiliser l’accès aux privilèges, déterminez qui disposera de l’autorité d’approbation pour les demandes entrantes d’accès à des tâches élevées et privilégiées.</span><span class="sxs-lookup"><span data-stu-id="ab100-118">Before you start using privilege access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks.</span></span> <span data-ttu-id="ab100-119">Tout utilisateur qui fait partie du groupe approbateurs est en mesure d’approuver les demandes d’accès.</span><span class="sxs-lookup"><span data-stu-id="ab100-119">Any user who is part of the Approvers’ group will be able to approve access requests.</span></span> <span data-ttu-id="ab100-120">Pour cela, vous créez un groupe de sécurité à extension messagerie dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="ab100-120">This is enabled by creating a mail-enabled security group in Office 365.</span></span> <span data-ttu-id="ab100-121">Créez un groupe de sécurité nommé « approbateurs d’accès privilégié » dans votre environnement de test et ajoutez « User 3 » précédemment créé dans les étapes du Guide de laboratoire de test précédent.</span><span class="sxs-lookup"><span data-stu-id="ab100-121">Create a new security group named "Privileged Access Approvers" in your test environment and add the "User 3" previously created in prior test lab guide steps.</span></span>

- [<span data-ttu-id="ab100-122">Étape 2 : activer l’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="ab100-122">Step 2: Enable privileged access</span></span>](https://docs.microsoft.com/microsoft-365/compliance/privileged-access-management-configuration#step-2-enable-privileged-access)

    <span data-ttu-id="ab100-123">L’accès privilégié doit être activé de manière explicite dans Office 365 avec le groupe d’approbateurs par défaut et inclure un ensemble de comptes système que vous souhaitez exclure du contrôle d’accès gestion des accès privilégiés.</span><span class="sxs-lookup"><span data-stu-id="ab100-123">Privileged access needs to be explicitly turned on in Office 365 with the default approver group and including a set of system accounts that you’d want to be excluded from the privileged access management access control.</span></span> <span data-ttu-id="ab100-124">Veillez à activer l’accès privilégié dans votre organisation Office 365 avant de commencer la phase 3 de ce guide.</span><span class="sxs-lookup"><span data-stu-id="ab100-124">Be sure to enable privileged access in your Office 365 organization before starting Phase 3 of this guide.</span></span>

## <a name="phase-3-verify-that-approval-is-required-for-elevated-and-privileged-tasks"></a><span data-ttu-id="ab100-125">Phase 3 : vérifier que l’approbation est requise pour les tâches avec privilèges élevés et privilégiées</span><span class="sxs-lookup"><span data-stu-id="ab100-125">Phase 3: Verify that approval is required for elevated and privileged tasks</span></span>

<span data-ttu-id="ab100-126">Dans cette phase, vous vérifiez que la stratégie d’accès privilégié fonctionne et que les utilisateurs demandent une approbation pour exécuter des tâches élevées et privilégiées définies.</span><span class="sxs-lookup"><span data-stu-id="ab100-126">In this phase, you verify that the privileged access policy is working and users require approval to execute defined elevated and privileged tasks.</span></span>

### <a name="test-ability-to-execute-a-task-not-defined-in-a-privileged-access-policy"></a><span data-ttu-id="ab100-127">Tester la possibilité d’exécuter une tâche non définie dans une stratégie d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="ab100-127">Test ability to execute a task NOT defined in a privileged access policy</span></span>

<span data-ttu-id="ab100-128">Tout d’abord, connectez-vous à Exchange Management PowerShell avec les informations d’identification d’un utilisateur configuré en tant qu’administrateur général dans votre environnement de test et essayez de créer une nouvelle règle de journal.</span><span class="sxs-lookup"><span data-stu-id="ab100-128">First, connect to Exchange Management PowerShell with the credentials of a user configured as a Global Administrator in your test environment and attempt to create a new Journal rule.</span></span> <span data-ttu-id="ab100-129">La tâche [New-JournalRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-journalrule?view=exchange-ps) n’est actuellement pas définie dans une stratégie d’accès privilégié pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ab100-129">The [New-JournalRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-journalrule?view=exchange-ps) task is not currently defined in a privileged access policy for your organization.</span></span>

1. <span data-ttu-id="ab100-130">Sur votre ordinateur local, ouvrez le module Exchange Online Remote PowerShell et connectez-vous au module **Microsoft** > **Exchange Online** PowerShell à l’aide du compte d’administrateur général pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="ab100-130">On your local computer, open and sign into the Exchange Online Remote PowerShell Module at **Microsoft Corporation** > **Microsoft Exchange Online Remote PowerShell Module** using the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="ab100-131">Dans Exchange Management PowerShell, créez une nouvelle règle de journal pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="ab100-131">In Exchange Management PowerShell, create a new Journal rule for your organization:</span></span>

```ExchangeManagementPowerShell
New-JournalRule -Name "JournalRule1" -Recipient joe@contoso.onmicrosoft.com -JournalEmailAddress barbara@adatum.com -Scope Global -Enabled $true
```

4. <span data-ttu-id="ab100-132">Affichage de la création de la nouvelle règle de journal dans Exchange Management PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ab100-132">View that the new Journal Rule was successfully created in Exchange Management PowerShell.</span></span>

### <a name="create-a-new-privileged-access-policy-for-the-new-journalrule-task"></a><span data-ttu-id="ab100-133">Créer une stratégie d’accès privilégié pour la tâche New-JournalRule</span><span class="sxs-lookup"><span data-stu-id="ab100-133">Create a new privileged access policy for the New-JournalRule task</span></span>

>[!NOTE]
><span data-ttu-id="ab100-134">Si vous n’avez pas déjà effectué les étapes 1 et 2 de la phase 2 de ce guide, assurez-vous de suivre les étapes nécessaires pour créer un groupe d’approbateurs nommé « approbateurs d’accès aux privilèges » et pour activer l’accès privilégié dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="ab100-134">If you haven't already completed the Steps 1 and 2 from Phase 2 of this guide, be sure follow the steps to create an approver's group named "Privilege Access Approvers" and to enable privileged access in your test environment.</span></span>

1. <span data-ttu-id="ab100-135">Connectez-vous au [Centre d’administration 365 de Microsoft](https://admin.microsoft.com) à l’aide des informations d’identification du compte d’administrateur global pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="ab100-135">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) using credentials the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="ab100-136">Dans le centre d’administration, accédez à **paramètres** > **Security & Privacy** > **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="ab100-136">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="ab100-137">Sélectionnez **gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="ab100-137">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="ab100-138">Sélectionnez **configurer les stratégies** et sélectionnez **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="ab100-138">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="ab100-139">Dans les champs de liste déroulante, sélectionnez ou entrez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ab100-139">From the drop-down fields, select or enter the following values:</span></span>

    <span data-ttu-id="ab100-140">**Type de stratégie**: tâche</span><span class="sxs-lookup"><span data-stu-id="ab100-140">**Policy type**: Task</span></span>

    <span data-ttu-id="ab100-141">**Étendue de stratégie**: Exchange</span><span class="sxs-lookup"><span data-stu-id="ab100-141">**Policy scope**: Exchange</span></span>

    <span data-ttu-id="ab100-142">**Nom**de la stratégie : nouvelle règle de journal</span><span class="sxs-lookup"><span data-stu-id="ab100-142">**Policy name**: New Journal Rule</span></span>

    <span data-ttu-id="ab100-143">**Type d’approbation**: Manuel</span><span class="sxs-lookup"><span data-stu-id="ab100-143">**Approval type**: Manual</span></span>

    <span data-ttu-id="ab100-144">**Groupe d’approbation**: approbateurs des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="ab100-144">**Approval group**: Privileged Access Approvers</span></span>

6. <span data-ttu-id="ab100-145">Sélectionnez **créer** , puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ab100-145">Select **Create** and then **Close**.</span></span> <span data-ttu-id="ab100-146">La configuration et l’activation de la stratégie peuvent prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="ab100-146">It may take a few minutes for the policy to be fully configured and enabled.</span></span> <span data-ttu-id="ab100-147">Veillez à laisser le temps nécessaire pour que la stratégie soit entièrement activée avant de tester les conditions d’approbation à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="ab100-147">Be sure to allow time for the policy to be fully enabled before testing the approval requirement in the next step.</span></span>

### <a name="test-approval-requirement-for-the-new-journalrule-task-defined-in-a-privileged-access-policy"></a><span data-ttu-id="ab100-148">Condition d’approbation de test pour la tâche New-JournalRule définie dans une stratégie d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="ab100-148">Test approval requirement for the New-JournalRule task defined in a privileged access policy</span></span>

1. <span data-ttu-id="ab100-149">Sur votre ordinateur local, ouvrez le module Exchange Online Remote PowerShell et connectez-vous au module **Microsoft** > **Exchange Online** PowerShell à l’aide d’un compte d’administrateur général pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="ab100-149">On your local computer, open and sign into the Exchange Online Remote PowerShell Module at **Microsoft Corporation** > **Microsoft Exchange Online Remote PowerShell Module** using an using the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="ab100-150">Dans Exchange Management PowerShell, créez une nouvelle règle de journal pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="ab100-150">In Exchange Management PowerShell, create a new Journal rule for your organization:</span></span>

```ExchangeManagementPowerShell
New-JournalRule -Name "JournalRule2" -Recipient user1@<your subscription domain> -JournalEmailAddress user1@<your subscription domain> -Scope Global -Enabled $true
```

3. <span data-ttu-id="ab100-151">Afficher l’erreur « autorisations insuffisantes » dans Exchange Management PowerShell :</span><span class="sxs-lookup"><span data-stu-id="ab100-151">View "Insufficient permissions" error in Exchange Management PowerShell:</span></span>

```ExchangeManagementPowerShell
Insufficient permissions. Please raise an elevated access request for this task.
    + CategoryInfo          : NotSpecified: (:) [], LocalizedException
    + FullyQualifiedErrorId : [Server=CY1PR00MB0220,RequestId=7b8c7470-ddd0-4528-a01e-5e20ecc9bd54,TimeStamp=9/19/2018
    7:38:34 PM] [FailureCategory=Cmdlet-LocalizedException] 882BD051
    + PSComputerName        : outlook.office365.com
```

### <a name="request-access-to-create-a-new-journal-rule-using-the-new-journalrule-task"></a><span data-ttu-id="ab100-152">Demander l’accès pour créer une nouvelle règle de journal à l’aide de la tâche New-JournalRule</span><span class="sxs-lookup"><span data-stu-id="ab100-152">Request access to create a new Journal Rule using the New-JournalRule task</span></span>

1. <span data-ttu-id="ab100-153">Connectez-vous au [Centre d’administration 365 de Microsoft](https://admin.microsoft.com) à l’aide du compte d’administrateur général pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="ab100-153">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) using the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="ab100-154">Dans le centre d’administration, accédez à **paramètres** > **Security & Privacy** > **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="ab100-154">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="ab100-155">Sélectionnez **gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="ab100-155">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="ab100-156">Sélectionnez **nouvelle demande**.</span><span class="sxs-lookup"><span data-stu-id="ab100-156">Select **New request**.</span></span> <span data-ttu-id="ab100-157">Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="ab100-157">From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="ab100-158">**Type de demande**: tâche</span><span class="sxs-lookup"><span data-stu-id="ab100-158">**Request type**: Task</span></span>

    <span data-ttu-id="ab100-159">**Étendue**de la demande : Exchange</span><span class="sxs-lookup"><span data-stu-id="ab100-159">**Request scope**: Exchange</span></span>

    <span data-ttu-id="ab100-160">**Demande**: nouvelle règle de journal</span><span class="sxs-lookup"><span data-stu-id="ab100-160">**Request for**: New Journal Rule</span></span>

    <span data-ttu-id="ab100-161">**Durée (heures)**: 2</span><span class="sxs-lookup"><span data-stu-id="ab100-161">**Duration (hours)**: 2</span></span>

    <span data-ttu-id="ab100-162">**Commentaires**: demander l’autorisation de créer une nouvelle règle de journal</span><span class="sxs-lookup"><span data-stu-id="ab100-162">**Comments**: Request permission to create a new Journal Rule</span></span>

5. <span data-ttu-id="ab100-163">Sélectionnez **Enregistrer** , puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ab100-163">Select **Save** and then **Close**.</span></span> <span data-ttu-id="ab100-164">Votre demande sera envoyée au groupe de l’approbateur par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="ab100-164">Your request will be sent to the approver's group via email.</span></span>

### <a name="approve-privileged-access-request-for-the-creation-of-a-new-journal-rule"></a><span data-ttu-id="ab100-165">Approuver une demande d’accès privilégié pour la création d’une nouvelle règle de journal</span><span class="sxs-lookup"><span data-stu-id="ab100-165">Approve privileged access request for the creation of a new Journal Rule</span></span>

1. <span data-ttu-id="ab100-166">Connectez-vous au [Centre d’administration 365 de Microsoft](https://admin.microsoft.com) à l’aide des informations d’identification de l’utilisateur 3 dans votre environnement de test (membre du groupe de sécurité « approbateurs avec accès privilégié » dans votre environnement de test).</span><span class="sxs-lookup"><span data-stu-id="ab100-166">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) using the credentials for User 3 in your test environment (member of the "Privileged Access Approvers" security group in your test environment).</span></span>

2. <span data-ttu-id="ab100-167">Dans le centre d’administration, accédez à **paramètres** > **Security & Privacy** > **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="ab100-167">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="ab100-168">Sélectionnez **gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="ab100-168">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="ab100-169">Sélectionnez la demande en attente et sélectionnez **approuver** pour accorder l’accès au compte d’administrateur général afin de créer une nouvelle règle de journal.</span><span class="sxs-lookup"><span data-stu-id="ab100-169">Select the pending request and select **Approve** to grant access to the Global Admin account to create a new Journal Rule.</span></span> <span data-ttu-id="ab100-170">Un courrier électronique de notification confirmant que l’approbation a été accordée est envoyé au compte d’administrateur global (l’utilisateur qui effectue la demande).</span><span class="sxs-lookup"><span data-stu-id="ab100-170">A notification email confirming that approval has been granted will be sent to the Global Admin account (the requesting user).</span></span>  

### <a name="test-creating-a-new-journal-rule-with-privileged-access-approved-for-the-new-journalrule-task"></a><span data-ttu-id="ab100-171">Tester la création d’une nouvelle règle de journal avec un accès privilégié approuvé pour la tâche New-JournalRule</span><span class="sxs-lookup"><span data-stu-id="ab100-171">Test creating a new Journal Rule with privileged access approved for the New-JournalRule task</span></span>

1. <span data-ttu-id="ab100-172">Sur votre ordinateur local, ouvrez le module Exchange Online Remote PowerShell et connectez-vous au module **Microsoft** > **Exchange Online** PowerShell à l’aide du compte d’administrateur général pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="ab100-172">On your local computer, open and sign into the Exchange Online Remote PowerShell Module at **Microsoft Corporation** > **Microsoft Exchange Online Remote PowerShell Module** using the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="ab100-173">Dans Exchange Management PowerShell, créez une nouvelle règle de journal pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="ab100-173">In Exchange Management PowerShell, create a new Journal rule for your organization:</span></span>

```ExchangeManagementPowerShell
New-JournalRule -Name "JournalRule2" -Recipient user1@<your subscription domain> -JournalEmailAddress user1@<your subscription domain> -Scope Global -Enabled $true
```

3. <span data-ttu-id="ab100-174">Affichage de la création de la nouvelle règle de journal dans Exchange Management PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ab100-174">View that the new Journal Rule was successfully created in Exchange Management PowerShell.</span></span>

## <a name="next-step"></a><span data-ttu-id="ab100-175">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="ab100-175">Next step</span></span>

<span data-ttu-id="ab100-176">Découvrez les fonctionnalités et les fonctionnalités de [protection des informations](m365-enterprise-test-lab-guides.md#information-protection) supplémentaires dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="ab100-176">Explore additional [information protection](m365-enterprise-test-lab-guides.md#information-protection) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab100-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab100-177">See also</span></span>

[<span data-ttu-id="ab100-178">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="ab100-178">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="ab100-179">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="ab100-179">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="ab100-180">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="ab100-180">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
