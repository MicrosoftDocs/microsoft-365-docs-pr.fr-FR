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
description: Découvrez comment configurer les stratégies de protection contre la perte de données (DLP) en utilisant les points de terminaison de protection contre la perte de données (EPDLP) de Microsoft 365.
ms.openlocfilehash: 1b918346467f9878582dfb301f48e530bfb400f8
ms.sourcegitcommit: 05f40904f8278f53643efa76a907968b5c662d9a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "52114092"
---
# <a name="using-endpoint-data-loss-prevention"></a><span data-ttu-id="82021-103">Utilisation de la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="82021-103">Using Endpoint data loss prevention</span></span>

<span data-ttu-id="82021-104">Cet article décrit trois scénarios dans lesquels vous créez et modifiez une stratégie DLP qui utilise des appareils comme emplacement.</span><span class="sxs-lookup"><span data-stu-id="82021-104">This article walks you through three scenarios where you create and modify a DLP policy that uses devices as a location.</span></span>

## <a name="dlp-settings"></a><span data-ttu-id="82021-105">Paramètres DLP</span><span class="sxs-lookup"><span data-stu-id="82021-105">DLP settings</span></span>

<span data-ttu-id="82021-106">Avant de commencer, vous devez configurer vos paramètres DLP appliqués à toutes les stratégies DLP pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="82021-106">Before you get started you should set up your DLP settings which are applied to all DLP policies for devices.</span></span> <span data-ttu-id="82021-107">Vous devez les configurer si vous envisagez de créer des stratégies qui appliquent :</span><span class="sxs-lookup"><span data-stu-id="82021-107">You must configure these if you intend to create policies that enforce:</span></span>

- <span data-ttu-id="82021-108">restrictions de sortie dans le Cloud</span><span class="sxs-lookup"><span data-stu-id="82021-108">cloud egress restrictions</span></span>
- <span data-ttu-id="82021-109">restrictions relatives aux applications non autorisées</span><span class="sxs-lookup"><span data-stu-id="82021-109">unallowed apps restrictions</span></span>

<span data-ttu-id="82021-110">Ou</span><span class="sxs-lookup"><span data-stu-id="82021-110">Or</span></span>

- <span data-ttu-id="82021-111">Si vous souhaitez exclure l’analyse des chemins d’accès aux fichiers bruyants</span><span class="sxs-lookup"><span data-stu-id="82021-111">If you want to exclude noisy file paths from monitoring</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="82021-112">![Paramètres DLP](../media/endpoint-dlp-1-using-dlp-settings.png)</span><span class="sxs-lookup"><span data-stu-id="82021-112">![DLP settings](../media/endpoint-dlp-1-using-dlp-settings.png)</span></span>

### <a name="file-path-exclusions"></a><span data-ttu-id="82021-113">Exclusions de chemin d’accès de fichier</span><span class="sxs-lookup"><span data-stu-id="82021-113">File path exclusions</span></span>

<span data-ttu-id="82021-114">Vous pouvez exclure certains chemins de la surveillance DLP, des alertes DLP et de l’application de stratégie DLP sur vos appareils, car ils sont trop bruyants ou ne contiennent pas les fichiers qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="82021-114">You may want to exclude certain paths from DLP monitoring, DLP alerting, and DLP policy enforcement on your devices because they are too noisy or don’t contain files you are interested in.</span></span> <span data-ttu-id="82021-115">Les fichiers stockés dans ces emplacements ne seront pas audités et tous les fichiers créés ou modifiés dans ces emplacements ne seront pas soumis à l’application de stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="82021-115">Files in those locations will not be audited and any files that are created or modified in those locations will not be subject to DLP policy enforcement.</span></span> <span data-ttu-id="82021-116">Vous pouvez configurer les exclusions de chemin d’accès dans les paramètres DLP.</span><span class="sxs-lookup"><span data-stu-id="82021-116">You can configure path exclusions in DLP settings.</span></span>

<span data-ttu-id="82021-117">Vous pouvez utiliser cette logique pour construire vos chemins d’exclusion :</span><span class="sxs-lookup"><span data-stu-id="82021-117">You can use this logic to construct your exclusion paths:</span></span>

- <span data-ttu-id="82021-118">Chemin d’accès de fichier valide se terminant par « \ », ce qui signifie uniquement les fichiers directement sous dossier.</span><span class="sxs-lookup"><span data-stu-id="82021-118">Valid file path that ends with ‘\’, which means only files directly under folder.</span></span> <br/><span data-ttu-id="82021-119">Par exemple: C:\Temp</span><span class="sxs-lookup"><span data-stu-id="82021-119">For example: C:\Temp</span></span>\

