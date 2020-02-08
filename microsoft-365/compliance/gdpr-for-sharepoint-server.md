---
title: RGPD pour SharePoint Server
description: Découvrez comment satisfaire aux exigences du RGPD dans un environnement SharePoint Server local.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.openlocfilehash: 6cbcb7f0918d472d953cb0f837adcb23b642a3a3
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41596391"
---
# <a name="gdpr-for-sharepoint-server"></a><span data-ttu-id="5c084-103">RGPD pour SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="5c084-103">GDPR for SharePoint Server</span></span>

<span data-ttu-id="5c084-104">S’applique à :</span><span class="sxs-lookup"><span data-stu-id="5c084-104">Applies to:</span></span>
- <span data-ttu-id="5c084-105">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c084-105">SharePoint Server 2013</span></span>
- <span data-ttu-id="5c084-106">SharePoint Server 2016</span><span class="sxs-lookup"><span data-stu-id="5c084-106">SharePoint Server 2016</span></span>
- <span data-ttu-id="5c084-107">SharePoint Server 2019</span><span class="sxs-lookup"><span data-stu-id="5c084-107">SharePoint Server 2019</span></span>

<span data-ttu-id="5c084-108">Dans le cadre de la protection des informations personnelles, nous vous recommandons d’effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="5c084-108">As part of safeguarding personal information, we recommend the following:</span></span>

-   <span data-ttu-id="5c084-109">Classer vos données à l’aide d’Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="5c084-109">Classify your data, using Azure Information Protection.</span></span>

