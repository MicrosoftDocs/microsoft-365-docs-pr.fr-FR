---
title: Gestion des accès privilégiés pour votre environnement de test Microsoft 365 Entreprise
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 09/21/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_TLGs
description: Utilisez ce Guide de laboratoire de Test pour permettre la gestion de l’accès privilégié de votre environnement de test Microsoft 365 pour entreprises.
ms.openlocfilehash: 5f1a416a12171504af110ec62b9a7882143263e6
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26866847"
---
# <a name="privileged-access-management-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="3868b-103">Gestion des accès privilégiés pour votre environnement de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="3868b-103">Privileged access management for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="3868b-104">Avec les instructions de cet article, vous configurez la gestion des accès privilégié pour renforcer la sécurité dans votre environnement de test Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="3868b-104">With the instructions in this article, you configure privileged access management to increase security in your Microsoft 365 Enterprise test environment.</span></span>

![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="3868b-106">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="3868b-106">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="3868b-107">Phase 1 : Création de votre environnement de test Microsoft 365 pour entreprises</span><span class="sxs-lookup"><span data-stu-id="3868b-107">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="3868b-108">Si vous souhaitez simplement configurer la gestion de l’accès privilégié de manière léger avec la configuration minimale requise, suivez les instructions de [configuration de base léger](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="3868b-108">If you just want to configure privileged access management in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="3868b-109">Si vous souhaitez configurer la gestion de l’accès privilégié dans une entreprise simulée, suivez les instructions de [l’authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="3868b-109">If you want to configure privileged access management in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="3868b-p101">Test de gestion de l’accès privilégié ne nécessite pas l’environnement de test simulé entreprise, qui comprend un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt Windows Server Active Directory. Il est fourni ici en tant qu’option pour que vous puissiez tester privilégié accéder à la gestion et tester dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="3868b-p101">Testing privileged access management does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Windows Server AD forest. It is provided here as an option so that you can test privileged access management and experiment with it in an environment that represents a typical organization.</span></span> 

## <a name="phase-2-configure-privileged-access-management"></a><span data-ttu-id="3868b-112">Phase 2 : Configurer la gestion des accès privilégié</span><span class="sxs-lookup"><span data-stu-id="3868b-112">Phase 2: Configure privileged access management</span></span>

<span data-ttu-id="3868b-p102">Durant cette phase, vous configurez un groupe approbateurs et activez la gestion de l’accès privilégié pour votre environnement de test Microsoft 365 pour entreprises. Pour plus d’informations et une vue d’ensemble des privilèges accéder à la gestion, voir [gestion de l’accès privilégié dans Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-overview).</span><span class="sxs-lookup"><span data-stu-id="3868b-p102">In this phase, you configure an approvers group and enable privileged access management for your Microsoft 365 Enterprise test environment. For additional details and an overview of privileged access management, see [Privileged access management in Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-overview).</span></span>

<span data-ttu-id="3868b-115">Suivez ces étapes pour configurer et utiliser un accès privilégié dans votre organisation Office 365 :</span><span class="sxs-lookup"><span data-stu-id="3868b-115">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="3868b-116">Étape 1 : Créer le groupe d’approbateur</span><span class="sxs-lookup"><span data-stu-id="3868b-116">Step 1: Create an approver's group</span></span>](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration#step-1---create-an-approvers-group)

    <span data-ttu-id="3868b-p103">Avant de commencer à l’aide de privilège d’accès, déterminer ayant autorité d’approbation pour les demandes entrantes pour l’accès aux tâches avec des privilèges élevés et privilégiés. Tout utilisateur qui fait partie du groupe des approbateurs sera en mesure d’approuver les demandes d’accès. Cette option est activée en créant un groupe de sécurité à extension messagerie dans Office 365. Créer un nouveau groupe de sécurité nommé « Approbateurs d’accès privilégié » dans votre environnement de test et ajouter le « utilisateur 3 », précédemment créé dans les étapes de guide de laboratoire de test préalable.</span><span class="sxs-lookup"><span data-stu-id="3868b-p103">Before you start using privilege access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks. Any user who is part of the Approvers’ group will be able to approve access requests. This is enabled by creating a mail-enabled security group in Office 365. Create a new security group named "Privileged Access Approvers" in your test environment and add the "User 3" previously created in prior test lab guide steps.</span></span>

- [<span data-ttu-id="3868b-121">Étape 2 : Activer l’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="3868b-121">Step 2: Enable privileged access</span></span>](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration#step-2---enable-privileged-access)

    <span data-ttu-id="3868b-p104">Accès privilégié doit être activé explicitement dans Office 365 avec le groupe d’approbateur par défaut et y compris un ensemble de comptes système que vous souhaitez exclure le contrôle d’accès de gestion des accès privilégié. Veillez à activer l’accès privilégié dans votre organisation Office 365 avant de commencer la Phase 3 de ce guide.</span><span class="sxs-lookup"><span data-stu-id="3868b-p104">Privileged access needs to be explicitly turned on in Office 365 with the default approver group and including a set of system accounts that you’d want to be excluded from the privileged access management access control. Be sure to enable privileged access in your Office 365 organization before starting Phase 3 of this guide.</span></span>

## <a name="phase-3-verify-that-approval-is-required-for-elevated-and-privileged-tasks"></a><span data-ttu-id="3868b-124">Phase 3 : Vérifiez que l’approbation est nécessaire pour les tâches avec des privilèges élevés et privilégiés</span><span class="sxs-lookup"><span data-stu-id="3868b-124">Phase 3: Verify that approval is required for elevated and privileged tasks</span></span>
<span data-ttu-id="3868b-125">Dans cette phase, vous vérifiez que la stratégie d’accès privilégié fonctionne et que les utilisateurs ont besoin d’approbation pour exécuter des tâches avec des privilèges élevés et privilégiés définies.</span><span class="sxs-lookup"><span data-stu-id="3868b-125">In this phase, you verify that the privileged access policy is working and users require approval to execute defined elevated and privileged tasks.</span></span>

### <a name="test-ability-to-execute-a-task-not-defined-in-a-privileged-access-policy"></a><span data-ttu-id="3868b-126">Tester la capacité à exécuter une tâche non définie dans une stratégie d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="3868b-126">Test ability to execute a task NOT defined in a privileged access policy</span></span>

<span data-ttu-id="3868b-p105">Tout d’abord, connectez-vous à Exchange Management PowerShell avec les informations d’identification d’un utilisateur configuré comme un administrateur Global dans votre environnement de test et essayez de créer une nouvelle règle de Journal. La tâche [New-JournalRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-journalrule?view=exchange-ps) n’est pas actuellement définie dans une stratégie d’accès privilégié pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3868b-p105">First, connect to Exchange Management PowerShell with the credentials of a user configured as a Global Administrator in your test environment and attempt to create a new Journal rule. The [New-JournalRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-journalrule?view=exchange-ps) task is not currently defined in a privileged access policy for your organization.</span></span>

1. <span data-ttu-id="3868b-129">Sur votre ordinateur local, ouvrez et connectez-vous à la le Exchange Online PowerShell Module distant **Microsoft**Corporation > **Exchange distant PowerShell Module Microsoft Online** à l’aide de l’administrateur Global de compte pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="3868b-129">On your local computer, open and sign into the the Exchange Online Remote PowerShell Module at **Microsoft Corporation** > **Microsoft Exchange Online Remote PowerShell Module** using the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="3868b-130">Dans Exchange Management Powershell, créez une nouvelle règle de Journal pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="3868b-130">In Exchange Management Powershell, create a new Journal rule for your organization:</span></span>

```
New-JournalRule -Name "JournalRule1" -Recipient joe@contoso.onmicrosoft.com -JournalEmailAddress barbara@adatum.com -Scope Global -Enabled $true
```
4. <span data-ttu-id="3868b-131">Affichage que la nouvelle règle de Journal a été créée dans Exchange Management PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3868b-131">View that the new Journal Rule was successfully created in Exchange Management PowerShell.</span></span>

### <a name="create-a-new-privileged-access-policy-for-the-new-journalrule-task"></a><span data-ttu-id="3868b-132">Créer une nouvelle stratégie d’accès privilégié pour la tâche New-JournalRule</span><span class="sxs-lookup"><span data-stu-id="3868b-132">Create a new privileged access policy for the New-JournalRule task</span></span>

> [!NOTE]
> <span data-ttu-id="3868b-133">Si vous n’avez pas déjà effectué les étapes 1 et 2 à partir de la Phase 2 de ce guide, vous pouvez être que suivre les étapes pour créer groupe d’un approbateur nommé « Privilège accès approbateurs » et permettre l’accès privilégié dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="3868b-133">If you haven't already completed the Steps 1 and 2 from Phase 2 of this guide, be sure follow the steps to create an approver's group named "Privilege Access Approvers" and to enable privileged access in your test environment.</span></span>

1. <span data-ttu-id="3868b-134">Se connecter au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide des informations d’identification pour votre environnement de test, le compte d’administrateur Global.</span><span class="sxs-lookup"><span data-stu-id="3868b-134">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="3868b-135">Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="3868b-135">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="3868b-136">Sélectionnez **Gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="3868b-136">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="3868b-137">Sélectionnez **configurer les stratégies** et sélectionnez **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="3868b-137">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="3868b-138">Dans les champs de liste déroulante, sélectionnez ou entrez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3868b-138">From the drop-down fields, select or enter the following values:</span></span>
    
    <span data-ttu-id="3868b-139">**Type de stratégie**: tâche</span><span class="sxs-lookup"><span data-stu-id="3868b-139">**Policy type**: Task</span></span>

    <span data-ttu-id="3868b-140">**Étendue de la stratégie**: Exchange</span><span class="sxs-lookup"><span data-stu-id="3868b-140">**Policy scope**: Exchange</span></span>

    <span data-ttu-id="3868b-141">**Nom de la stratégie**: nouvelle règle de Journal</span><span class="sxs-lookup"><span data-stu-id="3868b-141">**Policy name**: New Journal Rule</span></span>

    <span data-ttu-id="3868b-142">**Type d’approbation**: manuel</span><span class="sxs-lookup"><span data-stu-id="3868b-142">**Approval type**: Manual</span></span>

    <span data-ttu-id="3868b-143">**Groupe d’approbation**: privilégié approbateurs Access</span><span class="sxs-lookup"><span data-stu-id="3868b-143">**Approval group**: Privileged Access Approvers</span></span>

6. <span data-ttu-id="3868b-p106">Sélectionnez **créer** , puis sur **Fermer**. Il peut prendre quelques minutes pour la stratégie soit entièrement configuré et activé. Veillez à laisser le temps à la stratégie à activer entièrement avant de tester l’obligation d’approbation à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="3868b-p106">Select **Create** and then **Close**. It may take a few minutes for the policy to be fully configured and enabled. Be sure to allow time for the policy to be fully enabled before testing the approval requirement in the next step.</span></span>

### <a name="test-approval-requirement-for-the-new-journalrule-task-defined-in-a-privileged-access-policy"></a><span data-ttu-id="3868b-147">Demande d’approbation de test pour la tâche New-JournalRule définie dans une stratégie d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="3868b-147">Test approval requirement for the New-JournalRule task defined in a privileged access policy</span></span>

1. <span data-ttu-id="3868b-148">Sur votre ordinateur local, ouvrez et connectez-vous à la le Exchange Online PowerShell Module distant **Microsoft**Corporation > compte**Exchange à distance PowerShell Module Microsoft Online** à l’aide d’un à l’aide de l’administrateur Global de test environnement.</span><span class="sxs-lookup"><span data-stu-id="3868b-148">On your local computer, open and sign into the the Exchange Online Remote PowerShell Module at **Microsoft Corporation** > **Microsoft Exchange Online Remote PowerShell Module** using an using the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="3868b-149">Dans Exchange Management Powershell, créez une nouvelle règle de Journal pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="3868b-149">In Exchange Management Powershell, create a new Journal rule for your organization:</span></span>

```
New-JournalRule -Name "JournalRule2" -Recipient user1@<your subscription domain> -JournalEmailAddress user1@<your subscription domain> -Scope Global -Enabled $true
```
3. <span data-ttu-id="3868b-150">Afficher l’erreur « Autorisations insuffisant » dans Exchange Management PowerShell :</span><span class="sxs-lookup"><span data-stu-id="3868b-150">View "Insuffient permissions" error in Exchange Management PowerShell:</span></span>

```
Insufficient permissions. Please raise an elevated access request for this task.
    + CategoryInfo          : NotSpecified: (:) [], LocalizedException
    + FullyQualifiedErrorId : [Server=CY1PR00MB0220,RequestId=7b8c7470-ddd0-4528-a01e-5e20ecc9bd54,TimeStamp=9/19/2018
    7:38:34 PM] [FailureCategory=Cmdlet-LocalizedException] 882BD051
    + PSComputerName        : outlook.office365.com
```

### <a name="request-access-to-create-a-new-journal-rule-using-the-new-journalrule-task"></a><span data-ttu-id="3868b-151">Pour créer une nouvelle règle de Journal à l’aide de la tâche New-JournalRule pour demander l’accès</span><span class="sxs-lookup"><span data-stu-id="3868b-151">Request access to create a new Journal Rule using the New-JournalRule task</span></span>

1. <span data-ttu-id="3868b-152">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) utilisant le compte d’administrateur Global de votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="3868b-152">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="3868b-153">Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="3868b-153">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="3868b-154">Sélectionnez **Gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="3868b-154">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="3868b-p107">Sélectionnez **nouvelle demande**. Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="3868b-p107">Select **New request**. From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="3868b-157">**Type de demande**: tâche</span><span class="sxs-lookup"><span data-stu-id="3868b-157">**Request type**: Task</span></span>

    <span data-ttu-id="3868b-158">**Étendue de demande**: Exchange</span><span class="sxs-lookup"><span data-stu-id="3868b-158">**Request scope**: Exchange</span></span>

    <span data-ttu-id="3868b-159">**Demande de**: nouvelle règle de Journal</span><span class="sxs-lookup"><span data-stu-id="3868b-159">**Request for**: New Journal Rule</span></span>

    <span data-ttu-id="3868b-160">**Durée (en heures)**: 2</span><span class="sxs-lookup"><span data-stu-id="3868b-160">**Duration (hours)**: 2</span></span>

    <span data-ttu-id="3868b-161">**Commentaires**: demander l’autorisation de créer une nouvelle règle de Journal</span><span class="sxs-lookup"><span data-stu-id="3868b-161">**Comments**: Request permission to create a new Journal Rule</span></span>

5. <span data-ttu-id="3868b-p108">Sélectionnez **Enregistrer** , puis sur **Fermer**. Votre demande sera envoyée au groupe de l’approbateur par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="3868b-p108">Select **Save** and then **Close**. Your request will be sent to the approver's group via email.</span></span>

### <a name="approve-privileged-access-request-for-the-creation-of-a-new-journal-rule"></a><span data-ttu-id="3868b-164">Approuver les demandes d’accès privilégié de la création d’une nouvelle règle de Journal</span><span class="sxs-lookup"><span data-stu-id="3868b-164">Approve privileged access request for the creation of a new Journal Rule</span></span>

1. <span data-ttu-id="3868b-165">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) par les informations d’identification utilisateur 3 dans votre environnement de test (membre du groupe de sécurité « Approbateurs d’accès privilégié » dans votre environnement de test).</span><span class="sxs-lookup"><span data-stu-id="3868b-165">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using the credentials for User 3 in your test environment (member of the "Privileged Access Approvers" security group in your test environment).</span></span>

2. <span data-ttu-id="3868b-166">Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="3868b-166">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="3868b-167">Sélectionnez **Gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="3868b-167">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="3868b-p109">Sélectionnez la demande en attente, sélectionnez **Approuver** pour accorder l’accès au compte d’administrateur Global pour créer une nouvelle règle de Journal. Une notification électronique vous demandant de confirmer que la réception a été accordée sera envoyé au compte d’administrateur Global (l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="3868b-p109">Select the pending request and select **Approve** to grant access to the Global Admin account to create a new Journal Rule. An notification email confirming that approval has been granted will be sent to the Global Admin account (the requesting user).</span></span>  

### <a name="test-creating-a-new-journal-rule-with-privileged-access-approved-for-the-new-journalrule-task"></a><span data-ttu-id="3868b-170">Création d’une nouvelle règle de Journal avec un accès privilégié approuvé pour la tâche New-JournalRule de test</span><span class="sxs-lookup"><span data-stu-id="3868b-170">Test creating a new Journal Rule with privileged access approved for the New-JournalRule task</span></span>

1. <span data-ttu-id="3868b-171">Sur votre ordinateur local, ouvrez et connectez-vous à la le Exchange Online PowerShell Module distant **Microsoft**Corporation > **Exchange distant PowerShell Module Microsoft Online** à l’aide de l’administrateur Global de compte pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="3868b-171">On your local computer, open and sign into the the Exchange Online Remote PowerShell Module at **Microsoft Corporation** > **Microsoft Exchange Online Remote PowerShell Module** using the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="3868b-172">Dans Exchange Management Powershell, créez une nouvelle règle de Journal pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="3868b-172">In Exchange Management Powershell, create a new Journal rule for your organization:</span></span>

```
New-JournalRule -Name "JournalRule2" -Recipient user1@<your subscription domain> -JournalEmailAddress user1@<your subscription domain> -Scope Global -Enabled $true
```
3. <span data-ttu-id="3868b-173">Affichage que la nouvelle règle de Journal a été créée dans Exchange Management PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3868b-173">View that the new Journal Rule was successfully created in Exchange Management PowerShell.</span></span>

## <a name="next-step"></a><span data-ttu-id="3868b-174">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="3868b-174">Next step</span></span>

<span data-ttu-id="3868b-175">Explorez les fonctionnalités supplémentaires de [protection des informations](m365-enterprise-test-lab-guides.md#information-protection) et fonctionnalités dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="3868b-175">Explore additional [information protection](m365-enterprise-test-lab-guides.md#information-protection) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="3868b-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3868b-176">See also</span></span>

[<span data-ttu-id="3868b-177">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="3868b-177">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="3868b-178">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="3868b-178">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="3868b-179">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="3868b-179">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)