- <span data-ttu-id="82021-120">Chemin d’accès de fichier valide se terminant par « \* », ce qui signifie uniquement les sous-dossiers directement sous dossier.</span><span class="sxs-lookup"><span data-stu-id="82021-120">Valid file path that ends with ‘\*’, which means only files under sub-folders, besides the files directly under the folder.</span></span> <br/><span data-ttu-id="82021-121">Par exemple: C:\Temp\*</span><span class="sxs-lookup"><span data-stu-id="82021-121">For example: C:\Temp\*</span></span>

- <span data-ttu-id="82021-122">Chemin d’accès de fichier valide se terminant par « \ » ou «\*», ce qui signifie uniquement les fichiers directement sous dossier et tous les sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="82021-122">Valid file path that ends without ‘\’ or ‘\*’, which means all files directly under folder and all sub-folders.</span></span> <br/><span data-ttu-id="82021-123">Par exemple: C:\Temp</span><span class="sxs-lookup"><span data-stu-id="82021-123">For example: C:\Temp</span></span>

- <span data-ttu-id="82021-124">Un chemin d’accès avec un caractère générique entre' \ 'de chaque côté.</span><span class="sxs-lookup"><span data-stu-id="82021-124">A path with wildcard between ‘\’ from each side.</span></span> <br/><span data-ttu-id="82021-125">Par exemple : C:\Users\*\Desktop</span><span class="sxs-lookup"><span data-stu-id="82021-125">For example: C:\Users\*\Desktop</span></span>\

- <span data-ttu-id="82021-126">Un chemin d’accès comportant le caractère générique entre « \» de chaque côté et «(nombre)» pour indiquer le nombre exact de sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="82021-126">A path with wildcard between ‘\’ from each side and with ‘(number)’ to give exact number of subfolders.</span></span> <br/><span data-ttu-id="82021-127">Par exemple : C:\Users\*(1) \Downloads</span><span class="sxs-lookup"><span data-stu-id="82021-127">For example: C:\Users\*(1)\Downloads</span></span>\

- <span data-ttu-id="82021-128">Un chemin d’accès avec des variables d’environnement système.</span><span class="sxs-lookup"><span data-stu-id="82021-128">A path with SYSTEM environment variables.</span></span> <br/><span data-ttu-id="82021-129">Par exemple :%SystemDrive%\Test\*</span><span class="sxs-lookup"><span data-stu-id="82021-129">For example: %SystemDrive%\Test\*</span></span>

- <span data-ttu-id="82021-130">Un mélange de tous les éléments ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="82021-130">A mix of all the above.</span></span> <br/><span data-ttu-id="82021-131">Par exemple :%SystemDrive%\Users\*\Documents\*(2) \Sub</span><span class="sxs-lookup"><span data-stu-id="82021-131">For example: %SystemDrive%\Users\*\Documents\*(2)\Sub</span></span>\

### <a name="unallowed-apps"></a><span data-ttu-id="82021-132">Applications non autorisées</span><span class="sxs-lookup"><span data-stu-id="82021-132">Unallowed apps</span></span>

<span data-ttu-id="82021-133">Lorsque le paramètre **Accès par des applications et des navigateurs non autorisés** d’une stratégie est activé, et que les utilisateurs tentent d’utiliser ces applications pour accéder à un fichier protégé, l’activité est autorisée, bloquée, ou bloquée mais les utilisateurs peuvent annuler la restriction.</span><span class="sxs-lookup"><span data-stu-id="82021-133">When a policy's **Access by unallowed apps and browsers** setting is turned on and users attempt to use these apps to access a protected file, the activity will be allowed, blocked, or blocked but users can override the restriction.</span></span> <span data-ttu-id="82021-134">Toutes les activités sont auditées et disponibles pour révision dans l’Explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="82021-134">All activity is audited and available to review in activity explorer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82021-135">N’incluez pas le chemin d’accès du fichier exécutable, mais uniquement le nom du fichier exécutable (par exemple, browser.exe).</span><span class="sxs-lookup"><span data-stu-id="82021-135">Do not include the path to the executable, but only the executable name (such as browser.exe).</span></span>


