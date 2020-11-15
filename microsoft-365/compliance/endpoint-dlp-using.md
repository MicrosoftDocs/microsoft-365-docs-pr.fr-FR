---
title: Utilisation de la protection contre la perte de données de point de terminaison
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 07/21/2020
audience: ITPro
ms.topic: article
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MET150
description: Découvrez comment configurer les stratégies de protection contre la perte de données (DLP) pour utiliser les emplacements de protection contre la perte de données de point de terminaison (EPDLP) Microsoft 365.
ms.openlocfilehash: 64cdfeab4b527dd3b84e7586d1419e5bf8b383df
ms.sourcegitcommit: fcc1b40732f28f075d95faffc1655473e262dd95
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2020
ms.locfileid: "49073103"
---
# <a name="using-endpoint-data-loss-prevention"></a><span data-ttu-id="bfec5-103">Utilisation de la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bfec5-103">Using Endpoint data loss prevention</span></span>

<span data-ttu-id="bfec5-104">Cet article décrit trois scénarios dans lesquels vous créez et modifiez une stratégie DLP qui utilise des appareils comme emplacements.</span><span class="sxs-lookup"><span data-stu-id="bfec5-104">This article walks you through three scenarios where you create and modify a DLP policy that uses devices as a location.</span></span>

## <a name="dlp-settings"></a><span data-ttu-id="bfec5-105">Paramètres DLP</span><span class="sxs-lookup"><span data-stu-id="bfec5-105">DLP settings</span></span>

<span data-ttu-id="bfec5-p101">Avant de commencer, vous devez configurer vos paramètres DLP appliqués à toutes les stratégies DLP pour les appareils. Vous devez les configurer si vous envisagez de créer des stratégies qui appliquent :</span><span class="sxs-lookup"><span data-stu-id="bfec5-p101">Before you get started you should set up your DLP settings which are applied to all DLP policies for devices. You must configure these if you intend to create policies that enforce:</span></span>

- <span data-ttu-id="bfec5-108">des restrictions de sortie dans le cloud</span><span class="sxs-lookup"><span data-stu-id="bfec5-108">cloud egress restrictions</span></span>
- <span data-ttu-id="bfec5-109">restrictions relatives aux applications non autorisées</span><span class="sxs-lookup"><span data-stu-id="bfec5-109">unallowed apps restrictions</span></span>

<span data-ttu-id="bfec5-110">Ou</span><span class="sxs-lookup"><span data-stu-id="bfec5-110">Or</span></span>

- <span data-ttu-id="bfec5-111">Si vous souhaitez exclure l’analyse des chemins d’accès aux fichiers bruyants</span><span class="sxs-lookup"><span data-stu-id="bfec5-111">If you want to exclude noisy file paths from monitoring</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="bfec5-112">![Paramètres DLP](../media/endpoint-dlp-1-using-dlp-settings.png)</span><span class="sxs-lookup"><span data-stu-id="bfec5-112">![DLP settings](../media/endpoint-dlp-1-using-dlp-settings.png)</span></span>

### <a name="file-path-exclusions"></a><span data-ttu-id="bfec5-113">Exclusions de chemin d’accès de fichier</span><span class="sxs-lookup"><span data-stu-id="bfec5-113">File path exclusions</span></span>

<span data-ttu-id="bfec5-p102">Vous souhaiterez peut-être exclure certains chemins d’accès de la surveillance DLP, des alertes DLP et de l’application de la stratégie DLP sur vos appareils, car ils sont trop brouillons ou ne contiennent pas de fichiers intéressants. Les fichiers situés à ces emplacements ne seront pas audités et les fichiers qui sont créés ou modifiés dans ces emplacements ne seront pas soumis à l’application de la stratégie DLP. Vous pouvez configurer des exclusions de chemin d’accès dans les paramètres DLP.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p102">You may want to exclude certain paths from DLP monitoring, DLP alerting, and DLP policy enforcement on your devices because they are too noisy or don’t contain files you are interested in. Files in those locations will not be audited and any files that are created or modified in those locations will not be subject to DLP policy enforcement. You can configure path exclusions in DLP settings.</span></span>

