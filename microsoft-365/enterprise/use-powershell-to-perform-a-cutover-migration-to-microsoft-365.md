---
title: Utilisation de PowerShell pour effectuer une migration à basculement vers Microsoft 365
ms.author: sirkkuw
author: sirkkuw
manager: laurawi
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
ms.assetid: b468cb4b-a35c-43d3-85bf-65446998af40
description: Découvrez comment utiliser PowerShell pour déplacer le contenu d’un système de courrier source en une seule fois en effectuant une migration à basculement vers Microsoft 365.
ms.openlocfilehash: 74e7791c4292598e4717e56af25e39b3c8208108
ms.sourcegitcommit: dffb9b72acd2e0bd286ff7e79c251e7ec6e8ecae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "47948195"
---
# <a name="use-powershell-to-perform-a-cutover-migration-to-microsoft-365"></a><span data-ttu-id="0368b-103">Utilisation de PowerShell pour effectuer une migration à basculement vers Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0368b-103">Use PowerShell to perform a cutover migration to Microsoft 365</span></span>

<span data-ttu-id="0368b-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="0368b-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="0368b-105">Vous pouvez migrer le contenu des boîtes aux lettres utilisateur à partir d’un système de messagerie source vers Microsoft 365 en une seule fois à l’aide d’une migration à basculement.</span><span class="sxs-lookup"><span data-stu-id="0368b-105">You can migrate the contents of user mailboxes from a source email system to Microsoft 365 all at once by using a cutover migration.</span></span> <span data-ttu-id="0368b-106">Cet article décrit les tâches correspondant à une migration de messagerie à basculement à l'aide d'Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0368b-106">This article walks you through the tasks for an email cutover migration by using Exchange Online PowerShell.</span></span>