### <a name="browser-and-domain-restrictions"></a><span data-ttu-id="82021-136">Restrictions de navigateur et de domaine :</span><span class="sxs-lookup"><span data-stu-id="82021-136">Browser and domain restrictions</span></span>
<span data-ttu-id="82021-137">Empêchez les fichiers sensibles, qui correspondent à vos stratégies, d’être partagés avec des domaines de service cloud sans restriction.</span><span class="sxs-lookup"><span data-stu-id="82021-137">Restrict sensitive files that match your policies from being shared with unrestricted cloud service domains.</span></span>

#### <a name="service-domains"></a><span data-ttu-id="82021-138">Domaines de service</span><span class="sxs-lookup"><span data-stu-id="82021-138">Service domains</span></span>

<span data-ttu-id="82021-139">Vous pouvez déterminer si les fichiers sensibles protégés par vos stratégies peuvent être téléchargés vers des domaines de service spécifiques à partir de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="82021-139">You can control whether sensitive files protected by your policies can be uploaded to specific service domains from Microsoft Edge.</span></span>

<span data-ttu-id="82021-140">Si le mode de liste est paramétré sur **Bloquer**, l’utilisateur ne peut pas télécharger des éléments sensibles dans ces domaines.</span><span class="sxs-lookup"><span data-stu-id="82021-140">If the list mode is set to **Block**, then user will not be able to upload sensitive items to those domains.</span></span> <span data-ttu-id="82021-141">Lorsqu’une action de téléchargement est bloquée parce qu’un élément correspond à une stratégie DLP, DLP génère un avertissement ou bloque le téléchargement de l’élément sensible.</span><span class="sxs-lookup"><span data-stu-id="82021-141">When an upload action is blocked because an item matches a DLP policy, DLP will either generate a warning or block the upload of the sensitive item.</span></span>

<span data-ttu-id="82021-142">Si le mode liste est défini sur **Autoriser**, les utilisateurs pourront charger des éléments sensibles **_uniquement_** vers ces domaines, et l’accès au chargement vers tous les autres domaines n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="82021-142">If the list mode is set to **Allow**, then users will be able to upload sensitive items **_only_** to those domains, and upload access to all other domains is not allowed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82021-143">Lorsque le mode de restriction de service est configuré sur « Autoriser », vous devez configurer au moins un domaine de service avant l’application des restrictions.</span><span class="sxs-lookup"><span data-stu-id="82021-143">When the service restriction mode is set to "Allow", you must have at least one service domain configured before restrictions are enforced.</span></span>

#### <a name="unallowed-browsers"></a><span data-ttu-id="82021-144">Navigateurs non autorisés</span><span class="sxs-lookup"><span data-stu-id="82021-144">Unallowed browsers</span></span>

<span data-ttu-id="82021-145">Vous ajoutez des navigateurs, identifiés par leurs noms de exécutables, qui ne peuvent pas accéder à des fichiers qui remplissent les conditions d’une stratégie DLP appliquée dans laquelle la restriction de chargement vers les services Cloud est définie sur bloquer ou annuler le blocage.</span><span class="sxs-lookup"><span data-stu-id="82021-145">You add browsers, identified by their executable names, that will be blocked from accessing files that match the conditions of an enforced a DLP policy where the upload to cloud services restriction is set to block or block override.</span></span> <span data-ttu-id="82021-146">Lorsque ces navigateurs ne peuvent pas accéder à un fichier, les utilisateurs finaux voient s’afficher une notification leur demandant d’ouvrir le fichier via le Chromium Edge.</span><span class="sxs-lookup"><span data-stu-id="82021-146">When these browsers are blocked from accessing a file, the end users will see a toast notification asking them to open the file through Edge Chromium.</span></span>

### <a name="business-justification-in-policy-tips"></a><span data-ttu-id="82021-147">Justification métier dans les conseils de stratégie</span><span class="sxs-lookup"><span data-stu-id="82021-147">Business justification in policy tips</span></span>

<span data-ttu-id="82021-148">Vous pouvez contrôler l’interaction des utilisateurs avec l’option de justification métier dans les notifications de conseil de stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="82021-148">You can control how users interact with the business justification option in DLP policy tip notifications.</span></span> <span data-ttu-id="82021-149">Cette option s’affiche lorsque les utilisateurs effectuent une activité protégée par le paramètre **Bloquer avec remplacement** dans une stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="82021-149">This option appears when users perform an activity that's protected by the **Block with override** setting in a DLP policy.</span></span> <span data-ttu-id="82021-150">Vous pouvez choisir l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="82021-150">You can choose from one the following options:</span></span>