<span data-ttu-id="bfec5-117">Vous pouvez utiliser cette logique pour construire vos chemins d’exclusion :</span><span class="sxs-lookup"><span data-stu-id="bfec5-117">You can use this logic to construct your exclusion paths:</span></span>

- <span data-ttu-id="bfec5-118">Chemin d’accès de fichier valide se terminant par « \ », ce qui signifie uniquement les fichiers directement sous dossier.</span><span class="sxs-lookup"><span data-stu-id="bfec5-118">Valid file path that ends with ‘\’, which means only files directly under folder.</span></span> <br/><span data-ttu-id="bfec5-119">Par exemple: C:\Temp</span><span class="sxs-lookup"><span data-stu-id="bfec5-119">For example: C:\Temp</span></span>\

- <span data-ttu-id="bfec5-120">Chemin d’accès de fichier valide se terminant par « \* », ce qui signifie uniquement les sous-dossiers directement sous dossier.</span><span class="sxs-lookup"><span data-stu-id="bfec5-120">Valid file path that ends with ‘\*’, which means only files under sub-folders, besides the files directly under the folder.</span></span> <br/><span data-ttu-id="bfec5-121">Par exemple: C:\Temp\*</span><span class="sxs-lookup"><span data-stu-id="bfec5-121">For example: C:\Temp\*</span></span>

- <span data-ttu-id="bfec5-122">Chemin d’accès de fichier valide se terminant par « \ » ou «\*», ce qui signifie uniquement les fichiers directement sous dossier et tous les sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="bfec5-122">Valid file path that ends without ‘\’ or ‘\*’, which means all files directly under folder and all sub-folders.</span></span> <br/><span data-ttu-id="bfec5-123">Par exemple: C:\Temp</span><span class="sxs-lookup"><span data-stu-id="bfec5-123">For example: C:\Temp</span></span>

- <span data-ttu-id="bfec5-124">Un chemin d’accès avec un caractère générique entre' \ 'de chaque côté.</span><span class="sxs-lookup"><span data-stu-id="bfec5-124">A path with wildcard between ‘\’ from each side.</span></span> <br/><span data-ttu-id="bfec5-125">Par exemple : C:\Users\*\Desktop</span><span class="sxs-lookup"><span data-stu-id="bfec5-125">For example: C:\Users\*\Desktop</span></span>\

- <span data-ttu-id="bfec5-126">Un chemin d’accès comportant le caractère générique entre « \» de chaque côté et «(nombre)» pour indiquer le nombre exact de sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="bfec5-126">A path with wildcard between ‘\’ from each side and with ‘(number)’ to give exact number of subfolders.</span></span> <br/><span data-ttu-id="bfec5-127">Par exemple : C:\Users\*(1) \Downloads</span><span class="sxs-lookup"><span data-stu-id="bfec5-127">For example: C:\Users\*(1)\Downloads</span></span>\

- <span data-ttu-id="bfec5-128">Un chemin d’accès avec des variables d’environnement système.</span><span class="sxs-lookup"><span data-stu-id="bfec5-128">A path with SYSTEM environment variables.</span></span> <br/><span data-ttu-id="bfec5-129">Par exemple :%SystemDrive%\Test\*</span><span class="sxs-lookup"><span data-stu-id="bfec5-129">For example: %SystemDrive%\Test\*</span></span>

- <span data-ttu-id="bfec5-130">Un mélange de tous les éléments ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="bfec5-130">A mix of all the above.</span></span> <br/><span data-ttu-id="bfec5-131">Par exemple :%SystemDrive%\Users\*\Documents\*(2) \Sub</span><span class="sxs-lookup"><span data-stu-id="bfec5-131">For example: %SystemDrive%\Users\*\Documents\*(2)\Sub</span></span>\

