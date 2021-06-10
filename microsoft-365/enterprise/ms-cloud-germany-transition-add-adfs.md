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
ms.openlocfilehash: 12465acf5b4afe7e252586ddd076250628b57dd3
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51165656"
---
# <a name="ad-fs-migration-steps-for-the-migration-from-microsoft-cloud-deutschland"></a><span data-ttu-id="2e1b0-103">Étapes de migration AD FS pour la migration à partir de Microsoft Cloud Deutschland</span><span class="sxs-lookup"><span data-stu-id="2e1b0-103">AD FS migration steps for the migration from Microsoft Cloud Deutschland</span></span>

<span data-ttu-id="2e1b0-104">Cette modification de configuration doit être appliquée à tout moment avant le démarrage de la phase 2.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-104">This configuration change needs to be applied any time before phase 2 is starting.</span></span>
<span data-ttu-id="2e1b0-105">Une fois la phase 2 terminée, la modification de configuration fonctionne et vous pouvez vous Office 365 des points de terminaison globaux tels que `https://portal.office.com` .</span><span class="sxs-lookup"><span data-stu-id="2e1b0-105">Once phase 2 is completed the configuration change will work and you are able to sign in via Office 365 Global endpoints such as `https://portal.office.com`.</span></span> <span data-ttu-id="2e1b0-106">Si vous implémentez la modification de configuration avant la phase  2, les points de terminaison globaux Office 365 ne fonctionneront pas encore, mais la nouvelle confiance de partie de confiance fait toujours partie de votre configuration des services AD FS (Active Directory Federation Services).</span><span class="sxs-lookup"><span data-stu-id="2e1b0-106">If you are implementing the configuration change before phase 2, the Office 365 Global endpoints will _not yet work_ but the new relying party trust is still part of your Active Directory Federation Services (AD FS) configuration.</span></span>

<span data-ttu-id="2e1b0-107">Les clients qui utilisent l’authentification fédérée avec les services AD FS (Active Directory Federation Services) ne doivent pas apporter de modifications aux AUTHENTIFICATION d’émetteur utilisées pour toutes les authentifications avec les services de domaine Active Directory (AD DS) locaux lors de la migration.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-107">Customers who use federated authentication with Active Directory Federation Services (AD FS) shouldn't make changes to issuer URIs that are used for all authentications with on-premises Active Directory Domain Services (AD DS) during migration.</span></span> <span data-ttu-id="2e1b0-108">La modification des URL d’émetteur entraîne des échecs d’authentification pour les utilisateurs du domaine.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-108">Changing issuer URIs will lead to authentication failures for users in the domain.</span></span> <span data-ttu-id="2e1b0-109">Les URIs d’émetteur peuvent être modifiés directement dans  AD  FS ou lorsqu’un domaine est converti de géré en fédéré et vice-versa.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-109">Issuer URIs can be changed directly in AD FS or when a domain is converted from _managed_ to _federated_ and vice-versa.</span></span> <span data-ttu-id="2e1b0-110">Nous vous recommandons de ne pas ajouter, supprimer ou convertir un domaine fédéré dans le client Azure AD qui a été migré.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-110">We recommend that you do not add, remove, or convert a federated domain in the Azure AD tenant that has been migrated.</span></span> <span data-ttu-id="2e1b0-111">Les URL de l’émetteur peuvent être modifiées une fois la migration terminée.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-111">Issuer URIs can be changed after the migration is fully complete.</span></span>

<span data-ttu-id="2e1b0-112">Pour préparer votre batterie de serveurs AD FS pour la migration à partir de Microsoft Cloud Deutschland, effectuez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2e1b0-112">To prepare your AD FS farm for the migration from Microsoft Cloud Deutschland perform the following steps:</span></span>

