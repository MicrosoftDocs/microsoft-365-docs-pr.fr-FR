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
ms.openlocfilehash: 531fd5506aeb255e261c3cce35473f1ddad2aa42
ms.sourcegitcommit: 1a9f0f878c045e1ddd59088ca2a94397605a242a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "49667809"
---
# <a name="using-endpoint-data-loss-prevention"></a><span data-ttu-id="cf534-103">Utilisation de la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="cf534-103">Using Endpoint data loss prevention</span></span>

<span data-ttu-id="cf534-104">Cet article décrit trois scénarios dans lesquels vous créez et modifiez une stratégie DLP qui utilise des appareils comme emplacement.</span><span class="sxs-lookup"><span data-stu-id="cf534-104">This article walks you through three scenarios where you create and modify a DLP policy that uses devices as a location.</span></span>

## <a name="dlp-settings"></a><span data-ttu-id="cf534-105">Paramètres DLP</span><span class="sxs-lookup"><span data-stu-id="cf534-105">DLP settings</span></span>

<span data-ttu-id="cf534-106">Avant de commencer, vous devez configurer vos paramètres DLP appliqués à toutes les stratégies DLP pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="cf534-106">Before you get started you should set up your DLP settings which are applied to all DLP policies for devices.</span></span> <span data-ttu-id="cf534-107">Vous devez les configurer si vous envisagez de créer des stratégies qui appliquent :</span><span class="sxs-lookup"><span data-stu-id="cf534-107">You must configure these if you intend to create policies that enforce:</span></span>

- <span data-ttu-id="cf534-108">restrictions de sortie dans le Cloud</span><span class="sxs-lookup"><span data-stu-id="cf534-108">cloud egress restrictions</span></span>
- <span data-ttu-id="cf534-109">restrictions relatives aux applications non autorisées</span><span class="sxs-lookup"><span data-stu-id="cf534-109">unallowed apps restrictions</span></span>

<span data-ttu-id="cf534-110">Ou</span><span class="sxs-lookup"><span data-stu-id="cf534-110">Or</span></span>

- <span data-ttu-id="cf534-111">Si vous souhaitez exclure l’analyse des chemins d’accès aux fichiers bruyants</span><span class="sxs-lookup"><span data-stu-id="cf534-111">If you want to exclude noisy file paths from monitoring</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="cf534-112">![Paramètres DLP](../media/endpoint-dlp-1-using-dlp-settings.png)</span><span class="sxs-lookup"><span data-stu-id="cf534-112">![DLP settings](../media/endpoint-dlp-1-using-dlp-settings.png)</span></span>

### <a name="file-path-exclusions"></a><span data-ttu-id="cf534-113">Exclusions de chemin d’accès de fichier</span><span class="sxs-lookup"><span data-stu-id="cf534-113">File path exclusions</span></span>

<span data-ttu-id="cf534-114">Vous pouvez exclure certains chemins de la surveillance DLP, des alertes DLP et de l’application de stratégie DLP sur vos appareils, car ils sont trop bruyants ou ne contiennent pas les fichiers qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="cf534-114">You may want to exclude certain paths from DLP monitoring, DLP alerting, and DLP policy enforcement on your devices because they are too noisy or don’t contain files you are interested in.</span></span> <span data-ttu-id="cf534-115">Les fichiers stockés dans ces emplacements ne seront pas audités et tous les fichiers créés ou modifiés dans ces emplacements ne seront pas soumis à l’application de stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="cf534-115">Files in those locations will not be audited and any files that are created or modified in those locations will not be subject to DLP policy enforcement.</span></span> <span data-ttu-id="cf534-116">Vous pouvez configurer les exclusions de chemin d’accès dans les paramètres DLP.</span><span class="sxs-lookup"><span data-stu-id="cf534-116">You can configure path exclusions in DLP settings.</span></span>

<span data-ttu-id="cf534-117">Vous pouvez utiliser cette logique pour construire vos chemins d’exclusion :</span><span class="sxs-lookup"><span data-stu-id="cf534-117">You can use this logic to construct your exclusion paths:</span></span>