### <a name="service-domains"></a><span data-ttu-id="bfec5-132">Domaines de service</span><span class="sxs-lookup"><span data-stu-id="bfec5-132">Service domains</span></span>

<span data-ttu-id="bfec5-133">Vous pouvez ajouter à cette liste des domaines auxquels Edge Chromium fera référence lors de l’application de la restriction d’accès au téléchargement de la stratégie DLP pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="bfec5-133">You can add domains to this list that Edge Chromium will refer to when enforcing the Endpoint DLP policy cloud upload access restriction.</span></span> 

<span data-ttu-id="bfec5-p103">Si le mode liste est défini sur **Bloquer** , l’utilisateur ne pourra pas télécharger les éléments sensibles vers ces domaines. Lorsqu’une action de téléchargement est bloquée car un élément correspond à une stratégie DLP, DLP génère un avertissement ou bloque le téléchargement de l’élément sensible.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p103">If the list mode is set to **Block** , then user will not be able to upload sensitive items to those domains. When an upload action is blocked because an item matches a DLP policy, DLP will either generate a warning or block the upload of the sensitive item.</span></span>

<span data-ttu-id="bfec5-136">Si le mode de liste est paramétré sur **Autoriser** , les utilisateurs pourront charger des éléments sensibles \* *_uniquement_* dans ces domaines, et l’accès de chargement à tous les autres domaines n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="bfec5-136">If the list mode is set to **Allow** , then users will be able to upload sensitive items \* *_only_* _ to those domains, and upload access to all other domains is not allowed.</span></span>

### <a name="unallowed-apps"></a><span data-ttu-id="bfec5-137">Applications non autorisées</span><span class="sxs-lookup"><span data-stu-id="bfec5-137">Unallowed apps</span></span>

<span data-ttu-id="bfec5-p104">Lorsque le paramètre _ *Accès par des applications et navigateurs non autorisés* \* d’une stratégie est activé et que les utilisateurs tentent d’utiliser ces applications pour accéder à un fichier protégé, l’activité est autorisée, bloquée ou bloquée, mais les utilisateurs peuvent ignorer la restriction. Toutes les activités sont auditées et peuvent être consultées dans l’explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p104">When a policy's _ *Access by unallowed apps and browsers* \* setting is turned on and users attempt to use these apps to access a protected file, the activity will be allowed, blocked, or blocked but users can override the restriction. All activity is audited and available to review in activity explorer.</span></span>

### <a name="unallowed-browsers"></a><span data-ttu-id="bfec5-140">Navigateurs non autorisés</span><span class="sxs-lookup"><span data-stu-id="bfec5-140">Unallowed browsers</span></span>

<span data-ttu-id="bfec5-p105">Vous ajoutez des navigateurs, identifiés par leurs noms de fichiers exécutables, qui ne pourront pas accéder aux fichiers qui correspondent aux conditions d’une stratégie DLP appliquée dans laquelle la restriction de téléchargement vers les services cloud est définie sur bloquer ou bloquer le remplacement. Lorsque ces navigateurs ne peuvent pas accéder à un fichier, les utilisateurs finaux verront une notification toast leur demandant d’ouvrir le fichier via Edge Chromium.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p105">You add browsers, identified by their executable names, that will be blocked from accessing files that match the conditions of an enforced a DLP policy where the upload to cloud services restriction is set to block or block override. When these browsers are blocked from accessing a file, the end users will see a toast notification asking them to open the file through Edge Chromium.</span></span>

[!IMPORTANT]
<span data-ttu-id="bfec5-143">N’incluez pas le chemin d’accès du fichier exécutable, mais uniquement le nom du fichier exécutable (par exemple, browser.exe).</span><span class="sxs-lookup"><span data-stu-id="bfec5-143">Do not include the path to the executable, but only the executable name (i.e., browser.exe).</span></span>

## <a name="tying-dlp-settings-together"></a><span data-ttu-id="bfec5-144">Lier les paramètres DLP</span><span class="sxs-lookup"><span data-stu-id="bfec5-144">Tying DLP settings together</span></span>