1. <span data-ttu-id="2e1b0-113">En suivant ces étapes, vous pouvez également back up your AD FS settings, including the existing Microsoft Cloud Deutschland Relying Party [trust.](#backup)</span><span class="sxs-lookup"><span data-stu-id="2e1b0-113">Back up your AD FS settings, including the existing Microsoft Cloud Deutschland Relying Party trust, with [these steps](#backup).</span></span> <span data-ttu-id="2e1b0-114">Nommez la **sauvegarde MicrosoftCloudDeueulandOnly** pour indiquer qu’elle ne possède que les informations du client Microsoft Cloud Deutschland.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-114">Name the backup **MicrosoftCloudDeutschlandOnly** to indicate it only has the Microsoft Cloud Deutschland tenant info.</span></span>

   > [!NOTE]
   > <span data-ttu-id="2e1b0-115">La sauvegarde contiendra non seulement l’Office 365 trust de partie de confiance existante pour Microsoft Cloud Deutschland, mais également toutes les autres trusts de partie de confiance présentes sur la batterie de serveurs AD FS respective.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-115">The backup will not only contain the existing Office 365 Relying Party Trust for Microsoft Cloud Deutschland, but also all other Relying Party Trusts present on the respective AD FS farm.</span></span>

2. <span data-ttu-id="2e1b0-116">Testez la restauration à l’aide de la sauvegarde MicrosoftCloudDeueulandOnly, la batterie AD FS doit continuer à fonctionner en tant que Microsoft Cloud Deutschland uniquement.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-116">Test the restore using the MicrosoftCloudDeutschlandOnly backup, The AD FS farm should continue to operate as Microsoft Cloud Deutschland only.</span></span>

<span data-ttu-id="2e1b0-117">Une fois que vous avez terminé et testé la sauvegarde AD FS, effectuez les étapes suivantes pour ajouter une nouvelle confiance de partie de confiance à votre configuration ADFS :</span><span class="sxs-lookup"><span data-stu-id="2e1b0-117">Once you have completed and tested the AD FS backup, perform the following steps to add a new relying party trust to your ADFS configuration:</span></span>

1. <span data-ttu-id="2e1b0-118">Ouvrez la console de gestion AD FS.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-118">Open the AD FS management console.</span></span>

2. <span data-ttu-id="2e1b0-119">Dans le volet gauche de la console de gestion ADFS, accédez au menu Des **confiances de** partie de confiance.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-119">In the left pane of the ADFS management console navigate to the **Relying Party Trusts** menu.</span></span>

3. <span data-ttu-id="2e1b0-120">Dans le volet droit, sélectionnez **Ajouter une confiance de partie de confiance...**</span><span class="sxs-lookup"><span data-stu-id="2e1b0-120">In the right pane, select **Add Relying Party Trust...**</span></span>

4. <span data-ttu-id="2e1b0-121">Sélectionnez **Démarrer** sur la page **d’accueil** de l’Assistant Ajouter une confiance de partie de confiance.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-121">Select **Start** on the **Welcome** page of the Add Relying Party Trust wizard.</span></span>

5. <span data-ttu-id="2e1b0-122">Dans la page **Sélectionner une source de données,** sélectionnez Importer des données sur la partie de confiance publiée en ligne ou sur un réseau **local.**</span><span class="sxs-lookup"><span data-stu-id="2e1b0-122">On the **Select Data Source** page, select **Import data about the relying party published online or on a local network**.</span></span> <span data-ttu-id="2e1b0-123">La **valeur d’adresse de métadonnées de** fédération (nom d’hôte ou URL) doit être définie sur `https://nexus.microsoftonline-p.com/federationmetadata/2007-06/federationmetadata.xml` .</span><span class="sxs-lookup"><span data-stu-id="2e1b0-123">The **Federation metadata address (host name or URL)** value must be set to `https://nexus.microsoftonline-p.com/federationmetadata/2007-06/federationmetadata.xml`.</span></span> <span data-ttu-id="2e1b0-124">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-124">Click **Next**.</span></span>

6. <span data-ttu-id="2e1b0-125">Dans la page **Spécifier le nom complet,** tapez le nom complet tel que **Microsoft Office 365 Identity Platform WorldWide**.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-125">On the **Specify Display Name** page, type the display name such as **Microsoft Office 365 Identity Platform WorldWide**.</span></span> <span data-ttu-id="2e1b0-126">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-126">Click **Next**.</span></span>

7. <span data-ttu-id="2e1b0-127">Si vous utilisez ADFS dans Windows Server 2012, dans la page de l’Assistant Configurer l’authentification **multifacteur maintenant ?**, sélectionnez le choix approprié en fonction de vos exigences d’authentification.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-127">If you are using ADFS in Windows Server 2012, on the wizard page **Configure Multi-factor Authentication Now?**, select the appropriate choice according to your authentication requirements.</span></span> <span data-ttu-id="2e1b0-128">Si vous respectez la valeur par défaut, sélectionnez je ne souhaite pas configurer de **paramètres d’authentification multifacteur** pour cette relation d’confiance pour le moment.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-128">If you stick with the default, select **I don't want to configure multi-factor authentication settings for this relying party trust at this time**.</span></span> <span data-ttu-id="2e1b0-129">Vous pouvez modifier ce paramètre ultérieurement si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-129">You can change this setting later if you want to.</span></span>

8. <span data-ttu-id="2e1b0-130">For AD FS 2012: On the **Choose Issuance Authorization Rules**, keep Allow all users to access this **relying party** selected and click **Next**.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-130">For AD FS 2012: On the **Choose Issuance Authorization Rules**, keep **Permit all users to access this relying party** selected and click **Next**.</span></span>

9. <span data-ttu-id="2e1b0-131">Pour AD FS 2016 et AD FS 2019 : dans la **page** Choisir la stratégie de contrôle d’accès, sélectionnez la stratégie de contrôle d’accès appropriée, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-131">For AD FS 2016 and AD FS 2019: On the **Choose Access Control Policy** page, select the appropriate access control policy and click **Next**.</span></span> <span data-ttu-id="2e1b0-132">Si aucune n’est choisie, l’confiance de la partie de confiance **ne fonctionne** pas.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-132">If none is chosen, the Relying Party Trust will **NOT** work.</span></span>

10. <span data-ttu-id="2e1b0-133">Cliquez **sur Suivant** dans la page Prêt à ajouter **une** confiance pour terminer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-133">Click **Next** on the **Ready to Add Trust** page to complete the wizard.</span></span>

11. <span data-ttu-id="2e1b0-134">Cliquez **sur Fermer** sur la page Terminer. </span><span class="sxs-lookup"><span data-stu-id="2e1b0-134">Click **Close** on the **Finish** page.</span></span>

<span data-ttu-id="2e1b0-135">En fermant l’Assistant, l’confiance de la partie de confiance Office 365 service global est établie.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-135">By closing the wizard, the Relying Party Trust with the Office 365 Global service is established.</span></span> <span data-ttu-id="2e1b0-136">Toutefois, aucune règle de transformation d’émission n’est encore configurée.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-136">However, no Issuance Transform rules are configured yet.</span></span>

<span data-ttu-id="2e1b0-137">Vous pouvez utiliser [l’aide AD FS](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator) pour générer les règles de transformation d’émission correctes.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-137">You can use [AD FS Help](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator) to generate the correct Issuance Transform rules.</span></span> <span data-ttu-id="2e1b0-138">Les règles de revendication générées créées avec l’aide d’AD FS peuvent être ajoutées manuellement via la console de gestion AD FS ou avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-138">The generated claim rules created with AD FS Help can either be manually added through the AD FS management console or with PowerShell.</span></span> <span data-ttu-id="2e1b0-139">L’aide des AD FS génère les scripts PowerShell nécessaires à l’exécution.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-139">AD FS Help will generate the necessary PowerShell scripts that need to be executed.</span></span>  

> [!NOTE]
> <span data-ttu-id="2e1b0-140">[L’aide des AD FS](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator) génère les règles de transformation d’émission standard qui sont générées avec le produit.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-140">[AD FS Help](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator) will generate the standard issuance transform rules that ship with the product.</span></span> <span data-ttu-id="2e1b0-141">Toutefois, si des règles de transformation d’émission personnalisées sont en place dans l’trust de partie de confiance Microsoft Cloud Deutschland (par exemple, les UR d’émetteur personnalisés, les ID non standard immuables ou toute autre personnalisation), les règles générées par AD FS doivent être modifiées de manière à ce qu’elles correspondent à la logique personnalisée actuellement en place pour l’confiance de la partie de confiance Microsoft Cloud Deutschland.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-141">However, if custom issuance transform rules are in place in the Microsoft Cloud Deutschland Relying Party Trust (for example, custom issuer URIs, non-standard immutable IDs, or any other customizations), the rules generated by AD FS help must be modified in a way that they fit the custom logic currently in place for the Microsoft Cloud Deutschland relying party trust.</span></span> <span data-ttu-id="2e1b0-142">Si ces personnalisations ne sont pas intégrées aux règles générées via l’aide [d’AD FS,](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator)l’authentification à **Microsoft Office 365 Identity Platform WorldWide** ne fonctionne probablement pas pour vos identités fédérées. </span><span class="sxs-lookup"><span data-stu-id="2e1b0-142">If these customizations are not integrated in the rules generated via [AD FS Help](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator), authentication to **Microsoft Office 365 Identity Platform WorldWide** will most likely **not** work for your federated identities.</span></span>

1. <span data-ttu-id="2e1b0-143">Exécutez **l’aide** Générer des revendications [sur AD FS](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator) et copiez le script PowerShell à l’aide de l’option  Copier dans le coin supérieur droit du script.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-143">Run **Generate Claims** on [AD FS Help](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator) and copy the PowerShell script using the **Copy** option on the right upper corner of the script.</span></span>

2. <span data-ttu-id="2e1b0-144">Suivez les étapes décrites dans l’aide [AD FS](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator) sur la façon d’exécuter le script PowerShell dans votre batterie de serveurs AD FS pour générer l’trust de partie de confiance globale.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-144">Follow the steps outlined at [AD FS Help](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator) on how to run the PowerShell script in your AD FS farm to generate the global Relying Party Trust.</span></span> <span data-ttu-id="2e1b0-145">Avant d’exécuter le script, remplacez les lignes de code suivantes dans le script généré, comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="2e1b0-145">Before you run the script, replace the following code lines in the generated script as outlined below:</span></span>

   ```powershell
   # AD FS Help generated value
   $claims = Get-AdfsRelyingPartyTrust -Identifier $(Get-RpIdentifier) | Select-Object IssuanceTransformRules;
   # replace with
   $claims = Get-AdfsRelyingPartyTrust -Identifier urn:federation:MicrosoftOnline | Select-Object IssuanceTransformRules;

   # AD FS Help generated value
   Set-AdfsRelyingPartyTrust -TargetIdentifier $(Get-RpIdentifier) -IssuanceTransformRules $RuleSet.ClaimRulesString;
   # replace with
   Set-AdfsRelyingPartyTrust -TargetIdentifier urn:federation:MicrosoftOnline -IssuanceTransformRules $RuleSet.ClaimRulesString;
   ```

3. <span data-ttu-id="2e1b0-146">Vérifiez que deux parties de confiance sont présentes ; un pour Microsoft Cloud Deutschland et un autre pour le service Office 365 global.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-146">Verify that two Relying PartyTtrusts are present; one for Microsoft Cloud Deutschland and one for the Office 365 Global service.</span></span> <span data-ttu-id="2e1b0-147">La commande suivante peut être mise à profit pour la vérification.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-147">The following command can be leveraged for the check.</span></span> <span data-ttu-id="2e1b0-148">Elle doit renvoyer deux lignes, ainsi que les noms et identificateurs respectifs.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-148">It should return two rows and the respective names and identifiers.</span></span>

   ```powershell
   Get-AdfsRelyingPartyTrust | Where-Object {$_.Identifier -like 'urn:federation:MicrosoftOnline*'} | Select-Object Name, Identifier
   ```

4. <span data-ttu-id="2e1b0-149">Sauvegardez votre configuration de migration complète, y compris les deux confiances de partie de confiance, en suivant [ces étapes.](#backup)</span><span class="sxs-lookup"><span data-stu-id="2e1b0-149">Backup your full migration configuration, including both Relying Party trusts, using [these steps](#backup).</span></span> <span data-ttu-id="2e1b0-150">Enregistrez-le sous le **nom MicrosoftCloudDeueueulandAndWorldwide**.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-150">Save it with the name **MicrosoftCloudDeutschlandAndWorldwide**.</span></span>

5. <span data-ttu-id="2e1b0-151">Pendant la migration de votre client, vérifiez régulièrement que l’authentification AD FS fonctionne avec Microsoft Cloud Deutschland et le cloud global Microsoft dans les différentes étapes de migration prises en charge.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-151">While your tenant is in migration, regularly verify that AD FS authentication is working with Microsoft Cloud Deutschland and Microsoft Global cloud in the various supported migration steps.</span></span>

## <a name="ad-fs-disaster-recovery-wid-database"></a><span data-ttu-id="2e1b0-152">Récupération d’urgence AD FS (base de données WID)</span><span class="sxs-lookup"><span data-stu-id="2e1b0-152">AD FS Disaster Recovery (WID Database)</span></span>

<span data-ttu-id="2e1b0-153">Pour restaurer la batterie de serveurs AD FS en cas d’urgence, l’outil de restauration rapide [AD FS](/windows-server/identity/ad-fs/operations/ad-fs-rapid-restore-tool) doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-153">To restore the AD FS farm in a disaster [AD FS Rapid Restore Tool](/windows-server/identity/ad-fs/operations/ad-fs-rapid-restore-tool) needs to be leveraged.</span></span> <span data-ttu-id="2e1b0-154">Par conséquent, l’outil doit être téléchargé et avant le début de la migration, une sauvegarde doit être créée et stockée en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-154">Therefore, the tool must be downloaded and before the start of the migration a backup must be created and safely stored.</span></span> <span data-ttu-id="2e1b0-155">Dans cet exemple, les commandes suivantes ont été exécutés pour la back up d’une batterie de serveurs s’exécutant sur une base de données WID :</span><span class="sxs-lookup"><span data-stu-id="2e1b0-155">In this example, the following commands have been run to back up a farm running on a WID database:</span></span>

<h2 id="backup"></h2>

### <a name="back-up-an-ad-fs-farm"></a><span data-ttu-id="2e1b0-156">Back up an AD FS Farm</span><span class="sxs-lookup"><span data-stu-id="2e1b0-156">Back up an AD FS Farm</span></span>

1. <span data-ttu-id="2e1b0-157">Installez l’outil de restauration rapide AD FS sur le serveur AD FS principal.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-157">Install the AD FS Rapid Restore Tool on the primary AD FS server.</span></span>

2. <span data-ttu-id="2e1b0-158">Importez le module dans une session PowerShell avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-158">Import the module in a PowerShell session with this command.</span></span>

   ```powershell
   Import-Module "C:\Program Files (x86)\ADFS Rapid Recreation Tool\ADFSRapidRecreationTool.dll"
   ```

3. <span data-ttu-id="2e1b0-159">Exécutez la commande de sauvegarde :</span><span class="sxs-lookup"><span data-stu-id="2e1b0-159">Run the backup command:</span></span>

   ```powershell
   Backup-ADFS -StorageType "FileSystem" -storagePath "<Storage path of backup>" -EncryptionPassword "<password>" -BackupComment "Restore Doku" -BackupDKM
   ```

4. <span data-ttu-id="2e1b0-160">Stockez la sauvegarde en toute sécurité sur la destination souhaitée.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-160">Store the backup safely on a desired destination.</span></span>

### <a name="restore-an-ad-fs-farm"></a><span data-ttu-id="2e1b0-161">Restaurer une batterie de serveurs AD FS</span><span class="sxs-lookup"><span data-stu-id="2e1b0-161">Restore an AD FS Farm</span></span>

<span data-ttu-id="2e1b0-162">Si votre batterie de serveurs a complètement échoué et qu’il n’existe aucun moyen de revenir à l’ancienne batterie de serveurs, faites ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-162">If your farm failed completely and there is no way to return to the old farm, do the following.</span></span> 

1. <span data-ttu-id="2e1b0-163">Déplacez la sauvegarde précédemment générée et stockée vers le nouveau serveur AD FS principal.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-163">Move the previously generated and stored backup to the new primary AD FS server.</span></span>

2. <span data-ttu-id="2e1b0-164">Exécutez la commande `Restore-ADFS` PowerShell suivante.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-164">Run the following `Restore-ADFS` PowerShell command.</span></span> <span data-ttu-id="2e1b0-165">Si nécessaire, importez au préalable le certificat SSL AD FS.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-165">If necessary, import the AD FS SSL certificate beforehand.</span></span>

   ```powershell
   Restore-ADFS -StorageType "FileSystem" -StoragePath "<Path to Backup>" -DecryptionPassword "<password>" -GroupServiceAccountIdentifier "<gMSA>" -DBConnectionString "WID" -RestoreDKM
   ```

3. <span data-ttu-id="2e1b0-166">Pointez vos nouveaux enregistrements DNS ou équilibreur de charge vers les nouveaux serveurs AD FS.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-166">Point your new DNS records or load balancer to the new AD FS servers.</span></span>

## <a name="more-information"></a><span data-ttu-id="2e1b0-167">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2e1b0-167">More information</span></span>

<span data-ttu-id="2e1b0-168">Mise en place :</span><span class="sxs-lookup"><span data-stu-id="2e1b0-168">Getting started:</span></span>

- [<span data-ttu-id="2e1b0-169">Migration de Microsoft Cloud Deutschland vers Office 365 services dans les nouvelles régions de centres de données allemandes</span><span class="sxs-lookup"><span data-stu-id="2e1b0-169">Migration from Microsoft Cloud Deutschland to Office 365 services in the new German datacenter regions</span></span>](ms-cloud-germany-transition.md)
- [<span data-ttu-id="2e1b0-170">Aide à la migration de Microsoft Cloud Deutschland : </span><span class="sxs-lookup"><span data-stu-id="2e1b0-170">Microsoft Cloud Deutschland Migration Assistance</span></span>](https://aka.ms/germanymigrateassist)
- [<span data-ttu-id="2e1b0-171">Comment opter pour une migration</span><span class="sxs-lookup"><span data-stu-id="2e1b0-171">How to opt-in for migration</span></span>](ms-cloud-germany-migration-opt-in.md)
- [<span data-ttu-id="2e1b0-172">Expérience client pendant la migration</span><span class="sxs-lookup"><span data-stu-id="2e1b0-172">Customer experience during the migration</span></span>](ms-cloud-germany-transition-experience.md)

<span data-ttu-id="2e1b0-173">Transition :</span><span class="sxs-lookup"><span data-stu-id="2e1b0-173">Moving through the transition:</span></span>

- [<span data-ttu-id="2e1b0-174">Actions et impacts des phases de migration</span><span class="sxs-lookup"><span data-stu-id="2e1b0-174">Migration phases actions and impacts</span></span>](ms-cloud-germany-transition-phases.md)
- [<span data-ttu-id="2e1b0-175">Pré-travail supplémentaire</span><span class="sxs-lookup"><span data-stu-id="2e1b0-175">Additional pre-work</span></span>](ms-cloud-germany-transition-add-pre-work.md)
- <span data-ttu-id="2e1b0-176">Informations supplémentaires pour [Azure AD,](ms-cloud-germany-transition-azure-ad.md) [les appareils,](ms-cloud-germany-transition-add-devices.md) [les expériences](ms-cloud-germany-transition-add-experience.md)et [AD FS](ms-cloud-germany-transition-add-adfs.md).</span><span class="sxs-lookup"><span data-stu-id="2e1b0-176">Additional information for [Azure AD](ms-cloud-germany-transition-azure-ad.md), [devices](ms-cloud-germany-transition-add-devices.md), [experiences](ms-cloud-germany-transition-add-experience.md), and [AD FS](ms-cloud-germany-transition-add-adfs.md).</span></span>

<span data-ttu-id="2e1b0-177">Applications cloud :</span><span class="sxs-lookup"><span data-stu-id="2e1b0-177">Cloud apps:</span></span>

- [<span data-ttu-id="2e1b0-178">Informations sur le programme de migration Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2e1b0-178">Dynamics 365 migration program information</span></span>](/dynamics365/get-started/migrate-data-german-region)
- [<span data-ttu-id="2e1b0-179">Informations sur le programme de migration Power BI</span><span class="sxs-lookup"><span data-stu-id="2e1b0-179">Power BI migration program information</span></span>](/power-bi/admin/service-admin-migrate-data-germany)
- [<span data-ttu-id="2e1b0-180">Prise en main de votre mise à niveau vers Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2e1b0-180">Getting started with your Microsoft Teams upgrade</span></span>](/microsoftteams/upgrade-start-here)
