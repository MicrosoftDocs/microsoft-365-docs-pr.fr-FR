---
title: En savoir plus sur le scanneur local de protection contre la perte de données Microsoft 365 (préversion)
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: conceptual
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MET150
description: Le scanneur local de protection contre la perte de données Microsoft 365 en local étend la surveillance des activités sur fichier et des actions de protection pour les partages de fichiers locaux, pour les dossiers locaux et les bibliothèques de documents SharePoint. Le scanneur Azure Information Protection (AIP) analyse, puis protège les fichiers.
ms.openlocfilehash: 996de5ea640a16ef2a250830d7167aa316b54a21
ms.sourcegitcommit: 070724118be25cd83418d2a56863da95582dae65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "50417358"
---
# <a name="learn-about-the-microsoft-365-data-loss-prevention-on-premises-scanner-preview"></a><span data-ttu-id="8c042-104">En savoir plus sur le scanneur local de protection contre la perte de données Microsoft 365 (préversion)</span><span class="sxs-lookup"><span data-stu-id="8c042-104">Learn about the Microsoft 365 data loss prevention on-premises scanner (preview)</span></span>

<span data-ttu-id="8c042-105">Le scanneur de protection contre la perte de données Microsoft Points de terminaison Protection contre la perte de données (Endpoint DLP) fait partie de la suite de fonctionnalités de protection contre la perte de données (DLP) Microsoft 365 que vous pouvez utiliser pour découvrir, puis protéger les éléments sensibles dans les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8c042-105">Microsoft data loss prevention on-premises scanner is part of the Microsoft 365 data loss prevention (DLP) suite of features that you can use to discover and protect sensitive items across Microsoft 365 services.</span></span> <span data-ttu-id="8c042-106">Si vous souhaitez en savoir plus sur les offres DLP de Microsoft, veuillez consulter la rubrique [Vue d’ensemble de la protection contre la perte de données](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8c042-106">For more information about all of Microsoft’s DLP offerings, see [Overview of data loss prevention](data-loss-prevention-policies.md).</span></span>

<span data-ttu-id="8c042-107">Le **scanneur local de protection contre la perte de données** analyse les données locales au repos dans les partages de fichiers, ainsi que dans les dossiers et bibliothèques de documents SharePoint pour y rechercher les éléments sensibles. En cas de fuite, ces éléments constitueraient un risque pour votre organisation ou un risque de violation de la stratégie de conformité.</span><span class="sxs-lookup"><span data-stu-id="8c042-107">The **DLP on-premises scanner** crawls on-premises data-at-rest in file shares and SharePoint document libraries and folders for sensitive items that, if leaked, would pose a risk to your organization or pose a risk of compliance policy violation.</span></span> <span data-ttu-id="8c042-108">Ainsi, vous bénéficiez de la visibilité et du contrôle dont vous avez besoin pour garantir une utilisation et une protection correctes de ces éléments, puis éviter tout comportement risqué susceptible de les compromettre.</span><span class="sxs-lookup"><span data-stu-id="8c042-108">This gives you the visibility and control you need to ensure that sensitive items are used and protected properly, and to help prevent risky behavior that might compromise them.</span></span> <span data-ttu-id="8c042-109">Le scanneur local de protection contre la perte de données détecte les informations sensibles à l’aide de types d’informations [intégrées](sensitive-information-type-entity-definitions.md) ou [sensibles personnalisées](create-a-custom-sensitive-information-type.md), d’[étiquettes de niveau de](sensitivity-labels.md) ou de propriétés de fichier.</span><span class="sxs-lookup"><span data-stu-id="8c042-109">The DLP on-premises scanner detects sensitive information by using [built-in](sensitive-information-type-entity-definitions.md) or [custom sensitive information](create-a-custom-sensitive-information-type.md) types, [sensitivity labels](sensitivity-labels.md) or file properties.</span></span> <span data-ttu-id="8c042-110">Les informations relatives aux actions des utilisateurs avec les éléments sensibles apparaissent dans [l’Explorateur d’activités](data-classification-activity-explorer.md), et vous pouvez appliquer des actions de protection à ces éléments via les [stratégies DLP](create-test-tune-dlp-policy.md).</span><span class="sxs-lookup"><span data-stu-id="8c042-110">The information about what users are doing with sensitive items is made visible in [activity explorer](data-classification-activity-explorer.md) and you can enforce protective actions on those items via [DLP policies](create-test-tune-dlp-policy.md).</span></span>