- <span data-ttu-id="cf534-118">Chemin d’accès de fichier valide se terminant par « \ », ce qui signifie uniquement les fichiers directement sous dossier.</span><span class="sxs-lookup"><span data-stu-id="cf534-118">Valid file path that ends with ‘\’, which means only files directly under folder.</span></span> <br/><span data-ttu-id="cf534-119">Par exemple: C:\Temp</span><span class="sxs-lookup"><span data-stu-id="cf534-119">For example: C:\Temp</span></span>\

- <span data-ttu-id="cf534-120">Chemin d’accès de fichier valide se terminant par « \* », ce qui signifie uniquement les sous-dossiers directement sous dossier.</span><span class="sxs-lookup"><span data-stu-id="cf534-120">Valid file path that ends with ‘\*’, which means only files under sub-folders, besides the files directly under the folder.</span></span> <br/><span data-ttu-id="cf534-121">Par exemple: C:\Temp\*</span><span class="sxs-lookup"><span data-stu-id="cf534-121">For example: C:\Temp\*</span></span>

- <span data-ttu-id="cf534-122">Chemin d’accès de fichier valide se terminant par « \ » ou «\*», ce qui signifie uniquement les fichiers directement sous dossier et tous les sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="cf534-122">Valid file path that ends without ‘\’ or ‘\*’, which means all files directly under folder and all sub-folders.</span></span> <br/><span data-ttu-id="cf534-123">Par exemple: C:\Temp</span><span class="sxs-lookup"><span data-stu-id="cf534-123">For example: C:\Temp</span></span>

- <span data-ttu-id="cf534-124">Un chemin d’accès avec un caractère générique entre' \ 'de chaque côté.</span><span class="sxs-lookup"><span data-stu-id="cf534-124">A path with wildcard between ‘\’ from each side.</span></span> <br/><span data-ttu-id="cf534-125">Par exemple : C:\Users\*\Desktop</span><span class="sxs-lookup"><span data-stu-id="cf534-125">For example: C:\Users\*\Desktop</span></span>\

- <span data-ttu-id="cf534-126">Un chemin d’accès comportant le caractère générique entre « \» de chaque côté et «(nombre)» pour indiquer le nombre exact de sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="cf534-126">A path with wildcard between ‘\’ from each side and with ‘(number)’ to give exact number of subfolders.</span></span> <br/><span data-ttu-id="cf534-127">Par exemple : C:\Users\*(1) \Downloads</span><span class="sxs-lookup"><span data-stu-id="cf534-127">For example: C:\Users\*(1)\Downloads</span></span>\

- <span data-ttu-id="cf534-128">Un chemin d’accès avec des variables d’environnement système.</span><span class="sxs-lookup"><span data-stu-id="cf534-128">A path with SYSTEM environment variables.</span></span> <br/><span data-ttu-id="cf534-129">Par exemple :%SystemDrive%\Test\*</span><span class="sxs-lookup"><span data-stu-id="cf534-129">For example: %SystemDrive%\Test\*</span></span>

- <span data-ttu-id="cf534-130">Un mélange de tous les éléments ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="cf534-130">A mix of all the above.</span></span> <br/><span data-ttu-id="cf534-131">Par exemple :%SystemDrive%\Users\*\Documents\*(2) \Sub</span><span class="sxs-lookup"><span data-stu-id="cf534-131">For example: %SystemDrive%\Users\*\Documents\*(2)\Sub</span></span>\

### <a name="unallowed-apps"></a><span data-ttu-id="cf534-132">Applications non autorisées</span><span class="sxs-lookup"><span data-stu-id="cf534-132">Unallowed apps</span></span>

<span data-ttu-id="cf534-133">Lorsque le paramètre **Accès par des applications et des navigateurs non autorisés** d’une stratégie est activé, et que les utilisateurs tentent d’utiliser ces applications pour accéder à un fichier protégé, l’activité est autorisée, bloquée, ou bloquée mais les utilisateurs peuvent annuler la restriction.</span><span class="sxs-lookup"><span data-stu-id="cf534-133">When a policy's **Access by unallowed apps and browsers** setting is turned on and users attempt to use these apps to access a protected file, the activity will be allowed, blocked, or blocked but users can override the restriction.</span></span> <span data-ttu-id="cf534-134">Toutes les activités sont auditées et disponibles pour révision dans l’Explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="cf534-134">All activity is audited and available to review in activity explorer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf534-135">N’incluez pas le chemin d’accès du fichier exécutable, mais uniquement le nom du fichier exécutable (par exemple, browser.exe).</span><span class="sxs-lookup"><span data-stu-id="cf534-135">Do not include the path to the executable, but only the executable name (such as browser.exe).</span></span>


