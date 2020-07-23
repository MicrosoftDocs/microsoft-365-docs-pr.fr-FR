---
title: Chiffrement à double clé (DKE)
description: DKE vous permet de protéger les données hautement sensibles tout en conservant le contrôle total de votre clé.
author: kccross
ms.author: krowley
manager: laurawi
ms.date: 07/21/2020
ms.topic: conceptual
ms.service: information-protection
audience: Admin
ms.reviewer: esaggese
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.openlocfilehash: d9ed155576d69889e53e4e4d1ce03e4233fd08ff
ms.sourcegitcommit: 4789b261eb029d7c965421a1260acc110e6385db
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/23/2020
ms.locfileid: "45387441"
---
# <a name="double-key-encryption-dke"></a><span data-ttu-id="88d42-103">Chiffrement à double clé (DKE)</span><span class="sxs-lookup"><span data-stu-id="88d42-103">Double Key Encryption (DKE)</span></span>

> <span data-ttu-id="88d42-104">*S’applique à : double Key chiffrement pour la version préliminaire publique de Microsoft 365, [conformité microsoft 365](https://www.microsoft.com/microsoft-365/business/compliance-management), [Azure information protection](https://azure.microsoft.com/pricing/details/information-protection)*</span><span class="sxs-lookup"><span data-stu-id="88d42-104">*Applies to: Double Key Encryption for Microsoft 365 public preview, [Microsoft 365 Compliance](https://www.microsoft.com/microsoft-365/business/compliance-management), [Azure Information Protection](https://azure.microsoft.com/pricing/details/information-protection)*</span></span>
>
> <span data-ttu-id="88d42-105">*Instructions pour : [client d’étiquetage unifié Azure information protection pour Windows](https://docs.microsoft.com/azure/information-protection/faqs.md#whats-the-difference-between-the-azure-information-protection-classic-and-unified-labeling-clients)*</span><span class="sxs-lookup"><span data-stu-id="88d42-105">*Instructions for: [Azure Information Protection unified labeling client for Windows](https://docs.microsoft.com/azure/information-protection/faqs.md#whats-the-difference-between-the-azure-information-protection-classic-and-unified-labeling-clients)*</span></span>
>
> <span data-ttu-id="88d42-106">*Description du service : [conformité Microsoft 365](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance)*</span><span class="sxs-lookup"><span data-stu-id="88d42-106">*Service description for: [Microsoft 365 Compliance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance)*</span></span>

<span data-ttu-id="88d42-107">Le chiffrement à clé double (DKE) utilise deux clés ensemble pour accéder au contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="88d42-107">Double Key Encryption (DKE) uses two keys together to access protected content.</span></span> <span data-ttu-id="88d42-108">Vous stockez une clé dans Microsoft Azure et vous la maintenez.</span><span class="sxs-lookup"><span data-stu-id="88d42-108">You store one key in Microsoft Azure, and you hold the other key.</span></span> <span data-ttu-id="88d42-109">Le client d’étiquetage unifié Azure information Protection protège le contenu hautement sensible tout en conservant le contrôle total de l’une de vos clés.</span><span class="sxs-lookup"><span data-stu-id="88d42-109">The Azure Information Protection unified labeling client protects highly sensitive content while you maintain full control of one of your keys.</span></span>

<span data-ttu-id="88d42-110">Le chiffrement à double clé prend en charge les déploiements sur le Cloud et sur site.</span><span class="sxs-lookup"><span data-stu-id="88d42-110">Double Key Encryption supports both cloud and on-premises deployments.</span></span> <span data-ttu-id="88d42-111">Ces déploiements permettent de s’assurer que les données chiffrées restent opaques, où que vous stockez les données protégées.</span><span class="sxs-lookup"><span data-stu-id="88d42-111">These deployments help to ensure that encrypted data remains opaque wherever you store the protected data.</span></span>

<span data-ttu-id="88d42-112">Pour plus d’informations sur les clés de racine de client par défaut, consultez la rubrique [planification et implémentation de votre clé de client Azure information protection](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key).</span><span class="sxs-lookup"><span data-stu-id="88d42-112">For more information about the default, cloud-based tenant root keys, see [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key).</span></span>

<span data-ttu-id="88d42-113">La vidéo suivante montre comment le chiffrement à clé double fonctionne pour sécuriser votre contenu.</span><span class="sxs-lookup"><span data-stu-id="88d42-113">The following video shows how Double Key Encryption works to secure your content.</span></span>

> [!VIDEO https://msit.microsoftstream.com/embed/video/f466a1ff-0400-a936-221c-f1eab45dc756]

<span data-ttu-id="88d42-114">Si votre organisation dispose de l’une des conditions suivantes, vous pouvez utiliser DKE pour sécuriser votre contenu :</span><span class="sxs-lookup"><span data-stu-id="88d42-114">If your organizations have any of the following requirements, you can use DKE to help secure your content:</span></span>

- <span data-ttu-id="88d42-115">Vous souhaitez vous assurer que *vous* êtes le seul à pouvoir déchiffrer le contenu protégé, dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="88d42-115">You want to ensure that *only you* can ever decrypt protected content, under all circumstances.</span></span>
- <span data-ttu-id="88d42-116">Vous ne souhaitez pas que Microsoft ait accès aux données protégées de façon autonome.</span><span class="sxs-lookup"><span data-stu-id="88d42-116">You don't want Microsoft to have access to protected data on its own.</span></span>
- <span data-ttu-id="88d42-117">Vous avez des exigences réglementaires à maintenir des clés dans une limite géographique.</span><span class="sxs-lookup"><span data-stu-id="88d42-117">You have regulatory requirements to hold keys within a geographical boundary.</span></span> <span data-ttu-id="88d42-118">Toutes les clés que vous mettez en attente pour le chiffrement et le déchiffrement des données sont conservées dans votre centre de données.</span><span class="sxs-lookup"><span data-stu-id="88d42-118">All of the keys that you hold for data encryption and decryption are maintained in your data center.</span></span>

## <a name="system-and-licensing-requirements-for-dke"></a><span data-ttu-id="88d42-119">Exigences en matière de système et de licence pour DKE</span><span class="sxs-lookup"><span data-stu-id="88d42-119">System and licensing requirements for DKE</span></span>

<span data-ttu-id="88d42-120">Chiffrement à double clé pour Microsoft 365 partie de Microsoft 365 E5 et Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="88d42-120">Double Key Encryption for Microsoft 365 part of Microsoft 365 E5 and Office 365 E5.</span></span> <span data-ttu-id="88d42-121">Si vous n’avez pas de licence Microsoft 365 E5, vous pouvez vous inscrire pour obtenir une [version d’évaluation](https://aka.ms/M365E5ComplianceTrial).</span><span class="sxs-lookup"><span data-stu-id="88d42-121">If you don’t have a Microsoft 365 E5 license, you can sign up for a [trial](https://aka.ms/M365E5ComplianceTrial).</span></span> <span data-ttu-id="88d42-122">Pour plus d’informations sur ces licences, consultez [la rubrique Microsoft 365 Licensing Guidance for security & Compliance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).</span><span class="sxs-lookup"><span data-stu-id="88d42-122">For more information about these licenses, see [Microsoft 365 licensing guidance for security & compliance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).</span></span>

<span data-ttu-id="88d42-123">**Office Insider** Pour utiliser la préversion publique, vous devez être membre du programme Office Insider.</span><span class="sxs-lookup"><span data-stu-id="88d42-123">**Office Insider** To use the public preview, you must be a member of the Office Insider program.</span></span> <span data-ttu-id="88d42-124">Pour rejoindre Office Insider, accédez à [https://insider.office.com](https://insider.office.com) .</span><span class="sxs-lookup"><span data-stu-id="88d42-124">To join Office Insider, go to [https://insider.office.com](https://insider.office.com).</span></span> <span data-ttu-id="88d42-125">Une fois que vous êtes membre, préparez votre environnement pour déployer les builds Office Insider en choisissant la méthode de déploiement appropriée pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="88d42-125">Once you're a member, prepare your environment to deploy Office Insider builds by choosing the right deployment method for your organization.</span></span> <span data-ttu-id="88d42-126">Pour obtenir des instructions, consultez la rubrique [prise en main du déploiement des builds Office Insider](https://insider.office.com/business/deploy).</span><span class="sxs-lookup"><span data-stu-id="88d42-126">For instructions, see [Getting started on deploying Office Insider builds](https://insider.office.com/business/deploy).</span></span>

<span data-ttu-id="88d42-127">**Azure information protection**.</span><span class="sxs-lookup"><span data-stu-id="88d42-127">**Azure Information Protection**.</span></span> <span data-ttu-id="88d42-128">DKE fonctionne avec les étiquettes de confidentialité et nécessite Azure information protection.</span><span class="sxs-lookup"><span data-stu-id="88d42-128">DKE works with sensitivity labels and requires Azure Information Protection.</span></span>

## <a name="supported-environments-for-storing-and-viewing-dke-protected-content"></a><span data-ttu-id="88d42-129">Environnements pris en charge pour le stockage et l’affichage du contenu protégé par DKE</span><span class="sxs-lookup"><span data-stu-id="88d42-129">Supported environments for storing and viewing DKE-protected content</span></span>

<span data-ttu-id="88d42-130">**Applications prises en charge**.</span><span class="sxs-lookup"><span data-stu-id="88d42-130">**Supported applications**.</span></span> <span data-ttu-id="88d42-131">[Applications Microsoft 365 pour](https://www.microsoft.com/microsoft-365/business/microsoft-365-apps-for-enterprise-product) les clients d’entreprise sur Windows, y compris Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="88d42-131">[Microsoft 365 Apps for enterprise](https://www.microsoft.com/microsoft-365/business/microsoft-365-apps-for-enterprise-product) clients on Windows, including Word, Excel, and PowerPoint.</span></span>

<span data-ttu-id="88d42-132">**Prise en charge du contenu en ligne**.</span><span class="sxs-lookup"><span data-stu-id="88d42-132">**Online content support**.</span></span> <span data-ttu-id="88d42-133">Les documents et les fichiers stockés en ligne dans Microsoft SharePoint et OneDrive entreprise sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="88d42-133">Documents and files stored online in both Microsoft SharePoint and OneDrive for Business are supported.</span></span> <span data-ttu-id="88d42-134">Vous pouvez partager le contenu chiffré par courrier électronique, mais vous ne pouvez pas afficher les documents et fichiers chiffrés en ligne.</span><span class="sxs-lookup"><span data-stu-id="88d42-134">You can share encrypted content by email, but you can't view encrypted documents and files online.</span></span> <span data-ttu-id="88d42-135">Au lieu de cela, vous devez afficher le contenu protégé à l’aide des applications de bureau sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="88d42-135">Instead, you must view protected content using the desktop apps on your local computer.</span></span>

## <a name="about-this-public-preview-article"></a><span data-ttu-id="88d42-136">À propos de cet article d’aperçu public</span><span class="sxs-lookup"><span data-stu-id="88d42-136">About this public preview article</span></span>

<span data-ttu-id="88d42-137">Il existe plusieurs façons de procéder pour déployer le chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="88d42-137">There are several ways you can complete some of the steps to deploy Double Key Encryption.</span></span> <span data-ttu-id="88d42-138">Cet article fournit des instructions détaillées afin que les administrateurs moins expérimentés déploient correctement le service.</span><span class="sxs-lookup"><span data-stu-id="88d42-138">This article provides detailed instructions so that less experienced admins successfully deploy the service.</span></span> <span data-ttu-id="88d42-139">Si vous êtes familiarisé, vous pouvez choisir d’utiliser vos propres méthodes.</span><span class="sxs-lookup"><span data-stu-id="88d42-139">If you're comfortable doing so, you can choose to use your own methods.</span></span>

<span data-ttu-id="88d42-140">Cet article contient des instructions détaillées sur la façon de déployer le service de chiffrement à double clé sur Azure.</span><span class="sxs-lookup"><span data-stu-id="88d42-140">This article includes step-by-step instructions on how to deploy the Double Key Encryption service to Azure.</span></span> <span data-ttu-id="88d42-141">Ce scénario n’est pas très probable en production.</span><span class="sxs-lookup"><span data-stu-id="88d42-141">This scenario isn't something you'd likely do in production.</span></span> <span data-ttu-id="88d42-142">Pour la préversion publique, l’utilisation d’Azure est un moyen rapide de déployer DKE.</span><span class="sxs-lookup"><span data-stu-id="88d42-142">For public preview, using Azure is a quick way to deploy DKE.</span></span> <span data-ttu-id="88d42-143">Le déploiement vers Azure vous permet de commencer à utiliser le chiffrement à clé double immédiatement.</span><span class="sxs-lookup"><span data-stu-id="88d42-143">Deploying to Azure lets you get started using Double Key Encryption right away.</span></span>

<span data-ttu-id="88d42-144">Vous pouvez déployer le service localement sur votre réseau ou avec un autre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="88d42-144">You can deploy the service locally on your network or with another provider.</span></span> <span data-ttu-id="88d42-145">Vous devrez publier le magasin de clés à l’aide de méthodes appropriées pour cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="88d42-145">You'll need to publish the key store using methods that are appropriate for that location.</span></span>

## <a name="deploy-double-key-encryption"></a><span data-ttu-id="88d42-146">Déployer le chiffrement à double clé</span><span class="sxs-lookup"><span data-stu-id="88d42-146">Deploy Double Key Encryption</span></span>

<span data-ttu-id="88d42-147">Cet article et la vidéo de déploiement utilisent Azure comme destination de déploiement pour le service DKE.</span><span class="sxs-lookup"><span data-stu-id="88d42-147">This article and the deployment video use Azure as the deployment destination for the DKE service.</span></span> <span data-ttu-id="88d42-148">Si vous effectuez le déploiement vers un autre emplacement, vous devez fournir vos propres valeurs.</span><span class="sxs-lookup"><span data-stu-id="88d42-148">If you're deploying to another location, you'll need to provide your own values.</span></span>

<span data-ttu-id="88d42-149">Regardez la [vidéo sur le déploiement de chiffrement à double clé](https://msit.microsoftstream.com/video/cfdda3ff-0400-a521-1579-f1eacc37fc7e) pour voir pas à pas la présentation des concepts de l’article.</span><span class="sxs-lookup"><span data-stu-id="88d42-149">Watch the [Double Key Encryption deployment video](https://msit.microsoftstream.com/video/cfdda3ff-0400-a521-1579-f1eacc37fc7e) to see step-by-step overview of concepts in the article.</span></span> <span data-ttu-id="88d42-150">La vidéo prend environ 18 minutes.</span><span class="sxs-lookup"><span data-stu-id="88d42-150">The video takes about 18 minutes to complete.</span></span>

<span data-ttu-id="88d42-151">Suivez ces étapes générales pour configurer le chiffrement à double clé pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="88d42-151">You'll follow these general steps to set up Double Key Encryption for your organization.</span></span>

1. [<span data-ttu-id="88d42-152">Installer les composants logiciels requis</span><span class="sxs-lookup"><span data-stu-id="88d42-152">Install software prerequisites</span></span>](#install-software-prerequisites)
1. [<span data-ttu-id="88d42-153">Cloner le référentiel GitHub de chiffrement à double clé</span><span class="sxs-lookup"><span data-stu-id="88d42-153">Clone the Double Key Encryption GitHub repository</span></span>](#clone-the-dke-github-repository)
1. [<span data-ttu-id="88d42-154">Modifier les paramètres d’application</span><span class="sxs-lookup"><span data-stu-id="88d42-154">Modify application settings</span></span>](#modify-application-settings)
1. [<span data-ttu-id="88d42-155">Générer des clés de test</span><span class="sxs-lookup"><span data-stu-id="88d42-155">Generate test keys</span></span>](#generate-test-keys)
1. [<span data-ttu-id="88d42-156">Générer le projet</span><span class="sxs-lookup"><span data-stu-id="88d42-156">Build the project</span></span>](#build-the-project)
1. [<span data-ttu-id="88d42-157">Publier le magasin de clés</span><span class="sxs-lookup"><span data-stu-id="88d42-157">Publish the key store</span></span>](#publish-the-key-store)
1. [<span data-ttu-id="88d42-158">Valider votre déploiement</span><span class="sxs-lookup"><span data-stu-id="88d42-158">Validate your deployment</span></span>](#validate-your-deployment)
1. [<span data-ttu-id="88d42-159">Enregistrer votre magasin de clés</span><span class="sxs-lookup"><span data-stu-id="88d42-159">Register your key store</span></span>](#register-your-key-store)
1. [<span data-ttu-id="88d42-160">Créer des étiquettes de sensibilité</span><span class="sxs-lookup"><span data-stu-id="88d42-160">Create sensitivity labels</span></span>](#create-labels-using-dke)

<span data-ttu-id="88d42-161">Lorsque vous avez fini, vous pouvez chiffrer des documents et des fichiers à l’aide de DKE.</span><span class="sxs-lookup"><span data-stu-id="88d42-161">When you're done, you can encrypt documents and files using DKE.</span></span> <span data-ttu-id="88d42-162">Pour plus d’informations, consultez [la rubrique appliquer des étiquettes de confidentialité à vos fichiers et à votre messagerie électronique dans Office](https://support.microsoft.com/office/2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9).</span><span class="sxs-lookup"><span data-stu-id="88d42-162">For information, see [Apply sensitivity labels to your files and email in Office](https://support.microsoft.com/office/2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9).</span></span>

### <a name="install-software-prerequisites"></a><span data-ttu-id="88d42-163">Installer les composants logiciels requis</span><span class="sxs-lookup"><span data-stu-id="88d42-163">Install software prerequisites</span></span>

<span data-ttu-id="88d42-164">Il existe deux types de logiciels requis pour le chiffrement à double clé</span><span class="sxs-lookup"><span data-stu-id="88d42-164">There are two types of software prerequisites for Double Key Encryption</span></span>

- [<span data-ttu-id="88d42-165">Conditions préalables requises pour le service de chiffrement à clé double</span><span class="sxs-lookup"><span data-stu-id="88d42-165">Double Key Encryption service prerequisites</span></span>](#double-key-encryption-service-prerequisites)
- [<span data-ttu-id="88d42-166">Conditions préalables au chiffrement à double clé pour les ordinateurs clients</span><span class="sxs-lookup"><span data-stu-id="88d42-166">Double Key Encryption prerequisites for client computers</span></span>](#double-key-encryption-prerequisites-for-client-computers)

#### <a name="double-key-encryption-service-prerequisites"></a><span data-ttu-id="88d42-167">Conditions préalables requises pour le service de chiffrement à clé double</span><span class="sxs-lookup"><span data-stu-id="88d42-167">Double Key Encryption service prerequisites</span></span>

<span data-ttu-id="88d42-168">Installez ces éléments prérequis sur l’ordinateur sur lequel vous souhaitez installer le service DKE.</span><span class="sxs-lookup"><span data-stu-id="88d42-168">Install these prerequisites on the computer where you want to install the DKE service.</span></span>

<span data-ttu-id="88d42-169">**.Net Core 3,1 SDK**.</span><span class="sxs-lookup"><span data-stu-id="88d42-169">**.NET Core 3.1 SDK**.</span></span> <span data-ttu-id="88d42-170">Téléchargez et installez le kit de développement logiciel (SDK) à partir de [Télécharger .net Core 3,1](https://dotnet.microsoft.com/download/dotnet-core/3.1).</span><span class="sxs-lookup"><span data-stu-id="88d42-170">Download and install the SDK from [Download .NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1).</span></span>

<span data-ttu-id="88d42-171">**Visual Studio code**.</span><span class="sxs-lookup"><span data-stu-id="88d42-171">**Visual Studio Code**.</span></span> <span data-ttu-id="88d42-172">Téléchargez Visual Studio code à partir de [https://code.visualstudio.com/](https://code.visualstudio.com) .</span><span class="sxs-lookup"><span data-stu-id="88d42-172">Download Visual Studio Code from [https://code.visualstudio.com/](https://code.visualstudio.com).</span></span> <span data-ttu-id="88d42-173">Une fois installé, exécutez Visual Studio code et sélectionnez **Afficher** les \> **Extensions**.</span><span class="sxs-lookup"><span data-stu-id="88d42-173">Once installed, run Visual Studio Code and select **View** \> **Extensions**.</span></span> <span data-ttu-id="88d42-174">Installez ces extensions.</span><span class="sxs-lookup"><span data-stu-id="88d42-174">Install these extensions.</span></span>

- <span data-ttu-id="88d42-175">C# pour Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="88d42-175">C# for Visual Studio Code</span></span>

- <span data-ttu-id="88d42-176">Gestionnaire de package NuGet</span><span class="sxs-lookup"><span data-stu-id="88d42-176">NuGet Package Manager</span></span>

<span data-ttu-id="88d42-177">**Microsoft Office Insider**.</span><span class="sxs-lookup"><span data-stu-id="88d42-177">**Microsoft Office Insider**.</span></span> <span data-ttu-id="88d42-178">Configurez au moins une [méthode de déploiement](https://insider.office.com/business/deploy).</span><span class="sxs-lookup"><span data-stu-id="88d42-178">Set up at least one [deployment method](https://insider.office.com/business/deploy).</span></span>

<span data-ttu-id="88d42-179">**Ressources git**.</span><span class="sxs-lookup"><span data-stu-id="88d42-179">**Git resources**.</span></span> <span data-ttu-id="88d42-180">Téléchargez et installez l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="88d42-180">Download and install one of the following.</span></span>

- [<span data-ttu-id="88d42-181">Git</span><span class="sxs-lookup"><span data-stu-id="88d42-181">Git</span></span>](https://git-scm.com/downloads)

- [<span data-ttu-id="88d42-182">Bureau GitHub</span><span class="sxs-lookup"><span data-stu-id="88d42-182">GitHub Desktop</span></span>](https://desktop.github.com/)

- [<span data-ttu-id="88d42-183">GitHub entreprise</span><span class="sxs-lookup"><span data-stu-id="88d42-183">GitHub Enterprise</span></span>](https://github.com/enterprise)

<span data-ttu-id="88d42-184">**OpenSSL** [OpenSSL](https://slproweb.com/products/Win32OpenSSL.html) doit être installé pour [générer des clés de test](#generate-test-keys) une fois que vous avez déployé DKE.</span><span class="sxs-lookup"><span data-stu-id="88d42-184">**OpenSSL** You must have [OpenSSL](https://slproweb.com/products/Win32OpenSSL.html) installed to [generate test keys](#generate-test-keys) after you deploy DKE.</span></span> <span data-ttu-id="88d42-185">Vérifiez que vous l’appelez correctement à partir de votre chemin d’accès aux variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="88d42-185">Make sure you're invoking it correctly from your environment variables path.</span></span> <span data-ttu-id="88d42-186">Par exemple, pour plus d’informations, consultez la section « ajouter le répertoire d’installation au chemin d’accès » https://www.osradar.com/install-openssl-windows/ .</span><span class="sxs-lookup"><span data-stu-id="88d42-186">For example, see "Add the installation directory to PATH" at https://www.osradar.com/install-openssl-windows/ for details.</span></span>

#### <a name="double-key-encryption-prerequisites-for-client-computers"></a><span data-ttu-id="88d42-187">Conditions préalables au chiffrement à double clé pour les ordinateurs clients</span><span class="sxs-lookup"><span data-stu-id="88d42-187">Double Key Encryption prerequisites for client computers</span></span>

<span data-ttu-id="88d42-188">Installez ces éléments prérequis sur chaque ordinateur client sur lequel vous souhaitez protéger et consommer des documents protégés.</span><span class="sxs-lookup"><span data-stu-id="88d42-188">Install these prerequisites on each client computer where you want to protect and consume protected documents.</span></span>

<span data-ttu-id="88d42-189">**Microsoft Office** version \*. 12711 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="88d42-189">**Microsoft Office** version \*.12711 or later.</span></span>

<span data-ttu-id="88d42-190">Versions du **client d’étiquetage unifié Azure information protection** 2.7.93.0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="88d42-190">**Azure Information Protection Unified Labeling Client** versions 2.7.93.0 or later.</span></span> <span data-ttu-id="88d42-191">Téléchargez et installez le client d’étiquetage unifié de [Microsoft](https://www.microsoft.com/download/details.aspx?id=53018).</span><span class="sxs-lookup"><span data-stu-id="88d42-191">Download and install the Unified Labeling client from [Microsoft](https://www.microsoft.com/download/details.aspx?id=53018).</span></span>

### <a name="clone-the-dke-github-repository"></a><span data-ttu-id="88d42-192">Cloner le référentiel DKE GitHub</span><span class="sxs-lookup"><span data-stu-id="88d42-192">Clone the DKE GitHub repository</span></span>

<span data-ttu-id="88d42-193">Microsoft fournit les fichiers source DKE dans un référentiel GitHub.</span><span class="sxs-lookup"><span data-stu-id="88d42-193">Microsoft supplies the DKE source files in a GitHub repository.</span></span> <span data-ttu-id="88d42-194">Vous clonez le référentiel pour créer le projet localement pour l’utilisation de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="88d42-194">You clone the repository to build the project locally for your organization's use.</span></span> <span data-ttu-id="88d42-195">Le référentiel DKE GitHub se trouve à l’emplacement [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService) .</span><span class="sxs-lookup"><span data-stu-id="88d42-195">The DKE GitHub repository is located at [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService).</span></span>

<span data-ttu-id="88d42-196">Les instructions suivantes sont destinées aux utilisateurs de git ou de code Visual Studio inexpérimentés :</span><span class="sxs-lookup"><span data-stu-id="88d42-196">The following instructions are intended for inexperienced git or Visual Studio Code users:</span></span>

1. <span data-ttu-id="88d42-197">Dans votre navigateur, accédez à :[https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService)</span><span class="sxs-lookup"><span data-stu-id="88d42-197">In your browser, go to: [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService)</span></span>

1. <span data-ttu-id="88d42-198">Dans la partie droite de l’écran, sélectionnez **code**.</span><span class="sxs-lookup"><span data-stu-id="88d42-198">Towards the right side of the screen, select **Code**.</span></span> <span data-ttu-id="88d42-199">Votre version de l’interface utilisateur peut afficher un bouton **Clone ou télécharger** .</span><span class="sxs-lookup"><span data-stu-id="88d42-199">Your version of the UI might show a **Clone or download** button.</span></span> <span data-ttu-id="88d42-200">Ensuite, dans la liste déroulante qui apparaît, sélectionnez l’icône copier pour copier l’URL dans votre presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="88d42-200">Then, in the dropdown that appears, select the copy icon to copy the URL to your clipboard.</span></span>

    <span data-ttu-id="88d42-201">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88d42-201">For example:</span></span>

    :::image type="content" source="../media/dke-clone.png" alt-text="Cloner le référentiel du service de chiffrement à clé double à partir de GitHub":::

3. <span data-ttu-id="88d42-203">Dans Visual Studio code, sélectionnez **Afficher** la \> **palette de commandes** et sélectionnez **git : Clone**.</span><span class="sxs-lookup"><span data-stu-id="88d42-203">In Visual Studio Code, select **View** \> **Command Palette** and select **Git: Clone**.</span></span> <span data-ttu-id="88d42-204">Pour accéder à l’option dans la liste, commencez `git: clone` à taper pour filtrer les entrées, puis sélectionnez-la dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="88d42-204">To jump to the option in the list, start typing `git: clone` to filter the entries and then select it from the drop-down.</span></span> <span data-ttu-id="88d42-205">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88d42-205">For example:</span></span>

    :::image type="content" source="../media/dke-vscode-clone.png" alt-text="Option GIT : clone de Visual Studio code":::

4. <span data-ttu-id="88d42-207">Dans la zone de texte, collez l’URL que vous avez copiée à partir de git et sélectionnez **Clone dans GitHub**.</span><span class="sxs-lookup"><span data-stu-id="88d42-207">In the text box, paste the URL that you copied from Git and select **Clone from GitHub**.</span></span>

5. <span data-ttu-id="88d42-208">Dans la boîte de dialogue **Sélectionner un dossier** qui s’affiche, accédez à l’emplacement où vous souhaitez stocker le référentiel et sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="88d42-208">In the **Select Folder** dialog that appears, browse to and select a location to store the repository.</span></span> <span data-ttu-id="88d42-209">À l’invite, sélectionnez **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="88d42-209">At the prompt, select **Open**.</span></span>

    <span data-ttu-id="88d42-210">Le référentiel est ouvert dans Visual Studio code et affiche la branche git actuelle en bas à gauche.</span><span class="sxs-lookup"><span data-stu-id="88d42-210">The repository is opened in Visual Studio Code, and displays the current Git branch at the bottom left.</span></span> <span data-ttu-id="88d42-211">La branche doit être **Master**.</span><span class="sxs-lookup"><span data-stu-id="88d42-211">The branch should be **master**.</span></span>

    <span data-ttu-id="88d42-212">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88d42-212">For example:</span></span>

    :::image type="content" source="../media/dke-vscode-master.png" alt-text="Branche Visual Studio code Master":::

6. <span data-ttu-id="88d42-214">Sélectionnez le masque de mots **,** puis sélectionnez **public_preview** dans la liste des branches.</span><span class="sxs-lookup"><span data-stu-id="88d42-214">Select the word **master,** and then select **public_preview** from the list of branches.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="88d42-215">La sélection de la branche public_preview vous permet de vous assurer que vous disposez des fichiers appropriés pour générer le projet.</span><span class="sxs-lookup"><span data-stu-id="88d42-215">Selecting the public_preview branch ensures that you have the correct files to build the project.</span></span> <span data-ttu-id="88d42-216">Si vous ne sélectionnez pas la branche appropriée, votre déploiement échouera.</span><span class="sxs-lookup"><span data-stu-id="88d42-216">If you do not choose the correct branch your deployment will fail.</span></span>

<span data-ttu-id="88d42-217">Votre référentiel source DKE est maintenant configuré localement.</span><span class="sxs-lookup"><span data-stu-id="88d42-217">You now have your DKE source repository set up locally.</span></span> <span data-ttu-id="88d42-218">Ensuite, [Modifiez les paramètres d’application](#modify-application-settings) pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="88d42-218">Next, [modify application settings](#modify-application-settings) for your organization.</span></span>

### <a name="modify-application-settings"></a><span data-ttu-id="88d42-219">Modifier les paramètres d’application</span><span class="sxs-lookup"><span data-stu-id="88d42-219">Modify application settings</span></span>

<span data-ttu-id="88d42-220">Pour déployer le service DKE, vous devez modifier les types de paramètres d’application suivants :</span><span class="sxs-lookup"><span data-stu-id="88d42-220">To deploy the DKE service, you must modify the following types of application settings:</span></span>

- [<span data-ttu-id="88d42-221">Paramètres d’accès clés</span><span class="sxs-lookup"><span data-stu-id="88d42-221">Key access settings</span></span>](#key-access-settings)
- [<span data-ttu-id="88d42-222">Paramètres de client et de clé</span><span class="sxs-lookup"><span data-stu-id="88d42-222">Tenant and key settings</span></span>](#tenant-and-key-settings)

<span data-ttu-id="88d42-223">Vous modifiez les paramètres de l’application dans le fichier appsettings.js.</span><span class="sxs-lookup"><span data-stu-id="88d42-223">You modify application settings in the appsettings.json file.</span></span> <span data-ttu-id="88d42-224">Ce fichier se trouve dans le DoubleKeyEncryptionService référentiel que vous avez cloné localement sous DoubleKeyEncryptionService\src\customer-key-store.</span><span class="sxs-lookup"><span data-stu-id="88d42-224">This file is located in the DoubleKeyEncryptionService repo you cloned locally under DoubleKeyEncryptionService\src\customer-key-store.</span></span> <span data-ttu-id="88d42-225">Par exemple, dans Visual Studio code, vous pouvez accéder au fichier comme indiqué dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="88d42-225">For example, in Visual Studio Code, you can browse to the file as shown in the following picture.</span></span>

:::image type="content" source="../media/dke-appsettingsjson.png" alt-text="Recherche de la appsettings.jssur le fichier pour DKE.":::

#### <a name="key-access-settings"></a><span data-ttu-id="88d42-227">Paramètres d’accès clés</span><span class="sxs-lookup"><span data-stu-id="88d42-227">Key access settings</span></span>

<span data-ttu-id="88d42-228">Choisissez d’utiliser ou non l’autorisation de messagerie ou de rôle.</span><span class="sxs-lookup"><span data-stu-id="88d42-228">Choose whether to use email or role authorization.</span></span> <span data-ttu-id="88d42-229">DKE ne prend en charge qu’une seule de ces méthodes d’authentification à la fois.</span><span class="sxs-lookup"><span data-stu-id="88d42-229">DKE supports only one of these authentication methods at a time.</span></span>

- <span data-ttu-id="88d42-230">**Autorisation de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="88d42-230">**Email authorization**.</span></span> <span data-ttu-id="88d42-231">Permet à votre organisation d’autoriser l’accès aux clés en fonction des adresses de messagerie uniquement.</span><span class="sxs-lookup"><span data-stu-id="88d42-231">Allows your organization to authorize access to keys based on email addresses only.</span></span>

- <span data-ttu-id="88d42-232">**Autorisation de rôle**.</span><span class="sxs-lookup"><span data-stu-id="88d42-232">**Role authorization**.</span></span> <span data-ttu-id="88d42-233">Permet à votre organisation d’autoriser l’accès aux clés en fonction des groupes Active Directory et exige que le service Web interroge LDAP.</span><span class="sxs-lookup"><span data-stu-id="88d42-233">Allows your organization to authorize access to keys based on Active Directory groups, and requires that the web service can query LDAP.</span></span>

<span data-ttu-id="88d42-234">**Pour définir les paramètres d’accès clés pour DKE à l’aide de l’autorisation de messagerie**</span><span class="sxs-lookup"><span data-stu-id="88d42-234">**To set key access settings for DKE using email authorization**</span></span>

1. <span data-ttu-id="88d42-235">Ouvrez le fichier **appsettings.js** et localisez le `AuthorizedEmailAddress` paramètre.</span><span class="sxs-lookup"><span data-stu-id="88d42-235">Open the **appsettings.json** file and locate the `AuthorizedEmailAddress` setting.</span></span>

2. <span data-ttu-id="88d42-236">Ajoutez l’adresse ou les adresses de messagerie que vous souhaitez autoriser.</span><span class="sxs-lookup"><span data-stu-id="88d42-236">Add the email address or addresses that you want to authorize.</span></span> <span data-ttu-id="88d42-237">Séparez les adresses de messagerie par des guillemets et des virgules.</span><span class="sxs-lookup"><span data-stu-id="88d42-237">Separate multiple email addresses with double quotes and commas.</span></span> <span data-ttu-id="88d42-238">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88d42-238">For example:</span></span>

   ```json
   "AuthorizedEmailAddress": ["email1@company.com", "email2@company.com ", "email3@company.com"]
   ```

3. <span data-ttu-id="88d42-239">Recherchez le `LDAPPath` paramètre et supprimez le texte `If role authorization is used then this is the LDAP path` entre guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="88d42-239">Locate the `LDAPPath` setting and remove the text `If role authorization is used then this is the LDAP path` between the double quotes.</span></span> <span data-ttu-id="88d42-240">Laissez les guillemets doubles en place.</span><span class="sxs-lookup"><span data-stu-id="88d42-240">Leave the double quotes in place.</span></span> <span data-ttu-id="88d42-241">Lorsque vous avez terminé, le paramètre doit ressembler à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="88d42-241">When you're finished, the setting should look like this.</span></span>

   ```json
   "LDAPPath": ""
   ```

4. <span data-ttu-id="88d42-242">Localisez le `AuthorizedRoles` paramètre et supprimez la ligne entière.</span><span class="sxs-lookup"><span data-stu-id="88d42-242">Locate the `AuthorizedRoles` setting and delete the entire line.</span></span>

<span data-ttu-id="88d42-243">Cette image montre le **appsettings.jssur** un fichier correctement mis en forme pour l’autorisation de messagerie.</span><span class="sxs-lookup"><span data-stu-id="88d42-243">This image shows the **appsettings.json** file correctly formatted for email authorization.</span></span>

   :::image type="content" source="../media/dke-email-accesssetting.png" alt-text="appsettings.jssur le fichier affichant la méthode d’autorisation de messagerie":::

<span data-ttu-id="88d42-245">**Pour définir les paramètres d’accès clés pour DKE à l’aide de l’autorisation de rôle**</span><span class="sxs-lookup"><span data-stu-id="88d42-245">**To set key access settings for DKE using role authorization**</span></span>

1. <span data-ttu-id="88d42-246">Ouvrez le fichier **appsettings.js** et localisez le `AuthorizedRoles` paramètre.</span><span class="sxs-lookup"><span data-stu-id="88d42-246">Open the **appsettings.json** file and locate the `AuthorizedRoles` setting.</span></span>

2. <span data-ttu-id="88d42-247">Ajoutez les noms de groupe Active Directory que vous souhaitez autoriser.</span><span class="sxs-lookup"><span data-stu-id="88d42-247">Add the Active Directory group names you want to authorize.</span></span> <span data-ttu-id="88d42-248">Séparez les noms de plusieurs groupes par des guillemets et des virgules.</span><span class="sxs-lookup"><span data-stu-id="88d42-248">Separate multiple group names with double quotes and commas.</span></span> <span data-ttu-id="88d42-249">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88d42-249">For example:</span></span>

   ```json
   "AuthorizedRoles": ["group1", "group2", "group3"]
   ```

3. <span data-ttu-id="88d42-250">Localisez le `LDAPPath` paramètre et ajoutez le domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="88d42-250">Locate the `LDAPPath` setting and add the Active Directory domain.</span></span> <span data-ttu-id="88d42-251">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88d42-251">For example:</span></span>

   ```json
   "LDAPPath": "contoso.com"
   ```

4. <span data-ttu-id="88d42-252">Localisez le `AuthorizedEmailAddress` paramètre et supprimez la ligne entière.</span><span class="sxs-lookup"><span data-stu-id="88d42-252">Locate the `AuthorizedEmailAddress` setting and delete the entire line.</span></span>

<span data-ttu-id="88d42-253">Cette image montre le **appsettings.jssur** un fichier correctement mis en forme pour l’autorisation de rôle.</span><span class="sxs-lookup"><span data-stu-id="88d42-253">This image shows the **appsettings.json** file correctly formatted for role authorization.</span></span>

   :::image type="content" source="../media/dke-role-accesssetting.png" alt-text="appsettings.jssur le fichier affichant la méthode d’autorisation de rôle":::

#### <a name="tenant-and-key-settings"></a><span data-ttu-id="88d42-255">Paramètres de client et de clé</span><span class="sxs-lookup"><span data-stu-id="88d42-255">Tenant and key settings</span></span>

<span data-ttu-id="88d42-256">Les paramètres de client et de clé DKE se trouvent dans le fichier **appsettings.js** .</span><span class="sxs-lookup"><span data-stu-id="88d42-256">DKE tenant and key settings are located in the **appsettings.json** file.</span></span>

<span data-ttu-id="88d42-257">**Pour configurer les paramètres de client et de clé pour DKE**</span><span class="sxs-lookup"><span data-stu-id="88d42-257">**To configure tenant and key settings for DKE**</span></span>

1. <span data-ttu-id="88d42-258">Ouvrez le fichier **appsettings.js** .</span><span class="sxs-lookup"><span data-stu-id="88d42-258">Open the **appsettings.json** file.</span></span>

2. <span data-ttu-id="88d42-259">Recherchez le `ValidIssuers` paramètre et remplacez-le `<tenantid>` par votre ID de client.</span><span class="sxs-lookup"><span data-stu-id="88d42-259">Locate the `ValidIssuers` setting and replace `<tenantid>` with your tenant ID.</span></span> <span data-ttu-id="88d42-260">Vous pouvez localiser votre ID de locataire en accédant au portail Azure et en affichant les [Propriétés du client](https://aad.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span><span class="sxs-lookup"><span data-stu-id="88d42-260">You can locate your tenant ID by going to the Azure portal and viewing the [tenant properties](https://aad.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span></span> <span data-ttu-id="88d42-261">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88d42-261">For example:</span></span>

   ```json
   "ValidIssuers": [
     "https://sts.windows.net/9c99431e-b513-44be-a7d9-e7b500002d4b/"
   ]
   ```

<span data-ttu-id="88d42-262">Localisez le `JwtAudience` .</span><span class="sxs-lookup"><span data-stu-id="88d42-262">Locate the `JwtAudience`.</span></span> <span data-ttu-id="88d42-263">Remplacez `<yourhostname>` par le nom d’hôte de l’ordinateur sur lequel le service DKE s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="88d42-263">Replace `<yourhostname>` with the hostname of the machine where the DKE service will run.</span></span> <span data-ttu-id="88d42-264">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88d42-264">For example:</span></span>



  > [!IMPORTANT]
  > <span data-ttu-id="88d42-265">La valeur de `JwtAudience` doit correspondre *exactement*au nom de votre hôte.</span><span class="sxs-lookup"><span data-stu-id="88d42-265">The value for `JwtAudience` must match the name of your host *exactly*.</span></span> <span data-ttu-id="88d42-266">Vous pouvez utiliser **localhost : 5001** lors du débogage.</span><span class="sxs-lookup"><span data-stu-id="88d42-266">You may use **localhost:5001** while debugging.</span></span> <span data-ttu-id="88d42-267">Toutefois, lorsque vous avez fini de déboguer, veillez à mettre à jour cette valeur sur le nom d’hôte du serveur.</span><span class="sxs-lookup"><span data-stu-id="88d42-267">However, When you're done debugging, make sure to update this value to the server's hostname.</span></span>

- <span data-ttu-id="88d42-268">`TestKeys:Name`.</span><span class="sxs-lookup"><span data-stu-id="88d42-268">`TestKeys:Name`.</span></span> <span data-ttu-id="88d42-269">Entrez un nom pour votre clé.</span><span class="sxs-lookup"><span data-stu-id="88d42-269">Enter a name for your key.</span></span> <span data-ttu-id="88d42-270">Par exemple : `TestKey1`</span><span class="sxs-lookup"><span data-stu-id="88d42-270">For example: `TestKey1`</span></span>
- <span data-ttu-id="88d42-271">`TestKeys:Id`.</span><span class="sxs-lookup"><span data-stu-id="88d42-271">`TestKeys:Id`.</span></span> <span data-ttu-id="88d42-272">Créez un GUID et entrez-le en tant que `TestKeys:ID` valeur.</span><span class="sxs-lookup"><span data-stu-id="88d42-272">Create a GUID and enter it as the `TestKeys:ID` value.</span></span> <span data-ttu-id="88d42-273">Par exemple, `DCE1CC21-FF9B-4424-8FF4-9914BD19A1BE`.</span><span class="sxs-lookup"><span data-stu-id="88d42-273">For example, `DCE1CC21-FF9B-4424-8FF4-9914BD19A1BE`.</span></span> <span data-ttu-id="88d42-274">Vous pouvez utiliser un site comme le [Générateur de GUID en ligne](https://guidgenerator.com/) pour générer un GUID de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="88d42-274">You can use a site like [Online GUID Generator](https://guidgenerator.com/) to randomly generate a GUID.</span></span>

<span data-ttu-id="88d42-275">Cette image indique le format correct pour les paramètres de client et de clé dans **appsettings.jsactivé**.</span><span class="sxs-lookup"><span data-stu-id="88d42-275">This image shows the correct format for tenant and keys settings in **appsettings.json**.</span></span> <span data-ttu-id="88d42-276">`LDAPPath`est configuré pour l’autorisation de rôle.</span><span class="sxs-lookup"><span data-stu-id="88d42-276">`LDAPPath` is configured for role authorization.</span></span>

:::image type="content" source="../media/dke-appsettingsjson-tenantkeysettings.png" alt-text="Indique les paramètres client et clé corrects pour DKE dans le fichier appsettings.js.":::

### <a name="generate-test-keys"></a><span data-ttu-id="88d42-278">Générer des clés de test</span><span class="sxs-lookup"><span data-stu-id="88d42-278">Generate test keys</span></span>

<span data-ttu-id="88d42-279">Une fois que vous avez défini les paramètres de votre application, vous êtes prêt à générer des clés de test publiques et privées.</span><span class="sxs-lookup"><span data-stu-id="88d42-279">Once you have your application settings defined, you're ready to generate public and private test keys.</span></span>

<span data-ttu-id="88d42-280">Pour générer des clés :</span><span class="sxs-lookup"><span data-stu-id="88d42-280">To generate keys:</span></span>

1. <span data-ttu-id="88d42-281">Dans le menu Démarrer de Windows, exécutez l’invite de commandes OpenSSL.</span><span class="sxs-lookup"><span data-stu-id="88d42-281">From the Windows Start menu, run the OpenSSL Command Prompt.</span></span>

1. <span data-ttu-id="88d42-282">Accédez au dossier dans lequel vous souhaitez enregistrer les clés de test.</span><span class="sxs-lookup"><span data-stu-id="88d42-282">Change to the folder where you want to save the test keys.</span></span> <span data-ttu-id="88d42-283">Les fichiers que vous créez en suivant les étapes de cette tâche sont stockés dans le même dossier.</span><span class="sxs-lookup"><span data-stu-id="88d42-283">The files you create by completing the steps in this task are stored in the same folder.</span></span>

1. <span data-ttu-id="88d42-284">Générez la nouvelle clé de test.</span><span class="sxs-lookup"><span data-stu-id="88d42-284">Generate the new test key.</span></span>

   ```dos
   openssl req -x509 -newkey rsa:2048 -keyout key.pem -out cert.pem -days 365
   ```

2. <span data-ttu-id="88d42-285">Générez la clé privée.</span><span class="sxs-lookup"><span data-stu-id="88d42-285">Generate the private key.</span></span>

   ```dos
   openssl rsa -in key.pem -out privkeynopass.pem
   ```

1. <span data-ttu-id="88d42-286">Générez la clé publique.</span><span class="sxs-lookup"><span data-stu-id="88d42-286">Generate the public key.</span></span>

   ```dos
   openssl rsa -in key.pem -pubout > pubkeyonly.pem
   ```

1. <span data-ttu-id="88d42-287">Dans un éditeur de texte, ouvrez **pubkeyonly. pem**.</span><span class="sxs-lookup"><span data-stu-id="88d42-287">In a text editor, open **pubkeyonly.pem**.</span></span> <span data-ttu-id="88d42-288">Copiez tout le contenu du fichier **pubkeyonly. pem** , à l’exception de la première et de la dernière ligne, dans la `PublicPem` section du fichier **appsettings.js** .</span><span class="sxs-lookup"><span data-stu-id="88d42-288">Copy all of the content in the **pubkeyonly.pem** file, except the first and last lines, into the `PublicPem` section of the **appsettings.json** file.</span></span>

1. <span data-ttu-id="88d42-289">Dans un éditeur de texte, ouvrez **privkeynopass. pem**.</span><span class="sxs-lookup"><span data-stu-id="88d42-289">In a text editor, open **privkeynopass.pem**.</span></span> <span data-ttu-id="88d42-290">Copiez tout le contenu du fichier **privkeynopass. pem** , à l’exception de la première et de la dernière ligne, dans la `PrivatePem` section du fichier **appsettings.js** .</span><span class="sxs-lookup"><span data-stu-id="88d42-290">Copy all of the content in the **privkeynopass.pem** file, except the first and last lines, into the `PrivatePem` section of the **appsettings.json** file.</span></span>

1. <span data-ttu-id="88d42-291">Supprimez tous les espaces et lignes de nouvelle ligne dans les `PublicPem` `PrivatePem` sections et.</span><span class="sxs-lookup"><span data-stu-id="88d42-291">Remove all blank spaces and newlines in both the `PublicPem` and `PrivatePem` sections.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="88d42-292">Lorsque vous copiez ce contenu, ne supprimez pas les données du PEM.</span><span class="sxs-lookup"><span data-stu-id="88d42-292">When you copy this content, do not delete any of the PEM data.</span></span>

1. <span data-ttu-id="88d42-293">Dans Visual Studio code, accédez au fichier **Startup.cs** .</span><span class="sxs-lookup"><span data-stu-id="88d42-293">In Visual Studio Code, browse to the **Startup.cs** file.</span></span> <span data-ttu-id="88d42-294">Ce fichier se trouve dans le DoubleKeyEncryptionService référentiel que vous avez cloné localement sous DoubleKeyEncryptionService\src\customer-key-store\.</span><span class="sxs-lookup"><span data-stu-id="88d42-294">This file is located in the DoubleKeyEncryptionService repo you cloned locally under DoubleKeyEncryptionService\src\customer-key-store\.</span></span>

2. <span data-ttu-id="88d42-295">Recherchez les lignes suivantes :</span><span class="sxs-lookup"><span data-stu-id="88d42-295">Locate the following lines:</span></span>

   ```c#
        #if USE_TEST_KEYS
        #error !!!!!!!!!!!!!!!!!!!!!! Use of test keys is only supported for testing,
        DO NOT USE  FOR PRODUCTION !!!!!!!!!!!!!!!!!!!!!!!!!!!!!
        services.AddSingleton<ippw.IKeyStore, ippw.TestKeyStore>();
        #endif
   ```

3. <span data-ttu-id="88d42-296">Remplacez ces lignes par le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="88d42-296">Replace these lines with the following text:</span></span>

   ```csharp
   services.AddSingleton<ippw.IKeyStore, ippw.TestKeyStore>();
   ```

   <span data-ttu-id="88d42-297">Les résultats finaux doivent ressembler à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="88d42-297">The end results should look similar to the following.</span></span>

   :::image type="content" source="../media/dke-startupcs-usetestkeys.png" alt-text="fichier startup.cs pour la préversion publique":::

<span data-ttu-id="88d42-299">Vous êtes maintenant prêt à [créer votre projet DKE](#build-the-project).</span><span class="sxs-lookup"><span data-stu-id="88d42-299">Now you're ready to [build your DKE project](#build-the-project).</span></span>

### <a name="build-the-project"></a><span data-ttu-id="88d42-300">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="88d42-300">Build the project</span></span>

<span data-ttu-id="88d42-301">Suivez les instructions ci-dessous pour générer le projet DKE localement :</span><span class="sxs-lookup"><span data-stu-id="88d42-301">Use the following instructions to build the DKE project locally:</span></span>

1. <span data-ttu-id="88d42-302">Dans Visual Studio code, dans le référentiel du service DKE, sélectionnez **Afficher** la \> **palette de commandes** , puis tapez **générer** à l’invite.</span><span class="sxs-lookup"><span data-stu-id="88d42-302">In Visual Studio Code, in the DKE service repository, select **View** \> **Command Palette** and then type **build** at the prompt.</span></span>

1. <span data-ttu-id="88d42-303">Dans la liste, choisissez **tâches : exécuter la tâche de génération**.</span><span class="sxs-lookup"><span data-stu-id="88d42-303">From the list, choose **Tasks: Run build task**.</span></span>

   <span data-ttu-id="88d42-304">Si aucune tâche de génération n’a été trouvée, sélectionnez **configurer la tâche de génération** et créez-en une pour .net Core comme suit.</span><span class="sxs-lookup"><span data-stu-id="88d42-304">If there are no build tasks found, select **Configure Build Task** and create one for .NET core as follows.</span></span>

   :::image type="content" source="../media/dke-configurebuildtask.png" alt-text="Configurer une tâche de génération manquante pour .NET":::

   1. <span data-ttu-id="88d42-306">Choisissez **create tasks.json from template**.</span><span class="sxs-lookup"><span data-stu-id="88d42-306">Choose **Create tasks.json from template**.</span></span>

   :::image type="content" source="../media/dke-createtasksjsonfromtemplate.png" alt-text="Créer tasks.jssur le fichier à partir du modèle pour DKE":::

   2. <span data-ttu-id="88d42-308">Dans la liste des types de modèles, sélectionnez **.net Core**.</span><span class="sxs-lookup"><span data-stu-id="88d42-308">From the list of template types, select **.NET Core**.</span></span>

   :::image type="content" source="../media/dke-tasksjsontemplate.png" alt-text="Créer tasks.jssur le fichier à partir du modèle pour DKE":::

   3. <span data-ttu-id="88d42-310">Dans la section générer, recherchez le chemin d’accès au fichier **customerkeystore. csproj** .</span><span class="sxs-lookup"><span data-stu-id="88d42-310">In the build section, locate the path to the **customerkeystore.csproj** file.</span></span> <span data-ttu-id="88d42-311">Si ce n’est pas le cas, ajoutez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="88d42-311">If it's not there, add the following line:</span></span>

      ```json
      "${workspaceFolder}/src/customer-key-store/customerkeystore.csproj",
      ```

  4. <span data-ttu-id="88d42-312">Exécutez de nouveau la génération.</span><span class="sxs-lookup"><span data-stu-id="88d42-312">Run the build again.</span></span>

1. <span data-ttu-id="88d42-313">Vérifiez qu’il n’y a pas d’erreurs rouges dans la fenêtre sortie.</span><span class="sxs-lookup"><span data-stu-id="88d42-313">Verify that there are no red errors in the output window.</span></span>

   <span data-ttu-id="88d42-314">S’il y a des erreurs rouges, vérifiez la sortie de la console.</span><span class="sxs-lookup"><span data-stu-id="88d42-314">If there are red errors, check the console output.</span></span> <span data-ttu-id="88d42-315">Assurez-vous que vous avez effectué toutes les étapes précédentes correctement et que les versions de build correctes sont présentes.</span><span class="sxs-lookup"><span data-stu-id="88d42-315">Ensure that you completed all the previous steps correctly and the correct build versions are present.</span></span>

2. <span data-ttu-id="88d42-316">Sélectionnez **exécuter** \> **Démarrer le débogage** pour déboguer le processus.</span><span class="sxs-lookup"><span data-stu-id="88d42-316">Select **Run** \> **Start Debugging** to debug the process.</span></span> <span data-ttu-id="88d42-317">Si vous êtes invité à sélectionner un environnement, sélectionnez **.net Core**.</span><span class="sxs-lookup"><span data-stu-id="88d42-317">If you're prompted to select an environment, select **.NET core**.</span></span>

<span data-ttu-id="88d42-318">Le débogueur .net Core lance généralement vers' ' ' https://localhost:5001 `. To view your test key, go to ` https://localhost:5001 et ajoute une barre oblique (/) et le nom de votre clé.</span><span class="sxs-lookup"><span data-stu-id="88d42-318">The .NET core debugger typically launches to \`\`https://localhost:5001`. To view your test key, go to `https://localhost:5001\` and append a forward slash (/) and the name of your key.</span></span> <span data-ttu-id="88d42-319">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88d42-319">For example:</span></span>

```https
https://localhost:5001/TestKey1
```

<span data-ttu-id="88d42-320">La clé doit s’afficher au format JSON.</span><span class="sxs-lookup"><span data-stu-id="88d42-320">The key should display in JSON format.</span></span>

<span data-ttu-id="88d42-321">Votre installation est maintenant terminée.</span><span class="sxs-lookup"><span data-stu-id="88d42-321">Your setup is now complete.</span></span> <span data-ttu-id="88d42-322">Avant de publier le keystore, dans appsettings.jsactivé, pour le paramètre JwtAudience, vérifiez que la valeur de hostname correspond exactement au nom de l’hôte de service de l’application.</span><span class="sxs-lookup"><span data-stu-id="88d42-322">Before you publish the keystore, in appsettings.json, for the JwtAudience setting, ensure the value for hostname exactly matches your App Service host name.</span></span> <span data-ttu-id="88d42-323">Vous pouvez l’avoir remplacée par localhost pour dépanner la Build.</span><span class="sxs-lookup"><span data-stu-id="88d42-323">You may have changed it to localhost to troubleshoot the build.</span></span>

### <a name="publish-the-key-store"></a><span data-ttu-id="88d42-324">Publier le magasin de clés</span><span class="sxs-lookup"><span data-stu-id="88d42-324">Publish the key store</span></span>

<span data-ttu-id="88d42-325">Pour publier le magasin de clés, vous allez créer une instance de service d’application Azure pour héberger votre déploiement DKE.</span><span class="sxs-lookup"><span data-stu-id="88d42-325">To publish the key store, you'll create an Azure App Service instance to host your DKE deployment.</span></span> <span data-ttu-id="88d42-326">Ensuite, vous allez publier vos clés générées dans Azure.</span><span class="sxs-lookup"><span data-stu-id="88d42-326">Next, you'll publish your generated keys to Azure.</span></span>

<span data-ttu-id="88d42-327">**Pour créer une instance Azure Web App afin d’héberger votre déploiement DKE**</span><span class="sxs-lookup"><span data-stu-id="88d42-327">**To create an Azure Web App instance to host your DKE deployment**</span></span>

1. <span data-ttu-id="88d42-328">Dans votre navigateur, connectez-vous au [portail Microsoft Azure](https://ms.portal.azure.com)et accédez à **app services**  >  **Add**.</span><span class="sxs-lookup"><span data-stu-id="88d42-328">In your browser, sign in to the [Microsoft Azure portal](https://ms.portal.azure.com), and go to **App Services** > **Add**.</span></span>

1. <span data-ttu-id="88d42-329">Sélectionnez votre abonnement et le groupe de ressources, puis définissez les détails de votre instance.</span><span class="sxs-lookup"><span data-stu-id="88d42-329">Select your subscription and resource group and define your instance details.</span></span>

    - <span data-ttu-id="88d42-330">Entrez le nom d’hôte de l’ordinateur sur lequel vous souhaitez installer le service DKE.</span><span class="sxs-lookup"><span data-stu-id="88d42-330">Enter the hostname of the computer where you want to install the DKE service.</span></span> <span data-ttu-id="88d42-331">Assurez-vous qu’il s’agit du même nom que celui défini pour le paramètre JwtAudience dans le fichier [**appsettings.js**](#tenant-and-key-settings) .</span><span class="sxs-lookup"><span data-stu-id="88d42-331">Make sure it's the same name as the one defined for the JwtAudience setting in the [**appsettings.json**](#tenant-and-key-settings) file.</span></span> <span data-ttu-id="88d42-332">La valeur que vous fournissez pour le nom est également WebAppInstanceName.</span><span class="sxs-lookup"><span data-stu-id="88d42-332">The value you provide for the name is also the WebAppInstanceName.</span></span>

    - <span data-ttu-id="88d42-333">Pour **publier**, sélectionner le **code**et pour la **pile Runtime**, sélectionnez **.net Core 3,1**.</span><span class="sxs-lookup"><span data-stu-id="88d42-333">For **Publish**, select **code**, and for **Runtime stack**, select **.NET Core 3.1**.</span></span>

    <span data-ttu-id="88d42-334">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88d42-334">For example:</span></span>

    :::image type="content" source="../media/dke-azure-add-app-service.png" alt-text="Ajouter votre service d’application":::

1. <span data-ttu-id="88d42-336">Au bas de la page, sélectionnez **révision + créer**, puis **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="88d42-336">At the bottom of the page, select **Review + create**, and then select **Add**.</span></span>

1. <span data-ttu-id="88d42-337">Effectuez l’une des opérations suivantes pour publier vos clés générées dans Azure :</span><span class="sxs-lookup"><span data-stu-id="88d42-337">Do one of the following to publish your generated keys to Azure:</span></span>

    - [<span data-ttu-id="88d42-338">Publier via ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="88d42-338">Publish via ZipDeployUI</span></span>](#publish-via-zipdeployui)
    - [<span data-ttu-id="88d42-339">Publier via FTP</span><span class="sxs-lookup"><span data-stu-id="88d42-339">Publish via FTP</span></span>](#publish-via-ftp)
    - [<span data-ttu-id="88d42-340">Publier via Visual Studio 2019 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="88d42-340">Publish via Visual Studio 2019 or later</span></span>](https://docs.microsoft.com/aspnet/core/tutorials/)
    - [<span data-ttu-id="88d42-341">Publier sur un système local</span><span class="sxs-lookup"><span data-stu-id="88d42-341">Publish to an on-premises system</span></span>](https://docs.microsoft.com/aspnet/core/tutorials/publish-to-iis?view=aspnetcore-3.1&tabs=netcore-cli)

    > [!NOTE]
    > <span data-ttu-id="88d42-342">Vous pouvez préférer d’autres méthodes de déploiement de vos clés.</span><span class="sxs-lookup"><span data-stu-id="88d42-342">You may prefer other methods to deploy your keys.</span></span> <span data-ttu-id="88d42-343">Sélectionnez la méthode qui convient le mieux à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="88d42-343">Select the method that works best for your organization.</span></span>

    > [!TIP]
    > <span data-ttu-id="88d42-344">La [publication via Visual Studio](https://docs.microsoft.com/aspnet/core/tutorials/) et un [système local](https://docs.microsoft.com/aspnet/core/tutorials/publish-to-iis?view=aspnetcore-3.1&tabs=netcore-cli) est décrite dans la [documentation ASP.net](https://docs.microsoft.com/aspnet/core/).</span><span class="sxs-lookup"><span data-stu-id="88d42-344">[Publishing via Visual Studio](https://docs.microsoft.com/aspnet/core/tutorials/) and to an [on-premises system](https://docs.microsoft.com/aspnet/core/tutorials/publish-to-iis?view=aspnetcore-3.1&tabs=netcore-cli) is described in the [ASP .NET documentation](https://docs.microsoft.com/aspnet/core/).</span></span> <span data-ttu-id="88d42-345">Si vous utilisez l’une de ces méthodes, ouvrez les instructions dans un onglet distinct afin de pouvoir revenir rapidement une fois que vous avez fini.</span><span class="sxs-lookup"><span data-stu-id="88d42-345">If you use one of these methods, open the instructions in a separate tab so that you can return here easily when you're done.</span></span>

#### <a name="publish-via-zipdeployui"></a><span data-ttu-id="88d42-346">Publier via ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="88d42-346">Publish via ZipDeployUI</span></span>

1. <span data-ttu-id="88d42-347">Accédez à `https://<WebAppInstanceName>.scm.azurewebsites.net/ZipDeployUI`.</span><span class="sxs-lookup"><span data-stu-id="88d42-347">Go to `https://<WebAppInstanceName>.scm.azurewebsites.net/ZipDeployUI`.</span></span>

    <span data-ttu-id="88d42-348">Par exemple : https://customerkeystoreforpublicpreview.scm.azurewebsites.net/ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="88d42-348">For example: https://customerkeystoreforpublicpreview.scm.azurewebsites.net/ZipDeployUI</span></span>

1. <span data-ttu-id="88d42-349">Dans la base de code pour le magasin de clés, accédez au dossier **Customer-Key-store\src\customer-Key-Store** et vérifiez que ce dossier contient le fichier **customerkeystore. csproj** .</span><span class="sxs-lookup"><span data-stu-id="88d42-349">In the codebase for the key store, go to the **customer-key-store\src\customer-key-store** folder, and verify that this folder contains the **customerkeystore.csproj** file.</span></span>

1. <span data-ttu-id="88d42-350">Exécuter : **publication dotnet**</span><span class="sxs-lookup"><span data-stu-id="88d42-350">Run: **dotnet publish**</span></span>

     <span data-ttu-id="88d42-351">La fenêtre sortie affiche le répertoire dans lequel la publication a été déployée.</span><span class="sxs-lookup"><span data-stu-id="88d42-351">The output window displays the directory where the publish was deployed.</span></span>

    <span data-ttu-id="88d42-352">Par exemple : `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span><span class="sxs-lookup"><span data-stu-id="88d42-352">For example: `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span></span>

1. <span data-ttu-id="88d42-353">Envoyez tous les fichiers du répertoire de publication dans un fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="88d42-353">Send all files in the publish directory to a .zip file.</span></span> <span data-ttu-id="88d42-354">Lors de la création du fichier. zip, assurez-vous que tous les fichiers du répertoire sont au niveau racine du fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="88d42-354">When creating the .zip file, make sure that all files in the directory are at the root level of the .zip file.</span></span>

1. <span data-ttu-id="88d42-355">Faites glisser et déposez le fichier. zip que vous créez sur le site ZipDeployUI que vous avez ouvert ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="88d42-355">Drag and drop the .zip file you create to the ZipDeployUI site you opened above.</span></span> <span data-ttu-id="88d42-356">Par exemple : https://customerkeystoreforpublicpreview.scm.azurewebsites.net/ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="88d42-356">For example: https://customerkeystoreforpublicpreview.scm.azurewebsites.net/ZipDeployUI</span></span>

<span data-ttu-id="88d42-357">DKE est déployé et vous pouvez accéder aux clés de test que vous avez créées.</span><span class="sxs-lookup"><span data-stu-id="88d42-357">DKE is deployed and you can browse to the test keys you've created.</span></span> <span data-ttu-id="88d42-358">Poursuivez [la validation de votre déploiement](#validate-your-deployment) ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="88d42-358">Continue to [Validate your deployment](#validate-your-deployment) below.</span></span>

#### <a name="publish-via-ftp"></a><span data-ttu-id="88d42-359">Publier via FTP</span><span class="sxs-lookup"><span data-stu-id="88d42-359">Publish via FTP</span></span>

1. <span data-ttu-id="88d42-360">Connectez-vous au service d’application que vous avez créé [ci-dessus](#publish-the-key-store).</span><span class="sxs-lookup"><span data-stu-id="88d42-360">Connect to the App Service you created [above](#publish-the-key-store).</span></span>

    <span data-ttu-id="88d42-361">Dans votre navigateur, accédez à : **Azure portal**  >  **App Service**  >  **Centre de déploiement**de  >  **déploiement manuel**  >  **FTP**  >  **Dashboard**du centre de déploiement Azure Portal App.</span><span class="sxs-lookup"><span data-stu-id="88d42-361">In your browser, go to: **Azure portal** > **App Service** > **Deployment Center** > **Manual Deployment** > **FTP** > **Dashboard**.</span></span>

1. <span data-ttu-id="88d42-362">Copiez les chaînes de connexion affichées dans un fichier local.</span><span class="sxs-lookup"><span data-stu-id="88d42-362">Copy the connection strings displayed to a local file.</span></span> <span data-ttu-id="88d42-363">Vous utiliserez ces chaînes pour vous connecter au service d’application Web et télécharger des fichiers via FTP.</span><span class="sxs-lookup"><span data-stu-id="88d42-363">You'll use these strings to connect to the Web App Service and upload files via FTP.</span></span>

    <span data-ttu-id="88d42-364">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88d42-364">For example:</span></span>

    :::image type="content" source="../media/dke-ftp-dashboard.png" alt-text="Copier des chaînes de connexion à partir du tableau de bord FTP":::

1. <span data-ttu-id="88d42-366">Dans la base de code pour le stockage de clés, accédez au **répertoire Customer-Key-store\src\customer-Key-Store**</span><span class="sxs-lookup"><span data-stu-id="88d42-366">In the codebase for the key storage, go to the **customer-key-store\src\customer-key-store directory**.</span></span>

1. <span data-ttu-id="88d42-367">Vérifiez que ce répertoire contient le fichier **customerkeystore. csproj** .</span><span class="sxs-lookup"><span data-stu-id="88d42-367">Verify that this directory contains the **customerkeystore.csproj** file.</span></span>

1. <span data-ttu-id="88d42-368">Exécuter : **publication dotnet**</span><span class="sxs-lookup"><span data-stu-id="88d42-368">Run: **dotnet publish**</span></span>

    <span data-ttu-id="88d42-369">La sortie contient le répertoire dans lequel la publication a été déployée.</span><span class="sxs-lookup"><span data-stu-id="88d42-369">The output contains the directory where the publish was deployed.</span></span>

    <span data-ttu-id="88d42-370">Par exemple : `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span><span class="sxs-lookup"><span data-stu-id="88d42-370">For example: `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span></span>

1. <span data-ttu-id="88d42-371">Envoyez tous les fichiers du répertoire de publication dans un fichier zip.</span><span class="sxs-lookup"><span data-stu-id="88d42-371">Send all files in the publish directory to a zip file.</span></span> <span data-ttu-id="88d42-372">Lors de la création du fichier. zip, assurez-vous que tous les fichiers du répertoire sont au niveau racine du fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="88d42-372">When creating the .zip file, make sure that all files in the directory are at the root level of the .zip file.</span></span>

1. <span data-ttu-id="88d42-373">À partir de votre client FTP, utilisez les informations de connexion que vous avez copiées pour vous connecter à votre service d’application.</span><span class="sxs-lookup"><span data-stu-id="88d42-373">From your FTP client, use the connection information you copied to connect to your App Service.</span></span> <span data-ttu-id="88d42-374">Téléchargez le fichier. zip que vous avez créé à l’étape précédente dans le répertoire racine de votre application Web.</span><span class="sxs-lookup"><span data-stu-id="88d42-374">Upload the .zip file you created in the previous step to the root directory of your Web App.</span></span>

<span data-ttu-id="88d42-375">DKE est déployé et vous pouvez accéder aux clés de test que vous auriez créées.</span><span class="sxs-lookup"><span data-stu-id="88d42-375">DKE is deployed and you can browse to the test keys you'd created.</span></span> <span data-ttu-id="88d42-376">Ensuite, [validez votre déploiement](#validate-your-deployment).</span><span class="sxs-lookup"><span data-stu-id="88d42-376">Next, [Validate your deployment](#validate-your-deployment).</span></span>

### <a name="validate-your-deployment"></a><span data-ttu-id="88d42-377">Valider votre déploiement</span><span class="sxs-lookup"><span data-stu-id="88d42-377">Validate your deployment</span></span>

<span data-ttu-id="88d42-378">Après avoir déployé DKE à l’aide de l’une des méthodes décrites ci-dessus, validez les principaux paramètres de déploiement et de magasin de clés.</span><span class="sxs-lookup"><span data-stu-id="88d42-378">After deploying DKE using one of the methods described above, validate the deployment and the key store settings.</span></span>

<span data-ttu-id="88d42-379">Générer</span><span class="sxs-lookup"><span data-stu-id="88d42-379">Run:</span></span>

<span data-ttu-id="88d42-380">src\customer-key-store\scripts\key_store_tester.ps1 mykeystoreurl/MyKey</span><span class="sxs-lookup"><span data-stu-id="88d42-380">src\customer-key-store\scripts\key_store_tester.ps1 mykeystoreurl/mykey</span></span>

<span data-ttu-id="88d42-381">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88d42-381">For example:</span></span>

<span data-ttu-id="88d42-382">key_store_tester.ps1https://mycustomerkeystore.com/mykey</span><span class="sxs-lookup"><span data-stu-id="88d42-382">key_store_tester.ps1 https://mycustomerkeystore.com/mykey</span></span>

<span data-ttu-id="88d42-383">Assurez-vous qu’aucune erreur ne s’affiche dans la sortie.</span><span class="sxs-lookup"><span data-stu-id="88d42-383">Ensure that no errors appear in the output.</span></span> <span data-ttu-id="88d42-384">Lorsque vous êtes prêt, [Enregistrez votre magasin de clés](#register-your-key-store).</span><span class="sxs-lookup"><span data-stu-id="88d42-384">When you're ready, [register your key store](#register-your-key-store).</span></span>

## <a name="register-your-key-store"></a><span data-ttu-id="88d42-385">Enregistrer votre magasin de clés</span><span class="sxs-lookup"><span data-stu-id="88d42-385">Register your key store</span></span>

<span data-ttu-id="88d42-386">Les étapes suivantes vous permettent d’enregistrer votre magasin de clés.</span><span class="sxs-lookup"><span data-stu-id="88d42-386">The following steps enable you to register your key store.</span></span> <span data-ttu-id="88d42-387">L’inscription de votre magasin de clés est la dernière étape du déploiement d’DKE avant de commencer à créer des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="88d42-387">Registering your key store is the last step in deploying DKE before you can start creating labels.</span></span>

<span data-ttu-id="88d42-388">Pour enregistrer votre magasin de clés :</span><span class="sxs-lookup"><span data-stu-id="88d42-388">To register your key store:</span></span>

1. <span data-ttu-id="88d42-389">Dans votre navigateur, ouvrez le [portail Microsoft Azure](https://ms.portal.azure.com/), puis accédez à **toutes les** \> **Identity** \> **inscriptions des applications d'** identité des services.</span><span class="sxs-lookup"><span data-stu-id="88d42-389">In your browser, open the [Microsoft Azure portal](https://ms.portal.azure.com/), and go to **All Services** \> **Identity** \> **App Registrations**.</span></span>

2. <span data-ttu-id="88d42-390">Sélectionnez **nouvelle inscription**, puis entrez un nom explicite.</span><span class="sxs-lookup"><span data-stu-id="88d42-390">Select **New registration**, and enter a meaningful name.</span></span>

3. <span data-ttu-id="88d42-391">Sélectionnez un type de compte parmi les options affichées.</span><span class="sxs-lookup"><span data-stu-id="88d42-391">Select an account type from the options displayed.</span></span>

    <span data-ttu-id="88d42-392">Si vous utilisez Microsoft Azure avec un domaine non personnalisé, tel que **onmicrosoft.com**, sélectionnez **comptes dans cet annuaire d’organisation uniquement (Microsoft uniquement-client unique).**</span><span class="sxs-lookup"><span data-stu-id="88d42-392">If you're using Microsoft Azure with a non-custom domain, such as **onmicrosoft.com**, select **Accounts in this organizational directory only (Microsoft only - Single tenant).**</span></span>

    <span data-ttu-id="88d42-393">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88d42-393">For example:</span></span>

    :::image type="content" source="../media/dke-app-registration.png" alt-text="Inscription de l’application":::

4. <span data-ttu-id="88d42-395">Au bas de la page, sélectionnez **Enregistrer** pour créer la nouvelle inscription de l’application.</span><span class="sxs-lookup"><span data-stu-id="88d42-395">At the bottom of the page, select **Register** to create the new App Registration.</span></span>

5. <span data-ttu-id="88d42-396">Dans la nouvelle inscription de l’application, dans le volet gauche, sous **gérer**, sélectionnez **authentification**.</span><span class="sxs-lookup"><span data-stu-id="88d42-396">In your new App Registration, in the left pane, under **Manage**, select **Authentication**.</span></span>

6. <span data-ttu-id="88d42-397">Sélectionnez **Ajouter une plateforme**.</span><span class="sxs-lookup"><span data-stu-id="88d42-397">Select **Add a platform**.</span></span>
 
7. <span data-ttu-id="88d42-398">Dans la fenêtre contextuelle **configurer les plateformes** , sélectionnez **Web**.</span><span class="sxs-lookup"><span data-stu-id="88d42-398">On the **Configure platforms** popup, select **Web**.</span></span>
 
8. <span data-ttu-id="88d42-399">Sous **URI de redirection**, entrez l’URI de votre service de chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="88d42-399">Under **Redirect URIs**, enter the URI of your double key encryption service.</span></span> <span data-ttu-id="88d42-400">Entrez l’URL du service d’application, y compris le nom d’hôte et le domaine.</span><span class="sxs-lookup"><span data-stu-id="88d42-400">Enter the App Service URL, including both the hostname and domain.</span></span>

    <span data-ttu-id="88d42-401">Par exemple : https://mycustomerkeystoretest.com</span><span class="sxs-lookup"><span data-stu-id="88d42-401">For example: https://mycustomerkeystoretest.com</span></span>

    - <span data-ttu-id="88d42-402">L’URL que vous entrez doit correspondre au nom d’hôte dans lequel votre magasin de clés est déployé.</span><span class="sxs-lookup"><span data-stu-id="88d42-402">The URL you enter must match the hostname where your key store is deployed.</span></span>
    - <span data-ttu-id="88d42-403">Si vous testez localement avec Visual Studio, utilisez **https://localhost:5001** .</span><span class="sxs-lookup"><span data-stu-id="88d42-403">If you're testing locally with Visual Studio, use **https://localhost:5001**.</span></span>
    - <span data-ttu-id="88d42-404">Dans tous les cas, le modèle doit être **https**.</span><span class="sxs-lookup"><span data-stu-id="88d42-404">In all cases, the scheme must be **https**.</span></span>

    <span data-ttu-id="88d42-405">Vérifiez que le nom d’hôte correspond exactement au nom de l’hôte de service de l’application.</span><span class="sxs-lookup"><span data-stu-id="88d42-405">Ensure the hostname exactly matches your App Service host name.</span></span> <span data-ttu-id="88d42-406">Vous pouvez l’avoir modifié sur `localhost` pour dépanner la Build.</span><span class="sxs-lookup"><span data-stu-id="88d42-406">You may have changed it to `localhost` to troubleshoot the build.</span></span> <span data-ttu-id="88d42-407">Dans **appsettings.jsactivé**, cette valeur est le nom d’hôte que vous avez défini pour `JwtAudience` .</span><span class="sxs-lookup"><span data-stu-id="88d42-407">In **appsettings.json**, this value is the hostname you set for `JwtAudience`.</span></span>

6. <span data-ttu-id="88d42-408">Sous **attribution implicite**, activez la case à cocher **jetons d’ID** .</span><span class="sxs-lookup"><span data-stu-id="88d42-408">Under **Implicit grant**, select the **ID tokens** checkbox.</span></span>

1. <span data-ttu-id="88d42-409">Sélectionnez **Enregistrer** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="88d42-409">Select **Save** to save your changes.</span></span>

7. <span data-ttu-id="88d42-410">Dans le volet de gauche, sélectionnez **exposer une API**, puis en regard de l’ID d’application URI, sélectionnez **Set**.</span><span class="sxs-lookup"><span data-stu-id="88d42-410">On the left pane, select **Expose an API**, then next to Application ID URI, select **Set**.</span></span>

9. <span data-ttu-id="88d42-411">Toujours sur la page **exposer une API** , dans la zone **étendues définies par cette API** , sélectionnez **Ajouter une étendue**.</span><span class="sxs-lookup"><span data-stu-id="88d42-411">Still on the **Expose an API** page, in the **Scopes defined by this API** area, select **Add a scope**.</span></span> <span data-ttu-id="88d42-412">Dans la nouvelle étendue :</span><span class="sxs-lookup"><span data-stu-id="88d42-412">In the new scope:</span></span>

    1. <span data-ttu-id="88d42-413">Définissez le nom de l’étendue en tant que **user_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="88d42-413">Define the scope name as **user_impersonation**.</span></span>

    2. <span data-ttu-id="88d42-414">Sélectionnez les administrateurs et les utilisateurs qui peuvent consentir.</span><span class="sxs-lookup"><span data-stu-id="88d42-414">Select the administrators and users who can consent.</span></span>

    3. <span data-ttu-id="88d42-415">Définissez les valeurs restantes requises.</span><span class="sxs-lookup"><span data-stu-id="88d42-415">Define any remaining values required.</span></span>

    4. <span data-ttu-id="88d42-416">Sélectionnez **Ajouter une étendue.**</span><span class="sxs-lookup"><span data-stu-id="88d42-416">Select **Add scope.**</span></span>

    <span data-ttu-id="88d42-417">Sélectionnez **Enregistrer** dans la partie supérieure pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="88d42-417">Select **Save** at the top to save your changes.</span></span>

10. <span data-ttu-id="88d42-418">Toujours sur la page **exposer une API** , dans la zone **applications clientes autorisées** , sélectionnez **Ajouter une application cliente**.</span><span class="sxs-lookup"><span data-stu-id="88d42-418">Still on the **Expose an API** page, in the **Authorized client applications** area, select **Add a client application**.</span></span>

    <span data-ttu-id="88d42-419">Dans la nouvelle application cliente :</span><span class="sxs-lookup"><span data-stu-id="88d42-419">In the new client application:</span></span>

    1. <span data-ttu-id="88d42-420">Définissez l’ID client comme **d3590ed6-52b3-4102-Aeff-aad2292ab01c**.</span><span class="sxs-lookup"><span data-stu-id="88d42-420">Define the Client ID as **d3590ed6-52b3-4102-aeff-aad2292ab01c**.</span></span> <span data-ttu-id="88d42-421">Cette valeur est l’ID client Microsoft Office et permet à Office d’obtenir un jeton d’accès pour votre magasin de clés.</span><span class="sxs-lookup"><span data-stu-id="88d42-421">This value is the Microsoft Office client ID, and enables Office to obtain an access token for your key store.</span></span>

    2. <span data-ttu-id="88d42-422">Sous **étendues autorisées**, sélectionnez l’étendue **user_impersonation** .</span><span class="sxs-lookup"><span data-stu-id="88d42-422">Under **Authorized scopes**, select the **user_impersonation** scope.</span></span>

    3. <span data-ttu-id="88d42-423">Sélectionnez **Ajouter une application**.</span><span class="sxs-lookup"><span data-stu-id="88d42-423">Select **Add application**.</span></span>

    4. <span data-ttu-id="88d42-424">Sélectionnez **Enregistrer** dans la partie supérieure pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="88d42-424">Select **Save** at the top to save your changes.</span></span>

<span data-ttu-id="88d42-425">Votre magasin de clés DKE est maintenant enregistré.</span><span class="sxs-lookup"><span data-stu-id="88d42-425">Your DKE key store is now registered.</span></span> <span data-ttu-id="88d42-426">Continuez en [créant des étiquettes à l’aide de DKE](#create-labels-using-dke).</span><span class="sxs-lookup"><span data-stu-id="88d42-426">Continue by [creating labels using DKE](#create-labels-using-dke).</span></span>

## <a name="create-labels-using-dke"></a><span data-ttu-id="88d42-427">Créer des étiquettes à l’aide de DKE</span><span class="sxs-lookup"><span data-stu-id="88d42-427">Create labels using DKE</span></span>

<span data-ttu-id="88d42-428">Dans le centre de conformité Microsoft 365, créez une étiquette de sensibilité et appliquez le chiffrement comme vous le feriez autrement.</span><span class="sxs-lookup"><span data-stu-id="88d42-428">In the Microsoft 365 compliance center, create a new sensitivity label and apply encryption as you would otherwise.</span></span> <span data-ttu-id="88d42-429">Sélectionnez **utiliser le chiffrement à double clé** et entrez l’URL du point de terminaison de votre clé.</span><span class="sxs-lookup"><span data-stu-id="88d42-429">Select **Use Double Key Encryption** and enter the endpoint URL for your key.</span></span>

<span data-ttu-id="88d42-430">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="88d42-430">For example:</span></span>

:::image type="content" source="../media/dke-use-dke.png" alt-text="Sélectionnez utiliser le chiffrement à double clé dans le centre de conformité Microsoft 365":::

<span data-ttu-id="88d42-432">Toutes les étiquettes DKE que vous ajoutez commencent à apparaître pour les utilisateurs dans les versions les plus récentes des applications Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="88d42-432">Any DKE labels you add will start appearing for users in the latest versions of Microsoft 365 Apps for enterprise.</span></span>

> [!NOTE]
> <span data-ttu-id="88d42-433">L’actualisation des clients avec les nouvelles étiquettes peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="88d42-433">It may take up to 24 hours for the clients to refresh with the new labels.</span></span>

### <a name="enable-dke-in-your-client"></a><span data-ttu-id="88d42-434">Activer DKE dans votre client</span><span class="sxs-lookup"><span data-stu-id="88d42-434">Enable DKE in your client</span></span>

<span data-ttu-id="88d42-435">Si vos étiquettes DKE n’apparaissent pas sous le ruban de sensibilité dans Microsoft Office, il se peut que DKE ne soit pas activé pour votre client.</span><span class="sxs-lookup"><span data-stu-id="88d42-435">If your DKE labels don't appear under the Sensitivity ribbon in Microsoft Office, your client may not have DKE enabled.</span></span>

<span data-ttu-id="88d42-436">Activez DKE pour votre client en ajoutant les clés de Registre suivantes :</span><span class="sxs-lookup"><span data-stu-id="88d42-436">Enable DKE for your client by adding the following registry keys:</span></span>

```ini
    [HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\MSIPC\flighting]
    "DoubleKeyProtection"=dword:00000001

    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\flighting]
    "DoubleKeyProtection"=dword:00000001
```