<span data-ttu-id="bfec5-p106">Avec le navigateur web Edge Chromium et la DLP pour point de terminaison, vous pouvez limiter le partage involontaire d’éléments sensibles aux applications et services cloud non autorisés. Edge Chromium comprend quand un élément est restreint par une stratégie DLP pour point de terminaison et applique des restrictions d’accès.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p106">With Endpoint DLP and Edge Chromium Web browser, you can restrict unintentional sharing of sensitive items to unallowed cloud apps and services. Edge Chromium understands when an item is restricted by an Endpoint DLP policy and enforces access restrictions.</span></span>

<span data-ttu-id="bfec5-p107">Lorsque vous utilisez DLP pour point de terminaison comme emplacement dans une stratégie DLP correctement configurée et le navigateur Edge Chromium, les navigateurs non autorisés que vous avez définis dans ces paramètres ne pourront pas accéder aux éléments sensibles qui correspondent à vos contrôles de stratégie DLP. Les utilisateurs seront plutôt redirigés pour utiliser Edge Chromium qui, avec sa compréhension des restrictions imposées par DLP, peut bloquer ou restreindre les activités lorsque les conditions de la stratégie DLP sont remplies.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p107">When you use Endpoint DLP as a location in a properly configured DLP policy and the Edge Chromium browser, the unallowed browsers that you've defined in these settings will be prevented from accessing the sensitive items that match your DLP policy controls. Instead, users will be redirected to use Edge Chromium and Edge Chromium, with its understanding of DLP imposed restrictions, can block or restrict activities when the conditions in the DLP policy are met.</span></span>

<span data-ttu-id="bfec5-149">Pour utiliser cette restriction, vous devez configurer trois éléments importants :</span><span class="sxs-lookup"><span data-stu-id="bfec5-149">To use this restriction you’ll need to configure three important pieces:</span></span>

1. <span data-ttu-id="bfec5-150">Spécifier les emplacements ,services, domaines, adresses IP, avec lesquels vous ne souhaitez pas partager les éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="bfec5-150">Specify the places – services, domains, IP addresses – that you want to prevent sensitive items from being shared to.</span></span>

2. <span data-ttu-id="bfec5-151">Ajouter les navigateurs qui ne sont pas autorisés à accéder à certains éléments sensibles lorsqu’une correspondance de la stratégie DLP se produit.</span><span class="sxs-lookup"><span data-stu-id="bfec5-151">Add the browsers that aren’t allowed to access certain sensitive items when a DLP policy match occurs.</span></span>

3. <span data-ttu-id="bfec5-152">Configurez les stratégies DLP pour définir les types d’éléments sensibles pour lesquels le téléchargement doit être limité à ces emplacements en activant **Télécharger vers les services Cloud** et **Accès à partir d’un navigateur non autorisé**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-152">Configure DLP policies to define the kinds of sensitive items for which upload should be restricted to these places by turning on **Upload to cloud services** and **Access from unallowed browser**.</span></span>

<span data-ttu-id="bfec5-153">Vous pouvez continuer à ajouter de nouveaux services, applications et stratégies pour développer et augmenter vos restrictions afin de répondre aux besoins de votre entreprise et de protéger les données sensibles.</span><span class="sxs-lookup"><span data-stu-id="bfec5-153">You can continue to add new services, apps, and policies to extend and augment your restrictions to meet your business needs and protect sensitive data.</span></span> 

<span data-ttu-id="bfec5-154">Cette configuration vous permet de garantir la sécurité de vos données tout en évitant les restrictions inutiles qui empêchent les utilisateurs d’accéder aux éléments non sensibles et de les empêcher de les partager.</span><span class="sxs-lookup"><span data-stu-id="bfec5-154">This configuration will help ensure your data remains safe while also avoiding unnecessary restrictions that prevent or restrict users from accessing and sharing non-sensitive items.</span></span>

