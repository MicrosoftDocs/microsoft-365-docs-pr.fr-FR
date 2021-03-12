---
title: Étapes de migration AD FS pour la migration à partir de Microsoft Cloud Deutschland
ms.author: andyber
author: andybergen
manager: laurawi
ms.date: 12/01/2020
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
f1.keywords:
- CSH
ms.custom:
- Ent_TLGs
description: 'Résumé : Étapes de migration des services AD FS (Active Directory Federation Services) pour la migration à partir de Microsoft Cloud Deutschland.'
ms.openlocfilehash: 030515227f3abdae82736807a01d1691d2d45552
ms.sourcegitcommit: 3d48e198e706f22ac903b346cadda06b2368dd1e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/11/2021
ms.locfileid: "50727466"
---
# <a name="ad-fs-migration-steps-for-the-migration-from-microsoft-cloud-deutschland"></a><span data-ttu-id="97fae-103">Étapes de migration AD FS pour la migration à partir de Microsoft Cloud Deutschland</span><span class="sxs-lookup"><span data-stu-id="97fae-103">AD FS migration steps for the migration from Microsoft Cloud Deutschland</span></span>

<span data-ttu-id="97fae-104">Cette modification de configuration peut être appliquée à tout moment avant le démarrage de la phase 4.</span><span class="sxs-lookup"><span data-stu-id="97fae-104">This configuration change can be applied at any time before phase 4 is starting.</span></span>
<span data-ttu-id="97fae-105">Une fois la phase 2 terminée, la modification de configuration fonctionne et vous pouvez vous connectez aux points de terminaison globaux Office 365 tels que `https://portal.office.com` .</span><span class="sxs-lookup"><span data-stu-id="97fae-105">Once phase 2 is completed the configuration change will work and you are able to sign in to Office 365 Global endpoints such as `https://portal.office.com`.</span></span> <span data-ttu-id="97fae-106">Si vous implémentez la modification de configuration avant la phase 2, les points de terminaison globaux Office 365 ne fonctionneront pas encore, mais la nouvelle confiance de partie de confiance fait toujours partie de votre configuration AD FS (Active Directory Federation Services). </span><span class="sxs-lookup"><span data-stu-id="97fae-106">If you are implementing the configuration change before phase 2, the Office 365 Global endpoints will _not yet work_ but the new relying party trust is still part of your Active Directory Federation Services (AD FS) configuration.</span></span>

<span data-ttu-id="97fae-107">Pour migrer votre batterie de serveurs AD FS à partir de Microsoft Cloud Deutschland :</span><span class="sxs-lookup"><span data-stu-id="97fae-107">To migrate your AD FS farm from Microsoft Cloud Deutschland:</span></span>