- <span data-ttu-id="82021-151">Par défaut, les utilisateurs peuvent sélectionner une justification intégrée ou entrer leur propre texte.</span><span class="sxs-lookup"><span data-stu-id="82021-151">By default, users can select either a built-in justification, or enter their own text.</span></span>
- <span data-ttu-id="82021-152">Les utilisateurs ne peuvent sélectionner qu’une justification intégrée.</span><span class="sxs-lookup"><span data-stu-id="82021-152">Users can only select a built-in justification.</span></span>
- <span data-ttu-id="82021-153">Les utilisateurs ne peuvent entrer que leur propre justification.</span><span class="sxs-lookup"><span data-stu-id="82021-153">Users can only enter their own justification.</span></span>


## <a name="tying-dlp-settings-together"></a><span data-ttu-id="82021-154">Lier les paramètres DLP ensemble</span><span class="sxs-lookup"><span data-stu-id="82021-154">Tying DLP settings together</span></span>

<span data-ttu-id="82021-155">Avec les points de terminaison DLP et le navigateur Chromium Edge, vous pouvez limiter le partage involontaire des éléments sensibles aux applications et services Cloud non autorisés.</span><span class="sxs-lookup"><span data-stu-id="82021-155">With Endpoint DLP and Edge Chromium Web browser, you can restrict unintentional sharing of sensitive items to unallowed cloud apps and services.</span></span> <span data-ttu-id="82021-156">Le Chromium Edge comprend les conditions dans lesquelles un élément est limité par une stratégie DLP de point de terminaison et applique les restrictions d’accès.</span><span class="sxs-lookup"><span data-stu-id="82021-156">Edge Chromium understands when an item is restricted by an Endpoint DLP policy and enforces access restrictions.</span></span>

<span data-ttu-id="82021-157">Lorsque vous utilisez la fonctionnalité point de terminaison DLP comme emplacement dans une stratégie DLP correctement configurée et le navigateur Chromium Edge, les navigateurs non autorisés que vous avez définis dans ces paramètres ne pourront pas accéder aux éléments sensibles qui correspondent à vos contrôles de stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="82021-157">When you use Endpoint DLP as a location in a properly configured DLP policy and the Edge Chromium browser, the unallowed browsers that you've defined in these settings will be prevented from accessing the sensitive items that match your DLP policy controls.</span></span> <span data-ttu-id="82021-158">Au lieu de cela, les utilisateurs seront redirigés vers le Chromium Edge et le Chromium Edge, avec sa compréhension des restrictions imposées par DLP, peut bloquer ou restreindre les activités lorsque les conditions de la stratégie DLP sont réunies.</span><span class="sxs-lookup"><span data-stu-id="82021-158">Instead, users will be redirected to use Edge Chromium and Edge Chromium, with its understanding of DLP imposed restrictions, can block or restrict activities when the conditions in the DLP policy are met.</span></span>

<span data-ttu-id="82021-159">Pour utiliser cette restriction, vous devez configurer trois éléments importants :</span><span class="sxs-lookup"><span data-stu-id="82021-159">To use this restriction you’ll need to configure three important pieces:</span></span>

1. <span data-ttu-id="82021-160">Spécifier les emplacements ,services, domaines, adresses IP, avec lesquels vous ne souhaitez pas partager les éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="82021-160">Specify the places – services, domains, IP addresses – that you want to prevent sensitive items from being shared to.</span></span>

2. <span data-ttu-id="82021-161">Ajoutez les navigateurs qui ne sont pas autorisés à accéder à certains éléments sensibles lorsqu’une correspondance de la stratégie DLP se produit.</span><span class="sxs-lookup"><span data-stu-id="82021-161">Add the browsers that aren’t allowed to access certain sensitive items when a DLP policy match occurs.</span></span>

3. <span data-ttu-id="82021-162">Configurez les stratégies DLP pour définir les types d’éléments sensibles pour lesquels le téléchargement doit être limité à ces emplacements en activant **Télécharger vers les services Cloud** et **Accès à partir d’un navigateur non autorisé**.</span><span class="sxs-lookup"><span data-stu-id="82021-162">Configure DLP policies to define the kinds of sensitive items for which upload should be restricted to these places by turning on **Upload to cloud services** and **Access from unallowed browser**.</span></span>

