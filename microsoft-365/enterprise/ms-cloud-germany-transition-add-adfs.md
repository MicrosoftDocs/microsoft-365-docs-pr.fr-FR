---
title: Étapes de migration d’AD FS pour la migration à partir de Microsoft Cloud Deutschland
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
description: 'Résumé : étapes de migration des services ADFS (Active Directory Federation Services) pour la migration à partir de Microsoft Cloud Deutschland.'
ms.openlocfilehash: 175734851c2838eb2e224a9afb57a600d4ed9523
ms.sourcegitcommit: 38d828ae8d4350ae774a939c8decf30cb36c3bea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/02/2020
ms.locfileid: "49554797"
---
# <a name="ad-fs-migration-steps-for-the-migration-from-microsoft-cloud-deutschland"></a><span data-ttu-id="6c112-103">Étapes de migration d’AD FS pour la migration à partir de Microsoft Cloud Deutschland</span><span class="sxs-lookup"><span data-stu-id="6c112-103">AD FS migration steps for the migration from Microsoft Cloud Deutschland</span></span>

<span data-ttu-id="6c112-104">Pour migrer votre batterie de serveurs AD FS (Active Directory Federation Services) à partir de Microsoft Cloud Deutschland :</span><span class="sxs-lookup"><span data-stu-id="6c112-104">To migrate your Active Directory Federation Services (AD FS) farm from Microsoft Cloud Deutschland:</span></span>

