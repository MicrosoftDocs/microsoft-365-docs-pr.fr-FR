---
title: Déplacer des domaines & paramètres d’une organisation EOP vers une autre
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
ms.assetid: 9d64867b-ebdb-4323-8e30-4560d76b4c97
ms.custom:
- seo-marvel-apr2020
description: Dans cet article, vous allez découvrir comment déplacer des domaines et des paramètres d’une organisation (locataire) Microsoft Exchange Online Protection (EOP) vers une autre.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 4a9209f71905a858bb631a3c2901b7bfa62551d7
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51065217"
---
# <a name="move-domains-and-settings-from-one-eop-organization-to-another"></a><span data-ttu-id="be4d5-103">Déplacer des domaines et des paramètres d’une organisation EOP vers une autre</span><span class="sxs-lookup"><span data-stu-id="be4d5-103">Move domains and settings from one EOP organization to another</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="be4d5-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="be4d5-104">**Applies to**</span></span>
-  [<span data-ttu-id="be4d5-105">Exchange Online Protection autonome</span><span class="sxs-lookup"><span data-stu-id="be4d5-105">Exchange Online Protection standalone</span></span>](exchange-online-protection-overview.md)

<span data-ttu-id="be4d5-p101">L'évolution des besoins professionnels peut parfois imposer de séparer une organisation Microsoft Exchange Online Protection (EOP) (locataire) en deux organisations distinctes, de fusionner deux organisations en une seule ou de déplacer vos domaines et vos paramètres EOP d'une organisation vers une autre. Le déplacement d'une organisation EOP vers une deuxième organisation EOP peut être difficile, mais avec quelques scripts Windows PowerShell à distance basiques et un peu de préparation, cette opération peut être réalisée dans une fenêtre de maintenance relativement courte.</span><span class="sxs-lookup"><span data-stu-id="be4d5-p101">Changing business requirements can sometimes require splitting one Microsoft Exchange Online Protection (EOP) organization (tenant) into two separate organizations, merging two organizations into one, or moving your domains and EOP settings from one organization to another organization. Moving from one EOP organization to a second EOP organization can be challenging, but with a few basic remote Windows PowerShell scripts and a small amount of preparation, this can be achieved with a relatively small maintenance window.</span></span>

> [!NOTE]
>
> - <span data-ttu-id="be4d5-108">Les réglages ne peuvent être déplacés de manière fiable que depuis une organisation EOP (standard) autonome vers une autre organisation EOP standard ou vers une organisation avec licence d'accès client Exchange Enterprise avec services (EOP Premium), ou depuis une organisation EOP Premium vers une autre organisation EOP premium.</span><span class="sxs-lookup"><span data-stu-id="be4d5-108">Settings can be reliably moved only from an EOP standalone (Standard) organization to either another EOP Standard or an Exchange Enterprise CAL with Services (EOP Premium) organization, or from an EOP Premium organization to another EOP Premium organization.</span></span> <span data-ttu-id="be4d5-109">Étant donné que certaines fonctionnalités Premium ne sont pas pris en charge dans les organisations EOP Standard, le déplacement d’une organisation EOP Premium vers une organisation EOP Standard peut ne pas réussir.</span><span class="sxs-lookup"><span data-stu-id="be4d5-109">Because some premium features are not supported in EOP Standard organizations, moves from an EOP Premium organization to an EOP Standard organization might not be successful.</span></span>
>
> - <span data-ttu-id="be4d5-p103">Les présentes instructions ne concernent que les organisations à filtrage EOP uniquement. Le déplacement depuis une organisation Exchange Online vers une autre organisation Exchange Online pose des problèmes supplémentaires. Les organisations Exchange Online ne sont pas concernées par ces instructions.</span><span class="sxs-lookup"><span data-stu-id="be4d5-p103">These instructions are for EOP filtering-only organizations. There are additional considerations in moving from one Exchange Online organization to another Exchange Online organization. Exchange Online organizations are out of scope for these instructions.</span></span>

<span data-ttu-id="be4d5-p104">Dans l'exemple suivant, Contoso, Ltd. a fusionné avec Contoso Suites. L'image suivante illustre le processus de déplacement des domaines, des utilisateurs et groupes de messagerie, et des paramètres depuis l'organisation EOP source (contoso.onmicrosoft.com) vers l'organisation EOP cible (contososuites.onmicrosoft.com) :</span><span class="sxs-lookup"><span data-stu-id="be4d5-p104">In the following example, Contoso, Ltd. has merged with Contoso Suites. The following image shows the process of moving domains, mail users and groups, and settings from the source EOP organization (contoso.onmicrosoft.com) to the target EOP organization (contososuites.onmicrosoft.com):</span></span>

![Déplacer les paramètres et les domaines EOP](../../media/EOP-Move-domains-and-settings.jpg)

<span data-ttu-id="be4d5-p105">Le déplacement des domaines d'une organisation à une autre présente un défi de taille : un domaine vérifié ne peut pas exister dans deux organisations en même temps. Les étapes suivantes vous aident à résoudre ces difficultés.</span><span class="sxs-lookup"><span data-stu-id="be4d5-p105">The challenge in moving domains from one organization to another is that a verified domain can't exist in two organizations at the same time. The following steps help you work through this.</span></span>

## <a name="step-1-collect-data-from-the-source-organization"></a><span data-ttu-id="be4d5-118">Étape 1 : Collecter les données de l’organisation source</span><span class="sxs-lookup"><span data-stu-id="be4d5-118">Step 1: Collect data from the source organization</span></span>

<span data-ttu-id="be4d5-119">Afin de recréer l’organisation source dans l’organisation cible, veillez à collecter et stocker les informations suivantes concernant l’organisation source :</span><span class="sxs-lookup"><span data-stu-id="be4d5-119">In order to re-create the source organization in the target organization, make sure that you collect and store the following information about the source organization:</span></span>

- <span data-ttu-id="be4d5-120">Domaines</span><span class="sxs-lookup"><span data-stu-id="be4d5-120">Domains</span></span>
- <span data-ttu-id="be4d5-121">Utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="be4d5-121">Mail users</span></span>
- <span data-ttu-id="be4d5-122">Groupes</span><span class="sxs-lookup"><span data-stu-id="be4d5-122">Groups</span></span>
- <span data-ttu-id="be4d5-123">Anti-spam</span><span class="sxs-lookup"><span data-stu-id="be4d5-123">Anti-spam</span></span>
  - <span data-ttu-id="be4d5-124">Stratégies anti-courrier indésirable (également appelées stratégies de filtrage de contenu)</span><span class="sxs-lookup"><span data-stu-id="be4d5-124">Anti-spam policies (also known as content filter policies)</span></span>
  - <span data-ttu-id="be4d5-125">Stratégies de filtrage du courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="be4d5-125">Outbound spam filter policies</span></span>
  - <span data-ttu-id="be4d5-126">Stratégies de filtrage des connexions</span><span class="sxs-lookup"><span data-stu-id="be4d5-126">Connection filter policies</span></span>
- <span data-ttu-id="be4d5-127">Stratégies anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="be4d5-127">Anti-malware policies</span></span>
- <span data-ttu-id="be4d5-128">Connecteurs</span><span class="sxs-lookup"><span data-stu-id="be4d5-128">Connectors</span></span>
- <span data-ttu-id="be4d5-129">Règles de flux de messagerie (également appelées règles de transport)</span><span class="sxs-lookup"><span data-stu-id="be4d5-129">Mail flow rules (also known as transport rules)</span></span>

  > [!NOTE]
  > <span data-ttu-id="be4d5-130">La prise en charge des cmdlet pour l’exportation et l’importation de la collection de règles de flux de messagerie est actuellement prise en charge uniquement pour les plans d’abonnement EOP Premium.</span><span class="sxs-lookup"><span data-stu-id="be4d5-130">Cmdlet support for the export and import of the mail flow rule collection is currently only supported for EOP Premium subscription plans.</span></span>

<span data-ttu-id="be4d5-131">Le moyen le plus simple de collecter tous vos paramètres consiste à utiliser PowerShell.</span><span class="sxs-lookup"><span data-stu-id="be4d5-131">The easiest way to collect all of your settings is to use PowerShell.</span></span> <span data-ttu-id="be4d5-132">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="be4d5-132">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

<span data-ttu-id="be4d5-p107">Ensuite, vous pouvez collecter tous vos paramètres et les exporter vers un fichier .xml à importer dans le locataire cible. En général, vous pouvez orienter la sortie de la cmdlet **Get** pour chaque paramètre vers la cmdlet **Export-Clixml** afin d'enregistrer les paramètres dans des fichiers .xml, tel qu'illustré dans l'exemple de code ci-après.</span><span class="sxs-lookup"><span data-stu-id="be4d5-p107">Next, you can collect all your settings and export them to an .xml file to be imported into the target tenant. In general, you can pipe the output of the **Get** cmdlet for each setting to the **Export-Clixml** cmdlet to save the settings in .xml files, as shown in the following code sample.</span></span>

<span data-ttu-id="be4d5-135">Dans EOP PowerShell autonome, créez un répertoire appelé Exporter à un emplacement facile à trouver et à modifier dans ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="be4d5-135">In standalone EOP PowerShell, create a directory called Export in a location that's easy to find and change to that directory.</span></span> <span data-ttu-id="be4d5-136">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="be4d5-136">For example:</span></span>

```PowerShell
mkdir C:\EOP\Export
```

```PowerShell
cd C:\EOP\Export
```