## <a name="endpoint-dlp-policy-scenarios"></a><span data-ttu-id="bfec5-155">Scénarios de stratégie DLP pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bfec5-155">Endpoint DLP policy scenarios</span></span>

<span data-ttu-id="bfec5-p108">Pour vous aider à vous familiariser avec les fonctionnalités DLP pour point de terminaison et la manière dont elles apparaissent dans les stratégies DLP, nous avons rassemblé quelques scénarios à suivre. Tout le contenu DLP pour point de terminaison sera intégré à l’ensemble de contenu DLP principal lorsque DLP pour point de terminaison sera disponible pour le grand public.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p108">To help familiarize you with Endpoint DLP features and how they surface in DLP policies, we've put together some scenarios for you to follow. All the Endpoint DLP content will be folded in to the main DLP content set when Endpoint DLP becomes generally available.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bfec5-p109">Ces scénarios DLP pour point de terminaison ne sont pas les procédures officielles de création et de configuration des stratégies DLP. Reportez-vous aux rubriques ci-dessous lorsque vous devez travailler avec des stratégies DLP dans des situations générales :</span><span class="sxs-lookup"><span data-stu-id="bfec5-p109">These Endpoint DLP scenarios are not the official procedures for creating and tuning DLP policies. Refer to the below topics when you need to work with DLP policies in general situations:</span></span>
>- [<span data-ttu-id="bfec5-160">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="bfec5-160">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
>- [<span data-ttu-id="bfec5-161">Prise en main de la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="bfec5-161">Get started with the default DLP policy</span></span>](get-started-with-the-default-dlp-policy.md)
>- [<span data-ttu-id="bfec5-162">Création d’une stratégie DLP à partir d’un modèle</span><span class="sxs-lookup"><span data-stu-id="bfec5-162">Create a DLP policy from a template</span></span>](create-a-dlp-policy-from-a-template.md)
>- [<span data-ttu-id="bfec5-163">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="bfec5-163">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)

### <a name="scenario-1-create-a-policy-from-a-template-audit-only"></a><span data-ttu-id="bfec5-164">Scénario 1 : créer une stratégie à partir d’un modèle, audit uniquement</span><span class="sxs-lookup"><span data-stu-id="bfec5-164">Scenario 1: Create a policy from a template, audit only</span></span>

<span data-ttu-id="bfec5-p110">Ces scénarios nécessitent que vous ayez déjà des appareils intégrés et des rapports dans l’explorateur d’activité. Si vous n’avez pas encore intégré d’appareils, consultez l’article [Prise en main de la protection contre la perte de données de point de terminaison](endpoint-dlp-getting-started.md).</span><span class="sxs-lookup"><span data-stu-id="bfec5-p110">These scenarios require that you already have devices onboarded and reporting into Activity explorer. If you haven't onboarded devices yet, see [Get started with Endpoint data loss prevention](endpoint-dlp-getting-started.md).</span></span>

1. <span data-ttu-id="bfec5-167">Ouvrir la [page de protection contre la perte de données](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span><span class="sxs-lookup"><span data-stu-id="bfec5-167">Open the [Data loss prevention page](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span></span>

2. <span data-ttu-id="bfec5-168">Sélectionnez **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-168">Choose **Create policy**.</span></span>

3. <span data-ttu-id="bfec5-169">Dans le cadre de ce scénario, sélectionnez **Confidentialité** , **Données d’informations d’identification personnelles pour les États-Unis** puis, **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-169">For this scenario, choose **Privacy** , then **U.S. Personally Identifiable Information (PII) Data** and choose **Next**.</span></span>

4. <span data-ttu-id="bfec5-p111">Désactivez le champ **État** pour tous les emplacements, à l’exception de **Appareils**. Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p111">Toggle the **Status** field to off for all locations except **Devices**. Choose **Next**.</span></span>

5. <span data-ttu-id="bfec5-172">Acceptez la sélection par défaut **Vérifier et personnaliser les paramètres du modèle** , puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-172">Accept the default **Review and customize settings from the template** selection and choose **Next**.</span></span>

6. <span data-ttu-id="bfec5-173">Acceptez les valeurs par défaut **Actions de protection** et sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-173">Accept the default **Protection actions** values and choose **Next**.</span></span>

7. <span data-ttu-id="bfec5-p112">Sélectionnez **Auditer ou restreindre les activités sur les appareils Windows** et laissez les actions définies sur **Audit uniquement**. Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p112">Select **Audit or restrict activities on Windows devices** and leave the actions set to **Audit only**. Choose **Next**.</span></span>

8. <span data-ttu-id="bfec5-p113">Acceptez la valeur par défaut, **Je veux d’abord tester** et sélectionnez **Afficher les conseils de stratégie en mode de test**. Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p113">Accept the default **I'd like to test it out first** value and choose **Show policy tips while in test mode**. Choose **Next**.</span></span>

9. <span data-ttu-id="bfec5-178">Vérifiez vos paramètres, puis sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-178">Review your settings and choose **Submit**.</span></span>

10. <span data-ttu-id="bfec5-179">La nouvelle stratégie DLP s’affiche dans la liste des stratégies.</span><span class="sxs-lookup"><span data-stu-id="bfec5-179">The new DLP policy will appear in the policy list.</span></span>

11. <span data-ttu-id="bfec5-p114">Recherchez dans l’explorateur d’activité les données des points de terminaison surveillés. Définissez le filtre d’emplacement pour les appareils et ajoutez la stratégie. Ensuite, filtrez par nom de stratégie pour voir l’impact de cette stratégie. Consultez l’article [Prise en main de l’explorateur d’activités](data-classification-activity-explorer.md) si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p114">Check Activity explorer for data from the monitored endpoints. Set the location filter for devices and add the policy, then filter by policy name to see the impact of this policy. See, [Get started with activity explorer](data-classification-activity-explorer.md) if needed.</span></span>

12. <span data-ttu-id="bfec5-p115">Tenter de partager un test qui contient un contenu qui déclenchera la condition des données des informations personnelles identifiables pour les États-Unis avec une personne extérieure à votre organisation. Cela devrait déclencher la stratégie.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p115">Attempt to share a test that contains content that will trigger the U.S. Personally Identifiable Information (PII) Data condition with someone outside your organization. This should trigger the policy.</span></span>

13. <span data-ttu-id="bfec5-185">Consultez l’Explorateur d’activités pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="bfec5-185">Check Activity explorer for the event.</span></span>

### <a name="scenario-2-modify-the-existing-policy-set-an-alert"></a><span data-ttu-id="bfec5-186">Scénario 2 : modifier la stratégie existante, créer une alerte</span><span class="sxs-lookup"><span data-stu-id="bfec5-186">Scenario 2: Modify the existing policy, set an alert</span></span>

1. <span data-ttu-id="bfec5-187">Ouvrir[Page de protection contre la perte de données](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span><span class="sxs-lookup"><span data-stu-id="bfec5-187">Open the [Data loss prevention page](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span></span>

2. <span data-ttu-id="bfec5-188">Sélectionnez la stratégie **Données d’informations d’identification personnelle pour les États-Unis** que vous avez créée dans le scénario 1.</span><span class="sxs-lookup"><span data-stu-id="bfec5-188">Choose the **U.S. Personally Identifiable Information (PII) Data** policy that you created in scenario 1.</span></span>

3. <span data-ttu-id="bfec5-189">Sélectionnez **Modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-189">Choose **edit policy**.</span></span>

4. <span data-ttu-id="bfec5-190">Accédez à la page **Règles DLP avancées** et modifiez la **Faible quantité de contenu détectée pour les informations d’identification personnelle**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-190">Go to the **Advanced DLP rules** page and edit the **Low volume of content detected U.S. Personally Identifiable Inf**.</span></span>

5. <span data-ttu-id="bfec5-p116">Faites défiler jusqu’à la section **Rapports d’incident** et définissez **Envoyer une alerte aux administrateurs lorsqu’une correspondance de règle se produit** sur **Activé**. Les alertes par e-mail seront automatiquement envoyées à l’administrateur et aux autres personnes que vous ajoutez à la liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p116">Scroll down to the **Incident reports** section and set **Send an alert to admins when a rule match occurs** to **On**. Email alerts will be automatically sent to the administrator and anyone else you add to the list of recipients.</span></span> 

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="bfec5-193">![activer les rapports d’incident](../media/endpoint-dlp-2-using-dlp-incident-reports.png)</span><span class="sxs-lookup"><span data-stu-id="bfec5-193">![turn-on-incident-reports](../media/endpoint-dlp-2-using-dlp-incident-reports.png)</span></span>
   
6. <span data-ttu-id="bfec5-194">Dans le cadre de ce scénario, sélectionnez **Envoyer une alerte chaque fois qu’une activité correspond à la règle**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-194">For the purposes of this scenario, choose **Send alert every time an activity matches the rule**.</span></span>

7. <span data-ttu-id="bfec5-195">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-195">Choose **Save**.</span></span>

8. <span data-ttu-id="bfec5-196">Conservez tous vos paramètres précédents en choisissant **suivant** puis **Envoyez** les modifications apportées à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="bfec5-196">Retain all your previous settings by choosing **Next** and then **Submit** the policy changes.</span></span>

9. <span data-ttu-id="bfec5-p117">Tenter de partager un test qui contient un contenu qui déclenchera la condition des données des informations personnelles identifiables pour les États-Unis avec une personne extérieure à votre organisation. Cela devrait déclencher la stratégie.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p117">Attempt to share a test that contains content that will trigger the U.S. Personally Identifiable Information (PII) Data condition with someone outside your organization. This should trigger the policy.</span></span>

10. <span data-ttu-id="bfec5-199">Consultez l’Explorateur d’activités pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="bfec5-199">Check Activity explorer for the event.</span></span>

### <a name="scenario-3-modify-the-existing-policy-block-the-action-with-allow-override"></a><span data-ttu-id="bfec5-200">Scénario 3 : modifier la stratégie existante, bloquer l’action avec l’option autoriser le remplacement</span><span class="sxs-lookup"><span data-stu-id="bfec5-200">Scenario 3: Modify the existing policy, block the action with allow override</span></span>

1. <span data-ttu-id="bfec5-201">Ouvrir[Page de protection contre la perte de données](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span><span class="sxs-lookup"><span data-stu-id="bfec5-201">Open the [Data loss prevention page](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span></span>

2. <span data-ttu-id="bfec5-202">Sélectionnez la stratégie **Données d’informations d’identification personnelle pour les États-Unis** que vous avez créée dans le scénario 1.</span><span class="sxs-lookup"><span data-stu-id="bfec5-202">Choose the **U.S. Personally Identifiable Information (PII) Data** policy that you created in scenario 1.</span></span>

3. <span data-ttu-id="bfec5-203">Sélectionnez **Modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-203">Choose **edit policy**.</span></span>

4. <span data-ttu-id="bfec5-204">Accédez à la page **Règles DLP avancées** et modifiez la **Faible quantité de contenu détectée pour les informations d’identification personnelle**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-204">Go to the **Advanced DLP rules** page and edit the **Low volume of content detected U.S. Personally Identifiable Inf**.</span></span>

5. <span data-ttu-id="bfec5-205">Faites défiler vers le bas jusqu’à la section **Audit ou restreindre les activités sur les appareils Windows** et pour chaque activité définissez l’action correspondante sur **Bloquer avec remplacement**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-205">Scroll down to the **Audit or restrict activities on Windows device** section and for each activity set the corresponding action to  **Block with override**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="bfec5-206">![définir un blocage avec une action de remplacement](../media/endpoint-dlp-6-using-dlp-set-blocked-with-override.png)</span><span class="sxs-lookup"><span data-stu-id="bfec5-206">![set block with override action](../media/endpoint-dlp-6-using-dlp-set-blocked-with-override.png)</span></span>
   
6. <span data-ttu-id="bfec5-207">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-207">Choose **Save**.</span></span>

7. <span data-ttu-id="bfec5-208">Répétez les étapes 4-7 pour **Quantité de contenu élevé détectée le fichier INF (INF) US**.</span><span class="sxs-lookup"><span data-stu-id="bfec5-208">Repeat steps 4-7 for the **High volume of content detected U.S. Personally Identifiable Inf**.</span></span>

8. <span data-ttu-id="bfec5-209">Conservez tous vos paramètres précédents en choisissant **suivant** puis **Envoyez** les modifications apportées à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="bfec5-209">Retain all your previous settings by choosing **Next** and then **Submit** the policy changes.</span></span>

9. <span data-ttu-id="bfec5-p118">Tenter de partager un test qui contient un contenu qui déclenchera la condition des données des informations personnelles identifiables pour les États-Unis avec une personne extérieure à votre organisation. Cela devrait déclencher la stratégie.</span><span class="sxs-lookup"><span data-stu-id="bfec5-p118">Attempt to share a test that contains content that will trigger the U.S. Personally Identifiable Information (PII) Data condition with someone outside your organization. This should trigger the policy.</span></span>

   <span data-ttu-id="bfec5-212">Une fenêtre contextuelle semblable à celle-ci s’affiche sur l’appareil client :</span><span class="sxs-lookup"><span data-stu-id="bfec5-212">You'll see a popup like this on the client device:</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="bfec5-213">![blocage de la notification de remplacement par le client dlp de point de terminaison](../media/endpoint-dlp-3-using-dlp-client-blocked-override-notification.png)</span><span class="sxs-lookup"><span data-stu-id="bfec5-213">![endpoint dlp client blocked override notification](../media/endpoint-dlp-3-using-dlp-client-blocked-override-notification.png)</span></span>

10. <span data-ttu-id="bfec5-214">Consultez l’Explorateur d’activités pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="bfec5-214">Check Activity explorer for the event.</span></span>

## <a name="see-also"></a><span data-ttu-id="bfec5-215">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfec5-215">See also</span></span>

- [<span data-ttu-id="bfec5-216">Découvrir la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bfec5-216">Learn about Endpoint data loss prevention</span></span>](endpoint-dlp-learn-about.md)
- [<span data-ttu-id="bfec5-217">Prise en main la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bfec5-217">Get started with Endpoint data loss prevention</span></span>](endpoint-dlp-getting-started.md)
- [<span data-ttu-id="bfec5-218">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="bfec5-218">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="bfec5-219">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="bfec5-219">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="bfec5-220">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="bfec5-220">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="bfec5-221">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bfec5-221">Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection/)
- <span data-ttu-id="bfec5-222">[Outils et méthodes d’intégration pour les appareils Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="bfec5-222">[Onboarding tools and methods for Windows 10 machines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints)</span></span>
- [<span data-ttu-id="bfec5-223">Abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bfec5-223">Microsoft 365 subscription</span></span>](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1)
- [<span data-ttu-id="bfec5-224">Azure Active Directory (ADD) adhésion</span><span class="sxs-lookup"><span data-stu-id="bfec5-224">Azure Active Directory (AAD) joined</span></span>](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join)
- [<span data-ttu-id="bfec5-225">Télécharger le nouveau Microsoft Edge sur la base de chrome</span><span class="sxs-lookup"><span data-stu-id="bfec5-225">Download the new Microsoft Edge based on Chromium</span></span>](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium)
- [<span data-ttu-id="bfec5-226">Prise en main de la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="bfec5-226">Get started with the default DLP policy</span></span>](get-started-with-the-default-dlp-policy.md)
- [<span data-ttu-id="bfec5-227">Création d’une stratégie DLP à partir d’un modèle</span><span class="sxs-lookup"><span data-stu-id="bfec5-227">Create a DLP policy from a template</span></span>](create-a-dlp-policy-from-a-template.md)