<span data-ttu-id="82021-163">Vous pouvez continuer à ajouter de nouveaux services, applications et stratégies pour développer et augmenter vos restrictions afin de répondre aux besoins de votre entreprise et de protéger les données sensibles.</span><span class="sxs-lookup"><span data-stu-id="82021-163">You can continue to add new services, apps, and policies to extend and augment your restrictions to meet your business needs and protect sensitive data.</span></span> 

<span data-ttu-id="82021-164">Cette configuration vous permet de garantir la sécurité de vos données tout en évitant les restrictions inutiles qui empêchent les utilisateurs d’accéder aux éléments non sensibles et de les empêcher de les partager.</span><span class="sxs-lookup"><span data-stu-id="82021-164">This configuration will help ensure your data remains safe while also avoiding unnecessary restrictions that prevent or restrict users from accessing and sharing non-sensitive items.</span></span>

## <a name="endpoint-dlp-policy-scenarios"></a><span data-ttu-id="82021-165">Scénarios de stratégie DLP pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="82021-165">Endpoint DLP policy scenarios</span></span>

<span data-ttu-id="82021-166">Pour vous familiariser avec les fonctionnalités de point de terminaison DLP et la manière dont elles se trouvent dans les stratégies DLP, nous avons rassemblé certains scénarios que vous pouvez suivre.</span><span class="sxs-lookup"><span data-stu-id="82021-166">To help familiarize you with Endpoint DLP features and how they surface in DLP policies, we've put together some scenarios for you to follow.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82021-167">Ces scénarios de points de terminaison DLP ne sont pas les procédures officielles pour la création et le réglage des stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="82021-167">These Endpoint DLP scenarios are not the official procedures for creating and tuning DLP policies.</span></span> <span data-ttu-id="82021-168">Reportez-vous aux rubriques ci-dessous lorsque vous devez utiliser les stratégies DLP dans les situations générales suivantes :</span><span class="sxs-lookup"><span data-stu-id="82021-168">Refer to the below topics when you need to work with DLP policies in general situations:</span></span>

>- [<span data-ttu-id="82021-169">En savoir plus sur la prévention des pertes de données</span><span class="sxs-lookup"><span data-stu-id="82021-169">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)
>- [<span data-ttu-id="82021-170">Prise en main de la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="82021-170">Get started with the default DLP policy</span></span>](get-started-with-the-default-dlp-policy.md)
>- [<span data-ttu-id="82021-171">Création d’une stratégie DLP à partir d’un modèle</span><span class="sxs-lookup"><span data-stu-id="82021-171">Create a DLP policy from a template</span></span>](create-a-dlp-policy-from-a-template.md)
>- [<span data-ttu-id="82021-172">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="82021-172">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)

### <a name="scenario-1-create-a-policy-from-a-template-audit-only"></a><span data-ttu-id="82021-173">Scénario 1 : créer une stratégie à partir d’un modèle, audit uniquement</span><span class="sxs-lookup"><span data-stu-id="82021-173">Scenario 1: Create a policy from a template, audit only</span></span>

<span data-ttu-id="82021-174">Ces scénarios nécessitent que les appareils soient déjà intégrés et reportés dans l’Explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="82021-174">These scenarios require that you already have devices onboarded and reporting into Activity explorer.</span></span> <span data-ttu-id="82021-175">Si vous n’avez pas encore intégré d’appareils, consultez l’article [Prise en main de la protection contre la perte de données de point de terminaison](endpoint-dlp-getting-started.md).</span><span class="sxs-lookup"><span data-stu-id="82021-175">If you haven't onboarded devices yet, see [Get started with Endpoint data loss prevention](endpoint-dlp-getting-started.md).</span></span>