### <a name="browser-and-domain-restrictions"></a><span data-ttu-id="cf534-136">Restrictions de navigateur et de domaine :</span><span class="sxs-lookup"><span data-stu-id="cf534-136">Browser and domain restrictions</span></span>
<span data-ttu-id="cf534-137">Empêchez les fichiers sensibles, qui correspondent à vos stratégies, d’être partagés avec des domaines de service cloud sans restriction.</span><span class="sxs-lookup"><span data-stu-id="cf534-137">Restrict sensitive files that match your policies from being shared with unrestricted cloud service domains.</span></span>

#### <a name="service-domains"></a><span data-ttu-id="cf534-138">Domaines de service</span><span class="sxs-lookup"><span data-stu-id="cf534-138">Service domains</span></span>

<span data-ttu-id="cf534-139">Vous pouvez déterminer si les fichiers sensibles protégés par vos stratégies peuvent être téléchargés vers des domaines de service spécifiques à partir de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cf534-139">You can control whether sensitive files protected by your policies can be uploaded to specific service domains from Microsoft Edge.</span></span>

<span data-ttu-id="cf534-140">Si le mode de liste est paramétré sur **Bloquer**, l’utilisateur ne peut pas télécharger des éléments sensibles dans ces domaines.</span><span class="sxs-lookup"><span data-stu-id="cf534-140">If the list mode is set to **Block**, then user will not be able to upload sensitive items to those domains.</span></span> <span data-ttu-id="cf534-141">Lorsqu’une action de téléchargement est bloquée parce qu’un élément correspond à une stratégie DLP, DLP génère un avertissement ou bloque le téléchargement de l’élément sensible.</span><span class="sxs-lookup"><span data-stu-id="cf534-141">When an upload action is blocked because an item matches a DLP policy, DLP will either generate a warning or block the upload of the sensitive item.</span></span>

<span data-ttu-id="cf534-142">Si le mode liste est défini sur **Autoriser**, les utilisateurs pourront télécharger des éléments sensibles \**_uniquement_* _ vers ces domaines, et l’accès au téléchargement vers tous les autres domaines n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="cf534-142">If the list mode is set to **Allow**, then users will be able to upload sensitive items \**_only_* _ to those domains, and upload access to all other domains is not allowed.</span></span>

#### <a name="unallowed-browsers"></a><span data-ttu-id="cf534-143">Navigateurs non autorisés</span><span class="sxs-lookup"><span data-stu-id="cf534-143">Unallowed browsers</span></span>

<span data-ttu-id="cf534-144">Vous ajoutez des navigateurs, identifiés par leurs noms de exécutables, qui ne peuvent pas accéder à des fichiers qui remplissent les conditions d’une stratégie DLP appliquée dans laquelle la restriction de chargement vers les services Cloud est définie sur bloquer ou annuler le blocage.</span><span class="sxs-lookup"><span data-stu-id="cf534-144">You add browsers, identified by their executable names, that will be blocked from accessing files that match the conditions of an enforced a DLP policy where the upload to cloud services restriction is set to block or block override.</span></span> <span data-ttu-id="cf534-145">Lorsque ces navigateurs ne peuvent pas accéder à un fichier, les utilisateurs finaux voient s’afficher une notification leur demandant d’ouvrir le fichier via le Chromium Edge.</span><span class="sxs-lookup"><span data-stu-id="cf534-145">When these browsers are blocked from accessing a file, the end users will see a toast notification asking them to open the file through Edge Chromium.</span></span>


## <a name="tying-dlp-settings-together"></a><span data-ttu-id="cf534-146">Lier les paramètres DLP ensemble</span><span class="sxs-lookup"><span data-stu-id="cf534-146">Tying DLP settings together</span></span>