## <a name="the-dlp-on-premises-scanner-relies-on-azure-information-protection-scanner"></a><span data-ttu-id="8c042-111">Le scanneur local de protection contre la perte de données s’appuie sur le scanneur Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="8c042-111">The DLP on-premises scanner relies on Azure Information Protection scanner</span></span>

<span data-ttu-id="8c042-112">Le scanneur local de protection contre la perte de données s’appuie sur une implémentation complète du scanneur Azure Information Protection (AIP) pour surveiller, étiqueter, puis protéger les éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="8c042-112">The DLP on-premises scanner relies on a full implementation of the Azure Information Protection (AIP) scanner to monitor, label and protect sensitive items.</span></span> <span data-ttu-id="8c042-113">Si vous n’êtes pas familiarisé avec le scanneur AIP, nous vous recommandons vivement de vous y familiariser.</span><span class="sxs-lookup"><span data-stu-id="8c042-113">If you aren't familiar with the AIP scanner, we strongly recommend familiarizing yourself with it.</span></span> <span data-ttu-id="8c042-114">Veuillez consulter les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="8c042-114">See these articles:</span></span>

- [<span data-ttu-id="8c042-115">Qu'est-ce qu'Azure Information Protection ?</span><span class="sxs-lookup"><span data-stu-id="8c042-115">What is Azure Information Protection</span></span>](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)
- [<span data-ttu-id="8c042-116">Qu’est-ce que le scanneur d’étiquetage unifié Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="8c042-116">What is the Azure Information Protection unified labeling scanner</span></span>](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner)
- [<span data-ttu-id="8c042-117">Configuration requise pour l’installation et le déploiement du scanneur d’étiquetage unifié Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="8c042-117">Requirements for installing and deploying the Azure Information Protection unified labeling scanner</span></span>](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner-prereqs)
- [<span data-ttu-id="8c042-118">Tutoriel : Installation du scanneur d’étiquetage unifié Azure Information Protection (AIP)</span><span class="sxs-lookup"><span data-stu-id="8c042-118">Tutorial: Installing the Azure Information Protection (AIP) unified labeling scanner</span></span>](https://docs.microsoft.com/azure/information-protection/tutorial-install-scanner)
- [<span data-ttu-id="8c042-119">Configurer et installer le scanner d’étiquetage unifié Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="8c042-119">Configuring and installing the Azure Information Protection unified labeling scanner</span></span>](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner-configure-install)
- [<span data-ttu-id="8c042-120">Client d’étiquetage unifié Azure Information Protection : historique des versions et stratégie de support</span><span class="sxs-lookup"><span data-stu-id="8c042-120">Azure Information Protection unified labeling client - Version release history and support policy</span></span>](https://docs.microsoft.com/azure/information-protection/rms-client/unifiedlabelingclient-version-release-history)

## <a name="dlp-on-premises-scanner-actions"></a><span data-ttu-id="8c042-121">Actions du scanneur local de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="8c042-121">DLP on-premises scanner actions</span></span>

<span data-ttu-id="8c042-122">Le scanneur local de protection contre la perte de données détecte les fichiers par l’une des quatre méthodes ci-après :</span><span class="sxs-lookup"><span data-stu-id="8c042-122">DLP on-premises scanner detects files by one of these four methods:</span></span>

- <span data-ttu-id="8c042-123">types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="8c042-123">sensitive information types</span></span>
- <span data-ttu-id="8c042-124">étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="8c042-124">sensitivity labels</span></span>
- <span data-ttu-id="8c042-125">extension du fichier</span><span class="sxs-lookup"><span data-stu-id="8c042-125">file extension</span></span>
- <span data-ttu-id="8c042-126">propriétés de document personnalisées sur les fichiers Office uniquement</span><span class="sxs-lookup"><span data-stu-id="8c042-126">custom document properties on Office files only</span></span> 

<span data-ttu-id="8c042-127">Lorsqu’un fichier détecté présente un risque potentiel en cas de fuite ou de violation de stratégie de conformité, le scanneur local de protection contre la perte de données peut effectuer l’une de ces quatre actions.</span><span class="sxs-lookup"><span data-stu-id="8c042-127">When a detected file poses a potential risk if leaked or a compliance policy violation, the DLP on-premises scanner can take one of these four actions.</span></span>

|<span data-ttu-id="8c042-128">Opération</span><span class="sxs-lookup"><span data-stu-id="8c042-128">Action</span></span> |<span data-ttu-id="8c042-129">Description</span><span class="sxs-lookup"><span data-stu-id="8c042-129">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="8c042-130">**Empêcher ces personnes d’accéder à un fichier stocké dans un scanneur local : Tout le monde**</span><span class="sxs-lookup"><span data-stu-id="8c042-130">**Block these people from accessing file stored in  on-premises scanner - Everyone**</span></span> | <span data-ttu-id="8c042-131">Cette action bloque l’accès à tous les comptes à l’exception du propriétaire du contenu, du dernier compte qui a modifié l’élément et de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="8c042-131">When enforced, this action blocks access to all accounts except the content owner, the last account that modified the item and the administrator.</span></span> <span data-ttu-id="8c042-132">Pour ce faire, le programme supprime tous les comptes des autorisations NTFS/SharePoint au niveau du fichier, à l’exception du propriétaire du fichier, du propriétaire du référentiel (défini dans le paramètre de [définition du propriétaire du référentiel](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner-configure-install#use-a-data-loss-prevention-dlp-policy-public-preview) dans le travail d’analyse de contenu), du dernier modificateur (peut être identifié dans SharePoint uniquement) et de l’administrateur. Le compte du scanneur bénéficie également des droits FC sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="8c042-132">It does this by removing all accounts from NTFS/SharePoint permissions at the file level except the file owner, repository owner (set in the [Set repository owner](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner-configure-install#use-a-data-loss-prevention-dlp-policy-public-preview) setting in content scan job), last modifier (can be identified in SharePoint only) and admin. The scanner account is also granted FC rights on the file.</span></span>|
|<span data-ttu-id="8c042-133">**Empêcher ces personnes d’accéder à un fichier stocké dans un scanneur local : bloquer l’accès (public) à l’échelle de l’organisation**</span><span class="sxs-lookup"><span data-stu-id="8c042-133">**Block these people from accessing file stored in  on-premises scanner - block org-wide (public) access**</span></span>    |<span data-ttu-id="8c042-134">Cette action supprime les SID **_Tout le monde_*_, _*_NT AUTHORITY\utilisateurs identifiés_*_ et _*_Utilisateurs du domaine_** de la liste de contrôle d’accès au fichier (ACL).</span><span class="sxs-lookup"><span data-stu-id="8c042-134">When enforced, this action removes the **_Everyone_*_, _*_NT AUTHORITY\authenticated users_*_, and _*_Domain Users_** SIDs from the file access control list (ACL).</span></span> <span data-ttu-id="8c042-135">Seuls les utilisateurs et les groupes qui ont reçu explicitement les droits d’accès au fichier ou au dossier parent pourront accéder au fichier.</span><span class="sxs-lookup"><span data-stu-id="8c042-135">Only users and groups that have been explicitly granted rights to the file or parent folder will be able to access the file.</span></span>|
|<span data-ttu-id="8c042-136">**Définir des autorisations sur le fichier**</span><span class="sxs-lookup"><span data-stu-id="8c042-136">**Set permissions on the file**</span></span>|<span data-ttu-id="8c042-137">Cette action force le fichier à hériter des autorisations de son dossier parent.</span><span class="sxs-lookup"><span data-stu-id="8c042-137">When enforced, this action forces the file to inherit the permissions of its parent folder.</span></span> <span data-ttu-id="8c042-138">Par défaut, cette action n’est applicable que si les autorisations du dossier parent sont plus restrictives que celles déjà appliquées au fichier.</span><span class="sxs-lookup"><span data-stu-id="8c042-138">Be default, this action will only be enforced if the permissions on the parent folder are more restrictive than the permissions that are already on the file.</span></span> <span data-ttu-id="8c042-139">Par exemple, si vous avez défini la liste de contrôle d'accès du fichier pour autoriser uniquement des **_utilisateurs spécifiques_*_ et que vous avez configuré le dossier parent pour autoriser le groupe _*_Utilisateurs du domaine_*_, le fichier n’héritera pas des autorisations du dossier parent. Vous pouvez remplacer ce comportement en sélectionnant l’option _\* Inherit even if parent permissions are less restrictive*\* (Hériter, même si les autorisations parent sont moins restrictives).</span><span class="sxs-lookup"><span data-stu-id="8c042-139">For example, if the ACL on the file is set to only allow **_specific users_*_ and the parent folder is configured to allow _*_Domain Users_*_ group, the parent folder permissions would not be inherited by the file. You can override this behavior by selecting the _\* Inherit even if parent permissions are less restrictive*\* option.</span></span>|
|<span data-ttu-id="8c042-140">**Supprimer le fichier d’un emplacement incorrect**</span><span class="sxs-lookup"><span data-stu-id="8c042-140">**Remove the file from improper location**</span></span>|<span data-ttu-id="8c042-141">Cette action remplace le fichier d’origine par un fichier stub avec l’extension .txt, puis place une copie du fichier d’origine dans un dossier de mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="8c042-141">When enforced, this action replaces the original file with a stub file with .txt extension and places a copy of the original file in a quarantine folder.</span></span> 

## <a name="whats-different-in-the-on-premises-scanner"></a><span data-ttu-id="8c042-142">Différences dans le scanneur local</span><span class="sxs-lookup"><span data-stu-id="8c042-142">What's different in the on-premises scanner</span></span>

<span data-ttu-id="8c042-143">Vous devez tenir compte d’un certain nombre de concepts supplémentaires avant d’examiner en profondeur le scanneur local.</span><span class="sxs-lookup"><span data-stu-id="8c042-143">There are a few extra concepts that you need to be aware of before you dig into the on-premises scanner.</span></span>

### <a name="aip-repositories-and-content-scan-jobs"></a><span data-ttu-id="8c042-144">Référentiels et tâches d’analyse de contenu AIP</span><span class="sxs-lookup"><span data-stu-id="8c042-144">AIP repositories and content scan jobs</span></span>

<span data-ttu-id="8c042-145">Vous devez créer une tâche d’analyse de contenu AIP, puis spécifier les référentiels qui hébergent les fichiers que le moteur DLP doit évaluer selon vous.</span><span class="sxs-lookup"><span data-stu-id="8c042-145">You must create an AIP content scan jobs and identify the repositories that host the files that you want to be evaluated by DLP engine.</span></span> <span data-ttu-id="8c042-146">Veillez à activer les règles DLP dans la tâche d’analyse de contenu AIP créée.</span><span class="sxs-lookup"><span data-stu-id="8c042-146">Make sure you enable DLP rules in the created AIP content scan job.</span></span>

### <a name="policy-tips"></a><span data-ttu-id="8c042-147">Conseils de stratégie</span><span class="sxs-lookup"><span data-stu-id="8c042-147">Policy tips</span></span>

<span data-ttu-id="8c042-148">Les [Conseils de stratégie](use-notifications-and-policy-tips.md) ne sont pas disponibles sur le scanneur local.</span><span class="sxs-lookup"><span data-stu-id="8c042-148">[Policy tips](use-notifications-and-policy-tips.md) are not available in on-premises scanner.</span></span>


### <a name="viewing-dlp-on-premises-scanner-events"></a><span data-ttu-id="8c042-149">Affichage des événements liés au scanneur local de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="8c042-149">Viewing DLP on-premises scanner events</span></span>

<span data-ttu-id="8c042-150">Affichez les données du scanneur local de protection contre la perte de données dans l’[Explorateur d’activités](data-classification-activity-explorer.md) du Centre de conformité M365.</span><span class="sxs-lookup"><span data-stu-id="8c042-150">You view DLP on-premises scanner data in the M365 Compliance Center [activity explorer](data-classification-activity-explorer.md).</span></span> 

## <a name="next-steps"></a><span data-ttu-id="8c042-151">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="8c042-151">Next steps</span></span>

<span data-ttu-id="8c042-152">Maintenant que vous en savez plus sur le scanneur local de protection contre la perte de données, vos prochaines étapes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c042-152">Now that you've learned about DLP on-premises scanner, your next steps are:</span></span>

1. [<span data-ttu-id="8c042-153">Prise en main du scanner local de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="8c042-153">Get started with the DLP on-premises scanner</span></span>](dlp-on-premises-scanner-get-started.md)
2. [<span data-ttu-id="8c042-154">Utilisation du scanneur local de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="8c042-154">Use the DLP on-premises scanner</span></span>](dlp-on-premises-scanner-use.md)

## <a name="see-also"></a><span data-ttu-id="8c042-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c042-155">See also</span></span>

- [<span data-ttu-id="8c042-156">Prise en main du scanner local de protection contre la perte de données Microsoft</span><span class="sxs-lookup"><span data-stu-id="8c042-156">Getting started with the Microsoft data loss prevention on-premises scanner</span></span>](dlp-on-premises-scanner-get-started.md)
- [<span data-ttu-id="8c042-157">Utilisation du scanneur local de protection contre la perte de données Microsoft</span><span class="sxs-lookup"><span data-stu-id="8c042-157">Use the Microsoft data loss prevention on-premises scanner</span></span>](dlp-on-premises-scanner-use.md)
- [<span data-ttu-id="8c042-158">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="8c042-158">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="8c042-159">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="8c042-159">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="8c042-160">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="8c042-160">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)