-   <span data-ttu-id="5c084-p101">Exécuter SharePoint Server dans une configuration avec des privilèges minimaux. Pour plus d’informations, reportez-vous à l’article relatif à la [planification d’une administration avec des privilèges minimaux dans SharePoint Server](https://docs.microsoft.com/SharePoint/security-for-sharepoint-server/plan-for-least-privileged-administration) et à l’article [Sécurité pour SharePoint Server](https://docs.microsoft.com/sharepoint/security-for-sharepoint-server/security-for-sharepoint-server).</span><span class="sxs-lookup"><span data-stu-id="5c084-p101">Run SharePoint Server in a least-privileged configuration. See [Plan for least-privileged administration in SharePoint Server](https://docs.microsoft.com/SharePoint/security-for-sharepoint-server/plan-for-least-privileged-administration) and [Security for SharePoint Server](https://docs.microsoft.com/sharepoint/security-for-sharepoint-server/security-for-sharepoint-server) for more information.</span></span>

-   <span data-ttu-id="5c084-112">[Activer le chiffrement BitLocker sur vos serveurs](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server).</span><span class="sxs-lookup"><span data-stu-id="5c084-112">[Enable BitLocker encryption on your servers](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server).</span></span>

## <a name="user-generated-content"></a><span data-ttu-id="5c084-113">Contenu généré par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="5c084-113">User Generated content</span></span>

<span data-ttu-id="5c084-114">Voici l’approche à adopter concernant le contenu généré par l’utilisateur dans les bibliothèques et les sites SharePoint Server :</span><span class="sxs-lookup"><span data-stu-id="5c084-114">The basic recommended approach for user generated content contained in SharePoint Server sites and libraries is:</span></span>

-   <span data-ttu-id="5c084-115">Attribuez des étiquettes aux données sensibles à l’aide d’Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="5c084-115">Use Azure Information Protection to label sensitive data.</span></span>

-   <span data-ttu-id="5c084-116">Récupérez les données sensibles à l’aide des fonctions de [recherche SharePoint Server](https://docs.microsoft.com/SharePoint/search/search) et [eDiscovery](https://docs.microsoft.com/SharePoint/governance/ediscovery-and-in-place-holds-in-sharepoint-server).</span><span class="sxs-lookup"><span data-stu-id="5c084-116">Use [SharePoint Server search](https://docs.microsoft.com/SharePoint/search/search) and [eDiscovery](https://docs.microsoft.com/SharePoint/governance/ediscovery-and-in-place-holds-in-sharepoint-server) to retrieve sensitive data.</span></span>

<span data-ttu-id="5c084-117">Voici la procédure recommandée à suivre concernant les partages de fichiers, ainsi que les bibliothèques et les sites SharePoint :</span><span class="sxs-lookup"><span data-stu-id="5c084-117">The recommended approach for files shares and SharePoint sites and libraries includes these steps:</span></span>

1.  <span data-ttu-id="5c084-118">**[Installez et configurez le scanneur Azure Information Protection.](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-install#options-to-install-the-azure-information-protection-client-for-users)**</span><span class="sxs-lookup"><span data-stu-id="5c084-118">**[Install and configure Azure Information Protection scanner.](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-install#options-to-install-the-azure-information-protection-client-for-users)**</span></span>

    -   <span data-ttu-id="5c084-119">Déterminez les types de données sensibles à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5c084-119">Decide which sensitive data types to use.</span></span>

    -   <span data-ttu-id="5c084-120">Spécifiez les sites SharePoint à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5c084-120">Specify which SharePoint sites to use.</span></span>

2.  <span data-ttu-id="5c084-121">**Effectuez un cycle de détection.**</span><span class="sxs-lookup"><span data-stu-id="5c084-121">**Complete a discovery cycle.**</span></span>

    -   <span data-ttu-id="5c084-122">Exécutez le scanneur en mode de détection et validez les résultats.</span><span class="sxs-lookup"><span data-stu-id="5c084-122">Run the scanner in discovery mode and validate the findings.</span></span>

    -   <span data-ttu-id="5c084-123">Si nécessaire, optimisez les conditions et les types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="5c084-123">If needed, optimize the conditions and sensitive information types.</span></span>

    -   <span data-ttu-id="5c084-124">Évaluez l’incidence que peut avoir l’application automatique d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="5c084-124">Assess the expected impact of automatically applying labels.</span></span>

3.  <span data-ttu-id="5c084-125">**Exécutez le scanneur Azure Information Protection pour appliquer des étiquettes aux documents correspondants**.</span><span class="sxs-lookup"><span data-stu-id="5c084-125">**Run the Azure Information Protection scanner to apply labels to qualifying documents**.</span></span>

4.  <span data-ttu-id="5c084-126">**Pour une meilleure protection :**</span><span class="sxs-lookup"><span data-stu-id="5c084-126">**For protection:**</span></span>

    <span data-ttu-id="5c084-p102">a. configurez des règles de protection contre la perte de données Exchange pour protéger les documents avec l’étiquette souhaitée.</span><span class="sxs-lookup"><span data-stu-id="5c084-p102">a.  Configure Exchange data loss prevention rules to protect documents with the desired label.</span></span>

    <span data-ttu-id="5c084-p103">b. veillez à déterminer des autorisations pour limiter les personnes pouvant accéder aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="5c084-p103">b.  Be sure permissions to limit who can access files.</span></span>

    <span data-ttu-id="5c084-p104">c. pour SharePoint, utilisez la protection IRM pour les bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="5c084-p104">c.  For SharePoint, use IRM-protection for libraries.</span></span>

5.  <span data-ttu-id="5c084-133">**Pour la surveillance, intégrez un outil SIEM aux journaux Windows Server.**</span><span class="sxs-lookup"><span data-stu-id="5c084-133">**For monitoring, integrate Windows Server logs with a SIEM tool.**</span></span>

    <span data-ttu-id="5c084-p105">a. Pour rechercher des données personnelles pour les demandes d’objet de données, utilisez le Centre de recherche ou eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="5c084-p105">a.  To find personal data for data subject requests, use Search Center or eDiscovery.</span></span>

<span data-ttu-id="5c084-p106">Lorsque vous appliquez des étiquettes à des données sensibles, veillez à utiliser des étiquettes qui ne sont pas configurées avec un système de protection. La protection inclut le chiffrement, qui empêche les services de détecter les données sensibles dans les fichiers.</span><span class="sxs-lookup"><span data-stu-id="5c084-p106">When applying labels to sensitive data, be sure to use a label that is not configured with protection. Protection includes encryption which prevents services from detecting sensitive data in the files.</span></span>

<span data-ttu-id="5c084-138">Pour plus d’informations sur l’utilisation du scanneur Azure Information Protection pour la recherche et l’étiquetage des données personnelles, reportez-vous au [Kit de détection de données du RGPD Microsoft à l’adresse](https://aka.ms/gdprpartners) (https://aka.ms/gdprpartners)).</span><span class="sxs-lookup"><span data-stu-id="5c084-138">For more information on using Azure Information Protection scanner to find and label personal data, see the [Microsoft GDPR Data Discovery Toolkit](https://aka.ms/gdprpartners) (https://aka.ms/gdprpartners).</span></span>

<span data-ttu-id="5c084-p107">Pour plus d’informations sur la configuration du scanneur pour diverses conditions et sur l’utilisation des types d’informations sensibles Office 365 dans le cadre de la protection contre la perte de données, reportez-vous à l’article [Comment configurer des conditions pour la classification automatique et recommandée pour Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-classification). Notez que les nouveaux types d’informations sensibles Office 365 ne pourront pas immédiatement être utilisés avec le scanneur et que les types d’informations sensibles personnalisés ne peuvent pas être utilisés avec le scanneur.</span><span class="sxs-lookup"><span data-stu-id="5c084-p107">For information on configuring the scanner for conditions and using the Office 365 data loss prevention (DLP) sensitive information types, see [How to configure conditions for automatic and recommended classification for Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-classification). Note that new Office 365 sensitive information types will not be immediately available to use with the scanner and custom sensitive information types cannot be used with the scanner.</span></span>

## <a name="removing-personal-information-from-office-files"></a><span data-ttu-id="5c084-141">Suppression d’informations personnelles à partir de fichiers Office</span><span class="sxs-lookup"><span data-stu-id="5c084-141">Removing personal information from Office files</span></span>

<span data-ttu-id="5c084-p108">La suppression d’informations personnelles (par exemple, des métadonnées ou des commentaires dans un document Word) à partir de fichiers Office stockés dans une bibliothèque de documents SharePoint doit être effectuée manuellement. Procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5c084-p108">Removing personal information (such as metadata or comments in a Word document) from Office files that are stored in a SharePoint document library must be done manually. Follow these steps:</span></span>

1.  <span data-ttu-id="5c084-144">Téléchargez une copie du document à partir de SharePoint Server sur votre disque local.</span><span class="sxs-lookup"><span data-stu-id="5c084-144">Download a copy of the document from SharePoint Server to your local disk.</span></span>

2.  <span data-ttu-id="5c084-145">Supprimez le document de la bibliothèque de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5c084-145">Delete the document from the SharePoint document library.</span></span>

3.  <span data-ttu-id="5c084-146">Suivez la procédure indiquée dans l’article [Supprimer des données masquées et des informations personnelles en inspectant des documents](https://support.office.com/article/356B7B5D-77AF-44FE-A07F-9AA4D085966F).</span><span class="sxs-lookup"><span data-stu-id="5c084-146">Follow the steps in [Remove hidden data and personal information by inspecting documents](https://support.office.com/article/356B7B5D-77AF-44FE-A07F-9AA4D085966F).</span></span>

4.  <span data-ttu-id="5c084-147">Téléchargez de nouveau le document vers la bibliothèque de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5c084-147">Upload the document back to the SharePoint document library.</span></span>

## <a name="telemetry-and-log-files"></a><span data-ttu-id="5c084-148">Télémétrie et fichiers journaux</span><span class="sxs-lookup"><span data-stu-id="5c084-148">Telemetry and log files</span></span>

### <a name="uls-logs"></a><span data-ttu-id="5c084-149">Journaux ULS</span><span class="sxs-lookup"><span data-stu-id="5c084-149">ULS Logs</span></span>

<span data-ttu-id="5c084-p109">Les journaux du service ULS (Unified Logging Service) et les journaux d’utilisation dans SharePoint Server permettent d’effectuer le suivi de différentes fonctions système et peuvent contenir des informations sur l’utilisateur. Les journaux ULS et les journaux d’utilisation sont des fichiers texte et peuvent être recherchés à l’aide d’un large éventail d’outils. La [cmdlet PowerShell Merge-SPLogFile](https://docs.microsoft.com/powershell/module/sharepoint-server/merge-splogfile) fournit un moyen de renvoyer des enregistrements à partir des journaux ULS sur plusieurs serveurs dans une batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="5c084-p109">Unified Logging Service (ULS) and Usage logging in SharePoint Server track a variety of system functions and can contain user information. ULS logs and usage logs are text files and can be searched using a variety of searching tools. The [Merge-SPLogFile PowerShell cmdlet](https://docs.microsoft.com/powershell/module/sharepoint-server/merge-splogfile) provides a way to return records from the ULS logs on multiple servers in a farm.</span></span>

<span data-ttu-id="5c084-p110">Pensez à définir les stratégies de rétention des journaux sur la valeur minimale nécessaire selon vos besoins. Pour plus d’informations sur la configuration de la journalisation dans SharePoint Server, reportez-vous à l’article [Configurer la journalisation des diagnostics dans SharePoint Server](https://docs.microsoft.com/SharePoint/administration/configure-diagnostic-logging).</span><span class="sxs-lookup"><span data-stu-id="5c084-p110">Consider setting log retention policies to the minimum value needed for your business purposes. For information about configuring logging in SharePoint Server, see [Configure diagnostic logging in SharePoint Server](https://docs.microsoft.com/SharePoint/administration/configure-diagnostic-logging).</span></span>

<span data-ttu-id="5c084-155">Notez que certains événements système sont également enregistrés pour le journal des événements Windows.</span><span class="sxs-lookup"><span data-stu-id="5c084-155">Note that some system events are also logged to the Windows Event Log.</span></span>

### <a name="usage-database"></a><span data-ttu-id="5c084-156">Base de données d’utilisation</span><span class="sxs-lookup"><span data-stu-id="5c084-156">Usage Database</span></span>

<span data-ttu-id="5c084-p111">La base de données d’utilisation de SharePoint Server (nom par défaut : WSS_Logging) contient un sous-ensemble des informations figurant dans les journaux ULS. La durée maximale de rétention des données dans cette base de données est de 30 jours. Nous vous recommandons de la configurer sur la durée la plus courte possible en fonction de vos besoins. Pour plus d’informations, reportez-vous à l’article [Configurer la journalisation des diagnostics dans SharePoint Server](https://docs.microsoft.com/SharePoint/administration/configure-diagnostic-logging).</span><span class="sxs-lookup"><span data-stu-id="5c084-p111">The SharePoint Server Usage database (default name WSS_Logging) contains a subset of the information found in the ULS logs. The maximum retention of data in this database is 30 days. We recommend that you configure it for the shortest duration allowable by your business needs. For more information, see [Configure diagnostic logging in SharePoint Server](https://docs.microsoft.com/SharePoint/administration/configure-diagnostic-logging).</span></span>

## <a name="personal-information-and-search"></a><span data-ttu-id="5c084-161">Informations personnelles et recherche</span><span class="sxs-lookup"><span data-stu-id="5c084-161">Personal information and search</span></span>

<span data-ttu-id="5c084-162">Les enregistrements d’utilisation et l’historique des requêtes de recherche contiennent des références à des noms d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5c084-162">The search query history and usage records contain references to user names.</span></span>

### <a name="query-history-and-favorite-queries"></a><span data-ttu-id="5c084-163">Historique de requêtes et requêtes favorites</span><span class="sxs-lookup"><span data-stu-id="5c084-163">Query history and favorite queries</span></span>

<span data-ttu-id="5c084-p112">Dans SharePoint Server, les historiques de requête et les requêtes marquées comme « Favori » expirent automatiquement au bout de 365 jours. Si un utilisateur quitte votre organisation, vous pouvez supprimer les références à son nom d’utilisateur à partir de l’historique de requêtes en suivant la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5c084-p112">In SharePoint Server, query histories and ‘favorite’ queries automatically expire after 365 days. If a user leaves your organization, it is possible to remove references to a user's name from the query history using the steps below.</span></span>

<span data-ttu-id="5c084-166">Les requêtes SQL suivantes s’appliquent à SharePoint Server, et permettent d’effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="5c084-166">The following SQL queries apply to SharePoint Server and make it possible to:</span></span>

-   <span data-ttu-id="5c084-167">Exporter l’historique de requêtes et les requêtes favorites d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="5c084-167">Export a user’s query history or favorite queries</span></span>

-   <span data-ttu-id="5c084-168">Supprimer les références à des noms d’utilisateur dans l’historique de requêtes</span><span class="sxs-lookup"><span data-stu-id="5c084-168">Remove references to user names in the query history</span></span>

#### <a name="export-a-users-queries-since-a-specific-date"></a><span data-ttu-id="5c084-169">Exporter les requêtes d’un utilisateur depuis une date spécifique</span><span class="sxs-lookup"><span data-stu-id="5c084-169">Export a user’s queries since a specific date</span></span> 

<span data-ttu-id="5c084-170">La procédure suivante permet d’exporter des requêtes à partir des tables de journaux de requêtes Link Store effectuées par @UserName depuis @StartTime.</span><span class="sxs-lookup"><span data-stu-id="5c084-170">Use the following procedure to export queries from the Link Store query log tables, performed by @UserName since @StartTime.</span></span>

```sql
[In dbo].[LinkStore_<ID>]:
CREATE PROCEDURE proc_MSS_GetQueryTermsForUser 
( 
    @UserName nvarchar(256), 
    @StartTime datetime 
) 
AS 
BEGIN 
    SET NOCOUNT ON; 
    SELECT searchTime, queryString 
    FROM 
        dbo.MSSQLogPageImpressionQuery 
    WITH 
        (NOLOCK) 
    WHERE 
        userName = @UserName AND 
        searchTime > @StartTime 
END 
GO 
```

#### <a name="export-a-users-queries-from-the-past-100-days"></a><span data-ttu-id="5c084-171">Exporter les requêtes d’un utilisateur émises au cours des 100 derniers jours</span><span class="sxs-lookup"><span data-stu-id="5c084-171">Export a user’s queries from the past 100 days</span></span>

```sql
DECLARE @FROMDATE datetime 
SET @FROMDATE = DATEADD(day, -100, GETUTCDATE()) 
EXECUTE proc_MSS_GetQueryTermsForUser '0#.w|domain\username', @FROMDATE 
```

#### <a name="export-a-users-favorite-queries"></a><span data-ttu-id="5c084-172">Exporter les requêtes favorites d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="5c084-172">Export a user’s favorite queries</span></span>

<span data-ttu-id="5c084-173">Suivez la procédure ci-dessous pour exporter les requêtes favorites d’un utilisateur à partir des tables de résultats personnels de la base de données d’administration de recherche, effectuées par @UserName, depuis <DateTime>.</span><span class="sxs-lookup"><span data-stu-id="5c084-173">Use the following procedure to export a user's favorite queries from the Search Admin DB personal result tables, performed by @UserName, since <DateTime>.</span></span>

```sql
In [dbo].[Search_<ID>]:
CREATE PROCEDURE proc_MSS_GetPersonalFavoriteQueries 
( 
    @UserName nvarchar(256), 
    @SearchTime datetime 
) 
AS 
BEGIN 
    SET NOCOUNT ON; 
    SELECT max(queries.SearchTime) as SearchTime, 
           max(queries.querystring) as queryString, 
           max(url.url) as URL 
    FROM MSSQLogOwner owners WITH(NOLOCK) 
    JOIN MSSQLogPersonalResults results WITH(NOLOCK) on owners.OwnerId = results.OwnerId 
    JOIN MSSQLogUrl url WITH(NOLOCK) on results.ClickedUrlId = url.urlId 
    JOIN MSSQLogPersonalQueries queries WITH(NOLOCK) on results.OwnerId = queries.OwnerId 
    WHERE queries.SearchTime > @SearchTime 
        AND queries.UserName = @UserName 
        GROUP BY queries.QueryString,url.url 
END 
GO 
```

#### <a name="export-a-users-favorite-queries-from-the-past-100-days"></a><span data-ttu-id="5c084-174">Exporter les requêtes favorites d’un utilisateur émises au cours des 100 derniers jours</span><span class="sxs-lookup"><span data-stu-id="5c084-174">Export a user’s favorite queries from the past 100 days</span></span> 

```sql
DECLARE @FROMDATE datetime 
SET @FROMDATE = DATEADD(day, -100, GETUTCDATE()) 
EXECUTE proc_MSS_GetPersonalFavoriteQueries '0#.w|domain\username', @FROMDATE 
```

#### <a name="remove-references-to-user-names-that-are-more-than-x-days-old"></a><span data-ttu-id="5c084-175">Supprimer les références aux noms d’utilisateur qui datent de plus de X jours</span><span class="sxs-lookup"><span data-stu-id="5c084-175">Remove references to user names that are more than X days old</span></span>

<span data-ttu-id="5c084-p113">Procédez comme indiqué ci-dessous pour supprimer les références à *tous* les noms d’utilisateur qui datent de plus de @Days à partir des tables de journaux de requêtes Link Store. La procédure supprime uniquement les références antérieures jusqu’à l’heure du dernier nettoyage @LastCleanupTime.</span><span class="sxs-lookup"><span data-stu-id="5c084-p113">Use the following procedure to remove references to *all* user names that are more than @Days old, from the Links Store query log tables. The procedure only removes references backwards in time until it reaches the @LastCleanupTime.</span></span>

```sql
In [dbo].[LinksStore_<ID>]:  
CREATE PROCEDURE proc_MSS_QLog_Cleanup_Users 
( 
    @LastCleanupTime datetime, 
    @Days int 
) 
AS 
BEGIN 
    DECLARE @TooOld datetime 
    SET @TooOld = DATEADD(day, -@Days, GETUTCDATE()) 
    DECLARE @FromLast datetime 
    SET @FromLast = DATEADD(day, -@Days, @LastCleanupTime) 
    BEGIN TRANSACTION 
         UPDATE MSSQLogPageImpressionQuery 
    SET userName = 'NA' 
    WHERE @FromLast <= searchTime AND searchTime < @TooOld 
    UPDATE MSSQLogO14PageClick 
    SET userName = 'NA' 
    WHERE @FromLast <= searchTime AND searchTime < @TooOld 
    COMMIT TRANSACTION 
END 
GO 
```

#### <a name="remove-references-to-a-specific-user-name-thats-more-than-x-days-old"></a><span data-ttu-id="5c084-178">Supprimer les références à un nom d’utilisateur spécifique qui date de plus de X jours</span><span class="sxs-lookup"><span data-stu-id="5c084-178">Remove references to a specific user name that’s more than X days old</span></span>

<span data-ttu-id="5c084-p114">Procédez comme indiqué ci-dessous pour supprimer les références à un nom d’utilisateur *spécifique* des tables de journaux de requêtes Link Store, où les références datent de plus de @Days. La procédure supprime uniquement les références antérieures jusqu’à l’heure du dernier nettoyage @LastCleanupTime.</span><span class="sxs-lookup"><span data-stu-id="5c084-p114">Use the following procedure to remove references to a *specific* user name from the Links Store query log tables, where the references are more than @Days old. The procedure only removes references backwards in time until it reaches the @LastCleanupTime.</span></span>

```sql
In [dbo].[LinksStore_<ID>]:
CREATE PROCEDURE proc_MSS_QLog_Cleanup_Users 
( 
    @UserName nvarchar(256),
    @LastCleanupTime datetime, 
    @Days int 
) 
AS 
BEGIN 
    DECLARE @TooOld datetime 
    SET @TooOld = DATEADD(day, -@Days, GETUTCDATE()) 
    DECLARE @FromLast datetime 
    SET @FromLast = DATEADD(day, -@Days, @LastCleanupTime) 
    BEGIN TRANSACTION 
         UPDATE MSSQLogPageImpressionQuery 
    SET userName = 'NA' 
    WHERE @FromLast <= searchTime AND searchTime < @TooOld AND userName = @UserName
    UPDATE MSSQLogO14PageClick 
    SET userName = 'NA' 
    WHERE @FromLast <= searchTime AND searchTime < @TooOld AND userName = @UserName
    COMMIT TRANSACTION 
END 
GO 
```

#### <a name="remove-references-to-all-user-names-in-the-query-history-from-a-date-and-up-to-the-past-30-days"></a><span data-ttu-id="5c084-181">Supprimer les références à tous les noms d’utilisateur dans l’historique de requêtes entre une date spécifique et jusqu’aux 30 derniers jours</span><span class="sxs-lookup"><span data-stu-id="5c084-181">Remove references to all user names in the query history from a date and up to the past 30 days</span></span>

```sql
EXECUTE proc_MSS_QLog_Cleanup_Users '1-1-2017', 30 
```

### <a name="delete-usage-records"></a><span data-ttu-id="5c084-182">Supprimer les enregistrements d’utilisation</span><span class="sxs-lookup"><span data-stu-id="5c084-182">Delete usage records</span></span>

<span data-ttu-id="5c084-p115">SharePoint Server supprime automatiquement les enregistrements d’utilisation au bout de 3 ans. Vous pouvez supprimer manuellement ces enregistrements à l’aide de la procédure ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="5c084-p115">SharePoint Server automatically deletes usage records after 3 years. You can manually delete such records using the procedure below:</span></span>

<span data-ttu-id="5c084-185">Pour supprimer tous les enregistrements d’utilisation associés à des documents supprimés, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5c084-185">To delete all usage records associated with deleted documents:</span></span> 

1.  <span data-ttu-id="5c084-186">Assurez-vous que la dernière mise à jour de SharePoint est installée.</span><span class="sxs-lookup"><span data-stu-id="5c084-186">Ensure that you have the latest SharePoint update installed.</span></span> 

2.  <span data-ttu-id="5c084-187">Démarrez SharePoint Management Shell.</span><span class="sxs-lookup"><span data-stu-id="5c084-187">Start a SharePoint Management shell.</span></span>

3.  <span data-ttu-id="5c084-188">Arrêtez et effacez l’analyse de l’utilisation :</span><span class="sxs-lookup"><span data-stu-id="5c084-188">Stop and Clear the Usage Analytics analysis:</span></span> 

    ```powershell
    $tj = Get-SPTimerJob -Type Microsoft.Office.Server.Search.Analytics.UsageAnalyticsJobDefinition 
    $tj.DisableTimerjobSchedule()
    $tj.StopAnalysis() 
    $tj.ClearAnalysis() 
    $tj.EnableTimerjobSchedule()
    ```

4.  <span data-ttu-id="5c084-189">Attendez que l’analyse recommence (cela peut prendre jusqu’à 24 heures).</span><span class="sxs-lookup"><span data-stu-id="5c084-189">Wait for the analysis to start again (might take up to 24 hours).</span></span> 

5.  <span data-ttu-id="5c084-p116">Lors de la prochaine exécution de l’analyse, tous les enregistrements seront vidés de la base de données de création de rapports d’analyse. Ce vidage complet peut prendre du temps pour une base de données volumineuse avec de nombreuses entrées.</span><span class="sxs-lookup"><span data-stu-id="5c084-p116">On the next run of the analysis, it will dump all records from the Analytics Reporting database. This full dump may take a while for a large database with many entries.</span></span>

6.  <span data-ttu-id="5c084-p117">Attendez 10 jours. L’analyse s’exécute tous les jours. Les enregistrements associés à des documents supprimés sont supprimés au bout de la dixième exécution. Cette dernière peut prendre plus de temps que les autres, si les enregistrements à supprimer sont nombreux.</span><span class="sxs-lookup"><span data-stu-id="5c084-p117">Wait for 10 days. The analysis runs daily, and records associated with deleted documents will be removed after the 10^th^ run. This run may take longer than normal if many records need to be deleted.</span></span> 

### <a name="personal-information-and-search-in-sharepoint-server-2010"></a><span data-ttu-id="5c084-195">Informations personnelles et recherche dans SharePoint Server 2010</span><span class="sxs-lookup"><span data-stu-id="5c084-195">Personal information and search in SharePoint Server 2010</span></span>

#### <a name="fast-search-server-2010-for-sharepoint"></a><span data-ttu-id="5c084-196">FAST Search Server 2010 for SharePoint</span><span class="sxs-lookup"><span data-stu-id="5c084-196">FAST Search Server 2010 for SharePoint</span></span> 

<span data-ttu-id="5c084-p118">En plus de stocker des fichiers dans l’index, le module complémentaire FAST Search Server 2010 stocke également les fichiers au format intermédiaire FixML. Les fichiers FiXML sont régulièrement compactés, par défaut entre 3 h 00 et 5 h 00 toutes les nuits. Le compactage élimine automatiquement les fichiers supprimés des fichiers FiXML. Pour que les informations appartenant à des utilisateurs ou des documents supprimés soient supprimées au bon moment, veillez à ce que le compactage soit toujours activé.</span><span class="sxs-lookup"><span data-stu-id="5c084-p118">In addition to storing files in the index, the FAST Search Server 2010 Add-On also stores files in an intermediate format called FixML. FiXML files are compacted regularly, by default between 3 am and 5 am every night. Compaction removes deleted files from the FiXML files automatically. To ensure timely removal of information belonging to deleted users or documents, ensure that compaction is always enabled.</span></span>

### <a name="hybrid-search"></a><span data-ttu-id="5c084-201">Recherche hybride</span><span class="sxs-lookup"><span data-stu-id="5c084-201">Hybrid Search</span></span> 

<span data-ttu-id="5c084-p119">Les actions recommandées pour les solutions de recherche hybride sont les mêmes que pour la recherche dans SharePoint Server ou SharePoint Online. Il existe deux solutions de recherche hybride :</span><span class="sxs-lookup"><span data-stu-id="5c084-p119">The recommended actions for hybrid search solutions are the same as for search in SharePoint Server or SharePoint Online. There are two hybrid search solutions:</span></span>

<span data-ttu-id="5c084-p120">**Solution de recherche hybride dans le cloud :** avec la solution cloud de recherche hybride pour SharePoint, vous indexez l’ensemble de votre contenu analysé, y compris le contenu local, dans votre index de recherche dans Office 365. Lorsque les utilisateurs exécutent une requête dans votre index de recherche Office 365, ils reçoivent les résultats de recherche du contenu local et du contenu Office 365. Lorsque des documents sont supprimés de l’environnement SharePoint Server, ils sont également supprimés de l’index de recherche dans Office 365. [Découvrez la solution de recherche hybride sur le cloud](https://docs.microsoft.com/sharepoint/hybrid/learn-about-cloud-hybrid-search-for-sharepoint) et [comment les bases de données et composants de recherche interagissent dans la fonction de recherche hybride dans le cloud](https://docs.microsoft.com/sharepoint/hybrid/plan-cloud-hybrid-search-for-sharepoint) pour mieux comprendre l’incidence du RGPD sur l’environnement hybride.</span><span class="sxs-lookup"><span data-stu-id="5c084-p120">**The cloud hybrid search solution -** With the cloud hybrid search solution for SharePoint, you index all your crawled content, including on-premises content, in your search index in Office 365. When users query your search index in Office 365, they get search results from both on-premises and Office 365 content. When documents are deleted from the SharePoint Server environment, they are also deleted from the search index in Office 365. [Read more about the cloud hybrid search solution](https://docs.microsoft.com/sharepoint/hybrid/learn-about-cloud-hybrid-search-for-sharepoint) and [how search components and databases interact in cloud hybrid search](https://docs.microsoft.com/sharepoint/hybrid/plan-cloud-hybrid-search-for-sharepoint) to understand better how GDPR affects the hybrid environment.</span></span>

<span data-ttu-id="5c084-p121">**Solution de recherche fédérée hybride :** grâce à la solution de recherche fédérée hybride, vous utilisez votre index à la fois dans SharePoint Server et dans Office 365. Les services de recherche de SharePoint Server et de SharePoint Online peuvent exécuter une requête dans l’index de recherche dans l’autre environnement et renvoyer des résultats fédérés. Lorsque les utilisateurs effectuent une recherche à partir d’un centre de recherche, les résultats sont extraits de votre index de recherche dans SharePoint Server et dans Office 365. [Découvrez la solution de recherche fédérée hybride](https://docs.microsoft.com/sharepoint/hybrid/learn-about-hybrid-federated-search-for-sharepoint) pour mieux comprendre l’incident du RGPD sur l’environnement hybride.</span><span class="sxs-lookup"><span data-stu-id="5c084-p121">**The hybrid federated search solution -** With the hybrid federated search solution, you use both your index in SharePoint Server and your index in Office 365. Both SharePoint Server and SharePoint Online Search services can query the search index in the other environment and return federated results. When users search from a Search Center, the search results come from both your search index in SharePoint Server and your search index in Office 365. [Read more about the hybrid federated search solution](https://docs.microsoft.com/sharepoint/hybrid/learn-about-hybrid-federated-search-for-sharepoint) to understand better how GDPR affects the hybrid environment.</span></span>

## <a name="on-prem-to-cloud-migrations"></a><span data-ttu-id="5c084-212">Migrations depuis votre ordinateur local vers le cloud</span><span class="sxs-lookup"><span data-stu-id="5c084-212">On Prem to Cloud Migrations</span></span>

<span data-ttu-id="5c084-p122">Lors de la migration des données de SharePoint Server vers SharePoint Online, il se peut que des données existent en double aux deux emplacements pendant un certain temps. Si certaines données doivent être supprimées en cours de la migration, nous vous recommandons d’effectuer dans un premier temps la migration, puis de supprimer les données aux deux emplacements. Vous pouvez exécuter une requête de données pour exportation à partir d’un emplacement ou de l’autre.</span><span class="sxs-lookup"><span data-stu-id="5c084-p122">While migrating data from SharePoint Server to SharePoint Online, duplicate data may exist in both locations for a time. If you have data that you need to delete that is in mid-migration, we recommend that you complete the migration first, and then delete the data from both locations. You can query data for export from either location.</span></span>

## <a name="user-profile-data"></a><span data-ttu-id="5c084-216">Données des profils utilisateur</span><span class="sxs-lookup"><span data-stu-id="5c084-216">User Profile data</span></span>

<span data-ttu-id="5c084-p123">Le service de profil utilisateur permet d’importer des données de profil provenant de diverses sources externes. Les requêtes et les mises à jour liées à ces données de profil utilisateur doivent être gérées dans les systèmes dans lesquels les données sont administrées. Si vous effectuez des mises à jour sur le système externe, veillez à synchroniser à nouveau les profils utilisateur dans SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="5c084-p123">The User Profile Service allows for import of profile data from a variety of external sources. Queries for and update of such user profile data should be handled in the systems in which the data is mastered. If you make updates to the external system, be sure to synchronize the user profiles in SharePoint Server again.</span></span>

<span data-ttu-id="5c084-220">Suivez la procédure de base pour supprimer les informations personnelles d’un utilisateur de son profil utilisateur SharePoint Server :</span><span class="sxs-lookup"><span data-stu-id="5c084-220">Follow these basic steps to remove a user’s personal information from their SharePoint Server user profile:</span></span>

1.  <span data-ttu-id="5c084-p124">Supprimez les informations utilisateur sur tout système externe alimentant le profil utilisateur SharePoint Server. Si vous utilisez la synchronisation d’annuaires, l’utilisateur doit être supprimé de l’environnement Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="5c084-p124">Remove the user information from any external systems that feed into the SharePoint Server user profile. If you are using directory synchronization, the user must be removed from the on-premises Active Directory environment.</span></span>

2.  <span data-ttu-id="5c084-223">Exécutez une [synchronisation des profils](https://docs.microsoft.com/sharepoint/administration/start-profile-synchronization-manually) sur SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="5c084-223">Run a [profile synchronization](https://docs.microsoft.com/sharepoint/administration/start-profile-synchronization-manually) on SharePoint Server.</span></span>

3.  <span data-ttu-id="5c084-p125">Supprimez le profil de SharePoint Server. Une fois cette opération terminée, SharePoint Server supprime entièrement le profil de la base de données de profil utilisateur dans les 30 jours. Le site personnel et la page de profil de l’utilisateur sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="5c084-p125">Delete the profile from SharePoint Server. Once this is done, SharePoint Server will fully remove the profile from the User Profile Database in 30 days. The user’s profile page and personal site will be deleted.</span></span>

<span data-ttu-id="5c084-p126">Après la suppression d’un profil utilisateur, certaines informations limitées (par exemple, l’ID utilisateur) peuvent toujours être enregistrées dans les collections de sites que l’utilisateur a consultées. Si vous choisissez de supprimer ces données dans une collection de sites donnée, cette opération peut être effectuée à l’aide du modèle CSOM. Vous trouverez un exemple de script ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="5c084-p126">After deleting a user’s profile, some limited information (such as user ID) may still be recorded in site collections that the user has visited. If you choose to delete this data from a given site collection, this can be done using CSOM. A sample script is provided below:</span></span>

```powershell
$username = "<admin@company.sharepoint.com>"
$password = "password"
$url = "<https://site.sharepoint.com>"
$securePassword = ConvertTo-SecureString $Password -AsPlainText -Force

# the path here may need to change if you used e.g. C:Lib.
Add-Type -Path "c:\Program Files\Common Files\microsoft shared\Web Server Extensions\16ISAPIMicrosoft.SharePoint.Client.dll"
Add-Type -Path "c:\Program Files\Common Files\microsoft shared\Web Server Extensions\16ISAPIMicrosoft.SharePoint.Client.Runtime.dll"

# connect/authenticate to SharePoint Online and get ClientContext object.
$clientContext = New-Object Microsoft.SharePoint.Client.ClientContext($url)
$credentials = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($username, $securePassword)
$clientContext.Credentials = $credentials
if (!$clientContext.ServerObjectIsNull.Value)
{
    Write-Host "Connected to SharePoint Online site: '$Url'" -ForegroundColor Green
}

# Get user
$user = $clientContext.Web.SiteUsers.GetByLoginName("i:0#.f|membership|user@company.sharepoint.com")

# Redact user
$user.Email = "Redacted"
$user.Title = "Redacted"
$user.Update()
$clientContext.Load($user)
$clientContext.ExecuteQuery()

# Get users
$users = $clientContext.Web.SiteUsers

# Remove user from site
$users.RemoveById($user.Id)
$clientContext.Load($users)
$clientContext.ExecuteQuery()
```