<span data-ttu-id="0368b-107">En examinant la rubrique, [ce que vous devez savoir sur une migration de courrier à basculement vers Microsoft 365](https://go.microsoft.com/fwlink/p/?LinkId=536688), vous pouvez obtenir une vue d’ensemble du processus de migration.</span><span class="sxs-lookup"><span data-stu-id="0368b-107">By reviewing the topic, [What you need to know about a cutover email migration to Microsoft 365](https://go.microsoft.com/fwlink/p/?LinkId=536688), you can get an overview of the migration process.</span></span> <span data-ttu-id="0368b-108">Lorsque le contenu de cet article vous est familier, utilisez celui-ci pour commencer la migration de boîtes aux lettres d'un système à l'autre.</span><span class="sxs-lookup"><span data-stu-id="0368b-108">When you're comfortable with the contents of that article, use this one to begin migrating mailboxes from one email system to another.</span></span>

> [!NOTE]
> <span data-ttu-id="0368b-109">Vous pouvez également utiliser le Centre d'administration Exchange pour effectuer la migration à basculement.</span><span class="sxs-lookup"><span data-stu-id="0368b-109">You can also use the Exchange admin center to perform a cutover migration.</span></span> <span data-ttu-id="0368b-110">Voir [effectuer une migration à basculement de la messagerie vers Microsoft 365](https://go.microsoft.com/fwlink/p/?LinkId=536689).</span><span class="sxs-lookup"><span data-stu-id="0368b-110">See [Perform a cutover migration of email to Microsoft 365](https://go.microsoft.com/fwlink/p/?LinkId=536689).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="0368b-111">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="0368b-111">What do you need to know before you begin?</span></span>

<span data-ttu-id="0368b-112">Durée d'exécution estimée de cette tâche : entre 2 et 5 minutes pour créer un lot de migration.</span><span class="sxs-lookup"><span data-stu-id="0368b-112">Estimated time to complete this task: 2-5 minutes to create a migration batch.</span></span> <span data-ttu-id="0368b-113">Une fois la migration du lot commencée, la durée de l'opération varie en fonction du nombre de boîtes aux lettres incluses dans le lot, de la taille de chacune d'elles et de la capacité réseau disponible.</span><span class="sxs-lookup"><span data-stu-id="0368b-113">After the migration batch is started, the duration of the migration will vary based on the number of mailboxes in the batch, the size of each mailbox, and your available network capacity.</span></span> <span data-ttu-id="0368b-114">Pour plus d’informations sur les autres facteurs qui influent sur la durée de migration des boîtes aux lettres vers Microsoft 365, consultez la rubrique performance de la [migration](https://go.microsoft.com/fwlink/p/?LinkId=275079).</span><span class="sxs-lookup"><span data-stu-id="0368b-114">For information about other factors that affect how long it takes to migrate mailboxes to Microsoft 365, see [Migration Performance](https://go.microsoft.com/fwlink/p/?LinkId=275079).</span></span>

<span data-ttu-id="0368b-p105">Des autorisations doivent vous être attribuées avant que vous puissiez exécuter cette procédure. Pour connaître les autorisations nécessaires, consultez l'entrée « Migration » dans un tableau de la rubrique [Autorisations des destinataires](https://go.microsoft.com/fwlink/p/?LinkId=534105).</span><span class="sxs-lookup"><span data-stu-id="0368b-p105">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Migration" entry in a table in the [Recipients Permissions](https://go.microsoft.com/fwlink/p/?LinkId=534105) topic.</span></span>

<span data-ttu-id="0368b-p106">Pour utiliser les cmdlets Exchange Online PowerShell, vous devez vous connecter et importer les cmdlets dans votre session Windows PowerShell locale. Pour des instructions, voir [Connexion à Exchange Online à l'aide de Remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=534121).</span><span class="sxs-lookup"><span data-stu-id="0368b-p106">To use the Exchange Online PowerShell cmdlets, you need to sign in and import the cmdlets into your local Windows PowerShell session. See [Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=534121) for instructions.</span></span>

<span data-ttu-id="0368b-119">Pour la liste complète des commandes de migration, voir [Cmdlets de déplacement et de migration](https://go.microsoft.com/fwlink/p/?LinkId=534750).</span><span class="sxs-lookup"><span data-stu-id="0368b-119">For a full list of migration commands, see [Move and migration cmdlets](https://go.microsoft.com/fwlink/p/?LinkId=534750).</span></span>

## <a name="migration-steps"></a><span data-ttu-id="0368b-120">Étapes de migration</span><span class="sxs-lookup"><span data-stu-id="0368b-120">Migration steps</span></span>

### <a name="step-1-prepare-for-a-cutover-migration"></a><span data-ttu-id="0368b-121">Étape 1 : Préparez une migration à basculement</span><span class="sxs-lookup"><span data-stu-id="0368b-121">Step 1: Prepare for a cutover migration</span></span>
<span data-ttu-id="0368b-122"><a name="BK_Step1"> </a></span><span class="sxs-lookup"><span data-stu-id="0368b-122"><a name="BK_Step1"> </a></span></span>

- <span data-ttu-id="0368b-123">**Ajoutez votre organisation Exchange locale en tant que domaine accepté de votre organisation Microsoft 365.**</span><span class="sxs-lookup"><span data-stu-id="0368b-123">**Add your on-premises Exchange organization as an accepted domain of your Microsoft 365 organization.**</span></span> <span data-ttu-id="0368b-124">Le service de migration utilise l’adresse SMTP de vos boîtes aux lettres locales pour créer l’ID d’utilisateur et l’adresse de messagerie Microsoft Online Services pour les nouvelles boîtes aux lettres Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0368b-124">The migration service uses the SMTP address of your on-premises mailboxes to create the Microsoft Online Services user ID and email address for the new Microsoft 365 mailboxes.</span></span> <span data-ttu-id="0368b-125">La migration échoue si votre domaine Exchange n’est pas un domaine accepté ou le domaine principal de votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0368b-125">Migration will fail if your Exchange domain isn't an accepted domain or the primary domain of your Microsoft 365 organization.</span></span> <span data-ttu-id="0368b-126">Pour plus d’informations, consultez [la rubrique Verify Your Domain](https://go.microsoft.com/fwlink/p/?LinkId=534110).</span><span class="sxs-lookup"><span data-stu-id="0368b-126">For more information, see [Verify your domain](https://go.microsoft.com/fwlink/p/?LinkId=534110).</span></span>

- <span data-ttu-id="0368b-p108">**Configurez Outlook Anywhere sur votre serveur Exchange local** Le service de migration de messagerie utilise RPC sur HTTP ou Outlook Anywhere pour se connecter à votre serveur Exchange local. Pour plus d'informations sur la configuration d'Outlook Anywhere pour Exchange 2010, 2007 et 2003, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="0368b-p108">**Configure Outlook Anywhere on your on-premises Exchange server.** The email migration service uses RPC over HTTP, or Outlook Anywhere, to connect to your on-premises Exchange server. For information about how to set up Outlook Anywhere for Exchange 2010, Exchange 2007, and Exchange 2003, see the following:</span></span>

  - [<span data-ttu-id="0368b-130">Exchange 2010 : Activer Outlook Anywhere</span><span class="sxs-lookup"><span data-stu-id="0368b-130">Exchange 2010: Enable Outlook Anywhere</span></span>](https://go.microsoft.com/fwlink/?LinkID=187249)

  - [<span data-ttu-id="0368b-131">Exchange 2007 : Procédure d'activation d'Outlook Anywhere</span><span class="sxs-lookup"><span data-stu-id="0368b-131">Exchange 2007: How to Enable Outlook Anywhere</span></span>](https://go.microsoft.com/fwlink/?LinkID=167210)

  - [<span data-ttu-id="0368b-132">Exchange 2003 : Scénarios de déploiement RPC sur HTTP</span><span class="sxs-lookup"><span data-stu-id="0368b-132">Exchange 2003: Deployment Scenarios for RPC over HTTP</span></span>](https://go.microsoft.com/fwlink/?LinkID=73657)

  - [<span data-ttu-id="0368b-133">Procédure de configuration d'Outlook Anywhere avec Exchange 2003</span><span class="sxs-lookup"><span data-stu-id="0368b-133">How to Configure Outlook Anywhere with Exchange 2003</span></span>](https://go.microsoft.com/fwlink/?LinkID=167209)

    > [!IMPORTANT]
    > <span data-ttu-id="0368b-p109">La configuration d'Outlook Anywhere doit être réalisée à l'aide d'un certificat émis par une autorité de certification (CA) approuvée. Il ne peut être configuré à l'aide d'un certificat auto-signé. Pour plus d'informations, consultez la rubrique [Procédure de configuration de SSL pour Outlook Anywhere](https://go.microsoft.com/fwlink/?LinkID=80875).</span><span class="sxs-lookup"><span data-stu-id="0368b-p109">Your Outlook Anywhere configuration must be configured with a certificate issued by a trusted certification authority (CA). It can't be configured with a self-signed certificate. For more information, see [How to Configure SSL for Outlook Anywhere](https://go.microsoft.com/fwlink/?LinkID=80875).</span></span>

- <span data-ttu-id="0368b-p110">**Vérifiez que vous pouvez vous connecter à votre organisation Exchange à l'aide d'Outlook Anywhere** Pour tester vos paramètres de connexion, essayez l'une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0368b-p110">**Verify that you can connect to your Exchange organization using Outlook Anywhere.** Try one of these methods to test your connection settings:</span></span>

  - <span data-ttu-id="0368b-139">Utilisez Microsoft Outlook hors de votre réseau d'entreprise pour vous connecter à votre boîte aux lettres Exchange locale.</span><span class="sxs-lookup"><span data-stu-id="0368b-139">Use Microsoft Outlook from outside your corporate network to connect to your on-premises Exchange mailbox.</span></span>

  - <span data-ttu-id="0368b-p111">Utilisez l'[analyseur de connectivité à distance Exchange](https://www.testexchangeconnectivity.com/) de Microsoft pour tester vos paramètres de connexion. Utilisez Outlook Anywhere (RPC sur HTTP) ou les tests de découverte automatique d'Outlook.</span><span class="sxs-lookup"><span data-stu-id="0368b-p111">Use the Microsoft [Exchange Remote Connectivity Analyzer](https://www.testexchangeconnectivity.com/) to test your connection settings. Use the Outlook Anywhere (RPC over HTTP) or Outlook Autodiscover tests.</span></span>

  - <span data-ttu-id="0368b-142">Dans Exchange Online PowerShell, exécutez les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0368b-142">Run the following commands in Exchange Online PowerShell.</span></span>

  ```powershell
  $Credentials = Get-Credential
  ```

  ```powershell
  Test-MigrationServerAvailability -ExchangeOutlookAnywhere -Autodiscover -EmailAddress <email address for on-premises administrator> -Credentials $credentials
  ```

- <span data-ttu-id="0368b-143">**Attribuez à un compte d'utilisateur local les autorisations nécessaires pour accéder aux boîtes aux lettres de votre organisation Exchange.**</span><span class="sxs-lookup"><span data-stu-id="0368b-143">**Assign an on-premises user account the necessary permissions to access mailboxes in your Exchange organization.**</span></span> <span data-ttu-id="0368b-144">Le compte d’utilisateur local que vous utilisez pour vous connecter à votre organisation Exchange locale (également appelé administrateur de migration) doit disposer des autorisations nécessaires pour accéder aux boîtes aux lettres locales que vous souhaitez migrer vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0368b-144">The on-premises user account that you use to connect to your on-premises Exchange organization (also called the migration administrator) must have the necessary permissions to access the on-premises mailboxes that you want to migrate to Microsoft 365.</span></span> <span data-ttu-id="0368b-145">Ce compte d'utilisateur permet de créer un point de terminaison de migration pour votre organisation locale.</span><span class="sxs-lookup"><span data-stu-id="0368b-145">This user account is used to create a migration endpoint to your on-premises organization.</span></span>

    <span data-ttu-id="0368b-p113">La liste suivante montre les privilèges administratifs requis pour migrer des boîtes aux lettres à l'aide d'une migration à basculement. Trois options sont possibles.</span><span class="sxs-lookup"><span data-stu-id="0368b-p113">The following list shows the administrative privileges required to migrate mailboxes using a cutover migration. There are three possible options.</span></span>

  - <span data-ttu-id="0368b-148">L'administrateur de migration doit être membre du groupe **Administrateurs de domaine** dans Active Directory au sein de l'organisation locale.</span><span class="sxs-lookup"><span data-stu-id="0368b-148">The migration administrator must be a member of the **Domain Admins** group in Active Directory in the on-premises organization.</span></span>

    <span data-ttu-id="0368b-149">Ou</span><span class="sxs-lookup"><span data-stu-id="0368b-149">Or</span></span>

  - <span data-ttu-id="0368b-150">L'administrateur de migration doit disposer de l'autorisation **FullAccess** pour chaque boîte aux lettres locale.</span><span class="sxs-lookup"><span data-stu-id="0368b-150">The migration administrator must be assigned the **FullAccess** permission for each on-premises mailbox.</span></span>

    <span data-ttu-id="0368b-151">Ou</span><span class="sxs-lookup"><span data-stu-id="0368b-151">Or</span></span>

  - <span data-ttu-id="0368b-152">L'administrateur de migration doit disposer de l'autorisation **Receive As** pour la base de données de boîtes aux lettres locale stockant les boîtes aux lettres d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0368b-152">The migration administrator must be assigned the **Receive As** permission on the on-premises mailbox database that stores the user mailboxes.</span></span>

- <span data-ttu-id="0368b-p114">**Désactivez la messagerie unifiée.** Si les boîtes aux lettres locales que vous migrez sont activées pour la messagerie unifiée, vous devez désactiver cette dernière avant de procéder à la migration. Une fois la migration terminée, vous pouvez activer la messagerie unifiée sur les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="0368b-p114">**Disable Unified Messaging.** If the on-premises mailboxes you're migrating are enabled for Unified Messaging (UM), you have to disable UM on the mailboxes before you migrate them. You can then enable UM on the mailboxes after the migration is complete.</span></span>

- <span data-ttu-id="0368b-156">**Groupes de sécurité et délégués** Le service de migration de messagerie ne peut pas détecter si les groupes Active Directory sur site sont des groupes de sécurité ou non, et donc ne peuvent pas mettre en service les groupes migrés en tant que groupes de sécurité dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0368b-156">**Security Groups and Delegates** The email migration service cannot detect whether on-premises Active Directory groups are security groups or not, so it cannot provision any migrated groups as security groups in Microsoft 365.</span></span> <span data-ttu-id="0368b-157">Si vous souhaitez avoir des groupes de sécurité dans votre client Microsoft 365, vous devez d’abord configurer un groupe de sécurité à extension messagerie vide dans votre client Microsoft 365 avant de commencer la migration à basculement.</span><span class="sxs-lookup"><span data-stu-id="0368b-157">If you want to have security groups in your Microsoft 365 tenant, you must first provision an empty mail-enabled security group in your Microsoft 365 tenant before starting the cutover migration.</span></span> <span data-ttu-id="0368b-158">En outre, cette méthode de migration déplace uniquement les boîtes aux lettres, les utilisateurs de messagerie, les contacts de messagerie et les groupes à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="0368b-158">Additionally, this migration method only moves mailboxes, mail users, mail contacts, and mail-enabled groups.</span></span> <span data-ttu-id="0368b-159">Si un autre objet Active Directory, tel qu’un utilisateur qui n’est pas migré vers Microsoft 365, est affecté en tant que gestionnaire ou délégué à un objet en cours de migration, il doit être supprimé de l’objet avant la migration.</span><span class="sxs-lookup"><span data-stu-id="0368b-159">If any other Active Directory object, such as user that is not migrated to Microsoft 365, is assigned as a manager or delegate to an object being migrated, they must be removed from the object before you migrate.</span></span>

### <a name="step-2-create-a-migration-endpoint"></a><span data-ttu-id="0368b-160">Étape 2 : Créez un point de terminaison de migration</span><span class="sxs-lookup"><span data-stu-id="0368b-160">Step 2: Create a migration endpoint</span></span>
<span data-ttu-id="0368b-161"><a name="BK_Step2"> </a></span><span class="sxs-lookup"><span data-stu-id="0368b-161"><a name="BK_Step2"> </a></span></span>

<span data-ttu-id="0368b-162">Pour migrer le courrier électronique correctement, Microsoft 365 doit se connecter au système de courrier source et communiquer avec celui-ci.</span><span class="sxs-lookup"><span data-stu-id="0368b-162">To migrate email successfully, Microsoft 365 needs to connect and communicate with the source email system.</span></span> <span data-ttu-id="0368b-163">Pour ce faire, Microsoft 365 utilise un point de terminaison de migration.</span><span class="sxs-lookup"><span data-stu-id="0368b-163">To do this, Microsoft 365 uses a migration endpoint.</span></span> <span data-ttu-id="0368b-164">Pour créer un point de terminaison de migration Outlook Anywhere, afin d'effectuer une migration à basculement, commencez par vous [connecter à Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=534121).</span><span class="sxs-lookup"><span data-stu-id="0368b-164">To create an Outlook Anywhere migration endpoint for cutover migration, first [connect to Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=534121).</span></span>

<span data-ttu-id="0368b-165">Pour la liste complète des commandes de migration, voir [Cmdlets de déplacement et de migration](https://go.microsoft.com/fwlink/p/?LinkId=534750).</span><span class="sxs-lookup"><span data-stu-id="0368b-165">For a full list of migration commands, see [Move and migration cmdlets](https://go.microsoft.com/fwlink/p/?LinkId=534750).</span></span>

<span data-ttu-id="0368b-166">Dans Exchange Online PowerShell, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0368b-166">Run the following commands in Exchange Online PowerShell:</span></span>

```powershell
$Credentials = Get-Credential
```

<span data-ttu-id="0368b-167">Cet exemple utilise la cmdlet [Test-MigrationServerAvailability](https://go.microsoft.com/fwlink/p/?LinkId=534752) pour obtenir et tester les paramètres de connexion au serveur Exchange local, puis utilise ces paramètres de connexion pour créer le point de terminaison de migration appelé « CutoverEndpoint ».</span><span class="sxs-lookup"><span data-stu-id="0368b-167">The example uses the [Test-MigrationServerAvailability](https://go.microsoft.com/fwlink/p/?LinkId=534752) cmdlet to obtain and test the connection settings to the on-premises Exchange server, and then uses those connection settings to create the migration endpoint called "CutoverEndpoint".</span></span>

```powershell
$TSMA = Test-MigrationServerAvailability -ExchangeOutlookAnywhere -Autodiscover -EmailAddress administrator@contoso.com -Credentials $credentials
```

```powershell
New-MigrationEndpoint -ExchangeOutlookAnywhere -Name CutoverEndpoint -ConnectionSettings $TSMA.ConnectionSettings
```

> [!NOTE]
> <span data-ttu-id="0368b-p117">La cmdlet **New-MigrationEndpoint** peut être utilisée pour spécifier une base de données pour le service à l'aide de l'option **-TargetDatabase**. Sinon, une base de données est affectée de manière aléatoire à partir du site Services ADFS (Active Directory Federation Services) 2.0 où se trouve la boîte aux lettres de gestion.</span><span class="sxs-lookup"><span data-stu-id="0368b-p117">The **New-MigrationEndpoint** cmdlet can be used to specify a database for the service to use by using the **-TargetDatabase** option. Otherwise a database is randomly assigned from the Active Directory Federation Services (AD FS) 2.0 site where the management mailbox is located.</span></span>

#### <a name="verify-it-worked"></a><span data-ttu-id="0368b-170">Vérifier que l’opération a fonctionné</span><span class="sxs-lookup"><span data-stu-id="0368b-170">Verify it worked</span></span>

<span data-ttu-id="0368b-171">Dans Exchange Online PowerShell, exécutez la commande suivante pour afficher des informations sur le point de terminaison de migration « CutoverEndpoint » :</span><span class="sxs-lookup"><span data-stu-id="0368b-171">In Exchange Online PowerShell, run the following command to display information about the "CutoverEndpoint" migration endpoint:</span></span>

```powershell
Get-MigrationEndpoint CutoverEndpoint | Format-List EndpointType,ExchangeServer,UseAutoDiscover,Max*

```

### <a name="step-3-create-the-cutover-migration-batch"></a><span data-ttu-id="0368b-172">Étape 3 : Créez le lot de migration à basculement</span><span class="sxs-lookup"><span data-stu-id="0368b-172">Step 3: Create the cutover migration batch</span></span>
<span data-ttu-id="0368b-173"><a name="BK_Step3"> </a></span><span class="sxs-lookup"><span data-stu-id="0368b-173"><a name="BK_Step3"> </a></span></span>

<span data-ttu-id="0368b-p118">La cmdlet **New-MigrationBatch** d'Exchange Online PowerShell permet de créer un lot pour une migration à basculement. Vous pouvez créer un lot de migration et démarrer automatiquement son traitement en incluant le paramètre _AutoStart_. Vous pouvez également créer un lot de migration, puis démarrer manuellement son traitement par la suite à l'aide de la cmdlet **Start-MigrationBatch**. Cet exemple de code crée un lot de migration appelé « CutoverBatch » et utilise le point de terminaison de migration créé à l'étape précédente.</span><span class="sxs-lookup"><span data-stu-id="0368b-p118">You can use the **New-MigrationBatch** cmdlet in Exchange Online PowerShell to create a migration batch for a cutover migration. You can create a migration batch and start it automatically by including the _AutoStart_ parameter. Alternatively, you can create the migration batch and then manually start it afterwards by using the **Start-MigrationBatch** cmdlet. This example creates a migration batch called "CutoverBatch" and uses the migration endpoint that was created in the previous step.</span></span>

```powershell
New-MigrationBatch -Name CutoverBatch -SourceEndpoint CutoverEndpoint -AutoStart
```

<span data-ttu-id="0368b-p119">Cet exemple de code crée également un lot de migration appelé « CutoverBatch » et utilise le point de terminaison de migration créé à l'étape précédente. Le paramètre  _AutoStart_ n'étant pas inclus, le traitement du lot de migration doit être lancé manuellement sur le tableau de bord de migration ou à l'aide de la cmdlet **Start-MigrationBatch**. Comme indiqué précédemment, il ne peut y avoir qu'un seul lot de migration à basculement à la fois.</span><span class="sxs-lookup"><span data-stu-id="0368b-p119">This example also creates a migration batch called "CutoverBatch" and uses the migration endpoint that was created in the previous step. Because the  _AutoStart_ parameter isn't included, the migration batch has to be manually started on the migration dashboard or by using **Start-MigrationBatch** cmdlet. As previously stated, only one cutover migration batch can exist at a time.</span></span>

```powershell
New-MigrationBatch -Name CutoverBatch -SourceEndpoint CutoverEndpoint
```

#### <a name="verify-it-worked"></a><span data-ttu-id="0368b-181">Vérifier que l’opération a fonctionné</span><span class="sxs-lookup"><span data-stu-id="0368b-181">Verify it worked</span></span>

<span data-ttu-id="0368b-182">Pour vérifier que vous avez créé un lot de migration pour une migration à basculement, exécutez la commande suivante dans Exchange Online PowerShell pour afficher des informations sur le nouveau lot de migration :</span><span class="sxs-lookup"><span data-stu-id="0368b-182">To verify that you've successfully created a migration batch for a cutover migration, run the following command in Exchange Online PowerShell to display information about the new migration batch:</span></span>

```powershell
Get-MigrationBatch | Format-List
```

### <a name="step-4-start-the-cutover-migration-batch"></a><span data-ttu-id="0368b-183">Étape 4 : Démarrez le lot de migration à basculement</span><span class="sxs-lookup"><span data-stu-id="0368b-183">Step 4: Start the cutover migration batch</span></span>
<span data-ttu-id="0368b-184"><a name="BK_Step4"> </a></span><span class="sxs-lookup"><span data-stu-id="0368b-184"><a name="BK_Step4"> </a></span></span>

<span data-ttu-id="0368b-p120">Pour lancer le lot de migration dans Exchange Online PowerShell, exécutez la commande suivante. Cela crée un lot de migration appelé « CutoverBatch ».</span><span class="sxs-lookup"><span data-stu-id="0368b-p120">To start the migration batch in Exchange Online PowerShell, run the following command. This will create a migration batch called "CutoverBatch".</span></span>

```powershell
Start-MigrationBatch -Identity CutoverBatch
```

#### <a name="verify-it-worked"></a><span data-ttu-id="0368b-187">Vérifier que l’opération a fonctionné</span><span class="sxs-lookup"><span data-stu-id="0368b-187">Verify it worked</span></span>

<span data-ttu-id="0368b-p121">Si le traitement d’un lot de migration a démarré, son état dans le tableau de bord de migration est Synchronisation. Pour vérifier que le traitement d’un lot de migration a commencé à l’aide d’Exchange Online PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0368b-p121">If a migration batch is successfully started, its status on the migration dashboard is specified as Syncing. To verify that you've successfully started a migration batch using Exchange Online PowerShell, run the following command:</span></span>

```powershell
Get-MigrationBatch -Identity CutoverBatch |  Format-List Status
```

### <a name="step-5-route-your-email-to-microsoft-365"></a><span data-ttu-id="0368b-190">Étape 5 : acheminer votre courrier électronique vers Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0368b-190">Step 5: Route your email to Microsoft 365</span></span>
<span data-ttu-id="0368b-191"><a name="BK_Step5"> </a></span><span class="sxs-lookup"><span data-stu-id="0368b-191"><a name="BK_Step5"> </a></span></span>

<span data-ttu-id="0368b-192">Les systèmes de messagerie utilisent un enregistrement DNS appelé enregistrement MX pour identifier l'emplacement de remise des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="0368b-192">Email systems use a DNS record called an MX record to figure out where to deliver emails.</span></span> <span data-ttu-id="0368b-193">Pendant le processus de migration de la messagerie, votre enregistrement MX pointe vers votre système de messagerie source.</span><span class="sxs-lookup"><span data-stu-id="0368b-193">During the email migration process, your MX record was pointing to your source email system.</span></span> <span data-ttu-id="0368b-194">Une fois la migration de la messagerie vers Microsoft 365 terminée, il est temps de faire pointer votre enregistrement MX sur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0368b-194">Now that the email migration to Microsoft 365 is complete, it's time to point your MX record at Microsoft 365.</span></span> <span data-ttu-id="0368b-195">Cela permet de s’assurer que le courrier électronique est remis à vos boîtes aux lettres Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0368b-195">This helps make sure that email is delivered to your Microsoft 365 mailboxes.</span></span> <span data-ttu-id="0368b-196">En déplaçant l'enregistrement MX, vous pouvez également désactiver votre ancien système de messagerie lorsque vous êtes prêt.</span><span class="sxs-lookup"><span data-stu-id="0368b-196">By moving the MX record, you can also you turn off your old email system when you're ready.</span></span>

<span data-ttu-id="0368b-197">Pour plusieurs fournisseurs DNS, il existe des instructions spécifiques pour modifier votre enregistrement MX.</span><span class="sxs-lookup"><span data-stu-id="0368b-197">For many DNS providers, there are specific instructions to change your MX record.</span></span> <span data-ttu-id="0368b-198">Si votre fournisseur DNS n’est pas inclus ou si vous souhaitez obtenir un sens général, les [instructions générales de l’enregistrement MX](https://support.office.microsoft.com/article/7b7b075d-79f9-4e37-8a9e-fb60c1d95166#bkmk_add_mx) sont également fournies.</span><span class="sxs-lookup"><span data-stu-id="0368b-198">If your DNS provider isn't included, or if you want to get a sense of the general directions, [general MX record instructions](https://support.office.microsoft.com/article/7b7b075d-79f9-4e37-8a9e-fb60c1d95166#bkmk_add_mx) are provided as well.</span></span>

<span data-ttu-id="0368b-p124">Il faut compter jusqu'à 72 heures pour que les systèmes de messagerie de vos clients et partenaires reconnaissent l'enregistrement MX modifié. Patientez au moins 72 heures avant de procéder à la tâche suivante : [Étape 6 : Supprimez le lot de migration à basculement](use-powershell-to-perform-a-cutover-migration-to-microsoft-365.md#Bk_step6).</span><span class="sxs-lookup"><span data-stu-id="0368b-p124">It can take up to 72 hours for the email systems of your customers and partners to recognize the changed MX record. Wait at least 72 hours before you proceed to the next task: [Step 6: Delete the cutover migration batch](use-powershell-to-perform-a-cutover-migration-to-microsoft-365.md#Bk_step6).</span></span>

### <a name="step-6-delete-the-cutover-migration-batch"></a><span data-ttu-id="0368b-201">Étape 6 : Supprimez le lot de migration à basculement</span><span class="sxs-lookup"><span data-stu-id="0368b-201">Step 6: Delete the cutover migration batch</span></span>
<span data-ttu-id="0368b-202"><a name="Bk_step6"> </a></span><span class="sxs-lookup"><span data-stu-id="0368b-202"><a name="Bk_step6"> </a></span></span>

<span data-ttu-id="0368b-203">Une fois que vous avez modifié l’enregistrement MX et vérifié que tous les messages sont acheminés vers les boîtes aux lettres Microsoft 365, informez-les aux utilisateurs que leur courrier va vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0368b-203">After you change the MX record and verify that all email is being routed to Microsoft 365 mailboxes, notify the users that their mail is going to Microsoft 365.</span></span> <span data-ttu-id="0368b-204">Après cela, vous pouvez supprimer le lot de migration à basculement.</span><span class="sxs-lookup"><span data-stu-id="0368b-204">After this, you can delete the cutover migration batch.</span></span> <span data-ttu-id="0368b-205">Avant de supprimer le lot de migration, vérifiez les points suivants.</span><span class="sxs-lookup"><span data-stu-id="0368b-205">Verify the following before you delete the migration batch.</span></span>

- <span data-ttu-id="0368b-206">Tous les utilisateurs utilisent des boîtes aux lettres Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0368b-206">All users are using Microsoft 365 mailboxes.</span></span> <span data-ttu-id="0368b-207">Après la suppression du lot, les messages envoyés à des boîtes aux lettres sur le serveur Exchange local ne sont pas copiés dans les boîtes aux lettres Microsoft 365 correspondantes.</span><span class="sxs-lookup"><span data-stu-id="0368b-207">After the batch is deleted, mail sent to mailboxes on the on-premises Exchange Server isn't copied to the corresponding Microsoft 365 mailboxes.</span></span>

- <span data-ttu-id="0368b-208">Les boîtes aux lettres Microsoft 365 ont été synchronisées au moins une fois après leur envoi direct par le courrier.</span><span class="sxs-lookup"><span data-stu-id="0368b-208">Microsoft 365 mailboxes were synchronized at least once after mail began being sent directly to them.</span></span> <span data-ttu-id="0368b-209">Pour ce faire, assurez-vous que la valeur de la zone heure de la dernière synchronisation du lot de migration est plus récente que celle de l’envoi de messages démarré directement aux boîtes aux lettres Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0368b-209">To do this, make sure that the value in the Last Synced Time box for the migration batch is more recent than when mail started being routed directly to Microsoft 365 mailboxes.</span></span>

<span data-ttu-id="0368b-210">Pour supprimer le lot de migration « CutoverBatch » dans Exchange Online PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0368b-210">To delete the "CutoverBatch" migration batch in Exchange Online PowerShell, run the following command:</span></span>

```powershell
Remove-MigrationBatch -Identity CutoverBatch
```

### <a name="section-7-assign-user-licenses"></a><span data-ttu-id="0368b-211">Section 7 : Attribuez des licences utilisateur</span><span class="sxs-lookup"><span data-stu-id="0368b-211">Section 7: Assign user licenses</span></span>
<span data-ttu-id="0368b-212"><a name="BK_Step7"> </a></span><span class="sxs-lookup"><span data-stu-id="0368b-212"><a name="BK_Step7"> </a></span></span>

 <span data-ttu-id="0368b-213">**Activez les comptes d’utilisateur Microsoft 365 pour les comptes migrés en affectant des licences.**</span><span class="sxs-lookup"><span data-stu-id="0368b-213">**Activate Microsoft 365 user accounts for the migrated accounts by assigning licenses.**</span></span> <span data-ttu-id="0368b-214">Si vous n'attribuez pas de licence, la boîte aux lettres est désactivée à la fin de la période de grâce (30 jours).</span><span class="sxs-lookup"><span data-stu-id="0368b-214">If you don't assign a license, the mailbox is disabled when the grace period ends (30 days).</span></span> <span data-ttu-id="0368b-215">Pour attribuer une licence dans le centre d’administration 365 de Microsoft, consultez la rubrique [attribuer ou](https://docs.microsoft.com/microsoft-365/admin/manage/assign-licenses-to-users)supprimer l’attribution des licences.</span><span class="sxs-lookup"><span data-stu-id="0368b-215">To assign a license in the Microsoft 365 admin center, see [Assign or unassign licenses](https://docs.microsoft.com/microsoft-365/admin/manage/assign-licenses-to-users).</span></span>

### <a name="step-8-complete-post-migration-tasks"></a><span data-ttu-id="0368b-216">Étape 8 : Exécutez les tâches post-migration</span><span class="sxs-lookup"><span data-stu-id="0368b-216">Step 8: Complete post-migration tasks</span></span>
<span data-ttu-id="0368b-217"><a name="BK_Step8"> </a></span><span class="sxs-lookup"><span data-stu-id="0368b-217"><a name="BK_Step8"> </a></span></span>

- <span data-ttu-id="0368b-218">**Créer un enregistrement DNS de Autodiscover afin que les utilisateurs puissent facilement accéder à leurs boîtes aux lettres**</span><span class="sxs-lookup"><span data-stu-id="0368b-218">**Create an Autodiscover DNS record so users can easily get to their mailboxes.**</span></span> <span data-ttu-id="0368b-219">Une fois que toutes les boîtes aux lettres locales sont migrées vers Microsoft 365, vous pouvez configurer un enregistrement DNS de découverte automatique pour votre organisation Microsoft 365 afin de permettre aux utilisateurs de se connecter facilement à leurs nouvelles boîtes aux lettres Microsoft 365 avec Outlook et les clients mobiles.</span><span class="sxs-lookup"><span data-stu-id="0368b-219">After all on-premises mailboxes are migrated to Microsoft 365, you can configure an Autodiscover DNS record for your Microsoft 365 organization to enable users to easily connect to their new Microsoft 365 mailboxes with Outlook and mobile clients.</span></span> <span data-ttu-id="0368b-220">Ce nouvel enregistrement DNS de découverte automatique doit utiliser le même espace de noms que celui que vous utilisez pour votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0368b-220">This new Autodiscover DNS record has to use the same namespace that you're using for your Microsoft 365 organization.</span></span> <span data-ttu-id="0368b-221">Par exemple, si votre espace de noms en nuage est nuage.contoso.com, l’enregistrement DNS de découverte automatique que vous devez créer est decouverteautomatique.nuage.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="0368b-221">For example, if your cloud-based namespace is cloud.contoso.com, the Autodiscover DNS record you need to create is autodiscover.cloud.contoso.com.</span></span>

    <span data-ttu-id="0368b-222">Si vous conservez votre serveur Exchange, vous devez également vous assurer que l’enregistrement CNAMe DNS de découverte automatique doit pointer vers Microsoft 365 dans le DNS interne et externe après la migration afin que le client Outlook se connecte à la boîte aux lettres appropriée.</span><span class="sxs-lookup"><span data-stu-id="0368b-222">If you keep your Exchange Server, you should also make sure that Autodiscover DNS CNAME record has to point to Microsoft 365 in both internal and external DNS after the migration so that the Outlook client will to connect to the correct mailbox.</span></span>

    > [!NOTE]
    >  <span data-ttu-id="0368b-223">Dans Exchange 2007, Exchange 2010 et Exchange 2013, vous devez également définir  `Set-ClientAccessServer AutodiscoverInternalConnectionURI` sur `Null`.</span><span class="sxs-lookup"><span data-stu-id="0368b-223">In Exchange 2007, Exchange 2010, and Exchange 2013 you should also set `Set-ClientAccessServer AutodiscoverInternalConnectionURI` to `Null`.</span></span>

    <span data-ttu-id="0368b-224">Microsoft 365 utilise un enregistrement CNAMe pour implémenter le service de découverte automatique pour les clients Outlook et mobiles.</span><span class="sxs-lookup"><span data-stu-id="0368b-224">Microsoft 365 uses a CNAME record to implement the Autodiscover service for Outlook and mobile clients.</span></span> <span data-ttu-id="0368b-225">L'enregistrement CNAME de découverte automatique doit contenir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0368b-225">The Autodiscover CNAME record must contain the following information:</span></span>

  - <span data-ttu-id="0368b-226">**Alias :** autodiscover</span><span class="sxs-lookup"><span data-stu-id="0368b-226">**Alias:** autodiscover</span></span>

  - <span data-ttu-id="0368b-227">**Cible :** autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="0368b-227">**Target:** autodiscover.outlook.com</span></span>

    <span data-ttu-id="0368b-228">Pour plus d’informations, reportez-vous [à la rubrique ajouter des enregistrements DNS pour connecter votre domaine](https://go.microsoft.com/fwlink/p/?LinkId=535028).</span><span class="sxs-lookup"><span data-stu-id="0368b-228">For more information, see [Add DNS records to connect your domain](https://go.microsoft.com/fwlink/p/?LinkId=535028).</span></span>

- <span data-ttu-id="0368b-229">**Désactivez des serveurs Exchange locaux.**</span><span class="sxs-lookup"><span data-stu-id="0368b-229">**Decommission on-premises Exchange servers.**</span></span> <span data-ttu-id="0368b-230">Une fois que vous avez vérifié que tous les courriers électroniques sont acheminés directement vers les boîtes aux lettres Microsoft 365, et que vous n’avez plus besoin de conserver votre organisation de messagerie locale ou si vous ne prévoyez pas d’implémenter une solution d’authentification unique (SSO), vous pouvez désinstaller Exchange de vos serveurs et supprimer votre organisation Exchange locale.</span><span class="sxs-lookup"><span data-stu-id="0368b-230">After you've verified that all email is being routed directly to the Microsoft 365 mailboxes, and you no longer need to maintain your on-premises email organization or don't plan on implementing a single sign-on (SSO) solution, you can uninstall Exchange from your servers and remove your on-premises Exchange organization.</span></span>

    <span data-ttu-id="0368b-231">Pour plus d’informations, voir les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0368b-231">For more information, see the following:</span></span>

  - [<span data-ttu-id="0368b-232">Modifier ou supprimer Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="0368b-232">Modify or Remove Exchange 2010</span></span>](https://go.microsoft.com/fwlink/?LinkId=217936)

  - [<span data-ttu-id="0368b-233">Procédure de suppression d'une organisation Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="0368b-233">How to Remove an Exchange 2007 Organization</span></span>](https://go.microsoft.com/fwlink/?LinkID=100485)

  - [<span data-ttu-id="0368b-234">Procédure de désinstallation d'Exchange Server 2003</span><span class="sxs-lookup"><span data-stu-id="0368b-234">How to Uninstall Exchange Server 2003</span></span>](https://go.microsoft.com/fwlink/?LinkID=56561)