<span data-ttu-id="cf534-147">Avec les points de terminaison DLP et le navigateur Chromium Edge, vous pouvez limiter le partage involontaire des éléments sensibles aux applications et services Cloud non autorisés.</span><span class="sxs-lookup"><span data-stu-id="cf534-147">With Endpoint DLP and Edge Chromium Web browser, you can restrict unintentional sharing of sensitive items to unallowed cloud apps and services.</span></span> <span data-ttu-id="cf534-148">Le Chromium Edge comprend les conditions dans lesquelles un élément est limité par une stratégie DLP de point de terminaison et applique les restrictions d’accès.</span><span class="sxs-lookup"><span data-stu-id="cf534-148">Edge Chromium understands when an item is restricted by an Endpoint DLP policy and enforces access restrictions.</span></span>

<span data-ttu-id="cf534-149">Lorsque vous utilisez la fonctionnalité point de terminaison DLP comme emplacement dans une stratégie DLP correctement configurée et le navigateur Chromium Edge, les navigateurs non autorisés que vous avez définis dans ces paramètres ne pourront pas accéder aux éléments sensibles qui correspondent à vos contrôles de stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="cf534-149">When you use Endpoint DLP as a location in a properly configured DLP policy and the Edge Chromium browser, the unallowed browsers that you've defined in these settings will be prevented from accessing the sensitive items that match your DLP policy controls.</span></span> <span data-ttu-id="cf534-150">Au lieu de cela, les utilisateurs seront redirigés vers le Chromium Edge et le Chromium Edge, avec sa compréhension des restrictions imposées par DLP, peut bloquer ou restreindre les activités lorsque les conditions de la stratégie DLP sont réunies.</span><span class="sxs-lookup"><span data-stu-id="cf534-150">Instead, users will be redirected to use Edge Chromium and Edge Chromium, with its understanding of DLP imposed restrictions, can block or restrict activities when the conditions in the DLP policy are met.</span></span>

<span data-ttu-id="cf534-151">Pour utiliser cette restriction, vous devez configurer trois éléments importants :</span><span class="sxs-lookup"><span data-stu-id="cf534-151">To use this restriction you’ll need to configure three important pieces:</span></span>

1. <span data-ttu-id="cf534-152">Spécifier les emplacements ,services, domaines, adresses IP, avec lesquels vous ne souhaitez pas partager les éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="cf534-152">Specify the places – services, domains, IP addresses – that you want to prevent sensitive items from being shared to.</span></span>

2. <span data-ttu-id="cf534-153">Ajoutez les navigateurs qui ne sont pas autorisés à accéder à certains éléments sensibles lorsqu’une correspondance de la stratégie DLP se produit.</span><span class="sxs-lookup"><span data-stu-id="cf534-153">Add the browsers that aren’t allowed to access certain sensitive items when a DLP policy match occurs.</span></span>

3. <span data-ttu-id="cf534-154">Configurez les stratégies DLP pour définir les types d’éléments sensibles pour lesquels le téléchargement doit être limité à ces emplacements en activant les options *Télécharger vers les services cloud* et **Accès à partir d’un navigateur non autorisé**.</span><span class="sxs-lookup"><span data-stu-id="cf534-154">Configure DLP policies to define the kinds of sensitive items for which upload should be restricted to these places by turning on _ *Upload to cloud services*\* and **Access from unallowed browser**.</span></span>

<span data-ttu-id="cf534-155">Vous pouvez continuer à ajouter de nouveaux services, applications et stratégies pour développer et augmenter vos restrictions afin de répondre aux besoins de votre entreprise et de protéger les données sensibles.</span><span class="sxs-lookup"><span data-stu-id="cf534-155">You can continue to add new services, apps, and policies to extend and augment your restrictions to meet your business needs and protect sensitive data.</span></span> 

<span data-ttu-id="cf534-156">Cette configuration vous permet de garantir la sécurité de vos données tout en évitant les restrictions inutiles qui empêchent les utilisateurs d’accéder aux éléments non sensibles et de les empêcher de les partager.</span><span class="sxs-lookup"><span data-stu-id="cf534-156">This configuration will help ensure your data remains safe while also avoiding unnecessary restrictions that prevent or restrict users from accessing and sharing non-sensitive items.</span></span>

## <a name="endpoint-dlp-policy-scenarios"></a><span data-ttu-id="cf534-157">Scénarios de stratégie DLP pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="cf534-157">Endpoint DLP policy scenarios</span></span>