1. <span data-ttu-id="97fae-108">Back up your AD FS settings including FF trust info with [these steps](#backup).</span><span class="sxs-lookup"><span data-stu-id="97fae-108">Back up your AD FS settings including FF trust info with [these steps](#backup).</span></span> <span data-ttu-id="97fae-109">Nommez l’Deutschland_Only Microsoft **Cloud** de sauvegarde pour indiquer qu’elle ne possède que les informations client Microsoft Cloud Deutschland.</span><span class="sxs-lookup"><span data-stu-id="97fae-109">Name the backup **Microsoft Cloud Deutschland_Only** to indicate it only has the Microsoft Cloud Deutschland tenant info.</span></span>
2. <span data-ttu-id="97fae-110">Testez la restauration à l’aide de la sauvegarde microsoft cloud Deutschland_Only, la batterie AD FS doit continuer à fonctionner en tant que Microsoft Cloud Deutschland uniquement.</span><span class="sxs-lookup"><span data-stu-id="97fae-110">Test the restore using the Microsoft Cloud Deutschland_Only backup, The AD FS farm should continue to operate as Microsoft Cloud Deutschland only.</span></span>

<span data-ttu-id="97fae-111">Une fois que vous avez terminé et testé la sauvegarde AD FS, effectuez les étapes suivantes pour ajouter une nouvelle confiance de partie de confiance à votre configuration ADFS :</span><span class="sxs-lookup"><span data-stu-id="97fae-111">Once you have completed and tested the AD FS backup, perform the following steps to add a new relying party trust to your ADFS configuration:</span></span>

1. <span data-ttu-id="97fae-112">Ouvrir la console de gestion AD FS</span><span class="sxs-lookup"><span data-stu-id="97fae-112">Open the AD FS management console</span></span>
2. <span data-ttu-id="97fae-113">Dans le volet gauche de la console de gestion **ADFS, développez ADFS,** puis **Relations** d’confiance, puis **Trusting Party Trusts**</span><span class="sxs-lookup"><span data-stu-id="97fae-113">In the left pane of the ADFS management console, expand **ADFS**, then **Trust Relationships**, then **Relying Party Trusts**</span></span>
3. <span data-ttu-id="97fae-114">Dans le volet droit, sélectionnez **Ajouter une confiance de partie de confiance...**</span><span class="sxs-lookup"><span data-stu-id="97fae-114">In the right pane, select **Add Relying Party Trust...**</span></span>
4. <span data-ttu-id="97fae-115">Sélectionnez **Suivant** sur la page **d’accueil** de l’Assistant Ajouter une confiance de partie de confiance.</span><span class="sxs-lookup"><span data-stu-id="97fae-115">Select **Next** on the **Welcome** page of the Add Relying Party Trust wizard.</span></span>
5. <span data-ttu-id="97fae-116">Dans la page **Sélectionner une source de données,** sélectionnez Importer des données sur la partie de confiance publiée en ligne ou sur un réseau **local.**</span><span class="sxs-lookup"><span data-stu-id="97fae-116">On the **Select Data Source** page, select **Import data about the relying party published online or on a local network**.</span></span> <span data-ttu-id="97fae-117">La **valeur d’adresse de métadonnées de** fédération (nom d’hôte ou URL) doit être définie sur `https://nexus.microsoftonline-p.com/federationmetadata/2007-06/federationmetadata.xml` .</span><span class="sxs-lookup"><span data-stu-id="97fae-117">The **Federation metadata address (host name or URL)** value must be set to `https://nexus.microsoftonline-p.com/federationmetadata/2007-06/federationmetadata.xml`.</span></span> <span data-ttu-id="97fae-118">Ensuite, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="97fae-118">Then, click **Next**.</span></span>
6. <span data-ttu-id="97fae-119">Dans la page **Sélectionner une source de** données, tapez le nom complet tel que Microsoft Office **365 Identity Platform WorldWide**.</span><span class="sxs-lookup"><span data-stu-id="97fae-119">On the **Select Data Source** page, type the display name such as **Microsoft Office 365 Identity Platform WorldWide**.</span></span> <span data-ttu-id="97fae-120">Ensuite, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="97fae-120">Then, click **Next**.</span></span>
7. <span data-ttu-id="97fae-121">Dans la page de l’Assistant **Configurer l’authentification multifacteur maintenant ?**, sélectionnez le choix approprié en fonction de vos exigences d’authentification.</span><span class="sxs-lookup"><span data-stu-id="97fae-121">On the wizard page **Configure Multi-factor Authentication Now?**, select the appropriate choice according to your authentication requirements.</span></span> <span data-ttu-id="97fae-122">Si vous respectez la valeur par défaut, sélectionnez je ne souhaite pas configurer de **paramètres d’authentification multifacteur** pour cette relation d’confiance pour le moment.</span><span class="sxs-lookup"><span data-stu-id="97fae-122">If you stick with the default, select **I don't want to configure multi-factor authentication settings for this relying party trust at this time**.</span></span> <span data-ttu-id="97fae-123">Vous pouvez modifier ce paramètre ultérieurement si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="97fae-123">You can change this setting later if you want to.</span></span>
8. <span data-ttu-id="97fae-124">Dans la **sélection des règles d’autorisation d’émission,** conservez autoriser tous les utilisateurs à accéder à cette **partie de** confiance sélectionnée en **cliquant** sur Suivant</span><span class="sxs-lookup"><span data-stu-id="97fae-124">On the **Choose Issuance Authorization Rules**, keep **Permit all users to access this relying party** selected click **Next**</span></span>
9. <span data-ttu-id="97fae-125">Cliquez **sur Suivant** dans la page Prêt à ajouter **une** confiance pour terminer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="97fae-125">Click **Next** on the **Ready to Add Trust** page to complete the wizard.</span></span>
10. <span data-ttu-id="97fae-126">Cliquez **sur Fermer** sur la page Terminer. </span><span class="sxs-lookup"><span data-stu-id="97fae-126">Click **Close** on the **Finish** page.</span></span>

<span data-ttu-id="97fae-127">En fermant l’Assistant, l’confiance de partie de confiance avec les services globaux Office 365 est établie.</span><span class="sxs-lookup"><span data-stu-id="97fae-127">By closing the wizard, the Relying Party Trust with the Office 365 Global services is established.</span></span> <span data-ttu-id="97fae-128">Toutefois, aucune règle de transformation d’émission n’est encore configurée.</span><span class="sxs-lookup"><span data-stu-id="97fae-128">However, no Issuance Transform rules are configured yet.</span></span>

<span data-ttu-id="97fae-129">Vous pouvez utiliser [l’aide AD FS](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator) pour générer les règles de transformation d’émission correctes.</span><span class="sxs-lookup"><span data-stu-id="97fae-129">You can use [AD FS Help](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator) to generate the correct Issuance Transform rules.</span></span> <span data-ttu-id="97fae-130">Les règles de revendication générées créées avec l’aide d’AD FS peuvent être ajoutées manuellement via la console de gestion AD FS ou avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="97fae-130">The generated claim rules created with AD FS Help can either be manually added through the AD FS management console or with PowerShell.</span></span> <span data-ttu-id="97fae-131">L’aide des AD FS génère les scripts PowerShell nécessaires à l’exécution.</span><span class="sxs-lookup"><span data-stu-id="97fae-131">AD FS Help will generate the necessary PowerShell scripts that need to be executed.</span></span>  

<!--
    Question from ckinder
    is step #3 true?
    how to verify step 5? Need more information!
-->
1. <span data-ttu-id="97fae-132">Exécutez **l’aide** Générer des revendications sur AD FS  et copiez le script de transformation de revendications PowerShell à l’aide de l’option Copier dans le coin supérieur droit du script.</span><span class="sxs-lookup"><span data-stu-id="97fae-132">Run **Generate Claims** on AD FS help and copy the PowerShell claims transformation script using the **Copy** option on the right upper corner of the script.</span></span>
2. <span data-ttu-id="97fae-133">Ouvrez votre éditeur de texte préféré et collez le script PowerShell dans une nouvelle fenêtre de texte.</span><span class="sxs-lookup"><span data-stu-id="97fae-133">Open your preferred text editor and paste the PowerShell script into a new text window.</span></span>
3. <span data-ttu-id="97fae-134">Ajoutez les lignes PowerShell suivantes à la fin du script passé à l’étape 2</span><span class="sxs-lookup"><span data-stu-id="97fae-134">Add the following PowerShell lines to the end of the pasted script from step 2</span></span>
    ```powershell
    $authzRules = "=>issue(Type = `"http://schemas.microsoft.com/authorization/claims/permit`", Value = `"true`"); "
    $RuleSet = New-AdfsClaimRuleSet -ClaimRule "<AD FS Help generated PSH>"
    Set-AdfsRelyingPartyTrust -TargetName “Microsoft Office 365 Identity Platform WorldWide” -IssuanceTransformRules $RuleSet.ClaimRulesString -IssuanceAuthorizationRules $authzRules
    ```
4. <span data-ttu-id="97fae-135">Exécutez le script PowerShell en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="97fae-135">Safe and execute the PowerShell script.</span></span>
5. <span data-ttu-id="97fae-136">Vérifiez que deux confiances de partie de confiance sont présentes ; un pour Microsoft Cloud Deutschland et un pour le service global Office 365.</span><span class="sxs-lookup"><span data-stu-id="97fae-136">Verify that two Relying Party trusts are present; one for the Microsoft Cloud Deutschland and one for the Office 365 Global service.</span></span>
6. <span data-ttu-id="97fae-137">Sauvegardez vos confiances à [l’aide de ces étapes.](#backup)</span><span class="sxs-lookup"><span data-stu-id="97fae-137">Backup your trusts using [these steps](#backup).</span></span> <span data-ttu-id="97fae-138">Enregistrez-le sous le nom **FFAndWorldwide**.</span><span class="sxs-lookup"><span data-stu-id="97fae-138">Save it with the name **FFAndWorldwide**.</span></span>
7. <span data-ttu-id="97fae-139">Terminez votre migration back-end et vérifiez que les AD FS fonctionnent toujours pendant le processus de migration.</span><span class="sxs-lookup"><span data-stu-id="97fae-139">Complete your backend migration and verify that AD FS still works during the migration process.</span></span>

## <a name="ad-fs-disaster-recovery-wid-database"></a><span data-ttu-id="97fae-140">Récupération d’urgence AD FS (base de données WID)</span><span class="sxs-lookup"><span data-stu-id="97fae-140">AD FS Disaster Recovery (WID Database)</span></span>

<span data-ttu-id="97fae-141">Pour restaurer la batterie de serveurs AD FS en cas d’urgence, l’outil de restauration rapide [AD FS](https://docs.microsoft.com/windows-server/identity/ad-fs/operations/ad-fs-rapid-restore-tool) doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="97fae-141">To restore the AD FS farm in a disaster [AD FS Rapid Restore Tool](https://docs.microsoft.com/windows-server/identity/ad-fs/operations/ad-fs-rapid-restore-tool) needs to be leveraged.</span></span> <span data-ttu-id="97fae-142">Par conséquent, l’outil doit être téléchargé et avant le début de la migration, une sauvegarde doit être créée et stockée en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="97fae-142">Therefore, the tool must be downloaded and before the start of the migration a backup must be created and safely stored.</span></span> <span data-ttu-id="97fae-143">Dans cet exemple (environnements TAT), les commandes suivantes ont été exécutés pour la back up de la batterie de serveurs :</span><span class="sxs-lookup"><span data-stu-id="97fae-143">In this example (TAT environments) the following commands have been run to back up the farm:</span></span>

<h2 id="backup"></h2>

### <a name="back-up-an-ad-fs-farm"></a><span data-ttu-id="97fae-144">Back up an AD FS Farm</span><span class="sxs-lookup"><span data-stu-id="97fae-144">Back up an AD FS Farm</span></span>

1. <span data-ttu-id="97fae-145">Installez l’outil de restauration rapide AD FS sur le serveur AD FS principal.</span><span class="sxs-lookup"><span data-stu-id="97fae-145">Install the AD FS Rapid Restore Tool on the primary AD FS server.</span></span>
2. <span data-ttu-id="97fae-146">Importez le module dans une session PowerShell avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="97fae-146">Import the module in a PowerShell session with this command.</span></span>
    ```powershell
    Import-Module "C:\Program Files (x86)\ADFS Rapid Recreation Tool\ADFSRapidRecreationTool.dll"
    ```
3. <span data-ttu-id="97fae-147">Exécutez la commande de sauvegarde :</span><span class="sxs-lookup"><span data-stu-id="97fae-147">Run the backup command:</span></span>
    ```powershell
    Backup-ADFS -StorageType "FileSystem" -storagePath "<Storage path of backup>" -EncryptionPassword "<password>" -BackupComment "Restore Doku" -BackupDKM
    ```
4. <span data-ttu-id="97fae-148">Stockez la sauvegarde en toute sécurité sur la destination souhaitée.</span><span class="sxs-lookup"><span data-stu-id="97fae-148">Store the backup safely on a desired destination.</span></span>

### <a name="restore-an-ad-fs-farm"></a><span data-ttu-id="97fae-149">Restaurer une batterie de serveurs AD FS</span><span class="sxs-lookup"><span data-stu-id="97fae-149">Restore an AD FS Farm</span></span>

<span data-ttu-id="97fae-150">Si votre batterie de serveurs a complètement échoué et qu’il n’existe aucun moyen de revenir à l’ancienne batterie de serveurs, faites ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="97fae-150">If your farm failed completely and there is no way to return to the old farm, do the following.</span></span> 

1. <span data-ttu-id="97fae-151">Déplacez la sauvegarde précédemment générée et stockée vers le nouveau serveur AD FS principal.</span><span class="sxs-lookup"><span data-stu-id="97fae-151">Move the previously generated and stored backup to the new primary AD FS server.</span></span>
2. <span data-ttu-id="97fae-152">Exécutez la commande `Restore-ADFS` PowerShell suivante.</span><span class="sxs-lookup"><span data-stu-id="97fae-152">Run the following `Restore-ADFS` PowerShell command.</span></span> <span data-ttu-id="97fae-153">Si nécessaire, importez au préalable le certificat SSL AD FS.</span><span class="sxs-lookup"><span data-stu-id="97fae-153">If necessary, import the AD FS SSL certificate beforehand.</span></span>

    ```powershell
    Restore-ADFS -StorageType "FileSystem" -StoragePath "<Path to Backup>" -DecryptionPassword "<password>" -GroupServiceAccountIdentifier "<gMSA>" -DBConnectionString "WID" -RestoreDKM
    ```

3. <span data-ttu-id="97fae-154">Pointez vos nouveaux enregistrements DNS ou équilibreur de charge vers les nouveaux serveurs AD FS.</span><span class="sxs-lookup"><span data-stu-id="97fae-154">Point your new DNS records or load balancer to the new AD FS servers.</span></span>

## <a name="more-information"></a><span data-ttu-id="97fae-155">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="97fae-155">More information</span></span>

<span data-ttu-id="97fae-156">Mise en place :</span><span class="sxs-lookup"><span data-stu-id="97fae-156">Getting started:</span></span>

- [<span data-ttu-id="97fae-157">Migration de Microsoft Cloud Deutschland vers les services Office 365 dans les nouvelles régions de centres de données allemandes</span><span class="sxs-lookup"><span data-stu-id="97fae-157">Migration from Microsoft Cloud Deutschland to Office 365 services in the new German datacenter regions</span></span>](ms-cloud-germany-transition.md)
- [<span data-ttu-id="97fae-158">Aide à la migration de Microsoft Cloud Deutschland : </span><span class="sxs-lookup"><span data-stu-id="97fae-158">Microsoft Cloud Deutschland Migration Assistance</span></span>](https://aka.ms/germanymigrateassist)
- [<span data-ttu-id="97fae-159">Comment opter pour une migration</span><span class="sxs-lookup"><span data-stu-id="97fae-159">How to opt-in for migration</span></span>](ms-cloud-germany-migration-opt-in.md)
- [<span data-ttu-id="97fae-160">Expérience client pendant la migration</span><span class="sxs-lookup"><span data-stu-id="97fae-160">Customer experience during the migration</span></span>](ms-cloud-germany-transition-experience.md)

<span data-ttu-id="97fae-161">Transition :</span><span class="sxs-lookup"><span data-stu-id="97fae-161">Moving through the transition:</span></span>

- [<span data-ttu-id="97fae-162">Actions et impacts des phases de migration</span><span class="sxs-lookup"><span data-stu-id="97fae-162">Migration phases actions and impacts</span></span>](ms-cloud-germany-transition-phases.md)
- [<span data-ttu-id="97fae-163">Pré-travail supplémentaire</span><span class="sxs-lookup"><span data-stu-id="97fae-163">Additional pre-work</span></span>](ms-cloud-germany-transition-add-pre-work.md)
- <span data-ttu-id="97fae-164">Informations supplémentaires pour [Azure AD,](ms-cloud-germany-transition-azure-ad.md) [les appareils,](ms-cloud-germany-transition-add-devices.md) [les expériences](ms-cloud-germany-transition-add-experience.md)et [AD FS](ms-cloud-germany-transition-add-adfs.md).</span><span class="sxs-lookup"><span data-stu-id="97fae-164">Additional information for [Azure AD](ms-cloud-germany-transition-azure-ad.md), [devices](ms-cloud-germany-transition-add-devices.md), [experiences](ms-cloud-germany-transition-add-experience.md), and [AD FS](ms-cloud-germany-transition-add-adfs.md).</span></span>

<span data-ttu-id="97fae-165">Applications cloud :</span><span class="sxs-lookup"><span data-stu-id="97fae-165">Cloud apps:</span></span>

- [<span data-ttu-id="97fae-166">Informations sur le programme de migration Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="97fae-166">Dynamics 365 migration program information</span></span>](https://aka.ms/d365ceoptin)
- [<span data-ttu-id="97fae-167">Informations sur le programme de migration Power BI</span><span class="sxs-lookup"><span data-stu-id="97fae-167">Power BI migration program information</span></span>](https://aka.ms/pbioptin)
- [<span data-ttu-id="97fae-168">Prise en main de votre mise à niveau vers Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="97fae-168">Getting started with your Microsoft Teams upgrade</span></span>](https://aka.ms/SkypeToTeams-Home)