1. <span data-ttu-id="6c112-105">Sauvegardez vos paramètres AD FS, y compris les informations de confiance de FF, en [procédant comme suit](#backup).</span><span class="sxs-lookup"><span data-stu-id="6c112-105">Back up your AD FS settings including FF trust info with [these steps](#backup).</span></span> <span data-ttu-id="6c112-106">Nommez la sauvegarde **Cloud microsoft Deutschland_Only** pour indiquer qu’elle contient uniquement les informations du client Microsoft Cloud Deutschland.</span><span class="sxs-lookup"><span data-stu-id="6c112-106">Name the backup **Microsoft Cloud Deutschland_Only** to indicate it only has the Microsoft Cloud Deutschland tenant info.</span></span>
2. <span data-ttu-id="6c112-107">Test de la restauration à l’aide de Microsoft Cloud Deutschland_Only Backup, la batterie AD FS doit continuer à fonctionner en tant que Microsoft Cloud Deutschland uniquement.</span><span class="sxs-lookup"><span data-stu-id="6c112-107">Test the restore using the Microsoft Cloud Deutschland_Only backup, The AD FS farm should continue to operate as Microsoft Cloud Deutschland only.</span></span>
3. <span data-ttu-id="6c112-108">Créer une approbation de partie de confiance à partir des **services AD FS > Office 365**.</span><span class="sxs-lookup"><span data-stu-id="6c112-108">Create a new Relying Party trust from **AD FS >  Office 365 services**.</span></span>
4. <span data-ttu-id="6c112-109">Dans **approbations de partie de confiance** dans la console de gestion AD FS, sélectionnez **Ajouter une approbation de partie de confiance**.</span><span class="sxs-lookup"><span data-stu-id="6c112-109">In **Relying Party Trusts** in the AD FS management console, select **Add Relying Party Trust**.</span></span>
5. <span data-ttu-id="6c112-110">Sélectionnez **suivant** dans la page d' **Accueil** de l’Assistant Ajout d’approbation de partie de confiance.</span><span class="sxs-lookup"><span data-stu-id="6c112-110">Select **Next** on the **Welcome** page of the Add Relying Party Trust wizard.</span></span>
6. <span data-ttu-id="6c112-111">Dans la page **Sélectionner la source de données** , sélectionnez **Importer les données relatives à la partie de confiance publiée en ligne ou sur un réseau local**.</span><span class="sxs-lookup"><span data-stu-id="6c112-111">On the **Select Data Source** page, select **Import data about the relying party published online or on a local network**.</span></span> <span data-ttu-id="6c112-112">La valeur de l' **adresse de métadonnées de Fédération (nom d’hôte ou URL)** est définie sur `https://nexus.microsoftonline-p.com/federationmetadata/2007-06/federationmetadata.xml` .</span><span class="sxs-lookup"><span data-stu-id="6c112-112">The **Federation metadata address (host name or URL)** value is set to `https://nexus.microsoftonline-p.com/federationmetadata/2007-06/federationmetadata.xml`.</span></span> <span data-ttu-id="6c112-113">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6c112-113">Click **Next**.</span></span>
7. <span data-ttu-id="6c112-114">Dans la page **Sélectionner la source de données** , tapez le nom complet.</span><span class="sxs-lookup"><span data-stu-id="6c112-114">On the **Select Data Source** page, type the display name.</span></span> <span data-ttu-id="6c112-115">Microsoft recommande la **plateforme d’identité Microsoft Office 365 dans le monde**.</span><span class="sxs-lookup"><span data-stu-id="6c112-115">Microsoft recommends **Microsoft Office 365 Identity Platform WorldWide**.</span></span> <span data-ttu-id="6c112-116">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6c112-116">Click **Next**.</span></span>
8. <span data-ttu-id="6c112-117">Cliquez sur **suivant** dans la page **configurer l’authentification multifacteur maintenant ?**, **Choisissez règles d’autorisation d’émission** et **prêt à ajouter** des pages d’approbation.</span><span class="sxs-lookup"><span data-stu-id="6c112-117">Click **Next** on the **Configure Multi-factor Authentication Now?**, **Choose Issuance Authorization Rules**, and **Ready to Add Trust** pages.</span></span>
9. <span data-ttu-id="6c112-118">Cliquez sur **Fermer** sur la page **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="6c112-118">Click **Close** on the **Finish** page.</span></span>

<span data-ttu-id="6c112-119">En fermant l’Assistant, l’approbation de la partie de confiance pour le service Office 365 services eSTS est établie.</span><span class="sxs-lookup"><span data-stu-id="6c112-119">By closing the wizard, the Relying Party Trust to the Office 365 services eSTS is established.</span></span> <span data-ttu-id="6c112-120">Toutefois, aucune règle de transformation d’émission n’est établie.</span><span class="sxs-lookup"><span data-stu-id="6c112-120">However, no Issuance Transform rules are established.</span></span>

<span data-ttu-id="6c112-121">Vous pouvez utiliser l' [aide d’AD FS](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator) pour générer les règles de transformation d’émission correctes.</span><span class="sxs-lookup"><span data-stu-id="6c112-121">You can use [AD FS Help](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator) to generate the correct Issuance Transform rules.</span></span> <span data-ttu-id="6c112-122">Les règles de revendication générées créées avec l’aide d’AD FS peuvent être ajoutées manuellement via la console de gestion AD FS ou avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6c112-122">The generated claim rules created with AD FS Help can either be manually added through the AD FS management console or with PowerShell.</span></span> <span data-ttu-id="6c112-123">L’aide d’AD FS génère les scripts PowerShell nécessaires à exécuter.</span><span class="sxs-lookup"><span data-stu-id="6c112-123">AD FS Help will generate the necessary PowerShell scripts that need to be run.</span></span>  

1. <span data-ttu-id="6c112-124">Exécutez **générer des revendications** sur l’aide d’AD FS et copiez le script de transformation de revendications PowerShell à l’aide de l’option de **copie** située dans le coin supérieur droit du script.</span><span class="sxs-lookup"><span data-stu-id="6c112-124">Run **Generate Claims** on AD FS help and copy the PowerShell claims transformation script using the **Copy** option on the right upper corner of the script.</span></span>
2. <span data-ttu-id="6c112-125">Collez le PowerShell généré dans ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="6c112-125">Paste the generated PowerShell into the following:</span></span>

  ```powershell
  $RuleSet = New-AdfsClaimRuleSet -ClaimRule "<AD FS Help generated PSH>"
  Set-AdfsRelyingPartyTrust -TargetName “Microsoft Office 365 Identity Platform WorldWide” -IssuanceTransformRules $RuleSet.ClaimRulesString;
  ```
3.  <span data-ttu-id="6c112-126">Exécutez le script terminé.</span><span class="sxs-lookup"><span data-stu-id="6c112-126">Execute the completed script.</span></span>
4.  <span data-ttu-id="6c112-127">Vérifier que deux approbations de partie de confiance sont présentes ; un pour le monde entier et un pour BF.</span><span class="sxs-lookup"><span data-stu-id="6c112-127">Verify that two Relying Party trusts are present; one for worldwide and one for BF.</span></span>
5.  <span data-ttu-id="6c112-128">Sauvegardez vos approbations à l’aide de [ces étapes](#backup).</span><span class="sxs-lookup"><span data-stu-id="6c112-128">Backup your trusts using [these steps](#backup).</span></span> <span data-ttu-id="6c112-129">Enregistrez-le sous le nom **FFAndWorldwide**.</span><span class="sxs-lookup"><span data-stu-id="6c112-129">Save it with the name **FFAndWorldwide**.</span></span>
6.  <span data-ttu-id="6c112-130">Terminez votre migration principale et vérifiez qu’AD FS fonctionne toujours pendant le processus de migration.</span><span class="sxs-lookup"><span data-stu-id="6c112-130">Complete your backend migration and verify that AD FS still works during migration process.</span></span>

## <a name="ad-fs-disaster-recovery-wid-database"></a><span data-ttu-id="6c112-131">Récupération d’urgence AD FS (base de données WID)</span><span class="sxs-lookup"><span data-stu-id="6c112-131">AD FS Disaster Recovery (WID Database)</span></span>

<span data-ttu-id="6c112-132">La restauration de la batterie AD FS dans un incident de [restauration rapide AD FS](https://docs.microsoft.com/windows-server/identity/ad-fs/operations/ad-fs-rapid-restore-tool) doit être exploitée.</span><span class="sxs-lookup"><span data-stu-id="6c112-132">To restore the AD FS farm in a disaster [AD FS Rapid Restore Tool](https://docs.microsoft.com/windows-server/identity/ad-fs/operations/ad-fs-rapid-restore-tool) needs to be leveraged.</span></span> <span data-ttu-id="6c112-133">Par conséquent, l’outil doit être téléchargé et avant le début de la migration, une sauvegarde doit être créée et stockée en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="6c112-133">Therefore, the tool must be downloaded and before the start of the migration a backup must be created and safely stored.</span></span> <span data-ttu-id="6c112-134">Dans cet exemple (environnements TAT), les commandes suivantes ont été exécutées pour sauvegarder la batterie de serveurs :</span><span class="sxs-lookup"><span data-stu-id="6c112-134">In this example (TAT environments) the following commands have been run to back up the farm:</span></span>

<h2 id="backup"></h2>

### <a name="back-up-an-ad-fs-farm"></a><span data-ttu-id="6c112-135">Sauvegarder une batterie AD FS</span><span class="sxs-lookup"><span data-stu-id="6c112-135">Back up an AD FS Farm</span></span>

1. <span data-ttu-id="6c112-136">Installez l’outil de restauration rapide AD FS sur le serveur AD FS principal.</span><span class="sxs-lookup"><span data-stu-id="6c112-136">Install the AD FS Rapid Restore Tool on the primary AD FS server.</span></span>
2. <span data-ttu-id="6c112-137">Importez le module dans une session PowerShell à l’aide de cette commande.</span><span class="sxs-lookup"><span data-stu-id="6c112-137">Import the module in a PowerShell session with this command.</span></span>

  ```powershell
  Import-Module "C:\Program Files (x86)\ADFS Rapid Recreation Tool\ADFSRapidRecreationTool.dll"
  ```
3. <span data-ttu-id="6c112-138">Exécutez la commande Backup :</span><span class="sxs-lookup"><span data-stu-id="6c112-138">Run the backup command:</span></span>

  ```powershell
  Backup-ADFS -StorageType "FileSystem" -storagePath "<Storage path of backup>" -EncryptionPassword "<password>" -BackupComment "Restore Doku" -BackupDKM
  ```

4. <span data-ttu-id="6c112-139">Stockez la sauvegarde en toute sécurité sur une destination souhaitée.</span><span class="sxs-lookup"><span data-stu-id="6c112-139">Store the backup safely on a desired destination.</span></span> 

### <a name="restore-an-ad-fs-farm"></a><span data-ttu-id="6c112-140">Restaurer une batterie de serveurs AD FS</span><span class="sxs-lookup"><span data-stu-id="6c112-140">Restore an AD FS Farm</span></span>

<span data-ttu-id="6c112-141">Si votre batterie de serveurs a échoué complètement et qu’il n’existe aucun moyen de revenir à l’ancienne batterie de serveurs, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="6c112-141">If your farm failed completely and there is no way to return to the old farm, do the following.</span></span> 

1. <span data-ttu-id="6c112-142">Déplacez la sauvegarde précédemment générée et stockée sur le nouveau serveur AD FS principal.</span><span class="sxs-lookup"><span data-stu-id="6c112-142">Move the previously generated and stored backup to the new primary AD FS server.</span></span>
2. <span data-ttu-id="6c112-143">Exécutez la `Restore-ADFS` commande PowerShell suivante.</span><span class="sxs-lookup"><span data-stu-id="6c112-143">Run the following `Restore-ADFS` PowerShell command.</span></span> <span data-ttu-id="6c112-144">Si nécessaire, importez le certificat SSL AD FS à l’avance.</span><span class="sxs-lookup"><span data-stu-id="6c112-144">If necessary, import the AD FS SSL certificate beforehand.</span></span>

  ```powershell
  Restore-ADFS -StorageType "FileSystem" -StoragePath "<Path to Backup>" -DecryptionPassword "<password>" -GroupServiceAccountIdentifier "<gMSA>" -DBConnectionString "WID" -RestoreDKM
  ```

3. <span data-ttu-id="6c112-145">Pointez vos nouveaux enregistrements DNS ou équilibreur de charge vers les nouveaux serveurs AD FS.</span><span class="sxs-lookup"><span data-stu-id="6c112-145">Point your new DNS records or load balancer to the new AD FS servers.</span></span>

## <a name="more-information"></a><span data-ttu-id="6c112-146">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6c112-146">More information</span></span>

<span data-ttu-id="6c112-147">Mise en route :</span><span class="sxs-lookup"><span data-stu-id="6c112-147">Getting started:</span></span>

- [<span data-ttu-id="6c112-148">Migration de Microsoft Cloud Deutschland vers Office 365 services dans les nouvelles régions de centre de connaissances allemand</span><span class="sxs-lookup"><span data-stu-id="6c112-148">Migration from Microsoft Cloud Deutschland to Office 365 services in the new German datacenter regions</span></span>](ms-cloud-germany-transition.md)
- [<span data-ttu-id="6c112-149">Aide à la migration de Microsoft Cloud Deutschland : </span><span class="sxs-lookup"><span data-stu-id="6c112-149">Microsoft Cloud Deutschland Migration Assistance</span></span>](https://aka.ms/germanymigrateassist)
- [<span data-ttu-id="6c112-150">Comment opter pour une migration</span><span class="sxs-lookup"><span data-stu-id="6c112-150">How to opt-in for migration</span></span>](ms-cloud-germany-migration-opt-in.md)
- [<span data-ttu-id="6c112-151">Expérience client lors de la migration</span><span class="sxs-lookup"><span data-stu-id="6c112-151">Customer experience during the migration</span></span>](ms-cloud-germany-transition-experience.md)

<span data-ttu-id="6c112-152">Navigation par le biais de la transition :</span><span class="sxs-lookup"><span data-stu-id="6c112-152">Moving through the transition:</span></span>

- [<span data-ttu-id="6c112-153">Actions et impacts sur les phases de migration</span><span class="sxs-lookup"><span data-stu-id="6c112-153">Migration phases actions and impacts</span></span>](ms-cloud-germany-transition-phases.md)
- [<span data-ttu-id="6c112-154">Pré-travail supplémentaire</span><span class="sxs-lookup"><span data-stu-id="6c112-154">Additional pre-work</span></span>](ms-cloud-germany-transition-add-pre-work.md)
- <span data-ttu-id="6c112-155">Informations supplémentaires pour les [services](ms-cloud-germany-transition-add-general.md), les [appareils](ms-cloud-germany-transition-add-devices.md), les [expériences](ms-cloud-germany-transition-add-experience.md)et [AD FS](ms-cloud-germany-transition-add-adfs.md).</span><span class="sxs-lookup"><span data-stu-id="6c112-155">Additional information for [services](ms-cloud-germany-transition-add-general.md), [devices](ms-cloud-germany-transition-add-devices.md), [experiences](ms-cloud-germany-transition-add-experience.md), and [AD FS](ms-cloud-germany-transition-add-adfs.md).</span></span>

<span data-ttu-id="6c112-156">Applications Cloud :</span><span class="sxs-lookup"><span data-stu-id="6c112-156">Cloud apps:</span></span>

- [<span data-ttu-id="6c112-157">Informations sur le programme de migration Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6c112-157">Dynamics 365 migration program information</span></span>](https://aka.ms/d365ceoptin)
- [<span data-ttu-id="6c112-158">Informations sur le programme de migration Power BI</span><span class="sxs-lookup"><span data-stu-id="6c112-158">Power BI migration program information</span></span>](https://aka.ms/pbioptin)
- [<span data-ttu-id="6c112-159">Prise en main de votre mise à niveau vers Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6c112-159">Getting started with your Microsoft Teams upgrade</span></span>](https://aka.ms/SkypeToTeams-Home)