1. <span data-ttu-id="82021-176">Ouvrez la [page de protection contre la perte de données](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span><span class="sxs-lookup"><span data-stu-id="82021-176">Open the [Data loss prevention page](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span></span>

2. <span data-ttu-id="82021-177">Sélectionnez **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="82021-177">Choose **Create policy**.</span></span>

3. <span data-ttu-id="82021-178">Dans le cadre de ce scénario, sélectionnez **Confidentialité**, **Données d’informations d’identification personnelles (PII) pour les États-Unis** puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="82021-178">For this scenario, choose **Privacy**, then **U.S. Personally Identifiable Information (PII) Data** and choose **Next**.</span></span>

4. <span data-ttu-id="82021-179">Désactivez la case à cocher **État** pour tous les emplacements, sauf pour les **Appareils**.</span><span class="sxs-lookup"><span data-stu-id="82021-179">Toggle the **Status** field to off for all locations except **Devices**.</span></span> <span data-ttu-id="82021-180">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="82021-180">Choose **Next**.</span></span>

5. <span data-ttu-id="82021-181">Acceptez la sélection par défaut **Vérifier et personnaliser les paramètres du modèle**, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="82021-181">Accept the default **Review and customize settings from the template** selection and choose **Next**.</span></span>

6. <span data-ttu-id="82021-182">Acceptez les valeurs par défaut **Actions de protection** et choisissez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="82021-182">Accept the default **Protection actions** values and choose **Next**.</span></span>

7. <span data-ttu-id="82021-183">Sélectionnez **Audit ou restreindre les activités sur les appareils Windows** et laissez **Audit uniquement**.</span><span class="sxs-lookup"><span data-stu-id="82021-183">Select **Audit or restrict activities on Windows devices** and leave the actions set to **Audit only**.</span></span> <span data-ttu-id="82021-184">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="82021-184">Choose **Next**.</span></span>

8. <span data-ttu-id="82021-185">Accepter la valeur par défaut **Je veux tester le contenu tout d’abord** et choisir **Afficher les conseils de stratégie en mode test**.</span><span class="sxs-lookup"><span data-stu-id="82021-185">Accept the default **I'd like to test it out first** value and choose **Show policy tips while in test mode**.</span></span> <span data-ttu-id="82021-186">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="82021-186">Choose **Next**.</span></span>

9. <span data-ttu-id="82021-187">Passez en revue vos paramètres, puis sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="82021-187">Review your settings and choose **Submit**.</span></span>

10. <span data-ttu-id="82021-188">La nouvelle stratégie DLP s’affiche dans la liste de stratégies.</span><span class="sxs-lookup"><span data-stu-id="82021-188">The new DLP policy will appear in the policy list.</span></span>

11. <span data-ttu-id="82021-189">Consultez l’Explorateur d’activités pour les données des points de terminaison monitorés.</span><span class="sxs-lookup"><span data-stu-id="82021-189">Check Activity explorer for data from the monitored endpoints.</span></span> <span data-ttu-id="82021-190">Configurez le filtre d’emplacement pour les appareils et ajoutez la stratégie, puis filtrez par nom de stratégie pour afficher l’impact de cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="82021-190">Set the location filter for devices and add the policy, then filter by policy name to see the impact of this policy.</span></span> <span data-ttu-id="82021-191">Pour plus d’informations, voir [Prise en main de l’Explorateur d’activités](data-classification-activity-explorer.md) si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="82021-191">See, [Get started with activity explorer](data-classification-activity-explorer.md) if needed.</span></span>

12. <span data-ttu-id="82021-192">Essayez de partager un test qui contient du contenu qui déclenchera la condition de données d’informations d’identification personnelle (PII) américaine avec une personne extérieure à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="82021-192">Attempt to share a test that contains content that will trigger the U.S. Personally Identifiable Information (PII) Data condition with someone outside your organization.</span></span> <span data-ttu-id="82021-193">Cette opération doit déclencher la stratégie.</span><span class="sxs-lookup"><span data-stu-id="82021-193">This should trigger the policy.</span></span>

13. <span data-ttu-id="82021-194">Consultez l’Explorateur d’activités pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="82021-194">Check Activity explorer for the event.</span></span>

### <a name="scenario-2-modify-the-existing-policy-set-an-alert"></a><span data-ttu-id="82021-195">Scénario 2 : modifier la stratégie existante, créer une alerte</span><span class="sxs-lookup"><span data-stu-id="82021-195">Scenario 2: Modify the existing policy, set an alert</span></span>

1. <span data-ttu-id="82021-196">Ouvrir[Page de protection contre la perte de données](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span><span class="sxs-lookup"><span data-stu-id="82021-196">Open the [Data loss prevention page](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span></span>

2. <span data-ttu-id="82021-197">Sélectionnez la stratégie **Données d’informations d’identification personnelle (PII) pour les États-Unis** que vous avez créées dans le scénario 1.</span><span class="sxs-lookup"><span data-stu-id="82021-197">Choose the **U.S. Personally Identifiable Information (PII) Data** policy that you created in scenario 1.</span></span>

3. <span data-ttu-id="82021-198">Sélectionnez **Modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="82021-198">Choose **edit policy**.</span></span>

4. <span data-ttu-id="82021-199">Accédez à la page **Règles DLP avancées** et modifiez la **Faible quantité de contenu détectée pour les informations d’identification personnelle**.</span><span class="sxs-lookup"><span data-stu-id="82021-199">Go to the **Advanced DLP rules** page and edit the **Low volume of content detected U.S. Personally Identifiable Inf**.</span></span>

5. <span data-ttu-id="82021-200">Faites défiler vers le bas jusqu’à la section **Rapports d’incident** et configurez **Envoyer une alerte aux administrateurs lorsqu’une correspondance de règle se produit** sur **Activé**.</span><span class="sxs-lookup"><span data-stu-id="82021-200">Scroll down to the **Incident reports** section and set **Send an alert to admins when a rule match occurs** to **On**.</span></span> <span data-ttu-id="82021-201">Les alertes par courrier électronique sont envoyées automatiquement à l’administrateur et à toute autre personne que vous ajoutez à la liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="82021-201">Email alerts will be automatically sent to the administrator and anyone else you add to the list of recipients.</span></span> 

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="82021-202">![turn-on-incident-reports](../media/endpoint-dlp-2-using-dlp-incident-reports.png)</span><span class="sxs-lookup"><span data-stu-id="82021-202">![turn-on-incident-reports](../media/endpoint-dlp-2-using-dlp-incident-reports.png)</span></span>
   
6. <span data-ttu-id="82021-203">Dans le cadre de ce scénario, sélectionnez **Envoyer une alerte chaque fois qu’une activité correspond à la règle**.</span><span class="sxs-lookup"><span data-stu-id="82021-203">For the purposes of this scenario, choose **Send alert every time an activity matches the rule**.</span></span>

7. <span data-ttu-id="82021-204">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="82021-204">Choose **Save**.</span></span>

8. <span data-ttu-id="82021-205">Conservez tous vos paramètres précédents en choisissant **suivant** puis **Envoyer** les modifications apportées à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="82021-205">Retain all your previous settings by choosing **Next** and then **Submit** the policy changes.</span></span>

9. <span data-ttu-id="82021-206">Essayez de partager un test qui contient du contenu qui déclenchera la condition de données d’informations d’identification personnelle (PII) américaine avec une personne extérieure à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="82021-206">Attempt to share a test that contains content that will trigger the U.S. Personally Identifiable Information (PII) Data condition with someone outside your organization.</span></span> <span data-ttu-id="82021-207">Cette opération doit déclencher la stratégie.</span><span class="sxs-lookup"><span data-stu-id="82021-207">This should trigger the policy.</span></span>

10. <span data-ttu-id="82021-208">Consultez l’Explorateur d’activités pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="82021-208">Check Activity explorer for the event.</span></span>

### <a name="scenario-3-modify-the-existing-policy-block-the-action-with-allow-override"></a><span data-ttu-id="82021-209">Scénario 3 : modifier la stratégie existante, bloquer l’action avec l’option autoriser le remplacement</span><span class="sxs-lookup"><span data-stu-id="82021-209">Scenario 3: Modify the existing policy, block the action with allow override</span></span>

1. <span data-ttu-id="82021-210">Ouvrir[Page de protection contre la perte de données](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span><span class="sxs-lookup"><span data-stu-id="82021-210">Open the [Data loss prevention page](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span></span>

2. <span data-ttu-id="82021-211">Sélectionnez la stratégie **Données d’informations d’identification personnelle (PII) pour les États-Unis** que vous avez créées dans le scénario 1.</span><span class="sxs-lookup"><span data-stu-id="82021-211">Choose the **U.S. Personally Identifiable Information (PII) Data** policy that you created in scenario 1.</span></span>

3. <span data-ttu-id="82021-212">Sélectionnez **Modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="82021-212">Choose **edit policy**.</span></span>

4. <span data-ttu-id="82021-213">Accédez à la page **Règles DLP avancées** et modifiez la **Faible quantité de contenu détectée pour les informations d’identification personnelle**.</span><span class="sxs-lookup"><span data-stu-id="82021-213">Go to the **Advanced DLP rules** page and edit the **Low volume of content detected U.S. Personally Identifiable Inf**.</span></span>

5. <span data-ttu-id="82021-214">Faites défiler vers le bas jusqu’à la section **Audit ou restreindre les activités sur les appareils Windows** et pour chaque activité définissez l’action correspondante sur **Bloquer avec remplacement**.</span><span class="sxs-lookup"><span data-stu-id="82021-214">Scroll down to the **Audit or restrict activities on Windows device** section and for each activity set the corresponding action to  **Block with override**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="82021-215">![définir un blocage avec une action de remplacement](../media/endpoint-dlp-6-using-dlp-set-blocked-with-override.png)</span><span class="sxs-lookup"><span data-stu-id="82021-215">![set block with override action](../media/endpoint-dlp-6-using-dlp-set-blocked-with-override.png)</span></span>
   
6. <span data-ttu-id="82021-216">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="82021-216">Choose **Save**.</span></span>

7. <span data-ttu-id="82021-217">Répétez les étapes 4-7 pour **Quantité de contenu élevé détectée le fichier INF (INF) US**.</span><span class="sxs-lookup"><span data-stu-id="82021-217">Repeat steps 4-7 for the **High volume of content detected U.S. Personally Identifiable Inf**.</span></span>

8. <span data-ttu-id="82021-218">Conservez tous vos paramètres précédents en choisissant **suivant** puis **Envoyer** les modifications apportées à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="82021-218">Retain all your previous settings by choosing **Next** and then **Submit** the policy changes.</span></span>

9. <span data-ttu-id="82021-219">Essayez de partager un test qui contient du contenu qui déclenchera la condition de données d’informations d’identification personnelle (PII) américaine avec une personne extérieure à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="82021-219">Attempt to share a test that contains content that will trigger the U.S. Personally Identifiable Information (PII) Data condition with someone outside your organization.</span></span> <span data-ttu-id="82021-220">Cette opération doit déclencher la stratégie.</span><span class="sxs-lookup"><span data-stu-id="82021-220">This should trigger the policy.</span></span>

   <span data-ttu-id="82021-221">Une fenêtre contextuelle semblable à celle-ci s’affiche sur l’appareil client :</span><span class="sxs-lookup"><span data-stu-id="82021-221">You'll see a popup like this on the client device:</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="82021-222">![blocage de la notification de remplacement par le client dlp de point de terminaison](../media/endpoint-dlp-3-using-dlp-client-blocked-override-notification.png)</span><span class="sxs-lookup"><span data-stu-id="82021-222">![endpoint dlp client blocked override notification](../media/endpoint-dlp-3-using-dlp-client-blocked-override-notification.png)</span></span>

10. <span data-ttu-id="82021-223">Consultez l’Explorateur d’activités pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="82021-223">Check Activity explorer for the event.</span></span>

## <a name="see-also"></a><span data-ttu-id="82021-224">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82021-224">See also</span></span>

- [<span data-ttu-id="82021-225">Découvrir la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="82021-225">Learn about Endpoint data loss prevention</span></span>](endpoint-dlp-learn-about.md)
- [<span data-ttu-id="82021-226">Prise en main la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="82021-226">Get started with Endpoint data loss prevention</span></span>](endpoint-dlp-getting-started.md)
- [<span data-ttu-id="82021-227">En savoir plus sur la prévention des pertes de données</span><span class="sxs-lookup"><span data-stu-id="82021-227">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)
- [<span data-ttu-id="82021-228">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="82021-228">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="82021-229">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="82021-229">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="82021-230">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="82021-230">Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection/)
- <span data-ttu-id="82021-231">[Outils et méthodes d’intégration pour les appareils Windows 10](/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="82021-231">[Onboarding tools and methods for Windows 10 machines](/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints)</span></span>
- [<span data-ttu-id="82021-232">Abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="82021-232">Microsoft 365 subscription</span></span>](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1)
- [<span data-ttu-id="82021-233">Azure Active Directory (ADD) adhésion</span><span class="sxs-lookup"><span data-stu-id="82021-233">Azure Active Directory (AAD) joined</span></span>](/azure/active-directory/devices/concept-azure-ad-join)
- [<span data-ttu-id="82021-234">Télécharger le nouveau Microsoft Edge sur la base de chrome</span><span class="sxs-lookup"><span data-stu-id="82021-234">Download the new Microsoft Edge based on Chromium</span></span>](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium)
- [<span data-ttu-id="82021-235">Prise en main de la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="82021-235">Get started with the default DLP policy</span></span>](get-started-with-the-default-dlp-policy.md)
- [<span data-ttu-id="82021-236">Création d’une stratégie DLP à partir d’un modèle</span><span class="sxs-lookup"><span data-stu-id="82021-236">Create a DLP policy from a template</span></span>](create-a-dlp-policy-from-a-template.md)