<span data-ttu-id="cf534-158">Pour vous familiariser avec les fonctionnalités de point de terminaison DLP et la manière dont elles se trouvent dans les stratégies DLP, nous avons rassemblé certains scénarios que vous pouvez suivre.</span><span class="sxs-lookup"><span data-stu-id="cf534-158">To help familiarize you with Endpoint DLP features and how they surface in DLP policies, we've put together some scenarios for you to follow.</span></span> <span data-ttu-id="cf534-159">Tout le contenu de point de terminaison DLP sera affecté au contenu DLP principal lorsque le point de terminaison DLP est disponible en général.</span><span class="sxs-lookup"><span data-stu-id="cf534-159">All the Endpoint DLP content will be folded in to the main DLP content set when Endpoint DLP becomes generally available.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf534-160">Ces scénarios de points de terminaison DLP ne sont pas les procédures officielles pour la création et le réglage des stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="cf534-160">These Endpoint DLP scenarios are not the official procedures for creating and tuning DLP policies.</span></span> <span data-ttu-id="cf534-161">Reportez-vous aux rubriques ci-dessous lorsque vous devez utiliser les stratégies DLP dans les situations générales suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf534-161">Refer to the below topics when you need to work with DLP policies in general situations:</span></span>
>- [<span data-ttu-id="cf534-162">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="cf534-162">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
>- [<span data-ttu-id="cf534-163">Prise en main de la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="cf534-163">Get started with the default DLP policy</span></span>](get-started-with-the-default-dlp-policy.md)
>- [<span data-ttu-id="cf534-164">Création d’une stratégie DLP à partir d’un modèle</span><span class="sxs-lookup"><span data-stu-id="cf534-164">Create a DLP policy from a template</span></span>](create-a-dlp-policy-from-a-template.md)
>- [<span data-ttu-id="cf534-165">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="cf534-165">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)

### <a name="scenario-1-create-a-policy-from-a-template-audit-only"></a><span data-ttu-id="cf534-166">Scénario 1 : créer une stratégie à partir d’un modèle, audit uniquement</span><span class="sxs-lookup"><span data-stu-id="cf534-166">Scenario 1: Create a policy from a template, audit only</span></span>

<span data-ttu-id="cf534-167">Ces scénarios nécessitent que les appareils soient déjà intégrés et reportés dans l’Explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="cf534-167">These scenarios require that you already have devices onboarded and reporting into Activity explorer.</span></span> <span data-ttu-id="cf534-168">Si vous n’avez pas encore intégré d’appareils, consultez l’article [Prise en main de la protection contre la perte de données de point de terminaison](endpoint-dlp-getting-started.md).</span><span class="sxs-lookup"><span data-stu-id="cf534-168">If you haven't onboarded devices yet, see [Get started with Endpoint data loss prevention](endpoint-dlp-getting-started.md).</span></span>

1. <span data-ttu-id="cf534-169">Ouvrez la [page de protection contre la perte de données](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span><span class="sxs-lookup"><span data-stu-id="cf534-169">Open the [Data loss prevention page](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span></span>

2. <span data-ttu-id="cf534-170">Sélectionnez **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cf534-170">Choose **Create policy**.</span></span>

3. <span data-ttu-id="cf534-171">Dans le cadre de ce scénario, sélectionnez **Confidentialité**, **Données d’informations d’identification personnelles (PII) pour les États-Unis** puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf534-171">For this scenario, choose **Privacy**, then **U.S. Personally Identifiable Information (PII) Data** and choose **Next**.</span></span>

4. <span data-ttu-id="cf534-172">Désactivez la case à cocher **État** pour tous les emplacements, sauf pour les **Appareils**.</span><span class="sxs-lookup"><span data-stu-id="cf534-172">Toggle the **Status** field to off for all locations except **Devices**.</span></span> <span data-ttu-id="cf534-173">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf534-173">Choose **Next**.</span></span>

5. <span data-ttu-id="cf534-174">Acceptez la sélection par défaut **Vérifier et personnaliser les paramètres du modèle**, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf534-174">Accept the default **Review and customize settings from the template** selection and choose **Next**.</span></span>

6. <span data-ttu-id="cf534-175">Acceptez les valeurs par défaut **Actions de protection** et choisissez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf534-175">Accept the default **Protection actions** values and choose **Next**.</span></span>

7. <span data-ttu-id="cf534-176">Sélectionnez **Audit ou restreindre les activités sur les appareils Windows** et laissez **Audit uniquement**.</span><span class="sxs-lookup"><span data-stu-id="cf534-176">Select **Audit or restrict activities on Windows devices** and leave the actions set to **Audit only**.</span></span> <span data-ttu-id="cf534-177">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf534-177">Choose **Next**.</span></span>

8. <span data-ttu-id="cf534-178">Accepter la valeur par défaut **Je veux tester le contenu tout d’abord** et choisir **Afficher les conseils de stratégie en mode test**.</span><span class="sxs-lookup"><span data-stu-id="cf534-178">Accept the default **I'd like to test it out first** value and choose **Show policy tips while in test mode**.</span></span> <span data-ttu-id="cf534-179">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf534-179">Choose **Next**.</span></span>

9. <span data-ttu-id="cf534-180">Passez en revue vos paramètres, puis sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="cf534-180">Review your settings and choose **Submit**.</span></span>

10. <span data-ttu-id="cf534-181">La nouvelle stratégie DLP s’affiche dans la liste de stratégies.</span><span class="sxs-lookup"><span data-stu-id="cf534-181">The new DLP policy will appear in the policy list.</span></span>

11. <span data-ttu-id="cf534-182">Consultez l’Explorateur d’activités pour les données des points de terminaison monitorés.</span><span class="sxs-lookup"><span data-stu-id="cf534-182">Check Activity explorer for data from the monitored endpoints.</span></span> <span data-ttu-id="cf534-183">Configurez le filtre d’emplacement pour les appareils et ajoutez la stratégie, puis filtrez par nom de stratégie pour afficher l’impact de cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="cf534-183">Set the location filter for devices and add the policy, then filter by policy name to see the impact of this policy.</span></span> <span data-ttu-id="cf534-184">Pour plus d’informations, voir [Prise en main de l’Explorateur d’activités](data-classification-activity-explorer.md) si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="cf534-184">See, [Get started with activity explorer](data-classification-activity-explorer.md) if needed.</span></span>

12. <span data-ttu-id="cf534-185">Essayez de partager un test qui contient du contenu qui déclenchera la condition de données d’informations d’identification personnelle (PII) américaine avec une personne extérieure à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cf534-185">Attempt to share a test that contains content that will trigger the U.S. Personally Identifiable Information (PII) Data condition with someone outside your organization.</span></span> <span data-ttu-id="cf534-186">Cette opération doit déclencher la stratégie.</span><span class="sxs-lookup"><span data-stu-id="cf534-186">This should trigger the policy.</span></span>

13. <span data-ttu-id="cf534-187">Consultez l’Explorateur d’activités pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="cf534-187">Check Activity explorer for the event.</span></span>

### <a name="scenario-2-modify-the-existing-policy-set-an-alert"></a><span data-ttu-id="cf534-188">Scénario 2 : modifier la stratégie existante, créer une alerte</span><span class="sxs-lookup"><span data-stu-id="cf534-188">Scenario 2: Modify the existing policy, set an alert</span></span>

1. <span data-ttu-id="cf534-189">Ouvrir[Page de protection contre la perte de données](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span><span class="sxs-lookup"><span data-stu-id="cf534-189">Open the [Data loss prevention page](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span></span>

2. <span data-ttu-id="cf534-190">Sélectionnez la stratégie **Données d’informations d’identification personnelle (PII) pour les États-Unis** que vous avez créées dans le scénario 1.</span><span class="sxs-lookup"><span data-stu-id="cf534-190">Choose the **U.S. Personally Identifiable Information (PII) Data** policy that you created in scenario 1.</span></span>

3. <span data-ttu-id="cf534-191">Sélectionnez **Modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cf534-191">Choose **edit policy**.</span></span>

4. <span data-ttu-id="cf534-192">Accédez à la page **Règles DLP avancées** et modifiez la **Faible quantité de contenu détectée pour les informations d’identification personnelle**.</span><span class="sxs-lookup"><span data-stu-id="cf534-192">Go to the **Advanced DLP rules** page and edit the **Low volume of content detected U.S. Personally Identifiable Inf**.</span></span>

5. <span data-ttu-id="cf534-193">Faites défiler vers le bas jusqu’à la section **Rapports d’incident** et configurez **Envoyer une alerte aux administrateurs lorsqu’une correspondance de règle se produit** sur **Activé**.</span><span class="sxs-lookup"><span data-stu-id="cf534-193">Scroll down to the **Incident reports** section and set **Send an alert to admins when a rule match occurs** to **On**.</span></span> <span data-ttu-id="cf534-194">Les alertes par courrier électronique sont envoyées automatiquement à l’administrateur et à toute autre personne que vous ajoutez à la liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="cf534-194">Email alerts will be automatically sent to the administrator and anyone else you add to the list of recipients.</span></span> 

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="cf534-195">![turn-on-incident-reports](../media/endpoint-dlp-2-using-dlp-incident-reports.png)</span><span class="sxs-lookup"><span data-stu-id="cf534-195">![turn-on-incident-reports](../media/endpoint-dlp-2-using-dlp-incident-reports.png)</span></span>
   
6. <span data-ttu-id="cf534-196">Dans le cadre de ce scénario, sélectionnez **Envoyer une alerte chaque fois qu’une activité correspond à la règle**.</span><span class="sxs-lookup"><span data-stu-id="cf534-196">For the purposes of this scenario, choose **Send alert every time an activity matches the rule**.</span></span>

7. <span data-ttu-id="cf534-197">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf534-197">Choose **Save**.</span></span>

8. <span data-ttu-id="cf534-198">Conservez tous vos paramètres précédents en choisissant **suivant** puis **Envoyer** les modifications apportées à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="cf534-198">Retain all your previous settings by choosing **Next** and then **Submit** the policy changes.</span></span>

9. <span data-ttu-id="cf534-199">Essayez de partager un test qui contient du contenu qui déclenchera la condition de données d’informations d’identification personnelle (PII) américaine avec une personne extérieure à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cf534-199">Attempt to share a test that contains content that will trigger the U.S. Personally Identifiable Information (PII) Data condition with someone outside your organization.</span></span> <span data-ttu-id="cf534-200">Cette opération doit déclencher la stratégie.</span><span class="sxs-lookup"><span data-stu-id="cf534-200">This should trigger the policy.</span></span>

10. <span data-ttu-id="cf534-201">Consultez l’Explorateur d’activités pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="cf534-201">Check Activity explorer for the event.</span></span>

### <a name="scenario-3-modify-the-existing-policy-block-the-action-with-allow-override"></a><span data-ttu-id="cf534-202">Scénario 3 : modifier la stratégie existante, bloquer l’action avec l’option autoriser le remplacement</span><span class="sxs-lookup"><span data-stu-id="cf534-202">Scenario 3: Modify the existing policy, block the action with allow override</span></span>

1. <span data-ttu-id="cf534-203">Ouvrir[Page de protection contre la perte de données](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span><span class="sxs-lookup"><span data-stu-id="cf534-203">Open the [Data loss prevention page](https://compliance.microsoft.com/datalossprevention?viewid=policies).</span></span>

2. <span data-ttu-id="cf534-204">Sélectionnez la stratégie **Données d’informations d’identification personnelle (PII) pour les États-Unis** que vous avez créées dans le scénario 1.</span><span class="sxs-lookup"><span data-stu-id="cf534-204">Choose the **U.S. Personally Identifiable Information (PII) Data** policy that you created in scenario 1.</span></span>

3. <span data-ttu-id="cf534-205">Sélectionnez **Modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cf534-205">Choose **edit policy**.</span></span>

4. <span data-ttu-id="cf534-206">Accédez à la page **Règles DLP avancées** et modifiez la **Faible quantité de contenu détectée pour les informations d’identification personnelle**.</span><span class="sxs-lookup"><span data-stu-id="cf534-206">Go to the **Advanced DLP rules** page and edit the **Low volume of content detected U.S. Personally Identifiable Inf**.</span></span>

5. <span data-ttu-id="cf534-207">Faites défiler vers le bas jusqu’à la section **Audit ou restreindre les activités sur les appareils Windows** et pour chaque activité définissez l’action correspondante sur **Bloquer avec remplacement**.</span><span class="sxs-lookup"><span data-stu-id="cf534-207">Scroll down to the **Audit or restrict activities on Windows device** section and for each activity set the corresponding action to  **Block with override**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="cf534-208">![définir un blocage avec une action de remplacement](../media/endpoint-dlp-6-using-dlp-set-blocked-with-override.png)</span><span class="sxs-lookup"><span data-stu-id="cf534-208">![set block with override action](../media/endpoint-dlp-6-using-dlp-set-blocked-with-override.png)</span></span>
   
6. <span data-ttu-id="cf534-209">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf534-209">Choose **Save**.</span></span>

7. <span data-ttu-id="cf534-210">Répétez les étapes 4-7 pour **Quantité de contenu élevé détectée le fichier INF (INF) US**.</span><span class="sxs-lookup"><span data-stu-id="cf534-210">Repeat steps 4-7 for the **High volume of content detected U.S. Personally Identifiable Inf**.</span></span>

8. <span data-ttu-id="cf534-211">Conservez tous vos paramètres précédents en choisissant **suivant** puis **Envoyer** les modifications apportées à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="cf534-211">Retain all your previous settings by choosing **Next** and then **Submit** the policy changes.</span></span>

9. <span data-ttu-id="cf534-212">Essayez de partager un test qui contient du contenu qui déclenchera la condition de données d’informations d’identification personnelle (PII) américaine avec une personne extérieure à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cf534-212">Attempt to share a test that contains content that will trigger the U.S. Personally Identifiable Information (PII) Data condition with someone outside your organization.</span></span> <span data-ttu-id="cf534-213">Cette opération doit déclencher la stratégie.</span><span class="sxs-lookup"><span data-stu-id="cf534-213">This should trigger the policy.</span></span>

   <span data-ttu-id="cf534-214">Une fenêtre contextuelle semblable à celle-ci s’affiche sur l’appareil client :</span><span class="sxs-lookup"><span data-stu-id="cf534-214">You'll see a popup like this on the client device:</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="cf534-215">![blocage de la notification de remplacement par le client dlp de point de terminaison](../media/endpoint-dlp-3-using-dlp-client-blocked-override-notification.png)</span><span class="sxs-lookup"><span data-stu-id="cf534-215">![endpoint dlp client blocked override notification](../media/endpoint-dlp-3-using-dlp-client-blocked-override-notification.png)</span></span>

10. <span data-ttu-id="cf534-216">Consultez l’Explorateur d’activités pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="cf534-216">Check Activity explorer for the event.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf534-217">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf534-217">See also</span></span>

- [<span data-ttu-id="cf534-218">Découvrir la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="cf534-218">Learn about Endpoint data loss prevention</span></span>](endpoint-dlp-learn-about.md)
- [<span data-ttu-id="cf534-219">Prise en main la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="cf534-219">Get started with Endpoint data loss prevention</span></span>](endpoint-dlp-getting-started.md)
- [<span data-ttu-id="cf534-220">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="cf534-220">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="cf534-221">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="cf534-221">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="cf534-222">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="cf534-222">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="cf534-223">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="cf534-223">Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection/)
- <span data-ttu-id="cf534-224">[Outils et méthodes d’intégration pour les appareils Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="cf534-224">[Onboarding tools and methods for Windows 10 machines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints)</span></span>
- [<span data-ttu-id="cf534-225">Abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cf534-225">Microsoft 365 subscription</span></span>](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1)
- [<span data-ttu-id="cf534-226">Azure Active Directory (ADD) adhésion</span><span class="sxs-lookup"><span data-stu-id="cf534-226">Azure Active Directory (AAD) joined</span></span>](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join)
- [<span data-ttu-id="cf534-227">Télécharger le nouveau Microsoft Edge sur la base de chrome</span><span class="sxs-lookup"><span data-stu-id="cf534-227">Download the new Microsoft Edge based on Chromium</span></span>](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium)
- [<span data-ttu-id="cf534-228">Prise en main de la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="cf534-228">Get started with the default DLP policy</span></span>](get-started-with-the-default-dlp-policy.md)
- [<span data-ttu-id="cf534-229">Création d’une stratégie DLP à partir d’un modèle</span><span class="sxs-lookup"><span data-stu-id="cf534-229">Create a DLP policy from a template</span></span>](create-a-dlp-policy-from-a-template.md)