<span data-ttu-id="be4d5-137">Le script suivant peut être utilisé pour collecter tous les utilisateurs de messagerie, les groupes, les paramètres anti-courrier indésirable, les paramètres anti-programme malveillant, les connecteurs et les règles de flux de messagerie dans l’organisation source.</span><span class="sxs-lookup"><span data-stu-id="be4d5-137">The following script can be used to collect all the mail users, groups, anti-spam settings, anti-malware settings, connectors, and mail flow rules in the source organization.</span></span> <span data-ttu-id="be4d5-138">Copiez-collez le texte suivant dans un éditeur de texte comme le Bloc-notes, enregistrez le fichier sous le nom Source_EOP_Settings.ps1 dans le répertoire Export que vous venez de créer et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="be4d5-138">Copy and paste the following text into a text editor like Notepad, save the file as Source_EOP_Settings.ps1 in the Export directory you just created, and run the following command:</span></span>

```PowerShell
& "C:\EOP\Export\Source_EOP_Settings.ps1"
```

```PowerShell
#****************************************************************************
# Export Domains
#*****************************************************************************
Get-AcceptedDomain | Export-Clixml Domains.xml
#****************************************************************************
# Export mail users
#
#****************************************************************************
Get-Recipient -ResultSize unlimited -RecipientTypeDetails MailUser | Export-Clixml MailUsers.xml
#****************************************************************************
# Groups
#
# If you're using directory synchronization, you can skip this step and
# simply sync to the target
# tenant.
# First, you need to capture information about the distribution groups.
#****************************************************************************
Get-Recipient -ResultSize unlimited -RecipientTypeDetails MailUniversalDistributionGroup | Export-Clixml DistributionGroups.xml
Get-Recipient -ResultSize unlimited -RecipientTypeDetails MailUniversalSecurityGroup | Export-Clixml SecurityGroups.xml
#****************************************************************************
# And then we'll use that output to loop through each group and get the
# members.
#****************************************************************************
$DGs = Import-Clixml .\DistributionGroups.xml
ForEach ($dg in $DGs) {Get-DistributionGroupMember -Identity $dg.name | Export-Clixml $dg.ExternalDirectoryObjectId}
$SGs = Import-Clixml .\SecurityGroups.xml
ForEach ($sg in $SGs) {Get-DistributionGroupMember -Identity $sg.name | Export-Clixml $sg.ExternalDirectoryObjectId}
#*****************************************************************************
# Export dynamic distribution groups - EOP Premium Only
#
# If you're using directory synchronization, then you can skip this step and simply
# sync to the target tenant.
#*****************************************************************************
Get-DynamicDistributionGroup -ResultSize unlimited | Export-Clixml DynamicDistributionGroups.xml
#*****************************************************************************
# Export mail contacts - EOP Premium Only
#
# If you're using directory synchronization, then you can skip this step and simply
# sync to the target tenant.
#*****************************************************************************
Get-MailContact -ResultSize unlimited -RecipientTypeDetails MailContact | Export-Clixml MailContacts.xml
#****************************************************************************
# Anti-spam
#****************************************************************************
Get-HostedConnectionFilterPolicy | Export-Clixml HostedConnectionFilterPolicy.xml
Get-HostedContentFilterPolicy | Export-Clixml HostedContentFilterPolicy.xml
Get-HostedContentFilterRule | Export-Clixml HostedContentFilterRule.xml
Get-HostedOutboundSpamFilterPolicy | Export-Clixml HostedOutboundSpamFilterPolicy.xml
#****************************************************************************
# Anti-malware policies
#****************************************************************************
Get-MalwareFilterPolicy | Export-Clixml MalwareFilterPolicy.xml
Get-MalwareFilterRule | Export-Clixml MalwareFilterRule.xml
#****************************************************************************
# Connectors
#****************************************************************************
Get-InboundConnector | Export-Clixml InboundConnector.xml
Get-OutboundConnector | Export-Clixml OutboundConnector.xml
#****************************************************************************
# Exchange mail flow rules
#****************************************************************************
$file = Export-TransportRuleCollection
Set-Content -Path ".TransportRules.xml" -Value $file.FileData -Encoding Byte
```

<span data-ttu-id="be4d5-p110">Exécutez les commandes suivantes dans le répertoire Export pour mettre à jour les fichiers .xml dans l’organisation cible. Remplacez contoso.onmicrosoft.com et contososuites.onmicrosoft.com par les noms de vos organisations source et cible.</span><span class="sxs-lookup"><span data-stu-id="be4d5-p110">Run the following commands from the Export directory to update the .xml files with the target organization. Replace contoso.onmicrosoft.com and contososuites.onmicrosoft.com with your source and target organization names.</span></span>

```PowerShell
$files = ls
ForEach ($file in $files) { (Get-Content $file.Name) | Foreach-Object {$_ -replace 'contoso.onmicrosoft.com', 'contososuites.onmicrosoft.com'} | Set-Content $file.Name}
```

## <a name="step-2-add-domains-to-the-target-organization"></a><span data-ttu-id="be4d5-141">Étape 2 : Ajouter des domaines dans l’organisation cible</span><span class="sxs-lookup"><span data-stu-id="be4d5-141">Step 2: Add domains to the target organization</span></span>

<span data-ttu-id="be4d5-p111">Ajoutez des domaines dans l'organisation cible à l'aide du script suivant. Copiez-collez le texte suivant dans un éditeur de texte comme le Bloc-notes, enregistrez le script sous C:\EOP\Export\Add_Domains.ps1 et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="be4d5-p111">Add domains to the target organization by using the following script. Copy and paste the text into a text editor like Notepad, save the script as C:\EOP\Export\Add_Domains.ps1, and run the following command:</span></span>

```PowerShell
& "C:\EOP\Export\Add_Domains.ps1"
```

<span data-ttu-id="be4d5-144">Ces domaines ne seront pas vérifiés et ne peuvent pas être utilisés pour acheminer le courrier, mais une fois que les domaines sont ajoutés, vous pouvez collecter les informations nécessaires pour vérifier les domaines et même mettre à jour vos enregistrements MX (serveur de messagerie) pour le nouveau locataire.</span><span class="sxs-lookup"><span data-stu-id="be4d5-144">These domains won't be verified and can't be used to route mail, but after the domains are added, you can collect the information needed to verify the domains and eventually update your MX records for the new tenant.</span></span>

```PowerShell
#***********************************************************************
# Login to Azure Active Directory
#*****************************************************************************
$msolcred = Get-Credential
connect-msolservice -credential $msolcred
#****************************************************************************
# Add domains
#****************************************************************************
$Domains = Import-Clixml ".\Domains.xml"
Foreach ($domain in $Domains) {
    New-MsolDomain -Name $domain.Name
}
```

<span data-ttu-id="be4d5-145">Vous pouvez maintenant consulter et collecter les informations à partir du Centre d’administration Microsoft 365 de votre organisation cible afin de vérifier rapidement vos domaines lorsque le moment est venu :</span><span class="sxs-lookup"><span data-stu-id="be4d5-145">Now you can review and collect the information from the Microsoft 365 admin center of your target organization so you can quickly verify your domains when the time comes:</span></span>

1. <span data-ttu-id="be4d5-146">Connectez-vous au Centre d’administration Microsoft 365 à l’adresse <https://portal.office.com> .</span><span class="sxs-lookup"><span data-stu-id="be4d5-146">Sign in to the Microsoft 365 admin center at <https://portal.office.com>.</span></span>

2. <span data-ttu-id="be4d5-147">Cliquez sur **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="be4d5-147">Click **Domains**.</span></span>

   <span data-ttu-id="be4d5-148">Si vous ne voyez pas de domaines, cliquez sur Personnaliser **la navigation,** sélectionnez **Installation,** puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="be4d5-148">If you don't see domains, click **Customize navigation**, select **Setup**, and then click **Save**.</span></span>

3. <span data-ttu-id="be4d5-149">Cliquez sur chaque lien **Démarrer l'installation** et suivez les étapes de l'assistant d'installation.</span><span class="sxs-lookup"><span data-stu-id="be4d5-149">Click each **Start setup** link, and then proceed through the setup wizard.</span></span>

4. <span data-ttu-id="be4d5-150">Dans la page **Confirmer que vous êtes le propriétaire**, pour **Reportez-vous aux instructions étape par étape pour exécuter cette étape avec**, sélectionnez **Instructions générales**.</span><span class="sxs-lookup"><span data-stu-id="be4d5-150">On the **Confirm ownership** page, for **See step-by-step instructions for performing this step with**, select **General instructions**.</span></span>

5. <span data-ttu-id="be4d5-151">Sauvegardez l'enregistrement MX ou l'enregistrement TXT dossier que vous allez utiliser pour vérifier votre domaine, puis fermez l'assistant d'installation.</span><span class="sxs-lookup"><span data-stu-id="be4d5-151">Record the MX record or TXT record that you'll use to verify your domain, and finish the setup wizard.</span></span>

6. <span data-ttu-id="be4d5-152">Ajoutez les enregistrements TXT de vérification à vos enregistrements DNS.</span><span class="sxs-lookup"><span data-stu-id="be4d5-152">Add the verification TXT records to your DNS records.</span></span> <span data-ttu-id="be4d5-153">Vous pourrez ainsi vérifier plus rapidement les domaines de l'organisation source après leur retrait de l'organisation cible.</span><span class="sxs-lookup"><span data-stu-id="be4d5-153">This will let you more quickly verify the domains in the source organization after they're removed from the target organization.</span></span> <span data-ttu-id="be4d5-154">Pour plus d’informations sur la configuration du DNS, voir Créer des enregistrements DNS chez un fournisseur d’hébergement [DNS pour Microsoft 365.](../../admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md)</span><span class="sxs-lookup"><span data-stu-id="be4d5-154">For more information about configuring DNS, see [Create DNS records at any DNS hosting provider for Microsoft 365](../../admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span></span>

## <a name="step-3-force-senders-to-queue-mail"></a><span data-ttu-id="be4d5-155">Étape 3 : Forcer les expéditeurs à mettre les messages en attente</span><span class="sxs-lookup"><span data-stu-id="be4d5-155">Step 3: Force senders to queue mail</span></span>

<span data-ttu-id="be4d5-p113">Tout en déplaçant vos domaines d'un locataire vers un autre, vous devrez supprimer les domaines de l'organisation source, puis les vérifier dans votre organisation cible. Pendant ce temps, vous ne pourrez pas acheminer les messages via EOP.</span><span class="sxs-lookup"><span data-stu-id="be4d5-p113">While moving your domains from one tenant to another, you'll need to delete the domains from the source organization and then verify them in your target organization. During this time, you won't be able to route mail through EOP.</span></span>

<span data-ttu-id="be4d5-158">Une des manières de forcer les expéditeurs à mettre les messages en attente consiste à mettre à jour vos enregistrements MX pour qu'ils pointent directement vers votre serveur de messagerie local.</span><span class="sxs-lookup"><span data-stu-id="be4d5-158">One option to force senders to queue mail is to update your MX records to point directly to your on-premises mail server.</span></span>

<span data-ttu-id="be4d5-p114">Une autre option consiste à placer un enregistrement MX non valide dans chaque domaine où sont conservés les enregistrements DNS de votre domaine (également connu comme service d'hébergement DNS). L'expéditeur doit alors mettre vos messages en attente et retenter l'opération (les nouvelles tentatives ont généralement lieu sous 48 heures, mais cela peut varier d'un fournisseur à l'autre). Vous pouvez utiliser invalid.outlook.com comme cible MX non valide. L'abaissement de la durée de vie (TTL) à cinq minutes pour l'enregistrement MX permet de propager plus rapidement la modification aux fournisseurs DNS.</span><span class="sxs-lookup"><span data-stu-id="be4d5-p114">Another option is to put an invalid MX record in each domain where the DNS records for your domain are kept (also known as your DNS hosting service). This will cause the sender to queue your mail and retry (typical retry attempts are for 48 hours, but this might vary from provider to provider). You can use invalid.outlook.com as an invalid MX target. Lowering the Time to Live (TTL) value to five minutes on the MX record will help the change propagate to DNS providers more quickly.</span></span>

<span data-ttu-id="be4d5-163">Pour plus d’informations sur la configuration du DNS, voir Créer des enregistrements DNS chez un fournisseur d’hébergement [DNS pour Microsoft 365.](../../admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md)</span><span class="sxs-lookup"><span data-stu-id="be4d5-163">For more information about configuring DNS, see [Create DNS records at any DNS hosting provider for Microsoft 365](../../admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be4d5-p115">Chaque fournisseur met les messages en attente pour des durées différentes. Vous devrez configurer rapidement votre nouveau locataire et rétablir vos paramètres DNS afin d'éviter l'envoi de rapports de non-remise (NDR) à l'expéditeur lors de l'expiration du délai d'attente.</span><span class="sxs-lookup"><span data-stu-id="be4d5-p115">Different providers queue mail for different periods of time. You'll need to set up your new tenant quickly and revert your DNS settings to avoid non-delivery reports (NDRs) from being sent to the sender if the queuing time expires.</span></span>

## <a name="step-4-remove-users-groups-and-domains-from-the-source-organization"></a><span data-ttu-id="be4d5-166">Étape 4 : Supprimer les utilisateurs, les groupes et les domaines de l’organisation source</span><span class="sxs-lookup"><span data-stu-id="be4d5-166">Step 4: Remove users, groups, and domains from the source organization</span></span>

<span data-ttu-id="be4d5-167">Le script suivant supprime les utilisateurs, les groupes et les domaines du client source à l’aide d’Azure Active Directory PowerShell.</span><span class="sxs-lookup"><span data-stu-id="be4d5-167">The following script removes users, groups, and domains from the source tenant by using Azure Active Directory PowerShell.</span></span> <span data-ttu-id="be4d5-168">Copiez-collez le texte suivant dans un éditeur de texte comme le Bloc-notes, enregistrez le fichier sous C:\EOP\Export\Remove_Users_and_Groups.ps1 et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="be4d5-168">Copy and paste the following text into a text editor like Notepad, save the file as C:\EOP\Export\Remove_Users_and_Groups.ps1, and run the following command:</span></span>

```PowerShell
& "C:\EOP\Export\Remove_Users_and_Groups.ps1"
```

```PowerShell
#*****************************************************************************
# Login to Azure Active Directory
#*****************************************************************************
$msolcred= Get-Credential
connect-msolservice -credential $msolcred
#*****************************************************************************
# Remove users
#*****************************************************************************
$Users = Get-MSOLUser -All | sort UserPrincipalName
$user_count = $Users.count
write-host "Removing $user_count users."
Foreach ($User in $Users) {
write-host $User.UserPrincipalName
$User | Remove-MSOLUser -Force
}
#*****************************************************************************
# Remove groups
#*****************************************************************************
Get-MSOLGroup | Remove-MSOLGroup -Force
#*****************************************************************************
# Remove domains
# Note: Your onmicrosoft.com domain should be the default domain
#*****************************************************************************
$Domains = Get-MsolDomain
$Domain_count = $Domains.count
write-host "Removing $Domain_count domains."
Foreach ($Domain in $Domains) {
write-host $Domain.Name
Remove-MsolDomain -DomainName $Domain.Name -Force
}
```

## <a name="step-5-verify-domains-for-the-target-organization"></a><span data-ttu-id="be4d5-169">Étape 5 : Vérifier les domaines de l’organisation cible</span><span class="sxs-lookup"><span data-stu-id="be4d5-169">Step 5: Verify domains for the target organization</span></span>

1. <span data-ttu-id="be4d5-170">Connectez-vous au Centre d’administration à <https://portal.office.com> l’adresse .</span><span class="sxs-lookup"><span data-stu-id="be4d5-170">Sign in to the admin center at <https://portal.office.com>.</span></span>

2. <span data-ttu-id="be4d5-171">Cliquez sur **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="be4d5-171">Click **Domains**.</span></span>

3. <span data-ttu-id="be4d5-172">Cliquez sur chaque lien **Démarrer l’installation** pour le domaine cible et suivez les étapes de l’assistant d’installation.</span><span class="sxs-lookup"><span data-stu-id="be4d5-172">Click each **Start setup** link for the target domain and proceed through the setup wizard.</span></span>

## <a name="step-6-add-mail-users-and-groups-to-the-target-organization"></a><span data-ttu-id="be4d5-173">Étape 6 : Ajouter des utilisateurs de messagerie et des groupes à l’organisation cible</span><span class="sxs-lookup"><span data-stu-id="be4d5-173">Step 6: Add mail users and groups to the target organization</span></span>

<span data-ttu-id="be4d5-174">Une meilleure pratique pour EOP consiste à utiliser Azure Active Directory pour synchroniser votre système Active Directory sur site sur votre client cible.</span><span class="sxs-lookup"><span data-stu-id="be4d5-174">A best practice for EOP is to use Azure Active Directory to sync your on-premises Active Directory to your target tenant.</span></span> <span data-ttu-id="be4d5-175">Pour connaître la procédure détaillée, consultez la rubrique « Utilisation de la synchronisation d'annuaires pour gérer les utilisateurs de messagerie » dans [Gestion des utilisateurs de messagerie dans EOP](manage-mail-users-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="be4d5-175">For more information about how to do this, see "Use directory synchronization to manage mail users" in [Manage mail users in EOP](manage-mail-users-in-eop.md).</span></span> <span data-ttu-id="be4d5-176">Vous pouvez également utiliser le script suivant pour recréer vos utilisateurs et vos groupes à partir de votre client source.</span><span class="sxs-lookup"><span data-stu-id="be4d5-176">You can also use the following script to recreate your users and groups from your source tenant.</span></span> <span data-ttu-id="be4d5-177">Remarque : les mots de passe utilisateur ne peuvent pas être déplacés.</span><span class="sxs-lookup"><span data-stu-id="be4d5-177">Note: User passwords cannot be moved.</span></span> <span data-ttu-id="be4d5-178">D'autres mots de passe utilisateur sont créés et enregistrés dans le fichier intitulé UsersAndGroups.ps1.</span><span class="sxs-lookup"><span data-stu-id="be4d5-178">New user passwords are created and saved in the file named UsersAndGroups.ps1.</span></span>

<span data-ttu-id="be4d5-179">Pour utiliser le script, copiez-collez le texte suivant dans un éditeur de texte comme le Bloc-notes, enregistrez le fichier sous C:\EOP\Export\Add_Users_and_Groups.ps1 et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="be4d5-179">To use the script, copy and paste the following text into a text editor like Notepad, save the file as C:\EOP\Export\Add_Users_and_Groups.ps1, and run the following command:</span></span>

```PowerShell
& "C:\EOP\Export\Add_Users_and_Groups.ps1"
```

```PowerShell
#***********************************************************************
# makeparam helper function
#****************************************************************************
function makeparam ([string]$ParamName, [string[]] $ParamValue) {
    $FormattedParam = ""
    If($ParamValue.Count -gt 0) {
        $FormattedParam = " -$ParamName "
        Foreach ($value in $ParamValue) {
        If($value -eq "True") {$FormattedParam = " -$ParamName" + ":`$True,"}
        else{
            If($value -eq "False") {$FormattedParam = " -$ParamName" + ":`$False,"}
                else{$FormattedParam += "`"$value`","}
            }
        }
        $FormattedParam = $FormattedParam.TrimEnd(",")
    }
    Return $FormattedParam
 }
#****************************************************************************
# Variables
#****************************************************************************
$outfile = ".\UsersAndGroups.ps1"
rm -erroraction 'silentlycontinue' $outfile
#****************************************************************************
# Add mail users
#****************************************************************************
$rand = New-Object System.Random -ArgumentList (get-date).millisecond
$MailUsers = Import-Clixml ".\MailUsers.xml"
$MailUsersCount = $MailUsers.Name.Count
if($MailUsersCount -gt 0){
    Write-Host "Importing $MailUsersCount Mail Users"
    ForEach ($MailUser in $MailUsers) {
        $MailUsersCmdlet = "New-MailUser"
        If((Get-PSSession).ComputerName.Contains("ps.protection")) {
            $DistributionGroupsCmdlet = "New-EOPMailUser"
        }
        $MailUsersCmdlet += makeparam "LastName" $MailUser.LastName
        $MailUsersCmdlet += makeparam "FirstName" $MailUser.FirstName
        $MailUsersCmdlet += makeparam "DisplayName" $MailUser.DisplayName
        $MailUsersCmdlet += makeparam "Name" $MailUser.Name
        $MailUsersCmdlet += makeparam "Alias" $MailUser.Alias
        $MailUsersCmdlet += makeparam "MicrosoftOnlineServicesID" $MailUser.MicrosoftOnlineServicesID
        $MailUsersCmdlet += makeparam "ExternalEmailAddress" $MailUser.ExternalEmailAddress

        # Generate a new 10 character password
        $NewPassword = ""
        1..10 | ForEach { $NewPassword = $NewPassword + [char]$rand.next(40,127) }

        $MailUsersCmdlet += " -Password (ConvertTo-SecureString -String '$NewPassword' -AsPlainText -Force)"
        Add-Content $outfile "`n$MailUsersCmdlet"
    }
}
#****************************************************************************
# Add distribution groups
#****************************************************************************
$DistributionGroups = Import-Clixml ".\DistributionGroups.xml"
$DistributionGroupsCount = $DistributionGroups.Name.Count
if($DistributionGroupsCount -gt 0){
    Write-Host "Importing $DistributionGroupsCount Distribution Groups"
    ForEach ($DistributionGroup in $DistributionGroups) {
        $DistributionGroupsCmdlet = "New-DistributionGroup"
        If((Get-PSSession).ComputerName.Contains("ps.protection")) {
            $DistributionGroupsCmdlet = "New-EOPDistributionGroup"
        }
        $DistributionGroupsCmdlet += makeparam "Name" $DistributionGroup.Name
        $DistributionGroupsCmdlet += makeparam "Alias" $DistributionGroup.Alias
        $DistributionGroupsCmdlet += makeparam "DisplayName" $DistributionGroup.DisplayName
        $DistributionGroupsCmdlet += makeparam "ManagedBy" $DistributionGroup.ManagedBy

        $DistributionGroupsCmdlet += makeparam "Notes" $DistributionGroup.Notes
        $DistributionGroupsCmdlet += makeparam "PrimarySmtpAddress" $DistributionGroup.PrimarySmtpAddress
        $DistributionGroupsCmdlet += makeparam "Type" $DistributionGroup.Type
        $MembersCmdlet = "@("
        $memberslist = Import-Clixml $DistributionGroup.ExternalDirectoryObjectId
        ForEach ($user in $memberslist) {
            $MembersCmdlet += "`"$user.Name`","
        }
        $MembersCmdlet = $MembersCmdlet.TrimEnd(",")
        $MembersCmdlet += ")"
    }
    Add-Content $outfile "`n$DistributionGroupsCmdlet"
}
#****************************************************************************
# Add security groups
#****************************************************************************
$SecurityGroups = Import-Clixml ".\SecurityGroups.xml"
$SecurityGroupsCount = $SecurityGroups.Name.Count
if($SecurityGroupsCount -gt 0){
    Write-Host "Importing $SecurityGroupsCount Security Groups"
    ForEach ($SecurityGroup in $SecurityGroups) {
        $SecurityGroupsCmdlet = "New-SecurityGroup"
        If((Get-PSSession).ComputerName.Contains("ps.protection")) {
            $DistributionGroupsCmdlet = "New-EOPSecurityGroup"
        }
        $SecurityGroupsCmdlet += makeparam "Name" $SecurityGroup.Name
        $SecurityGroupsCmdlet += makeparam "Alias" $SecurityGroup.Alias
        $SecurityGroupsCmdlet += makeparam "DisplayName" $SecurityGroup.DisplayName
        $SecurityGroupsCmdlet += makeparam "ManagedBy" $SecurityGroup.ManagedBy

        $SecurityGroupsCmdlet += makeparam "Notes" $SecurityGroup.Notes
        $SecurityGroupsCmdlet += makeparam "PrimarySmtpAddress" $SecurityGroup.PrimarySmtpAddress
        $SecurityGroupsCmdlet += makeparam "Type" $SecurityGroup.Type
        $MembersCmdlet = "@("
        $memberslist = Import-Clixml $SecurityGroup.ExternalDirectoryObjectId
        ForEach ($user in $memberslist) {
            $MembersCmdlet += "`"$user.Name`","
        }
        $MembersCmdlet = $MembersCmdlet.TrimEnd(",")
        $MembersCmdlet += ")"
    }
    Add-Content $outfile "`n$SecurityGroupsCmdlet"
}
#****************************************************************************
# Add Dynamic Distribution Groups
#****************************************************************************
If((Get-PSSession).ComputerName.Contains("ps.protection")) {
    write-Host "No Synamic Distribution Groups for EOP Standard organizations."
}else{
    $DynamicDistributionGroups = Import-Clixml ".\DynamicDistributionGroups.xml"
    $DynamicDistributionGroupsCount = $DynamicDistributionGroups.Name.Count
    if($DynamicDistributionGroupsCount -gt 0){
        Write-Host "Importing $DynamicDistributionGroupsCount Dynamic Distribution Groups"
        foreach ($DynamicDistributionGroup in $DynamicDistributionGroups) {
            $DynamicDistributionGroupsCmdlet = "New-DynamicDistributionGroup"
            $DynamicDistributionGroupsCmdlet += " -Confirm:`$False"
            $DynamicDistributionGroupsCmdlet += makeparam "DisplayName" $DynamicDistributionGroup.DisplayName
            $DynamicDistributionGroupsCmdlet += makeparam "ModeratedBy" $DynamicDistributionGroup.ModeratedBy
            $DynamicDistributionGroupsCmdlet += makeparam "ModerationEnabled" $DynamicDistributionGroup.ModerationEnabled
            $DynamicDistributionGroupsCmdlet += makeparam "Name" $DynamicDistributionGroup.Name
            $DynamicDistributionGroupsCmdlet += makeparam "PrimarySmtpAddress" $DynamicDistributionGroup.PrimarySmtpAddress
            $DynamicDistributionGroupsCmdlet += makeparam "RecipientContainer" $DynamicDistributionGroup.RecipientContainer
            $RecipientFilterParam =  makeparam "RecipientFilter" $DynamicDistributionGroup.RecipientFilter
            $RecipientFilterParam = " -RecipientFilter {" + $RecipientFilterParam.Substring(19)
            $RecipientFilterParam = $RecipientFilterParam.Substring(0,$RecipientFilterParam.Length-1)
            $RecipientFilterParam += "}"
            $DynamicDistributionGroupsCmdlet +=  $RecipientFilterParam
            $DynamicDistributionGroupsCmdlet += makeparam "SendModerationNotifications" $DynamicDistributionGroup.SendModerationNotifications
            Add-Content $outfile "`n$DynamicDistributionGroupsCmdlet"
        }

    }else{
        Write-Host "No Dynamic Distribution Groups to add."
    }
}
#****************************************************************************
# Add Mail Contacts
#****************************************************************************
If((Get-PSSession).ComputerName.Contains("ps.protection")) {
    write-Host "No Mail Contact for EOP Standard organizations."
}else{
    $MailContacts = Import-Clixml ".\MailContacts.xml"
    $MailContactsCount = $MailContacts.Name.Count
    if($MailContactsCount -gt 0){
        Write-Host "Importing $MailContactsCount Dynamic Distribution Groups"
        foreach ($MailContact in $MailContacts) {
            $MailContactsCmdlet = "New-MailContact"
            $MailContactsCmdlet += makeparam "UsePreferMessageFormat" $MailContact.UsePreferMessageFormat
            $MailContactsCmdlet += makeparam "DisplayName" $MailContact.DisplayName
            $MailContactsCmdlet += makeparam "ModeratedBy" $MailContact.ModeratedBy
            $MailContactsCmdlet += makeparam "Name" $MailContact.Name
            $MailContactsCmdlet += makeparam "MessageBodyFormat" $MailContact.MessageBodyFormat
            $MailContactsCmdlet += makeparam "OrganizationalUnit" $MailContact.OrganizationalUnit
            $MailContactsCmdlet += makeparam "Initials" $MailContact.Initials
            $MailContactsCmdlet += makeparam "MessageFormat" $MailContact.MessageFormat
            $MailContactsCmdlet += makeparam "ModerationEnabled" $MailContact.ModerationEnabled
            $MailContactsCmdlet += makeparam "MacAttachmentFormat" $MailContact.MacAttachmentFormat
            $MailContactsCmdlet += makeparam "SendModerationNotifications" $MailContact.SendModerationNotifications
            $MailContactsCmdlet += " -Confirm:`$False"
            $MailContactsCmdlet += makeparam "ExternalEmailAddress" $MailContact.ExternalEmailAddress
            $MailContactsCmdlet += makeparam "FirstName" $MailContact.FirstName
            $MailContactsCmdlet += makeparam "Alias" $MailContact.Alias
            Add-Content $outfile "`n$MailContactsCmdlet"
        }

    }else{
        Write-Host "No Mail Contacts to add."
    }
}
#***********************************************************************
# makeparam helper function
#************************************************************************
 function makeparam ([string]$ParamName, [string[]] $ParamValue) {
    $FormattedParam = ""
    If($ParamValue.Count -gt 0) {
        $FormattedParam = " -$ParamName "
        Foreach ($value in $ParamValue) {
        If($value -eq "True") {$FormattedParam = " -$ParamName" + ":`$True,"}
        else{
            If($value -eq "False") {$FormattedParam = " -$ParamName" + ":`$False,"}
                else{$FormattedParam += "`"$value`","}
            }
        }
        $FormattedParam = $FormattedParam.TrimEnd(",")
    }
    Return $FormattedParam
 }
#****************************************************************************
# Variables
#****************************************************************************
$outfile = ".\UsersAndGroups.ps1"
rm -erroraction 'silentlycontinue' $outfile
#****************************************************************************
# Add mail users
#****************************************************************************
$rand = New-Object System.Random -ArgumentList (get-date).millisecond
$MailUsers = Import-Clixml ".\MailUsers.xml"
$MailUsersCount = $MailUsers.Name.Count
if($MailUsersCount -gt 0){
    Write-Host "Importing $MailUsersCount Mail Users"
    ForEach ($MailUser in $MailUsers) {
        $MailUsersCmdlet = "New-EOPMailUser"
        $MailUsersCmdlet += makeparam "LastName" $MailUser.LastName
        $MailUsersCmdlet += makeparam "FirstName" $MailUser.FirstName
        $MailUsersCmdlet += makeparam "DisplayName" $MailUser.DisplayName
        $MailUsersCmdlet += makeparam "Name" $MailUser.Name
        $MailUsersCmdlet += makeparam "Alias" $MailUser.Alias
        $MailUsersCmdlet += makeparam "MicrosoftOnlineServicesID" $MailUser.MicrosoftOnlineServicesID
        $MailUsersCmdlet += makeparam "ExternalEmailAddress" $MailUser.ExternalEmailAddress

        # Generate a new 10 character password
        $NewPassword = ""
        1..10 | ForEach { $NewPassword = $NewPassword + [char]$rand.next(40,127) }

        $MailUsersCmdlet += " -Password (ConvertTo-SecureString -String '$NewPassword' -AsPlainText -Force)"
        Add-Content $outfile "`n$MailUsersCmdlet"
    }
}
#****************************************************************************
# Add distribution groups
#****************************************************************************
$DistributionGroups = Import-Clixml ".\DistributionGroups.xml"
$DistributionGroupsCount = $DistributionGroups.Name.Count
if($DistributionGroupsCount -gt 0){
    Write-Host "Importing $DistributionGroupsCount Distribution Groups"
    ForEach ($DistributionGroup in $DistributionGroups) {
        $DistributionGroupsCmdlet = "New-EOPDistributionGroup"
        $DistributionGroupsCmdlet += makeparam "Name" $DistributionGroup.Name
        $DistributionGroupsCmdlet += makeparam "Alias" $DistributionGroup.Alias
        $DistributionGroupsCmdlet += makeparam "DisplayName" $DistributionGroup.DisplayName
        $DistributionGroupsCmdlet += makeparam "ManagedBy" $DistributionGroup.ManagedBy

        $DistributionGroupsCmdlet += makeparam "Notes" $DistributionGroup.Notes
        $DistributionGroupsCmdlet += makeparam "PrimarySmtpAddress" $DistributionGroup.PrimarySmtpAddress
        $DistributionGroupsCmdlet += makeparam "Type" $DistributionGroup.Type
        $MembersCmdlet = "@("
        $memberslist = Import-Clixml $DistributionGroup.ExternalDirectoryObjectId
        ForEach ($user in $memberslist) {
            $MembersCmdlet += "`"$user.Name`","
        }
        $MembersCmdlet = $MembersCmdlet.TrimEnd(",")
        $MembersCmdlet += ")"
    }
    Add-Content $outfile "`n$DistributionGroupsCmdlet"
}
#****************************************************************************
# Add security groups
#****************************************************************************
$SecurityGroups = Import-Clixml ".\SecurityGroups.xml"
$SecurityGroupsCount = $SecurityGroups.Name.Count
if($SecurityGroupsCount -gt 0){
    Write-Host "Importing $SecurityGroupsCount Security Groups"
    ForEach ($SecurityGroup in $SecurityGroups) {
        $SecurityGroupsCmdlet = "New-EOPSecurityGroup"
        $SecurityGroupsCmdlet += makeparam "Name" $SecurityGroup.Name
        $SecurityGroupsCmdlet += makeparam "Alias" $SecurityGroup.Alias
        $SecurityGroupsCmdlet += makeparam "DisplayName" $SecurityGroup.DisplayName
        $SecurityGroupsCmdlet += makeparam "ManagedBy" $SecurityGroup.ManagedBy

        $SecurityGroupsCmdlet += makeparam "Notes" $SecurityGroup.Notes
        $SecurityGroupsCmdlet += makeparam "PrimarySmtpAddress" $SecurityGroup.PrimarySmtpAddress
        $SecurityGroupsCmdlet += makeparam "Type" $SecurityGroup.Type
        $MembersCmdlet = "@("
        $memberslist = Import-Clixml $SecurityGroup.ExternalDirectoryObjectId
        ForEach ($user in $memberslist) {
            $MembersCmdlet += "`"$user.Name`","
        }
        $MembersCmdlet = $MembersCmdlet.TrimEnd(",")
        $MembersCmdlet += ")"
    }
    Add-Content $outfile "`n$SecurityGroupsCmdlet"
}
#****************************************************************************
# Add Dynamic Distribution Groups
#****************************************************************************
$DynamicDistributionGroups = Import-Clixml ".\DynamicDistributionGroups.xml"
$DynamicDistributionGroupsCount = $DynamicDistributionGroups.Name.Count
if($DynamicDistributionGroupsCount -gt 0){
    Write-Host "Importing $DynamicDistributionGroupsCount Dynamic Distribution Groups"
    foreach ($DynamicDistributionGroup in $DynamicDistributionGroups) {
        $DynamicDistributionGroupsCmdlet = "New-DynamicDistributionGroup"
        $DynamicDistributionGroupsCmdlet += " -Confirm:`$False"
        $DynamicDistributionGroupsCmdlet += makeparam "DisplayName" $DynamicDistributionGroup.DisplayName
        $DynamicDistributionGroupsCmdlet += makeparam "ModeratedBy" $DynamicDistributionGroup.ModeratedBy
        $DynamicDistributionGroupsCmdlet += makeparam "ModerationEnabled" $DynamicDistributionGroup.ModerationEnabled
        $DynamicDistributionGroupsCmdlet += makeparam "Name" $DynamicDistributionGroup.Name
        $DynamicDistributionGroupsCmdlet += makeparam "PrimarySmtpAddress" $DynamicDistributionGroup.PrimarySmtpAddress
        $DynamicDistributionGroupsCmdlet += makeparam "RecipientContainer" $DynamicDistributionGroup.RecipientContainer
        $RecipientFilterParam =  makeparam "RecipientFilter" $DynamicDistributionGroup.RecipientFilter
        $RecipientFilterParam = " -RecipientFilter {" + $RecipientFilterParam.Substring(19)
        $RecipientFilterParam = $RecipientFilterParam.Substring(0,$RecipientFilterParam.Length-1)
        $RecipientFilterParam += "}"
        $DynamicDistributionGroupsCmdlet +=  $RecipientFilterParam
        $DynamicDistributionGroupsCmdlet += makeparam "SendModerationNotifications" $DynamicDistributionGroup.SendModerationNotifications
        Add-Content $outfile "`n$DynamicDistributionGroupsCmdlet"
    }

}else{
    Write-Host "No Dynamic Distribution Groups to add."
}
#****************************************************************************
# Add Mail Contacts
#****************************************************************************
$MailContacts = Import-Clixml ".\MailContacts.xml"
$MailContactsCount = $MailContacts.Name.Count
if($MailContactsCount -gt 0){
    Write-Host "Importing $MailContactsCount Dynamic Distribution Groups"
    foreach ($MailContact in $MailContacts) {
        $MailContactsCmdlet = "New-MailContact"
        $MailContactsCmdlet += makeparam "UsePreferMessageFormat" $MailContact.UsePreferMessageFormat
        $MailContactsCmdlet += makeparam "DisplayName" $MailContact.DisplayName
        $MailContactsCmdlet += makeparam "ModeratedBy" $MailContact.ModeratedBy
        $MailContactsCmdlet += makeparam "Name" $MailContact.Name
        $MailContactsCmdlet += makeparam "MessageBodyFormat" $MailContact.MessageBodyFormat
        $MailContactsCmdlet += makeparam "OrganizationalUnit" $MailContact.OrganizationalUnit
        $MailContactsCmdlet += makeparam "Initials" $MailContact.Initials
        $MailContactsCmdlet += makeparam "MessageFormat" $MailContact.MessageFormat
        $MailContactsCmdlet += makeparam "ModerationEnabled" $MailContact.ModerationEnabled
        $MailContactsCmdlet += makeparam "MacAttachmentFormat" $MailContact.MacAttachmentFormat
        $MailContactsCmdlet += makeparam "SendModerationNotifications" $MailContact.SendModerationNotifications
        $MailContactsCmdlet += " -Confirm:`$False"
        $MailContactsCmdlet += makeparam "ExternalEmailAddress" $MailContact.ExternalEmailAddress
        $MailContactsCmdlet += makeparam "FirstName" $MailContact.FirstName
        $MailContactsCmdlet += makeparam "Alias" $MailContact.Alias
        Add-Content $outfile "`n$MailContactsCmdlet"
    }

}else{
    Write-Host "No Mail Contacts to add."
}
```

## <a name="step-7-add-protection-settings-to-the-target-organization"></a><span data-ttu-id="be4d5-180">Étape 7 : Ajouter des paramètres de protection à l’organisation cible</span><span class="sxs-lookup"><span data-stu-id="be4d5-180">Step 7: Add protection settings to the target organization</span></span>

<span data-ttu-id="be4d5-181">Vous pouvez exécuter le script suivant à partir du répertoire Export lorsque vous êtes connecté à votre organisation cible pour recréer les paramètres exportés plus tôt vers des fichiers .xml depuis l’organisation source.</span><span class="sxs-lookup"><span data-stu-id="be4d5-181">You can run the following script from the Export directory while logged in to your target organization to recreate the settings exported to .xml files earlier from the source organization.</span></span>

<span data-ttu-id="be4d5-182">Copiez-collez le script suivant dans un éditeur de texte comme le Bloc-notes, enregistrez le fichier sous C:\EOP\Export\Import_Settings.ps1 et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="be4d5-182">Copy and paste the script text into a text editor like Notepad, save the file as C:\EOP\Export\Import_Settings.ps1, and run the following command:</span></span>

```PowerShell
& "C:\EOP\Export\Import_Settings.ps1"
```

<span data-ttu-id="be4d5-183">Ce script importe les fichiers .xml et crée un fichier de script Windows PowerShell appelé Settings.ps1, que vous pouvez consulter, modifier et exécuter pour recréer vos paramètres de protection et de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="be4d5-183">This script imports the .xml files and create a Windows PowerShell script file called Settings.ps1 that you can review, edit, and then run to recreate your protection and mail-flow settings.</span></span>

```PowerShell
#***********************************************************************
# makeparam helper function
#****************************************************************************
 function makeparam ([string]$ParamName, [string[]] $ParamValue) {
    $FormattedParam = ""
    If($ParamValue.Count -gt 0) {
        $FormattedParam = " -$ParamName "
        Foreach ($value in $ParamValue) {
        If($value -eq "True") {$FormattedParam = " -$ParamName" + ":`$True,"}
        else{
            If($value -eq "False") {$FormattedParam = " -$ParamName" + ":`$False,"}
                else{$FormattedParam += "`"$value`","}
            }
        }
        $FormattedParam = $FormattedParam.TrimEnd(",")
    }
    Return $FormattedParam
 }
#****************************************************************************
# Variables
#****************************************************************************
$outfile = ".\Settings.ps1"
rm -erroraction 'silentlycontinue' $outfile
#****************************************************************************
# HostedContentFilterPolicy
#****************************************************************************
$HostedContentFilterPolicies = Import-Clixml ".\HostedContentFilterPolicy.xml"
$HostedContentFilterPolicyCount = $HostedContentFilterPolicies.Name.Count
if($HostedContentFilterPolicyCount -gt 0){
    Write-Host "Importing $HostedContentFilterPolicyCount Inbound Connectors"
    ForEach ($HostedContentFilterPolicy in $HostedContentFilterPolicies) {
        $HostedContentFilterPolicyCmdlet = "New-HostedContentFilterPolicy"
        if($HostedContentFilterPolicy.Name -eq "Default") {$HostedContentFilterPolicyCmdlet = "Set-HostedContentFilterPolicy -Identity Default"}
        else {
        $HostedContentFilterPolicyCmdlet += makeparam "Name" $HostedContentFilterPolicy.Name
        }
        $HostedContentFilterPolicyCmdlet += makeparam "AddXHeaderValue" $HostedContentFilterPolicy.AddXHeaderValue
        $HostedContentFilterPolicyCmdlet += makeparam "AdminDisplayName" $HostedContentFilterPolicy.AdminDisplayName
        $HostedContentFilterPolicyCmdlet += " -Confirm:`$False"
        $HostedContentFilterPolicyCmdlet += makeparam "DownloadLink" $HostedContentFilterPolicy.DownloadLink
        $HostedContentFilterPolicyCmdlet += makeparam "EnableEndUserSpamNotifications" $HostedContentFilterPolicy.EnableEndUserSpamNotifications
        $HostedContentFilterPolicyCmdlet += makeparam "EnableLanguageBlockList" $HostedContentFilterPolicy.EnableLanguageBlockList
        $HostedContentFilterPolicyCmdlet += makeparam "EnableRegionBlockList" $HostedContentFilterPolicy.EnableRegionBlockList
        if($HostedContentFilterPolicy.EndUserSpamNotificationCustomFromAddress.Length -gt 0)
        {
            $HostedContentFilterPolicyCmdlet += makeparam "EndUserSpamNotificationCustomFromAddress" $HostedContentFilterPolicy.EndUserSpamNotificationCustomFromAddress
        }
        $HostedContentFilterPolicyCmdlet += makeparam "EndUserSpamNotificationCustomFromName" $HostedContentFilterPolicy.EndUserSpamNotificationCustomFromName
        $HostedContentFilterPolicyCmdlet += makeparam "EndUserSpamNotificationCustomSubject" $HostedContentFilterPolicy.EndUserSpamNotificationCustomSubject
        $HostedContentFilterPolicyCmdlet += makeparam "EndUserSpamNotificationFrequency" $HostedContentFilterPolicy.EndUserSpamNotificationFrequency
        $HostedContentFilterPolicyCmdlet += makeparam "EndUserSpamNotificationLanguage" $HostedContentFilterPolicy.EndUserSpamNotificationLanguage
        $HostedContentFilterPolicyCmdlet += makeparam "LanguageBlockList" $HostedContentFilterPolicy.LanguageBlockList
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamBulkMail" $HostedContentFilterPolicy.MarkAsSpamBulkMail
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamEmbedTagsInHtml" $HostedContentFilterPolicy.MarkAsSpamEmbedTagsInHtml
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamEmptyMessages" $HostedContentFilterPolicy.MarkAsSpamEmptyMessages
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamFormTagsInHtml" $HostedContentFilterPolicy.MarkAsSpamFormTagsInHtml
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamFramesInHtml" $HostedContentFilterPolicy.MarkAsSpamFramesInHtml
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamFromAddressAuthFail" $HostedContentFilterPolicy.MarkAsSpamFromAddressAuthFail
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamJavaScriptInHtml" $HostedContentFilterPolicy.MarkAsSpamJavaScriptInHtml
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamNdrBackscatter" $HostedContentFilterPolicy.MarkAsSpamNdrBackscatter
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamObjectTagsInHtml" $HostedContentFilterPolicy.MarkAsSpamObjectTagsInHtml
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamSensitiveWordList" $HostedContentFilterPolicy.MarkAsSpamSensitiveWordList
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamSpfRecordHardFail" $HostedContentFilterPolicy.MarkAsSpamSpfRecordHardFail
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamWebBugsInHtml" $HostedContentFilterPolicy.MarkAsSpamWebBugsInHtml
        $HostedContentFilterPolicyCmdlet += makeparam "ModifySubjectValue" $HostedContentFilterPolicy.ModifySubjectValue
        $HostedContentFilterPolicyCmdlet += makeparam "Organization" $HostedContentFilterPolicy.Organization
        $HostedContentFilterPolicyCmdlet += makeparam "QuarantineRetentionPeriod" $HostedContentFilterPolicy.QuarantineRetentionPeriod
        $HostedContentFilterPolicyCmdlet += makeparam "RedirectToRecipients" $HostedContentFilterPolicy.RedirectToRecipients
        $HostedContentFilterPolicyCmdlet += makeparam "RegionBlockList" $HostedContentFilterPolicy.RegionBlockList
        $HostedContentFilterPolicyCmdlet += makeparam "SpamAction" $HostedContentFilterPolicy.SpamAction
        $HostedContentFilterPolicyCmdlet += makeparam "TestModeBccToRecipients" $HostedContentFilterPolicy.TestModeBccToRecipients
        Add-Content $outfile "`n$HostedContentFilterPolicyCmdlet"
    }
 }else{
    Write-Host "No Hosted Content Policy Filters to add."
 }
#****************************************************************************
# HostedContentFilterRule
#****************************************************************************
$HostedContentFilterRules = Import-Clixml ".\HostedContentFilterRule.xml"
$HostedContentFilterRuleCount = $HostedContentFilterRules.Name.Count
if($HostedContentFilterPolicyCount -gt 0){
    Write-Host "Importing $HostedContentFilterRuleCount Hosted Content Filter Rules"
    ForEach ($HostedContentFilterRule in $HostedContentFilterRules) {
        $HostedContentFilterRuleCmdlet = "New-HostedContentFilterRule"
        if($HostedContentFilterRule.Name -eq "Default") {$HostedContentFilterRuleCmdlet = "Set-HostedContentFilterRule Default"}
        $HostedContentFilterRuleCmdlet += makeparam "Name" $HostedContentFilterRule.Name
        $HostedContentFilterRuleCmdlet  += makeparam "HostedContentFilterPolicy" $HostedContentFilterRule.HostedContentFilterPolicy
        $HostedContentFilterRuleCmdlet += makeparam "Comments" $HostedContentFilterRule.Comments
        $HostedContentFilterRuleCmdlet += " -Confirm:`$False"
        $HostedContentFilterRuleCmdlet += makeparam "Enabled" $HostedContentFilterRule.Enabled
        $HostedContentFilterRuleCmdlet += makeparam "ExceptIfRecipientDomainIs" $HostedContentFilterRule.ExceptIfRecipientDomainIs
        $HostedContentFilterRuleCmdlet += makeparam "ExceptIfSentTo" $HostedContentFilterRule.ExceptIfSentTo
        $HostedContentFilterRuleCmdlet += makeparam "ExceptIfSentToMemberOf" $HostedContentFilterRule.ExceptIfSentToMemberOf
        $HostedContentFilterRuleCmdlet += makeparam "Priority" $HostedContentFilterRule.Priority
        $HostedContentFilterRuleCmdlet += makeparam "RecipientDomainIs" $HostedContentFilterRule.RecipientDomainIs
        $HostedContentFilterRuleCmdlet += makeparam "SentTo" $HostedContentFilterRule.SentTo
        $HostedContentFilterRuleCmdlet += makeparam "SentToMemberOf" $HostedContentFilterRule.SentToMemberOf
        Add-Content $outfile "`n$HostedContentFilterRuleCmdlet"
    }
 }else{
    Write-Host "No Hosted Content Filter Rules to add."
 }
#****************************************************************************
# HostedOutboundSpamFilterPolicy
#****************************************************************************
$HostedOutboundSpamFilterPolicies = Import-Clixml ".\HostedOutboundSpamFilterPolicy.xml"
$HostedOutboundSpamFilterPolicyCount = $HostedOutboundSpamFilterPolicies.Name.Count
if($HostedContentFilterPolicyCount -gt 0){
    Write-Host "Importing $HostedOutboundSpamFilterPolicyCount Hosted Outbound Spam Filter Policies"
    ForEach ($HostedOutboundSpamFilterPolicy in $HostedOutboundSpamFilterPolicies) {
        $HostedOutboundSpamFilterPolicyCmdlet = "Set-HostedOutboundSpamFilterPolicy Default"
        $HostedOutboundSpamFilterPolicyCmdlet += makeparam "AdminDisplayName" $HostedOutboundSpamFilterPolicy.AdminDisplayName
        $HostedOutboundSpamFilterPolicyCmdlet += makeparam "BccSuspiciousOutboundAdditionalRecipients"
        $HostedOutboundSpamFilterPolicy.BccSuspiciousOutboundAdditionalRecipients
        $HostedOutboundSpamFilterPolicyCmdlet += makeparam "BccSuspiciousOutboundMail" $HostedOutboundSpamFilterPolicy.BccSuspiciousOutboundMail
        $HostedOutboundSpamFilterPolicyCmdlet += " -Confirm:`$False"
        $HostedOutboundSpamFilterPolicyCmdlet += makeparam "NotifyOutboundSpam" $HostedOutboundSpamFilterPolicy.NotifyOutboundSpam
        $NotifyOutboundSpamRecipients  += makeparam "NotifyOutboundSpamRecipients" $HostedOutboundSpamFilterPolicy.NotifyOutboundSpamRecipients
        Add-Content $outfile "`n$HostedOutboundSpamFilterPolicyCmdlet"
    }
 }else{
    Write-Host "No Hosted Outbound Spam Filter Policies to add."
 }
#****************************************************************************
# HostedConnectionFilterPolicy
#****************************************************************************
$HostedConnectionFilterPolicies = Import-Clixml ".\HostedConnectionFilterPolicy.xml"
$HostedConnectionFilterPolicyCount = $HostedConnectionFilterPolicies.Name.Count
if($HostedContentFilterPolicyCount -gt 0){
    Write-Host "Importing $HostedConnectionFilterPolicyCount Hosted Connection Filter Policies"
    ForEach ($HostedConnectionFilterPolicy in $HostedConnectionFilterPolicies) {
        $HostedConnectionFilterPolicyCmdlet = "Set-HostedConnectionFilterPolicy"
        $HostedConnectionFilterPolicyCmdlet += makeparam "Identity" $HostedConnectionFilterPolicy.Name
        $HostedConnectionFilterPolicyCmdlet += makeparam "AdminDisplayName" $HostedConnectionFilterPolicy.AdminDisplayName
        $HostedConnectionFilterPolicyCmdlet += " -Confirm:`$False"
        $HostedConnectionFilterPolicyCmdlet += makeparam "EnableSafeList" $HostedConnectionFilterPolicy.EnableSafeList
        $HostedConnectionFilterPolicyCmdlet += makeparam "IPAllowList" $HostedConnectionFilterPolicy.IPAllowList
        $HostedConnectionFilterPolicyCmdlet += makeparam "IPBlockList" $HostedConnectionFilterPolicy.IPBlockList

        Add-Content $outfile "`n$HostedConnectionFilterPolicyCmdlet"
    }
 }else{
    Write-Host "No Hosted Connection Filter Policies to add."
 }
#****************************************************************************
# MalwareFilterPolicy
#****************************************************************************
$MalwareFilterPolicies = Import-Clixml ".\MalwareFilterPolicy.xml"
$MalwareFilterPolicyCount = $MalwareFilterPolicies.Name.Count
if($HostedContentFilterPolicyCount -gt 0){
    Write-Host "Importing $MalwareFilterPolicyCount Malware Filter Policies"
    ForEach ($MalwareFilterPolicy in $MalwareFilterPolicies) {
        $MalwareFilterPolicyCmdlet = "New-MalwareFilterPolicy"
        if($MalwareFilterPolicy.Name -eq "Default") {$MalwareFilterPolicyCmdlet = "Set-MalwareFilterPolicy Default"}
        else {
        $MalwareFilterPolicyCmdlet += makeparam "Name" $MalwareFilterPolicy.Name
        }
        $MalwareFilterPolicyCmdlet += makeparam "Action" $MalwareFilterPolicy.Action
        $MalwareFilterPolicyCmdlet += makeparam "DeleteAttachmentAndUseDefaultAlertText" $MalwareFilterPolicy.DeleteAttachmentAndUseDefaultAlertText
        $MalwareFilterPolicyCmdlet += makeparam "DeleteAttachmentAndUseCustomAlertText" $MalwareFilterPolicy.DeleteAttachmentAndUseCustomAlertText
        $MalwareFilterPolicyCmdlet += makeparam "AdminDisplayName" $MalwareFilterPolicy.AdminDisplayName
        $MalwareFilterPolicyCmdlet += " -Confirm:`$False"
        $MalwareFilterPolicyCmdlet += makeparam "CustomAlertText" $MalwareFilterPolicy.CustomAlertText
        $MalwareFilterPolicyCmdlet += makeparam "CustomExternalBody" $MalwareFilterPolicy.CustomExternalBody
        $MalwareFilterPolicyCmdlet += makeparam "CustomExternalSubject" $MalwareFilterPolicy.CustomExternalSubject
        if($MalwareFilterPolicy.CustomFromAddress.Length -gt 0) {
            $MalwareFilterPolicyCmdlet += makeparam "CustomFromAddress" $MalwareFilterPolicy.CustomFromAddress
        }
        $MalwareFilterPolicyCmdlet += makeparam "CustomFromName" $MalwareFilterPolicy.CustomFromName
        $MalwareFilterPolicyCmdlet += makeparam "CustomInternalBody" $MalwareFilterPolicy.CustomInternalBody
        $MalwareFilterPolicyCmdlet += makeparam "CustomInternalSubject" $MalwareFilterPolicy.CustomInternalSubject
        $MalwareFilterPolicyCmdlet += makeparam "CustomNotifications" $MalwareFilterPolicy.CustomNotifications
        $MalwareFilterPolicyCmdlet += makeparam "EnableExternalSenderAdminNotifications" $MalwareFilterPolicy.EnableExternalSenderAdminNotifications
        $MalwareFilterPolicyCmdlet += makeparam "EnableExternalSenderNotifications" $MalwareFilterPolicy.EnableExternalSenderNotifications
        $MalwareFilterPolicyCmdlet += makeparam "EnableInternalSenderAdminNotifications" $MalwareFilterPolicy.EnableInternalSenderAdminNotifications
        $MalwareFilterPolicyCmdlet += makeparam "EnableInternalSenderNotifications" $MalwareFilterPolicy.EnableInternalSenderNotifications
        if($MalwareFilterPolicy.ExternalSenderAdminAddress.Length -gt 0) {
        $MalwareFilterPolicyCmdlet += makeparam "ExternalSenderAdminAddress" $MalwareFilterPolicy.ExternalSenderAdminAddress
        }
        if($MalwareFilterPolicy.InternalSenderAdminAddress.Length -gt 0) {
        $MalwareFilterPolicyCmdlet += makeparam "InternalSenderAdminAddress" $MalwareFilterPolicy.InternalSenderAdminAddress
        }
        Add-Content $outfile "`n$MalwareFilterPolicyCmdlet"
    }
 }else{
    Write-Host "No Malware Filter Policies to add."
 }
#****************************************************************************
# MalwareFilterRule
#****************************************************************************
$MalwareFilterRules = Import-Clixml ".\MalwareFilterRule.xml"
$MalwareFilterRuleCount = $MalwareFilterRules.Name.Count
if($HostedContentFilterPolicyCount -gt 0){
    Write-Host "Importing $MalwareFilterRuleCount Malware Filter Rules"
    ForEach ($MalwareFilterRule in $MalwareFilterRules) {
        $MalwareFilterRuleCmdlet = "New-MalwareFilterRule"
        if($MalwareFilterRule.Name -eq "Default") {$MalwareFilterRuleCmdlet = "Set-MalwareFilterPolicy Default"}
        $MalwareFilterRuleCmdlet += makeparam "Name" $MalwareFilterRule.Name
        $MalwareFilterRuleCmdlet += makeparam "MalwareFilterPolicy" $MalwareFilterRule.MalwareFilterPolicy
        $MalwareFilterRuleCmdlet += makeparam "Comments" $MalwareFilterRule.Comments
        $MalwareFilterRuleCmdlet += " -Confirm:`$False"
        $MalwareFilterRuleCmdlet += makeparam "Enabled" $MalwareFilterRule.Enabled
        $MalwareFilterRuleCmdlet += makeparam "ExceptIfRecipientDomainIs" $MalwareFilterRule.ExceptIfRecipientDomainIs
        $MalwareFilterRuleCmdlet += makeparam "ExceptIfSentTo" $MalwareFilterRule.ExceptIfSentTo
        $MalwareFilterRuleCmdlet += makeparam "ExceptIfSentToMemberOf" $MalwareFilterRule.ExceptIfSentToMemberOf
        $MalwareFilterRuleCmdlet += makeparam "RecipientDomainIs" $MalwareFilterRule.RecipientDomainIs
        $MalwareFilterRuleCmdlet += makeparam "SentTo" $MalwareFilterRule.SentTo
        $MalwareFilterRuleCmdlet += makeparam "SentToMemberOf" $MalwareFilterRule.SentToMemberOf
        Add-Content $outfile "`n$MalwareFilterRuleCmdlet"
    }
 }else{
    Write-Host "No Malware Filter Rules to add."
 }
#****************************************************************************
# InboundConnectors
#****************************************************************************
$InboundConnectors = Import-Clixml ".\InboundConnector.xml"
$InboundConnectorCount = $InboundConnectors.Name.Count
if($InboundConnectorCount -gt 0){
    Write-Host "Importing $InboundConnectorCount Inbound Connectors"
    ForEach ($InboundConnector in $InboundConnectors) {
        $InboundConnectorCmdlet = "New-InboundConnector"
        $InboundConnectorCmdlet += makeparam "Name" $InboundConnector.Name
        $InboundConnectorCmdlet += makeparam "SenderDomains" $InboundConnector.SenderDomains

        If($InboundConnector.AssociatedAcceptedDomains.Count -gt 0) {
            If($InboundConnector.AssociatedAcceptedDomains[0].Contains("/")) {
                # This connector was created in an EOP Standard tenant
                # Strip out just the domain name
                $InboundConnectorCmdlet += " -AssociatedAcceptedDomains "
                ForEach  ($accepteddomain in $InboundConnectors.AssociatedAcceptedDomains) {
                    $accepteddomain = $accepteddomain.SubString($accepteddomain.LastIndexOf("/")+1)
                    $InboundConnectorCmdlet += "`"$accepteddomain`","
                }
                $InboundConnectorCmdlet = $InboundConnectorCmdlet.TrimEnd(",")
            }else{
                $InboundConnectorCmdlet += makeparam "AssociatedAcceptedDomains" $InboundConnector.AssociatedAcceptedDomains
            }
        }

        $InboundConnectorCmdlet += makeparam "CloudServicesMailEnabled" $InboundConnector.CloudServicesMailEnabled
        $InboundConnectorCmdlet += makeparam "Comment" $InboundConnector.Comment
        $InboundConnectorCmdlet += " -Confirm:`$False"
        $InboundConnectorCmdlet += makeparam "ConnectorSource" $InboundConnector.ConnectorSource
        $InboundConnectorCmdlet += makeparam "ConnectorType" $InboundConnector.ConnectorType
        $InboundConnectorCmdlet += makeparam "Enabled" $InboundConnector.Enabled
        $InboundConnectorCmdlet += makeparam "RequireTls" $InboundConnector.RequireTls
        $InboundConnectorCmdlet += makeparam "RestrictDomainsToCertificate" $InboundConnector.RestrictDomainsToCertificate
        $InboundConnectorCmdlet += makeparam "RestrictDomainsToIPAddresses" $InboundConnector.RestrictDomainsToIPAddresses
        $InboundConnectorCmdlet += makeparam "SenderIPAddresses" $InboundConnector.SenderIPAddresses
        $InboundConnectorCmdlet += makeparam "TlsSenderCertificateName" $InboundConnector.TlsSenderCertificateName
        Add-Content $outfile "`n$InboundConnectorCmdlet"
     }
}else{
    Write-Host "No Inbound Connectors to add."
 }
#****************************************************************************
# OutboundConnector
#****************************************************************************
$OutboundConnectors = Import-Clixml ".\OutboundConnector.xml"
$OutboundConnectorCount = $OutboundConnectors.Name.Count
if($OutboundConnectorCount -gt 0){
    Write-Host "Importing $OutboundConnectorCount Outbound Connectors"
    ForEach ($OutboundConnector in $OutboundConnectors) {
        $OutboundConnectorCmdlet = "New-OutboundConnector"
        $OutboundConnectorCmdlet += makeparam "Name" $OutboundConnector.Name
        $OutboundConnectorCmdlet += makeparam "AllAcceptedDomains" $OutboundConnector.AllAcceptedDomains
        $OutboundConnectorCmdlet += makeparam "BypassValidation" $OutboundConnector.BypassValidation
        $OutboundConnectorCmdlet += makeparam "CloudServicesMailEnabled" $OutboundConnector.CloudServicesMailEnabled
        $OutboundConnectorCmdlet += makeparam "Comment" $OutboundConnector.Comment
        $OutboundConnectorCmdlet += " -Confirm:`$False"
        $OutboundConnectorCmdlet += makeparam "ConnectorSource" $OutboundConnector.ConnectorSource
        $OutboundConnectorCmdlet += makeparam "ConnectorType" $OutboundConnector.ConnectorType
        $OutboundConnectorCmdlet += makeparam "IsTransportRuleScoped" $OutboundConnector.IsTransportRuleScoped
        $OutboundConnectorCmdlet += makeparam "RecipientDomains" $OutboundConnector.RecipientDomains
        $OutboundConnectorCmdlet += makeparam "RouteAllMessagesViaOnPremises" $OutboundConnector.RouteAllMessagesViaOnPremises
        $OutboundConnectorCmdlet += makeparam "SmartHosts" $OutboundConnector.SmartHosts
        $OutboundConnectorCmdlet += makeparam "TlsDomain" $OutboundConnector.TlsDomain
        $OutboundConnectorCmdlet += makeparam "TlsSettings" $OutboundConnector.TlsSettings
        $OutboundConnectorCmdlet += makeparam "UseMXRecord" $OutboundConnector.UseMXRecord
        Add-Content $outfile "`n$OutboundConnectorCmdlet"
    }
 }else{
    Write-Host "No Outbound Connectors to add."
 }
#*****************************************************************************
# TransportRule
#*****************************************************************************
Add-Content $outfile "`n[Byte[]]$Data = Get-Content -Path `".TransportRules.xml`" -Encoding Byte -ReadCount 0"
Add-Content $outfile "`nImport-TransportRuleCollection -FileData $Data"
#****************************************************************************
# Domain Type
#****************************************************************************
$Domains = Import-Clixml ".\Domains.xml"
$DomainCount = $Domains.Name.Count
if($HostedContentFilterPolicyCount -gt 0){
    Write-Host "Importing $DomainCount Domains"
    ForEach ($Domain in $Domains) {
        $DomainCmdlet = "Set-AcceptedDomain"
        $DomainCmdlet += makeparam "Identity" $Domain.Name
        $DomainCmdlet += makeparam "DomainType" $Domain.DomainType
        Add-Content $outfile "`n$DomainCmdlet"
    }
 }else{
    Write-Host "No Domains to add."
 }
```

## <a name="step-8-revert-your-dns-settings-to-stop-mail-queuing"></a><span data-ttu-id="be4d5-184">Étape 8 : Rétablir vos paramètres DNS pour interrompre la mise en attente des messages</span><span class="sxs-lookup"><span data-stu-id="be4d5-184">Step 8: Revert your DNS settings to stop mail queuing</span></span>

<span data-ttu-id="be4d5-185">Si vous avez choisi de définir vos enregistrements MX sur une adresse non valide pour que les expéditeurs placent les [](https://admin.microsoft.com)messages en file d’attente pendant votre transition, vous devez les définir à nouveau sur la valeur correcte, comme spécifié dans le Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="be4d5-185">If you chose to set your MX records to an invalid address to cause the senders to queue mail during your transition, you'll need to set them back to the correct value as specified in the [admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="be4d5-186">Pour plus d’informations sur la configuration du DNS, voir Créer des enregistrements DNS chez un fournisseur d’hébergement [DNS pour Microsoft 365.](../../admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md)</span><span class="sxs-lookup"><span data-stu-id="be4d5-186">For more information about configuring DNS, see [Create DNS records at any DNS hosting provider for Microsoft 365](../../admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span></span>